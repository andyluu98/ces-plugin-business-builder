# Kế hoạch Duy trì Kinh doanh trong Khủng hoảng (BCP) | ces-strategy

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng Business Continuity Plan (BCP) - kế hoạch đảm bảo doanh nghiệp tiếp tục hoạt động trong và sau các tình huống gián đoạn nghiêm trọng như thiên tai, dịch bệnh, sự cố công nghệ, mất nhân sự chủ chốt hoặc khủng hoảng tài chính. BCP giúp giảm thiểu tác động, rút ngắn thời gian phục hồi và duy trì niềm tin của khách hàng và đối tác. Phù hợp cho mọi quy mô doanh nghiệp, đặc biệt là các ngành dịch vụ và sản xuất quan trọng.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp hoạt động trong ngành nào? Các quy trình và dịch vụ nào là quan trọng nhất và không thể gián đoạn?
2. Những rủi ro gián đoạn nào có xác suất cao nhất với doanh nghiệp của bạn? (Mất điện, thiên tai, sự cố IT, dịch bệnh, mất nhân sự chủ chốt...)
3. Nếu hệ thống chính ngừng hoạt động, doanh nghiệp có thể chịu đựng được bao lâu? (RTO - Recovery Time Objective)
4. Dữ liệu quan trọng nhất của doanh nghiệp là gì? Hiện đang được sao lưu như thế nào và ở đâu?
5. Ai là nhân sự không thể thay thế? Nếu họ không thể làm việc, ai là người kế nhiệm?
6. Doanh nghiệp có cơ sở vật chất dự phòng, hệ thống backup hoặc nhà cung cấp thay thế không?
7. Khách hàng nào và hợp đồng nào là ưu tiên cao nhất cần bảo vệ trong khủng hoảng?

## Cấu trúc tài liệu

### Phần 1: Tổng quan BCP
- Mục đích và phạm vi áp dụng của BCP
- Định nghĩa: BCP vs DRP (Disaster Recovery Plan) vs Crisis Management
- Nguyên tắc: Prioritize People → Operations → Reputation → Financial
- Người chịu trách nhiệm BCP (Business Continuity Manager)
- Chu kỳ review và cập nhật BCP: hàng năm và sau mỗi sự cố

### Phần 2: Phân tích Tác động Kinh doanh (BIA - Business Impact Analysis)

#### 2.1 Danh sách Quy trình Kinh doanh Quan trọng
| Quy trình | Phòng ban | Mức độ quan trọng | Thời gian chịu đựng tối đa | RTO | RPO |
|-----------|-----------|-------------------|---------------------------|-----|-----|
| [QT1]     | ...       | Rất cao           | 4 giờ                     | 2h  | 1h  |
| [QT2]     | ...       | Cao               | 24 giờ                    | 8h  | 4h  |

*RTO: Recovery Time Objective - thời gian khôi phục mục tiêu*
*RPO: Recovery Point Objective - điểm dữ liệu mục tiêu có thể mất*

#### 2.2 Tác động Tài chính khi Gián đoạn
- Chi phí gián đoạn mỗi giờ/ngày theo từng quy trình
- Tổng thiệt hại ước tính theo kịch bản gián đoạn 1 ngày / 1 tuần / 1 tháng
- Khách hàng và hợp đồng có nguy cơ mất nếu gián đoạn kéo dài

### Phần 3: Đánh giá Rủi ro Gián đoạn

#### 3.1 Danh sách Rủi ro
| Rủi ro | Xác suất | Mức độ tác động | Điểm rủi ro | Ưu tiên |
|--------|----------|-----------------|-------------|---------|
| Mất điện kéo dài | Trung bình | Cao | 12 | 1 |
| Sự cố hệ thống IT | Cao | Rất cao | 20 | 1 |
| Dịch bệnh/cách ly | Thấp | Rất cao | 15 | 2 |
| Mất nhân sự chủ chốt | Trung bình | Cao | 12 | 2 |
| Thiên tai | Thấp | Rất cao | 10 | 3 |

#### 3.2 Kiểm soát Hiện tại
- Danh sách biện pháp kiểm soát rủi ro hiện đang áp dụng
- Đánh giá hiệu quả của từng biện pháp
- Khoảng trống cần bổ sung

### Phần 4: Kế hoạch Ứng phó theo Từng Kịch bản

#### Kịch bản 1: Sự cố Hệ thống IT / Mất dữ liệu
**Trigger:** Hệ thống chính ngừng hoạt động hoặc bị tấn công mạng

