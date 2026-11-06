# Portfolio cá nhân – Nguyễn Thanh Tùng

## Mô tả dự án

Website portfolio cá nhân giới thiệu Nguyễn Thanh Tùng, định hướng Frontend Developer. Trang được xây dựng bằng HTML và CSS thuần, tập trung vào bố cục rõ ràng, nội dung dễ theo dõi và hiển thị phù hợp trên nhiều kích thước màn hình.

## Chức năng

- Giới thiệu thông tin cá nhân và định hướng nghề nghiệp.
- Trình bày các kỹ năng và công nghệ.
- Hiển thị danh sách dự án dưới dạng thẻ có hình ảnh, mô tả và nhãn công nghệ.
- Điều hướng nhanh tới các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp thông tin liên hệ và liên kết quay lại đầu trang.
- Giao diện responsive cho điện thoại, máy tính bảng và máy tính.

> Một số liên kết dự án và mạng xã hội hiện vẫn là liên kết mẫu. Hãy cập nhật các địa chỉ này trước khi công bố website.

## Công nghệ sử dụng

- HTML5
- CSS3
- CSS Flexbox và Grid
- CSS custom properties (biến CSS)
- Ảnh tĩnh lưu trong thư mục `assets/img/`

Dự án hiện không sử dụng framework JavaScript, trình quản lý gói hoặc backend.

## Cấu trúc thư mục

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
├── docs/
│   ├── responsive-desktop.png
│   ├── responsive-mobile.png
│   └── responsive-tablet.png
├── README.md
├── RELEASENOTE.md
└── test_report.md
```

## Yêu cầu môi trường

### Chỉ xem trang

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Có thể mở `index.html` trực tiếp; tuy nhiên, nên chạy máy chủ web cục bộ để kiểm tra giống môi trường triển khai hơn.

### Chạy máy chủ web cục bộ

Chọn một trong các cách sau:

- Python 3 (không cần cài thêm thư viện).
- Docker Desktop hoặc Docker Engine nếu chạy bằng Docker.

## Cài đặt

1. Tải hoặc sao chép toàn bộ dự án về máy.
2. Mở Terminal/PowerShell tại thư mục gốc dự án (thư mục chứa `index.html`).
3. Không cần cài dependency để chạy phiên bản hiện tại.

Nếu dùng Git:

```bash
git clone <URL-repository>
cd <ten-thu-muc-du-an>
```

Thay `<URL-repository>` bằng địa chỉ repository thực tế. Nếu đã tải mã nguồn về máy, chỉ cần mở terminal tại thư mục đó.

## Cấu hình

Dự án hiện không yêu cầu tệp `.env`, cơ sở dữ liệu, API key hay bước build.

- Nội dung trang được khai báo trong `index.html`.
- Kiểu dáng và breakpoint responsive được khai báo trong `assets/css/styles.css`.
- Thay ảnh trong `assets/img/` và cập nhật đường dẫn ảnh tương ứng trong `index.html` khi cần.
- Trước khi phát hành, cập nhật các liên kết dự án/mạng xã hội đang để `#`; kiểm tra địa chỉ email và thông tin cá nhân có thể công khai.

## Chạy thử

### Windows (PowerShell)

Tại thư mục dự án, chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy nhưng đã cài Python, thử:

```powershell
python -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

> Nếu cổng `8000` đang được sử dụng, đổi `8000` trong lệnh và URL sang một cổng khác, ví dụ `8080`.

## Chạy bằng Docker

Dự án chưa kèm `Dockerfile` hoặc `docker-compose.yml`. Có thể dùng image Nginx có sẵn để phục vụ các tệp tĩnh, không cần tạo thêm cấu hình.

Yêu cầu: Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux) đang chạy.

### Windows (PowerShell)

Chạy tại thư mục gốc dự án:

```powershell
docker run --rm -d --name portfolio -p 8080:80 -v "$($PWD.Path):/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Khi chạy xong, dừng container:

```powershell
docker stop portfolio
```

### macOS và Linux

Chạy tại thư mục gốc dự án:

```bash
docker run --rm -d --name portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Khi chạy xong, dừng container:

```bash
docker stop portfolio
```

Lần đầu chạy, Docker có thể cần tải image `nginx:alpine` từ registry. Nếu tên container `portfolio` hoặc cổng `8080` đã được sử dụng, hãy chọn tên/cổng khác và dùng đúng tên khi dừng container.

## Kiểm tra trước khi bàn giao

- Mở trang trên desktop, tablet và điện thoại hoặc dùng chế độ giả lập thiết bị của trình duyệt.
- Kiểm tra các mục điều hướng, hình ảnh và mọi liên kết.
- Xác nhận nội dung cá nhân, địa chỉ email và các URL dự án/mạng xã hội.
- Xem [test_report.md](./test_report.md) để tham khảo các mục cần kiểm tra và các giới hạn đã ghi nhận.

## Thông tin liên hệ

- **Tên:** Nguyễn Thanh Tùng
- **Email:** [nguyenthanhtung36@gmail.com](mailto:nguyenthanhtung36@gmail.com)
- **GitHub:** [github.com/nguyenthanhtung](https://github.com/nguyenthanhtung) — vui lòng xác nhận/cập nhật URL nếu chưa chính xác.
- **LinkedIn:** linkedin.com/in/nguyenthanhtung — cập nhật liên kết hồ sơ thực tế trước khi công bố.