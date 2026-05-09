# Cap Table – Quản Lý Cổ Phần và Quyền Sở Hữu | ces-growth

## Mục đích & Phạm vi
Tài liệu này hướng dẫn xây dựng và duy trì Cap Table (Capitalization Table) — bảng quản lý toàn bộ cơ cấu sở hữu của doanh nghiệp, bao gồm cổ phần phổ thông, cổ phần ưu đãi, quyền mua cổ phần (options/warrants), và tác động pha loãng của các vòng đầu tư. Cap Table là tài liệu sống, được cập nhật mỗi khi có thay đổi cơ cấu sở hữu.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp được thành lập như thế nào? Vốn điều lệ ban đầu? Ai là cổ đông sáng lập và tỷ lệ?
2. Đã có vòng gọi vốn nào chưa? Nhà đầu tư nào và tỷ lệ sở hữu là bao nhiêu?
3. Có Employee Stock Option Plan (ESOP) không? Pool size là bao nhiêu %?
4. Có warrant, convertible note, hay SAFE nào đang outstanding không?
5. Valuation hiện tại (hoặc latest valuation) là bao nhiêu?
6. Có kế hoạch gọi vốn vòng mới không? Dự kiến dilution là bao nhiêu?
7. Ai hiện đang quản lý Cap Table? Dùng công cụ gì (Excel, Carta, AngelList)?

## Cấu trúc tài liệu

### Phần 1: Thông tin cơ bản doanh nghiệp
- Tên công ty và mã số doanh nghiệp
- Vốn điều lệ đăng ký và đã góp
- Tổng số cổ phần được phép phát hành (Authorized Shares)
- Tổng số cổ phần đang lưu hành (Issued & Outstanding Shares)
- Ngày cập nhật gần nhất

### Phần 2: Cap Table Hiện Tại (Summary View)

| Cổ đông | Loại cổ phần | Số cổ phần | % Fully Diluted | Giá trị (VND) |
|---------|-------------|-----------|----------------|--------------|
| **FOUNDERS** | | | | |
| [Tên Founder 1] | Common | | | |
| [Tên Founder 2] | Common | | | |
| **NHÀ ĐẦU TƯ** | | | | |
| [Investor 1] | Series A Preferred | | | |
| [Investor 2] | Series A Preferred | | | |
| **ESOP POOL** | | | | |
| Đã cấp (Granted) | Options | | | |
| Chưa cấp (Unissued) | Options | | | |
| **WARRANTS / SAFE / NOTES** | | | | |
| [Tên] | [Loại] | | | |
| **TỔNG** | | | **100%** | |

*Fully Diluted = bao gồm tất cả options, warrants, convertibles nếu được thực hiện*

### Phần 3: Chi Tiết Từng Loại Cổ Phần

**3.1 Common Shares (Cổ phần phổ thông)**
| Cổ đông | Ngày nhận | Số cổ phần | Vesting schedule | Shares vested | Shares unvested |
|---------|----------|-----------|----------------|--------------|-----------------|
| Founder 1 | | | 4Y/1Y cliff | | |
| Founder 2 | | | 4Y/1Y cliff | | |
| Early employee | | | 4Y/1Y cliff | | |

**3.2 Preferred Shares (Cổ phần ưu đãi)**
| Nhà đầu tư | Vòng | Ngày | Số CP | Giá/CP | Tổng đầu tư | Liquidation Pref |
|-----------|------|------|-------|--------|------------|-----------------|
| [Investor] | Seed | | | | | 1x non-participating |

**3.3 ESOP (Employee Stock Option Plan)**
- ESOP Pool size: ___% fully diluted
- Đã cấp: ___ options cho ___ nhân viên
- Chưa cấp: ___ options

| Nhân viên | Ngày grant | Số options | Strike price | Vesting | Expiry |
|----------|-----------|-----------|-------------|---------|--------|

**3.4 Convertibles (SAFE, Notes, Warrants)**
| Holder | Loại | Số tiền | Valuation Cap | Discount | Maturity/Trigger |
|--------|------|---------|--------------|---------|-----------------|

### Phần 4: Waterfall Analysis (Phân tích phân chia tại Exit)

Mô phỏng phân chia tiền khi bán công ty tại các mức giá khác nhau:

| Exit Value | Common | Series A Pref | Founder 1 | Founder 2 | Investor |
|-----------|--------|--------------|-----------|-----------|---------|
| 50 tỷ VND | | | | | |
| 100 tỷ VND | | | | | |
| 200 tỷ VND | | | | | |
| 500 tỷ VND | | | | | |

*Phân tích này phụ thuộc vào cấu trúc liquidation preference*

### Phần 5: Pro-forma Cap Table (Sau vòng gọi vốn mới)

Mô phỏng pha loãng khi gọi vốn vòng mới:

**Giả định:**
- Investment: ___ tỷ VND
- Pre-money valuation: ___ tỷ VND
- New shares issued: ___
- ESOP pool refresh (nếu có): ___

| Cổ đông | Trước | % Trước | Sau | % Sau | Dilution |
|---------|-------|--------|-----|-------|---------|

### Phần 6: Lịch Sử Thay Đổi Cap Table
| Ngày | Sự kiện | Chi tiết | Người thực hiện | Văn bản pháp lý |
|------|---------|---------|----------------|----------------|
| | Thành lập | Vốn ban đầu | | ĐKKD |
| | Seed Round | Phát hành Series A | | SHA |
| | ESOP Grant | Cấp options cho 5 NV | | ESOP Agreement |

## Định dạng & Lưu trữ
- Format: .xlsx (tính năng model đầy đủ) + công cụ chuyên dụng nếu có (Carta, Pulley)
- Đặt tên: `[CAP/YYYY-MM] GRW-CAP-001 - Cap Table [Tên CT] - CFO CONFIDENTIAL v1.0`
- Thư mục: `00 Hội Đồng ĐH / 03 Cap Table`
- Cập nhật: Sau mỗi sự kiện thay đổi cơ cấu sở hữu
- Bảo mật: Tối mật — chỉ founders, CFO, và nhà đầu tư

## Hướng dẫn cho Claude
1. Bắt đầu bằng cách thu thập thông tin lịch sử đầy đủ — mỗi lần thay đổi sở hữu cần được ghi nhận chính xác.
2. Luôn tính "Fully Diluted" cap table — bao gồm tất cả options và convertibles chưa chuyển đổi.
3. Waterfall Analysis là phần quan trọng để founders và nhà đầu tư hiểu rõ ai nhận được gì khi exit.
4. Nhắc rằng Cap Table cần khớp 100% với sổ đăng ký cổ đông pháp lý — bất kỳ mâu thuẫn nào đều gây vấn đề pháp lý.
5. Gợi ý dùng công cụ chuyên dụng (Carta, Pulley, Capdesk) thay vì Excel khi số lượng cổ đông và giao dịch tăng.
6. Mô phỏng pro-forma trước khi gọi vốn để founders thấy rõ dilution effect và đàm phán valuation phù hợp.
