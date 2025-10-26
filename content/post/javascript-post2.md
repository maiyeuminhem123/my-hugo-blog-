---
title: "Hello World với JavaScript (Trình duyệt & Node.js)"
date: 2025-10-17
categories: ["JavaScript"]
featured: "images/featured-6.svg"
image: "images/featured-6.svg"
description: "Hướng dẫn chi tiết cách viết chương trình Hello World với JavaScript trên trình duyệt và Node.js, từ cú pháp cơ bản đến các ví dụ nâng cao."
---

## 🚀 Viết chương trình Hello World với JavaScript

Chương trình **Hello World** trong JavaScript rất đơn giản và linh hoạt. Không giống Java, JavaScript không cần biên dịch và có thể chạy trực tiếp trong trình duyệt hoặc trên server với Node.js.

> **💡 Mục tiêu:** Học cách viết và chạy JavaScript trên cả trình duyệt và Node.js

## 🌐 JavaScript trên Trình duyệt

### **Cách 1: Console.log()** (Khuyên dùng để debug)

```javascript
// In ra developer console
console.log("Hello, World!");
console.log("Xin chào JavaScript!");
```

**Cách xem kết quả:**
- Mở trình duyệt (Chrome, Firefox, Edge)
- Nhấn `F12` hoặc `Ctrl+Shift+I` để mở Developer Tools
- Vào tab Console
- Gõ code và thấy kết quả

### **Cách 2: Alert() - Hiển thị popup**

```javascript
alert("Hello, World!");
```

**Ưu điểm:** Dễ thấy, không cần mở console  
**Nhược điểm:** Chặn UI, không tốt cho production

### **Cách 3: Document.write() - Viết lên trang**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello World</title>
</head>
<body>
    <h1>Chương trình Hello World</h1>
    <script>
        document.write("<p>Hello, World! Từ JavaScript</p>");
        document.write("<p>Chào mừng bạn đến với JavaScript!</p>");
    </script>
</body>
</html>
```

### **Cách 4: DOM Manipulation** (Modern cách)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello World</title>
</head>
<body>
    <div id="output"></div>
    
    <script>
        // Truy cập phần tử HTML bằng ID
        const output = document.getElementById("output");
        
        // Thay đổi nội dung
        output.innerHTML = "<h2>Hello, World!</h2>";
        output.innerHTML += "<p>Xin chào JavaScript!</p>";
        output.innerHTML += "<p>Đây là DOM manipulation</p>";
    </script>
</body>
</html>
```

## 🖥️ JavaScript với Node.js

### **Cài đặt Node.js**

```bash
# Windows: Tải từ nodejs.org
# Hoặc dùng Chocolatey
choco install nodejs -y

# Linux/macOS: Dùng package manager
# Ubuntu/Debian
sudo apt install nodejs npm

# macOS với Homebrew
brew install node
```

### **Kiểm tra cài đặt**

```bash
node --version  # Hiển thị phiên bản Node.js
npm --version   # Hiển thị phiên bản npm
```

### **Tạo và chạy file JavaScript**

**Bước 1:** Tạo file `hello.js`

```javascript
// hello.js
console.log("Hello, World!");
console.log("Xin chào từ Node.js!");

// Thêm thông tin hệ thống
console.log("Node.js version:", process.version);
console.log("Platform:", process.platform);
```

**Bước 2:** Chạy file

```bash
node hello.js
```

**Output:**
```
Hello, World!
Xin chào từ Node.js!
Node.js version: v18.17.0
Platform: win32
```

## 📚 So sánh Trình duyệt vs Node.js

| Đặc điểm | Trình duyệt | Node.js |
|----------|-------------|---------|
| **Global Object** | `window` | `global` |
| **File System** | ❌ Không có | ✅ Có (fs module) |
| **Network** | ✅ Fetch API | ✅ http/https modules |
| **Process Control** | ❌ Không có | ✅ Có (process module) |
| **Modules** | ES6 modules | CommonJS + ES6 |

## 🎨 Các biến thể nâng cao

### **1. Hello World với Template Literals**

```javascript
// ES6 Template Literals
const name = "Nguyễn Văn A";
const language = "JavaScript";

console.log(`Xin chào ${name}!`);
console.log(`Bạn đang học ${language}`);
console.log(`1 + 1 = ${1 + 1}`); // Expression trong template
```

