# SOP Thu chi Tiền mặt và Chuyển khoản | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng SOP (Standard Operating Procedure) chi tiết cho quy trình thu chi tiền mặt và chuyển khoản ngân hàng. SOP này đảm bảo mọi giao dịch tài chính được thực hiện đúng quy trình, có kiểm soát kép, chứng từ đầy đủ và được ghi nhận chính xác vào sổ kế toán. Phù hợp cho doanh nghiệp muốn chuẩn hóa quy trình tài chính, giảm thiểu rủi ro sai sót và gian lận trong giao dịch tiền tệ hàng ngày.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp có bao nhiêu quỹ tiền mặt? Mỗi quỹ do ai quản lý và hạn mức tối đa là bao nhiêu?
2. Có bao nhiêu tài khoản ngân hàng? Mỗi tài khoản dùng cho mục đích gì?
3. Phần mềm kế toán đang dùng là gì? Quy trình nhập liệu giao dịch hiện tại như thế nào?
4. Ai có quyền ký chứng từ thu chi tiền mặt? Ai có quyền ký lệnh chuyển khoản?
5. Hệ thống kiểm soát hiện tại có những điểm yếu nào? Đã từng xảy ra sai sót hoặc thất thoát chưa?
6. Tần suất đối soát quỹ tiền mặt và sao kê ngân hàng hiện tại là gì? Ai thực hiện?
7. Các loại giao dịch thu chi phổ biến nhất hàng ngày là gì? Giá trị trung bình mỗi giao dịch?

## Cấu trúc tài liệu

### Phần 1: Phạm vi và Nguyên tắc

#### 1.1 Phạm vi Áp dụng
- Áp dụng cho: tất cả giao dịch thu chi tiền mặt và chuyển khoản của doanh nghiệp
- Không áp dụng: giao dịch nội bộ bù trừ (xử lý theo SOP riêng)
- Người thực hiện: kế toán quỹ, kế toán ngân hàng, thủ quỹ

#### 1.2 Nguyên tắc Kiểm soát Cốt lõi
- **Tách biệt nhiệm vụ:** Người thu/chi ≠ người ghi sổ ≠ người phê duyệt
- **Kiểm soát kép:** Mọi chuyển khoản >X triệu cần 2 người ký (Maker + Checker)
- **Chứng từ trước, tiền sau:** Không chi tiền khi chưa có chứng từ phê duyệt đầy đủ
- **Hạn mức quỹ tiền mặt:** Không giữ quá [X] triệu VND tiền mặt tại quỹ
- **Không dùng tiền công ty cho mục đích cá nhân** dù tạm thời

### Phần 2: Quy trình Thu Tiền

#### 2.1 Thu Tiền mặt từ Khách hàng

**Sơ đồ Quy trình:**
```
KH đến thanh toán
       ↓
Kế toán/Thu ngân kiểm tra hóa đơn/biên bản nghiệm thu
       ↓
Lập Phiếu Thu (PT) trên phần mềm kế toán
       ↓
In PT, KH ký xác nhận
       ↓
Thủ quỹ đếm tiền, ký nhận PT
       ↓
Ghi nhận vào sổ quỹ
       ↓
KH nhận liên Phiếu Thu
       ↓
Cuối ngày: nộp tiền vào két sắt hoặc ngân hàng
```

**Bảng Phân công:**
| Bước | Người thực hiện | Thời gian tối đa | Chứng từ |
|------|----------------|-----------------|---------|
| Kiểm tra hóa đơn | Kế toán bán hàng | Ngay lập tức | Hóa đơn/BB |
| Lập Phiếu Thu | Kế toán quỹ | 5 phút | PT (3 liên) |
| Thu tiền & ký | Thủ quỹ | Ngay | PT đã ký |
| Ghi sổ quỹ | Kế toán quỹ | Cuối ngày | Sổ quỹ |
| Nộp ngân hàng | Thủ quỹ | Cuối ngày | Giấy nộp tiền |

**Kiểm soát:**
- Số Phiếu Thu phải liên tục, không được có khoảng trống
- Phiếu Thu bị hủy phải giữ lại đủ 3 liên, ghi chú "Hủy"
- Tiền thừa/thiếu so với Phiếu Thu: xử lý ngay, ghi nhận và báo cáo

#### 2.2 Thu Tiền qua Chuyển khoản Ngân hàng

```
Nhận thông báo thanh toán từ KH (email/SMS/app)
       ↓
Kế toán xác nhận số tiền khớp với hóa đơn
       ↓
Ghi nhận vào phần mềm kế toán (match với hóa đơn)
       ↓
Cập nhật trạng thái hóa đơn: "Đã thanh toán"
       ↓
Gửi xác nhận đã nhận tiền cho KH (nếu cần)
       ↓
Xuất sao kê tổng hợp cuối ngày
```

### Phần 3: Quy trình Chi Tiền

#### 3.1 Chi Tiền mặt từ Quỹ

**Điều kiện Chi:**
- Có Phiếu Đề nghị Chi đã được phê duyệt đúng thẩm quyền
- Số tiền chi ≤ hạn mức phê duyệt tiền mặt: [X] triệu VND/lần
- Giao dịch >hạn mức phải chuyển khoản, không chi tiền mặt

