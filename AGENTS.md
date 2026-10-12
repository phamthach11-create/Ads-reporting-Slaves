# Báo cáo trong repository

Repository này lưu nhiều báo cáo. Mỗi báo cáo có một thư mục riêng trong `reports/` và bộ skill riêng trong thư mục đó.

Khi người dùng yêu cầu làm LPC monthly report, đọc `reports/lpc monthly report/skills/lpc-monthly-report/SKILL.md` và các tài liệu được dẫn trong đó trước khi thực hiện.

Khi người dùng yêu cầu làm Pelican monthly report, đọc `reports/pelican monthly report/skills/monthly-report-pelican/SKILL.md` và các tài liệu được dẫn trong đó. Pelican có quy trình PowerPoint riêng; không dùng skill LPC cho Pelican.

Lưu đầu ra theo tháng, giữ nguyên các báo cáo cũ. Không tự suy đoán dữ liệu, định nghĩa chỉ số hoặc quy trình từ những cuộc trò chuyện không có trong ngữ cảnh hiện tại. Không lưu mật khẩu hoặc API key vào repository.

Mỗi báo cáo mới phải có thư mục riêng `reports/<tên báo cáo>/`, với skill, context, mẫu, dữ liệu, mã và đầu ra nằm trong thư mục đó. Chỉ áp dụng skill LPC cho LPC monthly report; không dùng quy tắc hoặc dữ liệu LPC cho báo cáo khác. Hướng dẫn ở gốc chỉ dùng để định tuyến và quy ước chung.


## Quy tắc chung sau bàn giao mọi báo cáo

Đọc và áp dụng `skills/report-delivery-cleanup/SKILL.md` khi làm bất kỳ báo cáo nào. Sau khi bàn giao bản final, hỏi người dùng báo cáo đã xong chưa. Khi người dùng xác nhận xong, rà soát và khai báo các file phát sinh (nháp, raw data tải về, file tạm và các file khác), kèm đường dẫn thư mục lưu và dung lượng nếu có, để người dùng chọn giữ hoặc xóa. Xác nhận xong không phải quyền xóa; chỉ xóa các file người dùng lựa chọn rõ ràng. Giữ bản final và các tài nguyên tái sử dụng không được chỉ định xóa. Quy tắc này áp dụng cả các loại báo cáo thêm sau này.
