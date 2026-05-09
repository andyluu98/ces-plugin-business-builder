# SOP Quản Lý Kho và Tồn Kho | ces-operations

## Mục đích & Phạm vi
Tài liệu này thiết lập quy trình chuẩn cho mọi hoạt động liên quan đến kho hàng, từ nhập kho, xuất kho, kiểm kê đến tối ưu tồn kho, đảm bảo hàng hóa được bảo quản đúng cách, dữ liệu tồn kho chính xác và tránh tình trạng thiếu hàng hoặc hàng tồn quá mức. Áp dụng cho bộ phận Kho và tất cả các bên có nhu cầu nhập/xuất hàng.

## Câu hỏi thu thập thông tin
1. Doanh nghiệp có bao nhiêu kho? Mỗi kho lưu trữ loại hàng gì?
2. Số lượng mặt hàng (SKU) đang quản lý là bao nhiêu?
3. Hệ thống quản lý kho hiện tại: thủ công, Excel hay phần mềm WMS?
4. Điều kiện bảo quản đặc biệt nào cần thiết (nhiệt độ, độ ẩm, ánh sáng)?
5. Tần suất kiểm kê kho: hàng ngày, hàng tuần hay hàng tháng?
6. Mức tồn kho tối thiểu (safety stock) và điểm đặt hàng lại (reorder point) đã xác định chưa?
7. Quy trình xử lý hàng hết hạn, hàng hỏng hoặc hàng chậm luân chuyển?

## Cấu trúc tài liệu

### Phần 1: Nguyên tắc quản lý kho
- FIFO (First In First Out): Hàng nhập trước xuất trước — bắt buộc với hàng có hạn sử dụng
- FEFO (First Expired First Out): Hàng hết hạn sớm nhất xuất trước — áp dụng với thực phẩm, dược phẩm
- Phân loại ABC: A (20% SKU — 80% giá trị) cần kiểm soát chặt nhất
- Nguyên tắc rõ ràng: Mỗi vị trí kho có địa chỉ rõ ràng (kệ, hàng, ô)

### Phần 2: Quy trình nhập kho

**Bước 1: Chuẩn bị nhận hàng**
- Xem xét PO và lịch giao hàng dự kiến
- Chuẩn bị không gian nhận hàng, thiết bị kiểm đếm

**Bước 2: Kiểm tra khi giao hàng**
- Kiểm tra phương tiện vận chuyển và điều kiện bảo quản
- Đối chiếu số lượng thực tế với Packing List / Vận đơn
- Kiểm tra chất lượng mẫu đại diện: ngoại quan, nhãn mác, hạn sử dụng
- Ghi nhận sai lệch (nếu có) vào Biên bản giao nhận

**Bước 3: Xử lý hàng sau kiểm tra**
- Hàng đạt: Lập Phiếu nhập kho, nhập hệ thống, sắp xếp vào vị trí kho
- Hàng không đạt: Cách ly khu vực Quarantine, thông báo Bộ phận Mua hàng xử lý với NCC
- Dán nhãn vị trí và cập nhật sơ đồ kho

**Bước 4: Cập nhật hệ thống**
- Nhập Phiếu nhập kho vào phần mềm/Excel ngay trong ngày nhận hàng
- Cập nhật số tồn kho thực tế
- Lưu hồ sơ: PO + Packing List + Phiếu nhập kho + Phiếu kiểm tra chất lượng

### Phần 3: Quy trình xuất kho

**Bước 1: Tiếp nhận yêu cầu xuất kho**
- Nhận Phiếu yêu cầu xuất kho / Lệnh xuất hàng từ bộ phận yêu cầu
- Kiểm tra: Có đủ tồn kho không? Người yêu cầu có thẩm quyền không?

**Bước 2: Chuẩn bị hàng xuất**
- Chọn hàng theo nguyên tắc FIFO/FEFO
- Kiểm tra chất lượng hàng trước khi xuất
- Đóng gói, dán nhãn theo yêu cầu

