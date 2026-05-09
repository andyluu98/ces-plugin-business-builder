# Ma trận BCG - Phân tích Danh mục Sản phẩm/Dịch vụ | ces-strategy

## Mục đích & Phạm vi
Template này hướng dẫn Claude thực hiện phân tích ma trận BCG (Boston Consulting Group) để đánh giá danh mục sản phẩm, dịch vụ hoặc đơn vị kinh doanh của doanh nghiệp. Ma trận BCG phân loại theo 2 chiều: tốc độ tăng trưởng thị trường và thị phần tương đối, tạo ra 4 nhóm: Stars, Cash Cows, Question Marks, Dogs. Kết quả giúp lãnh đạo quyết định phân bổ nguồn lực đầu tư, duy trì hay thoái vốn. Phù hợp cho doanh nghiệp có từ 3 sản phẩm/dịch vụ trở lên.

## Câu hỏi thu thập thông tin
1. Liệt kê tất cả sản phẩm, dịch vụ hoặc đơn vị kinh doanh (SBU) cần phân tích. Mỗi đơn vị có doanh thu bao nhiêu?
2. Tốc độ tăng trưởng của từng thị trường (ngành) mà mỗi sản phẩm/SBU đang cạnh tranh là bao nhiêu %/năm?
3. Thị phần của doanh nghiệp và đối thủ dẫn đầu trong từng thị trường? (để tính thị phần tương đối)
4. Mỗi sản phẩm/SBU đóng góp bao nhiêu % lợi nhuận gộp cho doanh nghiệp?
5. Kế hoạch đầu tư hiện tại cho từng sản phẩm/SBU là bao nhiêu so với doanh thu?
6. Doanh nghiệp có sản phẩm/dịch vụ mới nào đang trong giai đoạn phát triển hoặc thử nghiệm?
7. Trong 3 năm tới, bạn muốn danh mục sản phẩm trông như thế nào? Ưu tiên tăng trưởng hay ổn định?

## Cấu trúc tài liệu

### Phần 1: Phương pháp luận BCG
- Giải thích 2 trục: tốc độ tăng trưởng thị trường và thị phần tương đối
- Cách tính thị phần tương đối: thị phần DN / thị phần đối thủ dẫn đầu
- Ngưỡng phân loại: tăng trưởng >10%/năm = thị trường tăng trưởng cao; thị phần tương đối >1 = dẫn đầu
- Ý nghĩa tài chính của từng ô

### Phần 2: Dữ liệu Đầu vào
Bảng dữ liệu cho từng sản phẩm/SBU:
| Sản phẩm/SBU | Doanh thu | Tăng trưởng DT | Tăng trưởng thị trường | Thị phần DN | Thị phần đối thủ đầu | Thị phần tương đối |
|--------------|-----------|----------------|------------------------|-------------|----------------------|-------------------|
| [SP 1]       | ...       | ...%           | ...%                   | ...%        | ...%                 | ...x              |

### Phần 3: Ma trận BCG Trực quan

```
Tốc độ tăng trưởng thị trường
         Cao (>10%)  │  Thấp (<10%)
         ────────────┼────────────
    Cao  │  STARS ★  │ CASH COWS 🐄 │
  (>1x)  │  [Tên SP] │  [Tên SP]   │
─────────│           │             │
    Thấp │ QUESTION  │   DOGS 🐕   │
  (<1x)  │  MARKS ?  │  [Tên SP]   │
         │  [Tên SP] │             │
         └───────────┴─────────────┘
              Thị phần tương đối
```
(Kích thước vòng tròn = doanh thu tương đối)

### Phần 4: Phân tích từng Nhóm

#### Stars (Ngôi sao) - Tăng trưởng cao, Thị phần cao
Các sản phẩm/SBU thuộc nhóm này:
- Tên, doanh thu, thị phần tương đối của từng Stars
- Đặc điểm: tạo ra doanh thu lớn nhưng cũng cần đầu tư nhiều
- Tiềm năng: có thể trở thành Cash Cow khi thị trường bão hòa
- Chiến lược đề xuất: Giữ vững thị phần, đầu tư để duy trì vị thế
- Ngân sách đầu tư đề xuất và kỳ vọng kết quả

