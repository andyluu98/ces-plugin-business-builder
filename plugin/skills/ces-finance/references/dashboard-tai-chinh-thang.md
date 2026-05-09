# Dashboard Tài chính Theo dõi Hàng tháng | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude thiết kế Financial Dashboard hàng tháng - bảng điều khiển tài chính tổng hợp giúp CEO và CFO nắm bắt toàn bộ sức khỏe tài chính của doanh nghiệp trong 5-10 phút mỗi tháng. Dashboard kết hợp dữ liệu từ P&L, Cash Flow, Balance Sheet và các KPI vận hành thành một trang trực quan duy nhất với hệ thống đèn hiệu xanh-vàng-đỏ. Phù hợp cho CFO muốn trình bày báo cáo tài chính cho CEO/Hội đồng quản trị theo cách hiệu quả và dễ hiểu nhất.

## Câu hỏi thu thập thông tin
1. Đối tượng chính đọc dashboard là ai? CEO, HĐQT, nhà đầu tư hay cả ba? Mức độ hiểu biết tài chính của họ?
2. KPI tài chính nào CEO quan tâm nhất hàng tháng? (Doanh thu, dòng tiền, margin, công nợ...)
3. Doanh nghiệp có OKR/KPI vận hành nào cần theo dõi song song với tài chính không?
4. Dashboard sẽ được trình bày: trên màn hình (PowerPoint/Slides), in ra hay trên Google Sheets/Notion?
5. Tần suất cập nhật: hàng tuần hay chỉ cập nhật khi chốt số tháng?
6. Ngưỡng cảnh báo (threshold) cho từng KPI là gì? Khi nào chuyển từ xanh sang vàng, từ vàng sang đỏ?
7. Có muốn so sánh với cùng kỳ năm ngoái (YoY) bên cạnh so sánh với tháng trước (MoM) không?

## Cấu trúc tài liệu

### Phần 1: Thiết kế Dashboard - Tổng quan Layout

#### 1.1 Nguyên tắc Thiết kế
- **One page rule:** Toàn bộ dashboard phải vừa trong 1-2 trang A4 hoặc 1 màn hình
- **5-second rule:** CEO phải hiểu tình hình tài chính trong 5 giây đầu nhìn vào
- **Traffic light system:** Xanh (tốt) / Vàng (chú ý) / Đỏ (hành động ngay)
- **Exception reporting:** Chỉ highlight những gì cần chú ý, không báo cáo mọi thứ

#### 1.2 Cấu trúc Layout Đề xuất
```
┌─────────────────────────────────────────────────────────────────┐
│  FINANCIAL DASHBOARD | [Tháng/Năm] | Cập nhật: [DD/MM/YYYY]    │
├─────────────┬─────────────┬─────────────┬───────────────────────┤
│ DOANH THU   │ LỢI NHUẬN   │ DÒNG TIỀN   │  CÔNG NỢ              │
│ [KPI Box]   │ [KPI Box]   │ [KPI Box]   │  [KPI Box]            │
├─────────────┴─────────────┴─────────────┴───────────────────────┤
│ TREND CHART: Doanh thu & Lợi nhuận 12 tháng                     │
├─────────────────────────┬───────────────────────────────────────┤
│ P&L Tóm tắt             │ CASH POSITION                        │
│ vs Budget vs Tháng trước│ Số dư tiền + Hạn mức tín dụng       │
├─────────────────────────┼───────────────────────────────────────┤
│ TOP 5 RỦI RO / HÀNH ĐỘNG│ KPI OPERATIONS                       │
│ CẦN THỰC HIỆN NGAY      │ (DSO, DPO, Headcount, NPS...)        │
└─────────────────────────┴───────────────────────────────────────┘
```

### Phần 2: Các KPI Box - Chỉ số Tài chính Chính

#### Thiết kế KPI Box (áp dụng cho mỗi KPI):
```
┌─────────────────────────────┐
│ [Tên KPI]                   │
│                             │
│  [GIÁ TRỊ THỰC TẾ]         │
│  [Đơn vị]                   │
│                             │
│ vs Budget: [+/-X%] [↑↓]    │
│ vs Tháng trước: [+/-Y%]    │
│ vs Cùng kỳ năm ngoái: [Z%] │
│                             │
│ Trạng thái: [🟢/🟡/🔴]    │
└─────────────────────────────┘
```

#### KPI Box 1: Doanh thu
- Doanh thu tháng thực tế (VND)
- % vs Budget tháng
- % tăng trưởng MoM
- % tăng trưởng YoY
- YTD vs YTD Budget
- Ngưỡng: Xanh (>95% budget) / Vàng (85-95%) / Đỏ (<85%)

#### KPI Box 2: Gross Profit & Margin
- Gross Profit tháng (VND)
- Gross Margin % tháng
- vs Gross Margin % tháng trước
- vs Gross Margin % Budget
- Ngưỡng: Xanh (>GM% mục tiêu) / Vàng (-2pp) / Đỏ (-5pp)

#### KPI Box 3: EBITDA
- EBITDA tháng (VND) và margin %
- YTD EBITDA
- vs Budget
- Ngưỡng tùy theo mục tiêu lợi nhuận doanh nghiệp

#### KPI Box 4: Cash Position
- Tiền mặt + tiền gửi hiện tại (VND)
- Hạn mức tín dụng còn lại
- Tổng thanh khoản khả dụng
- Runway (tháng) = Tiền mặt / Monthly Cash Burn
- Ngưỡng: Xanh (>3 tháng runway) / Vàng (1-3 tháng) / Đỏ (<1 tháng)

