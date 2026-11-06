# Báo cáo kiểm thử trước bàn giao

## 1. Tiêu đề báo cáo & Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | My-CV — Portfolio cá nhân |
| Phiên bản | v1.0 |
| Ngày kiểm thử | 06/11/2026 |
| Người thực hiện/đánh giá | Chưa cung cấp |
| Phạm vi | Rà soát tĩnh mã nguồn HTML/CSS và tài liệu dự án |
| Môi trường kiểm thử | Chưa ghi nhận phiên bản trình duyệt, hệ điều hành hoặc cấu hình máy |
| Phương pháp | Đối chiếu cấu trúc và nội dung repository; chưa thực hiện kiểm thử tương tác trên trình duyệt, đa thiết bị hoặc Docker |

> **Lưu ý:** Đây là báo cáo rà soát sơ bộ dựa trên mã nguồn và tài liệu hiện có, không phải xác nhận đã chạy toàn bộ test. Các hạng mục chưa có minh chứng chạy thực tế được đánh dấu **Cần cải thiện** và cần được kiểm tra trước khi nghiệm thu.

### Quy ước trạng thái

- **Đạt:** Có thể xác minh từ mã nguồn/tài liệu trong phạm vi rà soát.
- **Chưa đạt:** Có lỗi hoặc thiếu sót đã xác định, cần khắc phục.
- **Cần cải thiện:** Chưa có đủ minh chứng kiểm thử hoặc cần hoàn thiện thêm trước khi kết luận.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các khu vực nội dung chính hiện diện; cần kiểm tra điều hướng, liên kết và nội dung thực tế trên trình duyệt. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | CSS có khai báo responsive; chưa có kết quả kiểm thử ở các kích thước màn hình/trình duyệt. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Dự án tĩnh, có hướng dẫn chạy; chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra lỗi tải tài nguyên. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy backend hoặc dữ liệu bí mật trong phạm vi rà soát; chưa thực hiện kiểm thử bảo mật/cấu hình triển khai. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Chưa đạt | Phát hiện lỗi cấu trúc nội dung HTML; cần sửa và rà soát lại các liên kết placeholder. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Có hướng dẫn chạy trực tiếp và Docker; chưa có biên bản chạy thử, ảnh chụp hoặc log kiểm thử. |

## 3. Nội dung chi tiết từng tiêu chí

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Các section và liên kết điều hướng tương ứng có trong [`index.html`](../index.html). |
| Menu điều hướng đến đúng section | Cần cải thiện | Có anchor `#about`, `#skills`, `#projects`, `#contact`; cần bấm thử trên trình duyệt để xác nhận hành vi. |
| Các liên kết xem chi tiết dự án có đích hoạt động | Chưa đạt | Các nút “Xem chi tiết” đang dùng `href="#"` trong [`index.html`](../index.html); chưa dẫn tới trang/đích dự án. |
| Liên kết email mở đúng ứng dụng email | Chưa đạt | Thuộc tính hiện có khoảng trắng sau `mailto:` (`mailto: trandangquang26102008@gmail.com`) trong [`index.html`](../index.html); cần sửa và thử bằng trình duyệt. |
| Liên kết GitHub và LinkedIn hoạt động | Chưa đạt | Cả hai liên kết đang dùng `href="#"`; nội dung hồ sơ cũng cần xác nhận trong [`index.html`](../index.html). |
| Nội dung và hình ảnh dự án phản ánh sản phẩm thật | Cần cải thiện | Tài liệu dự án ghi nhận một số nội dung là minh họa; cần thay bằng nội dung đã được duyệt trước phát hành. |

