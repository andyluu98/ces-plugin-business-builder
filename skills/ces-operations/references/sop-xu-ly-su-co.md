# SOP Xử Lý Sự Cố và Gián Đoạn Hoạt Động | ces-operations

## Mục đích & Phạm vi
Tài liệu này cung cấp quy trình chuẩn để phát hiện, phân loại, xử lý và học hỏi từ mọi sự cố ảnh hưởng đến hoạt động kinh doanh, từ sự cố kỹ thuật nhỏ đến gián đoạn hoạt động lớn. Áp dụng cho toàn bộ doanh nghiệp, tất cả loại sự cố: IT, vận hành, chất lượng, nhân sự và thiên tai.

## Câu hỏi thu thập thông tin
1. Loại sự cố nào thường xảy ra nhất trong doanh nghiệp?
2. Ai là người đầu tiên nhận báo cáo sự cố và xác định mức độ ưu tiên?
3. Thời gian phục hồi tối đa chấp nhận được (RTO) cho các hệ thống quan trọng?
4. Có kế hoạch dự phòng (backup plan) cho các quy trình cốt lõi chưa?
5. Doanh nghiệp đã từng trải qua gián đoạn hoạt động nghiêm trọng chưa? Bài học rút ra?
6. Ai có thẩm quyền quyết định leo thang sự cố lên cấp khủng hoảng?
7. Có hợp đồng bảo trì và hỗ trợ khẩn cấp với các nhà cung cấp IT/thiết bị quan trọng không?

## Cấu trúc tài liệu

### Phần 1: Phân loại sự cố theo mức độ nghiêm trọng

| Mức | Tên | Mô tả | Thời gian phản hồi | Thời gian giải quyết |
|-----|-----|-------|-------------------|---------------------|
| P1 | Khủng hoảng | Toàn bộ hoạt động bị dừng, ảnh hưởng khách hàng lớn | 15 phút | 4 giờ |
| P2 | Nghiêm trọng | Một bộ phận/hệ thống quan trọng bị ảnh hưởng | 30 phút | 8 giờ |
| P3 | Trung bình | Suy giảm hiệu suất, có workaround | 2 giờ | 24 giờ |
| P4 | Nhỏ | Ảnh hưởng nhỏ, không cản trở hoạt động chính | 8 giờ | 72 giờ |

### Phần 2: Quy trình xử lý sự cố theo mức độ

**GIAI ĐOẠN 1: Phát hiện và Báo cáo (Tất cả mức độ)**
- Bất kỳ ai phát hiện sự cố → Báo cáo ngay qua kênh được chỉ định
- Kênh báo cáo: Hotline nội bộ / Email / Hệ thống ticket / Chat nhóm khẩn
- Thông tin cần cung cấp: Ai / Cái gì / Khi nào / Ở đâu / Ảnh hưởng thế nào
- Không tự xử lý sự cố P1/P2 mà chưa thông báo — luôn báo cáo trước

**GIAI ĐOẠN 2: Đánh giá và Phân loại**
- Người tiếp nhận đánh giá mức độ (P1/P2/P3/P4) trong 5-15 phút
- Xác nhận phạm vi ảnh hưởng: Hệ thống nào, bộ phận nào, bao nhiêu người dùng
- Ghi nhận sự cố vào hệ thống ticket với mức độ ưu tiên

**GIAI ĐOẠN 3: Kích hoạt ứng phó**

*Sự cố P1 — Kích hoạt Crisis Team:*
- Thông báo ngay: CEO / COO / IT Manager / Trưởng bộ phận liên quan
- Họp khẩn (online hoặc trực tiếp) trong vòng 30 phút
- Phân công rõ: Người xử lý kỹ thuật / Người liên lạc khách hàng / Người quản lý thông tin

*Sự cố P2:*
- Thông báo: Trưởng bộ phận liên quan và IT Manager
- Check-in tiến độ mỗi 30 phút
- Đánh giá cần leo thang lên P1 không

*Sự cố P3/P4:*
- Giao cho team kỹ thuật / vận hành xử lý theo quy trình chuẩn
- Báo cáo tiến độ mỗi 2-4 giờ

**GIAI ĐOẠN 4: Giải pháp tạm thời (Workaround)**
- Xác định ngay workaround để duy trì hoạt động trong khi xử lý gốc rễ
- Thông báo cho người dùng/khách hàng về workaround và ETA giải quyết
- Không bỏ workaround cho đến khi giải quyết triệt để

