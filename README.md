# [Bài tập] Phối màu cho Newsletter (Newsletter Color Harmony)

## 📌 Giới thiệu & Mục tiêu
Bài tập thực hành kỹ năng phối màu sắc trong thiết kế trải nghiệm người dùng (UX) và giao diện người dùng (UI):
- Luyện tập sử dụng công cụ **Adobe Color** (`https://color.adobe.com/`) để khám phá và lựa chọn các bộ màu sắc hài hòa.
- Xây dựng khung Newsletter chuẩn responsive dựa trên **Bootstrap 5.3.3** với hệ thống biến màu CSS (`:root`).
- Triển khai **2 phiên bản Newsletter** mang hai ngôn ngữ thị giác và cảm xúc hoàn toàn khác biệt.

---

## 🎨 1. Phân Tích Chi Tiết 2 Bộ Màu Từ Adobe Color

### Phiên Bản 1: "Trello Ocean Breeze" (Năng Suất, Tập Trung & Tin Cậy)
Lấy cảm hứng từ giao diện quản lý công việc của Trello / Atlassian, áp dụng quy tắc phối màu **Analogous (Tương đồng)** kết hợp điểm nhấn **Complementary (Bổ túc)**:

| Thành phần | Tên màu | Mã HEX | Giá trị RGB | Vai trò thiết kế UI/UX |
| :--- | :--- | :---: | :---: | :--- |
| **Primary** | Trello Blue | `#0079BF` | `rgb(0, 121, 191)` | Nền Header chính, nút kêu gọi hành động CTA, tiêu đề chính. Tạo cảm giác tin cậy, an toàn, ổn định. |
| **Darker Primary** | Deep Ocean | `#026AA7` | `rgb(2, 106, 167)` | Trạng thái Hover của nút bấm và liên kết. |
| **Secondary** | Deep Navy Slate | `#253858` | `rgb(37, 56, 88)` | Nền Footer, khối tính năng tự động hóa (Butler). Mang vẻ chuyên nghiệp của các sản phẩm công nghệ lớn. |
| **Accent** | Growth Green | `#61BD4F` | `rgb(97, 189, 79)` | Khối tính năng Power-Ups, nút dùng thử Premium. Biểu trưng cho sự phát triển, hoàn thành công việc và tiến độ. |
| **Neutral BG** | Light Canvas | `#F4F5F7` | `rgb(244, 245, 247)` | Nền tổng thể newsletter dịu mắt, tăng độ tương phản cho văn bản. |
| **Text** | Charcoal Navy | `#172B4D` | `rgb(23, 43, 77)` | Màu chữ chính, đạt chuẩn tương phản cao WCAG AAA. |

---

### Phiên Bản 2: "Creative Sunset Energy" (Sáng Tạo, Đam Mê & Nhiệt Huyết)
Áp dụng quy tắc phối màu **Triad (Bộ ba)** kết hợp **Split-Complementary (Bổ túc tách)** để tạo ra sự phá cách, khơi dậy nguồn năng lượng và trí tưởng tượng:

| Thành phần | Tên màu | Mã HEX | Giá trị RGB | Vai trò thiết kế UI/UX |
| :--- | :--- | :---: | :---: | :--- |
| **Primary** | Violet Purple | `#7C3AED` | `rgb(124, 58, 237)` | Nền Header chính, nút kêu gọi hành động. Thể hiện tính hiện đại, tư duy đột phá, sáng tạo. |
| **Darker Primary** | Deep Violet | `#6D28D9` | `rgb(109, 40, 217)` | Trạng thái Hover của nút bấm. |
| **Secondary** | Rose Berry | `#BE185D` | `rgb(190, 24, 93)` | Nền Footer, khối tính năng Bảng ý tưởng (Brainstorming). Mang lại sự nhiệt huyết, đam mê, cá tính mạnh mẽ. |
| **Accent** | Sunset Amber | `#F59E0B` | `rgb(245, 158, 11)` | Khối tính năng Cảm xúc nhóm, nút đăng ký miễn phí. Thu hút ánh nhìn ngay lập tức (High Conversion CTA). |
| **Neutral BG** | Warm Cream | `#FFFBEB` | `rgb(255, 251, 235)` | Nền ấm áp, gần gũi, thân thiện hơn nền trắng lạnh. |
| **Text** | Indigo Black | `#1E1B4B` | `rgb(30, 27, 75)` | Màu chữ tím đen sắc nét, dễ đọc. |

---

## 📂 2. Cấu Trúc Dự Án

```
newsletter-color-palette/
├── index.html                   # Trang tổng quan so sánh 2 bản tin cạnh nhau (Side-by-side & Tabs)
├── newsletter_version1.html     # Phiên bản 1 hoàn chỉnh (Trello Ocean Breeze)
├── newsletter_version2.html     # Phiên bản 2 hoàn chỉnh (Creative Sunset Energy)
├── css/
│   ├── style-v1.css             # Định nghĩa biến CSS và lớp tiện ích cho Phiên bản 1
│   └── style-v2.css             # Định nghĩa biến CSS và lớp tiện ích cho Phiên bản 2
├── .gitignore                   # Loại trừ các file rác hệ thống
└── README.md                    # Tài liệu báo cáo chi tiết
```

---

## 🚀 3. Hướng Dẫn Sử Dụng & Trải Nghiệm

1. Clone kho lưu trữ về máy:
   ```bash
   git clone https://github.com/dtc245200862-dot/newsletter-color-palette.git
   ```
2. Mở file `index.html` bằng trình duyệt (Chrome, Edge, Firefox):
   - Bạn có thể xem trực quan hai bản tin đặt cạnh nhau ở chế độ **"So sánh song song"**.
   - Hoặc chuyển qua lại giữa các tab **"Chỉ xem Bản 1"** và **"Chỉ xem Bản 2"**.
   - Có thể mở trực tiếp từng file `newsletter_version1.html` và `newsletter_version2.html` độc lập.
