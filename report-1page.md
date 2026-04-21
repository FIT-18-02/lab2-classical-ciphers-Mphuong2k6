# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Tìm hiểu và triển khai hai thuật toán mã hóa cổ điển: Caesar Cipher (thay thế) và Rail Fence Cipher (hoán vị). Mục tiêu chính bao gồm việc xử lý đa dạng kiểu dữ liệu (chữ hoa, chữ thường, dấu cách), quản lý lỗi đầu vào và thao tác đọc dữ liệu từ tệp tin hệ thống.

## 2. Cách làm
- Hoàn thiện Caesar Cipher cho chữ thường, dấu cách và giải mã.
- Hoàn thiện Rail Fence Cipher cho giải mã, giữ dấu cách, kiểm tra đầu vào và đọc file.
- Chạy thử trên nhiều test case.

## 3. Kết quả chính
### 3.1 Caesar Cipher
| Input | Key | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 3 | L ORYH BRX | Mã hóa đúng, giữ nguyên dấu cách. |
| hello world | 5 | mjqqt btwqi | Hỗ trợ tốt chữ thường. |
| LORYH BRX | 3 | I LOVE YOU | Giải mã chính xác về bản rõ gốc. |

### 3.2 Rail Fence Cipher
| Input | Rails | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 2 | ILV OUI OE Y | Mã hóa 2 hàng, giữ khoảng cách. |
| I LOVE YOU | 4 | I ULOE Y OV | Cấu trúc zigzag phức tạp hơn, vẫn chính xác. |
| IOEOLVYU | 2 | I LOVE YOU | Giải mã thành công từ bản mã hoán vị. |

### 3.3 Input validation / file input
- Trường hợp đầu vào không hợp lệ: Khi nhập Key là chuỗi (ví dụ: "abc") hoặc số âm, chương trình hiển thị thông báo: "Error: Key must be a positive integer".
- Kết quả đọc từ `data/input.txt`:Chương trình tự động tải thông điệp từ file, thực hiện mã hóa và xuất kết quả ra màn hình mà không cần nhập tay.

## 4. Kết luận
Học được: Hiểu rõ sự khác biệt giữa mã hóa thay thế (Caesar) và mã hóa hoán vị (Rail Fence). Biết cách quản lý luồng dữ liệu thông qua file.

Khó khăn nhất: Việc lập chỉ mục (indexing) để vẽ lại ma trận zigzag trong thuật toán Rail Fence khi giải mã, đặc biệt là khi phải giữ nguyên vị trí các dấu cách.

Điều giúp hiểu rõ hơn: Việc vẽ tay ma trận đường ray trên giấy trước khi code giúp em hình dung được quy luật di chuyển của các ký tự, từ đó chuyển đổi sang vòng lặp for trong lập trình dễ dàng hơn.
