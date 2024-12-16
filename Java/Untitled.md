Okay, đây là danh sách các câu hỏi trong file cùng với câu trả lời ổn nhất cho từng câu, dựa trên những gì đã thảo luận trong đoạn hội thoại:

**Phần Thuật Toán và Cấu Trúc Dữ Liệu**

11. **Câu hỏi:** Em đã học những loại cấu trúc dữ liệu nào?
    *   **Trả lời:** Em đã học: Mảng, Set, Map, Stack, Queue, LinkedList.
12. **Câu hỏi:** Em đã học mảng mấy chiều rồi?
    *   **Trả lời:** Em mới dừng lại ở mảng 2 chiều.
13. **Câu hỏi:** Mảng hai chiều áp dụng vào cái gì?
    *   **Trả lời:** Em nghĩ nó dùng để lưu ma trận, và có ứng dụng nhiều trong AI.
14. **Câu hỏi:** Em có phân biệt được ngăn xếp (stack) và hàng đợi (queue) không?
    *   **Trả lời:** Stack là LIFO (Last In First Out), queue là FIFO (First In First Out). Stack thì em có code trên Leetcode, queue thì em thấy áp dụng nhiều trong tìm kiếm đồ thị.
15. **Câu hỏi:** Link list là gì?
    *   **Trả lời:** Nó là danh sách liên kết, các node liên kết với nhau. Có các loại: đơn, đôi, vòng.
16. **Câu hỏi:** Liên kết đơn là gì?
    *   **Trả lời:** Sử dụng con trỏ để trỏ tới phần tử tiếp theo. Con trỏ là một biến lưu địa chỉ của biến khác.
17. **Câu hỏi:**  Em học kiến thức về con trỏ bao lâu rồi?
    *   **Trả lời:** Khoảng 1 năm trước khi học C và C++.
18. **Câu hỏi:** Về thuật toán, em đã nắm được những gì?
    *   **Trả lời:** Em đã nắm được các thuật toán sắp xếp, tìm kiếm.
19. **Câu hỏi:** Thông thường, em dùng thuật toán sắp xếp gì?
     *   **Trả lời:** Với bài toán nhỏ thì dùng Selection Sort, với bài toán độ phức tạp O(nlogn) thì dùng Merge Sort.
20. **Câu hỏi:** Độ phức tạp O(n²) nghĩa là gì?
    *   **Trả lời:** Ví dụ có 2 vòng for lồng nhau, mỗi vòng chạy n lần thì độ phức tạp là O(n*n) hay O(n²).
21. **Câu hỏi:** Cho dãy số 1 2 3 5 8 13 21...., hãy tìm quy luật và in ra các số thuộc dãy nhỏ hơn n?
    *   **Trả lời:** Dãy số này là dãy Fibonacci. Quy luật là f(n) = f(n-1) + f(n-2). Em đã từng code bài này bằng cả đệ quy và dùng mảng (dùng mảng thì nhanh hơn).
    *   **Lưu ý:** Có thể code hoặc mô tả code bằng lời (nếu không tiện code lúc đó).

**Phần Java Core**

22. **Câu hỏi:** Trong Java, em phân biệt được biến 1 byte, 2 byte, 4 byte nghĩa là gì?
    *   **Trả lời:** Đó là dung lượng bộ nhớ mà biến đó chiếm. 1 byte thì chiếm 1 ô nhớ, 4 byte thì 4 ô nhớ.
23. **Câu hỏi:** Bộ nhớ là gì?
    *   **Trả lời:** Bộ nhớ chính (RAM), còn bộ nhớ phụ là HDD, USB.
24. **Câu hỏi:** Em có phân biệt được float và double?
    *   **Trả lời:** Khác nhau chủ yếu ở kích thước, float là 4 byte, double là 8 byte.
25. **Câu hỏi:**  Em có phân biệt được & và &&?
    *   **Trả lời:** & là toán tử AND bitwise, && là toán tử AND logic. && chỉ quan tâm kết quả cuối cùng, còn & thì xét cả 2 vế.
