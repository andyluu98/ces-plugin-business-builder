# Sổ Đăng ký Rủi ro (Risk Register) | ces-strategy

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng Sổ Đăng ký Rủi ro (Risk Register) - công cụ quản lý rủi ro toàn diện giúp doanh nghiệp nhận diện, đánh giá, ưu tiên hóa và theo dõi mọi rủi ro quan trọng. Risk Register là tài liệu sống, cần cập nhật thường xuyên và là đầu vào quan trọng cho quyết định chiến lược, lập ngân sách và kế hoạch BCP. Phù hợp cho mọi quy mô doanh nghiệp, đặc biệt hữu ích cho SME đang xây dựng hệ thống quản trị rủi ro chuyên nghiệp.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp hoạt động trong ngành nào? Đã từng gặp sự cố hoặc gần gặp sự cố (near-miss) nghiêm trọng nào chưa?
2. Ai là người chịu trách nhiệm quản lý rủi ro hiện tại? Có ủy ban rủi ro hay chỉ do CEO quyết định?
3. Các lĩnh vực hoạt động chính của doanh nghiệp là gì? (Sản xuất, bán hàng, CNTT, tài chính, nhân sự, pháp lý...)
4. Rủi ro nào đang làm bạn lo ngại nhất trong 12 tháng tới? Tại sao?
5. Doanh nghiệp có bảo hiểm rủi ro nào hiện tại không? Phạm vi bao phủ có đầy đủ không?
6. Mức độ chấp nhận rủi ro (risk appetite) của doanh nghiệp như thế nào? Bảo thủ hay chấp nhận rủi ro cao để tăng trưởng?
7. Doanh nghiệp có yêu cầu tuân thủ quy định pháp lý đặc biệt nào không? (ISO, ngành y tế, tài chính, thực phẩm...)

## Cấu trúc tài liệu

### Phần 1: Khung Quản lý Rủi ro

#### 1.1 Chính sách Rủi ro
- Mục tiêu quản lý rủi ro của doanh nghiệp
- Mức độ chấp nhận rủi ro (Risk Appetite Statement)
- Nguyên tắc phân loại và ưu tiên rủi ro
- Vai trò và trách nhiệm: Risk Owner, Risk Manager, Board oversight

#### 1.2 Phương pháp Đánh giá Rủi ro
- Thang đo Xác suất (Likelihood): 1-5
  - 1: Rất thấp (<5% / Hiếm khi)
  - 2: Thấp (5-15% / Đôi khi)
  - 3: Trung bình (15-40% / Thỉnh thoảng)
  - 4: Cao (40-75% / Thường xuyên)
  - 5: Rất cao (>75% / Gần như chắc chắn)
- Thang đo Tác động (Impact): 1-5
  - 1: Không đáng kể (ảnh hưởng tối thiểu)
  - 2: Nhỏ (<5% doanh thu hoặc tác động ngắn hạn)
  - 3: Trung bình (5-15% doanh thu hoặc gián đoạn vài tuần)
  - 4: Nghiêm trọng (15-30% doanh thu hoặc gián đoạn vài tháng)
  - 5: Thảm khốc (>30% doanh thu hoặc đe dọa sự tồn tại)
- Risk Score = Xác suất × Tác động (1-25)
- Ma trận rủi ro 5×5 với màu sắc phân loại

#### 1.3 Ma trận Rủi ro (Heat Map)
```
Tác động
  5 │ ●5  ●10  ●15  ●20  ●25
  4 │ ●4  ●8   ●12  ●16  ●20
  3 │ ●3  ●6   ●9   ●12  ●15
  2 │ ●2  ●4   ●6   ●8   ●10
  1 │ ●1  ●2   ●3   ●4   ●5
    └──────────────────────────
       1    2    3    4    5   Xác suất
       
Xanh (1-4): Chấp nhận  Vàng (5-9): Theo dõi  Cam (10-14): Giảm thiểu  Đỏ (15-25): Ưu tiên cao
```

### Phần 2: Danh mục Rủi ro theo Lĩnh vực

#### Rủi ro Chiến lược
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | Nguyên nhân | Hậu quả |
|----|-------------|----|----|------|-----|-------------|---------|
| S01 | Đối thủ mới gia nhập với giá thấp hơn | 3 | 4 | 12 | Cam | ... | ... |
| S02 | Mất khách hàng lớn | 2 | 5 | 10 | Cam | ... | ... |

#### Rủi ro Vận hành
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| O01 | Sự cố hệ thống IT kéo dài | 3 | 4 | 12 | Cam | |
| O02 | Mất nhân sự chủ chốt | 3 | 4 | 12 | Cam | |
| O03 | Chất lượng sản phẩm không đạt | 2 | 4 | 8 | Vàng | |

