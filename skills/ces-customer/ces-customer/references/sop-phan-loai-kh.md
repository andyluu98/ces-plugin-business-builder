# SOP Phân Loại Khách Hàng (Theo Giá Trị, Hành Vi) | ces-customer

## Mục đích & Phạm vi
Tài liệu này hướng dẫn xây dựng hệ thống phân loại khách hàng khoa học dựa trên giá trị kinh tế và hành vi mua hàng, giúp doanh nghiệp tập trung nguồn lực vào đúng phân khúc, cá nhân hóa chăm sóc và tối ưu doanh thu. Áp dụng cho toàn bộ cơ sở khách hàng hiện hữu, chạy định kỳ hàng quý.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp hiện có bao nhiêu khách hàng? Dữ liệu giao dịch đang lưu ở đâu?
2. Các tiêu chí quan trọng nhất để đánh giá giá trị khách hàng là gì?
3. Tần suất mua hàng trung bình của khách hàng là bao nhiêu lần/năm?
4. Doanh thu từ top 20% khách hàng chiếm bao nhiêu % tổng doanh thu?
5. Có khách hàng mang giá trị phi tài chính không? (Referral, review, influencer)
6. Đội ngũ CSKH có đủ để chăm sóc phân biệt theo tier không?

## Cấu trúc tài liệu

### Phần 1: Tại Sao Phân Loại Khách Hàng
- Nguyên tắc Pareto: 20% khách hàng tạo 80% doanh thu
- Chi phí giữ chân vs. tìm khách mới (x5–7 lần)
- Lợi ích: tập trung nguồn lực đúng chỗ, cá nhân hóa, tăng retention
- Rủi ro không phân loại: mất khách VIP vì thiếu quan tâm

### Phần 2: Mô Hình RFM — Phân Loại Theo Hành Vi
RFM = **R**ecency × **F**requency × **M**onetary

**Cách tính điểm (1–5 cho mỗi chiều)**:
- **Recency**: Lần mua gần nhất
  - 5: Trong 30 ngày | 4: 31–90 ngày | 3: 91–180 ngày | 2: 181–365 ngày | 1: Trên 1 năm
- **Frequency**: Số lần mua trong 12 tháng
  - 5: ≥10 lần | 4: 6–9 lần | 3: 3–5 lần | 2: 2 lần | 1: 1 lần
- **Monetary**: Tổng chi tiêu 12 tháng (phân vị)
  - 5: Top 20% | 4: 21–40% | 3: 41–60% | 2: 61–80% | 1: Bottom 20%

**Tổng điểm RFM** = R + F + M (dao động 3–15)

### Phần 3: Bảng Phân Khúc Theo RFM

| Phân Khúc | Điểm RFM | Mô Tả | Chiến Lược Chăm Sóc |
|-----------|---------|-------|-------------------|
| Champions | 13–15 | Mua nhiều, thường xuyên, gần đây | Reward, xin referral, ambassador |
| Loyal Customers | 10–12 | Thường xuyên, chi tiêu cao | Upsell, loyalty program, early access |
| Potential Loyalists | 8–9 | Tiềm năng, cần nuôi dưỡng | Onboard tốt, khuyến khích mua thêm |
| New Customers | 7–8 (R cao) | Mới mua lần đầu | Welcome series, hướng dẫn dùng |
| At Risk | 6–8 (R thấp) | Từng tốt, đang giảm | Win-back, ưu đãi đặc biệt |
| Hibernating | 4–5 | Ít mua, lâu không quay lại | Ưu đãi mạnh hoặc chấp nhận mất |
| Lost | 3 | Không mua rất lâu | Chiến dịch cuối, nếu không → archive |

### Phần 4: Phân Loại Theo Giá Trị Kinh Tế (CLV Tiers)
- **Platinum** (top 5%): CLV > X VND/năm — Account Manager riêng, ưu tiên tuyệt đối
- **Gold** (6–20%): CLV A–X VND — Check-in hàng quý, ưu đãi thành viên
- **Silver** (21–50%): CLV B–A VND — Email định kỳ, loyalty points
- **Bronze** (51–100%): CLV < B VND — Automated email, self-service

*(Điền ngưỡng CLV thực tế dựa trên doanh thu của doanh nghiệp)*

### Phần 5: Phân Loại Theo Giá Trị Phi Tài Chính
- **Brand Ambassadors**: ít mua nhưng giới thiệu nhiều khách mới → tặng referral bonus
- **Influencers/KOLs**: có ảnh hưởng online → ưu đãi đổi review/content
- **Strategic Accounts** (B2B): giá trị danh tiếng cao → chăm sóc như Platinum dù doanh thu chưa cao

### Phần 6: Quy Trình Phân Loại Định Kỳ (Hàng Quý)
1. Export dữ liệu giao dịch 12 tháng từ CRM/hệ thống bán hàng
2. Tính điểm RFM cho từng khách hàng (dùng Excel PERCENTILE hoặc CRM built-in)
3. Gán nhãn tier vào hồ sơ khách hàng trong CRM
4. Xác định khách vừa chuyển tier (lên/xuống) — kích hoạt hành động tương ứng
5. Kích hoạt chiến lược chăm sóc theo tier mới
6. Báo cáo phân bổ tier cho Ban Giám Đốc (số lượng và doanh thu theo tier)

### Phần 7: Ma Trận Chăm Sóc Theo Tier

| Tier | Kênh Ưu Tiên | Tần Suất | Loại Ưu Đãi | Người Phụ Trách |
|------|-------------|---------|------------|----------------|
| Platinum | Gặp mặt + Gọi điện | Hàng tháng | Custom, VIP access | Account Manager |
| Gold | Gọi điện + Email | Hàng quý | Loyalty points, discount | Senior CSKH |
| Silver | Email + Zalo | 2 tháng/lần | Promo code | CSKH |
| Bronze | Email tự động | Khi có promo | Mass campaign | Marketing |

### Phần 8: KPI Đo Lường Hiệu Quả Phân Loại
- % khách hàng theo từng tier và xu hướng mỗi quý
- % upgrade (tier thấp lên tier cao)
- % downgrade (tier cao xuống thấp) — cần hành động win-back
- Doanh thu trung bình theo tier và tốc độ tăng trưởng
- CLV trung bình toàn bộ khách hàng theo tháng

## Định dạng & Lưu trữ
- Format file: .docx (quy trình) + .xlsx (bảng tính RFM và template phân loại)
- Đặt tên: [STANDARD/YYYY] CX-007 - SOP Phân Loại Khách Hàng - Phòng CSKH v1.0
- Thư mục: 06 Khách Hàng & Dịch Vụ / 02 Quy Trình CSKH
- Chạy phân loại lại: hàng quý, lưu snapshot từng quý để theo dõi xu hướng

## Hướng dẫn cho Claude
Khi được yêu cầu tạo tài liệu này:
1. Hỏi về quy mô khách hàng và hệ thống dữ liệu để điều chỉnh ngưỡng RFM phù hợp
2. Tạo template Excel tính điểm RFM tự động với hướng dẫn dùng hàm PERCENTILE
3. Điều chỉnh ngưỡng CLV theo doanh thu thực tế — hỏi trước khi điền số cụ thể
4. Ví dụ minh họa: tạo bảng 5 khách hàng mẫu với điểm RFM và tier tương ứng
5. Nhấn mạnh: phân loại chỉ có giá trị khi đi kèm hành động chăm sóc khác biệt
6. Đặt tên file theo chuẩn và lưu đúng thư mục
