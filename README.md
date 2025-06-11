# 📦 System Metadata

**System Metadata** là kho lưu trữ tập trung các file cấu hình dạng **JSON**/**YAML**, phục vụ cho việc chia sẻ metadata giữa các hệ thống **backend**, **frontend**, hoặc các dịch vụ tích hợp.

Repo này hướng tới việc chuẩn hóa, version hóa và công khai các thông tin tĩnh của hệ thống dưới dạng dữ liệu có cấu trúc.

- Thông tin các cụm dịch vụ (clusters)
- Danh sách các endpoint API public
- Cấu hình vùng/môi trường
- Metadata phục vụ UI hoặc tài liệu kỹ thuật

---

## 🧩 Mục đích sử dụng

- Cung cấp metadata tĩnh, công khai, để các hệ thống có thể dễ dàng truy cập mà không cần phụ thuộc vào backend riêng.
- Là nơi lưu trữ các cấu hình của:
  - Thông tin cụm dịch vụ (clusters)
  - Endpoint API public
  - Cấu hình môi trường
  - **Các worker được data hóa bằng JSON/YAML** dùng cho **Kastra** hoặc các hệ thống **flow/workflow engine**
  - Metadata phục vụ cho UI động hoặc tài liệu hệ thống

---

## 📁 Cấu trúc thư mục (ví dụ)

```plaintext
system-metadata/
├── project-a/
│   ├── clusters/
│   │   ├── dev.json
│   │   └── prod.json
│   ├── workflows/
│   │   ├── kastra/
│   │   │   └── order-processing.yaml
│   │   └── other/
│   │       └── audit-log-flow.json
│   └── public-apis/
│       └── api-list.json
│
├── project-b/
│   └── clusters/
│       └── staging.json
│
├── metadata-schema/
│   └── cluster-schema.json
│
├── company-profile.json
├── contact-info.yaml
└── README.md
```
