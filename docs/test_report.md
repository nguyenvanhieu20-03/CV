# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio CV cá nhân — Nguyễn Văn Hiếu |
| Phiên bản đối chiếu | v1.0.0 |
| Ngày kiểm thử | 05/11/2026 |
| Người thực hiện/đánh giá | QA/QC — rà soát mã nguồn, tài liệu và kiểm tra trang triển khai; chưa ghi nhận danh tính cá nhân |
| Phạm vi | `index.html`, `assets/css/styles.css`, README, release note và cấu trúc repository |
| Phương pháp | Rà soát tĩnh, mở trang GitHub Pages và đối chiếu mã nguồn; kiểm tra responsive bằng ảnh chụp viewport |
| Môi trường kiểm thử | Chrome headless; viewport mục tiêu 390×2400, 820×2400 và 1440×2400 px; phiên bản trình duyệt chưa ghi nhận |

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ mã nguồn hoặc minh chứng kiểm thử đã ghi nhận.
- **Chưa đạt:** Có lỗi hoặc yêu cầu chưa được đáp ứng.
- **Cần cải thiện:** Có một phần đáp ứng, nhưng còn thiếu xác minh, minh chứng hoặc cần hoàn thiện trước khi bàn giao.

> Báo cáo này phản ánh rà soát tĩnh tại thời điểm lập báo cáo. Không xem các mục chưa chạy thực tế là đã kiểm thử thành công.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Có các phần nội dung chính và điều hướng nội bộ; liên kết dự án, thông tin liên hệ và metadata còn là mẫu/chưa nhất quán. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Có ảnh kiểm tra ở ba viewport; chưa kiểm thử trên thiết bị thật, các trình duyệt khác hoặc đánh giá tương phản/khả năng tiếp cận đầy đủ. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | README có hướng dẫn chạy máy chủ tĩnh; chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra xử lý lỗi. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy backend, dữ liệu người dùng hoặc bí mật cấu hình trong phạm vi rà soát; cần cập nhật dữ liệu mẫu và gia cố liên kết mở tab mới. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có cấu trúc HTML/CSS và tài liệu cơ bản; còn metadata sai tên, thông tin mẫu và chưa có kiểm tra tự động/minh chứng đầy đủ. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Trang `/CV/` hoạt động, nhưng repository/URL `/my-cv` được cung cấp không có nội dung và trả về 404; Docker và pipeline chưa được xác minh. |

## 3. Nội dung chi tiết theo tiêu chí

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Các section tương ứng có trong `index.html`; điều hướng nội bộ trỏ đến `#about`, `#skills`, `#projects`, `#contact`. |
| Nút điều hướng và liên kết trong trang | Cần cải thiện | Các liên kết đến section có đích tương ứng. Bốn liên kết “Xem chi tiết” đang dùng `href="#"`, chưa mở dự án. |
| Thông tin dự án và kỹ năng | Cần cải thiện | Có bốn thẻ dự án và danh sách kỹ năng; nội dung được ghi nhận là mẫu, chưa xác minh tính chính xác so với hồ sơ thực. |
| Thông tin nhận diện nhất quán | Chưa đạt | Tiêu đề trang và nội dung chính ghi Nguyễn Văn Hiếu, nhưng metadata `description` và `author` ghi Nguyễn Văn An; ký hiệu thương hiệu đang là chữ “A”. |
| Thông tin liên hệ sử dụng được | Cần cải thiện | Email `hieu.nguyen@example.com` và liên kết GitHub/LinkedIn cần được xác nhận. Liên kết GitHub trong HTML hiện là `#`. |
| Kiểm tra hành vi trên trình duyệt | Cần cải thiện | Chưa có kết quả chạy các thao tác điều hướng, nhấn email hoặc kiểm tra liên kết ngoài trên trình duyệt. |

