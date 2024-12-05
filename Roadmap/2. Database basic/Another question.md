### 1. N+1 query problem
Vấn đề `N+1 query problem` là một vấn đề hiệu suất phổ biến trong các ứng dụng cơ sở dữ liệu, đặc biệt là khi sử dụng ORM (Object-Relational Mapping) như Hibernate, Entity Framework, Django ORM, v.v. Nó xảy ra khi ứng dụng thực hiện một truy vấn để lấy danh sách các bản ghi, và sau đó thực hiện thêm một truy vấn riêng biệt cho từng bản ghi trong danh sách đó để lấy thông tin liên quan.
Ví dụ
Bảng Authors:

|author_id|name|
|---|---|
|1|J.K. Rowling|
|2|George Orwell|

Bảng Books:

| book_id | title          | author_id |
| ------- | -------------- | --------- |
| 1       | Harry Potter 1 | 1         |
| 2       | Harry Potter 2 | 1         |
| 3       | 1984           | 2         |
| 4       | Animal Farm    | 2         |
Truy vấn gây ra vấn đề `N+1`

1. **Truy vấn 1:** Lấy tất cả các tác giả.
	`SELECT * FROM Authors;`
2. **Truy vấn N:** Với mỗi tác giả, lấy tất cả các sách của họ.
    `SELECT * FROM Books WHERE author_id = 1; SELECT * FROM Books WHERE author_id = 2;`

Nếu có N tác giả, bạn sẽ có 1 truy vấn để lấy danh sách các tác giả và N truy vấn để lấy danh sách các sách cho từng tác giả, tổng cộng là `N+1` truy vấn. Khi số lượng tác giả và sách tăng lên, số lượng truy vấn cũng tăng theo, dẫn đến hiệu suất kém.
**Giải pháp cho vấn đề `N+1 query problem`**
1. Eager Loading (Tải dữ liệu sớm)
	Thay vì tải dữ liệu liên quan khi cần, bạn có thể tải tất cả dữ liệu liên quan trong một truy vấn duy nhất bằng cách sử dụng `JOIN`.
	`SELECT a.*, b.* FROM Authors a LEFT JOIN Books b ON a.author_id = b.author_id;`
2. Batch Fetching (Tải dữ liệu theo lô)
	Một số ORMs hỗ trợ batch fetching, nơi dữ liệu liên quan được tải theo lô để giảm số lượng truy vấn.