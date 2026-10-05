# Giai đoạn 4 — Mega Prompts 8s Zero-Transition (Nữ Tri Thức)

## Mục đích
Soạn thảo Mega Prompts 8 giây cho từng phân cảnh của video Nữ tri thức, tuân thủ nguyên lý **Single Continuous Unbroken Take** (cú máy đơn liên tục, không chia timeline) để video mượt mà, sắc nét, và **kế thừa chính xác 100% Token trang phục và bối cảnh động** đã xác định ở Giai đoạn 1.

---

## 1. Global Locks Chuẩn Hóa Với Khóa Góc Máy MCU & Token Động (Dán Trong Mọi Prompt)

⚠️ **LƯU Ý:** Không fix cứng trang phục áo sơ mi hay bối cảnh quán cafe vào Global Locks. Luôn sử dụng token động kết hợp với **khóa cứng góc máy MCU Eye-Level**:

```text
A candid real-life portrait of an elegant 28-year-old East Asian woman (@_Brand_Female_Lead), authentic delicate face, natural soft matte skin texture, visible natural micro-pores, refined facial features, wearing [DYNAMIC_OUTFIT_STRING], unobstructed natural neckline, elegant bare collarbone, delicate clean chest area, strictly no earrings, no necklace, no accessories, positioned in @_Location_ID ([DYNAMIC_ENVIRONMENT_STRING]). 
CAMERA FRAME LOCK: Locked-off eye-level medium close-up (MCU) portrait shot (from mid-chest up to top of head, exactly 10-15% headroom above hair), stationary tripod-mounted camera, eye-level lens height, perfectly perpendicular 90-degree angle to subject. Strictly zero camera movement, no zoom, no pan, no tilt, no angle change between scenes, fixed camera position, maintaining identical focal length, identical distance, and identical framing composition across 100% of scenes.
ACTING DYNAMICS: Subtle 3-tier micro-acting with steady posture: 70% direct lens eye contact with gentle 30% reflective contemplation, natural micro-blinking, subtle micro-nods and organic chest breathing, relaxed hand micro-gestures contained naturally within the lower third of the frame.
Stationary hands-free mounted camera, pristine clean sensor image, zero on-screen display, zero UI elements, no REC icon, no battery icon, no timecode, no camera viewfinder graphics. Soft diffused natural ambient daylight, neutral color balance, unretouched real human photography, zero AI plastic doll look, zero waxy shine, zero CGI rendering.
STRICT ASPECT RATIO LOCK: the output MUST be exactly [9:16 vertical 720x1280 | 16:9 landscape 1280x720].
```

### Nguyên tắc nạp giá trị cho Token động:
- **Nếu là Sáng tạo mới:** `[DYNAMIC_OUTFIT_STRING]` và `[DYNAMIC_ENVIRONMENT_STRING]` được tự động tạo theo kịch bản ở Giai đoạn 2 (ví dụ: `wearing an elegant white silk shirt with relaxed neckline`, `sitting by a sunny window in a modern library`).
- **Nếu là Clone đối thủ:** Dán nguyên văn `[CLONED_OUTFIT_STRING]` và `[CLONED_ENVIRONMENT_STRING]` đã bóc tách từ Hộp Khám Nghiệm Thị Giác ở Giai đoạn 1 vào TẤT CẢ các câu prompt của từng Scene. Cấm tuyệt đối quay về trang phục mặc định!

---

## 2. Quy Tắc Cú Máy Đơn Nhất 8s (CẤM Chia Timeline & CẤM Đổi Góc Máy)

- **TUYỆT ĐỐI CẤM:** Không thay đổi góc máy hay đổi sang Toàn cảnh (Wide) / Cận cảnh (Close-Up). Giữ nguyên 100% góc máy **Locked-off Eye-Level MCU** xuyên suốt toàn bộ các phân cảnh.
- **TUYỆT ĐỐI CẤM:** Không chia mốc thời gian như `[0.0s - 7.1s]... [7.1s - 8.0s]...`.
- **CÚ PHÁP CHUẨN:**
  ```text
  Locked-off eye-level medium close-up (MCU) shot, stationary camera. A continuous unbroken single-take video throughout all 8.0 seconds with zero camera movement, no zoom, no pan, strictly no fade to black, no dissolve, no motion blur, no scene transition, maintaining sharp focus, consistent headroom, and active lifelike presence throughout the entire 8.0 seconds.
  ```

---

## 3. Cú Pháp Khẩu Hình & Diễn Xuất

### Chế độ Thoại trực tiếp (Lip-sync):
```text
She speaks articulately and continuously throughout with natural realistic lip-sync, subtle organic micro-blinking, authentic micro-saccades, and gentle thoughtful head tilts, saying: "[Nguyên văn câu thoại tiếng Việt sạch từ 22-25 từ trong ngoặc kép]".
```

### Chế độ Voice-over rời (Khóa môi):
```text
The character remains completely silent with lips naturally closed, no mouth movement, chest gently rising and falling with calm natural breathing, expressing emotions purely through deep mindful gaze, subtle warm micro-smile, and serene presence.
```

---

## 4. Thứ Tự Nạp Reference (Bắt Buộc)
1. **Master Character Sheet** (`@_Brand_Female_Lead`)
2. **Keyframe First Frame** ($K_x$)
3. **Keyframe Last Frame** ($K_{x+1}$)
4. **Mega Prompt Text**

---

## Checklist Kiểm Định Giai Đoạn 4
- [ ] Mọi prompt đều kế thừa đúng Token `[DYNAMIC_OUTFIT_STRING]` và `[DYNAMIC_ENVIRONMENT_STRING]`.
- [ ] Tuyệt đối không áp đặt trang phục/bối cảnh mặc định.
- [ ] Không có mốc thời gian chia timeline trong prompt.
- [ ] Khóa nghiêm ngặt: không khuyên tai, không dây chuyền, không dây an toàn.
- [ ] Thứ tự nạp ref tuân thủ chính xác 100%.
