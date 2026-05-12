# 🧩 Sudoku CSP Solver (AC-3 & Backtracking)

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![AI](https://img.shields.io/badge/Focus-Artificial%20Intelligence-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

Dự án này sử dụng các kỹ thuật trong **Bài toán thỏa mãn ràng buộc (Constraint Satisfaction Problem - CSP)** để giải quyết các bảng Sudoku từ mức độ dễ đến cực khó. Chương trình tích hợp thuật toán **AC-3** để cắt tỉa miền giá trị và **Backtracking Search** kết hợp với chiến lược **MRV (Minimum Remaining Values)** để tìm lời giải tối ưu.

---

## 🚀 Tính năng nổi bật

-   **Thuật toán mạnh mẽ**: Kết hợp AC-3 tiền xử lý và Backtracking đệ quy với Forward Checking.
-   **Xử lý hàng loạt**: Tự động giải đồng thời 145 bảng Sudoku từ Project Euler và Magic Tour.
-   **Giao diện Pro (GUI)**:
    -   Duyệt qua từng bảng bằng nút `Next`/`Prev`.
    -   **Jump to Puzzle**: Nhảy nhanh đến bảng bất kỳ bằng cách nhập số thứ tự.
    -   **Dynamic Source Label**: Hiển thị nguồn dữ liệu (Project Euler hay Magic Tour) theo thời gian thực.
    -   **Clean UI**: Giao diện sáng (Light Mode), phân biệt số đề bài (Xanh đen) và số máy giải (Cam).
-   **Xuất kết quả chuẩn**: Tự động tạo file `solutions.txt` có phân loại Header theo yêu cầu của bài Lab.

---

## 🛠 Cấu trúc thư mục

```text
.
├── data/
│   ├── euler.txt        # 95 bảng từ Project Euler
│   └── magictour.txt    # 50 bảng Sudoku khó nhất (Top 95)
├── csp.py               # Định nghĩa mô hình CSP cho Sudoku
├── search.py            # Chứa thuật toán AC-3 và Backtracking
├── util.py              # Các cấu trúc dữ liệu bổ trợ
├── sudoku.py            # Script chạy chính (Batch processing & Export)
├── gui.py               # Giao diện người dùng đồ họa (Tkinter)
└── README.md            # Tài liệu hướng dẫn này
