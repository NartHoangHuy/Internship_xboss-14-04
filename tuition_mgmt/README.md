Many2one (N-1):
Phiếu đăng ký -> Học viên: Nhiều phiếu đăng ký có thể được tạo bởi cùng một học viên (học nhiều lớp khác nhau), nhưng một phiếu đăng ký cụ thể chỉ thuộc về duy nhất một học viên.

Phiếu đăng ký -> Lớp học: Tương tự, nhiều phiếu đăng ký cùng trỏ về một lớp học (lớp có nhiều người học), nhưng một phiếu đăng ký chỉ xác định cho một lớp học cụ thể.

Lớp học -> Khóa học: Nhiều lớp học (K1, K2, K3) có thể cùng triển khai nội dung của một khóa học.

One2many (1-N): (Đây là góc nhìn ngược chiều của Many2one, phục vụ cho UI/UX và truy xuất dữ liệu)

Lớp học -> Phiếu đăng ký: Từ góc độ quản lý, người vận hành cần đứng từ một Lớp học để nhìn thấy danh sách nhiều Phiếu đăng ký (tương đương danh sách lớp).

Many2many (N-N):

Học viên <-> Khóa học: Một học viên trong suốt vòng đời có thể học nhiều khóa học. Ngược lại, một khóa học sẽ có nhiều học viên từng tham gia. (Lưu ý trong thiết kế DB: Quan hệ N-N này thực chất đã được giải quyết thông qua thực thể trung gian là Phiếu đăng ký và Lớp học, nhưng hệ thống vẫn có thể thiết lập quan hệ trực tiếp để phục vụ báo cáo nhanh).