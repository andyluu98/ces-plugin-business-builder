# Báo cáo Lãi Lỗ (P&L Statement) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng Báo cáo Kết quả Hoạt động Kinh doanh (P&L - Profit & Loss Statement) toàn diện, bao gồm cả format pháp định theo VAS (Chuẩn mực Kế toán Việt Nam) và format quản trị nội bộ (Management P&L) linh hoạt hơn cho quyết định kinh doanh. Tài liệu hướng dẫn cách đọc, phân tích và diễn giải P&L để chuyển số liệu kế toán thành thông tin hữu ích cho lãnh đạo. Phù hợp cho kế toán trưởng, CFO và CEO muốn hiểu sâu hơn về hiệu quả kinh doanh qua báo cáo tài chính.

## Câu hỏi thu thập thông tin
1. Kỳ báo cáo: tháng, quý hay năm? Năm tài chính bắt đầu từ tháng mấy?
2. Chuẩn mực kế toán áp dụng: VAS hay IFRS? Doanh nghiệp có yêu cầu báo cáo theo chuẩn nào?
3. Cơ cấu doanh thu: có bao nhiêu dòng sản phẩm/dịch vụ, khu vực hoặc phân khúc KH cần tách riêng?
4. Cách phân bổ chi phí: theo phòng ban, theo sản phẩm, hay theo kênh bán hàng?
5. Đối tượng đọc P&L chính: CEO nội bộ, nhà đầu tư, ngân hàng, kiểm toán? Mức độ chi tiết cần thiết?
6. Có muốn so sánh với kỳ trước và với ngân sách không? Dữ liệu ngân sách có sẵn không?
7. Cần phân tích breakdown thêm không? (Gross Margin theo sản phẩm, chi phí theo phòng ban...)

## Cấu trúc tài liệu

### Phần 1: P&L theo VAS - Format Pháp định (Mẫu B02-DN)

#### Báo cáo Kết quả Hoạt động Kinh doanh
**Đơn vị: [Tên công ty] | Kỳ: [Tháng/Quý/Năm]**

| Chỉ tiêu | Mã số | Thuyết minh | Kỳ này | Kỳ trước |
|---------|-------|-------------|--------|---------|
| **1. Doanh thu bán hàng và CCDV** | 01 | | | |
| **2. Các khoản giảm trừ DT** | 02 | | | |
| **3. Doanh thu thuần (01-02)** | 10 | | | |
| **4. Giá vốn hàng bán** | 11 | | | |
| **5. Lợi nhuận gộp (10-11)** | 20 | | | |
| **6. DT hoạt động tài chính** | 21 | | | |
| **7. CP tài chính** | 22 | | | |
|   - Trong đó: Lãi vay | 23 | | | |
| **8. CP bán hàng** | 25 | | | |
| **9. CP quản lý doanh nghiệp** | 26 | | | |
| **10. LN từ HĐKD (20+21-22-25-26)** | 30 | | | |
| **11. Thu nhập khác** | 31 | | | |
| **12. Chi phí khác** | 32 | | | |
| **13. LN khác (31-32)** | 40 | | | |
| **14. Tổng LN trước thuế (30+40)** | 50 | | | |
| **15. Thuế TNDN hiện hành** | 51 | | | |
| **16. Thuế TNDN hoãn lại** | 52 | | | |
| **17. Lợi nhuận sau thuế TNDN (50-51-52)** | 60 | | | |
| Lãi cơ bản trên cổ phiếu (EPS) | 70 | | | |

### Phần 2: Management P&L - Format Quản trị Nội bộ

*Format linh hoạt hơn, phù hợp cho phân tích kinh doanh*

#### Management P&L - [Kỳ báo cáo]

| Chỉ tiêu | Tháng này | Tháng trước | Budget | vs Budget | YTD Thực | YTD Budget |
|---------|-----------|-------------|--------|-----------|----------|-----------|
| **DOANH THU** | | | | | | |
| Doanh thu [SP/DV A] | | | | | | |
| Doanh thu [SP/DV B] | | | | | | |
| Doanh thu [SP/DV C] | | | | | | |
| Tổng Doanh thu | | | | | | |
| **GIÁ VỐN (COGS)** | | | | | | |
| Nguyên vật liệu trực tiếp | | | | | | |
| Nhân công trực tiếp | | | | | | |
| Chi phí sản xuất chung | | | | | | |
| Tổng COGS | | | | | | |
| **LỢI NHUẬN GỘP** | | | | | | |
| *Gross Margin %* | | | | | | |
| **CHI PHÍ VẬN HÀNH (OPEX)** | | | | | | |
| *Chi phí Bán hàng* | | | | | | |
| - Lương nhóm Sales | | | | | | |
| - Hoa hồng | | | | | | |
| - Chi phí bán hàng khác | | | | | | |
| *Chi phí Marketing* | | | | | | |
| - Digital marketing | | | | | | |
| - Events, content | | | | | | |
| - Marketing khác | | | | | | |
| *Chi phí G&A (Quản lý Chung)* | | | | | | |
| - Lương bộ phận hỗ trợ | | | | | | |
| - Thuê văn phòng | | | | | | |
| - Công nghệ & phần mềm | | | | | | |
| - Pháp lý, kiểm toán | | | | | | |
| - G&A khác | | | | | | |
| **EBITDA** | | | | | | |
| *EBITDA Margin %* | | | | | | |
| Khấu hao & Phân bổ | | | | | | |
| **EBIT** | | | | | | |
| Chi phí lãi vay | | | | | | |
| Thu nhập tài chính | | | | | | |
| **EBT (Lợi nhuận trước thuế)** | | | | | | |
| Thuế TNDN | | | | | | |
| **Lợi nhuận sau thuế** | | | | | | |
| *Net Margin %* | | | | | | |

