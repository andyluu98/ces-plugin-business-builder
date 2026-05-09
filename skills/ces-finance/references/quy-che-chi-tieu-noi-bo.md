# Quy chế Chi tiêu Nội bộ (Phân cấp Phê duyệt) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude xây dựng Quy chế Chi tiêu Nội bộ toàn diện, xác định rõ ràng phân cấp thẩm quyền phê duyệt chi tiêu theo từng loại và mức giá trị. Quy chế giúp kiểm soát chi phí hiệu quả, giảm thiểu rủi ro gian lận, đẩy nhanh tốc độ ra quyết định và đảm bảo trách nhiệm giải trình rõ ràng. Phù hợp cho doanh nghiệp từ 15 nhân sự trở lên, cần hệ thống phê duyệt chi tiêu bài bản thay thế quy trình "hỏi sếp" không chính thức.

## Câu hỏi thu thập thông tin
1. Cơ cấu tổ chức hiện tại: các cấp quản lý gồm những chức danh nào? (Nhân viên, Trưởng nhóm, Trưởng phòng, GĐ, CEO...)
2. Các loại chi tiêu phổ biến nhất trong doanh nghiệp là gì? Loại nào chiếm tỷ trọng lớn nhất?
3. Hiện tại quy trình phê duyệt chi tiêu đang diễn ra như thế nào? Vấn đề lớn nhất là gì?
4. Ngưỡng chi tiêu nào bạn muốn CEO phải trực tiếp phê duyệt? Mức độ ủy quyền xuống dưới như thế nào?
5. Có danh mục chi tiêu nào đặc biệt nhạy cảm cần kiểm soát chặt hơn không? (Marketing, tiếp khách, đi lại...)
6. Quy trình thanh toán hiện tại: ai ký phiếu chi, ai ký séc/lệnh chuyển khoản, ai đối soát?
7. Phần mềm quản lý chi tiêu đang dùng là gì? Quy trình có thể chạy trên giấy tờ hay cần hệ thống?

## Cấu trúc tài liệu

### Chương 1: Nguyên tắc Chung
- Mục đích và phạm vi áp dụng của quy chế
- Nguyên tắc "4 mắt" (four-eyes principle): mọi khoản chi đều cần ít nhất 2 người phê duyệt
- Nguyên tắc tách biệt nhiệm vụ: người đề xuất ≠ người phê duyệt ≠ người thực hiện thanh toán
- Nguyên tắc minh bạch: mọi chi tiêu phải có chứng từ hợp lệ
- Cấm chi tiêu cá nhân bằng tiền công ty dưới mọi hình thức

### Chương 2: Phân cấp Thẩm quyền Phê duyệt

#### 2.1 Ma trận Thẩm quyền Tổng quát

| Mức chi tiêu | Cấp phê duyệt 1 | Cấp phê duyệt 2 | Ghi chú |
|-------------|-----------------|-----------------|---------|
| Dưới 2 triệu VND | Trưởng nhóm | - | 1 cấp phê duyệt |
| 2 - 10 triệu VND | Trưởng phòng | - | 1 cấp phê duyệt |
| 10 - 50 triệu VND | Trưởng phòng | CFO/GĐ Tài chính | 2 cấp |
| 50 - 200 triệu VND | CFO | CEO | 2 cấp |
| Trên 200 triệu VND | CEO | Hội đồng QT/Cổ đông | 2 cấp + Hội đồng |
| Đầu tư TSCĐ >500 triệu | CEO | HĐQT bỏ phiếu | Quyết định hội đồng |

*Lưu ý: Ngưỡng trên chỉ là ví dụ mẫu, điều chỉnh theo quy mô thực tế doanh nghiệp*

#### 2.2 Phân cấp theo Loại Chi tiêu Cụ thể

**Chi phí Nhân sự & Phúc lợi**
| Loại chi | Thẩm quyền phê duyệt | Giới hạn |
|----------|----------------------|---------|
| Lương thông thường | Bảng lương đã duyệt | Theo bảng lương |
| Thưởng không định kỳ | CEO | Theo ngân sách |
| Phụ cấp và trợ cấp | Trưởng phòng + CFO | Theo chính sách |
| Chi phí tuyển dụng | Trưởng phòng + CFO | Theo ngân sách |
| Đào tạo cá nhân | Trưởng phòng | Ngân sách phòng |
| Đào tạo toàn công ty | CEO + CFO | Ngân sách năm |

**Chi phí Marketing & Bán hàng**
| Loại chi | Thẩm quyền phê duyệt | Giới hạn |
|----------|----------------------|---------|
| Quảng cáo digital <10tr | Marketing Manager | Ngân sách tháng |
| Quảng cáo >10 triệu | GĐ Marketing + CFO | Ngân sách quý |
| Sự kiện, hội thảo | GĐ Marketing + CEO | Case by case |
| In ấn ấn phẩm | Marketing Manager | Ngân sách tháng |
| Hoa hồng sale | Theo chính sách sale | Chính sách đã duyệt |

**Chi phí Vận hành & Văn phòng**
| Loại chi | Thẩm quyền phê duyệt | Giới hạn |
|----------|----------------------|---------|
| Văn phòng phẩm | Hành chính | <5 triệu/tháng |
| Điện nước, internet | Hành chính | Hóa đơn thực tế |
| Sửa chữa nhỏ | Hành chính + Trưởng phòng | <10 triệu |
| Sửa chữa lớn | CFO + CEO | >10 triệu |
| Thuê văn phòng | CEO | Hợp đồng |

