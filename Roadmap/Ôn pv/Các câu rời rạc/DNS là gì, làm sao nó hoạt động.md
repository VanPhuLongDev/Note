DNS (Domain Name System) là hệ thống phân giải tên miền, giúp chuyển đổi các tên miền dễ nhớ như `www.google.com` thành các địa chỉ IP mà máy tính có thể hiểu được, như `142.250.72.238`. Đây là cách mà các trình duyệt và các thiết bị mạng khác nhau có thể tìm và truy cập vào các máy chủ trên Internet.

### Cách DNS Hoạt Động

1. **Client Request (Yêu cầu từ khách hàng)**:
    - Khi bạn nhập một tên miền vào trình duyệt, trình duyệt sẽ kiểm tra bộ nhớ cache của mình để xem liệu nó đã biết địa chỉ IP tương ứng chưa. Nếu không có trong bộ nhớ cache, nó sẽ tiếp tục với quá trình phân giải DNS.
2. **DNS Recursive Resolver (Bộ phân giải đệ quy DNS)**:
    - Trình duyệt gửi một yêu cầu tới bộ phân giải đệ quy DNS, thường là máy chủ DNS của ISP hoặc một dịch vụ DNS công cộng như Google DNS (`8.8.8.8`) hoặc Cloudflare DNS (`1.1.1.1`).
3. **Root Name Servers (Máy chủ tên gốc)**:
    - Nếu bộ phân giải đệ quy không có trong bộ nhớ cache, nó sẽ gửi một truy vấn tới một trong các máy chủ tên gốc. Các máy chủ này không biết địa chỉ IP của tên miền cụ thể, nhưng chúng có thể chuyển hướng tới các máy chủ tên miền cấp cao nhất (TLD) như `.com`, `.org`, `.net`.
4. **TLD Name Servers (Máy chủ tên miền cấp cao nhất)**:
    - Máy chủ tên gốc trả về địa chỉ của máy chủ TLD (ví dụ: máy chủ `.com`). Bộ phân giải đệ quy sau đó sẽ gửi truy vấn tới máy chủ TLD.
5. **Authoritative Name Servers (Máy chủ có thẩm quyền)**:
    - Máy chủ TLD sẽ trả về địa chỉ của máy chủ có thẩm quyền cho tên miền cụ thể (ví dụ: `google.com`). Bộ phân giải đệ quy sau đó sẽ gửi truy vấn tới máy chủ có thẩm quyền.
6. **Return IP Address (Trả về địa chỉ IP)**:
    - Máy chủ có thẩm quyền sẽ trả về địa chỉ IP của tên miền. Bộ phân giải đệ quy nhận địa chỉ IP này và lưu nó vào bộ nhớ cache để sử dụng trong tương lai, và sau đó trả về cho trình duyệt.
7. **Access Website (Truy cập trang web)**:
    - Trình duyệt nhận địa chỉ IP và sử dụng nó để kết nối với máy chủ web của tên miền, bắt đầu quá trình kết nối TCP và gửi yêu cầu HTTP.