### Phần 3: Phân tích P&L Đa chiều

#### 3.1 Gross Margin theo Dòng Sản phẩm/Dịch vụ
| Sản phẩm/DV | Doanh thu | COGS | Gross Profit | GM % | % Tổng DT |
|------------|---------|------|-------------|------|-----------|
| [SP A] | | | | | |
| [SP B] | | | | | |
| **Tổng** | | | | | |

#### 3.2 P&L theo Phòng ban / Cost Center
| Phòng ban | Doanh thu phân bổ | Chi phí trực tiếp | Chi phí phân bổ | Contribution |
|-----------|-----------------|-----------------|-----------------|-------------|

#### 3.3 P&L theo Kênh Bán hàng
| Kênh | Doanh thu | COGS | Marketing | Net Contribution | % |
|------|---------|------|-----------|-----------------|---|
| Online | | | | | |
| Offline | | | | | |
| Đại lý | | | | | |

### Phần 4: Phân tích Biến động và Nhận xét

#### 4.1 Bảng Giải thích Biến động So với Tháng Trước
| Chỉ tiêu | Thay đổi (VND) | Thay đổi (%) | Nguyên nhân chính |
|---------|--------------|------------|------------------|
| Doanh thu | | | |
| COGS | | | |
| Gross Profit | | | |
| Chi phí bán hàng | | | |
| EBITDA | | | |

#### 4.2 Bảng Giải thích Biến động So với Budget
*(Chỉ giải thích biến động >5% hoặc >X triệu VND)*

#### 4.3 Nhận xét Tổng quan của Kế toán trưởng/CFO
- Điểm nổi bật tích cực trong kỳ
- Điểm cần chú ý hoặc lo ngại
- Dự báo tháng tiếp theo
- Khuyến nghị hành động

### Phần 5: KPI Tài chính Quan trọng từ P&L
| KPI | Công thức | Kỳ này | Kỳ trước | Budget | Benchmark ngành |
|-----|----------|--------|---------|--------|----------------|
| Gross Margin % | Gross Profit / Revenue | | | | |
| EBITDA Margin % | EBITDA / Revenue | | | | |
| Net Margin % | Net Profit / Revenue | | | | |
| OpEx Ratio | Total OpEx / Revenue | | | | |
| Revenue/FTE | Revenue / Headcount | | | | |
| Revenue growth MoM | | | | | |

### Phần 6: Hướng dẫn Đọc P&L cho Lãnh đạo Không chuyên Tài chính
- Gross Margin là gì và tại sao quan trọng: "Cứ bán 100 đồng thì còn lại bao nhiêu sau khi trả chi phí sản xuất?"
- Sự khác biệt giữa Revenue và Cash: tại sao lợi nhuận cao nhưng dòng tiền vẫn thiếu?
- EBITDA vs Net Profit: khi nào dùng chỉ số nào để đánh giá?
- Tại sao margin % quan trọng hơn số tuyệt đối?
- Red flags cần chú ý: margin giảm, chi phí tăng nhanh hơn doanh thu, lỗ gộp...

## Định dạng & Lưu trữ
- Format: .xlsx (P&L với formula liên kết) + .pdf (bản phát hành chính thức)
- Đặt tên: [PL/YYYY-MM] FIN-016 - Bao Cao PL [Thang/Quy/Nam] - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/09-Bao-Cao-Tai-Chinh/[YYYY]/
- Phát hành: nội bộ (đầy đủ) và bản rút gọn cho CEO (1 trang)

## Hướng dẫn cho Claude
1. Phân biệt rõ P&L pháp định (VAS, cho kiểm toán/thuế) và Management P&L (cho quyết định kinh doanh).
2. Management P&L phải có cột "vs Budget" - đây là thông tin có giá trị nhất cho lãnh đạo.
3. Phân tích biến động phải đi kèm nguyên nhân cụ thể, không chỉ là số liệu tăng/giảm.
4. Gross Margin theo sản phẩm là thông tin chiến lược quan trọng - không phải mọi sản phẩm đều có lãi.
5. KPI dashboard tóm tắt trong 1 trang để CEO đọc nhanh - chi tiết để trong phần phụ lục.
6. Hướng dẫn đọc P&L cho lãnh đạo không chuyên tài chính là phần thường bị bỏ qua nhưng rất có giá trị.
7. Đảm bảo format nhất quán tháng này sang tháng khác để dễ so sánh xu hướng.