### **2. Hello World với Function**

```javascript
// Function declaration
function greet(name) {
    console.log(`Xin chào, ${name}!`);
    console.log("Chúc bạn học JavaScript vui vẻ!");
}

// Arrow function (ES6)
const greetArrow = (name) => {
    console.log(`Xin chào, ${name}! (Arrow function)`);
}

// Gọi function
greet("Nguyễn Văn A");
greetArrow("JavaScript Developer");
```

### **3. Hello World với Object**

```javascript
// Tạo object
const user = {
    name: "Nguyễn Văn A",
    language: "JavaScript",
    greeting: function() {
        console.log(`Xin chào, tôi là ${this.name}`);
        console.log(`Tôi đang học ${this.language}`);
    }
};

// Gọi method
user.greeting();

// Console log object
console.log("User object:", user);
console.log("User name:", user.name);
```

### **4. Hello World với Array**

```javascript
// Tạo array các ngôn ngữ
const languages = [
    "JavaScript",
    "Java",
    "Python",
    "C++",
    "Go"
];

// In ra từng ngôn ngữ
languages.forEach((lang, index) => {
    console.log(`${index + 1}. ${lang}`);
});

// Hoặc
console.log("Hello World trong các ngôn ngữ:");
languages.forEach(lang => {
    console.log(`Hello, World! (${lang})`);
});
```

### **5. Hello World với Class (ES6)**

```javascript
// ES6 Class
class Greeting {
    constructor(name) {
        this.name = name;
    }
    
    sayHello() {
        console.log(`Xin chào, ${this.name}!`);
        console.log("Chào mừng đến với JavaScript!");
    }
    
    sayHelloMultipleTimes(count) {
        for (let i = 0; i < count; i++) {
            console.log(`${i + 1}. Hello, ${this.name}!`);
        }
    }
}

// Tạo instance
const user = new Greeting("Nguyễn Văn A");
user.sayHello();
user.sayHelloMultipleTimes(3);
```

## 🌍 Ví dụ thực tế: Hello World Web App

### **Tạo một Web App đơn giản**

**index.html:**
```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World JavaScript</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }
        #output {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            backdrop-filter: blur(10px);
        }
        button {
            background: white;
            color: #667eea;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin: 5px;
        }
        button:hover {
            background: #f0f0f0;
        }
    </style>
</head>
<body>
    <h1>🚀 Hello World với JavaScript</h1>
    <div id="output">
        <p>Nhấn button để xem JavaScript hoạt động!</p>
    </div>
    
    <button onclick="showConsole()">Console Log</button>
    <button onclick="showAlert()">Show Alert</button>
    <button onclick="showDOM()">Update DOM</button>
    
    <script>
        // Function 1: Console log
        function showConsole() {
            console.log("Hello, World từ Console!");
            console.log("Bạn có thể mở F12 để xem Console");
            alert("Đã log vào Console! Mở F12 để xem");
        }
        
        // Function 2: Alert
        function showAlert() {
            alert("Hello, World từ Alert!\n\nChào mừng bạn đến với JavaScript!");
        }
        
        // Function 3: DOM manipulation
        function showDOM() {
            const output = document.getElementById("output");
            const timestamp = new Date().toLocaleString('vi-VN');
            
            output.innerHTML = `
                <h2>🌟 Hello, World!</h2>
                <p><strong>Xin chào!</strong> Đây là JavaScript DOM manipulation</p>
                <p>Thời gian: ${timestamp}</p>
                <p>Bạn đã tương tác với trang web bằng JavaScript</p>
            `;
        }
        
        // Auto-run on page load
        document.addEventListener('DOMContentLoaded', function() {
            console.log("✅ Trang đã load xong!");
            console.log("JavaScript đang chạy trong trình duyệt!");
        });
    </script>
</body>
</html>
```

## 🔧 Đọc tệp HTML và chạy Hello World

### **Cách 1: Mở trực tiếp**
1. Lưu file như `hello.html`
2. Double-click để mở trong trình duyệt
3. Mở Console (F12) để xem log

### **Cách 2: Dùng Live Server (VS Code)**
```bash
# Cài extension "Live Server" trong VS Code
# Click phải vào file HTML
# Chọn "Open with Live Server"
```