### 3.2 Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục responsive theo kích thước màn hình | Cần cải thiện | CSS khai báo mobile-first, breakpoint từ 768px và 1280px; đã chụp trang triển khai ở 390px, 820px và 1440px. Ảnh cho thấy bố cục theo từng viewport; chưa kiểm tra trên thiết bị thật hoặc toàn bộ ma trận trình duyệt. |
| Điều hướng bàn phím và trạng thái focus | Đạt | Có kiểu `:focus-visible` trong stylesheet. Chưa thực hiện kiểm thử thao tác bàn phím hoặc trình đọc màn hình. |
| Hỗ trợ giảm chuyển động | Đạt | Có `prefers-reduced-motion: reduce` để tắt transition, animation và cuộn mượt. |
| Khả năng đọc và tương phản màu | Cần cải thiện | Chưa đo tương phản màu hoặc đánh giá trên các thiết bị khác nhau; cần kiểm tra đặc biệt màu chữ phụ và màu thương hiệu. |
| Ảnh và văn bản thay thế | Cần cải thiện | Ảnh đại diện có `alt`, nhưng nội dung alt dùng “Hieu” không dấu. Ảnh minh họa dự án có mô tả; chưa kiểm tra tải ảnh và hiển thị thực tế. |
| Tương thích Chrome, Firefox, Edge, Safari và thiết bị di động | Cần cải thiện | Chưa có ma trận trình duyệt/thiết bị hoặc kết quả kiểm thử chéo. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Hướng dẫn chạy cục bộ | Đạt | README có lệnh Python HTTP server cho Windows, macOS và Linux. Chưa ghi nhận kết quả chạy thực tế. |
| Tải trang và tài nguyên cục bộ | Cần cải thiện | Mã HTML tham chiếu stylesheet và ảnh đại diện trong repository; chưa xác minh phản hồi HTTP hoặc tải tài nguyên khi chạy. |
| Hành vi khi thiếu tài nguyên hoặc cổng đã được sử dụng | Cần cải thiện | README có lưu ý đổi cổng nếu cổng mặc định đang bận; chưa có kiểm thử tình huống lỗi hoặc hướng dẫn xử lý lỗi tải tài nguyên. |
| Hiệu năng tải trang | Cần cải thiện | Không thấy JavaScript hoặc bước build trong phạm vi rà soát, nhưng chưa đo thời gian tải, kích thước tài nguyên hay chỉ số Lighthouse/Web Vitals. |
| Khả năng phục hồi/backend | Đạt | Phù hợp với phạm vi website tĩnh: không thấy backend hoặc dịch vụ dữ liệu bắt buộc. Đây không phải xác nhận về độ sẵn sàng của hạ tầng hosting. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bí mật và cấu hình môi trường | Đạt | Trong phạm vi repository đã xem, không thấy `.env`, thông tin xác thực hoặc cấu hình bí mật; website được mô tả là không cần backend. Chưa thực hiện quét bí mật tự động. |
| Thu thập/lưu trữ dữ liệu người dùng | Đạt | Không thấy biểu mẫu gửi dữ liệu hoặc logic lưu dữ liệu người dùng trong trang tĩnh hiện tại. |
| Liên kết ngoài mở tab mới | Cần cải thiện | Liên kết LinkedIn dùng `target="_blank"` nhưng chưa khai báo `rel="noopener noreferrer"`. |
| Dữ liệu liên hệ công khai | Cần cải thiện | Email và một số URL đang là thông tin mẫu. Xác nhận chủ sở hữu đồng ý công khai trước khi triển khai. |
| HTTPS, headers và cấu hình máy chủ | Cần cải thiện | Chưa có môi trường hosting/cấu hình máy chủ để kiểm tra HTTPS, security headers hoặc quyền truy cập. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc HTML và CSS tách biệt | Đạt | `index.html` liên kết stylesheet riêng tại `assets/css/styles.css`; nội dung có các vùng HTML ngữ nghĩa như `header`, `nav`, `main`, `section`, `footer`. |
| Tổ chức tài nguyên dự án | Đạt | Thư mục `assets` chứa CSS và ảnh đại diện; tài liệu dự án nằm trong `docs`. |
| Metadata và nội dung trang | Chưa đạt | `meta description` và `meta author` mang tên Nguyễn Văn An, không khớp tên Nguyễn Văn Hiếu ở tiêu đề/trang. |
| README và hướng dẫn vận hành | Đạt | README có mô tả, công nghệ, yêu cầu, cấu hình nội dung và hướng dẫn chạy trực tiếp/Docker cho các hệ điều hành chính. |
| Release note và quản lý thay đổi | Đạt | Có release note v1.0.0 và nhật ký thay đổi lớn; nội dung cần đồng bộ với các chỉnh sửa tiếp theo nếu có. |
| Kiểm tra chất lượng tự động | Cần cải thiện | Không thấy cấu hình lint, kiểm thử tự động hoặc CI trong repository đã rà soát. |

