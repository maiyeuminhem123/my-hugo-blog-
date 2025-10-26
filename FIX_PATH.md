# 🔧 SỬA LỖI PATH

## ❌ Lỗi hiện tại:
Đã thêm: `C:\Hugo\bin\hugo.exe` (SAI - đây là file .exe)
Phải là: `C:\Hugo\bin` (ĐÚNG - đây là thư mục)

## ✅ Sửa lại như sau:

### Cách 1: Sửa trực tiếp trong "Edit environment variable"

1. Mở lại cửa sổ "Edit environment variable" (như trong hình)
2. Tìm dòng: `C:\Hugo\bin\hugo.exe` 
3. Click chọn dòng đó
4. Click nút **"Edit text..."** (ở dưới cùng bên trái)
5. Xóa `\hugo.exe` đi, chỉ giữ lại: `C:\Hugo\bin`
6. Click OK để lưu
7. Mở lại terminal mới

### Cách 2: Dùng PowerShell để sửa

Mở PowerShell as Administrator và chạy:

```powershell
# Lấy PATH hiện tại
$oldPath = [Environment]::GetEnvironmentVariable("Path", "User")

# Xóa phần sai và thêm đúng
$newPath = $oldPath -replace 'C:\\Hugo\\bin\\hugo\\.exe;?', ''
$newPath = $newPath + ';C:\Hugo\bin'

# Lưu lại
[Environment]::SetEnvironmentVariable("Path", $newPath, "User")
```

### Cách 3: Thêm thủ công (Đơn giản nhất)

1. Mở "Edit environment variable"
2. Click **"New"** → thêm: `C:\Hugo\bin`
3. Tìm và xóa dòng: `C:\Hugo\bin\hugo.exe`
4. Click OK
5. **QUAN TRỌNG:** Đóng hết các terminal/PowerShell đang mở
6. Mở lại terminal mới
7. Test: `hugo version`

## ⚠️ Lưu ý:
- PATH phải chứa **THƯ MỤC** chứa file, không phải file .exe
- Sau khi sửa xong, **ĐÓNG TẤT CẢ TERMINAL** và mở lại
- Nếu vẫn lỗi, restart máy tính

## 🧪 Test sau khi sửa:

```powershell
hugo version
# Nên hiện: Hugo Static Site Generator v0.XXX.0/extended ...
```

