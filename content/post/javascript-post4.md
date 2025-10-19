---
title: "Khai báo biến và scope trong JavaScript"
date: 2025-10-17
categories: ["JavaScript"]
featured: "images/featured-8.svg"
image: "images/featured-8.svg"
---

## Biến và khai báo biến trong JavaScript

Trong JavaScript, biến dùng để lưu trữ dữ liệu. Có 3 cách khai báo biến:

- `var`: Khai báo biến toàn cục hoặc cục bộ, có thể bị hoisting (kéo lên đầu hàm).
- `let`: Khai báo biến trong phạm vi block (ES6), an toàn hơn var.
- `const`: Khai báo hằng số, không thể gán lại giá trị.

### Ví dụ:
```javascript
var x = 10;
let y = 20;
const PI = 3.14;
```

> Nên ưu tiên dùng let và const để code an toàn, dễ bảo trì.
### Lưu ý về scope và hoisting
- `var` có function scope và bị hoisting (biến có thể truy cập trước khi khai báo nhưng giá trị là undefined).
- `let` và `const` có block scope, an toàn hơn khi viết code hiện đại.

### Ví dụ hoisting
```javascript
console.log(x); // undefined
var x = 5;

console.log(y); // ReferenceError
let y = 10;
```

### Kết luận
Dùng `let`/`const` và hiểu scope giúp tránh bug khó tìm.
