---
name: report-delivery-cleanup
description: Bàn giao và rà soát file phát sinh sau mọi báo cáo, chỉ dọn những file được người dùng lựa chọn rõ ràng.
---

# Bàn giao và dọn file báo cáo

Áp dụng cho mọi báo cáo trong repository, bao gồm LPC monthly, Pelican monthly, Jason weekly và các báo cáo mới. Đây là quy tắc chung; không trộn quy trình lấy dữ liệu giữa các báo cáo.

## Trong quá trình thực hiện

- Ghi nhận các file và thư mục do lần làm này tạo hoặc tải về: bản nháp, bản đệm, raw data, bản xuất, ảnh tạm, preview, log, file kiểm tra, bản trung gian và đầu ra khác. Ghi đường dẫn thực tế và phân biệt file có sẵn trước khi làm.
- Dùng vị trí riêng theo báo cáo và kỳ; không gom file của báo cáo khác vào danh sách dọn. Không ghi bí mật vào danh sách.

## Sau khi bàn giao

1. Bàn giao bản final, nêu rõ đường dẫn và các phần còn do người dùng thực hiện. Sau đó hỏi: **“Báo cáo này đã xong chưa?”**
2. Nếu người dùng chưa xác nhận xong, tiếp tục chỉnh sửa khi được yêu cầu; không bắt đầu dọn file.
3. Khi người dùng xác nhận xong, kiểm tra lại các file phát sinh của lần làm này, gồm các thư mục dữ liệu/đầu ra/làm việc và các vị trí tải về hoặc tạm thực sự đã dùng. Không coi việc xác nhận xong là quyền xóa.
4. Khai báo danh sách để người dùng lựa chọn: tên file hoặc nhóm file được liệt kê cụ thể, mục đích/loại, đường dẫn thư mục lưu và dung lượng nếu xác định được. Đánh dấu bản final cần giữ và các file có thể dọn. Nêu rõ những vị trí không còn truy cập được, không tuyên bố đã kiểm tra chúng.
5. Hỏi người dùng muốn xóa những file nào. Có thể gợi ý chỉ giữ bản final của kỳ và dọn nháp/raw data/file tạm, nhưng phải chờ lựa chọn rõ ràng. Không tự xóa chỉ vì file được xem là không cần thiết hoặc vì đã có quyền dọn file trong một cuộc chat cũ.
6. Chỉ xóa chính xác các file đã được lựa chọn, kiểm tra đường dẫn và bảo đảm không xóa bản final, mẫu, skill, context, mã tái sử dụng, tài liệu repository hoặc file người dùng có sẵn nếu chúng không được chỉ định rõ. Nếu bản final nằm ngoài workspace, xác nhận nó tồn tại và đọc được trước khi dọn bản liên quan.
7. Sau khi dọn, kiểm tra bản final còn nguyên, báo đã xóa gì và dung lượng giải phóng nếu đo được. Nếu không có file phát sinh để dọn, báo rõ.

Không xóa cả thư mục bằng wildcard khi có file chưa được lựa chọn. Không sửa lịch sử Git để giảm dung lượng nếu chưa có yêu cầu riêng; xóa file ở checkout không loại bỏ bản đã nằm trong lịch sử Git. Phân biệt vị trí local, cloud và GitHub trong báo cáo dọn file.
