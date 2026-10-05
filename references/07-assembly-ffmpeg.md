# Giai đoạn 7 — Dựng Phim Bằng FFmpeg & Hậu Kỳ Tự Động

## Mục đích
Nối các clip 8 giây thành video dọc 9:16 (Shorts/TikTok/Reels) hoàn chỉnh, ghép nối liền mạch không lộ vết cắt (Zero-Transition), lồng ghép giọng đọc nữ chuẩn timecode và nhạc nền piano cafe sâu lắng.

---

## 1. Chuẩn Hóa Video Về 1080x1920 @ 24fps

```bash
ffmpeg -i clip_01.mp4 -vf "scale=1080:1920:force_original_aspect_ratio=decrease,pad=1080:1920:(ow-iw)/2:(oh-ih)/2,fps=24" -c:v libx264 -preset slow -crf 18 -pix_fmt yuv420p -an norm_01.mp4
```

---

## 2. Nối Các Cảnh Liền Mạch (Concat Demuxer)

Tạo file `inputs.txt`:
```text
file 'norm_01.mp4'
file 'norm_02.mp4'
file 'norm_03.mp4'
file 'norm_04.mp4'
file 'norm_05.mp4'
file 'norm_06.mp4'
file 'norm_07.mp4'
file 'norm_08.mp4'
```

Chạy lệnh ghép nối không nén lại:
```bash
ffmpeg -f concat -safe 0 -i inputs.txt -c copy video_merged.mp4
```

---

## 3. Lồng Ghép Giọng Đọc (VO) Theo Timecode Phân Cảnh

Giọng đọc bắt đầu sau $0.8\text{s}$ ($800\text{ ms}$) ở mỗi phân cảnh:
- Cảnh 1: `adelay=800|800`
- Cảnh 2: `adelay=8800|8800`
- Cảnh 3: `adelay=16800|16800`
- Cảnh 4: `adelay=24800|24800`
- Cảnh 5: `adelay=32800|32800`
- Cảnh 6: `adelay=40800|40800`
- Cảnh 7: `adelay=48800|48800`
- Cảnh 8: `adelay=56800|56800`

```bash
ffmpeg -i video_merged.mp4 \
  -i audio_01.mp3 -i audio_02.mp3 -i audio_03.mp3 -i audio_04.mp3 \
  -i audio_05.mp3 -i audio_06.mp3 -i audio_07.mp3 -i audio_08.mp3 \
  -filter_complex "\
    [1:a]adelay=800|800[a1]; \
    [2:a]adelay=8800|8800[a2]; \
    [3:a]adelay=16800|16800[a3]; \
    [4:a]adelay=24800|24800[a4]; \
    [5:a]adelay=32800|32800[a5]; \
    [6:a]adelay=40800|40800[a6]; \
    [7:a]adelay=48800|48800[a7]; \
    [8:a]adelay=56800|56800[a8]; \
    [a1][a2][a3][a4][a5][a6][a7][a8]amix=inputs=8:normalize=0[vo_mix]" \
  -map 0:v -map "[vo_mix]" -c:v copy -c:a aac -b:a 192k final_with_vo.mp4
```

---

## 4. Hòa Âm Nhạc Nền Piano Cafe & Tiếng Mưa

```bash
ffmpeg -i final_with_vo.mp4 -i bgm_piano_rain.mp3 \
  -filter_complex "\
    [1:a]volume=0.18[bgm]; \
    [0:a][bgm]amix=inputs=2:duration=first:dropout_transition=2[aout]" \
  -map 0:v -map "[aout]" -c:v copy -c:a aac -b:a 192k final_master.mp4
```

---

## Checklist Kiểm Định Giai Đoạn 7
- [ ] Clip hoàn chỉnh 64s, độ phân giải 1080x1920 chuẩn 24fps.
- [ ] Chuyển tiếp giữa các cảnh hoàn toàn tự nhiên, không giật hình.
- [ ] Giọng đọc khớp chính xác, âm thanh tiếng mưa và nhạc piano hòa quyện tinh tế.
