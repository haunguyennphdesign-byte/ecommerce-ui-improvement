# AI Usage Log

## 1. Công cụ AI
Tên công cụ: claude.ai (Claude, Anthropic)

## 2. Mục đích sử dụng
Đề xuất bố cục thẻ sản phẩm và hỗ trợ tạo mã HTML/CSS ban đầu; tạo ảnh minh họa đơn giản.

## 3. Prompt đã sử dụng
Prompt 1:
-Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử  
bằng HTML5 và CSS3.

Tôi muốn cải tiến khu vực: thẻ sản phẩm.

Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam.

Hãy đề xuất:  
1. Bố cục giao diện.  
2. Các thành phần HTML cần sử dụng.  
3. Cách tổ chức CSS.  
4. Cách hiển thị trên máy tính và điện thoại.  
5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế.  
Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.

Prompt 2: Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện  
thương mại điện tử bằng HTML5 và CSS3.

Yêu cầu:  
- Giao diện có tiêu đề và khu vực sản phẩm.  
- Có tối thiểu 4 sản phẩm mẫu.  
- Mỗi sản phẩm có hình ảnh, tên, giá và nút thao tác.  
- Bố cục phù hợp với màn hình máy tính và điện thoại.  
- Mã HTML có cấu trúc rõ ràng.  
- CSS được tách thành file riêng.  
- Không sử dụng backend hoặc cơ sở dữ liệu.  
- Không đưa thư viện hoặc thành phần không cần thiết vào dự án.

Giải thích cách chạy trang web và những phần tôi cần kiểm tra.

## 4. Kết quả AI đề xuất
- Cấu trúc `index.html` dùng `<ul>/<li>` cho danh sách sản phẩm, mỗi thẻ gồm ảnh, nhãn giảm giá, tên, giá, nút.
- `css/style.css` dùng CSS Grid, biến màu `:root`, media query cho điện thoại.
- 6 ảnh minh họa tự tạo (không dùng ảnh có bản quyền).

## 5. Kiểm tra và điều chỉnh
- Đã mở `index.html` trên Chrome, kiểm tra bằng DevTools ở 1366px, 768px, 375px.
- Đã kiểm tra % giảm: 590.000→413.000 (30%), 249.000→199.000 (20%), 480.000→360.000 (25%), 320.000→256.000 (20%), 400.000→340.000 (15%).
- Điểm tôi tự phát hiện và chỉnh sửa: 

## 6. Phần tôi hiểu và có thể giải thích
- `display: grid` + `repeat(auto-fill, minmax(220px, 1fr))`: tự chia số cột theo độ rộng màn hình.
- `@media (max-width: 600px)`: ép 2 cột và thu nhỏ chữ trên điện thoại.
- `position: relative` (ảnh) + `position: absolute` (nhãn giảm giá): đặt nhãn lên góc ảnh.
- `<del>` + `.price-old`: giá gốc gạch ngang.
- `aspect-ratio: 1/1` + `object-fit: cover`: mọi ảnh cùng kích thước, không méo.
- `margin-top: auto` trong thẻ dạng flex cột: nút luôn nằm đáy thẻ.
