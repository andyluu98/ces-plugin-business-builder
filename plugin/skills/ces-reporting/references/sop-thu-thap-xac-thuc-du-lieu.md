# SOP Thu Thập và Xác Thực Dữ Liệu Báo Cáo | ces-reporting

## Mục đích & Phạm vi
Tài liệu này quy định quy trình chuẩn thu thập, kiểm tra và xác thực dữ liệu đầu vào cho tất cả báo cáo nội bộ của doanh nghiệp. Mục tiêu là đảm bảo "Garbage In, Garbage Out" không xảy ra — mọi báo cáo đều dựa trên dữ liệu sạch, chính xác và nhất quán, từ đó xây dựng niềm tin của lãnh đạo vào hệ thống thông tin quản trị.

## Câu hỏi thu thập thông tin
1. Dữ liệu cho báo cáo hiện đến từ những nguồn nào (CRM, ERP, kế toán, Excel thủ công, Google Sheet)?
2. Có vấn đề nào về chất lượng dữ liệu hiện tại không (trùng lặp, thiếu, sai, không nhất quán)?
3. Ai chịu trách nhiệm nhập liệu ở từng hệ thống? Họ có được đào tạo về chuẩn nhập liệu chưa?
4. Có quy trình kiểm tra dữ liệu trước khi báo cáo không? Ai thực hiện?
5. Lỗi dữ liệu nghiêm trọng nhất từng xảy ra là gì? Hậu quả như thế nào?
6. Tần suất extract và validate dữ liệu cho báo cáo là bao lâu?
7. Có yêu cầu audit trail (lịch sử thay đổi dữ liệu) không?

## Cấu trúc tài liệu

### Phần 1: Thông tin SOP và nguyên tắc dữ liệu
- Mã SOP: RPT-SOP-001
- Phạm vi: Tất cả dữ liệu phục vụ báo cáo nội bộ
- Nguyên tắc Single Source of Truth
- Data Quality Dimensions: Accuracy, Completeness, Consistency, Timeliness, Uniqueness

### Phần 2: Sơ đồ luồng dữ liệu (Data Flow Map)

```
Nguồn dữ liệu gốc
  ↓ (Extract)
Data Staging Area / Staging Sheet
  ↓ (Transform + Validate)
Clean Data Repository
  ↓ (Load)
Báo cáo / Dashboard
```

**Nguồn dữ liệu và người sở hữu:**
| Hệ thống | Loại dữ liệu | Người sở hữu | Chuẩn nhập liệu |
|---------|-------------|-------------|----------------|
| CRM | Khách hàng, cơ hội, deal | Sales Admin | SOP-CRM-001 |
| Phần mềm kế toán | Doanh thu, chi phí, công nợ | Kế toán | SOP-ACC-001 |
| HRMS | Nhân sự, bảng lương | HR Admin | SOP-HR-001 |
| Excel/Manual | Dữ liệu chưa có hệ thống | Người phụ trách | Template chuẩn |

### Phần 3: Quy trình thu thập dữ liệu

**Bước 1 – Xác định dữ liệu cần thiết**
- Review template báo cáo để liệt kê tất cả data points cần có
- Xác nhận nguồn dữ liệu chính thức cho từng data point
- Không dùng "dữ liệu tiện tay" nếu không phải nguồn chính thức

**Bước 2 – Extract dữ liệu từ nguồn**
- Ghi lại ngày giờ extract
- Lưu file raw data trước khi xử lý (không ghi đè)
- Đặt tên file: `[RAW] [Tên nguồn] [YYYYMMDD] [HH:MM].xlsx`

**Bước 3 – Staging và chuẩn hóa**
- Copy vào staging sheet riêng
- Chuẩn hóa format: ngày tháng, số, text
- Xử lý giá trị null/blank theo quy tắc đã định
- Không xóa dữ liệu gốc

### Phần 4: Quy trình xác thực dữ liệu (Data Validation)