26. **Câu hỏi:** Em có phân biệt được JDK và JRE?
    *   **Trả lời:** JDK là bộ công cụ phát triển, bao gồm JRE. JRE cung cấp môi trường run-time cho Java.
27. **Câu hỏi:** Em có phân biệt được break và continue?
    *   **Trả lời:** break sẽ dừng vòng lặp, continue sẽ bỏ qua lệnh sau nó trong lần lặp hiện tại và chuyển sang lần lặp tiếp theo.
28. **Câu hỏi:** Hãy nêu các phạm vi tồn tại của biến trong Java?
    *   **Trả lời:** Local, static, global (member variable).
29. **Câu hỏi:** Em có phân biệt được String và char?
    *   **Trả lời:** String là một chuỗi ký tự, char là một ký tự. Char khai báo bằng nháy đơn, String thì nháy đôi. Char là kiểu dữ liệu nguyên thủy, String là kiểu dữ liệu tham chiếu.
30. **Câu hỏi:** Kiểu dữ liệu tham chiếu là gì?
    *   **Trả lời:** Biến lưu trữ địa chỉ của vùng nhớ (heap) nơi chứa dữ liệu, chứ không lưu trữ trực tiếp dữ liệu.
31. **Câu hỏi:** Biến tham chiếu có giống con trỏ không?
    *   **Trả lời:** Cũng tương tự, nhưng Java không có khái niệm con trỏ rõ ràng mà giấu nó đi.
32. **Câu hỏi:** Em hay dùng những phương thức nào của String?
    *   **Trả lời:** toUpperCase(), toLowerCase(), substring(), indexOf(),...
33. **Câu hỏi:** Muốn lấy kích thước của array thì dùng thuộc tính hay hàm?
    *   **Trả lời:** Thuộc tính `.length`.
34. **Câu hỏi:** Muốn lấy kích thước của ArrayList thì dùng gì?
    *   **Trả lời:** Hàm `.size()`.
35. **Câu hỏi:** Array và ArrayList khác nhau gì?
    *   **Trả lời:** Array thì kích thước cố định, ArrayList thì có thể thay đổi kích thước, ArrayList lưu được cả kiểu nguyên thủy và tham chiếu, Array chỉ lưu được 1 loại kiểu.
36. **Câu hỏi:** Khi nào dùng Array, khi nào dùng ArrayList?
    *   **Trả lời:** Nếu biết trước kích thước cụ thể thì dùng Array, không biết thì dùng ArrayList.
37. **Câu hỏi:** List và ArrayList khác nhau như thế nào?
    *   **Trả lời:** List là interface, ArrayList là class implement List.
38. **Câu hỏi:** Em có biết cách đọc file trong Java?
    *   **Trả lời:** Em đã học qua nhưng chưa nhớ rõ.
39. **Câu hỏi:**  Em có biết biểu thức chính quy (regular expression)?
    *   **Trả lời:** Em có nghe qua, dùng để tìm kiếm, nhưng không nhớ rõ cách sử dụng.
40. **Câu hỏi:** Muốn chuyển chuỗi thành số nguyên dùng hàm gì?
    *   **Trả lời:**  `Integer.parseInt()`.
41. **Câu hỏi:** Nếu chuyển chuỗi sai thì nó ném exception gì?
    *   **Trả lời:** Em không nhớ rõ. (Lưu ý: NumberFormatException)
42. **Câu hỏi:** File .jar là gì?
    *   **Trả lời:** Là file được tạo ra khi chương trình Java chạy xong.
43. **Câu hỏi:**  File .java và .class khác nhau gì?
    *   **Trả lời:** .java là file code, .class là file bytecode sau khi compiler biên dịch.
44. **Câu hỏi:** Em có biết khái niệm Build project?
    *   **Trả lời:** Em có nghe ở trong Maven và Gradle.
45. **Câu hỏi:** Lớp và đối tượng khác nhau gì?
    *   **Trả lời:** Lớp là template, đối tượng là instance của lớp.
46. **Câu hỏi:** Đối tượng có thuộc về lớp không?
    *   **Trả lời:** Theo em thì không.
