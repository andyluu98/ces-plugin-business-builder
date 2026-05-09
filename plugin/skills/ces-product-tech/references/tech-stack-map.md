# Bản Đồ Công Nghệ (Tech Stack Map) | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này lập bản đồ toàn bộ công nghệ, phần mềm, nền tảng và công cụ kỹ thuật mà doanh nghiệp đang sử dụng, bao gồm mục đích sử dụng, nhà cung cấp, chi phí và người quản lý. Đây là tài liệu tham chiếu quan trọng cho IT, ban lãnh đạo khi đưa ra quyết định công nghệ, kiểm toán chi phí và lập kế hoạch chuyển đổi số.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đang dùng những phần mềm/nền tảng nào cho các hoạt động chính: bán hàng, marketing, vận hành, kế toán, nhân sự, giao tiếp nội bộ?
2. Hạ tầng kỹ thuật (infrastructure) của doanh nghiệp là gì: on-premise server, cloud (AWS/GCP/Azure), hybrid?
3. Mỗi công cụ đang có bao nhiêu người dùng? Chi phí license hàng tháng/năm là bao nhiêu?
4. Công cụ nào đang gây khó khăn nhất (pain points) cho người dùng nội bộ?
5. Có công cụ nào trùng lặp chức năng hoặc không còn dùng nữa không?
6. Các hệ thống có kết nối (integrate) với nhau không? Dữ liệu chảy giữa các hệ thống như thế nào?
7. Kế hoạch công nghệ trong 12 tháng tới: thay thế, nâng cấp hay triển khai mới công cụ nào?

## Cấu trúc tài liệu

### Phần 1: Tổng quan hạ tầng công nghệ
- Sơ đồ kiến trúc kỹ thuật tổng quan
- Loại hạ tầng: Cloud / On-premise / Hybrid
- Nhà cung cấp dịch vụ IT chính

### Phần 2: Danh mục công nghệ theo lớp (Technology Layers)

**Lớp 1 – Hạ tầng (Infrastructure)**
- Server / Hosting / Cloud providers
- Network, VPN, Firewall
- Email hosting, Domain

**Lớp 2 – Nền tảng vận hành (Operations Platform)**
- ERP / CRM / Accounting software
- HR Management System (HRMS)
- Project Management tools

**Lớp 3 – Kinh doanh & Marketing (Business Tools)**
- CRM và Sales tools
- Marketing automation
- E-commerce platform
- Analytics & BI tools

**Lớp 4 – Giao tiếp & Cộng tác (Communication)**
- Email, Chat (Slack/Teams/Zalo)
- Video conferencing
- Document management (Drive, SharePoint)

**Lớp 5 – Bảo mật (Security)**
- Antivirus, Endpoint protection
- Password manager
- Backup solutions
- Access management (SSO, MFA)

**Lớp 6 – Phát triển sản phẩm (Product & Dev)**
- Code repositories, CI/CD
- Design tools
- Testing tools
- Monitoring & logging

### Phần 3: Bảng chi tiết từng công cụ
| Tên công cụ | Nhóm | Mục đích | Nhà cung cấp | Số user | Chi phí/tháng | Người quản lý | Ngày hết hạn |
|-------------|------|----------|--------------|---------|---------------|---------------|--------------|

### Phần 4: Sơ đồ tích hợp (Integration Map)
- Các hệ thống nào kết nối với nhau
- Luồng dữ liệu chính giữa các hệ thống
- API và middleware đang dùng

### Phần 5: Đánh giá và kế hoạch
- Công cụ cần thay thế (và lý do)
- Công cụ đang xem xét triển khai
- Ưu tiên đầu tư công nghệ theo quý

## Định dạng & Lưu trữ
- Format: .xlsx (bảng danh mục) + .docx hoặc draw.io (sơ đồ kiến trúc)
- Đặt tên: `[TECH/YYYY] IT-001 - Tech Stack Map - IT Dept v1.0`
- Thư mục: `05 Sản phẩm & CN / 05 Hạ Tầng IT`
- Review và cập nhật: 6 tháng/lần hoặc khi thêm/bỏ công cụ

## Hướng dẫn cho Claude
1. Bắt đầu bằng cách hỏi người dùng liệt kê tất cả phần mềm/công cụ đang dùng theo từng phòng ban.
2. Phân loại chúng vào các lớp công nghệ theo cấu trúc trên.
3. Tạo bảng tổng hợp với đầy đủ các cột: Tên | Nhóm | Mục đích | Chi phí | Số user | Người quản lý.
4. Tính tổng chi phí công nghệ hàng tháng và hàng năm — đây thường là con số bất ngờ cho lãnh đạo.
5. Phát hiện trùng lặp chức năng giữa các công cụ và đề xuất hợp nhất để tiết kiệm chi phí.
6. Gợi ý sơ đồ integration map bằng text/ASCII nếu có nhiều hệ thống kết nối với nhau.
