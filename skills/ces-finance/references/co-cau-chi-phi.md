# Phân tích Cơ cấu Chi phí (Fixed/Variable) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude thực hiện phân tích cơ cấu chi phí toàn diện cho doanh nghiệp, phân loại chi phí theo tính chất (cố định/biến đổi/hỗn hợp), theo chức năng (COGS/OPEX/CAPEX) và theo phòng ban. Phân tích cơ cấu chi phí giúp lãnh đạo hiểu rõ đòn bẩy tài chính, tối ưu hóa lợi nhuận, xác định chi phí có thể cắt giảm và ra quyết định định giá chính xác. Đây là đầu vào quan trọng cho phân tích break-even và kế hoạch tài chính.

## Câu hỏi thu thập thông tin
1. Doanh thu và tổng chi phí trong 12 tháng gần nhất là bao nhiêu? Lợi nhuận gộp và ròng là bao nhiêu?
2. Liệt kê tất cả các loại chi phí lớn của doanh nghiệp (top 10 hạng mục chi phí chiếm nhiều nhất).
3. Chi phí nào không thay đổi dù doanh số tăng gấp đôi hoặc giảm một nửa? (Chi phí cố định)
4. Chi phí nào tăng/giảm tỷ lệ thuận với doanh số hoặc sản lượng? (Chi phí biến đổi)
5. Trong 6 tháng qua, khi doanh thu tăng 10%, chi phí tổng thể tăng bao nhiêu %?
6. Chi phí nào bạn muốn cắt giảm nhưng chưa biết cách? Chi phí nào bạn nghĩ đang lãng phí?
7. Doanh nghiệp có kế hoạch mở rộng quy mô không? Chi phí sẽ thay đổi như thế nào khi scale up gấp đôi?

## Cấu trúc tài liệu

### Phần 1: Tổng quan Cơ cấu Chi phí

#### 1.1 Waterfall Chi phí Tổng thể
```
Doanh thu:                    100%
- Giá vốn hàng bán (COGS):   [X]%
= Lợi nhuận gộp:              [X]%
- Chi phí bán hàng:           [X]%
- Chi phí marketing:          [X]%
- Chi phí nhân sự G&A:        [X]%
- Chi phí công nghệ:          [X]%
- Chi phí vận hành khác:      [X]%
= EBITDA:                     [X]%
- Khấu hao:                   [X]%
= EBIT:                       [X]%
- Chi phí tài chính:          [X]%
= EBT:                        [X]%
- Thuế:                       [X]%
= Lợi nhuận ròng:             [X]%
```

#### 1.2 Biểu đồ Cơ cấu Chi phí
Mô tả cấu trúc pie chart:
- % COGS vs OPEX
- Top 5 hạng mục chi phí lớn nhất
- So sánh với benchmark ngành (nếu có)

### Phần 2: Phân loại Chi phí theo Tính chất

#### 2.1 Chi phí Cố định (Fixed Costs)
*Định nghĩa: Không thay đổi trong ngắn hạn, bất kể doanh thu tăng hay giảm*

| Hạng mục | Số tiền/tháng | % Tổng chi phí | Ghi chú |
|----------|---------------|----------------|---------|
| Tiền thuê văn phòng | | | Hợp đồng đến [ngày] |
| Lương nhân viên cố định | | | [Số lượng người] |
| BHXH cố định | | | Theo lương cố định |
| Khấu hao TSCĐ | | | Theo phương pháp đường thẳng |
| Chi phí internet, điện thoại | | | Gói cố định |
| Phần mềm SaaS subscription | | | [Tên phần mềm] |
| Lãi vay cố định | | | Hợp đồng vay |
| Bảo hiểm | | | Hàng năm |
| **Tổng Fixed Costs** | | | |

**Phân tích:**
- % Fixed costs / Tổng doanh thu: ...%
- Điểm rủi ro: khi doanh thu giảm, fixed costs vẫn phải trả
- Nếu doanh thu = 0, công ty chịu đựng được mấy tháng với tiền mặt hiện có?

#### 2.2 Chi phí Biến đổi (Variable Costs)
*Định nghĩa: Thay đổi tỷ lệ thuận với doanh thu hoặc sản lượng*

| Hạng mục | % Doanh thu | Số tiền ứng với DT hiện tại | Ghi chú |
|----------|-------------|----------------------------|---------|
| Nguyên vật liệu/Hàng hóa | ...% | | COGS trực tiếp |
| Hoa hồng bán hàng | ...% | | Theo tỷ lệ doanh thu |
| Chi phí giao hàng | ...% | | Theo đơn hàng |
| Phí cổng thanh toán | ...% | | Theo giá trị giao dịch |
| Chi phí đóng gói | ...% | | Theo sản lượng |
| Chi phí làm thêm giờ | ...% | | Theo sản xuất |
| **Tổng Variable Costs** | ...% | | |

**Phân tích:**
- Contribution Margin = Doanh thu - Variable Costs = ...%
- Khi doanh thu tăng 1 đồng, lợi nhuận biên tăng thêm [X] đồng

