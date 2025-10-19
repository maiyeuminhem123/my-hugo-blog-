---
title: "Kiểu dữ liệu trong JavaScript và ép kiểu"
date: 2025-10-17
categories: ["JavaScript"]
featured: "/images/featured-7.svg"
image: "/images/featured-7.svg"
---

## Các kiểu dữ liệu cơ bản trong JavaScript

JavaScript có 7 kiểu dữ liệu cơ bản:
- Number (Số)
- String (Chuỗi)
- Boolean (Đúng/Sai)
- Null (Rỗng)
- Undefined (Chưa xác định)
- Symbol (Ký hiệu, ES6)
- BigInt (Số lớn, ES2020)

### Ví dụ khai báo:
```javascript
let age = 20; // Number
let name = "An"; // String
let isStudent = true; // Boolean
let x = null; // Null
let y; // Undefined
let id = Symbol("id"); // Symbol
let big = 12345678901234567890n; // BigInt
```

> JavaScript rất linh hoạt về kiểu dữ liệu, hãy chú ý khi sử dụng!
### Lưu ý khi làm việc với kiểu dữ liệu
- Ep kiểu (type coercion): JavaScript tự động chuyển đổi kiểu trong nhiều trường hợp, có thể gây lỗi.
- So sánh: dùng `===` và `!==` để tránh ép kiểu không mong muốn.

### Ví dụ về ép kiểu
```javascript
console.log('5' - 2); // 3 (string được ép thành number)
console.log('5' + 2); // '52' (phép cộng nối chuỗi)
```

### Kết luận
Hiểu rõ cách ép kiểu và so sánh trong JavaScript giúp tránh lỗi logic.