47. **Câu hỏi:** Khi nào đối tượng được tạo thành?
    *   **Trả lời:** Khi dùng constructor và toán tử `new`.
48. **Câu hỏi:** Có mấy mức truy cập của lớp?
    *   **Trả lời:** `public` và `default`.
49. **Câu hỏi:** Có mấy mức truy cập của thành viên trong lớp?
    *   **Trả lời:** `public`, `private`, `protected`, `default`.
50. **Câu hỏi:** `protected` và `default` khác nhau gì?
    *   **Trả lời:** `protected` truy cập được trong cùng package hoặc từ class con khác package, `default` chỉ trong cùng package.
51. **Câu hỏi:** Mức truy cập nào cao hơn, `protected` hay `default`?
    *   **Trả lời:**  `protected` cao hơn.
52. **Câu hỏi:** Constructor mặc định và không mặc định khác nhau gì?
    *   **Trả lời:** Mặc định không tham số (do Java tự sinh nếu mình không viết), không mặc định thì do mình tự custom có tham số.
53. **Câu hỏi:** Em có biết lớp Object?
    *   **Trả lời:** Đó là lớp cha của mọi class trong Java.
54. **Câu hỏi:** Em có phân biệt được quan hệ "is a" và "has a"?
    *   **Trả lời:** "is a" là kế thừa, "has a" là quan hệ thành phần.
55. **Câu hỏi:** Em có phân biệt được overriding và overloading?
    *   **Trả lời:** Overriding thì signature (tên và tham số) giống hệt, overloading thì khác signature.
56. **Câu hỏi:** Cho ví dụ về tính đa hình?
    *   **Trả lời:** Overriding và Overloading đều là đa hình.
57. **Câu hỏi:** Em có phân biệt được đa hình runtime và compile time?
    *  **Trả lời:** Đa hình compile-time (thời gian biên dịch) là overloading, runtime (thời gian chạy) là overriding.
58.  **Câu hỏi:** Em có biết downcasting và upcasting?
     *   **Trả lời:** Upcasting là từ lớp con lên lớp cha, downcasting là ngược lại (nhưng cần ép kiểu tường minh).
59. **Câu hỏi:** Em có biết ép kiểu tường minh và ép kiểu ngầm định?
    *   **Trả lời:** Ngầm định là từ nhỏ lên lớn, tường minh là từ lớn xuống nhỏ (có thể mất mát dữ liệu).
60. **Câu hỏi:**  Trong hướng đối tượng có ép kiểu tường minh và ngầm định không?
     *   **Trả lời:** Dạ có, cũng tương tự như việc ép kiểu giữa các kiểu dữ liệu nguyên thủy
61. **Câu hỏi:** Hai biến tham chiếu có thể trỏ đến cùng 1 đối tượng không?
    *   **Trả lời:**   
62. **Câu hỏi:** Biến tham chiếu được gán `null` nghĩa là gì?
    *   **Trả lời:** Nghĩa là nó không trỏ đến bất kì đối tượng nào trên heap.
63. **Câu hỏi:** Có khi nào đối tượng không được biến nào trỏ tới không?
    *   **Trả lời:** Dạ có, khi mình gán lại giá trị cho biến tham chiếu. JVM sẽ dọn dẹp bộ nhớ này (garbage collection) khi không còn ai dùng tới.
64. **Câu hỏi:** `this` và `super` khác nhau gì?
    *   **Trả lời:** `this` gọi tới đối tượng hiện tại, `super` gọi tới đối tượng cha.
65. **Câu hỏi:** NullPointerException xảy ra khi nào?
    *   **Trả lời:** Khi mình truy cập thành viên (phương thức, biến) của 1 biến mà nó đang mang giá trị null (không trỏ tới object).
66. **Câu hỏi:**  `Sinhvien sinhvien1 = new Sinhvien()` có vấn đề gì không?
    *   **Trả lời:** Dạ không, đây là một khai báo bình thường.
67. **Câu hỏi:**  `sinhvien1` trong câu lệnh trên là gì?
     *   **Trả lời:** Nó là một biến tham chiếu.
