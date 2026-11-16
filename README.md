# E-commerce UI Improvement

## 1. Giới thiệu
Trang web minh họa cải tiến **thẻ sản phẩm** trong danh sách sản phẩm, lấy cảm hứng từ cách tổ chức giao diện của Tiki (không sao chép mã nguồn hay hình ảnh của Tiki): hiển thị rõ hình ảnh, tên, giá bán, giá gốc, % giảm giá và nút "Thêm vào giỏ", hiển thị tốt trên máy tính và điện thoại.

## 2. Website tham khảo
- Tên website: Tiki
- URL: https://tiki.vn
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng

## 3. Chức năng
- Hiển thị danh sách sản phẩm dạng lưới.
- Hiển thị tên và giá sản phẩm (giá bán nổi bật, giá gốc gạch ngang, nhãn % giảm).
- Bố cục hỗ trợ nhiều kích thước màn hình (máy tính: nhiều cột, điện thoại: 2 cột).

## 4. Công nghệ
- HTML5
- CSS3

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt.

## 6. Cải tiến đã thực hiện
**Vấn đề ban đầu:** Những gì em quan sát:

Giá bán **3.090.000** hiển thị chữ lớn, màu đỏ, nổi bật nhất trong khu vực giá.

Bên cạnh là nhãn **-48%** chữ nhỏ trên nền xanh nhạt, rồi giá gốc **5.990.000₫** chữ nhỏ, màu xám, gạch ngang, kèm biểu tượng thông tin (i).

Nhãn giảm giá và giá gốc nằm cùng một dòng với giá bán nên khách nhìn được ngay, nhưng cả hai đều nhỏ và nhạt hơn nhiều so với giá bán.

Cột bên phải có nút **Mua ngay** (đỏ), **Thêm vào giỏ** và **Mua trước trả sau** (viền xanh), kèm Số lượng và Tạm tính.

Phía dưới có khung ưu đãi và thông tin vận chuyển (Giao siêu tốc 2h, phí giao).

**Điểm hợp lý:**

- Giá bán chữ to, màu đỏ nên nhìn vào là thấy ngay.
- Giá gốc gạch ngang nằm cạnh giá bán, nhìn là biết đang giảm.
- Bên phải có nút Mua ngay, Thêm vào giỏ, số lượng và tạm tính nên mua rất tiện.

**Điểm có thể cải thiện:**

1. Nhãn giảm giá “-48%” hơi nhỏ và nhạt. Giảm gần một nửa là thông tin rất quan trọng, nhưng nhãn lại nhỏ hơn nhiều so với giá bán nên dễ bị bỏ qua.
2. Cách ghi tiền chưa đồng nhất. Giá bán “3.090.000” không có chữ ₫, còn giá gốc và tạm tính thì có. Nhìn hơi thiếu thống nhất.
3. Chỉ có % chứ chưa ghi số tiền tiết kiệm. Nếu ghi thêm “Tiết kiệm 2.900.000₫” thì khách dễ hình dung hơn là chỉ thấy 48%.
4. Biểu tượng (i) cạnh giá gốc không có chữ giải thích. Khách không biết bấm vào sẽ xem gì.
5. Hai nút “Thêm vào giỏ” và “Mua trước trả sau” có kiểu giống hệt nhau (cùng viền xanh) nên khó phân biệt nhanh.

**Đề xuất của em và lý do:**  
Em chọn thiết kế lại thẻ sản phẩm để: nhãn giảm giá màu đỏ, chữ trắng, đặt ở góc ảnh cho dễ thấy; giá bán to nhất; giá gốc gạch ngang nằm ngay cạnh; ghi ₫ thống nhất; nút “Thêm vào giỏ” đủ lớn để bấm trên điện thoại. Làm vậy khách so sánh giá giữa nhiều sản phẩm sẽ nhanh hơn.

**Thay đổi:**
- Giá bán to, màu đỏ; giá gốc nhỏ, màu xám, gạch ngang (`<del>`).
- Nhãn % giảm giá đặt trên góc ảnh; sản phẩm không giảm giá thì không hiện nhãn.
- Thẻ có thêm nhãn "Chính hãng", "Giao siêu tốc 2H", điểm đánh giá, số đã bán và dòng "Tiết kiệm …₫" (tham khảo các thông tin em thấy trên trang chi tiết của Tiki).
- Lưới `grid` + `auto-fill` cho máy tính, `@media (max-width: 600px)` chuyển 2 cột cho điện thoại.
- Tên sản phẩm giới hạn 2 dòng, nút luôn nằm đáy thẻ nên các thẻ đều nhau.
- Nút cao tối thiểu 44px để dễ chạm; có viền focus khi dùng bàn phím.

## 7. Hỗ trợ từ AI
Em dùng claude.ai để đề xuất bố cục và tạo mã HTML/CSS ban đầu. Em đã tự mở trang trên Chrome, kiểm tra ở kích thước máy tính và điện thoại, và chỉnh sửa: . Chi tiết trong `AI_USAGE.md`.
