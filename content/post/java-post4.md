---
title: "Lập trình hướng đối tượng (OOP) trong Java"
date: 2025-10-17
categories: ["Java"]
featured: "images/featured-4.svg"
image: "images/featured-4.svg"
---

## Lập trình hướng đối tượng (OOP) trong Java

Java hỗ trợ đầy đủ các tính năng của lập trình hướng đối tượng: Lớp, đối tượng, kế thừa, đóng gói, đa hình và trừu tượng.

### Các khái niệm cơ bản:
- Lớp (Class): Khuôn mẫu để tạo đối tượng.
- Đối tượng (Object): Thể hiện cụ thể của lớp.
- Kế thừa (Inheritance): Cho phép một lớp con kế thừa thuộc tính và phương thức của lớp cha.
- Đa hình (Polymorphism): Khả năng gọi cùng một phương thức trên các đối tượng khác nhau và thực hiện hành vi khác nhau.
- Đóng gói (Encapsulation): Ẩn dữ liệu bên trong lớp và cung cấp phương thức truy cập.

### Ví dụ:
```java
class Animal {
    void speak() {
        System.out.println("Animal speaks");
    }
}

class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("Dog barks");
    }
}

public class TestOOP {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.speak(); // Dog barks
    }
}
```

> Lập trình hướng đối tượng giúp tổ chức mã nguồn rõ ràng, dễ bảo trì và mở rộng.

### Lưu ý khi thiết kế OOP
- Thiết kế lớp hợp lý, tránh lặp lại code.
- Áp dụng SOLID principles khi xây dựng hệ thống lớn.

### Tài liệu tham khảo
- https://docs.oracle.com/javase/tutorial/java/concepts/
- https://en.wikipedia.org/wiki/Object-oriented_programming
