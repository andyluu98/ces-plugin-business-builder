# CES | Luồng Thực Thi 12 Skills Theo Thứ Tự

## Mục đích & Phạm vi
Định nghĩa thứ tự kích hoạt, điều kiện tiên quyết và điều kiện hoàn thành của từng skill trong hệ thống CES Business Builder. Claude dùng file này để điều phối toàn bộ quá trình xây dựng tài liệu doanh nghiệp từ đầu đến cuối.

---

## Câu hỏi xác định luồng phù hợp

1. Doanh nghiệp muốn xây dựng toàn bộ hệ thống hay chỉ một số skill cụ thể?
2. Có skill nào đã hoàn thành một phần chưa (cần tiếp tục thay vì bắt đầu lại)?
3. Có ràng buộc thời gian nào ảnh hưởng đến thứ tự ưu tiên không?
4. Skill nào cần hoàn thành trước một sự kiện quan trọng (kiểm toán, gọi vốn, khai trương...)?

---

## Sơ đồ luồng thực thi

```
[KHỞI ĐỘNG]
     │
     ▼
┌─────────────────────────────────────┐
│  ces-orchestrator (Điều phối)       │
│  - Intake → Scope → Maturity Score  │
│  - Tạo cây thư mục                  │
│  - Xác định lộ trình                │
└──────────────┬──────────────────────┘
               │
               ▼
    ┌─────────────────────┐
    │   TẦNG 1: NỀN TẢNG  │  ← Bắt buộc hoàn thành trước
    └─────────────────────┘
               │
    ┌──────────▼──────────┐
    │   ces-governance    │  Pháp lý, quản trị, hợp đồng
    └──────────┬──────────┘
               │ (Hoàn thành ≥ 70%)
               ▼
    ┌─────────────────────────────────┐
    │       TẦNG 2: QUẢN TRỊ NỘI BỘ  │
    └─────────────────────────────────┘
          │                    │
    ┌─────▼──────┐    ┌────────▼───────┐
    │ ces-finance│    │  ces-people    │
    │ Tài chính  │    │  Nhân sự       │
    └─────┬──────┘    └────────┬───────┘
          │                    │
          └────────┬───────────┘
                   │ (Cả hai ≥ 60%)
                   ▼
    ┌──────────────────────────────────────┐
    │         TẦNG 3: VẬN HÀNH            │
    └──────────────────────────────────────┘
          │              │             │
    ┌─────▼──────┐ ┌─────▼─────┐ ┌────▼──────────┐
    │ces-operations│ │ ces-sales │ │ ces-marketing │
    │  Vận hành  │ │  Bán hàng │ │  Marketing    │
    └─────┬──────┘ └─────┬─────┘ └────┬──────────┘
          │              │             │
          └──────────────┴─────────────┘
                         │ (≥ 1 trong 3 hoàn thành)
                         ▼
    ┌──────────────────────────────────────────┐
    │           TẦNG 4: HỖ TRỢ CHUYÊN BIỆT    │
    └──────────────────────────────────────────┘
          │                        │
    ┌─────▼──────────┐   ┌─────────▼────────┐
    │ ces-customer   │   │ ces-product-tech  │
    │ Khách hàng     │   │ Sản phẩm & CNTT  │
    └─────┬──────────┘   └─────────┬────────┘
          │                        │
          └───────────┬────────────┘
                      │ (Theo nhu cầu)
                      ▼
    ┌──────────────────────────────────────┐
    │         TẦNG 5: PHÁT TRIỂN           │
    └──────────────────────────────────────┘
          │                    │
    ┌─────▼──────┐    ┌────────▼───────┐
    │ces-strategy│    │  ces-growth    │
    │  Chiến lược│    │  Tăng trưởng  │
    └─────┬──────┘    └────────┬───────┘
          │                    │
          └────────┬───────────┘
                   │
                   ▼
    ┌──────────────────────────────────────┐
    │         TẦNG 6: ĐO LƯỜNG & ĐÀO TẠO  │
    └──────────────────────────────────────┘
          │                    │
    ┌─────▼──────────┐ ┌───────▼────────┐
    │ ces-reporting  │ │  ces-training  │
    │  Báo cáo       │ │  Đào tạo       │
    └─────┬──────────┘ └───────┬────────┘
          │                    │
          └────────┬───────────┘
                   │
                   ▼
    ┌──────────────────────────────────────┐
    │   ces-orchestrator: ĐÓNG GÓI         │
    │   Checklist → Bàn giao → Báo cáo    │
    └──────────────────────────────────────┘
```

