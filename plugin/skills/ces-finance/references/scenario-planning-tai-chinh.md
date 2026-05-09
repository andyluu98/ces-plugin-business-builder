# Kịch bản Tài chính (Lạc quan / Cơ sở / Thận trọng) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng mô hình kịch bản tài chính 3 chiều (Optimistic / Base / Conservative) với đầy đủ P&L, Cash Flow và Balance Sheet dự kiến cho từng kịch bản. Khác với kịch bản chiến lược định tính, tài liệu này tập trung vào con số tài chính cụ thể, giúp CFO và CEO hiểu rõ khoảng dao động tài chính có thể xảy ra và chuẩn bị kế hoạch ứng phó. Phù hợp cho lập kế hoạch năm, chuẩn bị pitchdeck tài chính hoặc đánh giá rủi ro tài chính.

## Câu hỏi thu thập thông tin
1. Kết quả tài chính thực tế năm hiện tại: doanh thu, gross margin, EBITDA, dòng tiền, số dư tiền mặt?
2. Kế hoạch cơ sở (base case) cho năm tới: giả định tăng trưởng doanh thu, chi phí chính?
3. Yếu tố nào tạo ra kịch bản lạc quan nhất? (Thêm khách hàng lớn, ra mắt sản phẩm mới thành công, mở rộng thị trường...)
4. Yếu tố nào tạo ra kịch bản xấu nhất mà vẫn có thể vượt qua? (Mất khách hàng lớn, dịch bệnh, suy thoái kinh tế...)
5. Cơ cấu chi phí cố định/biến đổi hiện tại? Chi phí nào có thể linh hoạt điều chỉnh nhanh nếu cần?
6. Số dư tiền mặt, hạn mức tín dụng và khả năng huy động vốn khẩn cấp hiện tại?
7. Kỳ hạn của mô hình: 1 năm, 2 năm hay 3 năm? Độ chi tiết: hàng tháng hay hàng quý?

## Cấu trúc tài liệu

### Phần 1: Khung Kịch bản Tài chính

#### 1.1 Tóm tắt 3 Kịch bản

| Tiêu chí | Lạc quan (Bull) | Cơ sở (Base) | Thận trọng (Bear) |
|----------|----------------|--------------|-------------------|
| Xác suất ước tính | 20% | 60% | 20% |
| Tên kịch bản | "[Tên gợi cảm hứng]" | "[Tên ổn định]" | "[Tên vượt khó]" |
| Tăng trưởng DT | +[X]% | +[Y]% | +[Z]% hoặc âm |
| EBITDA margin | [X]% | [Y]% | [Z]% |
| Dòng tiền cuối năm | +[X] tỷ | +[Y] tỷ | [±Z] tỷ |
| Số dư tiền cuối năm | [X] tỷ | [Y] tỷ | [Z] tỷ |
| Thời gian BEP (nếu startup) | Tháng [X] | Tháng [Y] | Tháng [Z] |

#### 1.2 Giả định Phân biệt Kịch bản

| Driver chính | Lạc quan | Cơ sở | Thận trọng |
|-------------|---------|-------|-----------|
| Tăng trưởng doanh thu | | | |
| Gross margin | | | |
| Chi phí bán hàng/DT | | | |
| DSO (ngày thu tiền) | | | |
| Tỷ lệ giữ chân KH | | | |
| Khách hàng mới/tháng | | | |
| Chi phí tuyển dụng | | | |
| Tỷ lệ lạm phát chi phí | | | |

### Phần 2: Mô hình P&L theo 3 Kịch bản

*(Trình bày 3 cột song song hoặc 3 bảng riêng)*

#### Kịch bản [X]: [Tên] - Báo cáo P&L Dự kiến

| Chỉ tiêu | Q1 | Q2 | Q3 | Q4 | Năm |
|----------|----|----|----|----|-----|
| **Doanh thu** | | | | | |
| Doanh thu sản phẩm A | | | | | |
| Doanh thu sản phẩm B | | | | | |
| Tổng Doanh thu | | | | | |
| **Giá vốn (COGS)** | | | | | |
| **Lợi nhuận gộp** | | | | | |
| *% Gross Margin* | | | | | |
| **Chi phí hoạt động** | | | | | |
| Chi phí bán hàng | | | | | |
| Chi phí Marketing | | | | | |
| Chi phí nhân sự G&A | | | | | |
| Chi phí công nghệ | | | | | |
| Chi phí vận hành khác | | | | | |
| **EBITDA** | | | | | |
| *% EBITDA Margin* | | | | | |
| Khấu hao | | | | | |
| **EBIT** | | | | | |
| Chi phí tài chính (lãi vay) | | | | | |
| **EBT** | | | | | |
| Thuế TNDN | | | | | |
| **Lợi nhuận sau thuế** | | | | | |
| *% Net Margin* | | | | | |

### Phần 3: Dự báo Dòng tiền theo 3 Kịch bản

*(Rút gọn theo quý)*

