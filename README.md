# VIDEO GLOBAL — công cụ dựng video độc lập

Bộ cài Windows và Mac dùng tài khoản, kho tư liệu và phiên Google Flow của chính người nhận. Giữ giao diện chọn bài → âm thanh/SRT → sửa cảnh → xuất video, cùng các tính năng của công cụ hiện tại.

## Tải bộ cài

- [Windows 64-bit](../../releases/latest/download/VIDEO-GLOBAL-WINDOWS-DOC-LAP-20261001-r3.zip) — Intel/AMD, có sẵn Python, FFmpeg và Node.js.
- [Mac Apple Silicon](../../releases/latest/download/VIDEO-GLOBAL-MAC-DOC-LAP-20261001-r3.zip) — ARM64, cần chạy `setup.sh` lần đầu.
- [Mã kiểm tra SHA-256](../../releases/latest/download/SHA256SUMS.txt).

Giải nén toàn bộ ZIP vào một thư mục cố định trước khi chạy. Không chạy trực tiếp trong ZIP.

## Windows

1. Mở `MO-VIDEO-GLOBAL.cmd`.
2. Trang cục bộ mở trong trình duyệt; tự tạo tài khoản quản trị và mật khẩu mới.
3. Đưa âm thanh, SRT và ảnh/video vào `KHO-TU-LIEU/BAI_001`, hoặc chọn kho có sẵn tại Quản lý kho.
4. Chọn bài, chỉnh các cảnh, bấm Lưu Video. Mặc định thành phẩm lưu vào `VIDEO-XUAT`; có thể chọn thư mục riêng.

Máy có NVIDIA dùng NVENC khi hỗ trợ; máy khác tự dùng CPU. Không cần cài Python hoặc Node riêng. Google Chrome chỉ cần cho chức năng Flow.

## Mac

1. Dùng Mac Apple Silicon, Python ARM64; không chạy qua Rosetta.
2. Cài Homebrew từ [brew.sh](https://brew.sh) nếu chưa có.
3. Mở Terminal, gõ `bash ` rồi kéo `setup.sh` vào và Enter. Bộ thiết lập kiểm tra/cài Python, FFmpeg có libass và Node.js.
4. Mở `Mở VIDEO GLOBAL.command`. Nếu Finder chặn, mở Terminal tại thư mục bộ cài và chạy `bash start.sh`.
5. Tạo tài khoản quản trị riêng rồi làm việc như Windows.

Mac dùng VideoToolbox khi có, tối đa 6 cảnh song song; khi dùng CPU sẽ giảm số luồng. Giữ cửa sổ đang chạy mở trong lúc làm việc.

## Flow bằng tài khoản của bạn

- Cài Google Chrome. Vào Cài đặt → Flow → Mở / kết nối.
- Đăng nhập Google của chính bạn trong cửa sổ Chrome riêng. Khi vào được Flow, đóng cửa sổ đăng nhập để bộ xử lý tự kết nối lại.
- Phiên được giữ trong hồ sơ riêng của bộ cài. Google vẫn có thể yêu cầu xác nhận lại khi phiên hết hạn.
- Nhập chuyển động mong muốn, chọn cột nhận, tạo video. Hàng đợi hỗ trợ 2–4 tác vụ và nhóm 50 ảnh; có hủy, thời gian chạy và trạng thái lỗi.
- MP4 được kiểm tra đúng cấu hình, lưu cùng thư mục ảnh theo mã bài rồi hiện trong cột đã chọn. Ảnh gốc được giữ nguyên.
- Lỗi nội dung bỏ qua yêu cầu đó; lỗi tài khoản, tín dụng hoặc giao diện lặp lại sẽ tạm dừng để kiểm tra. Trường hợp chưa rõ đã gửi tạo, không tự tạo lại để tránh tính phí trùng.

Flow cần Internet và quyền sử dụng/tín dụng trên tài khoản Google của bạn. Dịch, giọng đọc online, Drive và các kết nối tùy chọn cũng dùng cấu hình do bạn tự cung cấp; bộ cài không chứa thông tin của người gửi.

## Tính năng giữ lại

Chọn bài/kênh, kho nhiều thư mục, âm thanh và SRT, dịch, giọng đọc, ba cột tư liệu, bộ lọc, random và điền video, gộp/tách cảnh, cảnh chèn, cắt video, hiệu ứng/chuyển động, phụ đề, xem trước, nháp tự lưu, quản lý tài khoản/phân quyền, thống kê, cấu hình lưu video và Flow. Các kết nối quản lý máy/Drive có mã chức năng đầy đủ và không được cấu hình sẵn tới hệ thống khác.

## Dữ liệu và kiểm chứng

Bộ ZIP sạch không chứa tài khoản, mật khẩu, token, phiên Google, dữ liệu bài, danh mục kênh riêng, địa chỉ website công ty, cấu hình ghép máy hay lịch sử dự án. Ứng dụng mặc định chỉ nghe trên localhost.

Sau khi dùng, dữ liệu của **bạn** nằm trong `.data`, `.cache`, `FLOW-BRIDGE`, kho tư liệu và thư mục thành phẩm. Giữ các thư mục này để tiếp tục làm việc; không gửi thư mục đã đăng nhập cho người khác. Hãy chia sẻ ZIP gốc trong Releases.

Windows đã thử mở sạch, tạo tài khoản riêng, đăng nhập lại, xuất MP4 bằng GPU và CPU, kiểm tra khớp âm thanh/SRT và lưu đúng thư mục. Đã thử nhận MP4 Flow vào kho/cột bằng dữ liệu thử cục bộ; thử nghiệm này không dùng tài khoản Google hay tạo video trả phí. Bước điều khiển Chrome tự động gặp lỗi kết nối trong phiên công cụ thử nghiệm, nên **chưa xác nhận toàn bộ lượt tạo/tải Flow của bộ cài độc lập**; cần kiểm chứng sau khi người nhận đăng nhập Google trong phiên desktop của họ. Mac đã kiểm tra mã, giao diện chung, cú pháp và tính toàn vẹn gói; **chưa chạy thử trực tiếp trên phần cứng Mac**.