68. **Câu hỏi:** Đối tượng đã xuất hiện chưa?
    *   **Trả lời:** Rồi, sau toán tử `new` thì đối tượng được tạo trên heap.
69. **Câu hỏi:**  Vậy `sinhvien1` có `null` không?
    *   **Trả lời:** Không, `sinhvien1` đang trỏ tới đối tượng.
70. **Câu hỏi:**  `Sinhvien sv1; sv1.getHoTen()` có lỗi gì?
    *   **Trả lời:** Có lỗi NullPointerException.
71. **Câu hỏi:**  Chúng ta có thể tạo class kế thừa `java.lang.String` không?
    *   **Trả lời:** Dạ có.
72. **Câu hỏi:** Khi nào thì không thể kế thừa?
     *  **Trả lời:** Khi class đó được khai báo là `final`.
73. **Câu hỏi:** Em hiểu gì về `finally`?
    *   **Trả lời:** Nó luôn được thực thi sau `try` và `catch` (nếu có), kể cả khi có exception hay không.
    *   **Lưu ý:** Cần học thêm về mục đích và công dụng của nó (thường để giải phóng tài nguyên).
    
**Phần JDBC**
74. **Câu hỏi:**  Em biết cách kết nối cơ sở dữ liệu trong Java?
    *   **Trả lời:** Dạ có.
75. **Câu hỏi:** Em biết `ResultSet.next()` không?
    *   **Trả lời:** Dạ có, dùng để lấy từng hàng của kết quả query.
76. **Câu hỏi:** `ResultSet.next()` dùng để làm gì?
    *   **Trả lời:** Nó là lấy ra một hàng từ kết quả truy vấn, không phải trường dữ liệu.
77. **Câu hỏi:**  Em có phân biệt được Java và Java SQL?
     *   **Trả lời:** Em chưa rõ về sự khác nhau của hai loại này.
78. **Câu hỏi:** `Statement` và `PreparedStatement` khác nhau gì?
    *   **Trả lời:** `PreparedStatement` cho phép thêm điều kiện sau, bảo mật hơn `Statement` vì tránh được SQL injection.
 
**Phần Cơ Sở Dữ Liệu (Database)**
79. **Câu hỏi:** Em có học kỹ về SQL không?
    *   **Trả lời:** Em cũng không nhận là kỹ, mới học qua về SQL.
80. **Câu hỏi:** Em có phân biệt được quan hệ 1-1 và 1-nhiều không?
    *   **Trả lời:** (Câu trả lời của ứng viên chưa chính xác) Ví dụ: 1 giáo viên có thể dạy nhiều lớp (1-nhiều).
    *   **Lưu ý:** Cần tìm hiểu thêm và cho ví dụ chính xác hơn.
81. **Câu hỏi:** Khi gặp quan hệ nhiều - nhiều thì ta làm gì?
    *   **Trả lời:** Thêm một bảng quan hệ (junction table) giữa 2 bảng đó để giải quyết. Bảng này sẽ lưu khóa ngoại của 2 bảng kia.
82. **Câu hỏi:** Vì sao phải thêm bảng trung gian đó?
    *   **Trả lời:** (cần tìm hiểu thêm). Ứng viên trả lời có 1 ý đúng là tăng tốc độ truy vấn, tuy nhiên chưa đủ.
83. **Câu hỏi:** Em có phân biệt được `INNER JOIN` và `LEFT JOIN` không?
    *   **Trả lời:** `INNER JOIN` lấy những hàng có dữ liệu ở cả 2 bảng, `LEFT JOIN` lấy tất cả hàng của bảng bên trái và những hàng khớp với bảng phải, không có thì gán NULL.
84. **Câu hỏi:**  Cho một database quản lý sinh viên, yêu cầu liệt kê tất cả sinh viên và điểm môn Tin học đại cương của từng sinh viên thì dùng `INNER JOIN` hay `LEFT JOIN`?
    *   **Trả lời:** Ban đầu dùng `INNER JOIN` vì nghĩ là tất cả sinh viên đều có điểm, sau đó cần tìm hiểu để trả lời chính xác rằng dùng `LEFT JOIN` và bổ sung thêm các điều kiện hiển thị (ví dụ: Nếu chưa có điểm thì sẽ hiển thị chữ "chưa thi").
