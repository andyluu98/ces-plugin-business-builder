# Chương Trình Loyalty & Giữ Chân Khách Hàng | ces-customer

## Mục đích & Phạm vi
Tài liệu này hướng dẫn thiết kế và vận hành chương trình loyalty (khách hàng thân thiết) hiệu quả, giúp tăng tần suất mua hàng, nâng cao Customer Lifetime Value và giảm churn rate. Áp dụng cho doanh nghiệp muốn xây dựng nền tảng khách hàng trung thành bền vững.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp đã có chương trình khách hàng thân thiết nào chưa? Hiệu quả ra sao?
2. Tỷ lệ khách hàng quay lại mua lần 2 hiện tại là bao nhiêu %?
3. Vòng đời mua hàng trung bình của khách hàng là bao lâu? (Mua bao nhiêu tháng/năm)
4. Ngân sách dành cho chương trình loyalty hàng tháng/năm là bao nhiêu?
5. Hệ thống công nghệ hiện tại có hỗ trợ tích điểm/quản lý thẻ thành viên không?
6. Đối thủ cạnh tranh đang có chương trình loyalty như thế nào?
7. Loại phần thưởng nào khách hàng của bạn quan tâm nhất? (Giảm giá, quà tặng, trải nghiệm, ưu tiên)

## Cấu trúc tài liệu

### Phần 1: Mục Tiêu & KPI Chương Trình Loyalty
- Mục tiêu kinh doanh: tăng retention rate lên X%, tăng CLV Y%, giảm churn Z%
- KPI đo lường:
  - Repeat Purchase Rate (tỷ lệ mua lại)
  - Average Purchase Frequency (tần suất mua trung bình)
  - Customer Lifetime Value (CLV)
  - Program Participation Rate (% khách tham gia chương trình)
  - Redemption Rate (% điểm được đổi thưởng)
  - Net Promoter Score (NPS) của thành viên vs. non-member

### Phần 2: Cấu Trúc Chương Trình Loyalty

**Mô hình Points-Based (Tích Điểm)**:
- Tỷ lệ tích điểm: X điểm / Y VND chi tiêu
- Giá trị quy đổi: 1 điểm = Z VND (hoặc % giảm giá)
- Điểm có hạn sử dụng không? (Thường 12–24 tháng)
- Điểm thưởng bonus: sinh nhật, mua lần đầu, viết review, giới thiệu bạn
- Cách kiểm tra số điểm: app, website, nhắn tin

**Mô hình Tiered Membership (Hạng Thành Viên)**:

| Hạng | Điều Kiện | Quyền Lợi |
|------|----------|----------|
| Bronze | Đăng ký thành viên | Tích điểm cơ bản, sinh nhật ưu đãi |
| Silver | Chi tiêu ≥ X VND/năm | Điểm x1.5, ưu tiên CSKH, giảm 5% |
| Gold | Chi tiêu ≥ Y VND/năm | Điểm x2, giao hàng miễn phí, giảm 10% |
| Platinum | Chi tiêu ≥ Z VND/năm | Điểm x3, Account Manager, ưu đãi exclusive |

**Mô hình Subscription/Membership Fee**:
- Phí thành viên hàng năm: X VND
- Lợi ích vượt trội so với phí: giao miễn phí không giới hạn, giảm X%, trải nghiệm VIP
- Phù hợp khi: khách mua thường xuyên và lợi ích dễ nhận thấy (Amazon Prime model)

### Phần 3: Cơ Chế Tích Điểm Chi Tiết
- Điểm cơ bản: mỗi giao dịch mua hàng
- Điểm bonus theo sự kiện:
  - Đăng ký thành viên mới: +X điểm chào mừng
  - Sinh nhật tháng: +Y điểm hoặc quà tặng
  - Mua trong ngày đặc biệt (11/11, Black Friday): điểm x2
  - Giới thiệu bạn thành công: +Z điểm
  - Viết review sản phẩm: +A điểm
  - Đạt hạng mới: +B điểm thưởng
- Điểm bị trừ khi: hoàn tiền, hủy đơn hàng

