# 📥 Hướng dẫn cài Hugo trên Windows

## ⚠️ Vấn đề hiện tại
Blog đã có file build cũ trong thư mục `public/` nhưng **chưa build lại với CSS mới**. Cần cài Hugo để build lại.

## 🚀 Các cách cài Hugo

### Cách 1: Tải trực tiếp (Dễ nhất) ⭐

**Bước 1: Tải Hugo Extended**
- Truy cập: https://github.com/gohugoio/hugo/releases
- Tìm phiên bản **Extended** (có chữ "extended" trong tên file)
- Tải file: `hugo_0.XXX.0_windows-amd64.zip` (Extended version)

**Bước 2: Giải nén và cài đặt**
1. Giải nén file `.zip` vừa tải
2. Tạo thư mục: `C:\Hugo\`
3. Copy toàn bộ file từ folder giải nén vào `C:\Hugo\bin\`
4. Cấu trúc sẽ là: `C:\Hugo\bin\hugo.exe`

**Bước 3: Thêm vào PATH**
1. Nhấn `Win + R`, gõ: `sysdm.cpl` và Enter
2. Tab "Advanced" → "Environment Variables"
3. Trong "System variables", chọn "Path" → "Edit"
4. Click "New" → thêm: `C:\Hugo\bin`
5. Click "OK" để lưu

**Bước 4: Mở lại terminal và kiểm tra**
```powershell
hugo version
# Nên hiện: Hugo Static Site Generator v0.XXX.0/extended ...
```

### Cách 2: Cài qua Chocolatey

```powershell
# Cài Chocolatey trước (nếu chưa có)
# Mở PowerShell as Administrator
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Cài Hugo Extended
choco install hugo-extended -y
```

### Cách 3: Cài qua Scoop

```powershell
# Cài Scoop trước
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

# Cài Hugo
scoop install hugo-extended
```

---

## 📝 Sau khi cài Hugo xong

### Build lại website với CSS mới:

```powershell
# Di chuyển vào thư mục project
cd c:\Users\ASUS\myblog

# Build lại website
hugo --minify

# Xem preview trên local
hugo server -D
```

Sau đó mở trình duyệt: `http://localhost:1313`

---

## 🎯 Nếu không muốn cài Hugo (Tùy chọn)

### Cách 1: Dùng GitHub Actions (Tự động)

Bạn đã có file `.github/workflows/gh-pages.yml` rồi. Chỉ cần:

```powershell
# Commit và push lên GitHub
git add .
git commit -m "Update: Cải thiện giao diện tối giản"
git push origin main
```

GitHub sẽ tự động build và deploy lên GitHub Pages!

### Cách 2: Dùng Netlify

1. Đăng ký tài khoản Netlify (miễn phí)
2. Connect repository GitHub
3. Netlify sẽ tự động build và deploy
4. Có thể xem preview ngay

---

## ✅ Kiểm tra sau khi build

Sau khi chạy `hugo --minify`, kiểm tra:
- File CSS mới trong `public/scss/`
- Giao diện nhẹ nhàng, tối giản hơn
- Màu sắc: grays + blue accent

---

## 🆘 Nếu vẫn gặp lỗi

```powershell
# Kiểm tra Hugo đã cài chưa
hugo version

# Nếu chưa có, thử cài lại hoặc dùng đường dẫn đầy đủ
C:\Hugo\bin\hugo.exe version
```