85. **Câu hỏi:** Em có học `UNION` và `UNION ALL` chưa?
    *   **Trả lời:** Có thể đã học, nhưng cần xem lại.
86. **Câu hỏi:** Em biết các hàm `COUNT`, `SUM`, `MIN`, `MAX`, ... không?
    *   **Trả lời:** Dạ có.
87. **Câu hỏi:** Em biết `GROUP BY` không?
    *   **Trả lời:** Dạ có, dùng để nhóm các hàng có cùng giá trị của cột được chỉ định.
88. **Câu hỏi:** Em cho ví dụ về `GROUP BY`?
    *  **Trả lời:** Ví dụ `GROUP BY` cột giới tính để xem số lượng nam/nữ trong 1 bảng.
    *   **Lưu ý:** Cần lấy ví dụ chính xác, không nên dùng cột giới tính trong bảng lớp học.
89. **Câu hỏi:** Nếu em `SELECT` `hoTen` `FROM Sinhvien GROUP BY gioiTinh` có lỗi không?
    *   **Trả lời:** Dạ có, vì không thể hiển thị tất cả các giá trị `hoTen` trong khi đang nhóm theo `gioiTinh`.
90. **Câu hỏi:** Khi nào thì `SELECT` được, khi nào thì không khi dùng `GROUP BY`?
    *   **Trả lời:** Chỉ `SELECT` được cột dùng để `GROUP BY`, hoặc những cột dùng hàm tổng hợp (COUNT, SUM, MIN, ...).

**Phần Spring Framework**

91.  **Câu hỏi:** Em có học gì về Spring?
    *   **Trả lời:** Em mới học một số khái niệm cơ bản như Dependency Injection (DI) và Inversion of Control (IOC).
92. **Câu hỏi:** IOC là gì?
    *  **Trả lời:** (Câu trả lời chưa chính xác) IOC là đảo ngược lại quyền kiểm soát quá trình tạo đối tượng, thay vì mình tạo thì Spring sẽ tạo đối tượng cho mình.
    *   **Lưu ý:** Cần tìm hiểu bản chất của IOC, vì sao nó cần phải đảo ngược quyền kiểm soát.
93. **Câu hỏi:**  Vì sao lại cần đảo ngược quyền kiểm soát?
     *   **Trả lời:** (Chưa có câu trả lời đúng) Giúp tối ưu năng suất, đơn giản hóa quá trình.
94.  **Câu hỏi:** Dependency Injection (DI) là gì?
    *   **Trả lời:** Là khi đánh dấu để Spring tiêm phụ thuộc vào constructor hoặc method hoặc trường.
95. **Câu hỏi:** DI có liên quan gì đến IOC?
    *   **Trả lời:** (Câu trả lời chưa rõ ràng).  Cần làm rõ mối quan hệ giữa hai khái niệm này (DI là hiện thực của IOC)

**Tổng Kết**
*   **Điểm mạnh:** Nắm khá chắc kiến thức Java Core, tư duy logic tốt, có khả năng tự học và nghiên cứu, thái độ nghiêm túc.
*   **Điểm yếu:** Kiến thức còn nhiều chỗ mơ hồ, chưa hiểu rõ bản chất, kiến thức về cơ sở dữ liệu chưa tốt, thiếu kinh nghiệm thực tế (frontend), chưa có kinh nghiệm làm việc nhóm, cần bổ sung kiến thức về Spring Framework.
*   **Lời khuyên:**
    *   Tiếp tục học hỏi và thực hành nhiều hơn.
    *   Nghiên cứu kỹ bản chất của vấn đề, không chỉ học thuộc lòng lý thuyết.
    *   Tham gia các dự án thực tế để có thêm kinh nghiệm.
    *   Luyện tập phỏng vấn để trả lời tự tin hơn.

Hy vọng danh sách này giúp bạn hiểu rõ hơn về các câu hỏi và câu trả lời. Chúc bạn thành công!
