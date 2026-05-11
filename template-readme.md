# 🚀 Tên Dự Án

> Mô tả ngắn gọn về dự án của bạn — một câu súc tích, rõ ràng.

![Laravel](https://img.shields.io/badge/Laravel-v11-red)
![PHP](https://img.shields.io/badge/PHP-8.2-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-brightgreen)

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Cài đặt](#-cài-đặt)
- [Sử dụng](#-sử-dụng)
- [Cấu trúc thư mục](#-cấu-trúc-thư-mục)
- [Bảng so sánh](#-bảng-so-sánh)
- [FAQ](#-faq)
- [License](#-license)

---

## 📖 Giới thiệu

Đây là đoạn mô tả chi tiết hơn về dự án.  
Dùng **2 dấu cách** cuối dòng để xuống dòng trong cùng đoạn.

Hoặc để trống một dòng để tạo đoạn văn mới như thế này.

> 💡 **Tip:** Dùng blockquote để highlight thông tin quan trọng hoặc lưu ý đặc biệt.

---

## ✨ Tính năng

- ✅ Tính năng thứ nhất — mô tả ngắn
- ✅ Tính năng thứ hai — mô tả ngắn
- ✅ Tính năng thứ ba
  - Tính năng con A
  - Tính năng con B
- 🔄 Đang phát triển — tính năng sắp ra mắt
- 📌 Dự kiến — tính năng tương lai

---

## ⚙️ Cài đặt

### Yêu cầu hệ thống

| Công cụ | Phiên bản tối thiểu |
|---------|:-------------------:|
| PHP     | 8.2+                |
| Laravel | 11.x                |
| MySQL   | 8.0+                |
| Node.js | 18+                 |

### Các bước cài đặt

1. Clone repository về máy:

```bash
git clone https://github.com/username/ten-du-an.git
cd ten-du-an
```

2. Cài đặt dependencies:

```bash
composer install
npm install
```

3. Tạo file `.env` từ file mẫu:

```bash
cp .env.example .env
php artisan key:generate
```

4. Cấu hình database trong `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=ten_database
DB_USERNAME=root
DB_PASSWORD=
```

5. Chạy migration và seeder:

```bash
php artisan migrate --seed
```

6. Khởi động server:

```bash
php artisan serve
```

---

## 🚀 Sử dụng

### Ví dụ cơ bản

```php
// Khởi tạo ứng dụng
$app = new Application(
    $_ENV['APP_BASE_PATH'] ?? dirname(__DIR__)
);

// Chạy ứng dụng
$app->run();
```

### Lệnh Artisan hay dùng

```bash
# Xóa cache
php artisan cache:clear
php artisan config:clear
php artisan view:clear

# Chạy queue
php artisan queue:work

# Chạy scheduler
php artisan schedule:run
```

---

## 📁 Cấu trúc thư mục

```
ten-du-an/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   └── Middleware/
│   ├── Models/
│   └── Services/
├── database/
│   ├── migrations/
│   └── seeders/
├── public/
├── resources/
│   └── views/
├── routes/
│   ├── web.php
│   └── api.php
└── tests/
```

---

## 📊 Bảng so sánh

| Tính năng         | Free  | Pro   | Enterprise |
|-------------------|:-----:|:-----:|:----------:|
| Số người dùng     | 5     | 50    | Không giới hạn |
| Lưu trữ           | 1 GB  | 10 GB | 100 GB     |
| Hỗ trợ            | Email | Chat  | 24/7       |
| API access        | ❌    | ✅    | ✅         |

---

## 📝 Tiến độ

- [x] Thiết kế database
- [x] Xây dựng API cơ bản
- [x] Giao diện admin
- [ ] Tích hợp thanh toán
- [ ] Viết unit test
- [ ] Deploy production

---

## ❓ FAQ

<details>
<summary>Làm sao để reset mật khẩu admin?</summary>

Chạy lệnh sau trong terminal:

```bash
php artisan tinker
>>> \App\Models\User::find(1)->update(['password' => bcrypt('matkhaumoi')]);
```

</details>

<details>
<summary>Lỗi 500 sau khi deploy thì xử lý thế nào?</summary>

Kiểm tra các bước sau:

1. Chạy `php artisan config:cache`
2. Kiểm tra quyền thư mục `storage/` và `bootstrap/cache/`
3. Xem log tại `storage/logs/laravel.log`

</details>

<details>
<summary>Dự án có hỗ trợ Docker không?</summary>

Hiện tại chưa có, dự kiến hỗ trợ trong **v2.0**.

</details>

---

## 👥 Đóng góp

Mọi đóng góp đều được hoan nghênh!

1. Fork repository này
2. Tạo branch mới: `git checkout -b feature/ten-tinh-nang`
3. Commit thay đổi: `git commit -m 'Add: mô tả thay đổi'`
4. Push lên branch: `git push origin feature/ten-tinh-nang`
5. Tạo Pull Request

---

## 📄 License

Dự án này sử dụng giấy phép [MIT](LICENSE).

---

<p align="center">Made with ❤️ by <a href="https://github.com/username">Your Name</a></p>
