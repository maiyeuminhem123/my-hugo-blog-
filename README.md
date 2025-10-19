# 🚀 Blog Lập Trình Java & JavaScript

## 📝 Giới thiệu

Blog cá nhân chia sẻ kiến thức về lập trình Java & JavaScript, được xây dựng bằng **Hugo** và theme **Stack**. Blog này phục vụ cho đồ án học phần về lập trình mạng.

## ✨ Tính năng

- ✅ **Responsive Design** - Tương thích mọi thiết bị
- ✅ **Dark/Light Mode** - Chế độ sáng/tối
- ✅ **SEO Optimized** - Tối ưu hóa công cụ tìm kiếm
- ✅ **Fast Loading** - Tốc độ tải nhanh với Hugo SSG
- ✅ **Disqus Comments** - Hệ thống bình luận
- ✅ **RSS Feed** - Nguồn cấp dữ liệu RSS

## 📚 Nội dung

### ☕ **Java Programming (4 bài)**
1. Giới thiệu ngôn ngữ Java
2. Hello World và cách biên dịch
3. Kiểu dữ liệu cơ bản trong Java
4. Lập trình hướng đối tượng (OOP)

### 🟨 **JavaScript Programming (5 bài)**
1. Tổng quan về JavaScript
2. Hello World với JavaScript (Trình duyệt & Node.js)
3. Khai báo biến và scope trong JavaScript
4. Kiểu dữ liệu trong JavaScript và ép kiểu
5. Hàm closure và bất đồng bộ trong JavaScript

### 🌐 **Network Programming (1 bài)**
1. Lập trình mạng là gì? Học lập trình mạng cần ngôn ngữ gì

## 🛠️ Công nghệ sử dụng

- **Framework:** Hugo (Static Site Generator)
- **Theme:** Stack
- **Language:** Vietnamese
- **Deploy:** Netlify
- **Version Control:** Git

## 🚀 Cài đặt và chạy local

### Yêu cầu
- Hugo Extended (v0.80+)
- Git

### Các bước

1. **Clone repository:**
```bash
git clone https://github.com/yourusername/myblog.git
cd myblog
```

2. **Cài đặt theme:**
```bash
git submodule update --init --recursive
```

3. **Chạy development server:**
```bash
hugo server --disableFastRender
```

4. **Truy cập:** http://localhost:1313

## 📁 Cấu trúc thư mục

```
myblog/
├── content/           # Nội dung bài viết
│   ├── post/         # Bài viết blog
│   ├── _index.md     # Trang chủ
│   ├── about.md      # Trang giới thiệu
│   └── contact.md    # Trang liên hệ
├── static/           # File tĩnh (ảnh, CSS, JS)
├── themes/           # Theme Hugo
├── hugo.toml         # Cấu hình Hugo
└── public/           # File build (generated)
```

## ✍️ Viết bài mới

1. Tạo file mới trong `content/post/`
2. Thêm front matter:
```yaml
---
title: "Tiêu đề bài viết"
date: 2025-10-17
categories: ["Java"] # hoặc ["JavaScript"]
featured: "/images/featured-X.svg"
image: "/images/featured-X.svg"
---
```

3. Viết nội dung bằng Markdown

## 🎨 Tùy chỉnh

- **Cấu hình:** Chỉnh sửa `hugo.toml`
- **Theme:** Tùy chỉnh trong `themes/hugo-theme-stack/`
- **Styling:** Thêm CSS trong `assets/scss/`

## 📞 Liên hệ

- **Tác giả:** Nguyễn Văn Thuận
- **Email:** nguyenvanthuan7395@gmail.com
- **GitHub:** [github.com/maiyeuminhem123](https://github.com/maiyeuminhem123)

## 📄 License

Licensed under CC BY-NC-SA 4.0

---

> *"Học lập trình không chỉ là viết code, mà còn là cách tư duy và giải quyết vấn đề một cách logic và sáng tạo."*
