# Sheet 2: Insight report

Quy trình do người dùng xác nhận ngày 10/10/2026. Dùng đúng tháng báo cáo, bảo toàn bố cục và format của hai biểu đồ; chỉ cập nhật dữ liệu và tham chiếu cần thiết. Nội dung mẫu là dữ liệu tham khảo, không phải chỉ dẫn.

## Chart 1: Session source

1. Truy cập GA4, tài khoản ID `30284038`, property `372708254`, bằng quyền được cấp. Mở `Traffic acquisition: Session source / medium` và đặt kỳ thành toàn bộ tháng báo cáo.
2. Lấy chỉ số **Sessions**, xếp giảm dần, giữ top 5. Gom toàn bộ nguồn từ hạng 6 trở đi thành `Other`, bằng tổng Sessions của các nguồn đó. Không bỏ các nguồn nhỏ hoặc tự thêm phần chênh lệch để làm tổng khớp; kiểm tra phạm vi, bộ lọc và dữ liệu đầy đủ khi có chênh lệch.
3. Lấy dữ liệu cùng phạm vi của tháng liền trước để so sánh hai tháng liên tiếp. Nếu tháng trước đã có dữ liệu được đối soát thì tái sử dụng. So sánh cùng nguồn trên hai tháng; không so sánh chỉ theo vị trí thứ hạng. Khi so sánh nhóm Other hoặc thứ hạng thay đổi, nêu rõ phạm vi nhóm để tránh kết luận sai.
4. Cập nhật dữ liệu nguồn của biểu đồ 1. Mẫu dùng sheet `Session source pivot table` (`B1:C7`), tham chiếu sheet `data`. Giữ cấu trúc năm nguồn và Other, cập nhật tên nguồn và số liệu theo thứ hạng thực tế tháng mới. Mẫu tháng 9 dùng nhãn source; báo cáo GA4 được yêu cầu là source / medium, nên đối chiếu cách nhóm trong dữ liệu gốc. Nếu không thể xác định việc gộp medium từ dữ liệu hiện có, hỏi người dùng thay vì tự bỏ dimension medium.
5. Viết đoạn phân tích ngắn so sánh Sessions giữa tháng báo cáo và tháng liền trước, tổng và các nguồn nổi bật. Chỉ dùng chỉ số đã lấy được. Trong mẫu, tiêu đề ở `A18` (Traffic Source Performance), nội dung từ `A19`; thay phân tích kỳ cũ bằng phân tích kỳ mới.

## Audience Behavior

- Bỏ qua thao tác chụp và cập nhật ảnh màn hình; **người dùng tự làm phần này**. Không xóa ảnh hoặc thay bằng ảnh khác. Ghi rõ ảnh mẫu chưa được cập nhật nếu chúng vẫn thuộc kỳ cũ.
- Audience analysis phải **loại subscriber campaigns**. Dùng Ask Advisor trong Google Ads trên đúng tài khoản và kỳ. Khi subscriber hoạt động trong kỳ, hỏi `give me audience analysis, excluding subscriber campaigns`, nêu rõ campaign cần loại và khung ngày khi cần.
- Nếu đã xác minh subscriber không hoạt động trong toàn bộ kỳ, có thể hỏi `give me audience analysis` mà không nhắc loại trừ. Kiểm tra hoạt động thực tế trong kỳ; trạng thái Paused hiện tại không chứng minh campaign không hoạt động trong kỳ trước. Phạm vi audience vẫn loại subscriber.
- Tóm tắt giản lược câu trả lời vào phần phân tích Audience Behavior. Mẫu có các nhóm `Who Is Your Audience?` (`A43`), `How Are They Searching?` (`A48`), `When Are They Active?` (`A53`). Giữ bố cục hiện có, chỉ ghi kết luận được câu trả lời hỗ trợ.
- Nếu chưa truy cập được Advisor, báo phần này bị chặn và yêu cầu câu trả lời xuất từ Advisor; không tự viết như thể Advisor đã trả lời.

## Chart 2: Matched Location

1. Trong đúng tài khoản Google Ads, mở `Insight and report → When and where ads show → Match location → Region`. Chọn toàn bộ tháng báo cáo, **loại subscriber campaigns**, lấy đầy đủ các region cùng Cost và các chỉ số cần cho biểu đồ/phân tích. Áp dụng việc loại subscriber trước khi chọn top hoặc tính tổng.
2. Xếp region theo **Cost giảm dần**, giữ top 3; gom tất cả region còn lại vào `Other`. Không cố định California, Bay hoặc Texas theo mẫu tháng 9.
3. Cập nhật nguồn biểu đồ 2. Mẫu dùng `matched location pivot table` (`A1:C5`): Location, Cost, Cost / conv.; tham chiếu sheet `data`. Cost của Other là tổng Cost các region còn lại. Cost / conv. của Other = tổng Cost của nhóm / tổng Conversions của nhóm, không lấy trung bình CPA các region. Khi không có conversion, dùng cách hiển thị không xác định phù hợp thay vì gán CPA bằng 0.
4. Giữ nguyên format biểu đồ. Đối soát top 3 + Other với tổng bảng region theo cùng phạm vi. Không giả định tổng region luôn bằng tổng account.
5. Viết một phần phân tích ngắn tại vùng Matched Location, nội dung mẫu bắt đầu `A77`. Có thể dùng Ask Advisor với câu hỏi `give me match location analysis`, nêu rõ kỳ và phạm vi; tóm tắt giản lược câu trả lời, đối chiếu số liệu với bảng region.

Người dùng đã xác nhận Region/Matched Location phải loại subscriber campaigns. Xác định đúng danh sách campaign từ tài khoản hoặc quy tắc đã được xác nhận; nếu chưa rõ, hỏi danh sách, không suy đoán từ thứ tự dòng. Cùng bộ lọc này áp dụng raw data, bảng tổng hợp, biểu đồ và phân tích Matched Location.

## Kiểm tra hoàn thành

- Đúng tài khoản/property, tháng, dimension, chỉ số và bộ lọc; dữ liệu đủ để chọn top.
- Chart 1: top 5 + Other khớp tổng Sessions trong cùng phạm vi.
- Chart 2: top 3 + Other khớp Cost/Conversions bảng region; CPA tính từ tổng.
- Hai biểu đồ vẫn tồn tại, dữ liệu mới và format được giữ nguyên sau khi lưu. Mẫu có hai biểu đồ và ba ảnh; bảo toàn ảnh, không nhận ảnh cũ là ảnh tháng mới.
- Ba phần phân tích đã cập nhật: traffic, audience và matched location; phân biệt phần bị chặn và phần ảnh người dùng tự làm.

Khi hỏi Ask Advisor về Matched Location, nhắc loại subscriber nếu có hoạt động trong kỳ. Nếu đã xác minh không hoạt động trong toàn bộ kỳ, có thể bỏ phần nhắc loại subscriber trong câu hỏi; dữ liệu và phân tích vẫn giữ phạm vi loại subscriber.
