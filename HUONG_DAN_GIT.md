# Hướng dẫn Copy Project lên Repository ShadowSwap

## Bước 1: Khởi tạo Git Repository

Mở terminal/PowerShell tại thư mục project và chạy:

```bash
git init
```

## Bước 2: Thêm tất cả các file vào Git

```bash
git add .
```

## Bước 3: Commit code lần đầu

```bash
git commit -m "Initial commit: ShadowSwap project"
```

## Bước 4: Tạo Repository mới trên GitHub/GitLab

### Nếu dùng GitHub:
1. Đăng nhập vào GitHub
2. Click nút "+" ở góc trên bên phải → "New repository"
3. Đặt tên repository: **ShadowSwap**
4. Chọn Public hoặc Private tùy ý
5. **KHÔNG** tích vào "Initialize with README" (vì đã có code rồi)
6. Click "Create repository"

### Nếu dùng GitLab:
1. Đăng nhập vào GitLab
2. Click nút "+" → "New project/repository"
3. Đặt tên project: **ShadowSwap**
4. Chọn visibility tùy ý
5. **KHÔNG** tích vào "Initialize repository with a README"
6. Click "Create project"

## Bước 5: Kết nối với Remote Repository

**LƯU Ý:** Project hiện tại đã có remote origin trỏ đến `https://github.com/kientt15052004/Unity_ShadowSwap.git`

Bạn có 2 lựa chọn:

### Lựa chọn A: Thay đổi remote origin (Khuyến nghị)

Sau khi tạo repo ShadowSwap mới, thay đổi URL của origin:

```bash
git remote set-url origin https://github.com/YOUR_USERNAME/ShadowSwap.git
```

### Lựa chọn B: Thêm remote mới (Giữ repo cũ)

Nếu muốn giữ cả 2 repo, thêm remote mới:

```bash
git remote add shadowswap https://github.com/YOUR_USERNAME/ShadowSwap.git
```

Sau đó push vào remote mới:
```bash
git push -u shadowswap bacdv
```

## Bước 6: Đổi tên branch chính (nếu cần)

Nếu muốn đổi branch chính thành `main`:

```bash
git branch -M main
```

## Bước 7: Push code lên Repository

**LƯU Ý:** Branch hiện tại của bạn là `bacdv`

### Nếu chọn Lựa chọn A (thay đổi origin):
```bash
git push -u origin bacdv
```

Hoặc nếu muốn push lên branch `main`:
```bash
git branch -M main
git push -u origin main
```

### Nếu chọn Lựa chọn B (thêm remote mới):
```bash
git push -u shadowswap bacdv
```

## Hoàn thành!

Bây giờ project của bạn đã được upload lên repository ShadowSwap. Bạn có thể truy cập và xem code trên GitHub/GitLab.

---

## Lưu ý:

- File `.gitignore` đã được cấu hình để bỏ qua các file không cần thiết của Unity (Library, Temp, Logs, etc.)
- Chỉ các file source code và assets quan trọng sẽ được commit
- Nếu gặp lỗi authentication, bạn có thể cần:
  - Cài đặt GitHub CLI hoặc GitLab CLI
  - Hoặc sử dụng Personal Access Token thay vì password

