# Hướng Dẫn Thiết Kế Dashboard Quản Trị | ces-reporting

## Mục đích & Phạm vi
Tài liệu này hướng dẫn thiết kế các dashboard quản trị hiệu quả cho từng cấp lãnh đạo trong doanh nghiệp, bao gồm nguyên tắc thiết kế, lựa chọn biểu đồ phù hợp và cấu trúc bố cục tối ưu. Dashboard tốt giúp lãnh đạo nắm tình hình trong 30 giây, không cần phải đọc báo cáo dài, và phát hiện vấn đề trước khi chúng trở nên nghiêm trọng.

## Câu hỏi thu thập thông tin
1. Ai là người sẽ sử dụng dashboard này (CEO, Giám đốc phòng ban, Sales Manager)? Họ cần thấy gì đầu tiên?
2. Dashboard sẽ được xem trên thiết bị nào (màn hình lớn trên tường, laptop, điện thoại)?
3. Dữ liệu cập nhật theo tần suất nào (real-time, hàng ngày, hàng tuần)?
4. Dữ liệu đến từ nguồn nào (CRM, ERP, kế toán, Excel thủ công)?
5. Công cụ BI nào đang dùng hoặc có ngân sách đầu tư (Power BI, Looker Studio, Tableau, Metabase)?
6. Người dùng dashboard có biết cách đọc dữ liệu nâng cao không hay cần rất đơn giản?
7. Có action nào cần thực hiện khi thấy một chỉ số vượt ngưỡng không?

## Cấu trúc tài liệu

### Phần 1: Nguyên tắc thiết kế dashboard

**1.1 Nguyên tắc vàng của dashboard**
- **Mục đích trước, dữ liệu sau**: Bắt đầu bằng câu hỏi "Người dùng cần quyết định gì?", không phải "Dữ liệu nào có sẵn?"
- **Tối đa 7±2 metrics**: Con người không thể xử lý quá nhiều thông tin cùng lúc
- **Phân cấp thông tin**: Quan trọng nhất ở trên trái, chi tiết ở dưới phải (F-pattern / Z-pattern)
- **Màu sắc có ý nghĩa**: Đỏ = vấn đề, Xanh = tốt, Vàng = cần chú ý — nhất quán xuyên suốt
- **Context là vua**: Luôn hiển thị so sánh (vs. mục tiêu, vs. kỳ trước, vs. cùng kỳ năm ngoái)

**1.2 Các lỗi phổ biến cần tránh**
- Quá nhiều số, quá ít insight
- Biểu đồ 3D không cần thiết
- Màu sắc không nhất quán
- Thiếu context so sánh
- Font chữ quá nhỏ

### Phần 2: Lựa chọn loại biểu đồ phù hợp

| Mục đích | Loại biểu đồ phù hợp | Ví dụ |
|---------|---------------------|-------|
| So sánh giá trị | Bar/Column chart | Doanh số theo phòng ban |
| Xu hướng theo thời gian | Line chart | Doanh thu 12 tháng |
| Tỷ lệ phần | Donut chart (không dùng Pie 3D) | Cơ cấu doanh thu theo sản phẩm |
| Một con số quan trọng | KPI Card / Big Number | Doanh thu tháng này |
| So sánh mục tiêu | Bullet chart / Gauge | Tiến độ đạt KPI |
| Phân phối | Histogram / Box plot | Phân phối điểm NPS |
| Tương quan | Scatter plot | Chi phí vs. Doanh thu |
| Địa lý | Map chart | Doanh số theo tỉnh thành |

### Phần 3: Kiến trúc dashboard theo cấp lãnh đạo

**3.1 CEO Dashboard (Executive Summary)**
- Refresh: Hàng ngày
- Metrics (tối đa 8):
  - Doanh thu tháng (vs. mục tiêu, vs. tháng trước)
  - Lợi nhuận gộp %
  - Tiền mặt trong tay
  - Số khách hàng mới
  - NPS / Customer Satisfaction
  - Headcount và Turnover rate
  - Pipeline value
  - 1-2 KPI chiến lược của quý
- Layout: Hàng trên = KPIs tổng quan | Hàng giữa = Xu hướng | Hàng dưới = Cảnh báo

**3.2 Sales Dashboard**
- Refresh: Hàng ngày / Real-time
- Metrics: Doanh số hôm nay / tuần / tháng, Pipeline stage, Tỷ lệ chốt, Activity metrics, Leaderboard
- Đặc biệt: Forecast so với quota

**3.3 Operations Dashboard**
- Refresh: Hàng ngày
- Metrics: OTD rate, Defect rate, Capacity utilization, Thời gian xử lý, Backlog

**3.4 Finance Dashboard**
- Refresh: Hàng tuần / tháng
- Metrics: P&L summary, Cash position, Receivables aging, Budget vs. Actual, Burn rate

**3.5 HR Dashboard**
- Refresh: Hàng tháng
- Metrics: Headcount, Turnover, Recruitment pipeline, Training completion, Engagement score

### Phần 4: Quy trình thiết kế dashboard

**Bước 1 – Discovery (30 phút với user)**
- Ai dùng dashboard này?
- Quyết định nào họ đưa ra hàng ngày/tuần?
- Dữ liệu nào hiện có?

**Bước 2 – Wireframe (paper/whiteboard)**
- Vẽ tay layout trước khi lên tool
- Xác nhận với user: đây có phải những gì bạn cần không?

**Bước 3 – Prototype (tool BI)**
- Kết nối dữ liệu thực
- Tạo draft dashboard

**Bước 4 – User Testing**
- Đưa cho user thật dùng trong 1 tuần
- Ghi nhận feedback

**Bước 5 – Iterate & Publish**
- Chỉnh sửa theo feedback
- Training user cách đọc dashboard
- Lên lịch review định kỳ

### Phần 5: Tiêu chuẩn kỹ thuật
- Palette màu chuẩn (theo brand guideline)
- Font chữ: Sans-serif, tối thiểu 12pt
- Màu cảnh báo: Red (#E74C3C), Yellow (#F39C12), Green (#27AE60)
- Naming convention cho chart titles
- Chú thích nguồn dữ liệu và ngày cập nhật

## Định dạng & Lưu trữ
- Format: Tài liệu thiết kế .docx + File dashboard trong tool BI
- Đặt tên: `[MAN/YYYY] RPT-MAN-002 - Thiết Kế Dashboard [Tên] - BI Team v1.0`
- Thư mục: `09 Báo Cáo / 03 Dashboard`
- Review: Mỗi quý một lần — dashboard cần cập nhật theo thay đổi business

## Hướng dẫn cho Claude
1. Luôn bắt đầu bằng câu hỏi "User cần quyết định gì?" trước khi nghĩ đến biểu đồ hay layout.
2. Tạo wireframe text/ASCII đơn giản để người dùng hình dung layout trước khi đầu tư thời gian vào tool.
3. Giới hạn nghiêm ngặt ở 5-8 KPI mỗi dashboard — nhiều hơn thì phải tạo dashboard riêng.
4. Gợi ý luôn có "context" cho mỗi số: so vs. mục tiêu, vs. tháng trước, vs. cùng kỳ năm ngoái.
5. Đề xuất công cụ phù hợp với ngân sách: Looker Studio (miễn phí), Metabase (open source), Power BI (phổ biến tại VN).
6. Nhắc rằng dashboard tốt nhất là dashboard được dùng hàng ngày — đơn giản và nhanh > phức tạp và đầy đủ.
