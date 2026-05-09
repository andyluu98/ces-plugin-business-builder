# SOP Sao Lưu và Phục Hồi Dữ Liệu | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này quy định quy trình chuẩn sao lưu (backup) và phục hồi (recovery) dữ liệu cho toàn bộ hệ thống CNTT của doanh nghiệp, nhằm đảm bảo dữ liệu quan trọng được bảo vệ an toàn và có thể phục hồi trong thời gian chấp nhận được khi xảy ra sự cố. Phạm vi bao gồm tất cả dữ liệu kinh doanh, cơ sở dữ liệu, email, tài liệu và cấu hình hệ thống.

## Câu hỏi thu thập thông tin
1. Dữ liệu nào là quan trọng nhất cần sao lưu (cơ sở dữ liệu khách hàng, tài liệu tài chính, email, code, cấu hình hệ thống)?
2. Hiện tại doanh nghiệp đang sao lưu dữ liệu bằng phương pháp nào? Tần suất?
3. Backup được lưu ở đâu (local server, NAS, cloud, offsite)? Có phân tán địa lý không?
4. RTO (Recovery Time Objective) và RPO (Recovery Point Objective) mong muốn là bao nhiêu?
5. Đã từng thực hiện drill phục hồi dữ liệu chưa? Kết quả như thế nào?
6. Ai chịu trách nhiệm thực hiện và giám sát backup?
7. Có yêu cầu lưu trữ dữ liệu tối thiểu theo pháp luật không (ví dụ: hóa đơn điện tử 10 năm)?

## Cấu trúc tài liệu

### Phần 1: Thông tin SOP và định nghĩa
- Mã SOP, phiên bản, ngày hiệu lực
- RTO: thời gian phục hồi tối đa chấp nhận được
- RPO: lượng dữ liệu tối đa có thể mất (tính theo thời gian)
- Backup Types: Full / Incremental / Differential

### Phần 2: Phân loại dữ liệu cần sao lưu
| Loại dữ liệu | Mức ưu tiên | Tần suất backup | Thời gian lưu | Vị trí lưu |
|-------------|-------------|-----------------|---------------|------------|
| CSDL khách hàng | Critical | Mỗi giờ | 1 năm | Cloud + Local |
| Tài liệu tài chính | High | Hàng ngày | 7 năm | Cloud + Offsite |
| Email | Medium | Hàng ngày | 3 năm | Cloud |
| Tài liệu nội bộ | Medium | Hàng ngày | 2 năm | Cloud |
| Cấu hình hệ thống | High | Sau mỗi thay đổi | Vô thời hạn | Cloud + Local |

### Phần 3: Quy trình sao lưu tự động

**3.1 Backup hàng giờ (Hourly)**
- Đối tượng: Cơ sở dữ liệu sản xuất
- Phương pháp: Incremental backup
- Công cụ: [Tên công cụ backup]
- Xác nhận: Alert email/Slack khi hoàn thành/thất bại

**3.2 Backup hàng ngày (Daily)**
- Thời điểm: 2:00 AM
- Đối tượng: Toàn bộ dữ liệu kinh doanh
- Phương pháp: Full backup cuối tuần, Incremental các ngày khác
- Kiểm tra: Tự động verify checksum

**3.3 Backup hàng tuần (Weekly)**
- Thời điểm: Chủ nhật 3:00 AM
- Đối tượng: Full backup toàn hệ thống
- Phương pháp: Full backup
- Lưu trữ: Thêm 1 bản offsite/cloud

**3.4 Backup hàng tháng (Monthly)**
- Archive backup giữ lâu dài
- Encrypt và đưa vào cold storage

### Phần 4: Quy trình sao lưu thủ công
- Khi nào cần backup thủ công (trước major update, trước sự kiện lớn)
- Các bước thực hiện backup thủ công
- Xác nhận và ghi nhận vào log

### Phần 5: Quy trình phục hồi dữ liệu

**5.1 Phục hồi một phần (Partial Recovery)**
- Kịch bản: Xóa nhầm file/record
- Các bước: Xác định backup cần dùng → Restore vào môi trường test → Verify → Restore production
- Thời gian dự kiến: < 2 giờ

**5.2 Phục hồi toàn bộ hệ thống (Full System Recovery)**
- Kịch bản: Server crash, ransomware, thảm họa
- Các bước chi tiết từng hệ thống
- Thứ tự ưu tiên phục hồi (critical systems first)
- Thời gian dự kiến: < 24 giờ

**5.3 Phục hồi thảm họa (Disaster Recovery)**
- Kịch bản: Mất toàn bộ data center
- Failover sang site dự phòng
- Quy trình kích hoạt DR Plan

### Phần 6: Kiểm tra và xác nhận backup
- Kiểm tra tự động hàng ngày (checksum)
- Kiểm tra khôi phục thực tế hàng quý (Restore Drill)
- Biểu mẫu ghi nhận kết quả Restore Drill
- Báo cáo tình trạng backup hàng tháng

### Phần 7: Trách nhiệm và liên hệ
- IT Admin: thực hiện và giám sát backup hàng ngày
- IT Manager: review báo cáo hàng tháng, phê duyệt DR drill
- Liên hệ khẩn cấp khi xảy ra sự cố mất dữ liệu

## Định dạng & Lưu trữ
- Format: .docx
- Đặt tên: `[SOP/YYYY] IT-SOP-001 - Backup Phục Hồi Dữ Liệu - IT Dept v1.0`
- Thư mục: `05 Sản phẩm & CN / 04 SOP`
- Review: 6 tháng/lần hoặc sau mỗi sự cố

## Hướng dẫn cho Claude
1. Bắt đầu bằng việc xác định RTO và RPO — đây là nền tảng thiết kế toàn bộ chiến lược backup.
2. Giúp người dùng phân loại dữ liệu theo mức độ quan trọng trước khi quy định tần suất backup.
3. Nhấn mạnh nguyên tắc 3-2-1: 3 bản sao, 2 loại media khác nhau, 1 bản offsite.
4. Luôn bao gồm quy trình Restore Drill — backup không được test = không đáng tin cậy.
5. Gợi ý công cụ backup phù hợp với quy mô (Veeam, Acronis, AWS Backup, Backblaze...).
6. Nhắc yêu cầu lưu trữ pháp lý của Việt Nam: hóa đơn điện tử 10 năm, hồ sơ nhân sự 5 năm.
