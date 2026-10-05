---
name: "real-female-philosophy-v10"
description: "AI studio tạo video Triết Lý Nữ Xinh Đẹp / Vlog Đời Thực Đa Bối Cảnh Chân Thật 100% trọn gói từ ý tưởng đến video MP4: nhân vật nữ chính @_Brand_Female_Lead thanh tú quyến rũ tri thức, kịch bản lọc Anti-Slop sâu lắng, chuỗi keyframe match-cut, mega prompt 8s single-take zero-transition, Voice DNA Nữ Sài Gòn, và dựng tự động bằng FFmpeg. Dùng khi user muốn làm video triết lý nữ tính, vlog đời thực hoặc clone video đối thủ."
---

# Real Female Philosophy & Mindful Vlog Pipeline (Nữ Tri Thức V10)

**Tác giả:** Xuanlv  
**Đặc trưng:** 100% Người Thật Đời Thực • Nữ 28 tuổi Á Đông thanh tú • Quyến rũ tri thức thanh lịch • Trầm ấm sâu sắc • Zero-Transition 8s chống mờ • Triệt tiêu hoàn toàn mặt sáp và búp bê AI • **Trang phục & Bối cảnh động 100% (Zero-Default Rule)**.

## Purpose
Dẫn dắt toàn bộ quy trình sản xuất video Shorts/Long-form triết lý nữ tri thức người thật 100% — từ ý tưởng thô hoặc video mẫu của đối thủ thành file MP4 hoàn chỉnh — theo pipeline 8 giai đoạn chuẩn hóa.

---

## NGUYÊN TẮC CỐT LÕI: ZERO-DEFAULT & LOCKED-OFF MCU CAMERA RULE
1. **Khóa duy nhất khuôn mặt & ngũ quan nhân vật thương hiệu (`@_Brand_Female_Lead`):** Nữ 28 tuổi Á Đông thanh tú, quyến rũ tri thức, làn da matte có lỗ chân lông thật, triệt tiêu mặt búp bê AI, **khóa cấm 100% khuyên tai/dây chuyền**.
2. **Khóa Cứng Góc Máy Cố Định (Locked-off Eye-Level Medium Close-Up - MCU) Xuyên Suốt Toàn Bộ Phân Cảnh:**
   - **100% các phân cảnh** giữ nguyên góc máy ngang tầm mắt (Eye-level), cỡ cảnh Trung cận (MCU - từ giữa ngực lên đỉnh đầu, chừa 10-15% khoảng trống trên đầu - headroom).
   - Máy quay gắn chân cố định (tripod locked-off), cấm lia máy (pan/tilt), cấm zoom in/out, cấm đổi tiêu cự hay đổi góc giữa các cảnh.
   - **Diễn xuất vi mô 3 tầng (3-Tier Micro-Acting):** Tập trung năng lượng vào lời nói và thần thái tự nhiên:
     - Tầng 1 (Ánh mắt): 70% nhìn thẳng tương tác vào ống kính, 30% nhìn nghiêng chiêm nghiệm nhẹ nhàng.
     - Tầng 2 (Đầu & Thân): Nghiêng đầu nhẹ nhàng khi nhấn ý, nhịp thở lồng ngực tự nhiên, cơ mặt thả lỏng.
     - Tầng 3 (Bàn tay): Cử chỉ vi mô tự nhiên ở 1/3 dưới khung hình (chạm nhẹ tách cà phê/ly nước, lật trang sách, ngửa lòng bàn tay nhẹ nhàng).
3. **Trang phục (`[DYNAMIC_OUTFIT_STRING]`) và Bối cảnh (`[DYNAMIC_ENVIRONMENT_STRING]`) biến thiên 100%:**
   - **Khi Sáng tạo mới:** Tự động tạo bối cảnh và trang phục phù hợp với từng kịch bản cụ thể (quán cà phê, ban công, phòng làm việc, trên xe ô tô, thư viện, công viên...).
   - **Khi Clone đối thủ:** Bắt buộc chạy **Hộp Khám Nghiệm Thị Giác Đầu Vào (Vision Audit)** bóc tách chuẩn xác 100% từ video đối thủ (phân loại Áo đơn vs Áo 2 lớp, màu sắc, bối cảnh thực). CẤM TUYỆT ĐỐI dùng trang phục hoặc bối cảnh mặc định.

---

## Giai đoạn 0 — Thu Thập Đầu Vào (BẮT BUỘC HỎI TRƯỚC)
Hỏi user 4 thông số dưới đây trước khi bắt đầu. Chưa có đáp án thì chưa sang giai đoạn 1.

### 1. Thời lượng video mong muốn là bao lâu?
- Mỗi phân cảnh chuẩn hóa là **8.0 giây** (chuẩn nhịp thở âm học và single-take AI).
- **Số cảnh = làm tròn lên (thời lượng mong muốn ÷ 8).**
- *Ví dụ:* ~60s $\rightarrow$ 8 cảnh (khuyên dùng cho Shorts/Reels/TikTok); 5 phút $\rightarrow$ 38 cảnh.

### 2. Định dạng & Tỷ lệ khung hình: 9:16 (dọc) hay 16:9 (ngang)?
- ⚠️ **STRICT ASPECT RATIO LOCK:** Toàn bộ ảnh ref, keyframe và video xuất ra phải cùng 1 tỷ lệ đã khóa.

