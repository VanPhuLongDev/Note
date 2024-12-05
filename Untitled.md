### Singleton Pattern
Mục đích: Đảm bảo chỉ có một instance của một class duy nhất trong toàn bộ ứng dụng.
Cách dùng:
Các providers trong NestJS mặc định là singleton, có nghĩa là chúng chỉ có một instance cho toàn bộ ứng dụng.
Bạn có thể dễ dàng inject vào bất kỳ nơi nào mà không phải lo lắng về việc tạo lại instance.
#### Vì sao cần dùng Singleton Pattern?
1. Tránh tạo nhiều instance không cần thiết

Nếu một class được sử dụng ở nhiều nơi, việc tạo ra nhiều instance có thể gây lãng phí tài nguyên như bộ nhớ và CPU. Singleton đảm bảo chỉ có một instance duy nhất được tạo và tái sử dụng ở mọi nơi.
2. Đảm bảo trạng thái thống nhất

Singleton giúp duy trì một trạng thái duy nhất của dữ liệu. Ví dụ, khi một class quản lý cấu hình ứng dụng, việc sử dụng Singleton sẽ đảm bảo rằng tất cả các phần của ứng dụng đều truy cập cùng một cấu hình.
3. Điều phối hoặc chia sẻ tài nguyên chung

Một số tài nguyên như kết nối cơ sở dữ liệu, trình quản lý bộ nhớ đệm, hoặc logger cần được chia sẻ trên toàn bộ ứng dụng. Singleton giúp bạn tái sử dụng chúng mà không cần tạo mới ở từng nơi.
Điều gì xảy ra nếu không dùng Singleton Pattern?
1. Tốn tài nguyên hệ thống

Nếu mỗi nơi trong ứng dụng tạo một instance mới của class, điều này sẽ dẫn đến dư thừa bộ nhớ và giảm hiệu suất. Đặc biệt khi class đó thực hiện các công việc nặng như kết nối cơ sở dữ liệu hoặc khởi tạo tài nguyên.
2. Trạng thái không đồng nhất

Khi có nhiều instance, trạng thái của các instance có thể khác nhau, dẫn đến lỗi không mong muốn. Ví dụ, nếu một instance lưu trạng thái của một phiên làm việc (session) mà không được đồng bộ, ứng dụng có thể hoạt động không đúng.
3. Quản lý khó khăn

Nếu có nhiều instance của cùng một class, bạn sẽ phải quản lý chúng một cách thủ công, chẳng hạn như tìm cách đảm bảo chúng không xung đột hoặc không làm việc lặp lại.




### Decorator Pattern
#### **Vì sao dùng Decorator Pattern?**

**1. Thêm hành vi mà không làm thay đổi cấu trúc gốc của lớp**

- Decorator cho phép mở rộng chức năng hoặc thêm metadata cho một lớp/method mà không cần sửa đổi trực tiếp mã nguồn ban đầu. Điều này giúp giữ cho mã gốc sạch sẽ và dễ bảo trì.

**2. Tăng tính tái sử dụng**

- Các decorators có thể được tái sử dụng ở nhiều nơi trong ứng dụng. Ví dụ, trong NestJS, `@Get()` có thể được áp dụng trên nhiều route handler để định nghĩa endpoint HTTP GET.

**3. Cấu trúc rõ ràng và dễ hiểu hơn**

- Decorators làm cho mã dễ đọc hơn bằng cách thể hiện ý định trực tiếp. Ví dụ, khi nhìn vào `@Controller()` và `@Get()`, bạn có thể hiểu ngay đây là một lớp điều khiển và một phương thức xử lý route GET.

**4. Tăng tính mô-đun hóa**

- Decorators đóng gói logic phụ trợ như logging, kiểm tra quyền (authorization), hoặc xử lý lỗi mà không làm rối lớp chính.

### **Đồ thị tri thức (Knowledge Graph)**
là một cấu trúc dữ liệu biểu diễn thông tin dưới dạng các **thực thể (entities)** và **mối quan hệ (relationships)** giữa chúng. Thay vì lưu trữ dữ liệu trong các bảng như cơ sở dữ liệu quan hệ, đồ thị tri thức sử dụng các **đỉnh (nodes)** để đại diện cho thực thể và các **cạnh (edges)** để biểu diễn mối quan hệ.

### **Tại sao sử dụng đồ thị tri thức?**

1. **Biểu diễn tự nhiên hơn**:
    
    - Các mối quan hệ phức tạp và đa chiều giữa dữ liệu được thể hiện một cách trực quan và dễ hiểu hơn. Ví dụ, mối quan hệ kiểu "Người - Làm việc tại - Công ty" hoặc "Người - Bạn của - Người khác" rất phù hợp với mô hình đồ thị.
2. **Truy vấn quan hệ phức tạp hiệu quả hơn**:
    
    - Với đồ thị tri thức, bạn có thể dễ dàng thực hiện các truy vấn như "Tìm tất cả bạn của bạn của một người" hoặc "Tìm tất cả nhân viên làm việc trong một công ty cụ thể", mà không cần phải viết các truy vấn SQL phức tạp với nhiều phép JOIN.
3. **Mở rộng linh hoạt**:
    
    - Khi cần thêm thực thể hoặc quan hệ mới, đồ thị tri thức không yêu cầu thay đổi cấu trúc như các bảng trong cơ sở dữ liệu quan hệ.
4. **Tích hợp dữ liệu từ nhiều nguồn**:
    
    - Đồ thị tri thức giúp tích hợp thông tin từ các nguồn khác nhau, thậm chí có cấu trúc khác nhau, bằng cách tập trung vào mối quan hệ giữa dữ liệu.
5. **Hỗ trợ AI và học máy**:
    
    - Đồ thị tri thức cung cấp ngữ cảnh và thông tin liên kết, giúp cải thiện hiệu suất của các thuật toán học máy, xử lý ngôn ngữ tự nhiên (NLP), và ra quyết định.


### 