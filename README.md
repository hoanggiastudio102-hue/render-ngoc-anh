# VIDEO GLOBAL — công cụ dựng video độc lập

Bản mới đã bỏ Google Flow và cột video thứ ba. Mỗi cảnh còn một ô ảnh/tư liệu gốc và một ô video thay thế; giao diện gọn hơn, không chạy Chrome hay hàng đợi tạo video AI.

## Tải bộ cài

- [Windows 64-bit](https://github.com/hoanggiastudio102-hue/render-ngoc-anh/releases/latest/download/VIDEO-GLOBAL-WINDOWS-DOC-LAP-20261002-r2.zip) — Intel/AMD, có sẵn Python và FFmpeg.
- [Mac Apple Silicon](https://github.com/hoanggiastudio102-hue/render-ngoc-anh/releases/latest/download/VIDEO-GLOBAL-MAC-DOC-LAP-20261002-r2.zip) — ARM64, chạy setup.sh lần đầu.
- [Mã SHA-256](https://github.com/hoanggiastudio102-hue/render-ngoc-anh/releases/latest/download/SHA256SUMS.txt).

Bộ cài nằm trong Releases. Nút Code → Download ZIP chỉ tải tài liệu của kho GitHub.

## Cách chạy

**Windows:** giải nén toàn bộ ZIP vào thư mục cố định rồi mở MO-VIDEO-GLOBAL.cmd. Tự tạo tài khoản quản trị và mật khẩu riêng. Không cần cài Python, Node.js hoặc đăng nhập Google Flow.

**Mac:** dùng Apple Silicon và Python ARM64. Cài Homebrew từ https://brew.sh nếu chưa có; mở Terminal, gõ bash rồi kéo setup.sh vào và Enter. Sau đó mở Mở VIDEO GLOBAL.command, hoặc chạy bash start.sh nếu Finder chặn. Setup kiểm tra/cài Python và FFmpeg có libass. Giữ Terminal đang chạy khi render.

Đặt âm thanh, SRT và ảnh/video vào KHO-TU-LIEU/BAI_001 hoặc thêm kho riêng trong Quản lý kho. Chọn kênh/bài → chọn âm thanh/SRT cùng tên → sửa cảnh → Lưu Video. Thành phẩm mặc định ở VIDEO-XUAT; có thể chọn thư mục riêng.

## Các tính năng giữ lại

Chọn bài/kênh, kho nhiều thư mục, chọn đúng âm thanh/SRT theo bài, dịch và giọng đọc, hai ô tư liệu, bộ lọc từ khóa, random, điền video theo thứ tự, gộp/tách cảnh, cảnh chèn, cắt video, hiệu ứng/chuyển động ảnh, phụ đề, xem trước, nháp tự lưu, quản lý tài khoản/phân quyền, thống kê và cấu hình lưu video. Các kết nối quản lý máy/Drive không được cấu hình sẵn tới hệ thống khác.

Nháp cũ đang chọn video ở cột thứ ba được chuyển sang cột video còn lại, giữ đoạn cắt và thời gian cảnh. Những lựa chọn cũ khác được giữ trong dữ liệu nháp; file gốc trong kho không bị xóa. Video đã tạo được vẫn dùng như video thông thường.

## Dữ liệu và kiểm chứng

ZIP sạch không chứa tài khoản, mật khẩu, token, hồ sơ Chrome/Google, dữ liệu bài, danh mục kênh riêng, địa chỉ website công ty hoặc cấu hình ghép máy. Ứng dụng mặc định chỉ nghe trên localhost. Tự cấu hình các dịch vụ online và tài khoản của chính bạn nếu cần.

Windows đã kiểm tra tạo tài khoản mới, giữ tài khoản sau khởi động lại, xuất MP4 bằng NVIDIA NVENC/CPU, khớp âm thanh sau gộp/chèn cảnh và lưu bản sao đúng thư mục. Đã kiểm tra chuyển nháp ba cột sang hai cột và chặn API Flow cũ. Mac đã kiểm tra mã, cú pháp và tính toàn vẹn gói; chưa chạy trên phần cứng Mac.

Giữ .data, .cache, kho tư liệu và thư mục thành phẩm khi sử dụng. Không gửi thư mục đã đăng nhập cho người khác; hãy gửi ZIP gốc trong Releases. Khi cập nhật bản đang dùng, sao lưu dữ liệu trước và dùng đúng bộ cài độc lập, không dùng bộ cài nhân viên ghép máy.