**4.1 Kiểm tra tính đầy đủ (Completeness)**
- [ ] Số dòng dữ liệu có đúng kỳ vọng không?
- [ ] Có field nào bị blank không được phép blank không?
- [ ] Tất cả phòng ban/chi nhánh đã báo cáo chưa?

**4.2 Kiểm tra tính chính xác (Accuracy)**
- [ ] Tổng doanh thu khớp với phần mềm kế toán không?
- [ ] Số nhân viên khớp với danh sách HR không?
- [ ] Số liệu có nằm trong khoảng hợp lý không (outlier check)?

**4.3 Kiểm tra tính nhất quán (Consistency)**
- [ ] Định nghĩa KPI có được áp dụng nhất quán không?
- [ ] Cùng một thực thể có bị tính 2 lần ở nguồn khác nhau không?
- [ ] Phân loại dữ liệu có nhất quán xuyên suốt không?

**4.4 Kiểm tra tính kịp thời (Timeliness)**
- [ ] Dữ liệu có thuộc đúng kỳ báo cáo không?
- [ ] Có giao dịch nào bị missing do nhập liệu trễ không?

**4.5 Kiểm tra loại trừ trùng lặp (Uniqueness)**
- [ ] Có ID trùng lặp không?
- [ ] Có khách hàng/nhân viên bị đếm 2 lần không?

### Phần 5: Xử lý khi phát hiện lỗi dữ liệu

**Phân loại mức độ lỗi:**
- **Critical**: Lỗi ảnh hưởng >5% tổng số liệu hoặc làm sai kết luận báo cáo → Dừng báo cáo, báo cáo ngay lên trưởng phòng
- **Major**: Lỗi ảnh hưởng 1-5% → Sửa ngay trước khi báo cáo, ghi chú
- **Minor**: Lỗi ảnh hưởng <1% → Sửa và ghi chú vào audit log

**Quy trình sửa lỗi:**
1. Ghi nhận lỗi vào Data Error Log (ngày, loại lỗi, nguồn, ảnh hưởng)
2. Truy tìm nguyên nhân gốc (nhập liệu sai, lỗi hệ thống, quy trình bị bỏ sót)
3. Sửa dữ liệu với ghi chú "Đã hiệu chỉnh ngày [X] bởi [Y]"
4. Thông báo cho người nhận báo cáo nếu lỗi đã được gửi trước đó

### Phần 6: Data Error Log
| Ngày | Báo cáo | Loại lỗi | Mô tả | Mức độ | Người phát hiện | Cách xử lý | Nguyên nhân gốc |
|------|---------|---------|-------|--------|----------------|-----------|----------------|

### Phần 7: Đào tạo và năng lực
- Đào tạo nhập liệu chuẩn cho tất cả người dùng hệ thống
- Kiểm tra định kỳ chất lượng nhập liệu
- Feedback loop: thông báo lỗi nhập liệu về đúng người đã nhập

## Định dạng & Lưu trữ
- Format: .docx + checklist validation .xlsx
- Đặt tên: `[SOP/YYYY] RPT-SOP-001 - Thu Thập Xác Thực Dữ Liệu - BI Team v1.0`
- Thư mục: `09 Báo Cáo / 04 SOP`
- Data Error Log lưu tối thiểu 2 năm để phân tích xu hướng

## Hướng dẫn cho Claude
1. Hỏi về nguồn dữ liệu hiện tại và vấn đề chất lượng dữ liệu cụ thể trước khi soạn SOP.
2. Tạo checklist validation dạng bảng để người dùng tích vào từng bước.
3. Phần quan trọng nhất: xác định nguồn dữ liệu chính thức (Source of Truth) cho từng metric.
4. Nhấn mạnh nguyên tắc "Never modify raw data" — luôn làm việc trên bản copy.
5. Gợi ý tự động hóa một số bước validation bằng Excel formula hoặc Power Query.
6. Đề xuất Data Quality Dashboard để theo dõi tỷ lệ lỗi theo thời gian — khi trend cải thiện, đó là tín hiệu SOP đang hoạt động.
