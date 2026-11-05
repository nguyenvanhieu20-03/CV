# Nhật ký thay đổi lớn

Tệp này ghi lại các thay đổi quan trọng của dự án để tiện theo dõi lịch sử và tra cứu. Mỗi khi có thay đổi lớn, hãy bổ sung một mục mới ở đầu phần **Lịch sử thay đổi**, không xóa hoặc sửa các mục cũ trừ khi cần đính chính.

## Khi nào cần ghi log

Ghi log khi thay đổi ảnh hưởng đáng kể đến chức năng, giao diện chính, cấu trúc dự án, công nghệ sử dụng, cách cài đặt/chạy, hoặc khi phát hành một phiên bản mới. Không cần ghi các chỉnh sửa nhỏ như sửa lỗi chính tả hay định dạng.

## Mẫu ghi log

```text
### YYYY-MM-DD — Tên thay đổi
- Phiên bản: x.y.z (nếu có)
- Nội dung: Thay đổi chính và lý do thực hiện.
- Tệp/khu vực ảnh hưởng: Các tệp hoặc thành phần liên quan.
```

## Lịch sử thay đổi

### 2026-11-05 — Bổ sung tài liệu dự án và phát hành v1.0.0

- **Phiên bản:** v1.0.0
- **Nội dung:** Hoàn thiện README tiếng Việt với mô tả dự án, chức năng, công nghệ, yêu cầu môi trường, cấu hình và hướng dẫn chạy trên Windows, macOS, Linux, Docker. Bổ sung release note cho bản phát hành đầu tiên.
- **Tệp/khu vực ảnh hưởng:** `README.md`, `docs/RELEASENOTE.md`.

### 2026-11-05 — Phát hành portfolio CV cá nhân

- **Phiên bản:** v1.0.0
- **Nội dung:** Xây dựng website portfolio tĩnh với các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ; giao diện responsive dùng HTML5 và CSS3.
- **Tệp/khu vực ảnh hưởng:** `index.html`, `assets/css/styles.css`, `assets/img/avatar.jpg`.