#### Cash Cows (Bò sữa) - Tăng trưởng thấp, Thị phần cao
Các sản phẩm/SBU thuộc nhóm này:
- Tên, doanh thu, margin của từng Cash Cow
- Đặc điểm: tạo ra dòng tiền ổn định, chi phí đầu tư thấp
- Vai trò: nguồn tài trợ cho Stars và Question Marks tiềm năng
- Chiến lược đề xuất: Tối ưu hóa hiệu quả, khai thác tối đa dòng tiền
- Cảnh báo: tránh đầu tư quá nhiều, nhưng cũng không bỏ bê

#### Question Marks (Dấu chấm hỏi) - Tăng trưởng cao, Thị phần thấp
Các sản phẩm/SBU thuộc nhóm này:
- Tên, tốc độ tăng trưởng, thị phần hiện tại của từng QM
- Đặc điểm: cần nhiều tiền mặt để tăng thị phần trong thị trường đang lớn
- Phân tích từng QM: nên đầu tư hay thoái vốn?
- Tiêu chí quyết định: lợi thế cạnh tranh, nguồn lực sẵn có, chiến lược dài hạn
- Chiến lược đề xuất: Invest (biến thành Star) hoặc Divest

#### Dogs (Chó) - Tăng trưởng thấp, Thị phần thấp
Các sản phẩm/SBU thuộc nhóm này:
- Tên, doanh thu, margin của từng Dog
- Đặc điểm: ít tiềm năng, tiêu tốn nguồn lực không tương xứng
- Phân tích: có lý do chiến lược nào để giữ lại không? (niềm tin khách hàng, tránh để trống thị trường...)
- Chiến lược đề xuất: Duy trì tối thiểu, Phase out hoặc Sell off

### Phần 5: Chiến lược Phân bổ Nguồn lực
- Bảng phân bổ ngân sách đầu tư theo nhóm BCG
- Nguyên tắc: Cash Cow tài trợ cho Stars và QM tiềm năng
- Lộ trình chuyển đổi: QM nào sẽ đầu tư thành Star? Dog nào sẽ loại bỏ?
- Danh mục mục tiêu 3 năm: tỷ trọng mong muốn giữa 4 nhóm

### Phần 6: Kế hoạch Hành động
- Top 5 quyết định đầu tư/thoái vốn cần thực hiện trong 12 tháng
- KPI theo dõi sự dịch chuyển vị trí của từng SP trên ma trận
- Lịch review BCG matrix: hàng năm hoặc khi có thay đổi lớn

## Định dạng & Lưu trữ
- Format: .docx + hình ảnh ma trận (PNG) + .xlsx (dữ liệu đầu vào)
- Đặt tên: [STANDARD/YYYY] STR-009 - BCG Matrix - BGD v[X.X]
- Thư mục lưu: 01-Chien-Luoc/02-Phan-Tich-Chien-Luoc/

## Hướng dẫn cho Claude
1. Thu thập đủ dữ liệu định lượng: không có số liệu thị phần thực tế thì phân tích BCG mất giá trị.
2. Giúp khách hàng ước tính thị phần nếu không có số liệu chính xác: dùng doanh thu tương đối so với đối thủ.
3. Vẽ ma trận với vòng tròn có kích thước tỷ lệ với doanh thu - điều này giúp trực quan hơn nhiều.
4. Phần phân tích Question Marks là quan trọng nhất - đây là nơi quyết định tương lai danh mục.
5. Tránh đề xuất "giữ tất cả" hoặc "bỏ hết Dogs" - cần phân tích từng trường hợp cụ thể.
6. Kết nối BCG với chiến lược tổng thể: danh mục sản phẩm lý tưởng hỗ trợ tầm nhìn dài hạn như thế nào?
7. Nhắc nhở: BCG chỉ là một công cụ, cần kết hợp với phán đoán kinh doanh thực tế.
