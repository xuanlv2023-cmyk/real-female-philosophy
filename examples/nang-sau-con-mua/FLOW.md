# FLOW — "Nắng Sau Cơn Mưa" Đi Qua 8 Giai Đoạn

> **LƯU Ý QUAN TRỌNG:** Dự án "Nắng Sau Cơn Mưa" (áo sơ mi xanh lụa, quán cà phê kính Sài Gòn) chỉ là **MỘT VÍ DỤ MINH HỌA CỤ THỂ** để người dùng và AI hiểu phương pháp triển khai. Trong thực tế, **trang phục và bối cảnh biến thiên 100%** theo kịch bản mới hoặc bóc tách chính xác từ video đối thủ qua Hộp Khám Nghiệm Thị Giác.

---

## 1. Chuỗi Keyframe (Luật Match-Cut Liền Mạch)

```mermaid
flowchart LR
  K1["K1 · Ngắm mưa rơi bên cửa kính"] -->|Cảnh 1| K2["K2 · Tay chạm ly latte ấm"]
  K2 -->|Cảnh 2| K3["K3 · Khẽ nâng ly cà phê"]
  K3 -->|Cảnh 3| K4["K4 · Nhấp ngụm nhỏ thư thái"]
  K4 -->|Cảnh 4| K5["K5 · Ánh mắt nhìn ra phố"]
  K5 -->|Cảnh 5| K6["K6 · Nụ cười nhẹ tự tại"]
  K6 -->|Cảnh 6| K7["K7 · Lật trang sách dở"]
  K7 -->|Cảnh 7| K8["K8 · Ánh nắng đầu tiên ló rạng"]
  K8 -->|Cảnh 8| K9["K9 · Nụ cười rạng rỡ đón nắng"]
```

---

## 2. Bảng Phân Rã Tiến Trình 8 Giai Đoạn

| # | Giai đoạn | Nội dung thực hiện trong dự án mẫu | File sản phẩm đầu ra | Tiêu chuẩn kiểm định |
|---|---|---|---|---|
| **0** | **Thu thập đầu vào** | 64 giây (8 cảnh x 8s) · Thuyết minh Tiếng Việt Nữ Sài Gòn · 9:16 dọc | — | ✓ Số cảnh, tỷ lệ khung hình đã khóa |
| **1** | **Model Sheets** | Master Sheet Tuệ An 28 tuổi (@_Brand_Female_Lead) + Quán cafe ngày mưa | `CHARACTER_SHEETS.md` | ✓ Da thật matte, không phụ kiện |
| **2** | **Story Bible** | Logline "Đi qua cơn mưa lòng sẽ bình yên", 8 nhịp cảnh, màng lọc Anti-Slop | [`STORY.md`](STORY.md) | ✓ Sạch slop, đúng 22-25 từ/cảnh |
| **3** | **Keyframes** | 9 Keyframe ($K_1 \dots K_9$), khóa bố cục xương quai xanh và ánh sáng | `keyframes/` | ✓ Khung cuối N trùng khung đầu N+1 |
| **4** | **Mega Prompts** | 8 Mega Prompts: Global locks + Single continuous unbroken take | [`MEGA_PROMPTS.md`](MEGA_PROMPTS.md) | ✓ Không chia timeline, không tripod |
| **5** | **Generate Video** | Render 8 clip 8s trên AI Video, kiểm tra 24fps bằng ffprobe | `videos/` | ✓ Đúng tỷ lệ 9:16, không mờ đuôi |
| **6** | **Sản xuất Âm thanh** | TTS Giọng Nữ Sài Gòn thanh lịch (@Voice_Female_Intellectual), ambient mưa | [`VO_SCRIPT.md`](VO_SCRIPT.md), `audio/` | ✓ Trầm ấm, dịu dàng, không chói gắt |
| **7** | **Dựng & Hậu kỳ** | Normalize 1080x1920 $\rightarrow$ Ghép concat 8 cảnh $\rightarrow$ Mix VO $\rightarrow$ Mix BGM piano | `final_master.mp4` | ✓ Video 64s liền mạch tuyệt đối |

---

## 3. Thứ Tự Nạp Reference
```text
1. MASTER_FEMALE_SHEET  ← Khóa nhân vật thương hiệu nạp đầu tiên
2. KEYFRAME_START (K_x) ← Khung hình bắt đầu của cảnh
3. KEYFRAME_END (K_x+1) ← Khung hình kết thúc của cảnh
4. MEGA PROMPT TEXT     ← Câu lệnh điều khiển diễn xuất vi mô
```