### 3.2 Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có khai báo viewport cho thiết bị di động | Đạt | `index.html` khai báo `width=device-width, initial-scale=1.0`. |
| Có quy tắc responsive | Đạt | [`assets/css/styles.css`](../assets/css/styles.css) sử dụng bố cục mobile-first và breakpoint; cần kiểm tra giao diện thực tế ở các kích thước đại diện. |
| Bố cục ở màn hình điện thoại, máy tính bảng và desktop | Cần cải thiện | Chưa có ảnh chụp/kết quả kiểm thử ở các viewport; cần kiểm tra tràn ngang, cắt chữ và khả năng đọc. |
| Khả năng tương thích giữa các trình duyệt | Cần cải thiện | Chưa ghi nhận phiên bản hoặc kết quả trên Chrome, Edge, Firefox, Safari. |
| Hình ảnh và stylesheet tải thành công | Cần cải thiện | Đường dẫn tài nguyên có trong HTML; chưa chạy máy chủ hoặc xác nhận trên Network/Console. |
| Cấu trúc tiêu đề và khả năng truy cập cơ bản | Chưa đạt | Có thẻ tiêu đề dự án viết sai cấu trúc tại một card (`<h3> class="card-title"xinh hom </h3>`) trong [`index.html`](../index.html); cần sửa markup và kiểm tra lại thứ bậc tiêu đề. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Khởi chạy website bằng máy chủ HTTP cục bộ | Cần cải thiện | [`docs/README.md`](./README.md) có hướng dẫn dùng Python HTTP server trên Windows, macOS và Linux; chưa thực thi để xác nhận. |
| Trang tải đầy đủ CSS và hình ảnh | Cần cải thiện | Chưa có log máy chủ hoặc kết quả kiểm tra Console/Network. |
| Xử lý khi tài nguyên hoặc đường dẫn không tồn tại | Cần cải thiện | Chưa thử các tình huống mất ảnh, sai đường dẫn hoặc truy cập route không tồn tại. |
| Hiệu năng tải trang cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước tài nguyên hoặc chỉ số hiệu năng bằng công cụ kiểm thử. |
| Hành vi khi mở trực tiếp bằng `file://` | Cần cải thiện | Tài liệu khuyến nghị chạy qua HTTP; chưa xác nhận riêng hành vi mở trực tiếp. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Không đưa thông tin xác thực/secret vào mã nguồn | Đạt | Trong phạm vi các tệp được rà soát, không thấy cấu hình xác thực hoặc secret; cần rà soát toàn repository trước khi phát hành. |
| Bề mặt xử lý dữ liệu đầu vào | Đạt | Trang hiện là nội dung tĩnh; chưa thấy biểu mẫu, API hoặc backend xử lý dữ liệu người dùng. |
| Dữ liệu liên hệ công khai đúng và được chủ sở hữu cho phép | Cần cải thiện | Trang hiển thị email và hồ sơ cá nhân; cần xác nhận quyền công khai và độ chính xác trước khi bàn giao. |
| Cấu hình triển khai an toàn | Cần cải thiện | Docker dùng image `nginx:alpine` và mount thư mục; chưa kiểm thử cấu hình header, quyền truy cập, cập nhật image hoặc môi trường triển khai thực tế. |
| Kiểm tra phụ thuộc và lỗ hổng | Cần cải thiện | Không có manifest package của ứng dụng theo tài liệu; chưa thực hiện quét image Docker hoặc kiểm tra phụ thuộc môi trường. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Repository có cấu trúc cơ bản dễ nhận biết | Đạt | Có `index.html`, thư mục `assets` và `docs`; stylesheet và hình ảnh được tách riêng. |
| Markup HTML hợp lệ và nhất quán | Chưa đạt | Thẻ tiêu đề card bị sai cú pháp tại [`index.html`](../index.html); phần tên thương hiệu cũng cần rà soát thẻ đóng/mở. |
| Quy ước lớp CSS và khả năng bảo trì | Cần cải thiện | CSS được tách riêng và dùng biến; chưa chạy validator/linter hoặc đánh giá toàn bộ quy ước. |
| Tài liệu mô tả và hướng dẫn cài đặt/chạy | Đạt | [`docs/README.md`](./README.md) mô tả dự án, yêu cầu môi trường và cách chạy đa nền tảng/Docker; cần thực thi lệnh để xác nhận tính chính xác. |
| Release note phản ánh phiên bản | Đạt | [`docs/RELEASENOTE.md`](./RELEASENOTE.md) có phiên bản v1.0, ngày phát hành, chức năng, lỗi đã sửa và hạn chế. |
| Các liên kết và nội dung placeholder đã được xử lý | Chưa đạt | Các liên kết `href="#"`, thông tin hồ sơ và nội dung dự án minh họa còn cần hoàn thiện. |

