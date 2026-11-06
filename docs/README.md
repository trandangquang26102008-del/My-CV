# My-CV — Portfolio cá nhân

## Tên dự án

**My-CV** — trang portfolio/CV cá nhân của Trần Đăng Quang.

## Mô tả

Website tĩnh giới thiệu cá nhân, kỹ năng, một số dự án minh họa và thông tin liên hệ. Giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Giới thiệu bản thân và định hướng Frontend Developer.
- Hiển thị các kỹ năng và dự án tiêu biểu.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp email và các liên kết hồ sơ cá nhân.

Nội dung hiện được viết tĩnh trong HTML. Các thẻ dự án là nội dung minh họa; một số liên kết xem chi tiết và hồ sơ mạng xã hội chưa được cấu hình thành địa chỉ hoạt động. Trang chưa có backend, xử lý biểu mẫu hay chức năng JavaScript.

## Công nghệ

- HTML5
- CSS3 (Flexbox, CSS Grid, media queries)
- Docker và Nginx (tùy chọn, để phục vụ trang)

## Yêu cầu môi trường

### Chạy trực tiếp

- Trình duyệt hiện đại có hỗ trợ HTML5 và CSS3.
- Không cần Node.js, npm hoặc bước biên dịch.
- Để dùng máy chủ phát triển trong các ví dụ bên dưới: Python 3.
- Có thể mở `index.html` trực tiếp, nhưng chạy qua máy chủ HTTP giúp kiểm tra gần với môi trường triển khai hơn.

### Chạy bằng Docker

- Docker Engine/Desktop đã cài đặt và đang chạy.
- Kết nối Internet lần đầu để tải image `nginx:alpine`.

## Cài đặt

Tải hoặc clone dự án, sau đó mở terminal tại thư mục gốc có chứa `index.html`.

```text
My-CV/
├── index.html
├── assets/
│   ├── css/
│   └── img/
└── docs/
    └── README.md
```

Không cần cài thêm package.

## Cấu hình

- **Thông tin và nội dung trang:** sửa `index.html`.
- **Giao diện và breakpoint responsive:** sửa `assets/css/styles.css`.
- **Ảnh:** lưu trong `assets/img/` và cập nhật đường dẫn `src` trong `index.html`.
- **Visual Studio Code:** `.vscode/settings.json` đặt cổng Live Server mặc định là `5501`. Có thể cài extension Live Server và mở `index.html` bằng **Open with Live Server**.
- Trước khi phát hành, hãy thay nội dung dự án minh họa và kiểm tra lại các liên kết GitHub, LinkedIn trong `index.html`.

## Chạy thử

Sau khi chạy máy chủ, mở <http://localhost:5501> trong trình duyệt. Nếu sử dụng cổng khác, thay `5501` bằng cổng đã chọn.

### Windows (PowerShell)

Tại thư mục dự án:

```powershell
py -m http.server 5501
```

Nếu lệnh `py` không có sẵn, thử:

```powershell
python -m http.server 5501
```

Dừng máy chủ bằng `Ctrl+C`.

### macOS

Tại thư mục dự án:

```bash
python3 -m http.server 5501
```

Dừng máy chủ bằng `Ctrl+C`.

### Linux

Tại thư mục dự án:

```bash
python3 -m http.server 5501
```

Nếu Python 3 chưa được cài đặt, cài đặt Python 3 theo hướng dẫn của bản phân phối Linux rồi chạy lại lệnh. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Từ thư mục gốc dự án, chạy Nginx và mount mã nguồn chỉ đọc vào container.

**macOS / Linux:**

```bash
docker run --rm --name my-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

**Windows PowerShell:**

```powershell
docker run --rm --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080>. Dừng container bằng `Ctrl+C`; tùy chọn `--rm` tự xóa container sau khi dừng.

## Kiểm tra nhanh

- Trang mở được và không có lỗi tải `assets/css/styles.css` hoặc hình ảnh.
- Các mục điều hướng cuộn đến đúng phần.
- Bố cục hiển thị phù hợp ở cả màn hình nhỏ và màn hình lớn.
- Email mở đúng ứng dụng email; cập nhật GitHub, LinkedIn và liên kết dự án trước khi công khai.

## Thông tin liên hệ

- **Người thực hiện:** Trần Đăng Quang
- **Email:** [trandangquang26102008@gmail.com](mailto:trandangquang26102008@gmail.com)
- **GitHub:** `github.com/trandangquang26102008-del` (địa chỉ hiển thị trong trang; cần xác nhận và cập nhật liên kết)
- **LinkedIn:** thông tin trong trang hiện là văn bản placeholder; hãy bổ sung URL hồ sơ chính xác trước khi phát hành.