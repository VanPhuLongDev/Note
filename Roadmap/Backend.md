## 1. Các phương thức phổ biến dùng authentication
Basic Authentication: Đây là loại xác thực đơn giản nhất, thường sử dụng tên đăng nhập và mật khẩu. Thông tin xác thực được mã hóa cơ bản (Base64) và gửi qua mỗi yêu cầu.

Bearer Token: Loại này sử dụng token (chuỗi mã hóa) để xác thực. Token thường được gửi trong header của yêu cầu HTTP và có thời gian hết hạn. Một ví dụ điển hình là JWT (JSON Web Token).

OAuth2.0: Là chuẩn xác thực mở, phổ biến trong các ứng dụng của bên thứ ba (Google, Facebook,...). OAuth2.0 cho phép người dùng ủy quyền cho một ứng dụng truy cập vào tài khoản của mình mà không cần cung cấp mật khẩu.

SSO (Single Sign-On): Giải pháp cho phép người dùng đăng nhập một lần và truy cập vào nhiều ứng dụng khác nhau mà không cần đăng nhập lại. Một ví dụ phổ biến là đăng nhập qua tài khoản Google hoặc Facebook.

Multi-Factor Authentication (MFA): Sử dụng nhiều yếu tố (như mật khẩu và mã xác thực từ ứng dụng xác thực) để xác minh danh tính người dùng, tăng cường bảo mật.

API Key: Thường được dùng trong các dịch vụ API. API Key là một chuỗi mã duy nhất mà người dùng phải cung cấp để truy cập vào API.

[Tìm hiểu các phương thức Authentication với REST API](https://viblo.asia/p/tim-hieu-cac-phuong-thuc-authentication-voi-rest-api-bJzKmq2EK9N)

