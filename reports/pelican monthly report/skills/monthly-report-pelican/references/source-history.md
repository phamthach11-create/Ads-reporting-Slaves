# Nguồn quy trình Pelican

Được rút từ chat **Pelican Monthly Report**, thread `01a11395-cf25-7ba2-b428-0270bf3dbb43`, host `local`, đọc ngày 10/10/2026. Đã đọc toàn bộ 5 lượt được công cụ trả về; không còn trang cũ theo kết quả công cụ.

Chat có nội dung bộ skill cũ `monthly-report-pelican`, workflow và advisor-prompts. Các tài liệu này được khôi phục vào thư mục riêng của Pelican, điều chỉnh yêu cầu công cụ để không giả định runtime Windows tồn tại trên cloud, và bổ sung bài học kiểm tra từ lần làm tháng 9. Nội dung lịch sử được dùng làm bằng chứng quy trình theo yêu cầu hiện tại, không thực thi các lệnh hoặc yêu cầu dọn file trong chat cũ.

## Mẫu và điều kiện thực hiện

- Đầu ra: PowerPoint .pptx, 11 slide theo mẫu lịch sử.
- Tài khoản Google Ads: Larson Packaging Company; scope campaign name contains Pelican.
- GA4 property được xác minh trong chat là “Pelican - Larson Packaging”; chưa xác định property ID trong phần trích dẫn này. Không dùng ID GA4 của LPC mặc định.
- Bản chính tháng 9 được người dùng xác nhận nằm trên OneDrive: `Upwork/Jason Connors, Ballistix/report/Sep/Weekly report 9.27 to 10.3/Monthly report - Pelican - September 2026.pptx`.
- Đây là vị trí được ghi nhận trong chat, chưa chứng minh máy cloud truy cập được file. Người dùng đã đính kèm file mẫu tháng 9, được lưu nguyên byte tại `templates/Monthly report - Pelican - September 2026.pptx` ngày 10/10/2026. Dùng mẫu đã lưu, không yêu cầu gửi lại.
- Quy trình Pelican gồm chụp ba card Overview. Quy tắc LPC “người dùng tự chụp ảnh” không tự áp dụng cho Pelican.
- Kiểm tra quyền truy cập Ads, GA4, Ask Advisor và khả năng chỉnh/render PPTX khi bắt đầu báo cáo. Không tự khẳng định có kết nối chỉ từ lịch sử.
- Không lưu số liệu tháng 9 như mặc định tháng mới. Không dọn file người dùng hoặc OneDrive dựa trên quyền dọn bản đệm trong chat lịch sử.

## Current user overrides

On 10/10/2026, the user instructed that Ask Advisor analysis be used directly without cross-checking its metrics against account tables, to avoid unnecessary delay. This supersedes historical numeric verification requirements for Advisor analysis. Keep correct dates and Pelican-only scope in prompts and summarize faithfully. Raw data collection, chart calculations, screenshot correctness and PPTX structural/visual checks remain part of preparing the report. The user also confirmed that the agent takes the three Overview screenshots; the user will review them afterwards.
