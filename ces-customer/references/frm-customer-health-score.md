# Bảng Chấm Điểm Sức Khỏe Khách Hàng (Customer Health Score) | ces-customer

## Mục đích & Phạm vi
Tài liệu này hướng dẫn xây dựng hệ thống chấm điểm sức khỏe khách hàng (Customer Health Score) để phát hiện sớm khách hàng có nguy cơ rời bỏ (churn), kịp thời can thiệp và ưu tiên nguồn lực chăm sóc đúng chỗ. Đặc biệt quan trọng với doanh nghiệp có mô hình subscription/dịch vụ dài hạn.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp có mô hình subscription, hợp đồng dài hạn hay bán hàng một lần?
2. Tỷ lệ churn hiện tại là bao nhiêu %/tháng hay /năm?
3. Những dấu hiệu nào thường xuất hiện trước khi khách hàng rời bỏ (dựa trên kinh nghiệm)?
4. Dữ liệu nào doanh nghiệp đang thu thập về hành vi sử dụng của khách hàng?
5. Đội ngũ có bao nhiêu người để theo dõi và can thiệp khi phát hiện health score thấp?
6. Công cụ nào đang dùng để quản lý khách hàng? (CRM, app analytics, helpdesk...)

## Cấu trúc tài liệu

### Phần 1: Khái Niệm Customer Health Score
- Định nghĩa: điểm số tổng hợp phản ánh khả năng khách hàng tiếp tục sử dụng và phát triển cùng doanh nghiệp
- Tại sao quan trọng: phát hiện sớm churn risk trước khi quá muộn, ưu tiên can thiệp
- Nguyên tắc: Health Score không phải chỉ 1 con số — là tổng hợp nhiều tín hiệu
- Màu sắc trực quan:
  - 🟢 Green (Healthy): 70–100 điểm — khách hàng ổn định, có thể upsell
  - 🟡 Yellow (At Risk): 40–69 điểm — cần theo dõi và can thiệp nhẹ
  - 🔴 Red (Critical): 0–39 điểm — cần can thiệp khẩn cấp, nguy cơ churn cao

### Phần 2: Các Chiều Đo Lường Health Score

**Chiều 1: Mức Độ Sử Dụng (Usage/Engagement) — Trọng số 30%**
- Tần suất đăng nhập/sử dụng sản phẩm (so với baseline của người dùng tương tự)
- Số tính năng được sử dụng (breadth of adoption)
- Độ sâu sử dụng (depth of usage — dùng tính năng cơ bản hay nâng cao)
- Xu hướng: tăng, ổn định hay giảm so với tháng trước
- Điểm:
  - Sử dụng đều đặn, tăng dần: 10 điểm
  - Sử dụng ổn định: 7 điểm
  - Giảm 20–40%: 4 điểm
  - Giảm >40% hoặc không đăng nhập >14 ngày: 0–2 điểm

**Chiều 2: Kết Quả Đạt Được (Outcomes) — Trọng số 25%**
- Khách hàng có đạt được mục tiêu đặt ra ban đầu không?
- ROI thực tế so với kỳ vọng
- Milestone đã hoàn thành (onboarding checklist, kết quả đầu tiên...)
- Điểm:
  - Vượt kỳ vọng: 10 điểm
  - Đạt kỳ vọng: 7 điểm
  - Đạt một phần: 4 điểm
  - Chưa thấy kết quả: 0–2 điểm

**Chiều 3: Mức Độ Tương Tác (Relationship) — Trọng số 20%**
- Tần suất phản hồi email/liên hệ từ khách hàng
- Tham dự meeting check-in định kỳ
- Phản hồi khảo sát (NPS, CSAT)
- Tham gia webinar, sự kiện, cộng đồng
- Điểm:
  - Tương tác chủ động, phản hồi nhanh: 10 điểm
  - Phản hồi khi được liên hệ: 6 điểm
  - Ít phản hồi, thường xuyên ghosting: 2 điểm
  - Không phản hồi trong 30+ ngày: 0 điểm

**Chiều 4: Tình Trạng Tài Chính (Financial Health) — Trọng số 15%**
- Thanh toán đúng hạn không?
- Có công nợ quá hạn không?
- Xu hướng giá trị hợp đồng: tăng (upsell), ổn định hay giảm (downgrade)
- Điểm:
  - Thanh toán đúng hạn, có upsell: 10 điểm
  - Thanh toán đúng hạn, ổn định: 7 điểm
  - Chậm thanh toán 1–2 lần: 3 điểm
  - Nợ quá hạn hoặc yêu cầu giảm gói: 0 điểm

**Chiều 5: Tín Hiệu Rủi Ro (Risk Signals) — Trọng số 10%**
- Số ticket hỗ trợ mở (nhiều ticket = nhiều vấn đề)
- Có ticket nghiêm trọng chưa giải quyết không?
- Có khiếu nại, phàn nàn gần đây không?
- Có đề cập đến đối thủ hoặc giải pháp thay thế không?
- Người liên hệ chính có thay đổi không? (churn risk cao khi champion rời công ty)
- Điểm:
  - Không có rủi ro nào: 10 điểm
  - 1–2 tín hiệu nhỏ: 6 điểm
  - Nhiều tín hiệu đáng lo: 2 điểm
  - Tín hiệu khủng hoảng (đề cập hủy hợp đồng): 0 điểm

