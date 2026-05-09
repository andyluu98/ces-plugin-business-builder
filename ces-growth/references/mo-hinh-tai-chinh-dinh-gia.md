# Mô Hình Tài Chính và Định Giá Doanh Nghiệp | ces-growth

## Mục đích & Phạm vi
Tài liệu này hướng dẫn xây dựng mô hình tài chính (financial model) và thực hiện định giá doanh nghiệp bằng các phương pháp phổ biến (DCF, Revenue Multiple, EBITDA Multiple, Comparable Transactions). Dùng cho mục đích gọi vốn, M&A, mua lại cổ phần nội bộ, hoặc lập kế hoạch tài chính chiến lược.

## Câu hỏi thu thập thông tin
1. Mục đích của mô hình tài chính này là gì (gọi vốn, bán công ty, mua lại, lập kế hoạch nội bộ)?
2. Doanh nghiệp đang ở giai đoạn nào (startup, tăng trưởng, trưởng thành)? Có lợi nhuận chưa?
3. Mô hình kinh doanh là gì? Doanh thu đến từ đâu (SaaS, transaction, project, product)?
4. Dữ liệu tài chính lịch sử 3-5 năm có đầy đủ không?
5. Các giả định tăng trưởng dựa trên cơ sở nào (lịch sử, thị trường, pipeline)?
6. Phương pháp định giá nào phù hợp nhất với ngành và giai đoạn của doanh nghiệp?
7. Tỷ lệ chiết khấu (WACC/discount rate) dự kiến là bao nhiêu?

## Cấu trúc tài liệu

### Phần 1: Cấu trúc mô hình tài chính (Financial Model Architecture)

**Sheet 1 – Assumptions (Giả định)**
- Revenue assumptions: tốc độ tăng trưởng, giá bán, số khách hàng
- Cost assumptions: COGS%, headcount plan, opex growth
- Working capital: DSO, DIO, DPO
- Capex plan
- Tax rate, discount rate

**Sheet 2 – Revenue Model**
Tùy mô hình kinh doanh:

*SaaS/Subscription:*
| Tháng | Khách hàng đầu kỳ | New customers | Churned | Cuối kỳ | ARPU | MRR |
|-------|------------------|---------------|---------|---------|------|-----|

*Product/Retail:*
| Kỳ | Volume | ASP | Discount | Revenue | COGS | Gross Profit |
|----|--------|-----|---------|---------|------|-------------|

*Project/Service:*
| Kỳ | Số dự án | Giá TB/dự án | Revenue | Utilization rate | Gross Profit |
|----|---------|-------------|---------|-----------------|-------------|

**Sheet 3 – P&L (Income Statement) – 5 năm**
| | Y1 | Y2 | Y3 | Y4 | Y5 |
|--|----|----|----|----|-----|
| Revenue | | | | | |
| COGS | | | | | |
| Gross Profit | | | | | |
| Gross Margin % | | | | | |
| S&M | | | | | |
| R&D | | | | | |
| G&A | | | | | |
| Total OpEx | | | | | |
| EBITDA | | | | | |
| D&A | | | | | |
| EBIT | | | | | |
| Interest | | | | | |
| EBT | | | | | |
| Tax | | | | | |
| Net Income | | | | | |

**Sheet 4 – Balance Sheet**
**Sheet 5 – Cash Flow Statement**
**Sheet 6 – Valuation**

### Phần 2: Phương pháp Định giá

**2.1 DCF (Discounted Cash Flow) – Dòng tiền chiết khấu**

Công thức:
```
Enterprise Value = Σ (FCF_t / (1+WACC)^t) + Terminal Value / (1+WACC)^n
Terminal Value = FCF_n × (1+g) / (WACC - g)
Equity Value = Enterprise Value - Net Debt
Value per Share = Equity Value / Total Shares
```

Bước thực hiện:
1. Dự báo Free Cash Flow (FCF) 5-10 năm
2. Xác định WACC (thường 15-25% cho startup VN)
3. Tính Terminal Value (Terminal Growth Rate: 3-5%)
4. Chiết khấu về hiện tại
5. Sensitivity Analysis: thay đổi WACC và growth rate

**2.2 Revenue Multiple**

```
Valuation = ARR (hoặc Revenue) × Revenue Multiple
```

Revenue Multiple theo ngành và giai đoạn:
| Loại doanh nghiệp | Range Multiple |
|------------------|----------------|
| SaaS tăng trưởng cao (>50% YoY) | 8-15x ARR |
| SaaS tăng trưởng vừa (20-50% YoY) | 4-8x ARR |
| Tech/Software (non-SaaS) | 2-5x Revenue |
| Retail/F&B | 0.5-2x Revenue |
| Manufacturing | 0.3-1x Revenue |

**2.3 EBITDA Multiple**

```
Valuation = EBITDA × EBITDA Multiple
```

EBITDA Multiple theo ngành (VN market):
- Tech/Software: 8-15x
- F&B: 6-10x
- Retail: 5-8x
- Manufacturing: 4-7x
- Services: 4-8x

**2.4 Comparable Transactions (Transaction Comps)**
- Tìm M&A transactions tương tự trong 2-3 năm gần nhất
- Tính implied multiple từ transaction
- Áp dụng premium/discount cho specifics của công ty

### Phần 3: Sensitivity Analysis (Phân tích độ nhạy)

**Scenario Analysis:**
| | Bear Case | Base Case | Bull Case |
|--|-----------|-----------|-----------|
| Revenue growth | X% | Y% | Z% |
| Gross Margin | X% | Y% | Z% |
| Valuation | VND | VND | VND |

**Sensitivity Table (WACC vs. Terminal Growth Rate):**
| WACC \ g | 2% | 3% | 4% | 5% |
|----------|----|----|----|----|
| 12% | | | | |
| 15% | | | | |
| 18% | | | | |
| 20% | | | | |

### Phần 4: Output Tóm tắt định giá
- Range valuation từ các phương pháp
- Football field chart (hình dung khoảng giá trị)
- Kết luận và mức giá đề xuất

## Định dạng & Lưu trữ
- Format: .xlsx (model) + .pptx (valuation summary)
- Đặt tên: `[FIN/YYYY] GRW-FIN-001 - Mô Hình Tài Chính [Vòng/Mục đích] - CFO CONFIDENTIAL v1.0`
- Thư mục: `00 Hội Đồng ĐH / 02 Định Giá & Mô Hình TC`
- Bảo mật: Tối mật

## Hướng dẫn cho Claude
1. Bắt đầu bằng cách xác định mục đích — định giá cho gọi vốn khác với định giá nội bộ hay M&A.
2. Hỏi về mô hình kinh doanh để chọn Revenue Model phù hợp — SaaS dùng MRR/ARR model, retail dùng volume × ASP model.
3. Giả định (Assumptions) là phần quan trọng nhất — giúp người dùng justify từng con số bằng data thực tế.
4. Luôn xây dựng 3 scenarios (Bear/Base/Bull) — tránh chỉ có 1 scenario lạc quan.
5. Nhắc rằng DCF rất nhạy cảm với WACC và Terminal Growth Rate — Sensitivity Table là bắt buộc.
6. Với startup chưa có lợi nhuận: Revenue Multiple phù hợp hơn DCF; với công ty đã có lợi nhuận ổn định: cân bằng giữa DCF và EBITDA Multiple.
