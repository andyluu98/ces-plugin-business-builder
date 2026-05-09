# CES | Bộ Câu Hỏi Thu Thập Thông Tin Doanh Nghiệp

## Mục đích
Thu thập đầy đủ thông tin để xây dựng hệ thống tài liệu phù hợp với đặc thù từng doanh nghiệp. Đây là bước khởi động bắt buộc trước khi kích hoạt bất kỳ skill nào khác trong hệ thống CES.

---

## Nhóm câu hỏi 1: Thông tin cơ bản doanh nghiệp

1. Tên doanh nghiệp và tên viết tắt (nếu có)?
2. Loại hình doanh nghiệp (TNHH một thành viên / TNHH hai thành viên trở lên / Cổ phần / Hộ kinh doanh / Công ty hợp danh)?
3. Ngành nghề kinh doanh chính? Có ngành nghề phụ nào không?
4. Năm thành lập và địa chỉ trụ sở chính?
5. Quy mô hiện tại: tổng số nhân viên (bao gồm cả thời vụ nếu có)?

## Nhóm câu hỏi 2: Giai đoạn phát triển

6. Doanh nghiệp đang ở giai đoạn nào:
   - Startup (dưới 2 năm, đang tìm product-market fit)
   - Tăng trưởng (2–5 năm, đang mở rộng nhanh)
   - Ổn định (trên 5 năm, đang hệ thống hóa và tối ưu)
   - Chuyển đổi (đang thay đổi mô hình kinh doanh)
7. Doanh thu hàng năm gần nhất (ước tính): Dưới 5 tỷ / 5–50 tỷ / 50–200 tỷ / Trên 200 tỷ?
8. Có bao nhiêu chi nhánh, văn phòng đại diện, hoặc điểm hoạt động?

## Nhóm câu hỏi 3: Cấu trúc tổ chức hiện tại

9. Cơ cấu tổ chức: mấy phòng ban chính? Tên các phòng ban?
10. Hiện đã có những tài liệu nội bộ nào rồi (quy trình, nội quy, hợp đồng, sơ đồ tổ chức...)?
11. Phần mềm quản lý đang sử dụng (CRM, ERP, phần mềm kế toán, HRM, quản lý kho...)?
12. Có website, fanpage, hoặc sàn thương mại điện tử không?

## Nhóm câu hỏi 4: Ưu tiên và nhu cầu

13. Vấn đề cấp thiết nhất hiện tại là gì? (Ví dụ: nhân sự, tài chính, vận hành, pháp lý...)
14. Tài liệu hoặc hệ thống nào cần hoàn thiện trước tiên?
15. Dự kiến hoàn thành toàn bộ hệ thống tài liệu trong bao lâu?
16. Ai là người chịu trách nhiệm triển khai nội bộ?

## Nhóm câu hỏi 5: Đặc thù ngành và thị trường

17. Có quy định pháp lý đặc thù nào trong ngành cần tuân thủ không? (Ví dụ: giấy phép con, chứng chỉ hành nghề, quy định ATTP...)
18. Sản phẩm/dịch vụ bán cho khách hàng B2B, B2C, hay cả hai?
19. Kênh phân phối chính: trực tiếp / đại lý / online / xuất khẩu?
20. Thị trường chính: nội địa hay có yếu tố quốc tế?

---

## Hướng dẫn Claude xử lý sau khi thu thập thông tin

Sau khi người dùng trả lời đầy đủ các câu hỏi trên, Claude thực hiện theo thứ tự:

### Bước 1: Tổng hợp hồ sơ doanh nghiệp
Tóm tắt toàn bộ thông tin thành một đoạn mô tả ngắn (5–7 câu) về doanh nghiệp, bao gồm: đặc điểm, giai đoạn, điểm mạnh, điểm cần cải thiện.

### Bước 2: Đánh giá độ trưởng thành
Chấm điểm sơ bộ theo 6 tiêu chí (xem file `cham-diem-truong-thanh.md`). Đưa ra điểm tổng và nhận xét ngắn gọn từng tiêu chí.

### Bước 3: Xác định tầng ưu tiên
Dựa vào điểm số và nhu cầu cấp thiết, xác định thứ tự tầng cần xây dựng trước:
- **Tầng 1 - Nền tảng pháp lý:** ces-governance
- **Tầng 2 - Quản trị nội bộ:** ces-finance, ces-people
- **Tầng 3 - Vận hành:** ces-operations, ces-sales, ces-marketing
- **Tầng 4 - Phát triển:** ces-growth, ces-strategy
- **Tầng 5 - Hỗ trợ:** ces-reporting, ces-training, ces-customer, ces-product-tech

### Bước 4: Lập danh sách tài liệu theo thứ tự
Liệt kê cụ thể 10–20 tài liệu cần tạo đầu tiên, sắp xếp theo độ ưu tiên.

### Bước 5: Đề xuất lộ trình
Chia lộ trình hoàn thiện thành các giai đoạn (ví dụ: Tháng 1–2, Tháng 3–4, Tháng 5–6), mỗi giai đoạn có mục tiêu và tài liệu cụ thể.

---

## Định dạng output khi hoàn thành thu thập

```
## Hồ sơ Doanh nghiệp: [Tên DN]
- Loại hình: ...
- Ngành: ...
- Quy mô: ... nhân viên | ... chi nhánh
- Giai đoạn: ...
- Doanh thu: ...

## Điểm trưởng thành tổng: X/5
| Tiêu chí     | Điểm | Nhận xét |
|--------------|------|----------|
| Quản trị     | X/5  | ...      |
| Tài chính    | X/5  | ...      |
| Nhân sự      | X/5  | ...      |
| Vận hành     | X/5  | ...      |
| Kinh doanh   | X/5  | ...      |
| Công nghệ    | X/5  | ...      |

## Tầng ưu tiên cần làm trước: [Tầng X]

## Danh sách 10 tài liệu đầu tiên cần tạo:
1. ...
2. ...

## Lộ trình đề xuất:
- Giai đoạn 1 (Tháng 1–2): ...
- Giai đoạn 2 (Tháng 3–4): ...
```
