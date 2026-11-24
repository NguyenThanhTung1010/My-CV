# Portfolio cá nhân – Nguyễn Thanh Tùng

## Mô tả dự án

Website portfolio cá nhân giới thiệu Nguyễn Thanh Tùng, định hướng Frontend Developer. Trang được xây dựng bằng HTML và CSS thuần, áp dụng **chủ đề màu Hồng – Đen** hiện đại với hiệu ứng animation tinh tế và thiết kế responsive trên mọi thiết bị.

## Chức năng

- Giới thiệu thông tin cá nhân và định hướng nghề nghiệp.
- Trình bày các kỹ năng và công nghệ dưới dạng chip có hover animation.
- Hiển thị danh sách dự án dạng thẻ với hiệu ứng hover nâng card.
- Điều hướng sticky với hiệu ứng underline trượt khi hover.
- **Trang liên hệ cải tiến:** 4 thẻ liên hệ (Email, GitHub, LinkedIn, Điện thoại) với animation slide.
- Giao diện responsive cho điện thoại, máy tính bảng và máy tính.

> Một số liên kết dự án và mạng xã hội hiện vẫn là liên kết mẫu. Hãy cập nhật các địa chỉ này trước khi công bố website.

## Giao diện & Hiệu ứng (v1.1)

### Bảng màu: Hồng – Đen

| Vai trò | Màu | Hex |
|---|---|---|
| Nền trang chính | Đen sâu | `#0d0d0d` |
| Nền card/surface | Đen nhạt | `#161616` / `#1f1f1f` |
| Màu chính thương hiệu | Hồng neon | `#ff2d78` |
| Màu hover/dark | Hồng đậm | `#e0005e` |
| Màu nhấn phụ | Hồng pastel | `#ff79b0` |
| Chữ chính | Trắng ấm hồng | `#f0e6ea` |
| Chữ phụ | Xám hồng | `#9e8a93` |

### Hiệu ứng animation

- **Fade-in từ dưới lên** cho các phần tử hero (lần lượt có delay).
- **Float animation** cho ảnh đại diện (lơ lửng nhẹ).
- **Pulse hồng** cho logo brand trong header.
- **Underline trượt vào** khi hover link điều hướng.
- **Hover lift** cho card dự án: nâng lên + viền hồng sáng.
- **Slide hiệu ứng** cho thẻ liên hệ khi hover.
- **Gradient hero** với ánh hồng neon phát sáng từ phía trên.
- **Cursor nhấp nháy** sau dòng eyebrow.

## Công nghệ sử dụng

- HTML5 (semantic: `header`, `nav`, `main`, `section`, `article`, `footer`)
- CSS3 với Custom Properties (CSS Variables)
- CSS Flexbox và Grid
- CSS Animations & Transitions (keyframes)
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

Thay `<URL-repository>` bằng địa chỉ repository thực tế.

## Cấu hình

Dự án hiện không yêu cầu tệp `.env`, cơ sở dữ liệu, API key hay bước build.

- Nội dung trang được khai báo trong `index.html`.
- Toàn bộ màu sắc, khoảng cách và typography được định nghĩa qua **CSS Custom Properties** ở đầu `assets/css/styles.css` — chỉ cần sửa `:root` để đổi giao diện toàn trang.
- Thay ảnh trong `assets/img/` và cập nhật đường dẫn ảnh tương ứng trong `index.html` khi cần.
- Trước khi phát hành, cập nhật số điện thoại và các liên kết mạng xã hội chưa có đích thực tế.

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

### macOS / Linux

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

> Nếu cổng `8000` đang được sử dụng, đổi sang cổng khác, ví dụ `8080`.

## Chạy bằng Docker

```powershell
# Windows
docker run --rm -d --name portfolio -p 8080:80 -v "$($PWD.Path):/usr/share/nginx/html:ro" nginx:alpine
```

```bash
# macOS / Linux
docker run --rm -d --name portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Dừng: `docker stop portfolio`.

## Kiểm tra trước khi bàn giao

- Mở trang trên desktop, tablet và điện thoại hoặc dùng chế độ giả lập thiết bị của trình duyệt.
- Kiểm tra hiệu ứng animation khi tải trang và hover.
- Xác nhận thông tin liên hệ: email `mailto:`, GitHub, LinkedIn và số điện thoại.
- Xem [test_report.md](./test_report.md) để tham khảo các mục cần kiểm tra.

## Thông tin liên hệ

- **Tên:** Nguyễn Thanh Tùng
- **Email:** [nguyenthanhtung36@gmail.com](mailto:nguyenthanhtung36@gmail.com)
- **GitHub:** [github.com/nguyenthanhtung](https://github.com/nguyenthanhtung) — vui lòng xác nhận/cập nhật URL nếu chưa chính xác.
- **LinkedIn:** [linkedin.com/in/nguyenthanhtung](https://linkedin.com/in/nguyenthanhtung) — cập nhật liên kết hồ sơ thực tế trước khi công bố.
