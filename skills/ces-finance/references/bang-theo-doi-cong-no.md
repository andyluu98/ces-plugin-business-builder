# Bảng Theo dõi Công nợ (Excel Template) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude thiết kế và hướng dẫn sử dụng Bảng Theo dõi Công nợ toàn diện trên Excel, bao gồm theo dõi công nợ phải thu (AR Tracker) và công nợ phải trả (AP Tracker). Đây là công cụ quản lý vốn lưu động hàng ngày, giúp kế toán và CFO nắm bắt ngay tình trạng thu hồi tiền từ khách hàng và lịch thanh toán nhà cung cấp. Phù hợp cho doanh nghiệp chưa có phần mềm ERP hoặc cần công cụ bổ sung bên cạnh phần mềm kế toán.

## Câu hỏi thu thập thông tin
1. Số lượng khách hàng có công nợ thường xuyên là bao nhiêu? Tổng giá trị AR trung bình hàng tháng?
2. Số lượng nhà cung cấp có công nợ thường xuyên là bao nhiêu?
3. Điều khoản thanh toán phổ biến với KH là gì? (Net 15/30/60...) Và với NCC?
4. Ai cập nhật bảng theo dõi này? Tần suất cập nhật mong muốn là hàng ngày hay hàng tuần?
5. Cần phân tích theo chiều nào: theo KH/NCC, theo sản phẩm, theo khu vực, theo sales rep?
6. Dashboard cần thể hiện những chỉ số gì cho CFO đọc hàng tuần?
7. Có cần tích hợp với lịch nhắc nhở tự động (email alert khi đến hạn) không?

## Cấu trúc tài liệu

### Phần 1: Hướng dẫn Sử dụng File Excel

#### 1.1 Cấu trúc File Excel (Nhiều Sheet)
```
Sheet 1: DASHBOARD        → Tóm tắt toàn bộ công nợ, KPI, cảnh báo
Sheet 2: AR_TRACKER       → Theo dõi công nợ phải thu từng KH
Sheet 3: AR_AGING         → Phân tích tuổi nợ phải thu
Sheet 4: AP_TRACKER       → Theo dõi công nợ phải trả từng NCC
Sheet 5: AP_AGING         → Phân tích tuổi nợ phải trả
Sheet 6: PAYMENT_SCHEDULE → Lịch thanh toán sắp tới (30 ngày)
Sheet 7: KH_LIST          → Danh mục khách hàng (lookup)
Sheet 8: NCC_LIST         → Danh mục nhà cung cấp (lookup)
```

#### 1.2 Quy ước Màu sắc (Conditional Formatting)
- Xanh lá: Chưa đến hạn (Current)
- Vàng: Sắp đến hạn trong 7 ngày
- Cam: Quá hạn 1-30 ngày
- Đỏ nhạt: Quá hạn 31-60 ngày
- Đỏ đậm: Quá hạn >60 ngày (cần hành động khẩn)

### Phần 2: Sheet AR_TRACKER - Theo dõi Công nợ Phải thu

#### 2.1 Cấu trúc Cột (Headers)

| Cột | Tên cột | Kiểu dữ liệu | Mô tả |
|-----|---------|-------------|-------|
| A | Mã KH | Text | Mã khách hàng trong hệ thống |
| B | Tên Khách hàng | Text | Tên đầy đủ công ty |
| C | Sales phụ trách | Text | Dropdown từ KH_LIST |
| D | Số Hóa đơn | Text | Số hóa đơn VAT |
| E | Ngày HĐ | Date | Ngày phát hành hóa đơn |
| F | Ngày đến hạn | Date | Ngày phải thanh toán theo HĐ |
| G | Số tiền HĐ | Number | Giá trị hóa đơn (VND) |
| H | Đã thanh toán | Number | Số tiền KH đã trả |
| I | Còn phải thu | Formula | =G-H (tự động tính) |
| J | Số ngày quá hạn | Formula | =IF(I>0,MAX(0,TODAY()-F),"Đã TT") |
| K | Nhóm tuổi nợ | Formula | =IF(J=0,"Current",IF(J<=30,"1-30",IF(J<=60,"31-60",IF(J<=90,"61-90",">90")))) |
| L | Ghi chú / Cam kết | Text | Ngày KH cam kết trả |
| M | Trạng thái | Dropdown | Current/Nhắc lần 1/Nhắc lần 2/Cảnh báo/Pháp lý |
| N | Ngày nhắc gần nhất | Date | Ngày đôn đốc gần nhất |
| O | Dự phòng % | Formula | Theo tuổi nợ: 0/10/30/50/100% |
| P | Số tiền dự phòng | Formula | =I*O |

#### 2.2 Dòng Tổng hợp theo Khách hàng (Subtotal)
Sử dụng SUMIF để tổng hợp theo từng KH:
- Tổng phải thu: =SUMIF(A:A, mã_kh, I:I)
- Tổng quá hạn: =SUMPRODUCT((A2:A1000=mã_kh)*(J2:J1000>0)*I2:I1000)

### Phần 3: Sheet AR_AGING - Phân tích Tuổi Nợ Phải thu

#### 3.1 Bảng Aging Report

| Khách hàng | Tổng AR | Current | 1-30 ngày | 31-60 ngày | 61-90 ngày | >90 ngày | Dự phòng |
|-----------|---------|---------|-----------|------------|------------|----------|---------|
| [KH 1] | | | | | | | |
| [KH 2] | | | | | | | |
| **TỔNG** | | | | | | | |
| **%** | 100% | | | | | | |

