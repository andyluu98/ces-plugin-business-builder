# SOP Quy Trình Phát Triển Sản Phẩm Mới (NPD) | ces-product-tech

## Mục đích & Phạm vi
Tài liệu này định nghĩa quy trình chuẩn (Standard Operating Procedure) cho toàn bộ vòng đời phát triển sản phẩm mới — từ giai đoạn ý tưởng ban đầu đến khi sản phẩm được ra mắt thị trường và bàn giao vận hành. SOP áp dụng cho tất cả dự án phát triển sản phẩm/dịch vụ mới hoặc cải tiến lớn, đảm bảo tính nhất quán, kiểm soát chất lượng và phối hợp liên phòng ban hiệu quả.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đang dùng phương pháp phát triển sản phẩm nào (Agile/Scrum, Stage-Gate, Design Thinking, Lean Startup)?
2. Ai là người có quyền phê duyệt ý tưởng, ngân sách và quyết định ra mắt sản phẩm?
3. Các phòng ban nào tham gia vào quá trình phát triển sản phẩm (Product, Tech, Marketing, Sales, Operations, Legal)?
4. Thời gian trung bình từ ý tưởng đến ra mắt sản phẩm hiện tại là bao lâu? Có bottleneck nào không?
5. Doanh nghiệp dùng công cụ quản lý dự án nào (Jira, Asana, Notion, Trello)?
6. Quy trình kiểm thử và đảm bảo chất lượng trước khi ra mắt là gì?
7. Có yêu cầu tuân thủ pháp lý hay tiêu chuẩn ngành nào cần tích hợp vào quy trình không?

## Cấu trúc tài liệu

### Phần 1: Thông tin SOP
- Mã SOP, phiên bản, ngày hiệu lực
- Người soạn thảo, người phê duyệt
- Phạm vi áp dụng
- Tài liệu liên quan

### Phần 2: Định nghĩa và từ viết tắt
- NPD: New Product Development
- MVP: Minimum Viable Product
- Gate Review: Điểm kiểm soát chuyển giai đoạn
- PMF: Product-Market Fit
- GTM: Go-to-Market

### Phần 3: Tổng quan quy trình (Stage-Gate)

**Stage 0 – Khám phá ý tưởng (Discovery)**
- Nguồn ý tưởng: khách hàng, nhân viên, thị trường, R&D
- Công cụ: Brainstorming, Customer Interview, Market Research
- Output: Idea Brief (1 trang)
- Gate 0: Ủy ban sản phẩm xem xét, quyết định tiến/loại

**Stage 1 – Nghiên cứu sơ bộ (Scoping)**
- Phân tích thị trường nhanh
- Đánh giá kỹ thuật sơ bộ
- Ước tính nguồn lực
- Output: Product Brief
- Gate 1: Leadership review, phê duyệt ngân sách nghiên cứu

**Stage 2 – Xây dựng Business Case**
- Nghiên cứu khách hàng chuyên sâu (User Research)
- Phân tích tài chính (ROI, break-even)
- Kế hoạch dự án chi tiết
- Output: Business Case + Project Plan
- Gate 2: Ban Giám đốc phê duyệt đầu tư

**Stage 3 – Phát triển (Development)**
- Thiết kế UX/UI (nếu có)
- Phát triển MVP hoặc prototype
- Kiểm thử nội bộ (Alpha testing)
- Output: MVP / Prototype sẵn sàng test
- Gate 3: Product & Tech review chất lượng

**Stage 4 – Kiểm thử & Xác nhận (Testing & Validation)**
- Beta testing với nhóm khách hàng chọn lọc
- Đo lường PMF (Product-Market Fit)
- Hoàn thiện theo phản hồi
- Output: Sản phẩm finalized + GTM Plan
- Gate 4: Go/No-Go decision từ Ban Giám đốc

**Stage 5 – Ra mắt (Launch)**
- Thực thi GTM Plan
- Đào tạo đội ngũ Sales & Support
- Monitoring sau ra mắt (30-60-90 ngày)
- Output: Launch Report

**Stage 6 – Review sau ra mắt (Post-Launch Review)**
- So sánh kết quả vs. kế hoạch
- Bài học kinh nghiệm (Lessons Learned)
- Quyết định tiếp theo: Scale / Pivot / Sunset

### Phần 4: Ma trận RACI
| Hoạt động | Product | Tech | Marketing | Sales | Operations | CEO |
|-----------|---------|------|-----------|-------|------------|-----|
| Phê duyệt ý tưởng | R | C | C | C | I | A |
| Business Case | R | C | C | C | C | A |
| Phát triển MVP | C | R | I | I | I | I |
| Go/No-Go Launch | R | C | C | C | C | A |

### Phần 5: Mẫu biểu và công cụ
- Template Idea Brief
- Template Business Case
- Checklist Gate Review
- Checklist Launch Readiness

### Phần 6: Chỉ số đo lường quy trình
- Time-to-Market (từ Gate 0 đến Launch)
- Tỷ lệ ý tưởng qua từng Gate
- Chi phí phát triển vs. ngân sách
- NPS sản phẩm sau 90 ngày ra mắt

## Định dạng & Lưu trữ
- Format: .docx với bảng RACI và flowchart quy trình
- Đặt tên: `[SOP/YYYY] PRD-SOP-001 - Phát Triển Sản Phẩm Mới - Product Team v1.0`
- Thư mục: `05 Sản phẩm & CN / 04 SOP`
- Review định kỳ: 12 tháng/lần hoặc khi thay đổi phương pháp luận

## Hướng dẫn cho Claude
1. Hỏi về phương pháp phát triển hiện tại để điều chỉnh Stage-Gate phù hợp (có thể kết hợp Agile Sprint trong Stage 3).
2. Xác nhận ai là người ra quyết định tại mỗi Gate — đây là thông tin quan trọng nhất của SOP.
3. Tạo flowchart dạng text/ASCII cho toàn bộ quy trình để dễ hình dung.
4. Soạn ma trận RACI dựa trên cơ cấu tổ chức thực tế của doanh nghiệp.
5. Gợi ý các checklist cụ thể cho mỗi Gate Review để tránh bỏ sót tiêu chí.
6. Nhắc người dùng rằng SOP cần được pilot test với 1 dự án trước khi áp dụng toàn công ty.