### 3. Phương thức sáng tạo: Tạo Mới hay Clone Đối Thủ?
- **Tạo mới:** AI gợi ý ý tưởng và tự động thiết kế trang phục/bối cảnh theo kịch bản.
- **Clone đối thủ:** Người dùng gửi video MP4/link/transcript. AI bắt buộc xuất **Hộp Khám Nghiệm Thị Giác** ở đầu phản hồi để trích xuất token `[CLONED_OUTFIT_STRING]` và `[CLONED_ENVIRONMENT_STRING]`.

### 4. Chế độ âm thanh & Thoại
- `Voice-over rời` | `Thoại nhân vật (Lip-sync)` | `Thoại kết hợp (Hybrid)`.

---

## Workflow (8 Giai Đoạn Chuẩn Hóa)

1. **Character Model Sheet & Bóc Tách Thị Giác** $\rightarrow$ [`references/01-character-model-sheets.md`](references/01-character-model-sheets.md)  
   Khóa diện mạo Tuệ An (`@_Brand_Female_Lead`), phong cách quyến rũ điện ảnh thanh lịch, cấm khuyên tai/dây chuyền, Hộp Khám Nghiệm Thị Giác cho clone, quy chuẩn No-seatbelt và Zero-UI.

2. **Story Bible & Màng Lọc Anti-Slop** $\rightarrow$ [`references/02-story-bible-anti-slop.md`](references/02-story-bible-anti-slop.md)  
   Biên tập kịch bản lọc sạch sáo ngữ self-help nông cạn. Bắt buộc tuân thủ **Kỷ luật nhịp độ 8s: 22 - 25 từ (tối đa 28 từ)** cho mỗi cảnh.

3. **Keyframes & Luật Match-Cut** $\rightarrow$ [`references/03-keyframes-match-cut.md`](references/03-keyframes-match-cut.md)  
   Tạo chuỗi $N+1$ keyframe ($K_1 \dots K_{N+1}$) từ Model Sheet và Token bối cảnh/trang phục động. Khóa cứng quy tắc: Khung cuối cảnh $N$ = Khung đầu cảnh $N+1$.

4. **Mega Prompts 8s Zero-Transition** $\rightarrow$ [`references/04-mega-prompts-8s.md`](references/04-mega-prompts-8s.md)  
   Soạn thảo Mega Prompt nhúng Token động `[DYNAMIC_OUTFIT_STRING]` và `[DYNAMIC_ENVIRONMENT_STRING]`. CẤM chia mốc timeline `[0.0s - 7.1s]`. Áp dụng cú pháp Single Continuous Unbroken Take.

5. **Tạo Video & An Toàn Kiểm Duyệt** $\rightarrow$ [`references/05-video-generation-rules.md`](references/05-video-generation-rules.md)  
   Render trên Kling AI / Runway / Hailuo / Muse với First Frame & Last Frame. Đảm bảo an toàn kiểm duyệt AI (Non-NSFW) và kiểm định bằng `ffprobe`.

6. **Voice DNA & Sản Xuất Âm Thanh** $\rightarrow$ [`references/06-vo-and-audio-dna.md`](references/06-vo-and-audio-dna.md)  
   Sản xuất âm thanh với Voice DNA Nữ Sài Gòn 28 tuổi (`@Voice_Female_Intellectual`), thông số TTS ElevenLabs/Vbee và hòa âm không gian.

7. **Dựng Phim Bằng FFmpeg** $\rightarrow$ [`references/07-assembly-ffmpeg.md`](references/07-assembly-ffmpeg.md)  
   Chuẩn hóa độ phân giải 24fps $\rightarrow$ Nối các cảnh liền mạch không lộ vết cắt $\rightarrow$ Mix VO theo timecode delay $\rightarrow$ Cân bằng nhạc nền piano lofi.

8. **Bài Học Xương Máu** $\rightarrow$ [`references/08-lessons-learned.md`](references/08-lessons-learned.md)  
   10 bài học thực tế phòng tránh các lỗi AI (khuyên tai méo, cánh tay selfie biến dạng, mờ đuôi cảnh).

---

## Dự Án Mẫu Benchmark (Chỉ mang tính chất minh họa phương pháp)
Đọc dự án mẫu thực chiến:
- **Sơ đồ tiến trình & Chuỗi Keyframe:** [`examples/nang-sau-con-mua/FLOW.md`](examples/nang-sau-con-mua/FLOW.md)
- **Story Bible mẫu:** [`examples/nang-sau-con-mua/STORY.md`](examples/nang-sau-con-mua/STORY.md)
- **Mega Prompts mẫu 8 cảnh:** [`examples/nang-sau-con-mua/MEGA_PROMPTS.md`](examples/nang-sau-con-mua/MEGA_PROMPTS.md)
- **Kịch bản thoại sạch:** [`examples/nang-sau-con-mua/VO_SCRIPT.md`](examples/nang-sau-con-mua/VO_SCRIPT.md)

---

## Output Contract (Sản Phẩm Bắt Buộc)
1. `STORY.md` — Kịch bản Story Bible đã duyệt sạch slop.
2. `CHARACTER_SHEETS.md` — Sheet nhân vật & bối cảnh tương ứng của dự án.
3. `MEGA_PROMPTS.md` — Bộ prompt 8s cho toàn bộ các cảnh (chứa token động chuẩn xác).
4. `VO_SCRIPT.md` — File thoại sạch chuẩn đếm từ.
5. Quy trình dựng và nối video hoàn chỉnh bằng FFmpeg theo [`references/07-assembly-ffmpeg.md`](references/07-assembly-ffmpeg.md).
6. File video Master hoàn chỉnh (`final_master.mp4`).
