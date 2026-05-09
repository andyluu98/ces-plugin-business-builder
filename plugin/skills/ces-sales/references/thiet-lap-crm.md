# Hướng Dẫn Thiết Lập và Sử Dụng CRM | ces-sales

## Mục đích & Phạm vi
Tài liệu này hướng dẫn doanh nghiệp lựa chọn, thiết lập và vận hành hệ thống CRM (Customer Relationship Management) hiệu quả, đảm bảo đội ngũ sales sử dụng nhất quán và khai thác tối đa giá trị của công cụ. Áp dụng cho giai đoạn triển khai CRM mới hoặc chuẩn hóa CRM hiện có.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp hiện đang dùng CRM nào? (HubSpot, Salesforce, Pipedrive, Zoho, tự xây, hay chưa có?)
2. Quy mô đội sales và số lượng khách hàng/lead cần quản lý hàng tháng là bao nhiêu?
3. Ngân sách cho phần mềm CRM hàng tháng là bao nhiêu?
4. Những tính năng CRM nào quan trọng nhất với doanh nghiệp? (Pipeline, email automation, báo cáo...)
5. Dữ liệu khách hàng hiện tại đang lưu ở đâu? (Excel, Google Sheets, phần mềm khác?)
6. Đội sales có kỹ năng công nghệ ở mức nào? Cần CRM đơn giản hay phức tạp?
7. Có tích hợp với công cụ khác không? (Email marketing, kế toán, CSKH...)

## Cấu trúc tài liệu

### Phần 1: Lựa Chọn CRM Phù Hợp
- Tiêu chí đánh giá CRM: tính năng, giá, ease of use, hỗ trợ tiếng Việt
- Bảng so sánh top CRM phổ biến tại Việt Nam:
  - **Miễn phí / Chi phí thấp**: HubSpot Free, Bitrix24, Zoho CRM
  - **Trung bình**: Pipedrive, Freshsales, Base CRM
  - **Cao cấp**: Salesforce, HubSpot Pro
- Gợi ý theo quy mô doanh nghiệp (1-5 sales / 5-20 sales / 20+ sales)
- Checklist đánh giá trước khi quyết định

### Phần 2: Thiết Lập CRM Ban Đầu
- Cài đặt thông tin công ty và branding
- Tạo tài khoản và phân quyền người dùng (Admin / Manager / Sales Rep)
- Thiết lập Pipeline stages theo quy trình bán hàng của doanh nghiệp
- Tùy chỉnh các trường dữ liệu (Custom Fields) cần thiết
- Cài đặt thông báo và nhắc nhở tự động

### Phần 3: Cấu Trúc Dữ Liệu Trong CRM
- **Contacts**: thông tin cá nhân người liên hệ
- **Companies/Accounts**: thông tin doanh nghiệp khách hàng
- **Deals/Opportunities**: cơ hội bán hàng trong pipeline
- **Activities**: cuộc gọi, email, meeting, task
- **Products**: danh mục sản phẩm và giá
- Quy tắc đặt tên và phân loại thống nhất

### Phần 4: Import Dữ Liệu Hiện Có
- Chuẩn bị file CSV/Excel để import
- Mapping cột dữ liệu sang trường CRM
- Kiểm tra và làm sạch dữ liệu trước khi import (deduplication)
- Quy trình import và kiểm tra sau import
- Xử lý lỗi import phổ biến

### Phần 5: Quy Trình Sử Dụng Hàng Ngày
- **Buổi sáng**: review task và deal cần follow-up hôm nay
- **Trong ngày**: log mọi hoạt động ngay sau khi thực hiện (cuộc gọi, email, meeting)
- **Cuối ngày**: cập nhật stage deal, đặt next action cho ngày hôm sau
- Quy tắc bắt buộc: KHÔNG để deal không có next action
- Mobile app: cách dùng CRM trên điện thoại khi đi thực địa

### Phần 6: Tự Động Hóa (Automation)
- Tự động gửi email follow-up sau khi tạo deal mới
- Tự động nhắc nhở khi deal không có hoạt động > X ngày
- Tự động phân công lead cho sales theo vùng/sản phẩm
- Tự động tạo task khi deal chuyển stage
- Email sequences cho nurturing lead chưa sẵn sàng mua

### Phần 7: Báo Cáo & Dashboard
- Dashboard cá nhân: KPI của tôi, deal sắp đến hạn
- Dashboard team: pipeline tổng thể, leaderboard
- Báo cáo doanh số: thực tế vs. target theo tuần/tháng
- Báo cáo hoạt động: số cuộc gọi, email, meeting của từng sales
- Báo cáo win/loss: phân tích tỷ lệ và lý do

### Phần 8: Quy Định Sử Dụng CRM
- Bắt buộc: mọi deal phải được tạo trong CRM trước khi tiếp cận
- Bắt buộc: cập nhật CRM trong vòng 24 giờ sau mỗi tương tác
- Cấm: xóa deal hoặc contact mà không có phê duyệt
- Cấm: lưu thông tin khách hàng ra ngoài CRM (file cá nhân)
- Quy trình báo lỗi và yêu cầu hỗ trợ kỹ thuật

### Phần 9: Đào Tạo & Onboarding Sales Mới
- Checklist onboarding CRM cho nhân viên mới
- Video hướng dẫn sử dụng (link nội bộ)
- Bài tập thực hành: tạo deal, log activity, tạo báo cáo
- Người hỗ trợ nội bộ (CRM Champion)

## Định dạng & Lưu trữ
- Format file: .docx
- Đặt tên: [STANDARD/YYYY] CRM-001 - Hướng Dẫn Thiết Lập và Sử Dụng CRM - Phòng Sales v1.0
- Thư mục: 04 Kinh doanh & Marketing / 04 Quản Lý Pipeline & CRM
- Cập nhật: mỗi khi nâng cấp phiên bản CRM hoặc thay đổi quy trình

## Hướng dẫn cho Claude
Khi được yêu cầu tạo tài liệu này:
1. Hỏi về CRM cụ thể đang dùng hoặc dự định dùng để viết hướng dẫn phù hợp
2. Nếu chưa có CRM, gợi ý HubSpot Free hoặc Bitrix24 cho SME mới bắt đầu
3. Phần thiết lập pipeline stages phải khớp với quy trình bán hàng đã có của doanh nghiệp
4. Tạo checklist onboarding ngắn gọn để sales mới dùng ngay tuần đầu
5. Nhấn mạnh văn hóa CRM: công cụ chỉ hiệu quả khi mọi người dùng đúng và đủ
6. Đặt tên file theo chuẩn và lưu đúng thư mục
