# AI Usage Log

## 1. Công cụ AI
Tên công cụ: Claude (Anthropic)

## 2. Mục đích sử dụng
- Lập bảng phân tích 5 khu vực của website tham khảo (tiki.vn) dưới dạng giả thuyết để tự kiểm chứng.
- Đề xuất bố cục thẻ sản phẩm (hình ảnh, tên, giá bán, giá gốc, % giảm, nút mua).
- Tạo mã HTML/CSS ban đầu và giải thích tổng quan cách hoạt động.

## 3. Prompt đã sử dụng
- **Prompt 1 (phân tích website):** dùng đúng mẫu trong đề, với website là tiki.vn và 5 khu vực: trang chủ, danh mục sản phẩm, chi tiết sản phẩm, tìm kiếm, giỏ hàng.
- **Prompt 2 (đề xuất giao diện):** [dán prompt thực tế bạn đã dùng, hoặc ghi lại yêu cầu: cải tiến thẻ sản phẩm, hiển thị giá gốc/giá khuyến mãi/% giảm, đối tượng là khách mua sắm trực tuyến tại Việt Nam]
- **Prompt 3 (tạo mã nguồn):** [dán prompt thực tế: trang HTML5/CSS3, tối thiểu 4 sản phẩm mẫu, CSS tách file riêng, không backend, không thư viện]

## 4. Kết quả AI đề xuất
- Bảng phân tích 5 khu vực gồm mục đích, thành phần giao diện, điểm thuận tiện, vấn đề có thể phát sinh, đề xuất cải tiến. AI nêu rõ chưa quan sát được tiki.vn nên toàn bộ là đề xuất, không phải quan sát thực tế.
- Phương án thẻ sản phẩm: lưới 2/3/4 cột, giá bán nổi bật, giá gốc gạch ngang, nhãn % giảm trên ảnh, nút mua sát đáy thẻ.
- Bộ mã `index.html` + `css/style.css` + 4 ảnh SVG minh họa.

## 5. Kiểm tra và điều chỉnh
Đánh dấu [x] những mục bạn thực sự đã làm:
- [ ] Mở tiki.vn, đối chiếu từng ý trong bảng phân tích của AI; xóa ý không đúng hoặc không kiểm chứng được.
- [ ] Mở `index.html` bằng Chrome, kiểm tra ở khoảng 375px, 768px và trên 1000px bằng DevTools.
- [ ] Kiểm tra hình ảnh, nội dung, bố cục từng thẻ.
- [ ] Tự sửa ít nhất một điểm: [ghi rõ đã sửa gì, ở file nào, vì sao]
- Phần AI đề xuất nhưng không dùng: [điền, nếu có]

## 6. Phần tôi hiểu và có thể giải thích
- `<ul>/<li>` và `<article>`: danh sách sản phẩm và từng thẻ sản phẩm.
- `<s>`: giá gốc bị gạch; `.badge`: nhãn giảm giá đặt chồng lên ảnh.
- `display: grid` + `repeat(n, 1fr)`: chia cột; `@media (min-width)`: đổi số cột theo màn hình.
- `display: flex` + `margin-top: auto`: đẩy nút mua xuống đáy thẻ để các thẻ thẳng hàng.
- Biến màu trong `:root`: đổi màu toàn bộ giao diện ở một chỗ.
- [Phần bạn đã sửa: giải thích vai trò của đoạn HTML/CSS đó]
