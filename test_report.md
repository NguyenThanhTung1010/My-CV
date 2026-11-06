# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio cá nhân – Nguyễn Thanh Tùng |
| Phiên bản | v1.0 |
| Ngày kiểm thử | 06/11/2026 |
| Người thực hiện/đánh giá | Chưa cung cấp |
| Phạm vi | Đối chiếu mã nguồn và tài liệu hiện có trước khi bàn giao |
| Phương pháp | Rà soát tĩnh các tệp HTML, CSS, tài liệu và minh chứng trong repository |
| Môi trường kiểm thử | Chưa ghi nhận việc chạy thử trên trình duyệt hoặc thiết bị thực tế |

> **Lưu ý:** Trạng thái trong báo cáo phản ánh việc rà soát mã nguồn và minh chứng sẵn có. Những nội dung chưa chạy thử hoặc chưa có kết quả đo được được đánh dấu **Cần cải thiện**, không xem là đã kiểm thử đạt.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Có các mục nội dung chính; một số liên kết chưa hoàn thiện và chưa có kết quả kiểm thử tương tác. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | CSS có thiết kế mobile-first và breakpoint; chưa xác nhận hiển thị thực tế trên trình duyệt/thiết bị. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Trang tĩnh, không thấy luồng xử lý dữ liệu; chưa có kiểm thử vận hành hoặc số liệu hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Chưa thấy cấu hình hay bí mật trong phạm vi rà soát; chưa có kiểm tra bảo mật và thông tin email được công khai. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có tách HTML/CSS và thư mục ảnh; cần xử lý một số sai khác nội dung và hoàn thiện tài liệu. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Có ảnh minh chứng responsive trong `docs/`; chưa có hướng dẫn triển khai hoặc biên bản chạy kiểm thử. |

## 3. Nội dung chi tiết

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Trang có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Các section tương ứng có trong `index.html`. |
| Điều hướng nội bộ đến các khu vực trên trang | Cần cải thiện | Các liên kết điều hướng trỏ tới ID tương ứng; chưa thao tác kiểm thử trên trình duyệt. |
| Danh sách dự án và nội dung mô tả | Cần cải thiện | Có 4 thẻ dự án và ảnh cục bộ; liên kết “Xem chi tiết” hiện dùng `href="#"`, chưa dẫn tới trang dự án. |
| Thông tin liên hệ | Chưa đạt | Liên kết email dùng `href="nguyenthanhtung36@gmail.com"` thay vì dạng `mailto:`; GitHub và LinkedIn đang là liên kết `#`. |
| Tính nhất quán thông tin cá nhân | Cần cải thiện | Tiêu đề và nội dung hiển thị Nguyễn Thanh Tùng, nhưng metadata `author` ghi Nguyễn Văn An; alt ảnh đại diện ghi Nguyễn Thành Tùng. |
| Tác vụ liên hệ hoặc gửi dữ liệu | Cần cải thiện | Chưa có biểu mẫu liên hệ hay chức năng gửi dữ liệu; phù hợp với giới hạn của trang tĩnh hiện tại nhưng cần xác nhận yêu cầu sản phẩm. |

