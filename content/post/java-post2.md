---
title: "Hello World và Cách biên dịch trong Java"
date: 2025-10-17
categories: ["Java"]
featured: "images/featured-2.svg"
image: "images/featured-2.svg"
description: "Hướng dẫn chi tiết cách viết, biên dịch và chạy chương trình Hello World đầu tiên trong Java với các bước từ cài đặt đến thực thi."
---

## Viết chương trình Hello World với Java

Chương trình **Hello World** là ví dụ kinh điển và đơn giản nhất để bắt đầu với bất kỳ ngôn ngữ lập trình nào. Trong Java, đây là cách để bạn làm quen với cú pháp cơ bản và quy trình biên dịch.

> **💡 Mục tiêu:** Tạo chương trình Java đầu tiên, hiểu cấu trúc cơ bản và cách biên dịch

## 📝 Mã nguồn Hello World

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        System.out.println("Xin chào Java!");
        System.out.println("Chúc mừng bạn đã bắt đầu học Java!");
    }
}
```

## 🔍 Giải thích chi tiết từng phần

### 1. **Class Declaration**
```java
public class HelloWorld {
```
- `public`: Access modifier - class có thể truy cập từ bên ngoài
- `class`: Keyword định nghĩa một class
- `HelloWorld`: Tên class (phải trùng với tên file)
- `{`: Bắt đầu body của class

### 2. **Main Method**
```java
public static void main(String[] args) {
```
- `public`: Method có thể gọi từ bên ngoài
- `static`: Method thuộc về class, không cần tạo object
- `void`: Method không trả về giá trị
- `main`: Tên method - entry point của chương trình
- `String[] args`: Tham số command line arguments
- `{`: Bắt đầu body của method

### 3. **Output Statement**
```java
System.out.println("Hello, World!");
```
- `System`: Class chứa các thành phần hệ thống
- `out`: PrintStream object để xuất dữ liệu
- `println()`: Method in ra màn hình và xuống dòng
- `"Hello, World!"`: String literal - văn bản cần in

## 🛠️ Cài đặt môi trường phát triển

### **Bước 1: Tải và cài đặt JDK**
1. Truy cập [Oracle JDK](https://www.oracle.com/java/technologies/downloads/) hoặc [OpenJDK](https://openjdk.org/)
2. Tải phiên bản JDK 17 LTS (khuyến nghị)
3. Cài đặt theo hướng dẫn của hệ điều hành

### **Bước 2: Kiểm tra cài đặt**
```bash
# Kiểm tra phiên bản Java
java -version

# Kiểm tra compiler
javac -version
```

### **Bước 3: Cấu hình PATH (nếu cần)**
**Windows:**
```cmd
set JAVA_HOME=C:\Program Files\Java\jdk-17
set PATH=%JAVA_HOME%\bin;%PATH%
```

**Linux/macOS:**
```bash
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk
export PATH=$JAVA_HOME/bin:$PATH
```

## ⚙️ Biên dịch và chạy chương trình

### **Bước 1: Tạo file nguồn**
1. Tạo file `HelloWorld.java`
2. Copy mã nguồn vào file
3. Lưu file (đảm bảo encoding UTF-8)

### **Bước 2: Biên dịch**
```bash
javac HelloWorld.java
```
- Tạo file `HelloWorld.class` (bytecode)
- Nếu có lỗi, kiểm tra cú pháp

### **Bước 3: Chạy chương trình**
```bash
java HelloWorld
```
- Chạy file `.class` (không cần extension)

## 🎯 Các biến thể của Hello World

### **1. Hello World với biến**
```java
public class HelloWorld {
    public static void main(String[] args) {
        String message = "Hello, World!";
        String name = "Java Developer";
        
        System.out.println(message);
        System.out.println("Xin chào, " + name + "!");
    }
}
```

### **2. Hello World với input từ user**
```java
import java.util.Scanner;

public class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Nhập tên của bạn: ");
        String name = scanner.nextLine();
        
        System.out.println("Xin chào, " + name + "!");
        
        scanner.close();
    }
}
```

### **3. Hello World với command line arguments**
```java
public class HelloWorld {
    public static void main(String[] args) {
        if (args.length > 0) {
            System.out.println("Xin chào, " + args[0] + "!");
        } else {
            System.out.println("Xin chào, World!");
        }
    }
}
```

**Chạy với arguments:**
```bash
java HelloWorld Nguyễn Văn A
```

## 🐛 Xử lý lỗi thường gặp

### **1. Lỗi "javac is not recognized"**
```bash
# Windows
'javac' is not recognized as an internal or external command

# Giải pháp: Thêm JDK/bin vào PATH
```

### **2. Lỗi "Could not find or load main class"**
```bash
# Lỗi
Error: Could not find or load main class HelloWorld

# Nguyên nhân: Tên class không khớp với tên file
# Giải pháp: Đảm bảo tên class = tên file
```

### **3. Lỗi biên dịch**
```bash
# Lỗi cú pháp
HelloWorld.java:3: error: ';' expected

# Giải pháp: Kiểm tra dấu chấm phẩy, ngoặc nhọn
```

## 🎨 Best Practices

### **1. Naming Conventions**
- Class name: PascalCase (`HelloWorld`)
- Method name: camelCase (`main`)
- Variable name: camelCase (`userName`)

### **2. Code Formatting**
```java
public class HelloWorld {
    public static void main(String[] args) {
        // Proper indentation
        System.out.println("Hello, World!");
    }
}
```

### **3. Comments**
```java
/**
 * Chương trình Hello World đầu tiên
 * @author Your Name
 * @version 1.0
 */
public class HelloWorld {
    public static void main(String[] args) {
        // In ra màn hình lời chào
        System.out.println("Hello, World!");
    }
}
```

## 🚀 Mở rộng: Hello World nâng cao

### **1. Hello World với GUI (Swing)**
```java
import javax.swing.JOptionPane;

public class HelloWorldGUI {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hello, World!");
    }
}
```

### **2. Hello World với Date/Time**
```java
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;

public class HelloWorldTime {
    public static void main(String[] args) {
        LocalDateTime now = LocalDateTime.now();
        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd/MM/yyyy HH:mm:ss");
        
        System.out.println("Hello, World!");
        System.out.println("Thời gian hiện tại: " + now.format(formatter));
    }
}
```

### **3. Hello World với Properties**
```java
import java.util.Properties;

public class HelloWorldProps {
    public static void main(String[] args) {
        Properties props = System.getProperties();
        
        System.out.println("Hello, World!");
        System.out.println("Java Version: " + props.getProperty("java.version"));
        System.out.println("OS: " + props.getProperty("os.name"));
    }
}
```

## 📚 Bài tập thực hành

### **Bài tập 1: Personalized Hello**
Viết chương trình yêu cầu user nhập tên và in ra lời chào cá nhân hóa.

### **Bài tập 2: Multiple Languages**
Tạo chương trình in "Hello, World!" bằng nhiều ngôn ngữ khác nhau.

### **Bài tập 3: ASCII Art**
Tạo chương trình in ra hình ảnh ASCII đơn giản.

## 🎯 Kết luận

Chương trình Hello World là bước đầu tiên quan trọng trong hành trình học Java. Qua bài học này, bạn đã hiểu:

- ✅ Cấu trúc cơ bản của chương trình Java
- ✅ Cách biên dịch và chạy Java code
- ✅ Các lỗi thường gặp và cách xử lý
- ✅ Best practices trong Java programming

> **🚀 Bước tiếp theo:** Hãy thử viết các chương trình đơn giản khác để làm quen với cú pháp Java!

## 📖 Tài liệu tham khảo

- 📚 [Oracle Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- 🎓 [Java Code Style Guide](https://google.github.io/styleguide/javaguide.html)
- 💻 [IntelliJ IDEA - Java IDE](https://www.jetbrains.com/idea/)
- 🔧 [VS Code Java Extension Pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
