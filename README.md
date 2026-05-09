# CES Business Builder Plugin
## Bộ công cụ AI xây dựng tài liệu vận hành doanh nghiệp

Plugin này được phát triển bởi **CES Global**, hỗ trợ doanh nghiệp Việt Nam tạo ra **191 tài liệu vận hành chuẩn hóa** thông qua 13 skills AI chuyên biệt — phù hợp với pháp luật Việt Nam và chuẩn quốc tế ISO 9001:2015, EOS, McKinsey 7S, Lean, Balanced Scorecard.

---

### Thông tin phiên bản

| Trường | Thông tin |
|--------|-----------|
| **Phiên bản** | 1.0.0 |
| **Ngày phát hành** | 05/2026 |
| **Tác giả** | Tuấn Anh — CES Global |
| **Email** | cesglobal.pro@gmail.com |
| **Hotline** | 0911.991.288 |
| **Website** | www.cesglobal.com.vn |

---

### Cấu trúc thư mục plugin

```
plugin/
├── README-plugin.md              ← File này — tổng quan plugin
├── .claude-plugin/
│   └── plugin.json               ← Cấu hình plugin cho Claude
└── skills/
    ├── ces-orchestrator/         ← Tầng 0: Điều phối tổng thể
    ├── ces-governance/           ← Tầng 1: Quản trị & Pháp lý
    ├── ces-strategy/             ← Tầng 1: Chiến lược & Kế hoạch
    ├── ces-finance/              ← Tầng 2: Tài chính & Kế toán
    ├── ces-people/               ← Tầng 2: Nhân sự & Con người
    ├── ces-operations/           ← Tầng 2: Vận hành & Hành chính
    ├── ces-sales/                ← Tầng 3: Kinh doanh & Bán hàng
    ├── ces-marketing/            ← Tầng 3: Marketing & Thương hiệu
    ├── ces-customer/             ← Tầng 3: Khách hàng & Dịch vụ
    ├── ces-product-tech/         ← Tầng 4: Sản phẩm & Công nghệ
    ├── ces-training/             ← Tầng 4: Đào tạo & Phát triển
    ├── ces-reporting/            ← Tầng 4: Báo cáo & Đo lường
    └── ces-growth/               ← Tầng 5: Tăng trưởng & Đầu tư
```

---

### Cách cài đặt nhanh

#### Cách 1 — Claude Desktop (không cần biết lập trình)

1. Mở Claude Desktop → **Settings** → tab **Plugins**
2. Nhấn **"Import Plugin"** → chọn file `plugin/.claude-plugin/plugin.json`
3. Xác nhận cài đặt → Khởi động lại Claude Desktop
4. Kiểm tra: gõ `"Đóng gói doanh nghiệp"` vào chat

#### Cách 2 — Claude Code CLI (dành cho người dùng kỹ thuật)

```powershell
# Windows PowerShell
Copy-Item -Path ".\plugin\skills\*" -Destination "$env:USERPROFILE\.claude\skills\" -Recurse
```

```bash
# macOS / Linux Terminal
cp -r ./plugin/skills/* ~/.claude/skills/
```

Sau đó khởi động Claude Code và gõ `/skills` để xác nhận 13 skills CES đã được nhận diện.

---

### Danh sách 13 Skills CES

| # | Skill | Lĩnh vực | Số TL | Trigger nhanh |
|---|-------|----------|-------|---------------|
| 1 | `ces-orchestrator` | Điều phối tổng thể | 8 | "đóng gói doanh nghiệp" |
| 2 | `ces-governance` | Quản trị & Pháp lý | 19 | "tạo điều lệ công ty" |
| 3 | `ces-strategy` | Chiến lược & Kế hoạch | 18 | "kế hoạch kinh doanh" |
| 4 | `ces-finance` | Tài chính & Kế toán | 20 | "ngân sách / cashflow" |
| 5 | `ces-people` | Nhân sự & Con người | 22 | "sơ đồ tổ chức / nội quy" |
| 6 | `ces-operations` | Vận hành & Hành chính | 20 | "tạo SOP" |
| 7 | `ces-sales` | Kinh doanh & Bán hàng | 17 | "quy trình bán hàng" |
| 8 | `ces-marketing` | Marketing & Thương hiệu | 10 | "kế hoạch marketing" |
| 9 | `ces-customer` | Khách hàng & Dịch vụ | 12 | "chăm sóc khách hàng" |
| 10 | `ces-product-tech` | Sản phẩm & Công nghệ | 13 | "roadmap sản phẩm" |
| 11 | `ces-training` | Đào tạo & Phát triển | 10 | "kế hoạch đào tạo" |
| 12 | `ces-reporting` | Báo cáo & Đo lường | 10 | "từ điển KPI / dashboard" |
| 13 | `ces-growth` | Tăng trưởng & Đầu tư | 12 | "pitch deck / gọi vốn" |
| | **TỔNG** | | **191** | |

---

### Hướng dẫn sử dụng đầy đủ

Xem file: `docs/Huong-Dan-Su-Dung-CES-Business-Builder.md`

---

### Hỗ trợ

- **Website:** www.cesglobal.com.vn
- **Email:** cesglobal.pro@gmail.com
- **Hotline:** 0911.991.288
- **Địa chỉ:** 222 Nguyễn Văn Tuyết, Đống Đa, Hà Nội

*Khi liên hệ hỗ trợ kỹ thuật, vui lòng đặt tiêu đề email: `[CES BB Support] + Mô tả vấn đề`*

---

*CES Global © 2026 — Phiên bản 1.0.0*