**Sơ đồ Quy trình:**
```
Người đề nghị nộp Phiếu Đề nghị Chi + Chứng từ gốc
       ↓
Kế toán kiểm tra: đủ chứng từ? Đúng thẩm quyền?
       ↓
Thủ quỹ kiểm tra số dư quỹ
       ↓
Lập Phiếu Chi (PC) trên phần mềm
       ↓
PC được ký bởi: Thủ quỹ + Kế toán trưởng/CFO
       ↓
Chi tiền, người nhận ký PC
       ↓
Ghi sổ quỹ và phần mềm kế toán
```

#### 3.2 Chi Tiền qua Chuyển khoản Ngân hàng

**Quy trình Chuẩn:**
```
Bước 1 (MAKER - Kế toán):
- Kiểm tra Phiếu Đề nghị Thanh toán + chứng từ gốc
- Lập lệnh chuyển khoản trên Internet Banking
- Đính kèm ảnh chứng từ vào lệnh
- Chuyển sang Checker

Bước 2 (CHECKER - Kế toán trưởng/CFO):
- Kiểm tra đối chiếu: đúng người nhận, số tiền, số tài khoản?
- Đối chiếu với chứng từ đính kèm
- Nếu đúng: phê duyệt (duyệt trên app/token)
- Nếu sai: từ chối và yêu cầu chỉnh sửa

Bước 3 (Ghi nhận):
- Ghi nhận vào phần mềm kế toán sau khi chuyển khoản thành công
- Lưu xác nhận chuyển khoản vào hồ sơ
```

**Lịch Chuyển khoản:**
- Thông thường: 2 lần/tuần (Thứ 3 và Thứ 5) trước 15:00
- Khẩn cấp: được phép nhưng cần ghi lý do và phê duyệt thêm 1 cấp

**Kiểm soát Bổ sung cho Chuyển khoản Lớn:**
- >50 triệu: CFO phải là Checker
- >200 triệu: CEO phải phê duyệt thêm
- Thêm tài khoản mới vào danh mục: cần phê duyệt của CEO + thông báo qua email riêng

### Phần 4: Đối soát và Kiểm tra Định kỳ

#### 4.1 Đối soát Quỹ Tiền mặt
- Hàng ngày: Thủ quỹ kiểm đếm tiền mặt và khớp với sổ quỹ cuối ngày
- Hàng tuần: Kế toán trưởng kiểm tra đột xuất (không báo trước) một lần/tuần
- Hàng tháng: Kiểm kê quỹ có biên bản ký xác nhận bởi thủ quỹ + kế toán trưởng + người kiểm tra độc lập
- Xử lý chênh lệch: ghi nhận ngay, điều tra nguyên nhân trong 24 giờ

#### 4.2 Đối soát Sao kê Ngân hàng (Bank Reconciliation)
- Tần suất: hàng tháng, trong vòng 5 ngày làm việc sau khi nhận sao kê
- Người thực hiện: Kế toán ngân hàng (không phải người chi tiền)
- Quy trình: đối chiếu từng giao dịch trên sao kê với sổ sách kế toán
- Xử lý chênh lệch: báo cáo ngay lên Kế toán trưởng nếu phát hiện bất thường

### Phần 5: Xử lý Tình huống Bất thường
- Phát hiện tiền giả: quy trình báo cáo và xử lý
- Mất tiền mặt: quy trình khóa quỹ, điều tra, báo cáo công an
- Chuyển khoản nhầm: quy trình liên hệ ngân hàng xin hoàn tiền khẩn cấp
- Giao dịch nghi ngờ gian lận: quy trình báo cáo whistleblower

## Định dạng & Lưu trữ
- Format: .docx (SOP chính) + sơ đồ quy trình (flowchart PNG)
- Đặt tên: [SOP/YYYY] FIN-010 - SOP Thu Chi Tien Mat Chuyen Khoan - KeToan v[X.X]
- Thư mục lưu: 02-Tai-Chinh/05-SOP-Ke-Toan/
- Review hàng năm hoặc khi có thay đổi phần mềm, nhân sự chủ chốt

## Hướng dẫn cho Claude
1. Sơ đồ quy trình (flowchart) là quan trọng nhất - người thực hiện cần nhìn vào và hiểu ngay không cần đọc toàn bộ.
2. Nguyên tắc Maker-Checker cho chuyển khoản phải được thực thi không có ngoại lệ.
3. Hạn mức tiền mặt phải thực tế - quá thấp thì không vận hành được, quá cao thì rủi ro.
4. Phần xử lý bất thường thường bị bỏ qua nhưng quan trọng khi sự cố xảy ra.
5. Tích hợp với phần mềm kế toán cụ thể của doanh nghiệp - đừng viết SOP chung chung.
6. Training ngắn 30 phút cho nhân viên mới khi gia nhập bộ phận kế toán là bắt buộc.
7. Test SOP với kế toán trẻ nhất - nếu họ làm được mà không cần hỏi thì SOP đã đủ rõ.
