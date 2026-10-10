# Sheet 3: search term and keyword

Quy trình do người dùng xác nhận ngày 10/10/2026.

1. Truy cập đúng tài khoản Google Ads, mở phần **Search terms**, chọn toàn bộ tháng báo cáo.
2. Tạo hoặc dùng lại column view phù hợp với sheet mẫu. Các cột theo thứ tự mẫu: Search term, Match type, Campaign, Keyword, CTR, Avg. CPC, Cost, Conv. rate, Conversions, Cost / conv. Nếu trường không được cung cấp cho một loại campaign, giữ trạng thái thiếu/không áp dụng; không bịa keyword.
3. Áp dụng filter **Cost > 0** trước khi xuất dữ liệu. Bỏ các search term có Cost bằng 0; không dùng điều kiện Cost >= 0. Không thêm bộ lọc campaign hoặc conversion chưa được xác nhận.
4. Trích xuất đầy đủ kết quả sau lọc, không chỉ trang đang hiển thị. Lưu bản xuất gốc trong `data/YYYY-MM/` của báo cáo để kiểm tra lại.
5. Thay dữ liệu kỳ cũ trong sheet `search term and keyword` bằng dữ liệu mới, giữ format và thứ tự cột. Cập nhật dòng kỳ báo cáo, filter và số lượng search term theo kết quả thực tế. Mẫu: `A1` là tiêu đề, `A2` là kỳ/filter/số lượng, hàng 3 là tiêu đề cột.
6. Mẫu có các dòng tổng riêng như Total: Account, Total: Performance Max, Total: Filtered search terms. Cập nhật từ dữ liệu tổng tương ứng được Google Ads cung cấp, giữ rõ phạm vi từng dòng. Không coi tổng account hoặc Performance Max là tổng các search term đã lọc. Không giữ số tổng kỳ cũ và không lấy trung bình đơn giản các tỷ lệ.
7. Kiểm tra các dòng search term có Cost > 0, số bản ghi khớp bản xuất và kỳ đúng tháng. Không tính các dòng tiêu đề/tổng vào số search term. Xóa dữ liệu dư kỳ cũ nếu kỳ mới ít dòng hơn, không xóa các phần khác của workbook.

Sheet này là dữ liệu trích xuất; người dùng chưa yêu cầu thêm phân tích hoặc Ask Advisor cho sheet 3. Quyền truy cập tài khoản Google Ads là điều kiện để lấy dữ liệu mới; nếu bị chặn, báo rõ và có thể dùng bản xuất do người dùng cung cấp.
