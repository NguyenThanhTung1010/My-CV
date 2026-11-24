# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio cá nhân – Nguyễn Thanh Tùng |
| Phiên bản | v1.1 |
| Ngày kiểm thử | 24/11/2026 |
| Người thực hiện/đánh giá | Nguyễn Thanh Tùng |
| Phạm vi | Rà soát toàn bộ HTML, CSS, nội dung và giao diện sau cập nhật v1.1 |
| Phương pháp | Rà soát mã nguồn, kiểm thử thủ công giao diện và chức năng |
| Môi trường kiểm thử | Trình duyệt Chrome/Edge; giả lập mobile/tablet qua DevTools |

> **Lưu ý:** Báo cáo v1.1 phản ánh trạng thái sau khi áp dụng chủ đề Hồng–Đen, thêm animation và cải thiện phần liên hệ.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các mục nội dung chính đầy đủ; liên kết dự án và số điện thoại còn là placeholder. |
| 2 | Giao diện, trải nghiệm người dùng và tương thích | Đạt | Chủ đề Hồng–Đen nhất quán; animation mượt; breakpoint mobile/tablet/desktop hoạt động. |
| 3 | Hiệu ứng & Animation | Đạt | 7 loại animation được triển khai; hỗ trợ `prefers-reduced-motion`. |
| 4 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Trang tĩnh, không JS; chưa đo Core Web Vitals chính thức. |
| 5 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không có secret/key; email công khai cần chủ sở hữu xác nhận. |
| 6 | Chất lượng mã nguồn, cấu trúc repository và tài liệu | Đạt | HTML semantic, CSS custom properties, tài liệu đầy đủ sau v1.1. |
| 7 | Khả năng triển khai, kiểm thử và minh chứng | Cần cải thiện | Có ảnh docs/; chưa có biên bản kiểm thử trình duyệt thực tế đầy đủ. |

## 3. Nội dung chi tiết

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Trang có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Đủ 4 section trong `index.html`. |
| Điều hướng nội bộ đến các khu vực trên trang | Đạt | Nav sticky với `href="#id"`; `scroll-behavior: smooth`. |
| Danh sách dự án và nội dung mô tả | Cần cải thiện | 4 thẻ dự án với ảnh thực; link "Xem chi tiết" vẫn là `href="#"`. |
| Thông tin liên hệ – Email | Đạt | Sửa thành `mailto:nguyenthanhtung36@gmail.com`. |
| Thông tin liên hệ – GitHub | Cần cải thiện | URL đặt là `github.com/nguyenthanhtung`; cần xác nhận đúng. |
| Thông tin liên hệ – LinkedIn | Cần cải thiện | URL đặt là `linkedin.com/in/nguyenthanhtung`; cần xác nhận đúng. |
| Thông tin liên hệ – Điện thoại | Cần cải thiện | Placeholder `+84 xxx xxx xxx`; cần điền số thực tế. |
| Tính nhất quán thông tin cá nhân | Đạt | Tên Nguyễn Thanh Tùng nhất quán trong tiêu đề, nội dung và `alt`. |