---

## Chi tiết từng skill

### 1. ces-orchestrator (Điều phối)
- **Vai trò:** Khởi động, điều phối, đóng gói toàn bộ hệ thống
- **Kích hoạt:** Đầu tiên, luôn luôn
- **Đầu vào:** Thông tin doanh nghiệp từ intake
- **Đầu ra:** Hồ sơ DN, điểm trưởng thành, cây thư mục, lộ trình
- **Điều kiện hoàn thành:** Đã intake đầy đủ + lộ trình được phê duyệt

### 2. ces-governance (Quản trị & Pháp lý)
- **Vai trò:** Xây dựng nền tảng pháp lý và quản trị
- **Kích hoạt:** Sau khi ces-orchestrator hoàn thành intake
- **Đầu vào:** Loại hình DN, ngành nghề, cơ cấu cổ đông
- **Đầu ra:** 19 tài liệu pháp lý và quản trị
- **Điều kiện hoàn thành:** Điều lệ + ít nhất 1 loại hợp đồng mẫu + checklist pháp lý

### 3. ces-finance (Tài chính)
- **Vai trò:** Xây dựng hệ thống tài chính và kiểm soát
- **Kích hoạt:** Sau khi ces-governance hoàn thành ≥ 70%
- **Đầu vào:** Loại hình DN, ngành nghề, quy mô doanh thu
- **Đầu ra:** Biểu mẫu tài chính, quy trình kế toán, KPI tài chính
- **Điều kiện hoàn thành:** Bộ báo cáo tài chính + ngân sách mẫu

### 4. ces-people (Nhân sự)
- **Vai trò:** Xây dựng hệ thống quản lý nhân sự
- **Kích hoạt:** Song song với ces-finance (sau governance)
- **Đầu vào:** Quy mô nhân sự, cơ cấu phòng ban, chính sách hiện tại
- **Đầu ra:** Sơ đồ tổ chức, JD, quy trình tuyển dụng, hệ thống đánh giá
- **Điều kiện hoàn thành:** Nội quy LĐ + JD ≥ 3 vị trí chính + quy trình onboarding

### 5. ces-operations (Vận hành)
- **Vai trò:** Chuẩn hóa quy trình vận hành
- **Kích hoạt:** Sau khi ces-people có sơ đồ tổ chức
- **Đầu vào:** Các quy trình chính của DN, công cụ hiện có
- **Đầu ra:** SOP, checklist vận hành, KPI vận hành
- **Điều kiện hoàn thành:** SOP ≥ 3 quy trình chính

### 6. ces-sales (Bán hàng)
- **Vai trò:** Xây dựng hệ thống và quy trình bán hàng
- **Kích hoạt:** Sau khi ces-operations bắt đầu (song song được)
- **Đầu vào:** Sản phẩm/dịch vụ, kênh bán, đội ngũ sales
- **Đầu ra:** Sales playbook, pipeline, script, KPI bán hàng
- **Điều kiện hoàn thành:** Quy trình bán hàng + mẫu báo giá + KPI

### 7. ces-marketing (Marketing)
- **Vai trò:** Xây dựng chiến lược và kế hoạch marketing
- **Kích hoạt:** Song song với ces-sales
- **Đầu vào:** Thương hiệu, thị trường mục tiêu, ngân sách marketing
- **Đầu ra:** Brand guideline, kế hoạch marketing, content plan
- **Điều kiện hoàn thành:** Brand positioning + kế hoạch marketing 6 tháng

