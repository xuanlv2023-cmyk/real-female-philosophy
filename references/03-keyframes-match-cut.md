# Giai đoạn 3 — Keyframes & Luật Match-Cut Nữ Tri Thức

## Mục đích
Thiết lập chuỗi hình ảnh mốc (Keyframes) cho dự án video nữ tri thức. Áp dụng luật Match-Cut để tạo chuyển động vi mô liền mạch, bảo toàn góc nhìn (Eyeline match), ánh sáng qua cửa kính và nụ cười thanh lịch của nhân vật.

---

## 1. Nguyên Tắc Chuỗi Keyframe ($N$ Cảnh $\rightarrow N+1$ Keyframes)

$$\text{Cảnh } 1: K_1 \rightarrow K_2$$
$$\text{Cảnh } 2: K_2 \rightarrow K_3$$
$$\dots$$
$$\text{Cảnh } 8: K_8 \rightarrow K_9$$

### Luật Match-Cut Bất Biến & Khóa Khung Hình Đồng Nhất (Single Frame Perspective Lock):
- **Khung cuối của Cảnh $N$ ($K_{N+1}$) chính là Khung đầu của Cảnh $N+1$.**
- **Cố định phối cảnh và cự ly máy quay (MCU Eye-Level):**
  - Toàn bộ chuỗi keyframe $K_1 \dots K_{N+1}$ phải giữ **nguyên vẹn một cự ly và góc máy duy nhất**: Medium Close-Up (từ giữa ngực lên đỉnh đầu, chừa 10-15% khoảng trống trên đầu).
  - Không bao giờ thay đổi tiêu cự (focal length) hay vị trí đặt máy quay giữa các keyframe.
- **Kế thừa diễn xuất vi mô 3 tầng (3-Tier Micro-Acting):**
  1. **Ánh mắt:** 70% nhìn thẳng vào tâm ống kính, 30% nhìn nghiêng chiêm nghiệm.
  2. **Đầu & Hơi thở:** Tư thế đầu ổn định, ngực phập phồng tự nhiên theo nhịp thở.
  3. **Bàn tay:** Đặt rảnh tay hoặc cử chỉ vi mô nằm gọn trong 1/3 dưới khung hình.
- Giữ vững:
  1. Hướng ánh mắt và nét mặt thanh thoát tự nhiên.
  2. Bố cục thềm ngực và xương quai xanh (Decolletage framing).
  3. Ánh sáng và màu sắc bối cảnh nhất quán (Natural diffused lighting).

---

## 2. Kỹ Thuật Sinh Keyframe Chuẩn Nữ Tri Thức

Khi tạo Keyframe trên Midjourney / Flux / Muse, luôn kèm Master Model Sheet của `@_Brand_Female_Lead` làm ảnh tham chiếu:

```text
[Nhãn định danh]: A candid cinematic locked-off eye-level medium close-up (MCU) portrait shot of an elegant 28-year-old East Asian woman (@_Brand_Female_Lead), authentic delicate face, matte skin texture with visible micro-pores, wearing [DYNAMIC_OUTFIT_STRING], unobstructed natural neckline, bare collarbone, clean chest area, strictly no earrings, no necklace, no accessories, positioned in @_Location_ID ([DYNAMIC_ENVIRONMENT_STRING]). Framing strictly from mid-chest up to top of head with 10-15% headroom above hair. [Mô tả chi tiết tư thế & hành động của Keyframe K_x]. Soft diffused ambient daylight, natural color science, stationary hands-free tripod-mounted camera, pristine clean sensor image, zero UI elements, unretouched real human photography, zero AI plastic shine, zero CGI rendering --ar [9:16 | 16:9]
```

---

## Checklist Kiểm Định Giai Đoạn 3
- [ ] Số lượng keyframe = Số cảnh + 1.
- [ ] Toàn bộ chuỗi keyframe giữ đồng nhất 100% góc máy Locked-off Eye-Level MCU.
- [ ] Tư thế kết thúc cảnh N trùng khớp tuyệt đối với tư thế mở đầu cảnh N+1.
- [ ] Vùng cổ áo và tai thông thoáng, không có khuyên tai/dây chuyền lạ mọc thêm.
- [ ] Ánh sáng và màu sắc bối cảnh nhất quán 100%.
