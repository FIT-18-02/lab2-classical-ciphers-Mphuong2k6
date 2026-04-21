# Test Cases – FIT4012 Lab 2

## Caesar Cipher
- [x] Encrypt `I LOVE YOU` với key `3`
 → Output: `L OVEH BRX`
- [x] Encrypt `hello world` với key `5`
  → Output: `mjqqt btwqi`
- [x] Decrypt `LORYH BRX` với key `3`
  → Output: `I LOVE YOU`

## Rail Fence Cipher
- [x] Encrypt `I LOVE YOU` với `2` rails
    → Output: `IOEOLVYU`
- [x] Encrypt `I LOVE YOU` với `4` rails
  → Output: `IYLOEUOV`  
- [x] Decrypt một bản mã Rail Fence hợp lệ
  → Output: `ILOVEYOU`

## Validation / File input
Validation / File input
- [x] Kiểm tra đầu vào không hợp lệ  
  Input: `HELLO123`  
  → Output: `Invalid input`

- [ ] Đọc thông điệp từ `data/input.txt`
  Input file: `HELLO WORLD`  
  → Output: `MJQQT BTWQI`
