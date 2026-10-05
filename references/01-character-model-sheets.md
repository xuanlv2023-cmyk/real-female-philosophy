# Giai đoạn 1 — Character Model Sheets & Quy Chuẩn Trang Phục / Bối Cảnh Động

## Mục đích
Thiết lập Master Model Sheet cho nhân vật Nữ chính thương hiệu (`@_Brand_Female_Lead`) để khóa cố định 100% diện mạo khuôn mặt, thần thái tri thức và chất da thật. **TUYỆT ĐỐI KHÔNG KHÓA CỐ ĐỊNH TRANG PHỤC VÀ BỐI CẢNH**. Trang phục và bối cảnh là 2 biến số biến thiên linh hoạt theo từng kịch bản hoặc bóc tách chuẩn xác từ video đối thủ.

---

## 1. Yếu Tố Khóa Cố Định Duy Nhất: Khuôn Mặt & Ngũ Quan (@_Brand_Female_Lead)
- **Hình tượng thương hiệu:** Nữ 28 tuổi Á Đông thanh tú, quyến rũ tri thức, phong thái tự tại, điềm đạm và tự tin.
- **Đặc điểm diện mạo cố định:** Gương mặt trái xoan thanh tú, đôi mắt sáng thông tuệ có chiều sâu, sống mũi cao tự nhiên, khóe môi thoảng nét cười nhẹ nhàng.
- **Tiêu chuẩn bề mặt da:** Real human skin texture, natural soft matte finish, visible delicate micro-pores, natural healthy skin tone. Triệt tiêu hoàn toàn: `porcelain`, `plastic shine`, `doll skin`, `flawless airbrush`.
- **Kỷ luật phụ kiện tuyệt đối (Zero-Accessories Rule):** **TUYỆT ĐỐI KHÔNG MÔ TẢ PHỤ KIỆN** (hoàn toàn không có bông tai, khuyên tai, không dây chuyền hay bất kỳ trang sức kim loại nào). Giữ vùng cổ và tai thanh thoát tự nhiên để tránh AI vẽ lem nhem, méo mó.

---

## 2. Quy Chuẩn 2 Chế Độ Xác Định Trang Phục & Bối Cảnh

### CHẾ ĐỘ A: SÁNG TẠO MỚI (SCRIPT-DRIVEN DYNAMIC GENERATION)
Khi tạo video từ ý tưởng mới, **trang phục và bối cảnh biến chuyển linh hoạt 100% theo nội dung câu chuyện**:
- **Bối cảnh (`[DYNAMIC_ENVIRONMENT_STRING]`):** Tùy biến phong phú theo kịch bản (góc quán cà phê kính ngày mưa, bàn làm việc cạnh cửa sổ nhìn ra phố xá, ban công chung cư đón gió chiều, xe hơi ban ngày, thư viện cổ, góc phòng đọc sách ấm áp...).
- **Trang phục (`[DYNAMIC_OUTFIT_STRING]`):** Phù hợp hoàn cảnh câu chuyện theo phong cách quyến rũ thanh lịch (*Tasteful Decolletage*):
  - Đi làm/gặp gỡ: Áo sơ mi lụa mở 1 cúc nhẹ nhàng, áo blazer thanh lịch.
  - Đi dạo/cuối tuần: Đầm suông nhẹ nhàng, áo thun cổ tim ôm dáng vừa phải.
  - Ở nhà/đọc sách: Áo dệt kim cổ rộng để lộ xương quai xanh thanh tú.
  - *Luôn giữ nguyên tắc: thanh lịch, tôn dáng tự nhiên, 100% an toàn kiểm duyệt AI.*

---

### CHẾ ĐỘ B: CLONE ĐỐI THỦ (MULTIMODAL VISION AUDIT & ZERO-DEFAULT RULE)
Khi người dùng đính kèm video/ảnh đối thủ hoặc yêu cầu clone video, **VÔ HIỆU HÓA HOÀN TOÀN MỌI GIÁ TRỊ MẶC ĐỊNH**. AI bắt buộc thực hiện **Khám Nghiệm Thị Giác Đầu Vào** trước khi viết kịch bản:

#### Hộp Khám Nghiệm Thị Giác Đầu Vào (Bắt buộc in ra ở đầu phản hồi):
```text
🔍 BẢNG KHÁM NGHIỆM THỊ GIÁC ĐẦU VÀO (VISION AUDIT):
- Cấu trúc trang phục: [Phân loại rõ: ÁO ĐƠN (Single Garment) HOẶC NHIỀU LỚP (Layered Outfit)]
- Chi tiết trang phục thực tế quan sát được: [Mô tả chính xác kiểu áo, màu sắc, chất liệu, cổ áo, tay áo: ví dụ áo polo cộc tay màu trắng có cổ bẻ / áo thun đen ôm nhẹ / áo sơ mi / đầm suông...]
- Áo khoác ngoài: KHÔNG CÓ (Chỉ ghi nếu mắt thực tế nhìn thấy có áo khoác ngoài, tuyệt đối không tự bịa)
- Bối cảnh & Chi tiết (Environment & Lighting): [Không gian thực tế từ video gốc: ví dụ trong xe hơi ghế da đen, văn phòng kính, quán cafe, đường phố]
- Kiểm định Đạo cụ & Phụ kiện: KHÔNG TỰ BỊA VẬT THỂ (Không có dây an toàn seatbelt, không khuyên tai, không dây chuyền, không cầm điện thoại)
=> KHÓA TOKEN TRANG PHỤC: [CLONED_OUTFIT_STRING] = "wearing [MÔ_TẢ_TRANG_PHỤC_THỰC_TẾ]"
=> KHÓA TOKEN BỐI CẢNH: [CLONED_ENVIRONMENT_STRING] = "[Không gian và ánh sáng bóc tách chính xác từ video đối thủ]"
```

