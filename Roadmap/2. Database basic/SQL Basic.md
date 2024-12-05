### 1. SQL là gì?

Viết tắt của Structured Query Language – ngôn ngữ truy vấn cấu trúc. Nó được thiết kế để quản lý dữ liệu trong một hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS - Relational Database Management System). SQL là ngôn ngữ cơ sở dữ liệu, được dùng để tạo, xóa, lấy các hàng và sửa đổi các hàng.

### 2. Câu lệnh để chọn tất cả bản ghi từ table?

Cú pháp: **Select * from table_name**

### 3. Định nghĩa JOIN và các loại JOIN

Từ khóa JOIN được dùng để nạp dữ liệu từ 2 hay nhiều bảng liên quan. Sử dụng từ khóa JOIN khi cần truy vấn các cột dữ liệu từ nhiều bảng khác nhau để trả về trong cùng một tập kết quả.

Các loại JOIN:

- INNER JOIN
- LEFT OUTER JOIN
- RIGHT OUTER JOIN
- FULL OUTER JOIN

### 4. Cú pháp để thêm bản ghi vào 1 bảng là gì?

Sử dụng cú pháp INSERT để thêm bản ghi vào 1 bảng

Ví dụ: **INSERT** into table_name **VALUES** (value1, value2,…)

### 5. Làm thế nào để bạn thêm 1 cột vào 1 bảng?

Để thêm một cột khác vào bảng, sử dụng cú pháp:

**ALTER TABLE** table_name **ADD** (column_name)

### 6. Xác định câu lệnh Delete SQL

Câu lệnh này được sử dụng để xóa hàng hoặc các hàng từ một bảng dựa trên điều kiện được chỉ định.

Cú pháp:

**DELETE FROM** table_name<br>**WHERE<**Condition>

### 7. Xác định COMMIT

COMMIT lưu lại tất cả các thay đổi được thực hiện bởi các câu lệnh DML. DML cho phép thực hiện các truy vấn, bao gồm cú pháp để cập nhật, sửa đổi, chèn thêm và xóa các mẫu tin.

### 8. Khóa chính (PRIMARY KEY) là gì?

Khóa chính là cột có các giá trị xác định **duy nhất** mỗi hàng trong một bảng. Giá trị khóa chính không bao giờ được sử dụng lại.

Một cột là PRIMARY KEY thì không được phép có giá trị NULL. Mỗi bảng chỉ cho phép tối đa một PRIMARY KEY. Mỗi bảng đều cần có khóa chính

### 9. Khóa ngoại (FOREIGN KEY) là gì?

Khi một trường khóa chính của một bảng được thêm vào các bảng có liên quan để tạo ra trường phổ biến có liên quan đến 2 bảng, nó được gọi là khóa ngoại trong các bảng khác. Các ràng buộc khóa ngoại thực thi toàn vẹn tham chiếu.

### 10. CHECK Constraint – Ràng buộc CHECK là gì?

Một ràng buộc CHECK được sử dụng để giới hạn các giá trị hoặc loại dữ liệu có thể được lưu trữ trong một cột. Nếu bản ghi không đáp ứng được điều kiện này, thì sẽ không được lưu trữ vào trong bảng.

### **11.** Một bảng có thể có nhiều hơn một khóa ngoại không?

Một bảng có thể có nhiều hơn một khóa ngoại nhưng chỉ có một khóa chính.

### 12. Trường dữ liệu BOOLEAN có giá trị nào?

Đối với trường dữ liệu BOOLEAN, có 2 giá trị: -1 (TRUE) và 0 (FALSE)

### 13. Thủ tục lưu trữ (stored procedure) là gì?

Một thủ tục lưu trữ là một tập hợp các truy vấn SQL có thể lấy đầu vào và gửi lại đầu ra.

### 14. IDENTITY trong SQL là gì?

