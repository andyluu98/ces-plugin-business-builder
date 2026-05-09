# Lộ Trình Phát Triển Sản Phẩm (Product Roadmap) | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này trình bày lộ trình phát triển sản phẩm trong vòng 12–18 tháng tới, thể hiện thứ tự ưu tiên các sáng kiến, timeline dự kiến và mục tiêu chiến lược tương ứng. Roadmap là công cụ giao tiếp nội bộ giúp toàn đội ngũ — từ lãnh đạo đến kỹ thuật — hiểu rõ hướng đi và cam kết của bộ phận sản phẩm.

## Câu hỏi thu thập thông tin
1. Mục tiêu chiến lược của doanh nghiệp trong 12–18 tháng tới là gì? Bộ phận sản phẩm cần đóng góp gì vào mục tiêu đó?
2. Hiện tại có những sáng kiến/tính năng nào đang được cân nhắc đưa vào roadmap? Danh sách tạm thời là gì?
3. Tiêu chí ưu tiên hóa nào đang được dùng (RICE, MoSCoW, Impact vs Effort, OKR alignment)?
4. Các milestone quan trọng nào cần đạt được (ra mắt sản phẩm, hội chợ, mùa kinh doanh cao điểm)?
5. Nguồn lực kỹ thuật hiện có (số developer, velocity của team) có thể cam kết bao nhiêu capacity mỗi quý?
6. Phụ thuộc nào bên ngoài team (third-party, legal, infrastructure) có thể ảnh hưởng đến timeline?
7. Ai là các stakeholder cần được roadmap này phục vụ (ban lãnh đạo, sales, engineering, khách hàng)?

## Cấu trúc tài liệu

### Phần 1: Tóm tắt chiến lược sản phẩm
- Vision sản phẩm (1-2 câu)
- Mục tiêu năm (aligned với OKRs công ty)
- Nguyên tắc ưu tiên hóa đang áp dụng

### Phần 2: Roadmap theo quý (Q1–Q4 / Q1–Q6)
Với mỗi quý:
- **Theme chiến lược** (ví dụ: "Tăng retention", "Mở rộng B2B")
- **Danh sách sáng kiến** theo mức ưu tiên: Now / Next / Later
- **Mục tiêu đo lường** (KPI mỗi quý)
- **Capacity dự kiến** (story points hoặc % team)

### Phần 3: Chi tiết từng sáng kiến
Với mỗi item trong roadmap:
- Tên và mô tả ngắn
- Lý do ưu tiên (why now)
- Kết quả kỳ vọng (expected outcome)
- Mức độ nỗ lực ước tính (T-shirt sizing: S/M/L/XL)
- Phụ thuộc và rủi ro
- Team phụ trách

### Phần 4: Backlog (chưa lên lịch)
- Danh sách ý tưởng/yêu cầu đang chờ đánh giá
- Lý do chưa đưa vào roadmap

### Phần 5: Lịch sử thay đổi roadmap
- Các điều chỉnh lớn và lý do
- Ngày review gần nhất

## Định dạng & Lưu trữ
- Format: .xlsx (Gantt view) hoặc file Miro/Notion nếu dùng tool visual; bản PDF để chia sẻ
- Đặt tên: `[ROADMAP/YYYY] PRD-002 - Lộ Trình Sản Phẩm [Năm] - Product Team v1.0`
- Thư mục: `05 Sản phẩm & CN / 03 Roadmap`
- Phân quyền: Ban lãnh đạo, Product, Engineering; phiên bản rút gọn cho toàn công ty

## Hướng dẫn cho Claude
1. Bắt đầu bằng cách xác nhận mục tiêu chiến lược năm để đảm bảo roadmap aligned.
2. Giúp người dùng brainstorm và phân loại tất cả ý tưởng vào 3 bucket: Now / Next / Later.
3. Áp dụng khung RICE (Reach × Impact × Confidence ÷ Effort) để tính điểm ưu tiên nếu người dùng cần.
4. Tạo bảng roadmap theo quý với màu sắc phân biệt theme chiến lược.
5. Cảnh báo nếu một quý có quá nhiều sáng kiến so với capacity ước tính của team.
6. Nhắc nhở định kỳ review roadmap mỗi 6–8 tuần, không để roadmap trở thành "đá hoa cương".