### Phần 4: Cơ Chế Đổi Thưởng
- **Đổi thành voucher giảm giá**: X điểm = Y VND giảm giá
- **Đổi thành sản phẩm/quà tặng**: danh sách quà theo mức điểm
- **Đổi thành trải nghiệm**: vé sự kiện, buổi tư vấn VIP, tour tham quan...
- **Donate điểm**: quy đổi sang đóng góp từ thiện (tăng cảm xúc tích cực)
- Điều kiện đổi thưởng: điểm tối thiểu, thời hạn hiệu lực điểm
- Quy trình đổi thưởng: online, tại cửa hàng, qua app

### Phần 5: Chiến Lược Giữ Chân Khách Hàng (Retention)
- **Early Warning System**: phát hiện sớm dấu hiệu churn
  - Không mua trong X ngày (so với frequency bình thường)
  - Giảm tần suất đăng nhập app/website
  - Điểm NPS giảm
  - Liên hệ CSKH nhiều lần về cùng vấn đề
- **Retention Campaigns theo trigger**:
  - Sắp hết hạn điểm → nhắc nhở + khuyến khích đổi thưởng
  - X ngày không mua → email/Zalo "Chúng tôi nhớ bạn" + ưu đãi
  - Sắp xuống hạng → thông báo + khuyến khích đạt milestone giữ hạng
  - Sau khiếu nại được giải quyết → follow-up đặc biệt
- **Win-back Campaign** (khi đã churn):
  - Email 1: Nhắc nhở giá trị đã bỏ lỡ
  - Email 2: Ưu đãi đặc biệt "chỉ dành cho bạn"
  - Gọi điện: nếu là Gold/Platinum đã churn

### Phần 6: Truyền Thông & Kích Hoạt Chương Trình
- Kênh thông báo: email, SMS/Zalo, app push notification, tại điểm bán
- Onboarding thành viên mới: email series 3 email giải thích cách hoạt động
- Thông báo tự động: tích điểm, sắp hết hạn, đạt hạng mới, đổi thưởng thành công
- Báo cáo điểm hàng tháng: tóm tắt điểm, gợi ý cách dùng

### Phần 7: Công Nghệ & Vận Hành
- Giải pháp công nghệ theo quy mô:
  - Nhỏ: Dùng tính năng loyalty trong POS hoặc CRM hiện có
  - Vừa: Phần mềm loyalty chuyên biệt (Loyalzoo, Smile.io, Yotpo Loyalty)
  - Lớn: Xây dựng riêng hoặc enterprise solution
- Tích hợp với: website, POS, CRM, email marketing, app
- Quy trình vận hành hàng ngày: xử lý điểm, đổi thưởng, giải đáp thắc mắc
- Kiểm soát gian lận: phát hiện tích điểm bất thường, policy chống lạm dụng

### Phần 8: Đo Lường & Tối Ưu Chương Trình
- Dashboard loyalty hàng tháng: thành viên mới, điểm tích lũy, điểm đổi thưởng, redemption rate
- A/B test: bonus điểm vs. % giảm giá — loại nào thúc đẩy hành vi tốt hơn
- Phân tích cohort: nhóm khách tham gia loyalty vs. không tham gia — so sánh CLV và retention
- Review chương trình hàng năm: điều chỉnh quyền lợi, ngưỡng hạng, tỷ lệ quy đổi

## Định dạng & Lưu trữ
- Format file: .docx + bảng cơ chế điểm .xlsx
- Đặt tên: [STANDARD/YYYY] CX-008 - Chương Trình Loyalty & Retention - Phòng CSKH v1.0
- Thư mục: 06 Khách Hàng & Dịch Vụ / 05 Loyalty & Retention
- Review: hàng năm, cập nhật quyền lợi theo ngân sách và kết quả thực tế

## Hướng dẫn cho Claude
Khi được yêu cầu tạo tài liệu này:
1. Hỏi về ngân sách và quy mô khách hàng để chọn mô hình loyalty phù hợp
2. Tỷ lệ tích điểm và quy đổi phải đảm bảo doanh nghiệp vẫn có lãi — tính toán kỹ
3. Bảng so sánh quyền lợi theo tier trình bày dạng bảng trực quan, dễ hiểu
4. Gợi ý công cụ công nghệ phù hợp với quy mô và ngân sách của doanh nghiệp
5. Nhấn mạnh: chương trình loyalty thành công cần đơn giản, dễ hiểu và lợi ích rõ ràng
6. Đặt tên file theo chuẩn và lưu đúng thư mục
