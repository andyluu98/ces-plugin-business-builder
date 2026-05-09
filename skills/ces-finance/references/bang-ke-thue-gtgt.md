# Bảng kê Thuế GTGT Đầu vào/Đầu ra | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng bộ Bảng kê Thuế GTGT (Giá trị Gia tăng) đầu vào và đầu ra, hỗ trợ doanh nghiệp lập tờ khai thuế VAT hàng tháng/quý theo đúng quy định của Tổng cục Thuế Việt Nam (Mẫu 01/GTGT và các phụ lục). Tài liệu bao gồm template bảng kê Excel, hướng dẫn điền thông tin, các lưu ý kiểm soát chất lượng và quy trình đối soát trước khi nộp. Phù hợp cho kế toán thuế của doanh nghiệp nộp VAT theo phương pháp khấu trừ.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp khai thuế VAT theo kỳ nào: hàng tháng hay hàng quý? Kỳ tính thuế bắt đầu từ khi nào?
2. Phương pháp tính thuế VAT: phương pháp khấu trừ (trực tiếp trên GTGT nếu là hộ kinh doanh)?
3. Có phát sinh hóa đơn đầu vào mua hàng từ nhiều mức thuế suất không? (0%, 5%, 8%, 10%)
4. Có doanh thu từ hàng hóa/dịch vụ xuất khẩu (thuế suất 0%) không?
5. Phần mềm hóa đơn điện tử đang dùng là gì? Có thể xuất dữ liệu hóa đơn dưới dạng Excel không?
6. Số lượng hóa đơn đầu vào và đầu ra trung bình mỗi tháng là bao nhiêu?
7. Đã từng bị cơ quan thuế phát hiện sai sót trong khai báo VAT chưa? Loại sai sót nào?

## Cấu trúc tài liệu

### Phần 1: Tổng quan Thuế GTGT và Phương pháp Khấu trừ

#### 1.1 Nguyên tắc Cơ bản
- Thuế GTGT phải nộp = Thuế GTGT đầu ra - Thuế GTGT đầu vào được khấu trừ
- Nếu kết quả âm: được hoàn thuế hoặc khấu trừ kỳ sau
- Điều kiện khấu trừ thuế đầu vào: có hóa đơn hợp pháp + thanh toán qua ngân hàng (>20 triệu)

#### 1.2 Các Mức Thuế suất GTGT hiện hành
- 0%: Xuất khẩu hàng hóa/dịch vụ, vận tải quốc tế
- 5%: Hàng hóa thiết yếu (nước sạch, phân bón, thuốc chữa bệnh, sách giáo khoa...)
- 8%: Áp dụng theo chính sách giảm thuế tạm thời (cần kiểm tra thời hạn hiệu lực)
- 10%: Hàng hóa, dịch vụ thông thường (mức chuẩn)
- Không chịu thuế: theo danh mục Điều 5 Luật GTGT (dịch vụ y tế, giáo dục, tín dụng...)

### Phần 2: Bảng kê Hóa đơn Đầu ra (Phụ lục 01-1/GTGT)

#### 2.1 Cấu trúc Bảng kê Đầu ra

| STT | Tên người mua | MST người mua | Số HĐ | Ký hiệu HĐ | Ngày HĐ | Doanh thu chưa thuế | Thuế suất | Tiền thuế | Ghi chú |
|-----|-------------|---------------|-------|------------|---------|---------------------|-----------|-----------|---------|
| 1 | [Tên KH] | [MST] | [Số] | [Ký hiệu] | DD/MM/YYYY | | 10% | | |
| 2 | | | | | | | 5% | | |

**Tổng hợp Đầu ra theo Thuế suất:**
| Thuế suất | Doanh thu chưa thuế | Tiền thuế |
|----------|---------------------|-----------|
| 0% | | |
| 5% | | |
| 8% | | |
| 10% | | |
| Không chịu thuế | | 0 |
| **Tổng** | | |

#### 2.2 Kiểm soát Chất lượng Bảng kê Đầu ra
- [ ] Tổng doanh thu trên bảng kê khớp với sổ kế toán tài khoản 511/512
- [ ] Tổng tiền thuế đầu ra khớp với TK 33311
- [ ] Tất cả hóa đơn trong kỳ đã được đưa vào bảng kê (không bỏ sót)
- [ ] Hóa đơn hủy/điều chỉnh đã được xử lý đúng (trừ ra hoặc ghi âm)
- [ ] MST người mua điền đúng và đầy đủ
- [ ] Ngày hóa đơn trong đúng kỳ khai báo

### Phần 3: Bảng kê Hóa đơn Đầu vào (Phụ lục 01-2/GTGT)

#### 3.1 Cấu trúc Bảng kê Đầu vào

| STT | Tên người bán | MST người bán | Số HĐ | Ký hiệu | Ngày HĐ | Giá trị HHDV mua vào chưa thuế | Thuế suất | Tiền thuế | Phương thức TT | Ghi chú |
|-----|--------------|---------------|-------|---------|---------|-------------------------------|-----------|-----------|----------------|---------|
| 1 | [Tên NCC] | [MST] | [Số] | | DD/MM | | 10% | | CK/TM | |

**Tổng hợp Đầu vào theo Thuế suất:**
| Thuế suất | Giá trị mua vào | Thuế đầu vào | Được khấu trừ |
|----------|----------------|-------------|--------------|
| 5% | | | |
| 8% | | | |
| 10% | | | |
| **Tổng** | | | |

