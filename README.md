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

  
## 1. Các thành phần của mô hình CSP
- **Biến (Variables - $X$):** 81 ô trống trên lưới Sudoku (được định danh từ A1 đến I9).
- **Miền giá trị (Domains - $D$):** Tập hợp các số nguyên từ $\{1, 2, 3, 4, 5, 6, 7, 8, 9\}$. Ô đã có số sẽ có miền giá trị chỉ chứa duy nhất số đó.
- **Ràng buộc (Constraints - $C$):**
  - **Hàng (Rows):** 9 ô trong cùng một hàng phải có giá trị khác nhau.
  - **Cột (Columns):** 9 ô trong cùng một cột phải có giá trị khác nhau.
  - **Khối (Blocks 3x3):** 9 ô trong mỗi vùng 3x3 phải có giá trị khác nhau.

## 2. Thuật toán AC-3 (Arc Consistency)
- **Mục tiêu:** Thiết lập tính nhất quán cung để cắt tỉa miền giá trị trước khi bắt đầu tìm kiếm sâu.
- **Nguyên lý:** Kiểm tra mọi cặp ô có quan hệ ràng buộc (neighbors). Nếu một giá trị trong miền của ô $A$ không có giá trị tương ứng nào ở ô $B$ thỏa mãn ràng buộc, giá trị đó sẽ bị loại bỏ khỏi $A$.
- **Hiệu quả:** Loại bỏ hơn 90% các trường hợp sai lầm ngay từ bước tiền xử lý.

## 3. Backtracking Search kết hợp Heuristics
Khi AC-3 không thể suy diễn thêm, thuật toán sẽ thực hiện tìm kiếm đệ quy kết hợp với các kỹ thuật thông minh:
- **MRV (Minimum Remaining Values):** Luôn ưu tiên chọn ô có ít lựa chọn nhất (miền giá trị nhỏ nhất) để thử nghiệm. Điều này giúp nhanh chóng tìm ra lời giải hoặc phát hiện sớm các nhánh vô nghiệm.
- **Inference (Forward Checking):** Mỗi khi gán một số vào ô, thuật toán ngay lập tức lan truyền ràng buộc để loại bỏ số đó khỏi các ô hàng xóm, giúp ngăn chặn xung đột từ sớm.

## 4. Quy trình giải tổng quát
1. **Parse:** Chuyển chuỗi 81 ký tự thành đối tượng CSP.
2. **Pre-process:** Chạy AC-3 để lọc miền giá trị dựa trên các số đã biết.
3. **Search:** Sử dụng Recursive Backtracking để lấp đầy các ô trống còn lại.
4. **Output:** Xuất kết quả dưới dạng chuỗi hoặc hiển thị lên lưới giao diện (GUI).
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