### 3.2 Giao diện, Màu sắc, Hiệu ứng & Tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Chủ đề màu Hồng–Đen nhất quán toàn trang | Đạt | CSS Custom Properties: `--color-primary: #ff2d78`, nền `#0d0d0d`. |
| Bố cục responsive mobile-first (360px → 768px → 1280px) | Đạt | Breakpoints 768px và 1280px; hero 1→2 cột, grid dự án 1→2→3 cột. |
| Animation: fade-in hero có delay lần lượt | Đạt | `fadeInUp` với delay 0.1s–0.7s cho từng phần tử hero. |
| Animation: float cho avatar | Đạt | `floatY` 4s infinite ease-in-out. |
| Animation: pulse hồng cho logo | Đạt | `pinkPulse` 2.5s infinite. |
| Animation: underline trượt vào nav link | Đạt | `transform: scaleX(0→1)` với `transform-origin: left`. |
| Hover card dự án: nâng lên + viền hồng | Đạt | `translateY(-6px)` + `box-shadow` hồng. |
| Hover thẻ liên hệ: slide sang phải + viền hồng | Đạt | `translateX(4px)` + `border-color` hồng. |
| Hỗ trợ `prefers-reduced-motion` | Đạt | Media query tắt toàn bộ animation/transition khi người dùng bật tùy chọn này. |
| Hình ảnh không tràn/vỡ bố cục | Đạt | `max-width: 100%`, `height: auto`, `aspect-ratio: 5/3` cho card. |
| Phông chữ hệ thống, không lỗi font | Đạt | `system-ui, -apple-system, "Segoe UI", Roboto` – không phụ thuộc font ngoài. |
| Tiếng Việt hiển thị đúng | Đạt | `charset="UTF-8"`, `lang="vi"`. |
| Tương thích đa trình duyệt | Cần cải thiện | Chưa có kết quả kiểm thử toàn diện trên Safari/Firefox thực tế. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Tải trang và tài nguyên cục bộ | Đạt | HTML tham chiếu CSS và ảnh hợp lệ trong `assets/`. |
| Hành vi JavaScript/API | Đạt | Không có JavaScript; không có gọi API – phù hợp trang tĩnh. |
| Hoạt động không cần máy chủ ứng dụng | Đạt | Mở `index.html` trực tiếp hoặc qua `python -m http.server`. |
| Hiệu năng tải trang | Cần cải thiện | Chưa đo Core Web Vitals (LCP, CLS, INP) chính thức. |
| Xử lý lỗi khi thiếu tài nguyên | Cần cải thiện | Các ảnh có `alt` text; chưa kiểm thử kịch bản ảnh lỗi tải. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bí mật, khóa API trong mã nguồn | Đạt | Không có thông tin xác thực trong HTML/CSS. |
| Thông tin cá nhân được công khai | Cần cải thiện | Email hiển thị trực tiếp; chủ sở hữu cần xác nhận đồng ý. |
| Liên kết ngoài an toàn | Đạt | GitHub/LinkedIn dùng `target="_blank" rel="noopener noreferrer"`. |
| Kiểm tra bảo mật | Cần cải thiện | Chưa có kết quả quét bảo mật chuyên dụng. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Tách HTML và CSS | Đạt | `index.html` + `assets/css/styles.css` tách biệt. |
| Semantic HTML | Đạt | `header`, `nav`, `main`, `section`, `article`, `footer`, `figure`. |
| CSS Custom Properties | Đạt | Toàn bộ màu, font, spacing định nghĩa trong `:root`. |
| Nhất quán tên metadata và `alt` | Đạt | Tên Nguyễn Thanh Tùng nhất quán, `author` meta đã cập nhật. |
| Liên kết email đúng dạng `mailto:` | Đạt | Đã sửa từ `href="email"` thành `href="mailto:email"`. |
| Tài liệu README | Đạt | Cập nhật đầy đủ giao diện v1.1, bảng màu và animation. |
| Lint/validate HTML-CSS | Cần cải thiện | Chưa chạy W3C Validator hoặc stylelint chính thức. |

### 3.6 Khả năng triển khai và minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Hướng dẫn chạy local (Python / Docker) | Đạt | Có trong README.md. |
| Minh chứng giao diện responsive | Cần cải thiện | Ảnh docs/ cần chụp lại từ bản v1.1 mới. |
| Kịch bản và kết quả kiểm thử tương tác | Cần cải thiện | Cần bổ sung biên bản kiểm thử trên trình duyệt/thiết bị thực. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung (v1.1)

Phiên bản v1.1 cải thiện đáng kể so với v1.0: giao diện **Hồng–Đen** nhất quán, 7 loại animation được triển khai đúng kỹ thuật, phần liên hệ được tái cấu trúc thành 4 thẻ có icon, và lỗi link `mailto:` đã được sửa. Cấu trúc HTML semantic và CSS Custom Properties đảm bảo khả năng bảo trì tốt.

### Vấn đề cần ưu tiên khắc phục

1. **Điền thông tin thực tế:** Số điện thoại `+84 xxx xxx xxx`, URL GitHub/LinkedIn chính xác, link "Xem chi tiết" cho từng dự án.
2. **Chụp ảnh minh chứng mới** trong `docs/` phản ánh giao diện Hồng–Đen v1.1.
3. **Kiểm thử thực tế** trên Chrome, Edge, Firefox, Safari; trên thiết bị mobile thực.
4. **Chạy W3C Validator** cho HTML và CSS trước bàn giao.
5. Xác nhận đồng ý công khai email và thông tin liên hệ cá nhân.

### Khuyến nghị quyết định bàn giao

**Khuyến nghị: Có thể bàn giao sau khi** điền đầy đủ thông tin liên hệ thực tế, chụp ảnh minh chứng giao diện mới và hoàn thành kiểm thử trình duyệt. Phần lỗi kỹ thuật nghiêm trọng (link email, bố cục, font) đã được xử lý trong v1.1.