#### 3.2 Điều kiện Khấu trừ Thuế Đầu vào
Với mỗi hóa đơn đầu vào, kiểm tra:
- [ ] Hóa đơn hợp pháp: có đầy đủ thông tin, không tẩy xóa
- [ ] MST người bán hợp lệ (kiểm tra trên Cổng thông tin thuế)
- [ ] Hóa đơn liên quan đến HĐKD của doanh nghiệp (không phải chi tiêu cá nhân)
- [ ] Thanh toán qua ngân hàng (nếu giá trị >20 triệu VND/lần)
- [ ] Hóa đơn điện tử: đã được cơ quan thuế chấp nhận (trạng thái hợp lệ)
- [ ] Không phải hóa đơn giả, hóa đơn của doanh nghiệp bỏ trốn

#### 3.3 Hóa đơn KHÔNG được Khấu trừ
- HĐ không có chữ ký điện tử hợp lệ (đối với HĐĐT)
- HĐ của doanh nghiệp đã bị cơ quan thuế thông báo không còn giá trị
- HĐ thanh toán bằng tiền mặt >20 triệu VND
- HĐ không liên quan đến hoạt động kinh doanh chịu thuế
- HĐ mua hàng hóa/dịch vụ để cho tặng (không vì mục đích KD)

### Phần 4: Tổng hợp Tờ khai VAT (Mẫu 01/GTGT)

#### 4.1 Bảng Tổng hợp Kỳ khai

| Chỉ tiêu | Mã chỉ tiêu | Số tiền |
|---------|------------|---------|
| Tổng doanh thu hàng hóa DV bán ra | [31] | |
| Tổng thuế GTGT đầu ra | [32] | |
| Tổng giá trị HHDV mua vào | [23] | |
| Tổng thuế GTGT đầu vào | [24] | |
| Thuế GTGT đầu vào đủ điều kiện khấu trừ | [25] | |
| Thuế GTGT còn được khấu trừ kỳ trước | [22] | |
| **Thuế GTGT phải nộp ([32]-[25]-[22])** | **[40]** | |
| Hoặc: Thuế GTGT còn được khấu trừ | [43] | |

#### 4.2 Quy trình Nộp Tờ khai
1. Hoàn thiện bảng kê đầu vào và đầu ra
2. Import dữ liệu vào phần mềm HTKK hoặc eTax
3. Điền thông tin vào mẫu 01/GTGT
4. Kiểm tra cross-check: chỉ tiêu [32] = tổng bảng kê đầu ra, [24] = tổng bảng kê đầu vào
5. Ký số và nộp trên cổng thuế điện tử
6. Lưu biên bản tiếp nhận tờ khai
7. Nộp tiền thuế (nếu [40] > 0): nộp trước ngày 20 hoặc ngày cuối kỳ gia hạn

### Phần 5: Xử lý Tình huống Đặc biệt

#### 5.1 Hóa đơn Điều chỉnh/Thay thế
- HĐ điều chỉnh: ghi nhận chênh lệch (dương hoặc âm) trong kỳ phát sinh HĐ điều chỉnh
- HĐ thay thế: xóa HĐ gốc, ghi nhận HĐ mới trong cùng kỳ hoặc kỳ phát sinh

#### 5.2 Hàng hóa/Dịch vụ Vừa chịu Thuế Vừa không chịu Thuế
- Phân bổ thuế đầu vào theo tỷ lệ doanh thu chịu thuế / tổng doanh thu
- Lưu tài liệu tính toán phân bổ

#### 5.3 Thuế GTGT Hoàn lại
- Điều kiện hoàn thuế: số thuế khấu trừ liên tiếp 12 tháng âm, hoặc xuất khẩu...
- Quy trình nộp hồ sơ hoàn thuế lên cơ quan thuế
- Chuẩn bị hồ sơ: tờ khai, bảng kê, chứng từ thanh toán, hợp đồng, vận đơn...

### Phần 6: Lịch Nghĩa vụ Thuế VAT Hàng Tháng/Quý
| Kỳ | Deadline Nộp tờ khai | Deadline Nộp tiền | Lưu ý |
|----|--------------------|-----------------|-------|
| Tháng 1 | 20/2 | 20/2 | |
| Tháng 2 | 20/3 | 20/3 | |
| [Tiếp tục...] | | | |
| Quý 1 (nếu khai quý) | 30/4 | 30/4 | |

## Định dạng & Lưu trữ
- Format: .xlsx (bảng kê Excel) + file HTKK (nộp thuế điện tử)
- Đặt tên: [TAX/YYYY-MM] FIN-015 - Bang Ke Thue GTGT [Thang/Quy] - KeToan v[X.X]
- Thư mục lưu: 02-Tai-Chinh/08-Thue/GTGT/[YYYY]/
- Lưu trữ tối thiểu 10 năm (theo Luật Kế toán và Luật Quản lý Thuế)

## Hướng dẫn cho Claude
1. Luôn kiểm tra cross-check giữa bảng kê và sổ kế toán trước khi nộp - sai lệch là dấu hiệu có lỗi.
2. Điều kiện khấu trừ thanh toán qua ngân hàng >20 triệu là quy định rất hay bị vi phạm.
3. Kiểm tra MST người bán trên Cổng thông tin điện tử của Tổng cục Thuế trước khi khấu trừ.
4. Hóa đơn của doanh nghiệp bỏ trốn/mất tích: không được khấu trừ dù đã trả tiền.
5. Xuất dữ liệu từ phần mềm hóa đơn điện tử để giảm thiểu nhập liệu thủ công và sai sót.
6. Deadline 20 hàng tháng là cứng - nộp trễ bị phạt, đừng để đến sát ngày mới làm.
7. Lưu trữ đầy đủ: tờ khai + bảng kê + chứng từ thanh toán + hợp đồng (bộ hồ sơ hoàn chỉnh cho kiểm tra thuế).
