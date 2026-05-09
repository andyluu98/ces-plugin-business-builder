# Từ Điển KPI Toàn Doanh Nghiệp | ces-reporting

## Mục đích & Phạm vi
Tài liệu này là từ điển chuẩn hóa toàn bộ KPI (Key Performance Indicators) được sử dụng trong doanh nghiệp, bao gồm định nghĩa chính xác, công thức tính, đơn vị đo, tần suất đo và mức benchmark tham chiếu. Mục tiêu là đảm bảo mọi phòng ban dùng cùng một ngôn ngữ đo lường, loại bỏ mâu thuẫn số liệu và tạo nền tảng cho hệ thống báo cáo đáng tin cậy.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp hiện đang theo dõi những KPI nào? Ai quyết định KPI và quyết định như thế nào?
2. Có trường hợp các phòng ban báo cáo số liệu khác nhau cho cùng một chỉ số không?
3. KPI nào quan trọng nhất với CEO? Với HĐQT? Với từng phòng ban?
4. Hiện tại KPI được tính bằng công cụ gì (Excel thủ công, phần mềm ERP, CRM, BI tool)?
5. Tần suất đo lường KPI là bao nhiêu (hàng ngày, tuần, tháng, quý)?
6. Benchmark hoặc target cho từng KPI được xác định như thế nào?
7. KPI nào đang gây tranh cãi hoặc khó đo lường nhất?

## Cấu trúc tài liệu

### Phần 1: Hướng dẫn sử dụng từ điển KPI
- Mỗi KPI có mã định danh duy nhất (KPI-FIN-001, KPI-SAL-001, ...)
- Quy trình đề xuất thêm KPI mới
- Quy trình điều chỉnh định nghĩa KPI
- Người quản trị từ điển KPI (Data Governance Owner)

### Phần 2: KPI Tài chính (Financial KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target | Benchmark |
|----|---------|-----------|-----------|--------|---------|--------|-----------|
| KPI-FIN-001 | Doanh thu thuần | Tổng doanh thu sau khi trừ chiết khấu, hàng trả | Doanh thu brut - Chiết khấu - Hàng trả | VND | Tháng | X | Ngành |
| KPI-FIN-002 | Tỷ suất lợi nhuận gộp | % lợi nhuận gộp trên doanh thu | (Doanh thu - COGS) / Doanh thu × 100 | % | Tháng | X% | Ngành |
| KPI-FIN-003 | EBITDA | Lợi nhuận trước lãi vay, thuế, khấu hao | Lợi nhuận thuần + Lãi vay + Thuế + Khấu hao | VND | Tháng | X | Ngành |
| KPI-FIN-004 | Tỷ lệ chi phí / doanh thu | % chi phí hoạt động trên doanh thu | Tổng chi phí / Doanh thu × 100 | % | Tháng | <X% | Ngành |
| KPI-FIN-005 | Dòng tiền tự do (FCF) | Tiền mặt còn lại sau đầu tư | Operating Cash Flow - Capex | VND | Tháng | Dương | N/A |
| KPI-FIN-006 | Vòng quay hàng tồn kho | Số lần hàng tồn kho được bán trong kỳ | COGS / Hàng tồn kho trung bình | Lần | Quý | X | Ngành |
| KPI-FIN-007 | Số ngày phải thu (DSO) | Số ngày trung bình để thu hồi công nợ | (Phải thu / Doanh thu) × 365 | Ngày | Tháng | <X ngày | Ngành |

### Phần 3: KPI Kinh doanh / Sales (Business KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target |
|----|---------|-----------|-----------|--------|---------|--------|
| KPI-SAL-001 | Doanh số mới | Doanh thu từ khách hàng mới trong kỳ | Tổng hợp từ CRM | VND | Tháng | X |
| KPI-SAL-002 | Tỷ lệ chốt deal | % cơ hội được chuyển thành hợp đồng | Deals won / Total deals × 100 | % | Tháng | X% |
| KPI-SAL-003 | Thời gian bán hàng (Sales Cycle) | Số ngày từ lead đến chốt | Ngày chốt - Ngày tạo lead (TB) | Ngày | Tháng | <X ngày |
| KPI-SAL-004 | Giá trị đơn hàng trung bình (AOV) | Giá trị trung bình mỗi đơn hàng | Tổng doanh thu / Số đơn | VND | Tháng | X |
| KPI-SAL-005 | Tỷ lệ upsell/cross-sell | % khách hàng mua thêm sản phẩm | Số KH upsell / Tổng KH × 100 | % | Tháng | X% |
| KPI-SAL-006 | Pipeline value | Tổng giá trị cơ hội trong pipeline | Tổng từ CRM (theo stage) | VND | Tuần | X |

