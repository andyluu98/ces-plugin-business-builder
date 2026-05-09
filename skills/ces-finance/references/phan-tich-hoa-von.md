# Phân tích Điểm Hòa vốn (Break-even Analysis) | ces-finance

## Mục đích & Phạm vi
Template này hướng dẫn Claude thực hiện phân tích điểm hòa vốn (Break-even Analysis) toàn diện, xác định mức doanh thu/sản lượng tối thiểu để doanh nghiệp không lỗ. Phân tích bao gồm break-even theo sản lượng, doanh thu và thời gian, đồng thời mở rộng sang phân tích margin of safety và đòn bẩy vận hành. Kết quả giúp lãnh đạo ra quyết định định giá, phân bổ nguồn lực, đánh giá tính khả thi của sản phẩm mới và lên kế hoạch mở rộng. Phù hợp khi ra mắt sản phẩm mới, thay đổi mô hình kinh doanh hoặc đánh giá hiệu quả đầu tư.

## Câu hỏi thu thập thông tin
1. Sản phẩm/dịch vụ cần phân tích break-even là gì? Giá bán hiện tại hoặc dự kiến là bao nhiêu?
2. Chi phí biến đổi (variable cost) trên mỗi đơn vị sản phẩm/giao dịch là bao nhiêu? (Nguyên liệu, nhân công trực tiếp, hoa hồng...)
3. Tổng chi phí cố định hàng tháng cần được bù đắp là bao nhiêu? (Thuê mặt bằng, lương cố định, khấu hao...)
4. Sản lượng/doanh thu hiện tại là bao nhiêu? Công suất tối đa có thể đạt được là bao nhiêu?
5. Doanh nghiệp có nhiều dòng sản phẩm không? Mỗi dòng chiếm bao nhiêu % doanh thu?
6. Mục tiêu lợi nhuận (target profit) mong muốn đạt được là bao nhiêu/tháng hoặc/năm?
7. Kế hoạch thay đổi giá hoặc chi phí nào đang được cân nhắc? Cần phân tích tác động như thế nào?

## Cấu trúc tài liệu

### Phần 1: Cơ sở Lý thuyết và Phương pháp
- Định nghĩa Break-even Point (BEP): điểm doanh thu = tổng chi phí, lợi nhuận = 0
- Công thức cơ bản:
  - BEP (sản lượng) = Fixed Costs / (Price - Variable Cost per unit)
  - BEP (doanh thu) = Fixed Costs / Contribution Margin Ratio
  - Contribution Margin = Price - Variable Cost per unit
  - CM Ratio = Contribution Margin / Price
- Ý nghĩa của từng chỉ số và cách ứng dụng

### Phần 2: Thu thập và Phân loại Dữ liệu

#### 2.1 Bảng Chi phí Cố định Hàng tháng
| Hạng mục | Số tiền (VND) | Ghi chú |
|----------|---------------|---------|
| Tiền thuê mặt bằng | | |
| Lương nhân sự cố định | | |
| BHXH phần công ty | | |
| Khấu hao TSCĐ | | |
| Lãi vay | | |
| Phần mềm & công nghệ | | |
| Bảo hiểm, phí cố định khác | | |
| **Tổng Fixed Costs/tháng** | | |

#### 2.2 Bảng Chi phí Biến đổi trên Mỗi Đơn vị
| Hạng mục | Đơn vị tính | Chi phí/đơn vị | % Giá bán |
|----------|-------------|----------------|-----------|
| Nguyên vật liệu/Hàng hóa | | | |
| Nhân công trực tiếp | | | |
| Hoa hồng bán hàng | | | |
| Chi phí đóng gói, giao hàng | | | |
| Phí cổng thanh toán | | | |
| **Tổng Variable Cost/đơn vị** | | | |

### Phần 3: Tính toán Break-even

#### 3.1 Break-even Đơn sản phẩm

**Thông số cơ bản:**
- Giá bán (P): [X] VND/đơn vị
- Variable Cost (VC): [X] VND/đơn vị
- Contribution Margin (CM): P - VC = [X] VND/đơn vị
- CM Ratio: CM/P = [X]%
- Fixed Costs (FC): [X] VND/tháng

**Kết quả:**
- BEP sản lượng = FC / CM = [X] đơn vị/tháng
- BEP doanh thu = FC / CM Ratio = [X] VND/tháng
- BEP thời gian = BEP doanh thu / Doanh thu trung bình/ngày = [X] ngày/tháng

**Tình trạng hiện tại:**
- Sản lượng thực tế: [X] đơn vị/tháng
- Margin of Safety = (Sản lượng thực - BEP) / Sản lượng thực = [X]%
- Ý nghĩa: Doanh thu có thể giảm [X]% trước khi doanh nghiệp bắt đầu lỗ

#### 3.2 Break-even có Mục tiêu Lợi nhuận
- Target Profit: [X] VND/tháng
- Sản lượng cần thiết = (FC + Target Profit) / CM = [X] đơn vị/tháng
- Doanh thu cần thiết = (FC + Target Profit) / CM Ratio = [X] VND/tháng

