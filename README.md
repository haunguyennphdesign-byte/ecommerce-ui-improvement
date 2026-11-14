# E-commerce UI Improvement

## 1. Giới thiệu
Dự án cải tiến giao diện một khu vực của website thương mại điện tử, thực hiện cho bài tập cá nhân Chương 1 môn Phát triển ứng dụng WEB/TMĐT (ĐH Kinh tế TP.HCM). Khu vực được cải tiến là **thẻ sản phẩm trong danh sách sản phẩm** (hình ảnh, tên, giá bán, giá gốc, % giảm, nút mua), viết lại bằng HTML5 và CSS3 thuần với bố cục rõ ràng, dễ đọc và tương thích nhiều kích thước màn hình.

## 2. Website tham khảo
- Tên website: Tiki
- URL: https://tiki.vn
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng (khu vực chọn cải tiến: thẻ sản phẩm trong danh sách)

## 3. Chức năng
- Hiển thị danh sách sản phẩm.
- Hiển thị tên và giá sản phẩm, kèm giá gốc gạch ngang và nhãn % giảm giá (nếu có).
- Nút "Thêm vào giỏ" ở mỗi thẻ (chỉ là giao diện, chưa có xử lý).
- Bố cục hỗ trợ nhiều kích thước màn hình (2 / 3 / 4 cột).

## 4. Công nghệ
- HTML5
- CSS3

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt.

## 6. Cải tiến đã thực hiện
**Vấn đề ban đầu:**
- [Điền điều bạn tự quan sát trên Tiki, ví dụ: giá bán, giá gốc và % giảm khó phân biệt; thẻ hiển thị chật trên điện thoại.]

**Thay đổi đã thực hiện:**
- Dùng CSS Grid để chia lưới sản phẩm, tự động tăng/giảm số cột theo chiều rộng màn hình (media query).
- Chuẩn hóa ảnh sản phẩm thành khung vuông; giá bán in đậm màu đỏ, giá gốc nhỏ và gạch ngang, % giảm là nhãn riêng trên ảnh.
- Giới hạn tên sản phẩm 2 dòng và dùng flexbox để nút mua luôn nằm sát đáy thẻ.
- Thêm hiệu ứng hover cho thẻ và nút, thống nhất khoảng cách và font chữ.
- [Điểm bạn tự phát hiện và sửa: ...]

## 7. Hỗ trợ từ AI
**AI hỗ trợ:**
- Gợi ý phương án bố cục và cấu trúc HTML/CSS cho thẻ sản phẩm.
- Tạo mã HTML/CSS ban đầu và giải thích tổng quan cách hoạt động.

**Phần tôi đã kiểm tra, điều chỉnh hoặc bổ sung:**
- Tự chạy thử và kiểm tra giao diện trên các kích thước màn hình khác nhau bằng Chrome DevTools.
- Đối chiếu nhận xét của AI về Tiki với website thực tế, loại bỏ ý chưa kiểm chứng được.
- [Điều chỉnh màu sắc, khoảng cách, nội dung sản phẩm...]

Chi tiết xem thêm trong file `AI_USAGE.md`.
