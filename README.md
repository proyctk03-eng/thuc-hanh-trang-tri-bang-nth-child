# Thực Hành: Trang Trí Bảng Biểu với :nth-child() (Hiệu Ứng Zebra Striping)

## 1. Mục tiêu bài thực hành
- Áp dụng pseudo-class `:nth-child()` với các giá trị `even` hoặc `odd`.
- Chọn và định dạng các hàng chẵn/lẻ trong một bảng biểu để tạo hiệu ứng "ngựa vằn" (zebra striping).
- Tăng cường khả năng đọc dữ liệu trên các bảng có nhiều dòng, giúp mắt không bị "lạc dòng".
- Kết hợp với pseudo-class `:hover` để làm nổi bật dòng người dùng đang di chuột tới.

---

## 2. Các bước thực hiện
1. **Chuẩn bị cấu trúc HTML (`timetable.html` / `index.html`):**
   - Tạo bảng biểu thời khóa biểu tuần chuẩn Semantic với `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`.
   - Liên kết file `style.css` vào thẻ `<head>`.
2. **Định dạng cơ bản cho bảng (`table`, `th`, `td`, `thead th`):**
   - Đặt `width: 80%`, `margin: 40px auto` để căn giữa.
   - Sử dụng `border-collapse: collapse` để gộp các đường viền.
   - Thêm `border: 1px solid #ddd; padding: 12px` cho các ô dữ liệu.
   - Nổi bật hàng tiêu đề với `thead th { background-color: #007bff; color: white; }`.
3. **Áp dụng hiệu ứng Zebra Striping với `:nth-child()`:**
   - Sử dụng bộ chọn: `tbody tr:nth-child(even)` tô màu nền `#f2f2f2` cho các hàng chẵn (hàng 2, 4, 6, 8...).
   - (Mở rộng) Khi đổi sang `tbody tr:nth-child(odd)` sẽ áp dụng cho các hàng lẻ.
4. **Tương tác nâng cao với `:hover`:**
   - Thêm quy tắc `tbody tr:hover { background-color: #e2e2e2; }` để làm sáng rõ hàng khi di chuột qua.

---

## 3. Mã nguồn CSS cốt lõi
```css
/* Hiệu ứng Ngựa vằn cho các hàng chẵn */
tbody tr:nth-child(even) {
  background-color: #f2f2f2;
}

/* Hiệu ứng Hover làm nổi bật hàng khi di chuột */
tbody tr:hover {
  background-color: #e2e2e2;
}
```
