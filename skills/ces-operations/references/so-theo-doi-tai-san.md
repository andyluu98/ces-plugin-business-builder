# Sổ Theo Dõi Tài Sản Doanh Nghiệp | ces-operations

## Mục đích & Phạm vi
Tài liệu này thiết lập hệ thống ghi nhận và theo dõi toàn bộ tài sản của doanh nghiệp trong suốt vòng đời từ khi mua đến khi thanh lý, đảm bảo kiểm soát tài sản chặt chẽ, ngăn ngừa thất thoát và cung cấp thông tin chính xác cho báo cáo tài chính. Áp dụng cho tất cả tài sản cố định và công cụ dụng cụ có giá trị đáng kể của doanh nghiệp.

## Câu hỏi thu thập thông tin
1. Tổng số tài sản hiện có và phân loại theo nhóm (IT, văn phòng, xe cộ, máy móc)?
2. Doanh nghiệp đang dùng phương pháp nào để theo dõi tài sản (Excel, phần mềm, thủ công)?
3. Ai chịu trách nhiệm quản lý sổ tài sản và ai có quyền cập nhật?
4. Tần suất kiểm kê tài sản và ai tham gia kiểm kê?
5. Cách dán nhãn/mã hóa tài sản hiện tại: tem dán, mã QR hay chưa có?
6. Tài sản được phân bổ cho từng phòng ban hay dùng chung?
7. Quy trình khi tài sản bị mất, hỏng hoặc cần thanh lý?

## Cấu trúc tài liệu

### Phần 1: Danh mục tài sản tổng hợp

**Bảng tổng hợp theo nhóm:**
| Nhóm tài sản | Số lượng | Nguyên giá (triệu) | Giá trị còn lại | Ghi chú |
|-------------|---------|-------------------|----------------|---------|
| Thiết bị IT (Laptop, PC, Server) | ... | ... | ... | |
| Thiết bị văn phòng (Máy in, điện thoại) | ... | ... | ... | |
| Nội thất (Bàn, ghế, tủ) | ... | ... | ... | |
| Phương tiện vận tải | ... | ... | ... | |
| Máy móc / Thiết bị sản xuất | ... | ... | ... | |
| Phần mềm / Tài sản vô hình | ... | ... | ... | |
| **Tổng cộng** | ... | ... | ... | |

### Phần 2: Sổ theo dõi tài sản chi tiết (Asset Register)

**Cấu trúc mỗi dòng trong sổ tài sản:**
| Trường | Mô tả | Ví dụ |
|--------|-------|-------|
| Mã tài sản | Mã duy nhất theo hệ thống | IT-LPT-001 |
| Tên tài sản | Tên đầy đủ và mô tả | Laptop Dell XPS 15 |
| Nhóm/Loại | Phân loại tài sản | Thiết bị IT |
| Nhà sản xuất / Thương hiệu | ... | Dell |
| Model / Số series | ... | XPS 9500 / SN12345 |
| Ngày mua | DD/MM/YYYY | 15/03/2023 |
| Nhà cung cấp | Tên NCC đã mua | Công ty XYZ |
| Số hóa đơn | Hóa đơn VAT mua tài sản | HD-2023-0456 |
| Nguyên giá | Giá mua ban đầu (VNĐ) | 35.000.000 |
| Thời gian khấu hao | Số năm khấu hao | 5 năm |
| Khấu hao/năm | Mức khấu hao hàng năm | 7.000.000 |
| Giá trị còn lại | Nguyên giá - Khấu hao lũy kế | 21.000.000 |
| Vị trí | Phòng / Khu vực đặt tài sản | Phòng IT - Tầng 3 |
| Người sử dụng | Nhân viên được giao | Nguyễn Văn A |
| Phòng ban | Phòng ban quản lý | IT |
| Tình trạng | Tốt / Cần sửa / Hỏng / Thanh lý | Tốt |
| Bảo hành đến | Ngày hết bảo hành | 15/03/2026 |
| Ngày kiểm kê gần nhất | ... | 31/12/2024 |
| Ghi chú | Thông tin bổ sung | Có vết xước nhỏ ở góc |

### Phần 3: Hệ thống mã hóa tài sản

**Quy tắc đặt mã tài sản:**
```
[Nhóm]-[Loại]-[Số thứ tự 3 chữ số]

Nhóm:
IT  = Công nghệ thông tin
VF  = Văn phòng (Furniture)
XT  = Xe và phương tiện
MM  = Máy móc sản xuất
SW  = Phần mềm

Loại (trong nhóm IT):
LPT = Laptop
PC  = Máy tính để bàn
SRV = Server
PRN = Máy in
PHN = Điện thoại

Ví dụ: IT-LPT-001, VF-DSK-015, XT-CAR-003
```

