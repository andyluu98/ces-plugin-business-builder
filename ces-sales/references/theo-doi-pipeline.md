# Hệ Thống Theo Dõi Pipeline Bán Hàng | ces-sales

## Mục đích & Phạm vi
Tài liệu này hướng dẫn xây dựng và vận hành hệ thống theo dõi pipeline bán hàng hiệu quả, giúp đội ngũ sales và quản lý nắm rõ trạng thái từng cơ hội bán hàng, dự báo doanh thu chính xác và ưu tiên nguồn lực đúng chỗ. Áp dụng cho toàn bộ đội ngũ sales.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đang dùng công cụ gì để quản lý pipeline? (Excel, CRM, phần mềm riêng?)
2. Chu kỳ bán hàng trung bình của doanh nghiệp là bao lâu?
3. Hiện tại pipeline có bao nhiêu deal đang theo dõi? Giá trị trung bình mỗi deal?
4. Đội sales có bao nhiêu người? Mỗi người quản lý bao nhiêu deal cùng lúc?
5. Các giai đoạn (stage) trong pipeline hiện tại được định nghĩa như thế nào?
6. Tần suất review pipeline hiện tại là bao lâu? (Hàng ngày, tuần, tháng?)
7. Mục tiêu doanh thu tháng/quý là bao nhiêu? Tỷ lệ chốt sale kỳ vọng?

## Cấu trúc tài liệu

### Phần 1: Thiết Kế Pipeline Stages
- Định nghĩa từng stage (giai đoạn) trong pipeline:
  - **Stage 1 — Lead**: Có thông tin liên hệ, chưa đủ điều kiện
  - **Stage 2 — Qualified**: Đủ điều kiện BANT, có nhu cầu thực
  - **Stage 3 — Meeting/Demo**: Đã hẹn gặp hoặc demo sản phẩm
  - **Stage 4 — Proposal**: Đã gửi báo giá/proposal
  - **Stage 5 — Negotiation**: Đang đàm phán điều khoản
  - **Stage 6 — Closed Won**: Đã ký hợp đồng
  - **Stage 6 — Closed Lost**: Không thành công
- Tiêu chí chuyển từ stage này sang stage khác
- Xác suất chốt sale ước tính theo từng stage (%)

### Phần 2: Thông Tin Cần Ghi Nhận Cho Mỗi Deal
- Tên deal / tên khách hàng
- Giá trị deal dự kiến (Expected Value)
- Stage hiện tại và ngày cập nhật gần nhất
- Người phụ trách (Deal Owner)
- Ngày dự kiến chốt (Expected Close Date)
- Ghi chú hoạt động gần nhất (Last Activity)
- Bước tiếp theo cụ thể (Next Action + deadline)
- Lý do có thể thất bại (Risk Flags)

### Phần 3: Cách Tính Weighted Pipeline
- Công thức: Weighted Value = Deal Value × Win Rate (%)
- Ví dụ tính toán cụ thể theo từng stage
- Phân biệt: Pipeline thô vs. Weighted Pipeline vs. Committed Forecast
- Cách dùng Weighted Pipeline để dự báo doanh thu tháng/quý

### Phần 4: Quy Trình Cập Nhật Pipeline Hàng Ngày
- Thời điểm cập nhật: cuối ngày làm việc
- Các trường bắt buộc cập nhật hàng ngày
- Quy tắc: mỗi deal phải có "Next Action" cụ thể
- Xử lý deal stale (không có hoạt động > 7/14/30 ngày)

### Phần 5: Pipeline Review Meeting
- **Daily Standup** (15 phút): deal mới, deal cần hỗ trợ, deal sắp chốt
- **Weekly Pipeline Review** (1 giờ): review toàn bộ pipeline, dự báo tuần tới
- **Monthly Business Review** (2 giờ): phân tích win/loss, điều chỉnh chiến lược
- Template agenda cho từng loại meeting
- Câu hỏi review chuẩn: "Tại sao deal này chưa chuyển stage?"

### Phần 6: Dashboard & Báo Cáo Pipeline
- Dashboard cá nhân: deal của tôi theo stage, tổng giá trị, deadline
- Dashboard team: so sánh pipeline từng sales, top deals
- Báo cáo tuần: deals mới, deals tiến triển, deals won/lost
- Biểu đồ Funnel: conversion rate giữa các stage
- Forecast vs. Actual hàng tháng

### Phần 7: Phân Tích & Cải Thiện Pipeline
- Xác định stage có tỷ lệ drop-off cao nhất
- Phân tích lý do lose deal theo stage
- Benchmark: số deal trung bình cần có để đạt target
- Cách tính Pipeline Coverage Ratio (cần ít nhất 3x target)
- Hành động cụ thể để cải thiện từng điểm yếu

## Định dạng & Lưu trữ
- Format file: .docx (hướng dẫn) + .xlsx (template theo dõi nếu dùng Excel)
- Đặt tên: [STANDARD/YYYY] SLS-006 - Hệ Thống Theo Dõi Pipeline - Phòng Sales v1.0
- Thư mục: 04 Kinh doanh & Marketing / 04 Quản Lý Pipeline & CRM
- File Excel pipeline: lưu riêng, cập nhật hàng ngày

## Hướng dẫn cho Claude
Khi được yêu cầu tạo tài liệu này:
1. Hỏi về công cụ hiện đang dùng để hướng dẫn cụ thể (Excel thì tạo template, CRM thì hướng dẫn cài đặt)
2. Tạo template Excel pipeline nếu người dùng chưa có CRM (dạng bảng có thể dùng ngay)
3. Phần Weighted Pipeline giải thích bằng ví dụ số cụ thể, dễ hiểu
4. Nhấn mạnh tầm quan trọng của "Next Action" — không có next action = deal chết
5. Điều chỉnh số ngày stale deal phù hợp với chu kỳ bán hàng của từng doanh nghiệp
6. Đặt tên file theo chuẩn và lưu đúng thư mục
