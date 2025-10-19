---
title: "Kiểu dữ liệu cơ bản trong Java"
date: 2025-10-17
categories: ["Java"]
featured: "/images/featured-3.svg"
image: "/images/featured-3.svg"
---

## Các kiểu dữ liệu cơ bản trong Java

Java hỗ trợ nhiều kiểu dữ liệu cơ bản (primitive types):

| Kiểu dữ liệu | Kích thước | Giá trị |
|-------------|-----------|--------|
| byte        | 1 byte    | -128 đến 127 |
| short       | 2 bytes   | -32,768 đến 32,767 |
| int         | 4 bytes   | -2^31 đến 2^31-1 |
| long        | 8 bytes   | -2^63 đến 2^63-1 |
| float       | 4 bytes   | Số thực đơn |
| double      | 8 bytes   | Số thực kép |
| char        | 2 bytes   | Ký tự Unicode |
| boolean     | 1 bit     | true/false |

### Ví dụ khai báo:
```java
int age = 20;
double pi = 3.14;
char c = 'A';
boolean isStudent = true;
```

> Hiểu rõ kiểu dữ liệu giúp bạn lập trình Java hiệu quả hơn.
### Ứng dụng thực tế
Việc chọn kiểu dữ liệu phù hợp giúp tối ưu bộ nhớ và hiệu năng cho ứng dụng lớn (ví dụ chọn `int` hay `long` cho ID, `float` hay `double` cho tính toán số học).

### Kết luận
Nắm chắc các kiểu dữ liệu cơ bản giúp tránh lỗi và làm cho chương trình hoạt động ổn định hơn.