**Bước 3: Bàn giao và ghi nhận**
- Bàn giao cho người nhận / đơn vị vận chuyển, ký xác nhận
- Lập Phiếu xuất kho
- Cập nhật hệ thống ngay sau khi xuất hàng

### Phần 4: Kiểm kê kho định kỳ

**Kiểm kê toàn phần (Annual Physical Inventory):**
- Tần suất: 1-2 lần/năm (thường cuối năm tài chính)
- Dừng nhập/xuất kho trong thời gian kiểm kê
- Đội kiểm kê gồm: Kho + Kế toán + Đại diện BGĐ
- So sánh tồn kho thực tế với sổ sách, lập Biên bản chênh lệch

**Kiểm kê xoay vòng (Cycle Count):**
- Kiểm kê 1 phần kho hàng tuần / hàng tháng
- Ưu tiên nhóm hàng A và hàng sắp hết hạn
- Không cần dừng hoạt động kho
- Phát hiện sai lệch sớm để điều chỉnh kịp thời

### Phần 5: Quản lý mức tồn kho tối ưu
- **Safety Stock (Tồn kho an toàn):** Tính theo: Lead time × Nhu cầu trung bình ngày
- **Reorder Point (Điểm đặt hàng lại):** Safety Stock + (Lead time × Nhu cầu trung bình)
- **Economic Order Quantity (EOQ):** Lượng đặt hàng tối ưu giảm thiểu tổng chi phí
- Theo dõi tồn kho hàng ngày và cảnh báo khi đến điểm đặt hàng

### Phần 6: Xử lý hàng tồn đặc biệt
- Hàng hết hạn: Cách ly, báo cáo, tiêu hủy có biên bản theo quy định
- Hàng chậm luân chuyển (>6 tháng): Báo cáo tháng, đề xuất xử lý (giảm giá, trả NCC, thanh lý)
- Hàng bị hỏng/mất: Điều tra nguyên nhân, lập biên bản, hạch toán chi phí
- Hàng nguy hiểm: Tuân thủ quy định an toàn đặc thù

### Phần 7: KPI quản lý kho
| KPI | Mục tiêu | Tần suất đo |
|-----|----------|------------|
| Độ chính xác tồn kho | ≥99% | Hàng tháng |
| Tỷ lệ giao hàng đúng hạn | ≥98% | Hàng tuần |
| Tỷ lệ hàng hết hạn / hỏng | ≤0.5% | Hàng tháng |
| Vòng quay tồn kho | ≥X lần/năm | Hàng quý |
| Chi phí lưu kho / doanh thu | ≤X% | Hàng quý |

## Định dạng & Lưu trữ
- Format: .docx
- Đặt tên: [OPS-SOP-08] Quản lý kho và tồn kho - Vận hành v1.0
- Thư mục: 03 Hành chính & Vận hành / SOP / Kho
- Xem xét: 6 tháng/lần

## Lưu ý tuân thủ pháp lý
- Hàng hóa có hạn sử dụng phải kiểm soát theo FEFO nghiêm ngặt
- Tiêu hủy hàng hết hạn phải lập biên bản và thông báo cơ quan thuế nếu hạch toán chi phí
- Kho lưu trữ thực phẩm, hóa chất, thuốc cần tuân thủ quy định an toàn ngành đặc thù

## Hướng dẫn cho Claude
1. Hỏi về loại hàng hóa và quy mô kho để đề xuất cấu trúc phù hợp
2. Tạo sơ đồ bố trí kho mẫu theo nguyên tắc phân vùng ABC
3. Đề xuất phần mềm WMS phù hợp: từ Excel đến Odoo, SAP WM, hoặc phần mềm Việt
4. Tạo template Phiếu nhập kho và Phiếu xuất kho chuẩn
5. Hướng dẫn cách tính Safety Stock và Reorder Point với số liệu cụ thể
6. Đề xuất layout kho tối ưu theo nguyên tắc "hàng bán chạy gần cửa xuất"
