- **Authentication (Xác thực)**:
    
    - **Mục đích**: Xác minh danh tính của người dùng, đảm bảo rằng người dùng đã đăng nhập hợp lệ.
    - **Thành phần quan trọng**: `AuthenticationManager`, `AuthenticationProvider`, `UserDetailsService`.
    - **Cách hoạt động**: Sử dụng `AuthenticationManager` để quản lý quy trình xác thực, `AuthenticationProvider` để xác minh danh tính, và `UserDetailsService` để tải thông tin người dùng từ cơ sở dữ liệu.
- **Authorization (Ủy quyền)**:
    
    - **Mục đích**: Quản lý quyền truy cập vào các tài nguyên trong ứng dụng dựa trên quyền hạn (roles) hoặc quyền (authorities) của người dùng.
    - **Thành phần quan trọng**: `AccessDecisionManager`, `GrantedAuthority`, `Role`.
    - **Cách hoạt động**: Xác định người dùng có thể truy cập tài nguyên hay không dựa trên quyền được gán cho họ. Spring Security có thể cấu hình quyền theo cấp độ URL, cấp độ phương thức hoặc đối tượng.
- **Password Management (Quản lý mật khẩu)**:
    
    - **Mục đích**: Bảo mật mật khẩu bằng cách mã hóa và xác thực.
    - **Thành phần quan trọng**: `PasswordEncoder`.
    - **Cách hoạt động**: Sử dụng `PasswordEncoder` để mã hóa mật khẩu trước khi lưu vào cơ sở dữ liệu, đảm bảo rằng mật khẩu không được lưu trữ dưới dạng plain text.
- **Session Management (Quản lý phiên)**:
    
    - **Mục đích**: Bảo vệ phiên người dùng, ngăn chặn các cuộc tấn công như **session fixation**.
    - **Thành phần quan trọng**: `SessionManagementFilter`.
    - **Cách hoạt động**: Kiểm soát cách phiên của người dùng được xử lý và bảo vệ, bao gồm kiểm soát số lượng phiên tối đa và xác định hành vi khi hết hạn phiên.
- **Protection Against Common Vulnerabilities (Bảo vệ chống lại các lỗ hổng phổ biến)**:
    
    - **Mục đích**: Ngăn chặn các tấn công phổ biến như **Cross-Site Request Forgery (CSRF)**, **Cross-Site Scripting (XSS)** và **Clickjacking**.
    - **Thành phần quan trọng**: `CSRF Token`, `XSS Protection`, `Content Security Policy`.
    - **Cách hoạt động**: Tự động bảo vệ ứng dụng khỏi các tấn công này bằng cách thêm các cơ chế bảo vệ vào requests và responses.
- **Integration with OAuth2 and JWT (Tích hợp OAuth2 và JWT)**:
    
    - **Mục đích**: Cung cấp xác thực và ủy quyền qua token thay vì phiên.
    - **Thành phần quan trọng**: `OAuth2AuthorizationServer`, `JWT Token`.
    - **Cách hoạt động**: Sử dụng JWT để tạo và xác thực token giúp ứng dụng dễ dàng tích hợp với các hệ thống khác mà không cần lưu trữ phiên người dùng.