# Thiệp web phát sáng

## Mở bằng Visual Studio Code
1. Giải nén hoặc mở thư mục chứa `index.html` trong VS Code.
2. Cài extension **Live Server**.
3. Nhấp phải `index.html` → **Open with Live Server** để xem trang trên máy.
4. Sửa lời nhắn trực tiếp trong `index.html` (tìm cụm `Cảm ơn em` hoặc `Em là`). Lưu file để Live Server tự cập nhật.

## Dùng mã QR trên điện thoại
Mã QR cần trỏ tới một địa chỉ web công khai. Khi mới mở bằng Live Server, địa chỉ thường chỉ dùng được trên máy tính.

Có thể đăng trang tĩnh miễn phí bằng GitHub Pages:
1. Đưa `index.html` lên một repository GitHub.
2. Trong repository, vào **Settings → Pages**.
3. Chọn nhánh `main` và thư mục `/ (root)`, rồi lưu.
4. Mở đường dẫn GitHub Pages được cung cấp trên điện thoại và nhấn **Tạo mã QR**.

Nút QR sử dụng dịch vụ QRServer khi trang đã có địa chỉ web. Nội dung thiệp vẫn hiển thị nếu không tải được dịch vụ QR.

## Thay ảnh và lời nhắn trong album
1. Trong thư mục `outputs`, tạo thư mục mới tên `images`.
2. Chép ảnh của bạn vào đó, ví dụ `anh-1.jpg`.
3. Mở `index.html` trong VS Code và tìm `const slides`.
4. Mỗi mục có `image`, `title`, `text`. Ví dụ:

```js
{image:'images/anh-1.jpg',title:'Một ngày thật dịu dàng',text:'Lời nhắn của bạn ở đây.'}
```

Để thêm ảnh, sao chép một mục trong danh sách rồi đổi tên tệp và chữ. Album tự chạy từng ảnh; sau ảnh cuối, thiệp thu nhỏ như hộp quà và quay lại bìa. Nút **Tiếp theo** cũng cho phép chuyển ảnh thủ công.

## Màn ảnh trôi màu hồng
Sau màn trái tim có cánh, 8 khung ảnh trôi từ dưới lên với bóng bay gắn phía trên. Chạm giữ và kéo từng tấm ảnh để di chuyển.

Trong `index.html`, tìm `const carouselPhotos` để thay ảnh và chú thích. Chép ảnh vào `outputs/images`, rồi điền đường dẫn, ví dụ `{image:'images/anh-1.jpg',caption:'Kỷ niệm của chúng mình'}`. Nếu `image` để trống, trang sẽ hiện khung mẫu.

Tám ảnh được rải đều và bay lên lần lượt; trên điện thoại mỗi tấm thu gọn để giữ đủ viền.


## Màn cuối gửi lời cảm ơn
Sau 8 tấm ảnh trôi lên có gắn bóng bay, nhấn **Lời cảm ơn ♡** để mở trang cảm ơn nền tối với tấm thiệp màu kem. Album và chuyển màn đã được làm mềm hơn, bố cục ảnh tự co lại trên điện thoại. Có thể sửa nội dung trong phần `id="stage6"` của `index.html`. Khung lời nhắn hiện chỉ lưu trên thiết bị đang mở, không gửi qua mạng.

