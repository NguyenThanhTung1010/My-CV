# Release Note

## Phiên bản v1.1

- **Ngày phát hành:** 24/11/2026

## Chức năng mới & Cải tiến

### Giao diện – Chủ đề Hồng – Đen

- Áp dụng bảng màu **Hồng neon (#ff2d78) phối nền đen (#0d0d0d)** toàn trang.
- Toàn bộ màu sắc được quản lý qua CSS Custom Properties trong `:root` – dễ bảo trì và đổi chủ đề.
- Header sticky trong suốt với `backdrop-filter: blur` và viền hồng mờ.
- Gradient hero hồng neon phát sáng từ phía trên trang.
- Card dự án nền tối với viền hồng sáng khi hover.

### Hiệu ứng Animation (mới hoàn toàn)

- **`fadeInUp`** – Các phần tử hero (eyebrow, tiêu đề, vai trò, mô tả, nút, avatar) xuất hiện lần lượt khi tải trang.
- **`floatY`** – Ảnh đại diện lơ lửng nhẹ nhàng.
- **`pinkPulse`** – Logo brand trong header nhịp đập theo màu hồng.
- **Underline trượt** – Gạch chân hồng trượt vào khi hover link điều hướng.
- **Hover card nâng** – Card dự án nâng lên `6px` + glow hồng + zoom ảnh nhẹ.
- **Hover thẻ liên hệ** – Thẻ liên hệ trượt sang phải + viền hồng sáng.
- **Cursor nhấp nháy** – Hiệu ứng dấu gạch đứng sau eyebrow.
- Hỗ trợ `prefers-reduced-motion`: tắt toàn bộ animation cho người dùng có nhu cầu giảm chuyển động.

### Phần Liên hệ cải tiến

- Thiết kế lại hoàn toàn thành **2 cột**: phần CTA bên trái và danh sách thẻ bên phải.
- 4 thẻ liên hệ với icon: **Email**, **GitHub**, **LinkedIn**, **Điện thoại**.
- Nút CTA "Gửi email cho tôi" nổi bật với màu hồng gradient.
- Liên kết email sửa thành đúng dạng `mailto:`.
- GitHub và LinkedIn có `rel="noopener noreferrer"` cho bảo mật.

### Chất lượng mã nguồn

- Thêm gạch chân gradient hồng dưới mỗi tiêu đề section.
- Tiêu đề hero dùng gradient text (trắng → hồng).
- Chip kỹ năng có hover animation.
- Tag dự án dùng màu hồng thay vì xám.
- Nhất quán tên Nguyễn Thanh Tùng trong toàn bộ metadata và `alt`.
- Cập nhật tài liệu README và test_report.md theo giao diện mới.

## Lỗi đã sửa

- Sửa liên kết email từ `href="email@..."` thành `href="mailto:email@..."`.
- Đồng bộ tên tác giả trong `<meta name="author">` với nội dung trang.
- Sửa `alt` ảnh đại diện từ "Nguyễn Thành Tùng" thành "Nguyễn Thanh Tùng".

## Hạn chế còn tồn tại

- Các liên kết "Xem chi tiết" của dự án vẫn là placeholder `href="#"`.
- Số điện thoại chưa được điền thực tế (`+84 xxx xxx xxx`).
- Chưa có biểu mẫu liên hệ hoặc chức năng xử lý dữ liệu phía máy chủ.
- Ảnh minh chứng trong `docs/` cần chụp lại từ giao diện v1.1.

---

## Phiên bản v1.0

- **Ngày phát hành:** 06/11/2026

## Chức năng ban đầu

- Ra mắt trang portfolio cá nhân giới thiệu thông tin và vai trò Frontend Developer.
- Bổ sung các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ cùng điều hướng trong trang.
- Hiển thị kỹ năng và dự án bằng bố cục dạng thẻ.
- Hỗ trợ giao diện responsive trên máy tính, máy tính bảng và điện thoại.