**GIAI ĐOẠN 5: Giải quyết và Khôi phục**
- Triển khai giải pháp kỹ thuật / vận hành
- Kiểm tra đầy đủ trước khi tuyên bố đã giải quyết
- Khôi phục dịch vụ từng bước, theo dõi sát sau khi phục hồi
- Thông báo cho tất cả các bên khi sự cố được giải quyết hoàn toàn

**GIAI ĐOẠN 6: Phân tích sau sự cố (Post-Incident Review)**
- Thực hiện trong 24-48 giờ sau khi giải quyết P1/P2
- Nội dung: Timeline sự cố / Nguyên nhân gốc rễ / Tác động / Bài học
- Lập kế hoạch hành động phòng ngừa
- Chia sẻ bài học với toàn tổ chức (không quy trách nhiệm cá nhân)

### Phần 3: Kế hoạch kinh doanh liên tục (BCP)

**Xác định quy trình quan trọng:**
| Quy trình | Tác động nếu dừng | RTO | RPO | Phương án dự phòng |
|-----------|------------------|-----|-----|-------------------|
| Đặt hàng KH | Mất doanh thu | 4h | 1h | Nhận đơn qua email/điện thoại |
| Xử lý thanh toán | Không nhận tiền | 8h | 2h | Chuyển khoản thủ công |
| Hệ thống email | Mất liên lạc | 2h | 0 | Zalo/WhatsApp nhóm |
| Website/App | Mất kênh bán hàng | 4h | 1h | Redirect sang landing page dự phòng |

**Kịch bản gián đoạn phổ biến và phương án dự phòng:**
- Mất điện kéo dài: UPS, máy phát điện, làm việc từ xa
- Mất internet: SIM 4G backup, hotspot di động, kết nối qua VPN khác
- Hệ thống IT sập: Backup server, cloud failover, quy trình thủ công
- Nhân viên chủ chốt nghỉ đột xuất: Cross-training, tài liệu quy trình đầy đủ
- Thiên tai / Dịch bệnh: Làm việc từ xa, phân tán địa điểm

### Phần 4: Danh sách liên lạc khẩn cấp
| Vai trò | Tên | SĐT 1 | SĐT 2 | Email | Thời gian liên hệ |
|---------|-----|-------|-------|-------|------------------|
| Crisis Manager (CEO/COO) | ... | ... | ... | ... | 24/7 |
| IT Emergency | ... | ... | ... | ... | 24/7 |
| Trưởng phòng Vận hành | ... | ... | ... | ... | 24/7 |
| Nhà cung cấp IT chính | ... | ... | ... | ... | Giờ hành chính + Hotline |

### Phần 5: Biểu mẫu đính kèm
- F01: Phiếu báo cáo sự cố
- F02: Nhật ký xử lý sự cố (Incident Log)
- F03: Báo cáo phân tích sau sự cố (Post-Incident Report)
- F04: Checklist phục hồi sau sự cố

## Định dạng & Lưu trữ
- Format: .docx
- Đặt tên: [OPS-SOP-09] Xử lý sự cố và gián đoạn - Vận hành v1.0
- Thư mục: 03 Hành chính & Vận hành / SOP / Xử lý sự cố
- Phân phối: Tất cả Trưởng phòng và IT Team — phải biết nằm lòng
- Diễn tập: Ít nhất 1 lần/năm cho kịch bản P1

## Lưu ý tuân thủ pháp lý
- Sự cố liên quan đến rò rỉ dữ liệu cá nhân: Thông báo cơ quan có thẩm quyền trong 72 giờ (Nghị định 13/2023)
- Tai nạn lao động: Báo cáo Sở LĐTBXH trong 24 giờ (Luật ATVSLĐ 2015)
- Sự cố ảnh hưởng đến an toàn thực phẩm: Thông báo cơ quan quản lý ngay lập tức

## Hướng dẫn cho Claude
1. Hỏi về ngành và loại sự cố thường gặp nhất để tùy chỉnh kịch bản phù hợp
2. Xây dựng ma trận tác động x khả năng xảy ra để ưu tiên kế hoạch dự phòng
3. Tạo "Emergency Card" một trang với số điện thoại khẩn cấp và bước xử lý nhanh
4. Đề xuất công cụ quản lý incident: PagerDuty, Jira Service Management, hoặc Google Form đơn giản
5. Nhắc về việc test BCP định kỳ — kế hoạch không test là kế hoạch không hoạt động
6. Tạo checklist post-incident review giúp rút ra bài học có hệ thống
