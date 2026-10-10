# LPC monthly report

Thư mục dành riêng cho báo cáo LPC hằng tháng. Người dùng có thể yêu cầu: “Làm LPC monthly report tháng 09/2026”. Agent sẽ đọc skill riêng, kiểm tra nguồn dữ liệu và tạo báo cáo theo quy trình đã được lưu.

## Cấu trúc

- `skills/lpc-monthly-report/SKILL.md`: hướng dẫn thực hiện.
- `context/report-spec.md`: nguồn dữ liệu, chỉ số và mẫu báo cáo được xác nhận.
- `data/YYYY-MM/`: dữ liệu đầu vào theo tháng.
- `scripts/`: mã xử lý tái sử dụng khi quy trình đã rõ.
- `output/YYYY-MM/`: báo cáo và bằng chứng kiểm tra theo tháng.

## Trạng thái

Đã lưu mẫu Excel tháng 9/2026 trong `templates/` và ghi cấu trúc trong `context/template-structure.md`. Người dùng đã hướng dẫn xong quy trình cả 6 sheet ngày 10/10/2026. Bộ skill đã lưu quy trình lấy dữ liệu, phân tích, cập nhật biểu đồ và kiểm tra bảng pivot. Khi thực hiện, cần tháng báo cáo và quyền truy cập đúng tài khoản ads/GA4/Ask Advisor. Ảnh Audience Behavior do người dùng tự làm. Chưa chạy thử báo cáo tháng mới; skill và mẫu được quản lý trong repository, cùng thư mục riêng của LPC.