| Chỉ tiêu | Q1 | Q2 | Q3 | Q4 | Năm |
|----------|----|----|----|----|-----|
| Số dư đầu kỳ | | | | | |
| Operating Cash Flow | | | | | |
| Investing Cash Flow | | | | | |
| Financing Cash Flow | | | | | |
| **Số dư cuối kỳ** | | | | | |
| Hạn mức tín dụng còn | | | | | |
| **Tổng thanh khoản** | | | | | |
| Runway (tháng) | | | | | |

### Phần 4: Bảng Cân đối Kế toán Dự kiến cuối Năm

*(3 cột cho 3 kịch bản)*

| Khoản mục | Lạc quan | Cơ sở | Thận trọng |
|-----------|---------|-------|-----------|
| **TÀI SẢN** | | | |
| Tiền & tương đương | | | |
| Phải thu KH | | | |
| Tồn kho | | | |
| Tài sản ngắn hạn khác | | | |
| **Tổng Tài sản ngắn hạn** | | | |
| TSCĐ (ròng) | | | |
| Tài sản dài hạn khác | | | |
| **Tổng Tài sản** | | | |
| **NỢ PHẢI TRẢ** | | | |
| Phải trả NCC | | | |
| Vay ngắn hạn | | | |
| Nợ ngắn hạn khác | | | |
| **Tổng Nợ ngắn hạn** | | | |
| Vay dài hạn | | | |
| **Tổng Nợ** | | | |
| **VỐN CHỦ SỞ HỮU** | | | |
| Vốn góp | | | |
| Lợi nhuận giữ lại | | | |
| **Tổng VCSh** | | | |

### Phần 5: Chỉ số Tài chính So sánh 3 Kịch bản

| Chỉ số | Lạc quan | Cơ sở | Thận trọng | Mục tiêu |
|--------|---------|-------|-----------|---------|
| Revenue Growth | | | | |
| Gross Margin % | | | | |
| EBITDA Margin % | | | | |
| Net Margin % | | | | |
| Current Ratio | | | | |
| Debt/Equity | | | | |
| Cash Runway (tháng) | | | | |
| CAC Payback (tháng) | | | | |
| LTV/CAC | | | | |

### Phần 6: Kế hoạch Hành động theo Kịch bản

#### Nếu đang trong Kịch bản Lạc quan:
- Tín hiệu nhận biết: doanh thu tháng 3 đầu năm vượt kế hoạch >15%
- Hành động: đẩy nhanh tuyển dụng, tăng ngân sách marketing, xem xét mở rộng
- Rủi ro cần tránh: phát triển quá nóng, mất kiểm soát chi phí

#### Nếu đang trong Kịch bản Cơ sở:
- Tín hiệu nhận biết: thực tế trong khoảng ±10% so với kế hoạch
- Hành động: thực hiện kế hoạch như đã lập, review hàng quý
- Điều chỉnh nếu lệch quá 10%

#### Nếu đang trong Kịch bản Thận trọng:
- Tín hiệu nhận biết: doanh thu thấp hơn kế hoạch >15% trong 2 tháng liên tiếp
- Hành động tức thì:
  - Cắt giảm chi phí không thiết yếu (dừng ngay trong tháng)
  - Trì hoãn đầu tư và tuyển dụng
  - Kích hoạt hạn mức tín dụng dự phòng
  - Họp khẩn Ban lãnh đạo để điều chỉnh kế hoạch

### Phần 7: Kiểm tra Căng thẳng (Stress Test)
- Kịch bản căng thẳng cực đoan: mất 40% doanh thu, doanh nghiệp có thể tồn tại không?
- Điểm chịu đựng tối đa (Breaking Point): khi nào cần cắt giảm nhân sự?
- Khi nào cần huy động vốn khẩn cấp?
- Các "tripwire" - ngưỡng tự động kích hoạt hành động ứng phó

## Định dạng & Lưu trữ
- Format: .xlsx (mô hình liên kết động 3 kịch bản) + .pptx (slides tóm tắt cho BGĐ)
- Đặt tên: [SCENARIO/YYYY] FIN-007 - Kich Ban Tai Chinh - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/03-Phan-Tich-Tai-Chinh/

## Hướng dẫn cho Claude
1. Xây dựng mô hình Excel tích hợp: thay đổi giả định ở 1 sheet thì toàn bộ P&L, CF, BS tự cập nhật.
2. Các kịch bản phải nội tại nhất quán - không thể doanh thu lạc quan nhưng chi phí lại theo kịch bản thận trọng.
3. Kịch bản thận trọng phải đủ thực tế để gây lo ngại, đủ nghiêm túc để lãnh đạo chuẩn bị.
4. Phần "kế hoạch hành động theo kịch bản" thường bị bỏ qua nhưng lại có giá trị thực tiễn nhất.
5. Stress test giúp lãnh đạo biết "giới hạn chịu đựng" của doanh nghiệp - thông tin quan trọng để ra quyết định.
6. Cập nhật actuals hàng tháng và xác định doanh nghiệp đang theo kịch bản nào - đây là mục đích chính của công cụ.
7. Trình bày tóm tắt 1-2 trang cho CEO, bản đầy đủ cho CFO và nhà đầu tư.
