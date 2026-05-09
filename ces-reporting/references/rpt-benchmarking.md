# Template Benchmarking So Sánh Với Thị Trường | ces-reporting

## Mục đích & Phạm vi
Tài liệu này hướng dẫn thực hiện và trình bày báo cáo benchmarking — so sánh hiệu suất của doanh nghiệp với các đối thủ cạnh tranh, ngành và các công ty tốt nhất trong lĩnh vực (best-in-class). Benchmarking giúp doanh nghiệp biết mình đang đứng ở đâu trong ngành, xác định khoảng cách cần thu hẹp và học hỏi từ best practices bên ngoài.

## Câu hỏi thu thập thông tin
1. Mục đích benchmarking là gì (cải thiện hiệu suất nội bộ, thuyết phục nhà đầu tư, định giá doanh nghiệp)?
2. So sánh với ai: đối thủ trực tiếp, công ty cùng quy mô trong ngành, hay công ty tốt nhất thế giới?
3. Benchmarking tập trung vào lĩnh vực nào (tài chính, vận hành, nhân sự, marketing, sản phẩm)?
4. Nguồn dữ liệu benchmarking có sẵn là gì (báo cáo ngành, database, công ty tư vấn, dữ liệu công khai)?
5. Dữ liệu nội bộ nào có thể chia sẻ trong báo cáo này (doanh thu, margin, headcount, NPS)?
6. Tần suất benchmarking: một lần hay định kỳ hàng năm?
7. Kết quả sẽ được trình bày cho ai và dùng để ra quyết định gì?

## Cấu trúc tài liệu

### Phần 1: Phạm vi và phương pháp benchmarking

**1.1 Xác định peer group (nhóm so sánh)**
- Tiêu chí chọn đối tượng so sánh: ngành, quy mô, thị trường, giai đoạn tăng trưởng
- Danh sách công ty/chỉ số ngành được chọn để so sánh
- Nguồn dữ liệu và mức độ tin cậy

**1.2 Lĩnh vực benchmarking**
- Benchmarking tài chính (Financial benchmarking)
- Benchmarking hoạt động (Operational benchmarking)
- Benchmarking quy trình (Process benchmarking)
- Benchmarking chiến lược (Strategic benchmarking)

### Phần 2: Benchmarking Tài chính

**2.1 Bảng so sánh KPIs tài chính**

| KPI | Công ty mình | Trung vị ngành | Top quartile | Best-in-class | Khoảng cách |
|-----|-------------|--------------|--------------|--------------|------------|
| Tỷ suất lợi nhuận gộp (%) | | | | | |
| EBITDA margin (%) | | | | | |
| Tốc độ tăng trưởng doanh thu (%) | | | | | |
| CAC (Chi phí thu hút KH) | | | | | |
| LTV/CAC ratio | | | | | |
| Tỷ lệ churn (nếu SaaS/subscription) | | | | | |
| Revenue per employee | | | | | |

**2.2 Phân tích khoảng cách (Gap Analysis)**
- KPI nào đang tốt hơn trung bình ngành?
- KPI nào đang kém hơn và khoảng cách bao nhiêu?
- Nếu đạt mức top quartile, tác động tài chính là gì?

### Phần 3: Benchmarking Vận hành

| KPI Vận hành | Công ty mình | Trung vị ngành | Top quartile | Khoảng cách |
|-------------|-------------|--------------|------------|------------|
| Tỷ lệ đúng hạn (OTD) | | | | |
| Tỷ lệ lỗi (Defect Rate) | | | | |
| Thời gian xử lý đơn hàng | | | | |
| NPS / CSAT | | | | |
| Employee retention rate | | | | |
| Revenue per FTE | | | | |

### Phần 4: Benchmarking Nhân sự và Văn hóa

| KPI Nhân sự | Công ty mình | Benchmark ngành | Khoảng cách |
|------------|-------------|----------------|------------|
| Turnover rate (%) | | | |
| Thời gian tuyển dụng (ngày) | | | |
| Chi phí tuyển dụng/hire | | | |
| Employee engagement score | | | |
| Training hours/nhân viên/năm | | | |

### Phần 5: Benchmarking Sản phẩm & Đổi mới

| Chỉ số | Công ty mình | Benchmark | Nhận xét |
|--------|-------------|-----------|---------|
| % doanh thu từ sản phẩm mới (<2 năm) | | | |
| Time-to-market (ngày) | | | |
| R&D spend (% doanh thu) | | | |
| NPS sản phẩm | | | |

### Phần 6: Phân tích Best Practices
- Top 3 điều học được từ công ty tốt nhất trong ngành
- Specific practices có thể áp dụng cho doanh nghiệp mình
- Điều kiện để áp dụng thành công

### Phần 7: Kết luận và Kế hoạch hành động

**Ma trận ưu tiên:**
| KPI cần cải thiện | Mức độ khoảng cách | Khả năng cải thiện | Ưu tiên |
|------------------|------------------|-------------------|--------|

**Kế hoạch hành động:**
- KPI ưu tiên 1: Mục tiêu → Hành động → Timeline → Người chịu trách nhiệm
- KPI ưu tiên 2: ...

## Định dạng & Lưu trữ
- Format: .pptx (trình bày) + .xlsx (data tables)
- Đặt tên: `[RPT/YYYY] RPT-BMK-001 - Benchmarking [Năm] - CEO Office v1.0`
- Thư mục: `09 Báo Cáo / 08 Benchmarking`
- Bảo mật: Nếu có dữ liệu nhạy cảm của đối thủ, cần giới hạn phân phối

## Hướng dẫn cho Claude
1. Hỏi về ngành nghề cụ thể để tìm benchmark phù hợp — benchmark sai ngành là vô nghĩa.
2. Giúp tìm nguồn dữ liệu benchmark công khai: báo cáo ngành, McKinsey, Deloitte, SaaS metrics (OpenView, SaaStr), HR benchmark (Mercer, Korn Ferry).
3. Tạo spider/radar chart để hình dung tổng thể vị trí công ty vs. ngành trên nhiều chiều.
4. Nhắc cẩn thận với dữ liệu của đối thủ — chỉ dùng thông tin công khai, không dùng thông tin thu được qua cách không hợp pháp.
5. Kết nối Gap Analysis với kế hoạch hành động cụ thể — benchmarking không có giá trị nếu không dẫn đến hành động.
6. Cập nhật benchmarking hàng năm để theo dõi tiến trình cải thiện.