#### 3.2 Biểu đồ Aging (mô tả để tự tạo trong Excel)
- Stacked bar chart thể hiện tỷ trọng từng nhóm tuổi nợ
- Trend line: xu hướng tổng AR theo tháng
- DSO chart: DSO theo tháng trong 12 tháng gần nhất

### Phần 4: Sheet AP_TRACKER - Theo dõi Công nợ Phải trả

Cấu trúc tương tự AR_TRACKER nhưng với logic ngược:

| Cột | Tên cột | Mô tả |
|-----|---------|-------|
| A | Mã NCC | Mã nhà cung cấp |
| B | Tên NCC | Tên đầy đủ |
| C | Người phụ trách | Buyer/Procurement |
| D | Số HĐ/Invoice NCC | Số hóa đơn NCC gửi |
| E | Ngày nhận HĐ | Ngày nhận hóa đơn NCC |
| F | Ngày đến hạn | Ngày phải thanh toán |
| G | Số tiền | Giá trị phải trả |
| H | Đã thanh toán | Số tiền đã chi |
| I | Còn phải trả | =G-H |
| J | Ngày còn lại | =F-TODAY() (âm = quá hạn) |
| K | Trạng thái | Chưa đến hạn/Đến hạn/Quá hạn |
| L | Ưu tiên thanh toán | Cao/Trung bình/Thấp |
| M | Ghi chú | |

### Phần 5: Sheet PAYMENT_SCHEDULE - Lịch Thanh toán 30 Ngày

Tự động tổng hợp các khoản phải trả trong 30 ngày tới:

| Ngày đến hạn | Tên NCC | Số HĐ | Số tiền | Tài khoản NCC | Ghi chú |
|-------------|---------|-------|---------|--------------|---------|
| [tự lấy từ AP_TRACKER] | | | | | |

Tổng cần thanh toán tuần này: [SUM]
Tổng cần thanh toán tháng này: [SUM]
Số dư tiền mặt hiện tại: [Link từ quỹ]
**Thiếu hụt/Dư thừa:** [Chênh lệch]

### Phần 6: Sheet DASHBOARD - Bảng Điều khiển Tổng hợp

#### 6.1 KPI Box (4 ô lớn đầu trang)
```
┌──────────────────┬──────────────────┬──────────────────┬──────────────────┐
│  TỔNG AR         │  AR QUÁ HẠN      │  TỔNG AP         │  AP ĐẾN HẠN 7N   │
│  [X] triệu      │  [Y] triệu       │  [A] triệu       │  [B] triệu       │
│  DSO: [X] ngày  │  % quá hạn: [Y]% │  DPO: [A] ngày  │  Cần trả: [B]    │
└──────────────────┴──────────────────┴──────────────────┴──────────────────┘
```

#### 6.2 Bảng Cảnh báo Hành động (Action Required)
Top 10 KH có AR quá hạn cần xử lý ngay:
| # | KH | Số tiền quá hạn | Số ngày QH | Hành động cần thiết |
|---|----|-----------------|-----------|--------------------|

Top 5 NCC cần thanh toán trong 7 ngày:
| # | NCC | Số tiền | Ngày đến hạn | Ghi chú |
|---|-----|---------|-------------|---------|

#### 6.3 Biểu đồ Xu hướng
- Trend AR và AP theo 12 tháng
- DSO vs DPO comparison
- % AR quá hạn theo tháng

### Phần 7: Quy trình Cập nhật Hàng ngày/Tuần
- Ai cập nhật: Kế toán công nợ
- Khi nào cập nhật:
  - Ngay khi phát sinh giao dịch (thu tiền, phát hành HĐ)
  - Cuối mỗi ngày: kiểm tra ngày quá hạn mới
  - Hàng tuần thứ 2: CFO review dashboard
- Backup: tự động lưu phiên bản hàng tuần vào Google Drive

## Định dạng & Lưu trữ
- Format: .xlsx (Google Sheets hoặc Excel Online để cộng tác thời gian thực)
- Đặt tên: [TRACKER/YYYY] FIN-014 - Bang Theo Doi Cong No - KeToan v[X.X]
- Thư mục lưu: 02-Tai-Chinh/06-Cong-No/
- Lưu phiên bản cuối tháng: 02-Tai-Chinh/06-Cong-No/[YYYY]/Archive/

## Hướng dẫn cho Claude
1. Conditional formatting màu sắc là tính năng quan trọng nhất - giúp phát hiện vấn đề ngay khi mở file.
2. Mọi tính toán phải dùng formula tự động - không để kế toán tự tính tay rồi nhập số.
3. Sheet PAYMENT_SCHEDULE là công cụ quản lý dòng tiền ngắn hạn quan trọng - phải luôn cập nhật.
4. Dashboard phải đơn giản đủ để CEO đọc trong 2 phút, không cần mở sheet chi tiết.
5. Hướng dẫn protect sheet với password để tránh người dùng vô tình xóa formula.
6. Gợi ý Google Sheets + Zapier để tự động gửi email nhắc nhở khi KH đến hạn.
7. Kết nối file này với Cash Flow Forecast: AP đến hạn là tiền ra, AR đến hạn là tiền vào.
