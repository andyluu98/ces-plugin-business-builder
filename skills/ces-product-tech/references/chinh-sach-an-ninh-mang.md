# Chính Sách An Ninh Mạng và Bảo Mật Thông Tin | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này thiết lập khung chính sách an ninh mạng và bảo mật thông tin toàn diện cho doanh nghiệp, bao gồm các biện pháp kỹ thuật, quy trình vận hành và trách nhiệm nhân sự nhằm bảo vệ tài sản thông tin khỏi các mối đe dọa nội bộ và bên ngoài. Áp dụng cho toàn bộ hệ thống CNTT, dữ liệu và nhân sự liên quan đến tài sản thông tin của công ty.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đang lưu trữ loại dữ liệu nhạy cảm nào (dữ liệu khách hàng, dữ liệu tài chính, bí mật kinh doanh, dữ liệu cá nhân theo PDPA/GDPR)?
2. Đã từng xảy ra sự cố bảo mật (hack, mất dữ liệu, lừa đảo phishing) chưa? Bài học rút ra là gì?
3. Hiện tại có những biện pháp bảo mật nào đang áp dụng (firewall, antivirus, MFA, VPN)?
4. Ai chịu trách nhiệm về an ninh mạng (CISO, IT Manager, hay thuê ngoài)?
5. Nhân viên đã được đào tạo về an ninh mạng chưa? Tần suất đào tạo?
6. Có yêu cầu tuân thủ pháp lý nào về bảo mật dữ liệu (ISO 27001, PCI-DSS, Nghị định 13/2023)?
7. Kế hoạch phản ứng khi xảy ra sự cố bảo mật (Incident Response Plan) có chưa?

## Cấu trúc tài liệu

### Phần 1: Tuyên bố chính sách và phạm vi
- Cam kết của lãnh đạo về bảo mật thông tin
- Phạm vi: hệ thống, dữ liệu, nhân sự, địa điểm
- Tài liệu tham chiếu (ISO 27001, Nghị định 13/2023 VN)

### Phần 2: Phân loại và bảo vệ thông tin
- Cấp độ phân loại: Công khai / Nội bộ / Bí mật / Tối mật
- Quy tắc xử lý từng cấp độ
- Dán nhãn tài liệu và dữ liệu số

### Phần 3: Kiểm soát truy cập (Access Control)
- Nguyên tắc Least Privilege (quyền tối thiểu cần thiết)
- Quản lý tài khoản: tạo, sửa, xóa
- Xác thực đa yếu tố (MFA) — bắt buộc với hệ thống nào
- Xem xét quyền truy cập định kỳ (Access Review)
- Tài khoản đặc quyền (Admin/Root) — quy trình quản lý

### Phần 4: Bảo mật mạng
- Phân đoạn mạng (Network Segmentation)
- Quy định firewall và quy tắc cho phép/chặn
- VPN cho remote access
- WiFi công ty: mạng cho nhân viên vs. mạng khách
- Giám sát lưu lượng mạng

### Phần 5: Bảo mật endpoint
- Yêu cầu antivirus/EDR trên tất cả thiết bị
- Cập nhật OS và phần mềm định kỳ (Patch Management)
- Mã hóa ổ đĩa (Full Disk Encryption)
- Chính sách màn hình khóa tự động

### Phần 6: Bảo mật dữ liệu
- Mã hóa dữ liệu lưu trữ và truyền tải
- Kiểm soát thiết bị lưu trữ ngoài (USB, external HDD)
- Chính sách xóa dữ liệu an toàn (Data Sanitization)
- Data Loss Prevention (DLP)

### Phần 7: Quản lý sự cố bảo mật
- Định nghĩa các loại sự cố (mức độ 1-3)
- Quy trình phát hiện và báo cáo sự cố
- Escalation path (ai báo cho ai)
- Quy trình điều tra và khắc phục
- Thông báo cho cơ quan có thẩm quyền (nếu bắt buộc)
- Bài học kinh nghiệm sau sự cố

### Phần 8: Nâng cao nhận thức bảo mật
- Chương trình đào tạo bảo mật cho nhân viên
- Phishing simulation định kỳ
- Kênh báo cáo sự cố (đường dây nóng IT)

### Phần 9: Tuân thủ và kiểm toán
- Audit bảo mật nội bộ định kỳ
- Kiểm tra thâm nhập (Penetration Testing) — tần suất
- Báo cáo tuân thủ cho ban lãnh đạo

## Định dạng & Lưu trữ
- Format: .docx
- Đặt tên: `[POL/YYYY] IT-POL-002 - An Ninh Mạng Bảo Mật TT - IT Dept v1.0`
- Thư mục: `05 Sản phẩm & CN / 06 Chính Sách IT`
- Review: 12 tháng/lần hoặc sau mỗi sự cố bảo mật lớn

## Hướng dẫn cho Claude
1. Hỏi ngành nghề và quy mô để xác định mức độ rủi ro bảo mật và yêu cầu tuân thủ pháp lý phù hợp.
2. Luôn đề cập đến Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân của Việt Nam.
3. Phần Incident Response Plan nên có sơ đồ luồng quyết định rõ ràng (ai làm gì khi phát hiện sự cố).
4. Tạo danh sách kiểm tra bảo mật (Security Checklist) theo từng vai trò: IT Admin, Nhân viên thông thường, Manager.
5. Gợi ý thực hiện Security Awareness Training ít nhất 2 lần/năm với nội dung thực tế (phishing, social engineering).
6. Nhắc nhở người dùng rằng chính sách bảo mật cần được luật sư hoặc chuyên gia bảo mật review trước khi ban hành.