#### 3.3 Break-even Đa sản phẩm (Weighted Average)

| Sản phẩm | Giá bán | VC/đơn vị | CM | CM Ratio | % Mix | Weighted CM Ratio |
|----------|---------|------------|-----|----------|-------|-------------------|
| SP A | | | | | 40% | |
| SP B | | | | | 35% | |
| SP C | | | | | 25% | |
| **Tổng** | | | | | 100% | **Weighted Avg** |

- BEP đa sản phẩm (doanh thu) = FC / Weighted Average CM Ratio
- Phân bổ BEP cho từng sản phẩm theo % mix

### Phần 4: Biểu đồ Break-even (Mô tả dạng text)

```
Doanh thu/Chi phí (VND)
       │                        /Doanh thu
       │                       /
       │         Vùng lãi     /
BEP DT─┤- - - - - - - - - -●/- - -
       │                 /  /
       │      Vùng lỗ  /  /Tổng chi phí
FC ────┤──────────────/──/
       │            /  / Chi phí biến đổi
       │           /  /
       └──────────────────────────────
                BEP SL            Sản lượng
```

Mô tả các điểm quan trọng trên biểu đồ:
- Điểm xuất phát chi phí cố định (trục tung = FC)
- Điểm BEP (giao điểm đường doanh thu và đường tổng chi phí)
- Vùng lỗ (bên trái BEP)
- Vùng lãi (bên phải BEP)
- Vị trí hiện tại của doanh nghiệp trên biểu đồ

### Phần 5: Phân tích Nhạy cảm (What-if Analysis)

#### 5.1 Tác động khi Thay đổi Giá bán
| Thay đổi giá | Giá mới | CM mới | BEP mới (SL) | BEP mới (DT) | Thay đổi BEP |
|-------------|---------|--------|--------------|--------------|--------------|
| Giảm 10% | | | | | |
| Giảm 5% | | | | | |
| Hiện tại | | | | | |
| Tăng 5% | | | | | |
| Tăng 10% | | | | | |

#### 5.2 Tác động khi Thay đổi Chi phí Biến đổi
| Thay đổi VC | VC mới | CM mới | BEP mới | Thay đổi |
|------------|--------|--------|---------|---------|

#### 5.3 Tác động khi Thay đổi Chi phí Cố định
| Thay đổi FC | FC mới | BEP mới (SL) | BEP mới (DT) | Thay đổi |
|------------|--------|--------------|--------------|---------|
| Giảm FC 20% (cắt giảm chi phí) | | | | |
| Tăng FC 20% (mở rộng quy mô) | | | | |

### Phần 6: Phân tích Đòn bẩy Vận hành
- Operating Leverage = CM / EBIT
- Ý nghĩa: khi doanh thu tăng 1%, EBIT tăng [X]%
- Rủi ro: đòn bẩy càng cao, biến động lợi nhuận càng lớn khi doanh thu thay đổi
- So sánh đòn bẩy trước và sau khi thay đổi cơ cấu chi phí

### Phần 7: Khuyến nghị và Kế hoạch Hành động
- Đánh giá tình trạng hiện tại: Margin of Safety có đủ an toàn không?
- Khuyến nghị cải thiện break-even:
  - Tăng giá bán (nếu thị trường chấp nhận)
  - Giảm variable cost (đàm phán NCC, tối ưu quy trình)
  - Giảm fixed cost (renegotiate thuê mặt bằng, tự động hóa)
  - Tăng volume để tận dụng operating leverage
- Lộ trình thực hiện và KPI theo dõi

## Định dạng & Lưu trữ
- Format: .xlsx (mô hình tự động tính toán + biểu đồ) + .docx (phân tích và khuyến nghị)
- Đặt tên: [ANALYSIS/YYYY] FIN-006 - Phan Tich Hoa Von - CFO v[X.X]
- Thư mục lưu: 02-Tai-Chinh/03-Phan-Tich-Tai-Chinh/

## Hướng dẫn cho Claude
1. Thu thập dữ liệu chi phí chính xác - phân tích BEP chỉ tốt khi dữ liệu đầu vào chính xác.
2. Giúp khách hàng phân loại chi phí Fixed vs Variable một cách chính xác trước khi tính toán.
3. Với doanh nghiệp đa sản phẩm, phân tích weighted average CM Ratio quan trọng hơn BEP từng sản phẩm.
4. Phần What-if analysis thường có giá trị thực tiễn nhất - đây là nơi CEO tìm câu trả lời cho quyết định.
5. Margin of Safety phải được diễn giải rõ ràng: "Doanh thu có thể giảm X% trước khi bắt đầu lỗ."
6. Xây dựng file Excel tương tác để khách hàng tự thử các kịch bản giá và chi phí khác nhau.
7. Kết nối phân tích BEP với chính sách định giá và kế hoạch ngân sách để tạo giá trị thực tiễn.