Một cột IDENTITY trong SQL sẽ tự động sinh ra các giá trị số tự tăng. Có thể định nghĩa giá trị bắt đầu và gia tăng của cột nhận dạng.

### 15. NOMALIZATION – Chuẩn hóa là gì?

Quá trình thiết kế bảng để giảm thiểu sự thừa số liệu được gọi là chuẩn hóa. Chúng ta cần chia một cơ sở dữ liệu thành hai hay nhiều bảng và xác định các mối quan hệ giữa chúng.

### 16. Trigger là gì?

Trigger là một thủ tục được thực thi từ phía máy chủ cơ sở dữ liệu khi một sự kiện bảng xảy ra (chèn, cập nhật, xóa lệnh thực hiện đối với một bảng cụ thể).

### 17. Làm thế nào để lấy ra các hàng ngẫu nhiên từ một bảng?

Sử dụng câu lệnh SAMPLE chúng ta có thể chọn các hàng ngẫu nhiên. Ví dụ:

`SELECT * FROM table_name SAMPLE(10)`

### 18. Cổng TCP/IP nào mà SQL server chạy?

Mặc định SQL Server chạy trên cổng 1433

##### 19. Viết một truy vấn SELECT SQL để trả về mỗi bản ghi chỉ một lần từ một bảng?

Để có được mỗi tên một lần duy nhất, chúng ta cần phải sử dụng từ khóa DISTINCT. Cú pháp: 

**SELECT DISTINCT** name **FROM** table_name

### 20. DML và DDL là gì?

DML là viết tắt của Ngôn ngữ thao tác dữ liệu (Data Manipulation Language): INSERT, UPDATE và DELETE là các câu lệnh DML.

DDL là viết tắt của Ngôn ngữ định nghĩa dữ liệu (Data Definition Language): CREATE, ALTER, DROP, RENAME là các câu lệnh DDL.

##### 21. Lệnh nào để đổi tên một cột trong đầu ra của truy vấn SQL?

Sử dụng cú pháp: **SELECT** column_name **AS** new_name **FROM** table_name;

### 22. Thứ tự của SQL ?

Thứ tự các mệnh đề SQL SELECT là: 
1. **FROM**: Xác định bảng hoặc bảng liên kết được sử dụng trong câu lệnh.
2. **JOIN**: Bao gồm các loại như Inner Join, Left Join, Right Join, Cross Join, Self Join.
3. **WHERE**: Lọc dữ liệu dựa trên điều kiện được chỉ định.
4. **GROUP BY**: Gộp nhiều row có cùng điều kiện lại (tuỳ chọn).
5. **HAVING**: Lọc dữ liệu sau khi đã gộp (tuỳ chọn).
6. **SELECT**: Chọn các cột dữ liệu cần hiển thị.
7. **ORDER BY**: Sắp xếp dữ liệu theo thứ tự (tuỳ chọn)

### **23.** Giả sử một bảng Student có 2 cột, Name và Marks. Làm thế nào để có được điểm của 3 sinh viên top đầu? _(lưu ý, nếu nhiều sinh viên trùng điểm thì coi như 1 hạng, ví dụ: có 5 sinh viên 10 điểm, 1 sinh viên 9 điểm, 2 sinh viên 8 điểm, top 3 ở đây sẽ bao gồm 3 nhóm sinh viên trên)_

Câu lệnh: 

```sql
select Name, Marks FROM Student s1 where s1.marks in (select distinct top 3 marks from Student s2 order by s2.marks desc)
```

### 24. SQL comments là gì?

Khi muốn thêm chú thích vào truy vấn SQL để rõ ràng, chi tiết hơn, người ta sử dụng SQL comment. SQL comment có thể được đặt bởi 2 dấu nối liên tiếp (-) hoặc /*….*/.

Khi câu truy vấn được thực hiện thì trình biên dịch sẽ tự động bỏ qua những dòng có comment.