#### Kỷ luật phân loại trang phục 2 nhánh (Two-Branch Outfit Classification):
- **Nhánh 1 (Áo đơn - Single Garment):** Nếu nhân vật trong video gốc chỉ mặc 1 áo (áo polo, áo thun, sơ mi, váy đầm...):
  - BẮT BUỘC chỉ mô tả duy nhất 1 lớp áo.
  - TUYỆT ĐỐI CẤM dùng từ `"underneath"`, CẤM tự bịa áo khoác ngoài.
  - Cú pháp token: `wearing an authentic [màu sắc] [chất liệu] [kiểu áo]`.
- **Nhánh 2 (Áo nhiều lớp - Layered Outfit):** CHỈ KHI mắt thấy rõ ràng nhân vật đang mặc áo khoác ngoài bên trên một áo trong:
  - Cú pháp token: `wearing [ÁO_TRONG] underneath an open [ÁO_NGOÀI]`.

---

## 3. Quy Chuẩn Cố Định Góc Máy MCU & Diễn Xuất Vi Mô Tự Nhiên

- **Khóa Cứng Góc Máy Cố Định (Locked-off Eye-Level MCU):**
  - Cố định 100% các phân cảnh ở góc máy ngang tầm mắt (Eye-level), cỡ cảnh Trung cận (Medium Close-Up - MCU từ giữa ngực lên đỉnh đầu, chừa 10-15% khoảng trống trên đỉnh đầu).
  - CẤM TUYỆT ĐỐI chuyển góc máy sang Toàn cảnh (Wide) hay Cận cảnh (Close-up), cấm lia máy (pan/tilt), cấm zoom in/out, cấm đổi tiêu cự giữa các cảnh.
- **Diễn Xuất Vi Mô 3 Tầng (3-Tier Micro-Acting):**
  - **Tầng 1 (Ánh mắt):** 70% nhìn thẳng vào tâm ống kính giao tiếp với khán giả; 30% chớp mắt và liếc nhẹ chiêm nghiệm.
  - **Tầng 2 (Đầu & Hơi thở):** Chuyển động cơ mặt tự nhiên, đầu nghiêng nhẹ theo nhịp thoại, nhịp thở lồng ngực tự nhiên, cơ mặt thả lỏng.
  - **Tầng 3 (Bàn tay):** Đặt rảnh tay hoặc cử chỉ vi mô nằm gọn trong 1/3 dưới khung hình (chạm nhẹ tách cà phê/ly nước, lật trang sách, ngửa lòng bàn tay nhẹ nhàng).
- **Vùng ngực và cổ áo thông thoáng, tự nhiên:** `unobstructed natural neckline, elegant bare collarbone, delicate natural decolletage, clean chest area, no seatbelt, no necklace, no earrings`.
- **Không tự bịa dây an toàn:** Tuyệt đối KHÔNG tự ý đưa dây an toàn (`seatbelt`) vào bối cảnh xe nếu video gốc không có.
- **CẤM từ khóa `selfie`:** Dùng `Stationary locked-off hands-free tripod-mounted camera, eye-level medium close-up (MCU) portrait shot, both hands relaxed naturally`.
- **Chống rác màn hình:** `Pristine clean sensor image, zero on-screen display, zero UI elements, no REC icon, no battery icon, no timecode, no camera viewfinder graphics`.

---

## 4. Master Prompt Tạo Model Sheet Khóa Diện Mạo Nhân Vật

```text
A professional four-view character turnaround model sheet of an elegant 28-year-old East Asian intellectual woman (@_Brand_Female_Lead), displaying front view, three-quarter view, profile side view, and warm smiling facial expression close-up. Authentic natural Asian beauty, delicate oval face, intelligent deep dark brown eyes with natural moisture reflection, natural soft matte skin finish, visible natural skin micro-pores, subtle natural laughter lines. Wearing neutral simple clothes for reference, unobstructed natural neckline, elegant bare collarbone, clean chest area, strictly no earrings, no necklace, no accessories. Stationary locked-off hands-free tripod-mounted camera, eye-level medium close-up (MCU) portrait framing from chest up to head, both hands relaxed naturally. Soft diffused natural morning daylight, neutral studio background, pristine clean sensor image, zero on-screen display, zero UI elements, unretouched real human photography, zero AI plastic doll look, zero waxy shine, zero CGI rendering --ar 16:9
```

---

## Checklist Kiểm Định Giai Đoạn 1
- [ ] Khuôn mặt và chất da của Tuệ An được khóa nhất quán on-model.
- [ ] Hoàn toàn không mô tả khuyên tai, không dây chuyền.
- [ ] Trang phục được thiết kế linh hoạt theo kịch bản HOẶC bóc tách chính xác từ video đối thủ qua Hộp Khám Nghiệm Thị Giác.
- [ ] Tuyệt đối không áp đặt trang phục hoặc bối cảnh mặc định.
- [ ] Tuân thủ nghiêm ngặt Quy tắc 2 Nhánh (Áo đơn vs Áo 2 lớp).
