# Báo Cáo Định Giá Doanh Nghiệp (DCF, P/E, Revenue Multiple) | ces-growth

## Mục đích & Phạm vi
Tài liệu này hướng dẫn lập báo cáo định giá doanh nghiệp toàn diện sử dụng nhiều phương pháp kết hợp, phù hợp cho mục đích gọi vốn, M&A, mua lại cổ phần nội bộ (ESOP pricing), hoặc tranh chấp pháp lý. Báo cáo định giá chuyên nghiệp kết hợp phân tích định lượng (các phương pháp tính) với phân tích định tính (yếu tố thị trường, cạnh tranh, rủi ro) để đưa ra range giá trị hợp lý.

## Câu hỏi thu thập thông tin
1. Mục đích của báo cáo định giá (gọi vốn, bán công ty, ESOP pricing, kiểm toán nội bộ)?
2. Ngày định giá (Valuation Date) là khi nào? Số liệu tài chính cắt đến kỳ nào?
3. Phương pháp định giá nào phù hợp nhất với giai đoạn và ngành của doanh nghiệp?
4. Có báo cáo tài chính kiểm toán không? Nếu không, dùng management accounts?
5. Đối thủ cạnh tranh nào có thể dùng làm comparable companies?
6. Có transaction nào tương đương trong ngành gần đây không?
7. Báo cáo sẽ được sử dụng bởi bên thứ ba (nhà đầu tư, ngân hàng, tòa án)?

## Cấu trúc tài liệu

### Phần 1: Tóm Tắt Định Giá (Executive Summary)

**Thông tin định giá:**
- Tên doanh nghiệp và ngành
- Ngày định giá: [DD/MM/YYYY]
- Mục đích: [Gọi vốn Series A / M&A / ESOP]
- Người thực hiện định giá

**Kết quả định giá:**
| Phương pháp | Enterprise Value | Equity Value | Trọng số |
|-------------|-----------------|--------------|---------|
| DCF | | | 40% |
| Revenue Multiple | | | 30% |
| EBITDA Multiple | | | 20% |
| Comparable Transactions | | | 10% |
| **Weighted Average** | | | 100% |

**Kết luận:** Equity Value nằm trong khoảng **[X – Y] tỷ VND**, giá trị trung tâm **Z tỷ VND**

### Phần 2: Mô Tả Doanh Nghiệp
- Tổng quan hoạt động kinh doanh
- Sản phẩm/dịch vụ chính và thị trường mục tiêu
- Lịch sử tài chính tóm tắt (3-5 năm)
- Cơ cấu sở hữu và quản trị
- Lợi thế cạnh tranh (moat)

### Phần 3: Phương Pháp 1 – DCF (Discounted Cash Flow)

**3.1 Dự báo Free Cash Flow (5-10 năm)**

| Năm | Revenue | EBITDA | EBIT | Tax | NOPAT | D&A | CapEx | ΔNWC | FCF |
|-----|---------|--------|------|-----|-------|-----|-------|------|-----|
| Y1 | | | | | | | | | |
| Y2-Y5 | | | | | | | | | |

**3.2 Xác định WACC**
- Cost of Equity = Rf + β × ERP + Size Premium
  - Rf (Risk-free rate): Lãi suất TPCP VN 10 năm = X%
  - β (Beta): Unlevered beta ngành × Leverage adjustment
  - ERP (Equity Risk Premium): VN market = 7-10%
  - Size Premium: 2-4% (doanh nghiệp vừa nhỏ)
- Cost of Debt = Lãi suất vay thực tế × (1 - Tax rate)
- WACC = Ke × We + Kd × Wd

**3.3 Terminal Value**
- Terminal Growth Rate: [g] = X% (thường 3-5%)
- Terminal Value = FCF_n × (1+g) / (WACC-g)

**3.4 Enterprise Value và Equity Value**
- Enterprise Value = PV(FCF 1-n) + PV(Terminal Value)
- (+) Tiền mặt và tương đương
- (-) Tổng nợ vay
- = **Equity Value**

