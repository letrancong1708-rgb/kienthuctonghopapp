KIẾN THỨC TỔNG HỢP — TẠO APK OFFLINE BẰNG GITHUB ACTIONS

Dự án được đóng gói bằng Capacitor: website và các file JSON trong thư mục www/ được nhúng trực tiếp vào APK. Sau khi cài đặt, nội dung có sẵn trong gói chạy không cần Internet. Các tính năng phụ thuộc dịch vụ ngoài (nếu có) vẫn có thể cần mạng.

CÁCH DÙNG
1. Giải nén ZIP này. Tạo repository GitHub mới (hoặc cập nhật repository hiện tại) và tải toàn bộ nội dung bên trong thư mục Kienthuc-tonghop-main lên repository.
2. Đảm bảo file .github/workflows/android-apk.yml nằm đúng đường dẫn trong repository và nhánh chính là main hoặc master.
3. Mở GitHub → repository → tab Actions → chọn “Build Android APK (Offline)” → Run workflow. Có thể đợi workflow tự chạy sau khi push lên main/master.
4. Khi workflow xanh (Success), mở lần chạy đó → phần Artifacts → tải “Kien-thuc-tong-hop-offline-debug-apk.zip”. Giải nén và lấy app-debug.apk.
5. Chuyển APK sang Android và cài đặt. Có thể cần bật quyền “Cài ứng dụng không rõ nguồn gốc” cho ứng dụng quản lý tệp/trình duyệt bạn dùng.

CẬP NHẬT NỘI DUNG
- Sửa các file website trong www/; sửa dữ liệu sách trong www/books/ và danh mục trong www/books.json.
- Commit/push lên main hoặc master; GitHub Actions sẽ build APK mới.
- Lưu ý: nếu chỉ sửa file gốc bên ngoài www/, nội dung ứng dụng không tự cập nhật; cần cập nhật bản tương ứng trong www/.

LƯU Ý QUAN TRỌNG
- Đây là APK debug để thử nghiệm/cài trực tiếp, chưa phải bản release đã ký để phát hành rộng rãi.
- APK chứa nội dung offline có tại thời điểm build; cập nhật nội dung mới cần build và cài APK mới.
- Phông chữ Google trong website có thể không tải khi offline; hệ thống sẽ dùng phông chữ dự phòng.
- Nếu repository dùng tên nhánh khác, sửa branches trong workflow cho đúng.
- Nếu GitHub Actions báo lỗi, mở log của bước thất bại và gửi log để sửa tiếp.