### 3.2 Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục responsive theo hướng mobile-first | Cần cải thiện | `assets/css/styles.css` khai báo bố cục mobile-first và breakpoint từ 768px, 1280px; chưa kiểm tra trực tiếp trên màn hình thực tế. |
| Bố cục co giãn và hiển thị hình ảnh | Cần cải thiện | CSS giới hạn ảnh theo chiều rộng khung; chưa xác nhận không tràn hoặc vỡ bố cục ở các kích thước khác nhau. |
| Điều hướng bằng bàn phím và trạng thái focus | Cần cải thiện | CSS có `:focus-visible` cho liên kết điều hướng; chưa thực hiện kiểm thử bàn phím đầy đủ. |
| Nội dung thay thế cho hình ảnh | Cần cải thiện | Các ảnh chính có thuộc tính `alt`; cần sửa nội dung tên trong alt ảnh đại diện và kiểm tra mức độ mô tả phù hợp. |
| Minh chứng giao diện desktop/tablet/mobile | Cần cải thiện | Có các tệp `docs/responsive-desktop.png`, `docs/responsive-tablet.png`, `docs/responsive-mobile.png`; chưa đối chiếu ảnh với phiên bản đang chạy. |
| Tương thích đa trình duyệt | Cần cải thiện | Chưa có kết quả kiểm thử trên các trình duyệt hoặc hệ điều hành khác nhau. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Tải trang và tài nguyên cục bộ | Cần cải thiện | HTML tham chiếu CSS và ảnh trong `assets/`; chưa chạy kiểm tra để xác nhận mọi đường dẫn tải thành công. |
| Xử lý lỗi khi thiếu tài nguyên hoặc có lỗi truy cập | Cần cải thiện | Chưa có kết quả kiểm thử lỗi tải ảnh/CSS hoặc hành vi khi truy cập đường dẫn không hợp lệ. |
| Hiệu năng tải trang | Cần cải thiện | Chưa đo thời gian tải, kích thước trang, hiệu năng hoặc chỉ số Core Web Vitals. |
| Hành vi JavaScript/API | Đạt | Trong phạm vi `index.html` được rà soát, không thấy luồng JavaScript hoặc gọi API; kết luận này không thay thế kiểm thử runtime toàn trang. |
| Hoạt động không cần máy chủ ứng dụng | Cần cải thiện | Cấu trúc hiện tại có vẻ là trang HTML/CSS tĩnh; chưa thực hiện thử nghiệm triển khai hoặc mở trang từ môi trường mục tiêu. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bí mật, khóa API hoặc thông tin xác thực trong mã được rà soát | Đạt | Không thấy thông tin xác thực trong các phần HTML/CSS đã xem; chưa thực hiện quét toàn repository chuyên dụng. |
| Cấu hình môi trường và dữ liệu nhạy cảm | Cần cải thiện | Chưa có tài liệu cấu hình/môi trường; cần xác nhận không có tệp cấu hình hoặc dữ liệu nhạy cảm ngoài phạm vi rà soát. |
| Thông tin cá nhân được công khai | Cần cải thiện | Địa chỉ email được hiển thị trực tiếp trên trang; chủ sở hữu cần xác nhận đồng ý công khai. |
| Liên kết bên ngoài và điều hướng an toàn | Cần cải thiện | Các liên kết mạng xã hội hiện là placeholder `#`; chưa có đích ngoài để đánh giá hoặc kiểm tra điều hướng. |
| Kiểm tra bảo mật tự động/thủ công | Cần cải thiện | Chưa có kết quả quét bảo mật hoặc kiểm thử bảo mật chuyên biệt. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Tách cấu trúc HTML và CSS | Đạt | Trang chính nằm trong `index.html`; stylesheet tách tại `assets/css/styles.css`; ảnh nằm trong `assets/img/`. |
| Tính rõ ràng và ngữ nghĩa HTML | Cần cải thiện | Có cấu trúc `header`, `nav`, `main`, `section`, `article`, `footer`; cần rà soát lại metadata và nội dung alt cho nhất quán. |
| Chất lượng nội dung và liên kết | Chưa đạt | Có liên kết mẫu `#`, metadata tên khác nội dung hiển thị và sai khác tên trong alt ảnh. |
| Hướng dẫn sử dụng/triển khai | Cần cải thiện | Chưa có hướng dẫn chạy hoặc triển khai được xác nhận trong tài liệu hiện có; cần bổ sung nếu yêu cầu bàn giao bao gồm hướng dẫn. |
| Tính nhất quán tên tài liệu phát hành | Cần cải thiện | Có `RELEASENOTE.md` và tệp `RELEASNOT.md` được cung cấp ban đầu; cần xác nhận tên chuẩn và tránh duy trì hai tên gây nhầm lẫn. |
| Kiểm tra lint/validate HTML-CSS | Cần cải thiện | Chưa có kết quả từ validator, linter hoặc quy trình kiểm tra chất lượng mã. |

### 3.6 Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn triển khai và môi trường mục tiêu | Cần cải thiện | Chưa có hướng dẫn hosting, cấu hình domain hoặc quy trình phát hành được xác nhận. |
| Kiểm thử trên bản triển khai | Cần cải thiện | Chưa có URL môi trường kiểm thử hay kết quả xác nhận trên bản triển khai. |
| Minh chứng giao diện | Cần cải thiện | Repository có ảnh responsive desktop, tablet và mobile trong `docs/`; cần xác nhận ảnh được tạo từ bản hiện tại và bổ sung thông tin kích thước/trình duyệt. |
| Kịch bản và kết quả kiểm thử | Chưa đạt | Chưa có nhật ký chạy test hoặc kết quả pass/fail; báo cáo này là rà soát tĩnh, không phải biên bản thực thi kiểm thử. |
| Khả năng lặp lại kiểm thử | Cần cải thiện | Cần ghi lại bước chạy, thiết bị/trình duyệt, dữ liệu đầu vào và kết quả để người nhận có thể tái kiểm tra. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm đã có nền tảng portfolio tĩnh với các khu vực nội dung chính, stylesheet riêng, ảnh cục bộ và định hướng responsive. Tuy nhiên, đánh giá hiện tại chỉ dựa trên rà soát tĩnh; chưa có kết quả chạy thử trên trình duyệt, kiểm thử tương thích, đo hiệu năng hoặc xác nhận triển khai. Vì vậy, sản phẩm **chưa đủ căn cứ để kết luận sẵn sàng bàn giao**.

### Vấn đề cần ưu tiên khắc phục

1. Thay các liên kết `#` bằng địa chỉ dự án/mạng xã hội thực tế hoặc bỏ liên kết nếu chưa có đích; sửa liên kết email thành `mailto:`.
2. Đồng bộ tên Nguyễn Thanh Tùng trong metadata, nội dung hiển thị và thuộc tính `alt`.
3. Chạy kiểm thử chức năng và giao diện trên desktop, tablet, mobile; xác nhận các ảnh/CSS tải thành công và ghi lại trình duyệt, thiết bị cùng kết quả.
4. Bổ sung hướng dẫn chạy/triển khai, kịch bản kiểm thử và kết quả thực thi để bàn giao có thể tái lập.
5. Xác nhận email có được phép công khai và thực hiện kiểm tra bảo mật, cấu hình trên toàn repository trước khi phát hành.
6. Chuẩn hóa tên tệp release note, xác nhận nội dung tài liệu và bổ sung kết quả lint/validate nếu nằm trong tiêu chí bàn giao.

### Khuyến nghị quyết định bàn giao

**Khuyến nghị: Chưa bàn giao chính thức.** Có thể chuyển sang vòng xác nhận cuối sau khi xử lý các lỗi nội dung/liên kết và hoàn thành kiểm thử thực tế, cung cấp minh chứng cùng thông tin môi trường triển khai.