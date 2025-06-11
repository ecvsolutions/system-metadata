# 📦 System Metadata

**System Metadata** là một kho lưu trữ tập trung các file cấu hình dạng JSON/XML, phục vụ cho việc chia sẻ thông tin tĩnh giữa các hệ thống backend, frontend hoặc dịch vụ bên ngoài.

Mục tiêu của repo là cung cấp một nguồn duy nhất, minh bạch và có thể version hóa cho các metadata công khai (public) như:

- Thông tin các cụm dịch vụ (clusters)
- Danh sách các endpoint API public
- Cấu hình vùng/môi trường
- Metadata phục vụ UI hoặc tài liệu kỹ thuật

---

## 🧩 Mục đích sử dụng

- Cho phép frontend truy cập các cấu hình hệ thống mà không cần hard-code.
- Cho phép backend tham chiếu thông tin cụm hoặc môi trường mà không phụ thuộc cấu hình nội bộ.
- Dễ dàng quản lý và cập nhật thông tin metadata thông qua Git, có thể tích hợp CI/CD để kiểm tra schema.

---

## 📁 Cấu trúc thư mục (ví dụ)

```plaintext
system-metadata/
├── clusters/
│   ├── dev.json
│   ├── staging.json
│   └── prod.json
│
├── public-apis/
│   └── api-list.json
│
└── metadata-schema/
    └── cluster-schema.json
