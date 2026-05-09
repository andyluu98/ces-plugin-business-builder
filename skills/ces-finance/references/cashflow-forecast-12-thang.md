# Dự báo Dòng tiền 12 Tháng | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng mô hình dự báo dòng tiền (Cash Flow Forecast) chi tiết theo tháng trong 12 tháng tới. Dự báo dòng tiền là công cụ quản lý tài chính quan trọng nhất cho SME - nhiều doanh nghiệp có lợi nhuận kế toán dương vẫn phá sản vì thiếu tiền mặt (profit ≠ cash). Template bao gồm 3 dòng tiền: hoạt động kinh doanh (Operating), đầu tư (Investing) và tài chính (Financing). Phù hợp cho CFO, kế toán trưởng và chủ doanh nghiệp dùng để quản lý thanh khoản chủ động.

## Câu hỏi thu thập thông tin
1. Số dư tiền mặt và tiền gửi ngân hàng hiện tại là bao nhiêu? Phân bổ ở những tài khoản nào?
2. Chu kỳ thu tiền từ khách hàng trung bình bao lâu? Có khách hàng lớn nào trả chậm không?
3. Chu kỳ thanh toán cho nhà cung cấp là bao nhiêu ngày? Có áp lực thanh toán nào sắp tới không?
4. Các khoản thu lớn (non-recurring) dự kiến trong 12 tháng tới là gì? (Thu nợ cũ, bán tài sản, nhận vốn...)
5. Các khoản chi lớn (non-recurring) dự kiến là gì? (Mua TSCĐ, trả nợ vay, nộp thuế lớn, lương thưởng cuối năm...)
6. Mùa vụ kinh doanh: tháng nào doanh thu cao/thấp nhất? Tháng nào chi phí cao nhất?
7. Hạn mức tín dụng ngân hàng (overdraft, LC, factoring...) hiện có là bao nhiêu? Đã dùng bao nhiêu?

## Cấu trúc tài liệu

### Phần 1: Giả định Dự báo
- Tốc độ tăng trưởng doanh thu theo tháng
- DSO - Days Sales Outstanding (số ngày thu tiền bình quân): [X] ngày
- DPO - Days Payable Outstanding (số ngày thanh toán bình quân): [X] ngày
- DIO - Days Inventory Outstanding (nếu có tồn kho): [X] ngày
- Các giả định đặc biệt theo tháng (khai trương, lễ tết, mùa vụ...)
- Tỷ lệ tiền mặt vs chuyển khoản trong thu chi

### Phần 2: Mô hình Dự báo Dòng tiền 12 Tháng

#### Bảng Dự báo Tổng hợp (12 cột tháng + Tổng năm)

**I. Dòng tiền từ Hoạt động Kinh doanh (Operating Cash Flow)**

| Khoản mục | T1 | T2 | T3 | T4 | T5 | T6 | T7 | T8 | T9 | T10 | T11 | T12 | Tổng |
|-----------|----|----|----|----|----|----|----|----|----|----|-----|-----|------|
| **TIỀN VÀO** | | | | | | | | | | | | | |
| Thu tiền từ KH (doanh thu tháng trước) | | | | | | | | | | | | | |
| Thu nợ cũ | | | | | | | | | | | | | |
| Doanh thu tiền mặt | | | | | | | | | | | | | |
| Tiền đặt cọc nhận | | | | | | | | | | | | | |
| Thu nhập tài chính (lãi tiết kiệm) | | | | | | | | | | | | | |
| **Tổng Tiền vào** | | | | | | | | | | | | | |
| **TIỀN RA** | | | | | | | | | | | | | |
| Thanh toán NCC hàng hóa/NVL | | | | | | | | | | | | | |
| Chi lương và BHXH | | | | | | | | | | | | | |
| Chi phí thuê mặt bằng | | | | | | | | | | | | | |
| Chi phí vận hành (điện, nước, internet) | | | | | | | | | | | | | |
| Chi phí marketing & bán hàng | | | | | | | | | | | | | |
| Chi phí công nghệ | | | | | | | | | | | | | |
| Thuế VAT nộp | | | | | | | | | | | | | |
| Thuế TNCN nộp | | | | | | | | | | | | | |
| Chi phí khác | | | | | | | | | | | | | |
| **Tổng Tiền ra** | | | | | | | | | | | | | |
| **Net Operating Cash Flow** | | | | | | | | | | | | | |

**II. Dòng tiền từ Hoạt động Đầu tư (Investing Cash Flow)**

| Khoản mục | T1 | T2 | ... | T12 | Tổng |
|-----------|----|----|-----|-----|------|
| Mua TSCĐ, thiết bị | | | | | |
| Mua phần mềm, bản quyền | | | | | |
| Đầu tư tài chính | | | | | |
| Tiền thu từ thanh lý TSCĐ | | | | | |
| **Net Investing Cash Flow** | | | | | |