#### KPI Box 5: Công nợ
- Tổng AR (VND) và DSO (ngày)
- % AR quá hạn >30 ngày
- Tổng AP và DPO
- Ngưỡng: Xanh (DSO < target) / Vàng (+5 ngày) / Đỏ (+10 ngày)

### Phần 3: P&L Summary Table

| Chỉ tiêu | Tháng này | Budget | vs Budget | Tháng trước | MoM% | YTD Thực | YTD Budget |
|---------|-----------|--------|-----------|-------------|------|----------|-----------|
| Doanh thu | | | | | | | |
| COGS | | | | | | | |
| Gross Profit | | | | | | | |
| GM% | | | | | | | |
| Chi phí bán hàng | | | | | | | |
| Chi phí marketing | | | | | | | |
| Chi phí G&A | | | | | | | |
| EBITDA | | | | | | | |
| EBITDA% | | | | | | | |
| Net Profit | | | | | | | |
| Net Margin% | | | | | | | |

*Màu đỏ: vượt budget chi phí >10% hoặc thiếu budget doanh thu >10%*

### Phần 4: Cash Flow Summary

```
CASH POSITION - [Tháng/Năm]
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Số dư đầu tháng:     [X] tỷ
+ Thu từ KH:         [+Y] tỷ
- Chi cho NCC:       [-Z] tỷ
- Chi lương:         [-A] tỷ
- Chi khác:          [-B] tỷ
= Operating CF:      [±C] tỷ
- Đầu tư:           [-D] tỷ
+/- Vay/Trả nợ:     [±E] tỷ
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Số dư cuối tháng:    [F] tỷ
Hạn mức tín dụng:   [G] tỷ
TỔNG THANH KHOẢN:    [F+G] tỷ
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Phần 5: Trending Charts (12 Tháng)

Mô tả các biểu đồ cần tạo:
1. **Revenue & Gross Profit Trend:** Cột chart 12 tháng, 2 chuỗi
2. **EBITDA Margin Trend:** Line chart, có đường budget tham chiếu
3. **Cash Balance Trend:** Area chart, highlight tháng thấp nhất
4. **DSO & DPO Trend:** Dual-axis line chart

### Phần 6: KPI Vận hành Bổ sung

| KPI | Đơn vị | Tháng này | Tháng trước | Mục tiêu | Trạng thái |
|-----|--------|-----------|------------|---------|-----------|
| Headcount | Người | | | | |
| Revenue/FTE | Triệu VND | | | | |
| Số KH mới | KH | | | | |
| Tỷ lệ giữ chân KH | % | | | | |
| NPS (nếu đo) | Điểm | | | | |
| DSO | Ngày | | | | |
| DPO | Ngày | | | | |
| % AR quá hạn | % | | | | |

### Phần 7: Top Actions Required (Hành động Cần Thực hiện)

```
🔴 CRITICAL (Cần hành động trong tuần này):
   1. [Vấn đề cụ thể] → [Hành động] → [Người chịu trách nhiệm] → [Deadline]
   2. ...

🟡 ATTENTION (Theo dõi chặt trong tháng tới):
   1. [Vấn đề cụ thể] → [Hành động] → [Owner] → [Timeline]
   2. ...

🟢 GOOD NEWS (Điểm tích cực cần khuếch đại):
   1. [Thành tích] → [Cách nhân rộng]
   2. ...
```

### Phần 8: Ngưỡng và Hệ thống Cảnh báo

Bảng định nghĩa ngưỡng traffic light cho từng KPI:
| KPI | Xanh (Tốt) | Vàng (Chú ý) | Đỏ (Hành động ngay) |
|-----|-----------|------------|-------------------|
| DT vs Budget | >95% | 85-95% | <85% |
| Gross Margin | >GM mục tiêu | -2pp so mục tiêu | <-5pp |
| Cash Runway | >3 tháng | 1-3 tháng | <1 tháng |
| DSO | <DSO target | +5 ngày | +10 ngày |
| % AR quá hạn | <10% | 10-20% | >20% |
| EBITDA margin | >mục tiêu | -3pp | <0% (lỗ) |

### Phần 9: Quy trình Tạo và Phát hành Dashboard
- Ai tạo dashboard: CFO hoặc Financial Analyst
- Timeline: hoàn thành trước ngày 10 tháng sau
- Review: CFO đọc và bổ sung nhận xét trước khi gửi CEO
- Phát hành: email kèm file PDF/link Notion/Google Slides
- Meeting: 30 phút monthly financial review với CEO sau khi phát hành

## Định dạng & Lưu trữ
- Format: Google Slides / PowerPoint (1-2 trang trình chiếu) + Google Sheets (dữ liệu nguồn)
- Đặt tên: [DASHBOARD/YYYY-MM] FIN-020 - Financial Dashboard [Thang] - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/10-Dashboard/[YYYY]/
- Archive: lưu tất cả dashboard hàng tháng để theo dõi xu hướng dài hạn

## Hướng dẫn cho Claude
1. Dashboard phải cung cấp insight, không chỉ là data dump - mỗi số liệu phải có context (tốt hay xấu so với gì).
2. Traffic light system phải nhất quán và được định nghĩa rõ ràng trước - không thay đổi ngưỡng tùy tiện.
3. "Top Actions Required" là phần có giá trị thực tế nhất - đây là lý do CEO cần đọc dashboard.
4. Thiết kế cho đối tượng ít kiến thức tài chính nhất trong phòng: CEO thường không phải CFO.
5. Biểu đồ 12 tháng quan trọng hơn số tháng đơn lẻ - xu hướng mới là thông tin.
6. Tự động hóa tối đa: Google Sheets kết nối Google Slides để cập nhật số tự động.
7. Thêm "Điểm tin tốt" (Good News) để tạo cân bằng - dashboard không chỉ báo cáo vấn đề.
