KIẾN THỨC TỔNG HỢP — TỰ CẬP NHẬT SÁCH VÀ ĐỌC OFFLINE

CƠ CHẾ
- Khi online, ứng dụng kiểm tra books.json trên website và tải các file sách JSON về IndexedDB của điện thoại.
- Khi offline, ứng dụng đọc bản sách đã lưu trong IndexedDB.
- Khi có mạng trở lại, ứng dụng tự kiểm tra lại danh mục và nội dung sách.
- Thêm sách mới: tải file JSON mới lên hosting, thêm mục vào books.json, triển khai website; app sẽ phát hiện ở lần đồng bộ tiếp theo.
- Các sách đã tải vẫn dùng được khi mất mạng. Sách mới cần có mạng ít nhất một lần để tải về thiết bị.

QUAN TRỌNG — CẤU HÌNH URL CHO APK
1. Mở index.html (và đồng bộ nội dung đó trong thư mục www/index.html).
2. Tìm dòng: var REMOTE_BASE_URL = "https://YOUR-WEBSITE-DOMAIN/";
3. Thay bằng địa chỉ HTTPS thật của website, ví dụ: https://ten-website.vercel.app/ (giữ dấu / cuối URL).
4. Commit/push toàn bộ dự án lên GitHub. Vào Actions chạy workflow để tạo APK mới.

Nếu để nguyên YOUR-WEBSITE-DOMAIN, APK vẫn đọc sách đã đóng gói trong app nhưng sẽ không thể biết URL máy chủ thật để tự cập nhật.

LƯU Ý
- Đây là đồng bộ tự động khi app đang mở và có mạng; không bảo đảm tải nền khi app đã bị Android đóng.
- Trình duyệt/WebView phải cho phép HTTPS và máy chủ cần công khai books.json cùng thư mục books/.
- Sách được lưu theo từng thiết bị; xóa dữ liệu ứng dụng có thể xóa bản offline.