### 3.6 Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Hướng dẫn triển khai/chạy bằng Docker | Cần cải thiện | Trang GitHub Pages tại `https://nguyenvanhieu20-03.github.io/CV/` đã mở được; README hướng dẫn Docker nhưng chưa có kết quả Docker build/run. URL theo repository `my-cv` trả về 404. |
| Chạy thử trên Windows, macOS và Linux | Cần cải thiện | Có hướng dẫn lệnh tương ứng trong README nhưng chưa có biên bản xác nhận chạy trên từng hệ điều hành. |
| Bộ kiểm thử và kết quả thực thi | Cần cải thiện | Chưa thấy test suite hoặc kết quả kiểm thử chức năng, giao diện, trình duyệt và hiệu năng. |
| Minh chứng trực quan | Cần cải thiện | Bổ sung ảnh responsive trong `docs/screenshots/`; cần tiếp tục lưu kết quả smoke test và kiểm thử trên trình duyệt/thiết bị khác. |
| Khả năng lặp lại và bàn giao | Cần cải thiện | Có hướng dẫn cơ bản; cần bổ sung phiên bản môi trường, kết quả thực thi và quy trình triển khai đã xác minh để người nhận có thể tái lập. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm hiện đáp ứng ở mức nền tảng cho một portfolio tĩnh: có các khu vực nội dung chính, stylesheet riêng, bố cục responsive được khai báo và tài liệu hướng dẫn chạy. Tuy nhiên, đây mới là **đánh giá tĩnh**, chưa có minh chứng chạy trên trình duyệt hoặc môi trường Docker. Do còn metadata sai tên, liên kết/nội dung mẫu và các nhóm kiểm thử thực thi chưa được xác minh, sản phẩm **chưa nên được xác nhận sẵn sàng bàn giao chính thức** cho đến khi hoàn thành các việc cần làm dưới đây.

### Vấn đề cần xử lý trước bàn giao

1. **Ưu tiên cao:** Sửa metadata `description`/`author`, ký hiệu thương hiệu và nội dung nhận diện để thống nhất với chủ sở hữu portfolio.
2. **Ưu tiên cao:** Thay và xác nhận email, GitHub, LinkedIn; thay các liên kết dự án `#` bằng URL hợp lệ hoặc thể hiện rõ dự án chưa có liên kết.
3. **Ưu tiên cao:** Chạy smoke test trên trình duyệt ở mobile, tablet và desktop; kiểm tra điều hướng, ảnh, liên kết email/ngoài và ghi lại trình duyệt/phiên bản đã dùng.
4. **Ưu tiên trung bình:** Bổ sung `rel="noopener noreferrer"` cho liên kết mở tab mới; xác minh nội dung liên hệ được phép công khai.
5. **Ưu tiên trung bình:** Kiểm tra khả năng tiếp cận cơ bản, tương phản màu, thao tác bàn phím và nội dung `alt`.
6. **Ưu tiên trung bình:** Chạy Docker theo README và ghi lại kết quả; cân nhắc bổ sung Dockerfile/Compose nếu cần triển khai lặp lại.
7. **Ưu tiên trung bình:** Thu thập minh chứng (ảnh chụp màn hình, kết quả smoke test và kết quả đo hiệu năng cơ bản) và lưu trong thư mục tài liệu bàn giao.

### Kết luận bàn giao

- **Trạng thái hiện tại:** Cần cải thiện trước khi bàn giao.
- **Điều kiện đề nghị đóng kiểm thử:** Hoàn thành các mục ưu tiên cao; thống nhất repository/URL triển khai; thực hiện smoke test trên các kích thước màn hình mục tiêu và Docker (nếu chọn triển khai Docker); cập nhật minh chứng và kết quả vào báo cáo.
- **Kết quả đã xác minh:** Trang GitHub Pages tại `/CV/` mở được và hiển thị portfolio; mã `index.html` trên GitHub có cùng blob SHA với tệp local tại thời điểm đối chiếu; đã chụp giao diện ở ba viewport. Các kiểm tra chưa nêu kết quả vẫn chưa được thực hiện.

## 5. Nhật ký kiểm thử và minh chứng

