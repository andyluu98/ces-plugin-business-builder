# CES | Đánh Giá Phạm Vi Công Việc (Scope Assessment)

## Mục đích & Phạm vi
Template này hướng dẫn Claude đánh giá toàn diện phạm vi công việc cần thực hiện sau khi thu thập thông tin từ doanh nghiệp. Kết quả giúp lập kế hoạch triển khai thực tế, tránh ước lượng sai nguồn lực và thời gian.

---

## Câu hỏi thu thập thông tin bổ sung

1. Ngoài các tài liệu mà doanh nghiệp đã có, những lĩnh vực nào hoàn toàn chưa được hệ thống hóa?
2. Có deadline cứng nào không? (Ví dụ: kiểm toán, thanh tra, IPO, gọi vốn...)
3. Đội ngũ nội bộ có thể dành bao nhiêu giờ/tuần để phối hợp xây dựng tài liệu?
4. Có ngân sách thuê tư vấn pháp lý, kế toán để hỗ trợ một số tài liệu chuyên biệt không?
5. Ưu tiên hoàn thiện chiều rộng (nhiều tài liệu ở mức cơ bản) hay chiều sâu (ít tài liệu nhưng chi tiết hoàn chỉnh)?
6. Có yêu cầu song ngữ (Việt – Anh) cho bất kỳ tài liệu nào không?

---

## Outline: Báo cáo Đánh giá Phạm vi

### 1. Tổng quan hiện trạng
- Danh sách tài liệu đã có (đánh giá chất lượng: tốt / cần cập nhật / lạc hậu)
- Danh sách lĩnh vực chưa có tài liệu
- Rủi ro pháp lý và vận hành nếu để trống các khoảng thiếu

### 2. Phân loại công việc theo độ phức tạp

| Mức độ | Mô tả | Ví dụ tài liệu | Thời gian ước tính |
|--------|-------|----------------|-------------------|
| Đơn giản | Claude tạo hoàn toàn, ít điều chỉnh | Nội quy, checklist, template email | 30–60 phút/tài liệu |
| Trung bình | Cần thông tin bổ sung từ DN | Quy trình, KPI, hợp đồng mẫu | 1–3 giờ/tài liệu |
| Phức tạp | Cần tư vấn chuyên gia | Điều lệ, chiến lược, chính sách thuế | 1–3 ngày/tài liệu |

### 3. Ma trận ưu tiên (Urgency × Impact)

```
          | Impact cao      | Impact thấp
----------|-----------------|-------------
Urgent    | LÀM NGAY       | Lên lịch sớm
Không gấp | Lên kế hoạch   | Làm sau cùng
```

Phân loại từng tài liệu vào 4 ô trên.

### 4. Ước tính nguồn lực

- Tổng số tài liệu cần tạo: [X] tài liệu
- Tổng thời gian ước tính: [X] giờ làm việc
- Phân bổ theo skill:
  - ces-governance: [X] tài liệu, ~[X] giờ
  - ces-finance: [X] tài liệu, ~[X] giờ
  - ces-people: [X] tài liệu, ~[X] giờ
  - ces-operations: [X] tài liệu, ~[X] giờ
  - ces-sales / ces-marketing: [X] tài liệu, ~[X] giờ
  - ces-growth / ces-strategy: [X] tài liệu, ~[X] giờ

### 5. Rủi ro và giảm thiểu

| Rủi ro | Xác suất | Tác động | Biện pháp |
|--------|----------|----------|-----------|
| Thông tin DN không đầy đủ | Cao | Trung bình | Phỏng vấn bổ sung |
| Thay đổi cơ cấu tổ chức giữa chừng | Trung bình | Cao | Đóng băng cơ cấu trước khi soạn |
| Quy định pháp lý thay đổi | Thấp | Cao | Gắn ngày hiệu lực vào tài liệu |

### 6. Đề xuất phương án triển khai

**Phương án A – Nhanh (4–8 tuần):** Tập trung tầng 1–2, bộ tài liệu thiết yếu nhất.
**Phương án B – Cân bằng (3–6 tháng):** Hoàn thiện đủ 5 tầng theo lộ trình.
**Phương án C – Toàn diện (6–12 tháng):** Xây dựng hệ thống chuẩn, sẵn sàng kiểm toán và mở rộng.

---

## Hướng dẫn định dạng output

- **Tên file báo cáo:** `scope-assessment-[TenDN]-[YYYYMM].md`
- **Định dạng:** Markdown, có bảng và tiêu đề phân cấp rõ ràng
- **Độ dài:** 2–4 trang A4 (khoảng 800–1.500 từ)
- **Phần kết:** Luôn kết thúc bằng "Khuyến nghị bước tiếp theo" với 3–5 hành động cụ thể

---

## Lưu ý khi đánh giá

- Không hứa hẹn thời gian cụ thể nếu DN chưa cam kết phối hợp
- Ghi rõ các tài liệu cần tư vấn pháp lý/thuế chuyên biệt, Claude không thay thế tư vấn pháp lý
- Ưu tiên tài liệu giảm rủi ro pháp lý trước, tài liệu tối ưu hiệu suất sau