### 8. ces-customer (Khách hàng)
- **Vai trò:** Xây dựng hệ thống chăm sóc khách hàng
- **Kích hoạt:** Sau khi ces-sales có quy trình bán hàng
- **Đầu vào:** Hành trình khách hàng, kênh hỗ trợ, chính sách hiện có
- **Đầu ra:** Quy trình CSKH, xử lý khiếu nại, chương trình loyalty
- **Điều kiện hoàn thành:** SOP CSKH + chính sách đổi trả

### 9. ces-product-tech (Sản phẩm & CNTT)
- **Vai trò:** Tài liệu hóa sản phẩm và hệ thống CNTT
- **Kích hoạt:** Theo nhu cầu, thường sau tầng 3
- **Đầu vào:** Danh mục sản phẩm, hệ thống IT hiện có
- **Đầu ra:** Product roadmap, tài liệu kỹ thuật, chính sách bảo mật
- **Điều kiện hoàn thành:** Danh mục sản phẩm + chính sách IT

### 10. ces-strategy (Chiến lược)
- **Vai trò:** Xây dựng tầm nhìn và kế hoạch chiến lược
- **Kích hoạt:** Sau khi tầng 2–3 ổn định
- **Đầu vào:** Mục tiêu dài hạn, thị trường, năng lực cốt lõi
- **Đầu ra:** Vision/Mission/Values, SWOT, chiến lược 3–5 năm
- **Điều kiện hoàn thành:** Tuyên bố tầm nhìn + kế hoạch chiến lược 1 năm

### 11. ces-growth (Tăng trưởng)
- **Vai trò:** Lập kế hoạch mở rộng và tăng trưởng
- **Kích hoạt:** Song song với ces-strategy
- **Đầu vào:** Thị trường tiềm năng, mô hình mở rộng, nguồn vốn
- **Đầu ra:** Growth plan, model mở rộng, pitch deck cơ bản
- **Điều kiện hoàn thành:** Kế hoạch tăng trưởng 12 tháng

### 12. ces-reporting (Báo cáo)
- **Vai trò:** Xây dựng hệ thống báo cáo và KPI tổng hợp
- **Kích hoạt:** Sau khi tất cả các tầng chính hoàn thành
- **Đầu vào:** KPI từ tất cả bộ phận, chu kỳ báo cáo
- **Đầu ra:** Dashboard KPI, mẫu báo cáo định kỳ
- **Điều kiện hoàn thành:** Dashboard tổng hợp + lịch báo cáo

### 13. ces-training (Đào tạo)
- **Vai trò:** Đóng gói tài liệu thành chương trình đào tạo
- **Kích hoạt:** Song song với ces-reporting
- **Đầu vào:** Toàn bộ tài liệu đã tạo, nhu cầu đào tạo
- **Đầu ra:** Chương trình đào tạo, tài liệu onboarding, quiz
- **Điều kiện hoàn thành:** Chương trình đào tạo nhân viên mới

---

## Điều kiện kích hoạt nhanh (Fast Track)

Khi doanh nghiệp có deadline gấp, bỏ qua thứ tự tầng và kích hoạt trực tiếp:

| Tình huống | Skill kích hoạt ngay |
|------------|---------------------|
| Chuẩn bị kiểm toán | ces-governance + ces-finance |
| Tuyển dụng hàng loạt | ces-people |
| Ra mắt sản phẩm mới | ces-marketing + ces-sales |
| Gọi vốn / IPO | ces-governance + ces-finance + ces-strategy |
| Mở chi nhánh | ces-operations + ces-people |
| Xảy ra tranh chấp | ces-governance (hợp đồng) |

---

## Hướng dẫn định dạng output

Khi trình bày lộ trình cho doanh nghiệp:
- Dùng bảng Gantt đơn giản hoặc timeline theo tháng
- Đánh dấu rõ skill nào song song được, skill nào phải tuần tự
- Ghi rõ "Cột mốc hoàn thành" sau mỗi tầng
- Kèm chỉ số đo lường hoàn thành (%) cho từng skill