| Mã | Hạng mục | Kết quả | Minh chứng/Đường dẫn |
|---|---|---|---|
| DOC-01 | Rà soát cấu trúc HTML/CSS và tài liệu | Đã rà soát tĩnh | `index.html`, `assets/css/styles.css`, `README.md`, `docs/RELEASENOTE.md` |
| LIVE-01 | Mở trang GitHub Pages | Đạt trên URL `/CV/`; URL `/my-cv/` trả về 404 | [GitHub Pages CV](https://nguyenvanhieu20-03.github.io/CV/); [repository my-cv](https://github.com/nguyenvanhieu20-03/my-cv) |
| SRC-01 | Đối chiếu HTML local với repository GitHub CV | Đạt cho `index.html` | Git blob SHA local và GitHub đều là `cb0cc75c3a1a0ea3fcff09a7cafa425997f4aab7` |
| RUN-01 | Smoke test trang trên trình duyệt | Đạt: trang tải và hiển thị các khu vực chính | GitHub Pages CV; bản chụp viewport trong `docs/screenshots/` |
| DOCKER-01 | Chạy website bằng Docker | Chưa thực hiện/không có kết quả ghi nhận | Chưa có |
| UI-01 | Kiểm tra giao diện ở ba viewport | Đã chụp ở 390px, 820px và 1440px; chưa kiểm tra thiết bị thật | [Mobile](./screenshots/responsive-mobile.png), [Tablet](./screenshots/responsive-tablet.png), [Desktop](./screenshots/responsive-desktop.png) |
| PERF-01 | Đo hiệu năng cơ bản | Chưa thực hiện/không có kết quả ghi nhận | Chưa có |

## 6. Chấm điểm theo rubric A2.2

Điểm dưới đây là **đánh giá tạm thời theo bằng chứng hiện có**, quy đổi trên tổng trọng số 100 điểm. Mục demo chưa được cung cấp nên tạm tính 0 điểm; điểm mục này cần cập nhật sau khi xem phần trình bày thực tế.

| Tiêu chí | Trọng số | Điểm tạm tính | Nhận xét và bằng chứng |
|---|---:|---:|---|
| **A2.2.TC1** — Repository rõ ràng, tối thiểu 3 commit, thông điệp hợp lý và thể hiện quá trình sửa lỗi | 20% | **10/20** | Cấu trúc source rõ ràng. Local có 3 commit nhưng GitHub `CV` hiện chỉ có 2 commit; commit thứ ba đang ở local và chưa đẩy lên remote. Các commit hiện có chủ yếu thêm nội dung/tài liệu, chưa thể hiện rõ một commit sửa lỗi và xác minh sau sửa. |
| **A2.2.TC2** — README chuyên nghiệp, AI_LOG thể hiện trách nhiệm học thuật và đối chiếu thực tế | 15% | **10/15** | README hướng dẫn dự án và cách chạy khá đầy đủ; AI_LOG có ghi lịch sử thay đổi. Nhật ký chưa nêu rõ phần việc có AI hỗ trợ, phần người học tự thực hiện/kiểm chứng, nguồn tham khảo và kết quả đối chiếu thực tế. |
| **A2.2.TC3** — GitHub Pages hoạt động, khớp repository và có minh chứng | 30% | **15/30** | `https://nguyenvanhieu20-03.github.io/CV/` tải được; SHA của `index.html` local khớp blob SHA trên GitHub. Tuy nhiên repository `my-cv` được cung cấp hiện rỗng và URL Pages `/my-cv/` trả về 404; cần thống nhất repo được chấm và URL triển khai. |
| **A2.2.TC4** — Release note v1.0, thay đổi rõ, luồng end-to-end được kiểm chứng | 20% | **10/20** | Có release note v1.0.0 nêu chức năng và hạn chế. Đã xác minh luồng tải trang GitHub Pages và ghi nhận ảnh responsive, nhưng chưa có biên bản end-to-end đầy đủ cho các luồng chức năng, liên hệ và triển khai Docker. |
| **A2.2.TC5** — Demo mạch lạc, giải thích quyết định kỹ thuật, giới hạn và trả lời đúng trọng tâm | 15% | **0/15 (tạm tính)** | Chưa có video, kịch bản demo hoặc buổi trình bày để đánh giá. Đây là điểm tạm theo minh chứng chưa được cung cấp, không phải kết luận về năng lực trình bày. |
| **Tổng điểm tạm thời** | **100%** | **45/100** | Cần đẩy commit còn thiếu, làm rõ repo/URL Pages, bổ sung bằng chứng kiểm thử end-to-end và cung cấp demo để chấm lại. |

### Ưu tiên cải thiện để nâng điểm

1. Đẩy commit thứ ba lên đúng repository được chấm; bổ sung commit sửa lỗi thực tế với thông điệp mô tả thay đổi và cách xác minh, không tạo commit chỉ để đủ số lượng.
2. Chọn một repository làm nguồn chính. Nếu dùng `CV`, cập nhật liên kết bàn giao tới `https://nguyenvanhieu20-03.github.io/CV/`; nếu dùng `my-cv`, đẩy source và cấu hình GitHub Pages để URL tương ứng hoạt động.
3. Bổ sung AI_LOG trung thực: nêu phần có AI hỗ trợ, phần người học tự làm/biên tập, những nội dung đã kiểm chứng và các nguồn tham khảo thực tế; không ghi nhận hoạt động chưa thực hiện.
4. Ghi một kịch bản end-to-end có bước thao tác, kết quả mong đợi/thực tế và minh chứng; bao gồm mở trang, điều hướng, kiểm tra liên hệ và triển khai đã chọn.
5. Chuẩn bị demo ngắn: giới thiệu chức năng, giải thích HTML/CSS responsive, các quyết định kỹ thuật, hạn chế còn lại và trả lời theo đúng câu hỏi.