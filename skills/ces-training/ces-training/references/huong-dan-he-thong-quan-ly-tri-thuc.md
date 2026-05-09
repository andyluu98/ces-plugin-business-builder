# Hướng Dẫn Xây Dựng Hệ Thống Quản Lý Tri Thức | ces-training

## Mục đích & Phạm vi
Tài liệu này hướng dẫn doanh nghiệp xây dựng hệ thống quản lý tri thức (Knowledge Management System – KMS) để thu thập, lưu trữ, tổ chức và chia sẻ kiến thức trong tổ chức một cách có hệ thống. KMS giúp tránh "brain drain" khi nhân viên nghỉ việc, giảm lãng phí khi phải giải quyết lại vấn đề đã có giải pháp, và tăng tốc độ học tập của nhân viên mới.

## Câu hỏi thu thập thông tin
1. Kiến thức quan trọng nhất của doanh nghiệp hiện đang nằm ở đâu (trong đầu người, trong email, trong file tản mác)?
2. Điều gì xảy ra khi một nhân viên key người nghỉ việc? Tri thức của họ có được lưu lại không?
3. Nhân viên mới mất bao lâu để tìm thấy thông tin họ cần? Họ thường hỏi ai?
4. Doanh nghiệp đã có hệ thống/công cụ nào để chia sẻ kiến thức chưa (wiki, intranet, Google Site, Notion)?
5. Ai sẽ chịu trách nhiệm xây dựng và duy trì KMS (HR, IT, hay từng phòng ban)?
6. Văn hóa chia sẻ kiến thức hiện tại như thế nào — nhân viên có tự nguyện chia sẻ không?
7. Ngân sách cho KMS là bao nhiêu (công cụ, thời gian nhân sự)?

## Cấu trúc tài liệu

### Phần 1: Khung quản lý tri thức

**1.1 Phân loại tri thức**
- **Explicit Knowledge (Tri thức hiện)**:  Có thể tài liệu hóa — quy trình, hướng dẫn, báo cáo, case study
- **Tacit Knowledge (Tri thức ẩn)**: Trong đầu người — kinh nghiệm, kỹ năng, trực giác → cần "khai thác" qua phỏng vấn, job shadowing

**1.2 Vòng đời tri thức**
```
Thu thập → Tổ chức → Lưu trữ → Chia sẻ → Áp dụng → Cập nhật
```

**1.3 KMS Framework cho doanh nghiệp SME**
- Không cần hệ thống phức tạp — Notion, Confluence, Google Sites đều có thể làm được
- Quan trọng: Cấu trúc rõ ràng + Người duy trì + Văn hóa đóng góp

### Phần 2: Kiến trúc thư viện tri thức

**Cấu trúc thư mục tri thức đề xuất:**
```
Knowledge Base/
├── 01. Công ty & Văn hóa
│   ├── Lịch sử, tầm nhìn, giá trị
│   ├── Cơ cấu tổ chức
│   └── Chính sách nội bộ
├── 02. Sản phẩm & Dịch vụ
│   ├── Mô tả sản phẩm
│   ├── FAQ khách hàng
│   └── Competitive intelligence
├── 03. Quy trình & SOP
│   ├── Theo phòng ban
│   └── Cross-functional
├── 04. Học liệu & Đào tạo
│   ├── Tài liệu onboarding
│   ├── Khóa học nội bộ
│   └── Best practices
├── 05. Case Studies & Bài học kinh nghiệm
│   ├── Dự án thành công
│   ├── Thất bại và bài học
│   └── Giải pháp vấn đề thường gặp
└── 06. Tài nguyên theo phòng ban
    ├── Kinh doanh
    ├── Marketing
    ├── Vận hành
    └── ...
```

### Phần 3: Quy trình thu thập và tài liệu hóa tri thức

**3.1 Thu thập tri thức thường xuyên**
- After Action Review (AAR) sau mỗi dự án lớn
- Exit Interview tri thức khi nhân viên nghỉ việc
- Weekly Lessons Learned (5 phút trong họp nhóm)
- Template ghi nhận best practice

**3.2 Format tài liệu tri thức chuẩn**
- Tiêu đề rõ ràng, có thể tìm kiếm
- Ngữ cảnh: Vấn đề/Tình huống ban đầu
- Giải pháp hoặc kiến thức quan trọng
- Kết quả đạt được
- Tag/Keyword để tìm kiếm
- Tác giả và ngày tạo
- Lần review tiếp theo

**3.3 Phỏng vấn tri thức (Knowledge Elicitation)**
- Dùng khi nhân viên quan trọng sắp nghỉ việc hoặc chuyển vai trò
- Câu hỏi mẫu:
  - "3 điều quan trọng nhất ai kế nhiệm bạn cần biết là gì?"
  - "Vấn đề nào thường xuyên xảy ra và bạn giải quyết như thế nào?"
  - "Những mối quan hệ nào quan trọng nhất cần duy trì?"

### Phần 4: Hệ thống tìm kiếm và phân loại
- Tag taxonomy (hệ thống nhãn/thẻ) chuẩn
- Search best practices trong công cụ đã chọn
- Trang chủ KMS: Featured articles, Recent updates, Quick links

### Phần 5: Quản trị và duy trì KMS

**Knowledge Owner cho từng lĩnh vực:**
| Lĩnh vực | Knowledge Owner | Review định kỳ |
|----------|----------------|---------------|
| Quy trình vận hành | Operations Manager | 6 tháng |
| Sản phẩm & Dịch vụ | Product Manager | 3 tháng |
| Nhân sự & Chính sách | HR Manager | 12 tháng |

**Quy trình cập nhật:**
- Mỗi tác giả chịu trách nhiệm cập nhật bài viết của mình
- Bài viết > 6 tháng không được review → tự động đánh dấu "Cần xem xét"
- Knowledge Manager review tổng thể hàng quý

### Phần 6: Khuyến khích đóng góp tri thức
- Gamification: điểm thưởng cho mỗi bài đóng góp được người khác đánh giá hữu ích
- "Knowledge Contributor of the Month" được vinh danh
- Tích hợp đóng góp KMS vào KPI đào tạo cá nhân

## Định dạng & Lưu trữ
- Format: .docx (hướng dẫn) + Notion/Confluence (platform thực tế)
- Đặt tên: `[GDL/YYYY] HR-TRN-008 - Hướng Dẫn Quản Lý Tri Thức - HR Dept v1.0`
- Thư mục: `08 Đào Tạo / 09 Knowledge Management`
- KMS chính: [link platform được chọn]

## Hướng dẫn cho Claude
1. Hỏi về quy mô doanh nghiệp và công cụ hiện có để đề xuất platform phù hợp (< 20 người: Notion; 20-100: Confluence/Notion; > 100: có thể cần SharePoint hoặc Guru).
2. Nhấn mạnh: công cụ là thứ yếu, văn hóa chia sẻ mới là yếu tố quyết định thành bại của KMS.
3. Giúp thiết kế cấu trúc thư mục đơn giản trước — có thể mở rộng sau, nhưng khó thu gọn.
4. Đề xuất bắt đầu với 1 use case có giá trị ngay: ví dụ FAQ khách hàng hoặc onboarding guide.
5. Gợi ý After Action Review là công cụ đơn giản nhất để bắt đầu thu thập tri thức ngay.
6. Nhắc điều quan trọng nhất: phải có 1 người chịu trách nhiệm (Knowledge Manager) — nếu không ai own, KMS sẽ chết trong vài tháng.