**3.5 Sensitivity Analysis DCF**
| WACC \ Growth | 2% | 3% | 4% | 5% |
|---|---|---|---|---|
| 12% | | | | |
| 15% | | | | |
| 18% | | | | |
| 22% | | | | |

### Phần 4: Phương Pháp 2 – Revenue Multiple (EV/Revenue)

**4.1 Comparable Companies Analysis (Public Comps)**
| Công ty | Quốc gia | Revenue | EV | EV/Revenue | Growth |
|---------|---------|---------|----|-----------|----|
| [Comp 1] | | | | | |
| [Comp 2] | | | | | |
| Median | | | | | |

**4.2 Áp dụng cho doanh nghiệp**
- Revenue (TTM hoặc NTM): X tỷ
- Selected Multiple: Y×  (median ± discount/premium)
- Enterprise Value = X × Y
- Premium/Discount factors:
  - (+) Growth premium nếu tăng trưởng > peers
  - (-) Size discount nếu nhỏ hơn peers
  - (-) Liquidity discount (private company): 20-30%

### Phần 5: Phương Pháp 3 – EBITDA Multiple (EV/EBITDA)
*(Áp dụng khi doanh nghiệp đã có EBITDA dương)*

- EBITDA (TTM): X tỷ
- Industry EBITDA Multiple: Y× (từ comparable companies)
- Enterprise Value = X × Y
- Điều chỉnh: +/- normalization adjustments

### Phần 6: Phương Pháp 4 – Comparable Transactions (Transaction Comps)

| Giao dịch | Ngày | Seller | Buyer | EV | Revenue | EBITDA | EV/Rev | EV/EBITDA |
|-----------|------|--------|-------|----|---------|----|--------|-----------|

- Implied multiple từ transactions
- Áp dụng control premium (thường 20-30% so với minority stake)

### Phần 7: Phân Tích Rủi Ro Ảnh Hưởng Đến Định Giá
- Key value drivers và sensitivity
- Rủi ro chính làm giảm giá trị
- Yếu tố tiềm năng làm tăng giá trị

### Phần 8: Kết Luận và Football Field Chart

**Football Field Chart** (hình dung range giá trị theo phương pháp):
```
                        Low ←——————→ High
DCF:            ████████████████████████████
Revenue Mult:           ████████████████
EBITDA Mult:                    ████████████
Transaction:        ██████████████████
Weighted Avg:           ⬛⬛⬛⬛⬛⬛
```

**Kết luận định giá:** [Mức giá đề xuất và lý luận]

## Định dạng & Lưu trữ
- Format: .xlsx (model) + .docx (báo cáo tường thuật) + .pdf (phát hành)
- Đặt tên: `[VAL/YYYY-MM] GRW-VAL-001 - Định Giá [Tên CT] [Ngày] - CFO CONFIDENTIAL v1.0`
- Thư mục: `00 Hội Đồng ĐH / 02 Định Giá & Mô Hình TC`
- Bảo mật: Tối mật

## Hướng dẫn cho Claude
1. Xác định rõ mục đích định giá trước — định giá cho gọi vốn thường cao hơn định giá cho mua lại cổ phần nội bộ.
2. Không có phương pháp nào là "đúng" — kết hợp nhiều phương pháp và trọng số phù hợp với context.
3. WACC cho startup Việt Nam thường 18-25% — cao hơn đáng kể so với công ty niêm yết phương Tây.
4. Luôn áp dụng Private Company Discount 20-30% so với public comparables — thanh khoản thấp hơn.
5. Football Field Chart là cách trực quan nhất để trình bày range định giá cho người không chuyên về finance.
6. Nhắc nhở: báo cáo định giá chính thức dùng cho mục đích pháp lý hoặc giao dịch lớn cần được thực hiện bởi định giá viên chuyên nghiệp có chứng chỉ.
