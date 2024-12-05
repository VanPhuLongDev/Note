### 1. Spring profile
Là một tính năng cốt lõi, cho phép ánh xạ với các profile khác nhau như dev, test, prod. Được dùng  thông qua annotation @Profile

### 2. Bean scope:
- bean là những module chính của chương trình, được tạo ra và quản lý bởi Spring IoC container
* **singleton** (mặc định): Một instance duy nhất được tạo và chia sẻ trong toàn bộ Spring container.
- **prototype**: Mỗi lần bean được yêu cầu, một instance mới được tạo.
- **request**: Một instance được tạo cho mỗi HTTP request (dành cho ứng dụng web).
- **session**: Một instance được tạo cho mỗi HTTP session (dành cho ứng dụng web).
- **application**: Một instance được tạo cho mỗi ServletContext (dành cho ứng dụng web).

### 3. Spring IoC Container
a. IOC
	IoC (Inversion of Control) là một nguyên lý thiết kế trong lập trình, trong đó luồng điều khiển của chương trình được đảo ngược. Thay vì code của chúng ta kiểm soát luồng và gọi thư viện, framework sẽ kiểm soát luồng và gọi code của chúng ta.

b. Spring IoC container
	Spring IoC container là core của Spring Framework. Nó tạo các đối tượng, kết nối chúng, cấu hình chúng, và quản lý vòng đời của chúng từ khi tạo đến khi bị hủy.

c. DI là gì và nó liên quan thế nào đến IoC
	DI (Dependency Injection) là một design parten, trong đó các dependencies (phụ thuộc) được "tiêm" vào một đối tượng từ bên ngoài thay vì được tạo bên trong đối tượng đó. Spring Framework sử dụng DI để thực hiện IoC.
	- Có 3 dạng là : Contructor Injection, Setter Injection, Interface Injection

d. Làm thế nào để định nghĩa một Bean trong Spring Boot? 
	Có thể định nghĩa Bean bằng cách sử dụng annotation @Bean trong các class cấu hình (@Configuration), hoặc sử dụng @Component, @Service, @Repository, @Controller trên các class.

e. Bean trong Spring là gì? 
	Bean là các đối tượng được tạo và quản lý bởi Spring IoC container.

f. Làm thế nào để resolve các bean conflicts trong Spring? 
	Sử dụng @Qualifier, @Primary, hoặc đặt tên cụ thể cho bean.

g. Sự khác biệt giữa BeanFactory và ApplicationContext? 
	ApplicationContext là interface con của BeanFactory, cung cấp nhiều tính năng hơn như internationalization, event propagation, resource loading, v.v.
h. Bean lifecycle
- Khởi tạo
- Dependency Injection
- Post-construction
- Pre-destruction
- Destruction
i. Tránh xung đột bean cùng class: Để tránh xung đột khi có nhiều bean cùng class:
	Sử dụng @Qualifier để chỉ định tên bean cụ thể.
	Đặt tên bean khác nhau bằng @Bean(name = "customName").
	Sử dụng @Primary để ưu tiên một bean khi autowiring.
	Dùng @Profile để tạo bean cho các môi trường khác nhau.

### 4. Solid là gì ?
là bộ 5 nguyên tắc trong lập trình, giúp code dễ đọc, dễ hiểu, và dễ bảo trì hơn
- Một class chỉ nên giữ 1 trách nhiệm duy nhất
- Có thể thoải mái mở rộng 1 class, nhưng không được sửa đổi bên trong class đó ( mỗi khi ta muốn thêm chức năng,.. cho chương trình, chúng ta nên viết class mới mở rộng class cũ ( bằng cách kế thừa hoặc sở hữu class cũ) không nên sửa đổi class cũ.)
- Trong một chương trình, các object của class con có thể thay thế class cha mà không làm thay đổi tính đúng đắn của chương trình
- Thay vì dùng 1 interface lớn, ta nên tách thành nhiều interface nhỏ, với nhiều mục đích cụ thể
- Các module cấp cao không nên phụ thuộc vào các modules cấp thấp.

## 5. concurrency
- async/parallel/reactive programming
- Chủ yếu dùng bất đồng bộ, dùng để call api
- [Spring Boot @Async Controller with CompletableFuture (howtodoinjava.com)](https://howtodoinjava.com/spring-boot/spring-async-completablefuture/)
## 6. Index
![](w.save/Basic-20241017202621759.webp)
## 7. redis
![](w.save/Basic-20241017203437882.webp)
![](w.save/Basic-20241017203508546.webp)
