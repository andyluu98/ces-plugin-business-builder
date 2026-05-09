# CES | Lịch Gia Hạn và Theo Dõi Các Loại Giấy Phép

## Mục đích & Phạm vi
Hướng dẫn Claude tạo hệ thống theo dõi và nhắc nhở gia hạn toàn bộ giấy phép, chứng chỉ và nghĩa vụ pháp lý định kỳ của doanh nghiệp. Mục tiêu: không để giấy phép hết hạn mà không được gia hạn kịp thời, tránh rủi ro bị đình chỉ hoạt động hoặc bị xử phạt hành chính.

---

## Câu hỏi thu thập thông tin

1. Liệt kê tất cả giấy phép và chứng chỉ hiện có: tên giấy phép, ngày cấp, ngày hết hạn, cơ quan cấp?
2. Ai hiện đang chịu trách nhiệm theo dõi và gia hạn giấy phép trong doanh nghiệp?
3. Doanh nghiệp muốn được nhắc nhở trước bao lâu khi giấy phép sắp hết hạn (60, 90, hay 180 ngày)?
4. Có giấy phép nào đã hết hạn hoặc sắp hết hạn trong 6 tháng tới không?
5. Hệ thống nhắc nhở muốn dùng: Google Calendar / Excel / phần mềm quản lý / khác?

---

## Outline Hệ Thống Theo Dõi Giấy Phép

### Phần 1: Sổ theo dõi giấy phép tổng hợp (Master License Tracker)

**Cấu trúc bảng theo dõi:**

| Cột | Nội dung | Ví dụ |
|-----|----------|-------|
| Mã GP | Mã định danh nội bộ | GP001 |
| Tên giấy phép / chứng chỉ | Tên đầy đủ | Giấy CN cơ sở đủ điều kiện ATTP |
| Nhóm | Phân loại | Vệ sinh ATTP |
| Cơ quan cấp | Tên cơ quan | Sở Y tế TP. HCM |
| Số giấy phép | Số hiệu chính thức | 12/2022/CNAT-SYT |
| Ngày cấp | DD/MM/YYYY | 15/03/2022 |
| Ngày hết hạn | DD/MM/YYYY | 14/03/2025 |
| Thời hạn hiệu lực | Số năm/tháng | 3 năm |
| Ngày nhắc lần 1 | 180 ngày trước HH | 14/09/2024 |
| Ngày nhắc lần 2 | 90 ngày trước HH | 14/12/2024 |
| Ngày nhắc lần 3 | 30 ngày trước HH | 13/02/2025 |
| Người phụ trách | Tên nhân viên | Nguyễn Thị A |
| Trạng thái | Còn hiệu lực / Sắp hết hạn / Đã hết hạn / Đang gia hạn | Còn hiệu lực |
| Chi phí gia hạn ước tính | VNĐ | 2.000.000 |
| Hồ sơ lưu trữ | Link file scan | [link] |
| Ghi chú | Yêu cầu đặc biệt khi gia hạn | Cần kiểm tra cơ sở trước khi gia hạn |

---

### Phần 2: Lịch gia hạn hàng năm (Annual Renewal Calendar)

**Mẫu lịch theo tháng:**

#### Tháng 1
| Hạng mục | Hạn thực hiện | Phụ trách | Chi phí |
|----------|--------------|-----------|---------|
| Nộp thuế môn bài năm [YYYY] | 30/01 | Kế toán | Theo bậc |
| Gia hạn [tên GP nếu HH tháng 1] | [ngày] | [người] | [số tiền] |

#### Tháng 2
*(Tương tự — điền theo giấy phép thực tế của DN)*

#### Tháng 3
| Hạng mục | Hạn thực hiện | Phụ trách |
|----------|--------------|-----------|
| Quyết toán thuế TNDN năm trước | 31/03 | Kế toán |
| Nộp BCTC năm trước | 31/03 | Kế toán |
| Gia hạn [tên GP] | [ngày] | [người] |

#### Tháng 4
| Hạng mục | Hạn thực hiện |
|----------|--------------|
| ĐHĐCĐ thường niên (nếu là CTCP) | Trước 30/04 |
| Báo cáo lao động 6 tháng đầu năm | Tháng 6 |

*(Tiếp tục cho 12 tháng...)*

---

### Phần 3: Dashboard tình trạng giấy phép

**Bảng tóm tắt theo màu sắc:**

| Màu | Ý nghĩa | Hành động |
|-----|---------|-----------|
| Đỏ | Đã hết hạn (quá hạn) | Xử lý NGAY — nguy cơ bị phạt/đình chỉ |
| Cam | Còn 0–30 ngày | Nộp hồ sơ ngay tuần này |
| Vàng | Còn 31–90 ngày | Chuẩn bị hồ sơ, liên hệ cơ quan |
| Xanh nhạt | Còn 91–180 ngày | Bắt đầu lên kế hoạch |
| Xanh lá | Còn trên 180 ngày | Theo dõi định kỳ |