**Chi phí Đi lại & Tiếp khách**
| Loại chi | Thẩm quyền phê duyệt | Giới hạn/Người/Ngày |
|----------|----------------------|---------------------|
| Đi lại nội thành | Trưởng nhóm | [mức cụ thể] |
| Đi lại liên tỉnh | Trưởng phòng | [mức cụ thể] |
| Công tác nước ngoài | CEO | [mức cụ thể] |
| Tiếp khách nội bộ | Trưởng phòng | [mức cụ thể] |
| Tiếp khách bên ngoài | GĐ + CFO | [mức cụ thể] |

**Chi phí Công nghệ & Phần mềm**
| Loại chi | Thẩm quyền phê duyệt | Giới hạn |
|----------|----------------------|---------|
| Phần mềm SaaS <5tr/tháng | IT Manager | Ngân sách IT |
| Phần mềm >5tr/tháng | IT Manager + CFO | Phê duyệt mới |
| Thiết bị IT <20tr | IT Manager | Ngân sách |
| Dự án IT lớn | CFO + CEO | Case by case |

### Chương 3: Quy trình Phê duyệt Chi tiêu

#### 3.1 Quy trình Chuẩn (Standard Process)
```
Bước 1: Người đề xuất điền Phiếu Đề nghị Chi (PĐC)
  → Ghi rõ: mục đích, số tiền, nhà cung cấp, thời hạn cần
  → Đính kèm: báo giá, hợp đồng, hoặc hóa đơn ước tính

Bước 2: Trưởng trực tiếp xem xét và ký phê duyệt cấp 1
  → Kiểm tra: ngân sách còn không, có hợp lý không
  → Ký hoặc từ chối trong vòng 1 ngày làm việc

Bước 3: Chuyển lên cấp phê duyệt tiếp theo (nếu cần)
  → Cấp phê duyệt 2 xem xét và ký trong vòng 2 ngày

Bước 4: Kế toán nhận PĐC đã đủ chữ ký
  → Kiểm tra tính hợp lệ của chứng từ
  → Thực hiện thanh toán theo phương thức đã quy định

Bước 5: Lưu trữ chứng từ gốc
  → Hóa đơn VAT, hợp đồng, biên bản nghiệm thu
```

#### 3.2 Quy trình Khẩn cấp (Emergency Process)
- Điều kiện được xử lý khẩn: tình huống ảnh hưởng trực tiếp đến hoạt động kinh doanh
- Phê duyệt bằng email/điện thoại trong giờ làm việc với điều kiện bổ sung PĐC ngay sau đó
- Phê duyệt bằng email/Zalo ngoài giờ: CEO hoặc người được ủy quyền, hoàn thiện chứng từ trong 24 giờ

#### 3.3 Ủy quyền Phê duyệt Tạm thời
- Điều kiện ủy quyền: người phê duyệt vắng mặt >2 ngày làm việc
- Quy trình ủy quyền: văn bản ủy quyền có chữ ký, gửi kế toán trước khi vắng mặt
- Phạm vi ủy quyền: chỉ trong mức thẩm quyền và thời gian vắng mặt cụ thể

### Chương 4: Chứng từ và Hóa đơn Hợp lệ
- Loại chứng từ được chấp nhận theo từng loại chi tiêu
- Yêu cầu hóa đơn VAT: điều kiện, thông tin bắt buộc
- Chứng từ thanh toán cho cá nhân: bảng kê, phiếu chi có ký nhận
- Thời hạn nộp chứng từ sau khi chi tiêu: tối đa 5 ngày làm việc
- Xử lý khi mất chứng từ: quy trình và chế tài

### Chương 5: Chế tài Vi phạm
- Chi tiêu không có phê duyệt đúng thẩm quyền
- Chi tiêu vượt ngân sách không có phê duyệt bổ sung
- Nộp chứng từ giả mạo hoặc không hợp lệ
- Mức chế tài theo từng mức độ vi phạm: cảnh cáo, khấu trừ lương, thôi việc, truy cứu pháp lý

## Định dạng & Lưu trữ
- Format: .docx (quy chế chính) + .xlsx (ma trận thẩm quyền để tra cứu nhanh)
- Đặt tên: [POLICY/YYYY] FIN-002 - Quy Che Chi Tieu Noi Bo - BGD v[X.X]
- Thư mục lưu: 02-Tai-Chinh/01-Chinh-Sach-Tai-Chinh/
- In và dán bảng tóm tắt ma trận phê duyệt tại bàn kế toán và trên intranet

## Hướng dẫn cho Claude
1. Ma trận phân cấp thẩm quyền là trái tim của tài liệu - phải rõ ràng, không có vùng xám.
2. Điều chỉnh ngưỡng phê duyệt theo quy mô thực tế: mức 200 triệu với startup 5 tỷ doanh thu là khác với doanh nghiệp 200 tỷ.
3. Quy trình khẩn cấp phải tồn tại và hợp lý - nếu không, mọi thứ đều được gọi là "khẩn cấp".
4. Mỗi loại chi tiêu phải rõ ai phê duyệt, không để tình trạng "hỏi thêm".
5. Phần chế tài phải cụ thể và đã được HR review - chế tài mơ hồ thì không ai sợ.
6. Cung cấp template Phiếu Đề nghị Chi kèm theo để hoàn chỉnh hệ thống.
7. Pilot test với 1-2 phòng ban trước khi roll out toàn công ty.
