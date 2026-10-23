KIẾN THỨC TỔNG HỢP - HƯỚNG DẪN TRIỂN KHAI

1. Đưa toàn bộ nội dung thư mục này lên hosting tĩnh (ví dụ Vercel, Netlify hoặc GitHub Pages).
2. Giữ nguyên cấu trúc thư mục books/ và file books.json.
3. Truy cập website qua HTTPS và thử mở từng môn học.
4. Đóng gói URL website bằng BWA Builder để tạo APK Android.

ICON / PWA
- icon-192.png, icon-512.png: icon ứng dụng/PWA.
- icon-maskable-512.png: icon maskable cho Android.
- icon-72.png đến icon-384.png: các kích thước icon bổ sung.
- favicon.svg / favicon.png: favicon trình duyệt.
- apple-touch-icon.png: icon khi thêm website vào màn hình chính iOS.
- manifest.json: tên ứng dụng, màu giao diện, chế độ standalone và icon.

LƯU Ý
- Dự án này được cấu hình theo hướng online; không thêm service worker/offline cache.
- Nếu hosting triển khai ở thư mục con, manifest dùng đường dẫn tương đối để dễ tương thích hơn.
- Trong BWA Builder, hãy đặt icon ứng dụng bằng icon-512.png (hoặc icon-maskable-512.png nếu trường đó yêu cầu maskable).
- Nếu BWA Builder không tự nhận manifest, vẫn có thể chọn icon APK trực tiếp trong phần cấu hình builder.

THÊM SÁCH MỚI
1. Tạo file books/<ten-sach>.json theo cấu trúc các file hiện có.
2. Thêm mục tương ứng vào books.json.
3. Triển khai lại website.