### 3.6 Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn chạy trên Windows, macOS và Linux | Đạt | Các lệnh Python HTTP server được ghi trong [`docs/README.md`](./README.md); chưa chạy xác minh trên từng hệ điều hành. |
| Có hướng dẫn chạy bằng Docker | Đạt | Tài liệu có lệnh chạy Nginx và ánh xạ cổng; chưa xác minh Docker Engine, mount volume hoặc truy cập HTTP. |
| Có cấu hình build/deploy tự động | Cần cải thiện | Chưa thấy cấu hình CI/CD hoặc pipeline triển khai trong phạm vi repository được rà soát. |
| Có bộ test tự động và kết quả test | Cần cải thiện | Chưa thấy bộ test tự động hoặc báo cáo kết quả chạy test. |
| Có minh chứng nghiệm thu | Chưa đạt | Chưa có ảnh chụp màn hình, log chạy, danh sách môi trường hoặc biên bản kiểm thử đính kèm. |
| Có thể tái hiện kết quả kiểm thử | Cần cải thiện | Cần ghi lại trình duyệt/phiên bản, hệ điều hành, kích thước viewport, lệnh chạy và kết quả tương ứng. |

## 4. Đánh giá tổng kết & Đề xuất

### Nhận định chung

Sản phẩm đã có nền tảng portfolio tĩnh với các phần nội dung chính, stylesheet responsive và tài liệu hướng dẫn chạy. Tuy nhiên, báo cáo này chỉ dựa trên rà soát tĩnh; chưa có minh chứng chạy thử thực tế trên trình duyệt, các hệ điều hành hoặc Docker. Một số lỗi markup và liên kết chưa hoạt động đã được xác định. Vì vậy, sản phẩm **chưa nên xác nhận sẵn sàng bàn giao** cho đến khi xử lý các mục **Chưa đạt** và hoàn thành kiểm thử xác nhận.

### Vấn đề cần khắc phục trước bàn giao

1. Sửa markup thẻ tiêu đề card trong [`index.html`](../index.html) và rà soát các thẻ đóng/mở HTML.
2. Sửa cú pháp liên kết email; thay `href="#"` của GitHub, LinkedIn và các dự án bằng URL chính xác, hoặc hiển thị rõ rằng mục đó chưa khả dụng.
3. Thay nội dung minh họa bằng nội dung dự án đã được duyệt; xác nhận thông tin liên hệ được phép công khai.
4. Chạy thử hướng dẫn Windows, macOS, Linux và Docker; ghi lại kết quả, môi trường và lỗi phát sinh.
5. Kiểm tra giao diện trên các viewport và trình duyệt mục tiêu; xác nhận CSS, ảnh, điều hướng và không có lỗi Console/Network.
6. Bổ sung minh chứng bàn giao: ảnh chụp giao diện, log chạy thử và bảng kết quả kiểm thử đã cập nhật.

### Kết luận nghiệm thu

**Trạng thái đề xuất: Chưa nghiệm thu — cần khắc phục và kiểm thử lại.**

Sau khi hoàn tất các mục trên, cập nhật trạng thái từng checklist bằng kết quả thực tế và đính kèm minh chứng tương ứng trước khi phê duyệt bàn giao.