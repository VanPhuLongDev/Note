## 1. Luồng chạy
![](w.save/Spring%20security-20241208131903735.webp)

## 2. Các cách xác thực trong API
1. Basic Authentication:
	**Cách hoạt động:**
	Username và password được mã hóa Base64 và gửi qua tiêu đề HTTP.
	**Ưu điểm:**
	Đơn giản, dễ triển khai.
	**Nhược điểm:**
	Kém an toàn nếu không sử dụng HTTPS, username/password được gửi trong mỗi yêu cầu.
2. Token-based Authentication (OAuth 2.0, JWT):
	**a. OAuth 2.0:**
	**Cách hoạt động:**
	Sử dụng một nhà cung cấp dịch vụ (Identity Provider) để xác thực người dùng và cấp token truy cập.
	Người dùng không cần chia sẻ trực tiếp username/password với ứng dụng bên thứ ba.
	**Ưu điểm:**
	Phân quyền tốt, phù hợp cho việc tích hợp bên thứ ba.
	Token có thể thu hồi được.
	**Nhược điểm:**
	Triển khai phức tạp.
	**b. JWT (JSON Web Token):**
	**Cách hoạt động:**
	Sau khi xác thực, server cấp một token chứa thông tin người dùng (payload). Token này được gửi kèm theo mỗi yêu cầu.
	**Ưu điểm:**
	Stateless (không cần lưu trạng thái server-side).
	Phù hợp với hệ thống phân tán hoặc microservices.
	**Nhược điểm:**
	Token không thể thu hồi dễ dàng.
	Kích thước lớn hơn do chứa payload.
3. **Session-based Authentication (Form-based):**
	**Cách hoạt động:**
	Server tạo một session ID và lưu trong cookie khi người dùng đăng nhập. Cookie này được gửi tự động trong mỗi yêu cầu sau đó.
	**Ưu điểm:**
	Dễ triển khai, phù hợp với ứng dụng web truyền thống.
	**Nhược điểm:**
	Phụ thuộc vào trình duyệt (không lý tưởng cho API).
	Quản lý session server-side có thể gây quá tải.
4. API Key Authentication:
	**Cách hoạt động:**
	Mỗi ứng dụng hoặc người dùng được cấp một API key duy nhất. API key được gửi kèm mỗi yêu cầu.
	**Ưu điểm:**
	Dễ triển khai, phù hợp với dịch vụ public (ví dụ: Google Maps API).
	**Nhược điểm:**
	Kém bảo mật nếu key bị lộ (thường không có cơ chế thu hồi hoặc hết hạn).
5. Single Sign-On (SSO):
	**Cách hoạt động:**
	Cho phép người dùng đăng nhập một lần để truy cập nhiều ứng dụng. SSO thường sử dụng các giao thức như OAuth 2.0, OpenID Connect, hoặc SAML.
	**Ưu điểm:**
	Trải nghiệm người dùng tốt, phù hợp với hệ thống lớn.
	**Nhược điểm:**
	Cấu hình và triển khai phức tạp.


## 3. Các cách để phân quyền api
a. Dùng @HasRole
![](w.save/Spring%20security-20241208154100436.webp)
phải khai báo @enableMethodSecurity(jsr250Enabled)

Ngoài ra để chỉ định cụ thể ip nào được truy cập thì dùng thêm @PostAuthorize(ip)

b. Khai báo trong config
![](w.save/Spring%20security-20241208154306110.webp)