#### Rủi ro Tài chính
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| F01 | Thiếu hụt dòng tiền | 3 | 5 | 15 | Đỏ | |
| F02 | Nợ xấu khách hàng | 3 | 3 | 9 | Vàng | |
| F03 | Biến động tỷ giá | 2 | 3 | 6 | Vàng | |

#### Rủi ro Nhân sự
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| H01 | Tỷ lệ nghỉ việc cao | 3 | 3 | 9 | Vàng | |
| H02 | Vi phạm đạo đức nghề nghiệp | 2 | 4 | 8 | Vàng | |

#### Rủi ro Pháp lý & Tuân thủ
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| L01 | Thay đổi quy định ảnh hưởng hoạt động | 2 | 4 | 8 | Vàng | |
| L02 | Tranh chấp hợp đồng | 2 | 3 | 6 | Vàng | |

#### Rủi ro Công nghệ & An ninh mạng
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| T01 | Tấn công mạng / ransomware | 2 | 5 | 10 | Cam | |
| T02 | Rò rỉ dữ liệu khách hàng | 2 | 4 | 8 | Vàng | |

#### Rủi ro Môi trường & Ngoại cảnh
| ID | Mô tả rủi ro | XS | TĐ | Điểm | Mức | ... |
|----|-------------|----|----|------|-----|-----|
| E01 | Thiên tai, dịch bệnh | 1 | 5 | 5 | Vàng | |
| E02 | Biến động kinh tế vĩ mô | 2 | 4 | 8 | Vàng | |

### Phần 3: Kế hoạch Xử lý Rủi ro Chi tiết

Với mỗi rủi ro có điểm ≥ 10 (Cam và Đỏ):

| Trường | Nội dung |
|--------|----------|
| Mã rủi ro | [ID] |
| Mô tả | [Chi tiết] |
| Phương án xử lý | Avoid / Reduce / Transfer / Accept |
| Hành động kiểm soát | [Danh sách hành động cụ thể] |
| Risk Owner | [Tên / Chức vụ] |
| Deadline | [Ngày hoàn thành] |
| Ngân sách | [Ước tính chi phí kiểm soát] |
| KRI - Chỉ báo rủi ro chính | [Chỉ số theo dõi] |
| Ngưỡng cảnh báo | [Giá trị trigger hành động] |
| Rủi ro còn lại sau xử lý | [Điểm rủi ro residual] |
| Tình trạng | Mở / Đang xử lý / Đã giải quyết |

### Phần 4: Dashboard Rủi ro
- Top 10 rủi ro cao nhất hiện tại
- Xu hướng: rủi ro nào đang tăng/giảm so với kỳ trước
- Tóm tắt theo danh mục rủi ro
- Rủi ro mới phát sinh trong kỳ
- Rủi ro đã đóng/giải quyết trong kỳ

### Phần 5: Quy trình Vận hành Risk Register
- Tần suất review: hàng tháng cho rủi ro Đỏ/Cam, hàng quý cho Vàng
- Người chịu trách nhiệm cập nhật từng rủi ro
- Quy trình thêm rủi ro mới: ai có thể đề xuất, ai phê duyệt
- Báo cáo rủi ro cho Ban Giám đốc: tần suất và format
- Tích hợp với quy trình lập kế hoạch và ngân sách

## Định dạng & Lưu trữ
- Format: .xlsx (tracker chính, có conditional formatting màu sắc) + .docx (chính sách và hướng dẫn)
- Đặt tên: [RISK/YYYY-QX] STR-018 - Risk Register - BGD v[X.X]
- Thư mục lưu: 01-Chien-Luoc/07-Quan-Ly-Rui-Ro/
- Cập nhật phiên bản mỗi quý, giữ lịch sử các phiên bản

## Hướng dẫn cho Claude
1. Bắt đầu với brainstorming tất cả rủi ro có thể (không lọc), sau đó mới đánh giá và ưu tiên.
2. Thang điểm xác suất và tác động phải được định nghĩa cụ thể bằng ngưỡng số tiền/% để đánh giá nhất quán.
3. Mỗi rủi ro phải có Risk Owner cụ thể - rủi ro "của tất cả mọi người" là rủi ro không ai quản lý.
4. Phân biệt rõ Inherent Risk (trước kiểm soát) và Residual Risk (sau kiểm soát) - đây là 2 con số khác nhau.
5. KRI (Key Risk Indicators) phải là chỉ số leading (dự báo rủi ro sắp xảy ra), không phải lagging (đã xảy ra rồi).
6. Risk Register phải được review bởi cả leadership team, không chỉ do một người tự điền.
7. Tạo file Excel với conditional formatting tự động tô màu theo mức rủi ro để dễ nhìn và cập nhật.
