# Danh Sách Tài Khoản Hệ Thống và Phân Quyền | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này duy trì danh sách đầy đủ và cập nhật của tất cả tài khoản người dùng trên các hệ thống CNTT của doanh nghiệp, kèm theo cấp độ phân quyền tương ứng. Đây là công cụ quản trị thiết yếu giúp IT kiểm soát truy cập, phát hiện tài khoản dư thừa, và đảm bảo nguyên tắc Least Privilege được tuân thủ xuyên suốt tổ chức.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đang vận hành những hệ thống nào cần quản lý tài khoản (email, CRM, ERP, phần mềm kế toán, GitHub, AWS, Slack...)?
2. Có bao nhiêu nhân viên đang hoạt động? Cơ cấu phòng ban như thế nào?
3. Hiện tại ai đang có quyền Admin/Super Admin trên các hệ thống quan trọng?
4. Quy trình tạo tài khoản cho nhân viên mới và thu hồi khi nghỉ việc như thế nào?
5. Có nhà thầu, freelancer hoặc đối tác bên ngoài nào có tài khoản truy cập hệ thống không?
6. Tài khoản dịch vụ (service accounts) và tài khoản chia sẻ (shared accounts) nào đang tồn tại?
7. Lần gần nhất review và dọn dẹp tài khoản là khi nào?

## Cấu trúc tài liệu

### Phần 1: Chính sách phân quyền tổng quan
- Nguyên tắc Least Privilege
- Các cấp độ quyền truy cập chuẩn: Viewer / Editor / Manager / Admin / Super Admin
- Quy trình phê duyệt khi cấp quyền đặc biệt

### Phần 2: Danh sách tài khoản theo hệ thống

Với mỗi hệ thống, lập bảng:

| Tên hệ thống | Tên người dùng | Email | Phòng ban | Chức vụ | Cấp quyền | Ngày tạo | Ngày hết hạn | Ghi chú |
|-------------|---------------|-------|-----------|---------|-----------|----------|--------------|---------|

**Nhóm hệ thống cần liệt kê:**
- Hệ thống email và Google Workspace / Microsoft 365
- CRM (Salesforce, HubSpot, ...)
- Phần mềm kế toán (MISA, Fast, QuickBooks, ...)
- HR/Payroll system
- Cloud infrastructure (AWS, GCP, Azure)
- Code repository (GitHub, GitLab, Bitbucket)
- Project management (Jira, Asana, Notion, ...)
- Communication (Slack, Teams, Zalo Work)
- File storage (Google Drive, SharePoint, Dropbox)
- Các hệ thống nghiệp vụ đặc thù

### Phần 3: Danh sách tài khoản đặc quyền (Privileged Accounts)
- Super Admin và Admin của từng hệ thống
- Yêu cầu: MFA bắt buộc, review hàng quý
- Người backup khi Admin chính không có mặt

### Phần 4: Tài khoản dịch vụ và chia sẻ
- Service accounts (dùng cho automation, integration)
- Shared accounts (nếu có — ghi rõ lý do và người chịu trách nhiệm)
- Quy định bảo mật đặc biệt cho loại tài khoản này

### Phần 5: Nhà thầu và bên ngoài
- Tài khoản tạm thời cho nhà thầu, tư vấn
- Ngày hết hạn bắt buộc
- Quyền hạn giới hạn nghiêm ngặt

### Phần 6: Quy trình vòng đời tài khoản
- **Onboarding**: Tạo tài khoản trong 24h kể từ ngày đầu làm việc
- **Transfer**: Điều chỉnh quyền khi nhân viên đổi phòng ban/chức vụ
- **Offboarding**: Thu hồi tất cả tài khoản trong 4h kể từ khi nghỉ việc
- **Review định kỳ**: Kiểm tra toàn bộ danh sách hàng quý

### Phần 7: Log thay đổi
- Ngày thay đổi | Hệ thống | Tài khoản | Loại thay đổi | Người thực hiện | Phê duyệt bởi

## Định dạng & Lưu trữ
- Format: .xlsx (mỗi sheet = 1 hệ thống) — BẢO MẬT CAO
- Đặt tên: `[CONFIDENTIAL/YYYY] IT-ACC-001 - Danh Sách Tài Khoản Hệ Thống - IT Dept v1.0`
- Thư mục: `05 Sản phẩm & CN / 07 Quản Lý Tài Khoản` — Hạn chế truy cập: chỉ IT Admin và CEO
- Mã hóa file và đặt password bắt buộc

## Hướng dẫn cho Claude
1. Cảnh báo rõ đây là tài liệu tối mật — không được chia sẻ qua email hay chat thông thường.
2. Giúp người dùng tạo template bảng cho từng hệ thống quan trọng nhất trước.
3. Gợi ý tích hợp với Identity Provider (Okta, Azure AD) để quản lý tập trung thay vì spreadsheet thủ công.
4. Nhắc nguyên tắc quan trọng: ngay khi nhân viên nghỉ việc phải thu hồi tài khoản trong ngày.
5. Đề xuất thiết lập cảnh báo tự động khi có tài khoản không hoạt động quá 30 ngày.
6. Lên lịch Access Review hàng quý — yêu cầu mỗi manager xác nhận danh sách quyền truy cập của nhóm mình.
