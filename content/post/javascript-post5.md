---
title: "Hàm, closure và bất đồng bộ trong JavaScript"
date: 2025-10-17
categories: ["JavaScript"]
featured: "images/featured-9.svg"
image: "images/featured-9.svg"
---

## Hàm trong JavaScript

Hàm (function) là khối mã thực hiện một nhiệm vụ cụ thể, giúp tái sử dụng code.

### Cách khai báo hàm:
```javascript
// Hàm truyền thống
function sayHello(name) {
	return "Hello, " + name + "!";
}

// Hàm mũi tên (arrow function, ES6)
const sum = (a, b) => a + b;
```

### Gọi hàm:
```javascript
console.log(sayHello("An")); // Hello, An!
console.log(sum(2, 3)); // 5
```

> Hàm giúp code gọn gàng, dễ bảo trì và mở rộng.
### Closure và callback
```javascript
function makeCounter() {
	let count = 0;
	return function() { return ++count; };
}

const counter = makeCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

Callback example:
```javascript
function fetchData(callback) {
	setTimeout(() => callback('data'), 500);
}

fetchData((d) => console.log(d));
```

### Kết luận
Hàm là công cụ mạnh trong JavaScript; hiểu closure và callback giúp viết code bất đồng bộ tốt hơn.
