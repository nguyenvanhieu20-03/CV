# Portfolio CV — Nguyễn Văn Hiếu

Trang portfolio/CV cá nhân giới thiệu Nguyễn Văn Hiếu, các kỹ năng Frontend, một số dự án tiêu biểu và thông tin liên hệ. Giao diện được xây dựng theo hướng tối giản, responsive và hỗ trợ tiếng Việt.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày kỹ năng dưới dạng danh sách và dự án dưới dạng thẻ.
- Hiển thị ảnh đại diện và thông tin liên hệ.
- Bố cục thích ứng với màn hình điện thoại, máy tính bảng và máy tính.

Các thẻ dự án hiện là nội dung giới thiệu mẫu. Liên kết “Xem chi tiết” chưa trỏ đến trang dự án. Portfolio hiện là website tĩnh, không có backend hoặc chức năng gửi biểu mẫu.

## Công nghệ

- **HTML5:** cấu trúc nội dung và các vùng ngữ nghĩa.
- **CSS3:** tạo kiểu, responsive, Flexbox và CSS Grid.
- **Nginx (tùy chọn):** phục vụ website khi chạy bằng Docker.

Website hiện không cần JavaScript để hiển thị và không sử dụng công cụ build, framework hay thư viện bên ngoài.

## Yêu cầu môi trường

### Chạy trực tiếp

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để chạy qua máy chủ cục bộ: Python 3 (hoặc một máy chủ tĩnh tương đương).
- Không cần cài Node.js, npm hay cơ sở dữ liệu.

### Chạy bằng Docker

- Docker Engine trên Linux, hoặc Docker Desktop trên Windows/macOS.
- Docker daemon đang chạy và có thể tải image `nginx:alpine` trong lần chạy đầu tiên.

## Cài đặt

Tải mã nguồn hoặc clone repository, sau đó chuyển vào thư mục dự án:

```bash
git clone https://github.com/nguyenvanhieu20-03/CV.git
cd CV
```

Nếu bạn đã tải mã nguồn về máy, hãy mở terminal tại thư mục chứa `index.html`.

## Cấu hình nội dung

Đây là website tĩnh nên không có tệp cấu hình môi trường `.env` hoặc bước cài đặt dependency. Có thể chỉnh sửa trực tiếp:

- `index.html`: tên, phần giới thiệu, kỹ năng, dự án và thông tin liên hệ.
- `assets/css/styles.css`: màu sắc, kiểu chữ, khoảng cách và breakpoint responsive.
- `assets/img/avatar.jpg`: ảnh đại diện. Nếu thay ảnh, giữ nguyên tên tệp hoặc cập nhật đường dẫn `src` trong `index.html`.

Trước khi công khai website, hãy thay email mẫu `hieu.nguyen@example.com`, kiểm tra lại đường dẫn GitHub/LinkedIn và cập nhật các liên kết dự án đang để `#`.

## Chạy thử

### Windows (PowerShell)

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, dùng:

```powershell
python -m http.server 8000
```

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Sau khi máy chủ khởi động, mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`. Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác và truy cập đúng cổng đó.

> Có thể mở trực tiếp `index.html` trong trình duyệt để xem giao diện. Dùng máy chủ cục bộ được khuyến nghị để kiểm tra website trong môi trường gần với khi triển khai.

## Chạy bằng Docker

Các lệnh sau chạy Nginx ở foreground, gắn thư mục dự án chỉ-đọc vào web root và phục vụ website tại cổng `8080`. Lần đầu chạy, Docker sẽ tải image `nginx:alpine`.

### Windows (PowerShell)

Chạy tại thư mục dự án:

```powershell
docker run --rm --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS

Chạy tại thư mục dự án:

```bash
docker run --rm --name portfolio-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

### Linux

Chạy tại thư mục dự án:

```bash
docker run --rm --name portfolio-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem website. Dừng container bằng `Ctrl+C`; tùy chọn `--rm` sẽ tự xóa container sau khi dừng. Nếu cổng `8080` đã được sử dụng, đổi phần `8080:80` thành một cổng trống, ví dụ `8081:80`, rồi truy cập cổng mới.

## Thông tin liên hệ

- **Tên:** Nguyễn Văn Hiếu
- **Email:** `hieu.nguyen@example.com` (địa chỉ mẫu, cần cập nhật)
- **GitHub:** [github.com/nguyenvanhieu](https://github.com/nguyenvanhieu) (kiểm tra và cập nhật liên kết trước khi sử dụng)
- **LinkedIn:** [linkedin.com/in/nguyenvanhieu](https://linkedin.com/in/nguyenvanhieu) (kiểm tra và cập nhật liên kết trước khi sử dụng)

## Bản quyền

© 2026 Nguyễn Văn Hiếu.