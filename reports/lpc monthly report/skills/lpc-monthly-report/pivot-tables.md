# Các bảng pivot cấp dữ liệu cho biểu đồ

Người dùng xác nhận ngày 10/10/2026: các sheet pivot được sinh từ sheet raw data, dùng cấp dữ liệu cho biểu đồ ở sheet `Insight report`. Khi cập nhật nguồn đúng, chúng phải cập nhật theo; luôn kiểm tra lại.

Dùng tên sheet thay vì số thứ tự để tránh nhầm. Trong workbook mẫu có 6 sheet: raw data tên `data`; hai sheet tổng hợp tên `matched location pivot table` và `Session source pivot table`. Người dùng gọi chúng là sheet 4/5 và nguồn sheet 3; ánh xạ theo vai trò và tên thực tế trong mẫu, không đổi nguồn thành `search term and keyword`.

## Quy trình

1. Cập nhật raw data theo `sheet-4-data.md` và quy tắc `sheet-2-insight-report.md` trước.
2. Kiểm tra nguồn tham chiếu, phạm vi, tên nhóm và thứ hạng trong hai bảng tổng hợp. Mẫu hiện dùng các công thức tham chiếu sheet `data`; không giả định có pivot refresh tự động hoặc công thức cố định luôn chọn đúng top khi thứ hạng thay đổi.
3. Nếu workbook có pivot thực, refresh/recalculate bằng công cụ hỗ trợ khi cần. Với công thức, bảo đảm tính lại và cập nhật phạm vi/tham chiếu hoặc nhãn theo nguồn mới nếu cần. Việc lưu bằng thư viện không tính công thức chưa chứng minh số liệu đã cập nhật.
4. `Session source pivot table`: top 5 theo Sessions và Other gồm toàn bộ phần còn lại; tên nguồn phải khớp số liệu, tổng khớp raw data cùng phạm vi.
5. `matched location pivot table`: top 3 theo Cost và Other; toàn bộ nguồn loại subscriber campaigns. Kiểm tra Cost, Conversions dùng tính CPA; CPA của Other là tổng Cost / tổng Conversions, không trung bình CPA.
6. Kiểm tra biểu đồ tương ứng ở `Insight report` lấy đúng bảng và đúng phạm vi, hiển thị dữ liệu tháng mới. Giữ nguyên format, vị trí và kích thước biểu đồ.
7. Đối soát giá trị sau khi tính lại, không chỉ xem công thức. Nếu công cụ không tính lại/refresh được, ghi rõ phần kiểm tra chưa hoàn tất; không khẳng định các bảng hay biểu đồ đã cập nhật tự động.

Không nhập số liệu độc lập vào bảng pivot làm mất liên kết nguồn. Không giữ giá trị cache của tháng cũ hoặc nhãn nhóm cũ khi số liệu đã thay đổi.
