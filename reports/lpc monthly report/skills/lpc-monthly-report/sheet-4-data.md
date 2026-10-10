# Sheet 4: data

Quy trình do người dùng xác nhận ngày 10/10/2026. Sheet này lưu raw data từ GA4 và Google Ads, dùng làm nguồn cho các bảng và biểu đồ. Không chỉ lưu các nhóm top/Other thay cho raw data đầy đủ.

## Traffic acquisition: Session source

- Lấy từ GA4 account `30284038`, property `372708254`, theo cách đã ghi trong `sheet-2-insight-report.md`: Traffic acquisition: Session source / medium, chỉ số Sessions, đúng toàn bộ tháng báo cáo.
- Lưu đầy đủ dữ liệu nguồn trước khi chọn top 5 và gộp Other. Giữ dimension và phạm vi được xuất, không tự bỏ medium khi chưa xác định quy tắc nhóm.
- Cập nhật dữ liệu kỳ cũ và kỳ ghi trong tiêu đề; giữ format sheet. Đối soát tổng với GA4 trong cùng phạm vi.

## Matched locations report — Region — subscriber campaigns excluded

- Lấy từ Google Ads theo cách sheet 2: Insight and report → When and where ads show → Match location → Region.
- Chọn đúng toàn bộ tháng báo cáo và **loại subscriber campaigns trước khi lấy dữ liệu**, trước khi tính tổng, chọn top 3 theo Cost hoặc nhóm Other.
- Xác định subscriber campaigns bằng cấu hình/phân loại campaign của tài khoản hoặc quy tắc đã được xác nhận, không suy đoán từ vị trí dòng trong mẫu. Nếu chưa xác định được danh sách, hỏi để xác nhận.
- Lưu đầy đủ các region trong phạm vi này và các cột theo mẫu, bao gồm region có 0 conversions. Không áp dụng filter Cost > 0 của Search terms sang bảng này nếu chưa được yêu cầu.
- Cập nhật khung ngày trên tiêu đề, giữ ghi chú `subscriber campaigns excluded`. Không giữ chữ September khi làm tháng khác.
- Đối soát Cost và Conversions với bảng Region đã loại subscriber. Cost / conv. tính từ Cost / Conversions; tổng và nhóm Other tính từ tổng tử số/mẫu số, không trung bình CPA.

## Liên kết và kiểm tra

- Cập nhật vùng nguồn và công thức ở `Session source pivot table` và `matched location pivot table` theo dữ liệu thực tế. Giữ format biểu đồ sheet 2.
- Mọi bảng/biểu đồ Matched Location trong workbook phải dùng cùng phạm vi loại subscriber campaign, kể cả khi vị trí sheet thay đổi. Người dùng nhắc “sheet 2 và 3” khi nói về Matched Location; mẫu hiện tại đặt phần này ở sheet 2 và sheet `data`, còn sheet 3 là Search terms. Không diễn giải ghi chú này thành yêu cầu loại subscriber khỏi Search terms.
- Xóa raw data dư của kỳ cũ trong vùng tương ứng, giữ các phần khác. Không tự tạo chênh lệch bù tổng. Lưu bản xuất gốc trong `data/YYYY-MM/` của báo cáo và ghi phạm vi/bộ lọc để đối soát.