#### 2.3 Chi phí Hỗn hợp (Mixed/Step Costs)
*Định nghĩa: Có phần cố định và phần biến đổi, hoặc tăng theo bậc thang*

| Hạng mục | Phần cố định | Phần biến đổi | Trigger tăng |
|----------|-------------|---------------|-------------|
| Điện, nước | [Base] | [Theo sản xuất] | - |
| Nhân sự bán thời gian | - | [Theo giờ] | - |
| Vận chuyển | [Xe cố định] | [Theo số chuyến] | Thêm xe khi >X chuyến/tháng |
| Dịch vụ thuê ngoài | [Retainer] | [Theo dự án] | - |

### Phần 3: Phân loại Chi phí theo Chức năng

#### 3.1 COGS - Giá vốn Hàng bán
- Nguyên vật liệu trực tiếp
- Nhân công trực tiếp
- Chi phí sản xuất chung
- % COGS/Doanh thu: ...% | Gross Margin: ...%
- So sánh với benchmark ngành: cao hơn/thấp hơn bao nhiêu?

#### 3.2 SG&A - Chi phí Bán hàng, Tiếp thị & Quản lý

**Selling Expenses (Chi phí Bán hàng)**
- Chi tiết từng hạng mục và % doanh thu
- Hiệu quả: mỗi đồng chi cho bán hàng tạo ra bao nhiêu đồng doanh thu?

**Marketing Expenses (Chi phí Tiếp thị)**
- Chi tiết theo kênh và chiến dịch
- CAC (Customer Acquisition Cost) theo kênh

**G&A Expenses (Chi phí Quản lý Chung)**
- Chi tiết theo phòng ban
- Tỷ lệ G&A/Doanh thu so với ngành

#### 3.3 R&D - Chi phí Nghiên cứu & Phát triển (nếu có)

### Phần 4: Phân tích Chi phí theo Phòng ban

Bảng phân bổ chi phí theo trung tâm chi phí (Cost Center):
| Phòng ban | Chi phí trực tiếp | Chi phí phân bổ | Tổng | % Tổng | % Doanh thu |
|-----------|------------------|-----------------|------|--------|-------------|

### Phần 5: Phân tích Đòn bẩy Vận hành (Operating Leverage)
- Operating Leverage = % thay đổi EBIT / % thay đổi Doanh thu
- Rủi ro của đòn bẩy cao: khi doanh thu giảm, lợi nhuận giảm mạnh hơn
- Cơ hội của đòn bẩy cao: khi doanh thu tăng, lợi nhuận tăng nhanh hơn
- Khuyến nghị tỷ lệ Fixed/Variable phù hợp với giai đoạn doanh nghiệp

### Phần 6: Cơ hội Tối ưu hóa Chi phí

#### 6.1 Chi phí có thể Cắt giảm Ngay (Quick Wins)
| Hạng mục | Tiết kiệm ước tính | Thời gian thực hiện | Rủi ro |
|----------|-------------------|---------------------|--------|

#### 6.2 Chi phí cần Tái cơ cấu (Medium-term)
| Hạng mục | Hiện tại | Mục tiêu | Cách thực hiện |
|----------|---------|---------|----------------|

#### 6.3 Chi phí Đầu tư để Tiết kiệm (Spend to Save)
| Đầu tư | Chi phí | Tiết kiệm kỳ vọng | Payback period |
|--------|---------|-------------------|----------------|

### Phần 7: Benchmark và KPI Chi phí
- Tỷ lệ chi phí chuẩn của ngành (nếu có dữ liệu)
- KPI chi phí theo dõi hàng tháng: Cost per unit, cost as % of revenue
- Mục tiêu tối ưu chi phí trong 12 tháng tới

## Định dạng & Lưu trữ
- Format: .xlsx (phân tích chi tiết) + .docx (thuyết minh và khuyến nghị)
- Đặt tên: [ANALYSIS/YYYY] FIN-004 - Co Cau Chi Phi - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/03-Phan-Tich-Tai-Chinh/

## Hướng dẫn cho Claude
1. Thu thập dữ liệu chi phí thực tế 12 tháng trước khi phân tích - không có số liệu thực thì phân tích vô nghĩa.
2. Phân loại Fixed vs Variable phải dựa trên hành vi thực tế của chi phí, không phải lý thuyết.
3. Contribution Margin là chỉ số quan trọng nhất - giúp hiểu khi bán thêm 1 đơn hàng, lợi nhuận tăng bao nhiêu.
4. Benchmark ngành giúp xác định chi phí nào đang cao bất thường - tìm nguồn tham chiếu phù hợp.
5. Phần tối ưu chi phí phải có con số cụ thể và kế hoạch thực hiện - không chỉ là danh sách gợi ý.
6. Trực quan hóa bằng biểu đồ waterfall và pie chart để lãnh đạo dễ hiểu.
7. Cập nhật phân tích này hàng quý để theo dõi xu hướng thay đổi cơ cấu chi phí.