### Phần 4: KPI Vận hành (Operational KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target |
|----|---------|-----------|-----------|--------|---------|--------|
| KPI-OPS-001 | Tỷ lệ đúng hạn (OTD) | % đơn hàng/dự án giao đúng hạn cam kết | Đúng hạn / Tổng × 100 | % | Tháng | ≥X% |
| KPI-OPS-002 | Tỷ lệ lỗi / Defect Rate | % sản phẩm/dịch vụ không đạt chất lượng | Số lỗi / Tổng sản phẩm × 100 | % | Tháng | <X% |
| KPI-OPS-003 | Năng suất lao động | Doanh thu tạo ra trên 1 nhân viên | Doanh thu / Số FTE | VND/người | Tháng | X |
| KPI-OPS-004 | Thời gian xử lý trung bình | Thời gian trung bình hoàn thành 1 đơn vị công việc | Tổng thời gian / Số đơn vị | Giờ/ngày | Tuần | <X |

### Phần 5: KPI Nhân sự (HR KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target |
|----|---------|-----------|-----------|--------|---------|--------|
| KPI-HR-001 | Tỷ lệ nghỉ việc (Turnover) | % nhân viên nghỉ việc trong kỳ | Số nghỉ / Bình quân NV × 100 | % | Tháng | <X% |
| KPI-HR-002 | Thời gian tuyển dụng (TTH) | Ngày từ đăng tin đến onboard | Ngày onboard - Ngày đăng tin | Ngày | Tháng | <X ngày |
| KPI-HR-003 | Employee Engagement Score | Mức độ gắn kết nhân viên | Khảo sát engagement (thang 0-100) | Điểm | Năm | ≥X |
| KPI-HR-004 | Chi phí tuyển dụng / hire | Tổng chi phí để tuyển được 1 người | Tổng chi phí / Số hire | VND/người | Quý | <X |
| KPI-HR-005 | Tỷ lệ hoàn thành đào tạo | % nhân viên hoàn thành đào tạo bắt buộc | Hoàn thành / Tổng NV × 100 | % | Quý | 100% |

### Phần 6: KPI Marketing (Marketing KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target |
|----|---------|-----------|-----------|--------|---------|--------|
| KPI-MKT-001 | Chi phí thu hút khách (CAC) | Chi phí marketing để có 1 khách hàng mới | Tổng chi phí MKT / Số KH mới | VND/KH | Tháng | <X |
| KPI-MKT-002 | Tỷ lệ chuyển đổi lead | % lead chuyển thành cơ hội kinh doanh | Leads qualified / Total leads × 100 | % | Tháng | X% |
| KPI-MKT-003 | Return on Ad Spend (ROAS) | Doanh thu tạo ra trên 1 đồng quảng cáo | Doanh thu / Chi phí quảng cáo | Lần | Tháng | ≥X |

### Phần 7: KPI Khách hàng (Customer KPIs)

| Mã | Tên KPI | Định nghĩa | Công thức | Đơn vị | Tần suất | Target |
|----|---------|-----------|-----------|--------|---------|--------|
| KPI-CUS-001 | NPS (Net Promoter Score) | Mức độ sẵn sàng giới thiệu của KH | % Promoters - % Detractors | Điểm (-100 đến 100) | Quý | ≥X |
| KPI-CUS-002 | Customer Lifetime Value (CLV) | Tổng doanh thu từ 1 KH trong suốt vòng đời | AOV × Tần suất mua × Số năm giữ chân | VND | Năm | X |
| KPI-CUS-003 | Tỷ lệ giữ chân KH (Retention) | % KH còn mua hàng ở kỳ tiếp theo | KH còn lại / KH đầu kỳ × 100 | % | Tháng/Năm | ≥X% |
| KPI-CUS-004 | Thời gian giải quyết khiếu nại | Thời gian TB xử lý khiếu nại KH | Tổng thời gian / Số khiếu nại | Giờ | Tháng | <X giờ |

## Định dạng & Lưu trữ
- Format: .xlsx (dễ lọc, tìm kiếm) + .docx (tài liệu chính thức)
- Đặt tên: `[MAN/YYYY] RPT-MAN-001 - Từ Điển KPI - CEO Office v1.0`
- Thư mục: `09 Báo Cáo / 02 Từ Điển KPI`
- Review: 6 tháng/lần; mỗi thay đổi định nghĩa phải được CEO/CFO phê duyệt

## Hướng dẫn cho Claude
1. Bắt đầu bằng 5-10 KPI quan trọng nhất với CEO thay vì cố gắng định nghĩa hết tất cả.
2. Với mỗi KPI, luôn hỏi: "Dữ liệu này lấy từ đâu? Ai sở hữu dữ liệu đó?"
3. Phát hiện và giải quyết các KPI có nhiều cách tính khác nhau — đây thường là nguồn gốc của tranh cãi số liệu.
4. Đề xuất mã hóa KPI theo phòng ban (KPI-FIN, KPI-SAL, ...) để dễ quản lý.
5. Gợi ý dùng mô hình "Balanced Scorecard" (Tài chính + Khách hàng + Quy trình + Học tập) làm khung tổ chức KPI.
6. Nhắc nhở: ít KPI nhưng đúng và được theo dõi đều đặn tốt hơn nhiều KPI nhưng không ai quan tâm.