Giờ 0-2 (Phát hiện & Đánh giá):
- Ai được thông báo đầu tiên? Kênh thông báo nào?
- Ai ra quyết định khai báo tình trạng khẩn cấp?
- Quy trình đánh giá ban đầu: phạm vi và mức độ nghiêm trọng

Giờ 2-24 (Ứng phó Ngay lập tức):
- Kích hoạt hệ thống backup như thế nào?
- Quy trình làm việc thủ công thay thế
- Thông báo cho khách hàng và đối tác
- Đội kỹ thuật khắc phục sự cố

Ngày 2-7 (Phục hồi):
- Lộ trình khôi phục từng bước
- Kiểm tra và xác nhận dữ liệu sau khôi phục
- Đánh giá và ghi nhận bài học

#### Kịch bản 2: Mất Nhân sự Chủ chốt
[Cấu trúc tương tự]

#### Kịch bản 3: Gián đoạn Cơ sở Vật chất (thiên tai, hỏa hoạn)
[Cấu trúc tương tự]

#### Kịch bản 4: Dịch bệnh / Cách ly hàng loạt
[Cấu trúc tương tự]

#### Kịch bản 5: Khủng hoảng Tài chính (dòng tiền cạn kiệt)
[Cấu trúc tương tự]

### Phần 5: Nguồn lực Dự phòng

#### 5.1 Nhân sự Kế nhiệm
| Vị trí chủ chốt | Người hiện tại | Người kế nhiệm 1 | Người kế nhiệm 2 | Mức sẵn sàng |
|-----------------|---------------|------------------|------------------|--------------|
| CEO             | ...           | ...              | ...              | Cao/TB/Thấp  |
| CFO             | ...           | ...              | ...              | ...          |

#### 5.2 Hệ thống và Công nghệ Dự phòng
- Backup dữ liệu: tần suất, địa điểm lưu trữ, kiểm tra định kỳ
- Phần mềm thay thế khẩn cấp
- Thiết bị dự phòng
- Kế hoạch làm việc từ xa (remote work)

#### 5.3 Nhà cung cấp Thay thế
| Nhà cung cấp chính | Hàng hóa/DV | Nhà cung cấp thay thế | Thời gian chuyển đổi |
|--------------------|-------------|----------------------|----------------------|

#### 5.4 Tài chính Dự phòng
- Quỹ dự phòng khủng hoảng: mức tối thiểu cần duy trì
- Hạn mức tín dụng khẩn cấp đã được phê duyệt
- Tài sản có thể thanh lý nhanh nếu cần

### Phần 6: Truyền thông Khủng hoảng
- Danh sách liên lạc khẩn cấp (nội bộ và bên ngoài)
- Template thông báo cho từng nhóm đối tượng:
  - Nhân viên
  - Khách hàng ưu tiên
  - Đối tác và nhà cung cấp
  - Báo chí (nếu cần)
- Người phát ngôn chính thức và người dự phòng
- Kênh truyền thông khẩn cấp

### Phần 7: Kiểm tra và Diễn tập BCP
- Lịch kiểm tra BCP hàng năm: tabletop exercise và thực hành
- Quy trình đánh giá sau kiểm tra
- Cập nhật BCP dựa trên kết quả kiểm tra

## Định dạng & Lưu trữ
- Format: .docx (bản đầy đủ) + tóm tắt 1 trang (Quick Reference Card)
- BCP phải in ra và lưu cả bản cứng ở vị trí an toàn
- Đặt tên: [BCP/YYYY] STR-016 - Ke Hoach Duy Tri Kinh Doanh - BGD v[X.X]
- Thư mục lưu: 01-Chien-Luoc/07-Quan-Ly-Rui-Ro/

## Hướng dẫn cho Claude
1. BIA (Business Impact Analysis) là nền tảng của BCP - không có BIA tốt thì BCP sẽ sai trọng tâm.
2. Kế hoạch ứng phó phải đủ chi tiết để người không quen việc cũng thực hiện được trong tình huống hỗn loạn.
3. RTO và RPO phải thực tế - đừng đặt mục tiêu khôi phục trong 1 giờ nếu không có hệ thống hot standby.
4. Phần nhân sự kế nhiệm thường bị bỏ qua nhưng là rủi ro lớn nhất của SME Việt Nam.
5. BCP phải được test thực tế ít nhất 1 lần/năm - tài liệu không được test là tài liệu chết.
6. Tạo Quick Reference Card (1 trang) để dán ở văn phòng và gửi cho nhân sự chủ chốt lưu trên điện thoại.
7. Lưu bản cứng ở nơi an toàn ngoài văn phòng chính - BCP không dùng được nếu văn phòng đang cháy.