### Phần 3: Bảng Tính Health Score Tổng Hợp

| Chiều Đo | Trọng Số | Điểm Thô (0–10) | Điểm Có Trọng Số |
|----------|---------|----------------|-----------------|
| Mức độ sử dụng | 30% | ___ | ___ × 0.30 = ___ |
| Kết quả đạt được | 25% | ___ | ___ × 0.25 = ___ |
| Mức độ tương tác | 20% | ___ | ___ × 0.20 = ___ |
| Tình trạng tài chính | 15% | ___ | ___ × 0.15 = ___ |
| Tín hiệu rủi ro | 10% | ___ | ___ × 0.10 = ___ |
| **TỔNG HEALTH SCORE** | **100%** | | **___ / 10 × 10 = ___ điểm** |

**Quy đổi sang thang 100**: Tổng điểm có trọng số × 10 = Health Score (0–100)

### Phần 4: Playbook Can Thiệp Theo Màu

**🟢 Green (70–100): Healthy**
- Tần suất check-in: theo lịch thông thường (hàng quý)
- Hành động: cảm ơn, chia sẻ best practices, đề xuất upsell phù hợp, xin referral/testimonial
- Mục tiêu: duy trì và phát triển

**🟡 Yellow (40–69): At Risk**
- Tần suất check-in: tăng lên hàng tháng
- Hành động trong 48 giờ:
  - Liên hệ proactive: "Em muốn check-in xem anh/chị đang cần hỗ trợ gì không?"
  - Tìm hiểu nguyên nhân điểm thấp (usage giảm? chưa đạt kết quả?)
  - Tạo action plan cụ thể để giải quyết vấn đề
  - Cung cấp training bổ sung hoặc hỗ trợ triển khai thêm
- Mục tiêu: đưa về Green trong 30–60 ngày

**🔴 Red (0–39): Critical**
- Hành động trong 24 giờ: Account Manager / Customer Success Manager liên hệ trực tiếp
- Cuộc họp khẩn: tìm hiểu toàn diện vấn đề, không bán thêm
- Executive Sponsor: nếu là khách hàng lớn, đưa Giám đốc vào cuộc
- Recovery Plan: kế hoạch hành động chi tiết với deadline
- Nếu không cải thiện sau 30 ngày: chuẩn bị cho khả năng churn, đảm bảo offboarding tốt để mở cơ hội win-back sau

### Phần 5: Quy Trình Cập Nhật & Review Health Score
- **Tần suất cập nhật**: hàng tuần (tự động từ data) + hàng tháng (review thủ công với context)
- **Người cập nhật**: Customer Success Manager phụ trách tài khoản
- **Trigger cập nhật đột xuất**: khi có sự kiện quan trọng (khiếu nại, thanh toán trễ, key contact thay đổi)
- **Health Score Review Meeting**: hàng tháng — review toàn bộ danh sách Red + Yellow
- **Báo cáo Health Score**: phân bổ Green/Yellow/Red theo tháng, xu hướng thay đổi

### Phần 6: Tự Động Hóa Health Score
- Kết nối dữ liệu sử dụng từ hệ thống → tự động tính điểm Usage
- Kết nối CRM/Helpdesk → tự động cập nhật số ticket và tình trạng hỗ trợ
- Alert tự động: khi Health Score giảm xuống ngưỡng Yellow hoặc Red
- Công cụ gợi ý: Gainsight, ChurnZero, Totango (enterprise) / HubSpot Service Hub, custom Google Sheets (SME)

### Phần 7: KPI Hệ Thống Health Score
- % khách hàng ở từng vùng (Green/Yellow/Red) — mục tiêu >70% Green
- Churn rate theo Health Score: so sánh churn rate của Red vs. Green
- Thời gian trung bình từ Yellow → Green sau can thiệp
- Accuracy: % Red accounts thực sự churn (validate model)
- Net Revenue Retention (NRR): tổng hợp kết quả giữ chân và mở rộng

## Định dạng & Lưu trữ
- Format file: .docx (hướng dẫn) + .xlsx (bảng tính Health Score theo khách hàng)
- Đặt tên: [STANDARD/YYYY] CX-012 - Customer Health Score - Phòng CSKH v1.0
- Thư mục: 06 Khách Hàng & Dịch Vụ / 02 Quy Trình CSKH
- Cập nhật bảng tính: hàng tháng; review mô hình scoring: mỗi 6 tháng

## Hướng dẫn cho Claude
Khi được yêu cầu tạo tài liệu này:
1. Hỏi về mô hình kinh doanh (subscription vs. one-time) và dữ liệu sẵn có để thiết kế scoring phù hợp
2. Trọng số các chiều có thể điều chỉnh — hỏi người dùng chiều nào quan trọng nhất với ngành của họ
3. Tạo template Excel bảng tính Health Score với công thức tự động tính tổng điểm
4. Playbook can thiệp viết cụ thể với script liên hệ khách hàng theo từng màu
5. Với SME chưa có công cụ fancy: Google Sheets đơn giản cũng đủ dùng — hướng dẫn cụ thể
6. Đặt tên file theo chuẩn và lưu đúng thư mục