### 25. Transaction trong SQL là gì
Là một nhóm các câu lệnh SQL. Nếu một transaction được thực hiện thành công, tất cả các thay đổi dữ liệu được thực hiện trong transaction được lưu vào cơ sở dữ liệu. Nếu một transaction bị lỗi và được rollback, thì tất cả các sửa đổi dữ liệu sẽ bị xóa (dữ liệu được khôi phục về trạng thái trước khi thực hiện transaction).

### 26. Transaction có mấy thuộc tính cơ bản?
Có 4 thuộc tính cơ bản, gọi tắt là ACID
- Atomicity ( Tính bảo toàn ): đảm bảo rằng tất cả các câu lệnh trong nhóm lệnh được thực thi thành công. Nếu không, transaction bị hủy bỏ tại thời điểm thất bại và tất cả các thao tác trước đó được khôi phục về trạng thái cũ.
- Consistency ( Tính nhất quán ): đảm bảo rằng cơ sở dữ liệu thay đổi chính xác các trạng thái khi một transaction được thực thi thành công.
- Isolation ( tính độc lập ): đảm bảo các transaction thực hiện độc lập và minh bạch với nhau
- Durability ( tính bền vững ): đảm bảo rằng kết quả của một transaction được commit vẫn tồn tại trong trường hợp lỗi hệ thống.

### 27. Các lệnh được sử dụng để xử lý transaction?
- **COMMIT** - để lưu các thay đổi.
- **ROLLBACK** - để khôi phục lại các thay đổi.
- **SAVEPOINT** - tạo ra các điểm trong transaction để ROLLBACK.
- **SET TRANSACTION** - thiết lập các thuộc tính cho transaction.


### 28. Sự khác nhau giữa UNIQUE và PRIMARY KEY constraints là gì?

### 29. Index là gì?

Index (Chỉ mục) là bảng tra cứu đặc biệt mà Database Search Engine có thể sử dụng để giảm thời gian và tăng hiệu suất thực hiện các truy vấn. Index có thể được tạo trên một hoặc nhiều cột của một bảng.
Index là một cấu trúc dữ liệu được dùng để định vị và truy cập nhanh nhất vào dữ liệu trong các bảng database
Index là một cách tối ưu hiệu suất truy vấn database bằng việc giảm lượng truy cập vào bộ nhớ khi thực hiện truy vấn

### 30. Có mấy loại index
- Primary Index
- Unique Index
- Full-Text Index
- Composite Index
- Spatial Index
- Clustered Index
- Non-Clustered Index

> Cách lưu trữ index là B-tree, hashmap, bitmap

### 31. Schema là gì?

Biểu đồ là tập hợp các đối tượng cơ sở dữ liệu của người dùng

### 32. Bảng là gì?

Một bảng là đơn vị cơ bản của lưu trữ dữ liệu trong hệ thống quản lý cơ sở dữ liệu. Dữ liệu bảng được lưu trữ trong hàng và cột.

### 33. Sự khác nhau giữa mệnh đề Having và mệnh đề Where?
**Mệnh đề `WHERE`**
- **Mục đích:** Lọc các hàng dữ liệu trước khi bất kỳ phép toán nhóm nào (`GROUP BY`) được thực hiện.
- **Hoạt động:** Lọc các hàng riêng lẻ trong bảng dựa trên các điều kiện được chỉ định.
- **Sử dụng với:** Các cột và biểu thức, nhưng không thể sử dụng với các hàm tổng hợp (aggregate functions) trực tiếp.
**Mệnh đề `HAVING`**
- **Mục đích:** Lọc các nhóm dữ liệu sau khi phép toán nhóm (`GROUP BY`) đã được thực hiện.
- **Hoạt động:** Lọc các nhóm dữ liệu dựa trên các điều kiện được chỉ định.
- **Sử dụng với:** Các hàm tổng hợp như `SUM()`, `AVG()`, `COUNT()`, `MAX()`, `MIN()`.