**Dán nhãn tài sản:**
- Tem nhãn tài sản: In mã QR hoặc barcode + Mã tài sản + Tên công ty
- Vị trí dán: Góc dưới bên phải của thiết bị, nơi dễ nhìn thấy
- Màu sắc tem theo nhóm tài sản (tùy chọn để nhận dạng nhanh)

### Phần 4: Quy trình cập nhật sổ tài sản

**Khi mua tài sản mới:**
1. Tài chính/kế toán thêm tài sản vào sổ sau khi thanh toán và nhận hàng
2. Gán mã tài sản và dán tem nhãn
3. Bàn giao cho người sử dụng và ghi nhận vào sổ
4. Lưu hồ sơ: Hóa đơn + Biên bản giao nhận

**Khi chuyển giao tài sản (người dùng thay đổi / chuyển phòng ban):**
1. Điền Phiếu chuyển giao tài sản
2. Người nhận ký xác nhận tình trạng
3. Cập nhật sổ: Người sử dụng mới, vị trí mới, ngày chuyển giao

**Khi tài sản hỏng / cần sửa chữa:**
1. Người dùng báo cáo IT/Hành chính
2. Cập nhật trạng thái tài sản: "Đang sửa chữa"
3. Ghi nhận chi phí sửa chữa (nếu hạch toán)
4. Cập nhật lại trạng thái sau khi sửa xong

**Khi thanh lý tài sản:**
1. Lập Hội đồng thanh lý (theo quy định nội bộ)
2. Lập Biên bản thanh lý tài sản
3. Xóa khỏi sổ tài sản đang sử dụng, chuyển sang sổ tài sản đã thanh lý
4. Hạch toán kế toán: Xóa sổ và ghi nhận lãi/lỗ thanh lý

### Phần 5: Kiểm kê tài sản định kỳ

**Quy trình kiểm kê hàng năm:**
- Thời điểm: Cuối năm tài chính (tháng 12)
- Đội kiểm kê: Hành chính/IT + Kế toán + Đại diện BGĐ
- Phương pháp: Đối chiếu tài sản thực tế với sổ sách từng mục
- Xử lý chênh lệch: Tài sản thừa (điều tra nguồn gốc), tài sản thiếu (xử lý trách nhiệm)
- Kết quả: Biên bản kiểm kê + Quyết định xử lý chênh lệch

**Mẫu Biên bản kiểm kê:**
| STT | Mã tài sản | Tên | Sổ sách (cái) | Thực tế (cái) | Chênh lệch | Ghi chú |
|-----|-----------|-----|--------------|--------------|-----------|---------|
| 1 | IT-LPT-001 | Laptop Dell | 1 | 1 | 0 | Tốt |
| 2 | VF-DSK-005 | Bàn họp | 1 | 0 | -1 | Không tìm thấy |

### Phần 6: Báo cáo tài sản định kỳ
- Báo cáo tháng: Biến động tài sản (mua mới, thanh lý, chuyển giao)
- Báo cáo quý: Khấu hao lũy kế và giá trị còn lại toàn bộ tài sản
- Báo cáo năm: Toàn bộ tài sản sau kiểm kê, phục vụ báo cáo tài chính năm

## Định dạng & Lưu trữ
- Format: .xlsx (sổ tài sản chính) + .docx (biên bản kiểm kê, chuyển giao, thanh lý)
- Đặt tên: [OPS-TS-01] Sổ theo dõi tài sản - [Tên công ty] [Năm] v1.0
- Thư mục: 03 Hành chính & Vận hành / Tài sản / Sổ theo dõi
- Cập nhật: Liên tục khi có biến động tài sản
- Phân quyền: Kế toán và Hành chính (chỉnh sửa), Trưởng phòng (xem)

## Lưu ý tuân thủ pháp lý
- Sổ tài sản cố định là tài liệu kế toán bắt buộc, lưu trữ tối thiểu 10 năm
- Khấu hao TSCĐ theo đúng khung Thông tư 45/2013/TT-BTC và sửa đổi
- Hội đồng thanh lý TSCĐ phải có quyết định thành lập và biên bản thanh lý
- Chênh lệch kiểm kê phải được giải trình và xử lý theo quy định kế toán

## Hướng dẫn cho Claude
1. Hỏi về số lượng và loại tài sản để đề xuất cấu trúc phân loại phù hợp
2. Tạo template Excel với tab riêng cho từng nhóm tài sản và tab tổng hợp
3. Xây dựng công thức tự động tính khấu hao và giá trị còn lại
4. Đề xuất hệ thống mã QR để kiểm kê nhanh bằng điện thoại
5. Gợi ý phần mềm quản lý tài sản phù hợp quy mô: từ Excel đến Asset Panda, EZOfficeInventory
6. Tạo dashboard tóm tắt: Tổng tài sản, tài sản sắp hết khấu hao, tài sản cần thay thế
