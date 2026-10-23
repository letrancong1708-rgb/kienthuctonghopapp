KIẾN THỨC TỔNG HỢP — BẢN SỬA PWA BUILDER

1. Giải nén ZIP. Tải TOÀN BỘ nội dung trong thư mục Kienthuc-tonghop-main lên đúng thư mục website đang chạy (ghi đè index.html, manifest.json; tải thêm toàn bộ icon và sw.js).
2. Giữ nguyên cấu trúc thư mục books/ và books.json.
3. Mở website bằng HTTPS. Kiểm tra các URL /manifest.json, /icon-192.png, /icon-512.png và /sw.js (nếu website ở thư mục con thì kiểm tra theo đường dẫn thư mục con).
4. Mở lại PWABuilder, chạy kiểm tra lại. Nếu vẫn báo lỗi cũ, làm mới trang/đợi cache cập nhật rồi quét lại.
5. Trong PWABuilder, chọn Publish/Package -> Android (tên mục có thể khác), tạo APK và tải APK đã ký.

Ghi chú: Service worker dùng online-first và cache các GET cùng domain thành công để hỗ trợ dự phòng; đây không phải cam kết toàn bộ nội dung hoạt động offline.