**III. Dòng tiền từ Hoạt động Tài chính (Financing Cash Flow)**

| Khoản mục | T1 | T2 | ... | T12 | Tổng |
|-----------|----|----|-----|-----|------|
| Vay ngân hàng mới | | | | | |
| Trả nợ gốc vay | | | | | |
| Trả lãi vay | | | | | |
| Nhận vốn góp | | | | | |
| Chia cổ tức | | | | | |
| **Net Financing Cash Flow** | | | | | |

**IV. Tổng hợp Dòng tiền**

| Khoản mục | T1 | T2 | ... | T12 |
|-----------|----|----|-----|-----|
| Số dư đầu kỳ | | | | |
| Net Cash Flow trong kỳ | | | | |
| **Số dư cuối kỳ** | | | | |
| Hạn mức tín dụng còn lại | | | | |
| **Khả năng thanh khoản tổng** | | | | |

### Phần 3: Phân tích Tháng Trọng yếu

#### 3.1 Xác định Tháng Căng thẳng Dòng tiền
- Tháng nào số dư tiền cuối kỳ thấp nhất?
- Tháng nào có nguy cơ âm tiền mặt?
- Nguyên nhân: doanh thu thấp, chi phí cao, hay cả hai?

#### 3.2 Kế hoạch Ứng phó cho Tháng Căng thẳng
- Biện pháp đẩy nhanh thu tiền: chính sách chiết khấu thanh toán sớm, đòi nợ tích cực hơn
- Biện pháp trì hoãn chi tiêu: đàm phán gia hạn với NCC, trì hoãn đầu tư không cấp bách
- Biện pháp bổ sung thanh khoản: rút hạn mức tín dụng, thu xếp vốn ngắn hạn

### Phần 4: Phân tích Nhạy cảm (Sensitivity Analysis)
| Kịch bản | Giả định thay đổi | Tác động lên số dư tiền tháng thấp nhất |
|----------|------------------|----------------------------------------|
| Base Case | Như kế hoạch | [Số dư] |
| Downside -20% DT | Doanh thu giảm 20% | [Số dư] |
| DSO tăng 15 ngày | KH trả chậm hơn | [Số dư] |
| Chi phí tăng 10% | Áp lực chi phí | [Số dư] |

### Phần 5: KPI Dòng tiền và Thanh khoản
- Cash Ratio = Tiền mặt / Nợ ngắn hạn (mục tiêu >1.0)
- Current Ratio = Tài sản ngắn hạn / Nợ ngắn hạn (mục tiêu >1.5)
- Operating Cash Flow / Net Income ratio
- Days Cash on Hand = Tiền mặt / (Chi phí hàng ngày) - cần duy trì tối thiểu [X] ngày
- Monthly Cash Burn Rate (nếu là startup chưa có lợi nhuận)

### Phần 6: Quy trình Quản lý Dòng tiền
- Cập nhật forecast hàng tuần: ai cập nhật, ai review
- Báo cáo dòng tiền tuần cho CEO: format và deadline
- Ngưỡng cảnh báo: khi số dư dự kiến xuống dưới [X] triệu thì báo cáo ngay
- Quy trình phê duyệt chi tiêu lớn trong bối cảnh căng thẳng dòng tiền

## Định dạng & Lưu trữ
- Format: .xlsx (mô hình động, tự tính toán khi thay đổi giả định)
- Đặt tên: [FORECAST/YYYY-MM] FIN-005 - Cash Flow Forecast 12M - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/04-Dong-Tien/
- Cập nhật hàng tháng với actual T-1 và rolling forecast 12 tháng tiếp theo

## Hướng dẫn cho Claude
1. Nhấn mạnh: dòng tiền ≠ lợi nhuận - doanh nghiệp lợi nhuận cao vẫn có thể chết vì thiếu tiền mặt.
2. DSO và DPO là 2 đòn bẩy quan trọng nhất - giảm DSO 15 ngày có thể giải phóng hàng trăm triệu tiền mặt.
3. Xây dựng mô hình Excel tự động: nhập số liệu thực tế tháng trước thì forecast tự cập nhật.
4. Phần tháng căng thẳng phải có kế hoạch ứng phó cụ thể - không chỉ là cảnh báo.
5. Rolling 12-month forecast (luôn nhìn 12 tháng phía trước) tốt hơn là forecast cố định theo năm tài chính.
6. Kết nối với lịch thuế để đưa các khoản thuế lớn vào đúng tháng phải nộp.
7. Review thực tế vs forecast hàng tháng để cải thiện độ chính xác của mô hình theo thời gian.