### **Cách 3: Dùng Node.js server**

**server.js:**
```javascript
const http = require('http');
const fs = require('fs');

const server = http.createServer((req, res) => {
    if (req.url === '/') {
        fs.readFile('index.html', (err, data) => {
            if (err) {
                res.writeHead(404);
                res.end('File not found');
            } else {
                res.writeHead(200, { 'Content-Type': 'text/html' });
                res.end(data);
            }
        });
    } else if (req.url === '/hello.js') {
        fs.readFile('hello.js', (err, data) => {
            res.writeHead(200, { 'Content-Type': 'application/javascript' });
            res.end(data);
        });
    }
});

server.listen(3000, () => {
    console.log('✅ Server đang chạy tại http://localhost:3000');
});
```

**Chạy:**
```bash
node server.js
# Mở browser: http://localhost:3000
```

## 📊 So sánh Console API

```javascript
// console.log() - In thông tin
console.log("Hello, World!");

// console.info() - Thông tin
console.info("Đây là thông tin");

// console.warn() - Cảnh báo (màu vàng)
console.warn("Đây là cảnh báo!");

// console.error() - Lỗi (màu đỏ)
console.error("Đây là lỗi!");

// console.table() - Hiển thị dạng bảng
const users = [
    {name: "Nguyễn Văn A", age: 25},
    {name: "Trần Thị B", age: 30}
];
console.table(users);

// console.group() - Nhóm logs
console.group("Thông tin user");
console.log("Name:", "Nguyễn Văn A");
console.log("Age:", 25);
console.groupEnd();
```

## 🎯 Bài tập thực hành

### **Bài 1: Personalized Greeting**
Viết function nhận vào tên và in ra lời chào cá nhân

**Giải:**
```javascript
function personalizedGreeting(name) {
    console.log(`Xin chào ${name}!`);
    console.log(`Chúc ${name} một ngày tốt lành!`);
}

personalizedGreeting("Nguyễn Văn A");
```

### **Bài 2: Multiple Languages**
In "Hello, World!" bằng 3 ngôn ngữ khác nhau

**Giải:**
```javascript
const greetings = {
    vi: "Xin chào Thế giới!",
    en: "Hello, World!",
    ja: "こんにちは世界！",
    es: "¡Hola, Mundo!",
    fr: "Bonjour le Monde!"
};

for (const [lang, greeting] of Object.entries(greetings)) {
    console.log(`${lang}: ${greeting}`);
}
```

### **Bài 3: Interactive Greeting**
Tạo form nhận input và hiển thị greeting

```html
<input type="text" id="nameInput" placeholder="Nhập tên">
<button onclick="greet()">Chào hỏi</button>
<div id="result"></div>

<script>
function greet() {
    const name = document.getElementById("nameInput").value;
    const result = document.getElementById("result");
    
    if (name) {
        result.innerHTML = `<h2>Xin chào, ${name}!</h2>`;
    } else {
        alert("Vui lòng nhập tên!");
    }
}
</script>
```

## 🐛 Debug với Console

```javascript
// Debug với console
let name = "JavaScript";
console.log("Name variable:", name);
console.log("Type:", typeof name);
console.log("Length:", name.length);

// Debug complex object
const user = {
    name: "Nguyễn Văn A",
    skills: ["JavaScript", "HTML", "CSS"],
    age: 25,
    isActive: true
};
console.log("Full user object:", user);

// Debug với JSON
console.log("User as JSON:", JSON.stringify(user, null, 2));
```

## 🎉 Kết luận

Qua bài học này, bạn đã học được:

- ✅ Cách in ra console và alert trong trình duyệt
- ✅ Cách chạy JavaScript với Node.js
- ✅ Template literals và arrow functions
- ✅ DOM manipulation cơ bản
- ✅ So sánh trình duyệt vs Node.js

> **🚀 Bước tiếp theo:** Học về biến, kiểu dữ liệu và hàm trong JavaScript!

## 📖 Tài liệu tham khảo

- 📚 [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- 🌐 [JavaScript.info](https://javascript.info/)
- 🎓 [Node.js Documentation](https://nodejs.org/docs/)
- 💻 [Can I Use](https://caniuse.com/) - Check browser support