---

### Phần 4: Quy trình gia hạn chuẩn

**Bước 1 — 180 ngày trước hết hạn:**
- [ ] Xác nhận cơ quan cấp còn hoạt động và thẩm quyền không thay đổi
- [ ] Kiểm tra điều kiện gia hạn có thay đổi so với lần cấp trước
- [ ] Lập danh sách hồ sơ cần chuẩn bị

**Bước 2 — 90 ngày trước hết hạn:**
- [ ] Thu thập và hoàn thiện hồ sơ
- [ ] Kiểm tra điều kiện cơ sở vật chất (nếu cần kiểm tra thực địa)
- [ ] Gia hạn/tái ký hợp đồng liên quan (thuê mặt bằng, dịch vụ...)
- [ ] Ước tính chi phí và lập dự toán

**Bước 3 — 60 ngày trước hết hạn:**
- [ ] Nộp hồ sơ (trực tiếp hoặc trực tuyến)
- [ ] Lưu biên nhận hồ sơ
- [ ] Theo dõi tiến trình xử lý

**Bước 4 — Sau khi được cấp:**
- [ ] Cập nhật Sổ theo dõi giấy phép
- [ ] Scan và lưu bản số hóa
- [ ] Cập nhật lịch nhắc nhở cho kỳ tiếp theo
- [ ] Thông báo cho các bộ phận liên quan

**Bước 5 — Nếu chậm trễ (dưới 30 ngày mà chưa được cấp):**
- [ ] Liên hệ trực tiếp cơ quan cấp để hỏi tiến độ
- [ ] Xem xét tạm dừng hoạt động liên quan nếu cần (tránh rủi ro pháp lý)
- [ ] Báo cáo BGĐ ngay

---

### Phần 5: Hồ sơ gia hạn mẫu theo từng loại giấy phép

*(Claude điền vào phần này sau khi biết danh sách giấy phép thực tế của DN)*

**Mẫu cho Giấy CN ATTP:**
- Đơn đề nghị cấp lại GCN ATTP (theo mẫu)
- Bản sao GCN ĐKKD
- Bản thuyết minh về cơ sở vật chất (có cập nhật so với lần trước)
- Kết quả kiểm nghiệm nước (nếu dùng nước giếng/bể)
- Danh sách nhân viên kèm GCN tập huấn kiến thức ATTP (còn hiệu lực)
- Giấy khám sức khỏe định kỳ của nhân viên trực tiếp sản xuất

**Mẫu cho Giấy phép kinh doanh vận tải:**
- Đơn đề nghị cấp lại
- Bản sao GCN ĐKKD
- Danh sách phương tiện và GCN kiểm định còn hiệu lực
- Hợp đồng lao động với lái xe
- Bằng lái xe của lái xe (còn hiệu lực)
- Hợp đồng bảo hiểm xe

---

### Phần 6: Kế hoạch ngân sách gia hạn hàng năm

| Giấy phép | Năm gia hạn | Chi phí phí nhà nước | Chi phí tư vấn (nếu có) | Tổng dự kiến |
|-----------|-------------|---------------------|------------------------|-------------|
| GP001 | [YYYY] | [X] VNĐ | [X] VNĐ | [X] VNĐ |
| GP002 | [YYYY] | [X] VNĐ | — | [X] VNĐ |
| **Tổng năm [YYYY]** | | | | **[X] VNĐ** |

---

## Hướng dẫn định dạng output

- **Sổ theo dõi tổng hợp:** `00_so-theo-doi-giay-phep-[TenDN-viettat].xlsx`
  - Sheet 1: Tất cả giấy phép (sorted theo ngày hết hạn)
  - Sheet 2: Lịch gia hạn 12 tháng
  - Sheet 3: Dashboard màu sắc
  - Sheet 4: Ngân sách gia hạn
- **Cài đặt nhắc nhở:** Hướng dẫn tạo reminder trong Google Calendar hoặc Outlook kèm theo
- **Cập nhật:** Rà soát toàn bộ sổ 2 lần/năm (tháng 1 và tháng 7)

---

## Lưu ý pháp lý

- Hoạt động sau khi giấy phép hết hạn: bị xử phạt theo Nghị định chuyên ngành (thường 5–50 triệu VNĐ/lần) và đình chỉ hoạt động
- Một số giấy phép: cơ quan có thể thu hồi nếu không gia hạn đúng hạn, phải làm thủ tục cấp mới (phức tạp hơn gia hạn)
- Giấy phép kinh doanh có điều kiện: khi thay đổi địa điểm, quy mô, người phụ trách chuyên môn — phải cập nhật lại giấy phép, không chỉ gia hạn
- Lưu bản gốc giấy phép an toàn và scan lưu số hóa có backup
- Một số ngành: chứng chỉ hành nghề của cá nhân gắn liền với giấy phép DN — nếu người đó nghỉ việc phải tìm người thay thế và cập nhật giấy phép ngay
