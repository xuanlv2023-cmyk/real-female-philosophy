# Giai đoạn 5 — Quy Chuẩn Tạo Video AI & An Toàn Kiểm Duyệt

## Mục đích
Thiết lập các thông số render trên các công cụ sinh video AI (Kling 1.5, Runway Gen-3, Hailuo, Muse), đảm bảo tính chân thật người thật 100%, an toàn kiểm duyệt hình ảnh và kiểm định kỹ thuật bằng `ffprobe`.

---

## 1. Kiểm Soát An Toàn Kiểm Duyệt Hình Ảnh (NSFW Safety)

- **Phong cách quyến rũ điện ảnh thanh lịch:** Mục tiêu là sự cuốn hút tự nhiên qua xương quai xanh thanh tú, đường viền cổ trang nhã và ánh mắt sâu thẳm.
- **Quy tắc an toàn:**
  - Áo sơ mi hoặc đầm mở cổ ở mức độ vừa phải, trang nhã.
  - Tuyệt đối KHÔNG sử dụng các từ khóa nhạy cảm kích hoạt bộ lọc NSFW của AI (như *cleavage, provocative, sexy, busty*).
  - ✅ **Dùng cụm từ an toàn điện ảnh:** `Tasteful elegant neckline, bare collarbone, serene sophisticated presence, classy natural beauty`.

---

## 2. Phòng Chống Rò Rỉ Token Thiết Bị (Zero Token Bleed)

- Tuyệt đối **CẤM** các từ: `tripod, camera operator, rig, studio lighting, selfie stick`.
- Sử dụng cụm từ cố định: `Stationary hands-free mounted camera, eye-level candid view`.

---

## 3. Kiểm Định Kỹ Thuật Bằng FFprobe

```bash
ffprobe -v error -select_streams v:0 \
  -show_entries stream=width,height,r_frame_rate,duration \
  -of default=noprint_wrappers=1 <clip_name>.mp4
```

### Tiêu Chuẩn Phê Duyệt:
1. Độ phân giải đạt chuẩn 9:16 (`720x1280` hoặc `1080x1920`).
2. Thời lượng ~8.0s ($\pm 0.2s$).
3. Tốc độ khung hình 24 fps.
4. Gương mặt và đôi mắt chuyển động tự nhiên, không bị biến dạng ngón tay khi cầm tách cà phê.

---

## Checklist Kiểm Định Giai Đoạn 5
- [ ] Render trọn bộ các cảnh với First Frame & Last Frame.
- [ ] Hình ảnh đạt chuẩn quyến rũ thanh lịch, 100% an toàn kiểm duyệt AI.
- [ ] Không rò rỉ chân máy hay biểu tượng lạ trên màn hình.
- [ ] Đã verify thông số bằng `ffprobe`.
