# Đặc tả LPC monthly report

## Đã xác nhận

- Tên: LPC monthly report.
- Tần suất: hằng tháng.
- Mục tiêu: người dùng yêu cầu qua chat để agent thực hiện báo cáo.
- Mỗi báo cáo có thư mục và bộ skill riêng.
- Mẫu được người dùng cung cấp ngày 10/10/2026: `templates/Monthly report - September 2026 - LPC.xlsx`.
- Đầu ra mẫu là Excel `.xlsx`, gồm 6 sheet; xem `template-structure.md` để biết tên và cấu trúc.
- Giữ file mẫu nguyên vẹn; dùng bản sao khi tạo báo cáo tháng mới.

## Quy trình đã xác nhận

Người dùng xác nhận đã hướng dẫn xong toàn bộ quy trình ngày 10/10/2026. Bộ skill bao phủ cả 6 sheet của mẫu.

Hai sheet pivot được xác nhận ngày 10/10/2026 là các bảng sinh từ raw data, cấp dữ liệu cho biểu đồ `Insight report`; sau khi cập nhật nguồn cần kiểm tra chúng đã cập nhật đúng. Trong mẫu, tên nguồn là `data`, tên bảng là `matched location pivot table` và `Session source pivot table`. Dùng tên/vai trò thay vì số thứ tự được nhắc trong chat. Chi tiết kiểm tra: `../skills/lpc-monthly-report/pivot-tables.md`.

Sheet 4 `data` đã được hướng dẫn ngày 10/10/2026: raw data Traffic acquisition: Session source lấy từ GA4; raw data Matched locations report — Region lấy từ Google Ads theo cách sheet 2. **Matched Location loại subscriber campaigns** trong raw data và mọi phần tổng hợp/biểu đồ/phân tích. Chi tiết: `../skills/lpc-monthly-report/sheet-4-data.md`. Ghi chú này không tự mở rộng thành bộ lọc loại subscriber cho Search terms (sheet 3).

Sheet 3 `search term and keyword` đã được hướng dẫn ngày 10/10/2026: Google Ads → Search terms; tạo column view phù hợp mẫu, chọn tháng báo cáo, lọc **Cost > 0**, trích xuất và cập nhật dữ liệu mới. Chi tiết: `../skills/lpc-monthly-report/sheet-3-search-term-and-keyword.md`.

Sheet 2 `Insight report` đã được hướng dẫn ngày 10/10/2026. GA4 account `30284038`, property `372708254`; Traffic acquisition: Session source / medium, chỉ số Sessions, top 5 + Other, so sánh hai tháng liên tiếp. Audience: người dùng tự chụp ảnh; phân tích dùng Google Ads Ask Advisor (`give me audience analysis`). Matched Location: Google Ads → Insight and report → When and where ads show → Match location → Region, top 3 theo Cost + Other; phân tích ngắn, có thể dùng Advisor (`give me match location analysis`). Giữ format biểu đồ. Chi tiết: `../skills/lpc-monthly-report/sheet-2-insight-report.md`.

Sheet 1 `Larsonpkg` đã được hướng dẫn ngày 10/10/2026: báo cáo tổng quan gồm dữ liệu từ Google Ads, LinkedIn Ads và các nền tảng ads liên quan; phân tích Google Ads dùng Ask Advisor với ba nhóm câu hỏi về performance (tách subscriber campaign và các campaign khác), keyword/search term và competitors. Tóm tắt câu trả lời vào Excel. Quy trình chi tiết và vị trí trong mẫu: `../skills/lpc-monthly-report/sheet-1-larsonpkg.md`. Tài khoản ads cụ thể và quyền truy cập cần được kiểm tra khi thực hiện.

## Điều kiện khi thực hiện

- Xác định tháng báo cáo và đúng tài khoản Google Ads/LinkedIn Ads/các nền tảng liên quan; tái sử dụng quyền truy cập có sẵn. GA4 đã có ID trong quy trình.
- Có quyền đọc dữ liệu và truy cập Ask Advisor; nếu thiếu, báo phần bị chặn và dùng bản xuất/câu trả lời do người dùng cung cấp nếu có.
- Dùng mẫu và quy trình đã lưu, không yêu cầu người dùng hướng dẫn lại toàn bộ. Chỉ hỏi các thông tin thực sự cần và chưa thể xác định từ tài khoản, mẫu hoặc dữ liệu.
- Ảnh Audience Behavior do người dùng tự làm.
- Quy trình đã được ghi nhận; chưa chạy thử tạo báo cáo mới hoặc xác minh quyền truy cập tài khoản. Skill và mẫu được quản lý trong repository, trong thư mục riêng của LPC.

## Quy tắc subscriber bổ sung

Performance phân tích riêng subscriber và các campaign khác. Matched Location và Audience analysis loại subscriber. Nếu đã xác minh subscriber không hoạt động trong toàn bộ kỳ, có thể bỏ phần nhắc subscriber trong câu hỏi Ask Advisor; không chỉ dựa vào trạng thái Paused hiện tại.

## Campaign không có chi tiêu

Quy tắc chung xác nhận ngày 11/10/2026: Mọi campaign có Cost = 0 trong khoảng thời gian báo cáo được coi là không chạy trong kỳ và không hiển thị trong báo cáo, bất kể loại campaign hoặc trạng thái hiện tại. Chỉ trình bày campaign có Cost > 0. Giữ dữ liệu gốc và tổng nguồn để đối soát; cập nhật công thức và biểu đồ theo các campaign còn lại. Quy trình chi tiết được duy trì tại `../skills/lpc-monthly-report/sheet-1-larsonpkg.md`, mục `Campaign không có chi tiêu`.
