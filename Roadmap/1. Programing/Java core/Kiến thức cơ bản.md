## I. Giới thiệu
### 1. Java là gì?
Java là một một ngôn ngữ lập trình hiện đại, bậc cao, hướng đối tượng, bảo mật và mạnh mẽ. và là một Platform.

**Java** is a programming language that is modern, easy to use, and secure. It is also a platform because it has a special environment (JVM) where Java code can run on any device.

### 2. What is the difference between JDK, JRE, and JVM?
JDK (Java Development Kit) là một Kit cung cấp môi trường để phát triển và thực thi (chạy) chương trình Java. JDK là một bộ (hoặc gói) bao gồm hai thứ:  
+ Công cụ phát triển (để cung cấp một môi trường để phát triển các chương trình java của bạn)  
+ JRE (để thực thi chương trình java của bạn).

JRE (Java Runtime Environment) là một gói cài đặt cung cấp một môi trường để chỉ chạy (không phát triển) chương trình java (hoặc ứng dụng) vào máy của bạn. JRE chỉ được sử dụng bởi những người chỉ muốn chạy các chương trình Java là người dùng cuối của hệ thống của bạn. 

JVM (Java Virtual Machine) là một phần rất quan trọng của cả JDK và JRE vì nó được chứa hoặc có sẵn trong cả hai. Bất cứ chương trình Java nào bạn chạy bằng JRE hoặc JDK đều đi vào JVM và JVM chịu trách nhiệm thực thi chương trình java từng dòng, do đó nó còn được gọi là interpreter.

### 3. Heap và Stack
Bộ nhớ Heap là bộ nhớ được sử dụng ở runtime (Khi chương trình đang chạy) để lưu các Objects(các đối tượng) . Bất cứ khi nào ở đâu trong chương trình của bạn khi bạn tạo Object thì nó sẽ được lưu trong Heap (thực thi toán tử new)  

Dung lượng Heap thường lớn hơn Stack.  

Bộ nhớ stack để lưu các biến local trong hàm.  

Các biến local bao gồm loại nguyên thuỷ (primitive) và loại tham chiếu tới đối tượng trong heap (reference) khai báo trong hàm, hoặc đối số được truyền vào hàm, thường có thời gian sống ngắn.  

Bộ nhớ stack thường nhỏ.

### 4. File có tên trống ".java" có hợp lệ không?
Có, bạn có thể lưu file java với tên ".java", sau đó biên dịch bằng lệnh **javac .java** và chạy bằng lệnh **java ten_lop**. Ví dụ:
Biên dịch: **javac .java**
Run: **java A**

### 5. Chuyện gì xảy ra nếu khai báo static public void thay vì public static void?
Chương trình được biên dịch và run đúng.

### 6. Giá trị mặc định của các biến local là gì?
Các biến local không được khởi tạo với bất kỳ giá trị mặc định nào, bất kể là nguyên thủy hay tham chiếu đối tượng.

### 7. This keyword
Tham chiếu tới đối tượng của lớp hiện tại. 

### 8. Tại sao Java không phải là hướng đối tượng 100%?

Java không phải là ngôn ngữ hướng đối tượng hoàn toàn vì Java có sử dụng cả các loại dữ liệu khác như byte, char, float, v.v.

### 9. Trình biên dịch JIT trong Java

Trình biên dịch JIT trong Java hay còn được biết đến với tên gọi Just-In-Time – là một kỹ thuật biên dịch các phần mã byte có các chức năng tương tự trong cùng một thời gian, qua đó giảm thời gian biên dịch cần thiết.

## II. Biến, Kiểu dữ liệu, Arrays, Function
### 1. Explain the 'final' keyword in Java
Từ khóa final để tuyên bố các biến , method, class không thể bị thay đổi.  
- Biến: Không thể thay đổi giá trị, nếu chưa gán giá trị thì có thể gán trong constructor.  
- Method: Không thể ghi đè ( overriding )  
- Class: Không thể kế thừa class

### 2. Static
Method và biến static thuộc về lớp chứ k thuộc về đối tượng của lớp, tất cả đối tượng đều dùng chung. Method static chỉ được truy cập biến static, method static có thể gọi mà k cần tạo đối tượng

### 3. equals() vs ==
equals so sánh giá trị của object, == so sánh địa chỉ bộ nhớ  
String str1 = new String("Hello");  
String str2 = new String("Hello");  
boolean referenceComparison = (str1 == str2); // false (different objects)  
boolean contentComparison = str1.equals(str2); // true (same content)

### 4. instanceof
Kiểm tra xem có phải là một đối tượng của lớp nào đó không, nếu nó là đối tượng của lớp con thì nó cũng là đối tượng của lớp cha

### 5. String vs StringBuffer vs StringBuilder
Lớp String là bất biến (immutable).
Lớp StringBuffer là có thể sửa đổi (mutable).
Khi bạn thực hiện nối nhiều chuỗi thì lớp String xử lý chậm và tốn nhiều bộ nhớ hơn, bởi vì mỗi lần nối thêm chuỗi nó tạo ra instance mới. 
StringBuffer là đồng bộ (synchronized) tức là luồng an toàn. 
Điều này có nghĩa là không thể có 2 luồng cùng truy cập phương thức của lớp StringBuffer đồng thời.StringBuilder là không đồng bộ (non-synchronized) tức là luồng không an toàn. Điều này có nghĩa là có 2 luồng cùng truy cập phương thức của lớp StringBuilder đồng thời. StringBuffer không hiệu quả bằng StringBuilder.

### 6. What primitive types do you know?
8 primitive data types: byte, short, int, long, float, double, boolean, char.

### 7. String Pool in Java
String Pool là một phần của bộ nhớ heap trong Java, nơi các đối tượng String được lưu trữ. Khi bạn tạo một chuỗi trong Java, JVM sẽ kiểm tra xem chuỗi đó đã tồn tại trong String Pool hay chưa:

Nếu chuỗi đã tồn tại, nó sẽ trả về tham chiếu đến chuỗi đó.
Nếu không, nó sẽ tạo một đối tượng String mới và lưu trữ nó trong String Pool.
Ví dụ:
```java
public class StringPoolExample {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = "Hello";

        System.out.println(str1 == str2); // In ra true, vì cả hai tham chiếu đến cùng một đối tượng trong String Pool

        String str3 = new String("Hello");
        System.out.println(str1 == str3); // In ra false, vì str3 là một đối tượng mới không trong String Pool
    }
}
```

Vấn đề liên quan đến String
1. So sánh chuỗi:
	Sử dụng == để so sánh tham chiếu, không phải nội dung.
	Sử dụng .equals() để so sánh nội dung của chuỗi.
2. Immutable Strings:
	Các đối tượng String trong Java là bất biến (immutable). Khi bạn thay đổi một chuỗi, một đối tượng mới được tạo ra.
	```java
	String str = "Hello";
	str = str + " World"; // Tạo một đối tượng mới
	```
3. Performance:

	Nếu bạn thực hiện nhiều thao tác nối chuỗi, sử dụng StringBuilder hoặc StringBuffer sẽ hiệu quả hơn, vì chúng cho phép thay đổi nội dung mà không tạo ra nhiều đối tượng mới.
	Ví dụ về StringBuilder:
	```java
	public class StringBuilderExample {
	    public static void main(String[] args) {
	        StringBuilder sb = new StringBuilder("Hello");
	        sb.append(" World");
	        System.out.println(sb.toString()); // In ra: Hello World
	    }
	}
	```

### 8. Stream API
Stream API là một trong những feature chính của java 8 khi nó được giới thiệu, toàn bộ nằm trong package _java.util.stream_ , gồm những API xử lý tuần tự các element cho collection.

## III. Collections & collection
Tổng quan:
![[Kiến thức cơ bản-20240728201932070.webp]]

![[Kiến thức cơ bản-20240728202130645.webp]]


### 1. Array vs ArrayList
- Kích thước arr cố định, k thay đổi được, còn arrlist thì mặc định ban đầu là 10, sau đó tự tăng thêm  
- arr có thể lưu nguyên thủy (int) và đối tượng (Integer), còn arrlist chỉ lưu đối tượng, nếu cố tình add int vào thì nó sẽ tự động convert qua nhờ cơ chế auto-boxing.  
- arr thao tác vào lưu trữ nhanh hơn  
- arr chỉ có một thuộc tính

### 2. What is the Java Collections Framework?  Giải thích về khung collections trong Java và mục đích của nó
Java Collections Framework là một tập hợp các lớp và interface trong Java, cung cấp các cấu trúc dữ liệu và các thuật toán để lưu trữ, quản lý và thao tác với dữ liệu.

### 3. What are the main interfaces of the Java Collections Framework?
- Collection: Interface gốc cho tất cả các loại collection, đại diện cho một nhóm các đối tượng.
- List: Kế thừa từ Collection, cho phép lưu trữ các phần tử có thứ tự và cho phép trùng lặp. Ví dụ: ArrayList, LinkedList.
- Set: Cũng kế thừa từ Collection, không cho phép trùng lặp và không có thứ tự. Ví dụ: HashSet, TreeSet.
- Queue: Kế thừa từ Collection, được sử dụng để lưu trữ các phần tử theo thứ tự mà chúng được thêm vào, thường dùng cho các tác vụ hàng đợi. Ví dụ: LinkedList, PriorityQueue.
- Map: Mặc dù không kế thừa từ Collection, nó lưu trữ các cặp key-value. Ví dụ: HashMap, TreeMap.
- SortedSet: Kế thừa từ Set, lưu trữ các phần tử theo thứ tự tự nhiên hoặc theo một Comparator.
- SortedMap: Kế thừa từ Map, lưu trữ các cặp key-value theo thứ tự tự nhiên của key hoặc theo một Comparator.

### 4. What is the difference between List and Set?
- Trật tự:
	- List: Lưu trữ các phần tử theo thứ tự, cho phép truy cập theo chỉ số (index).
	- Set: Không có thứ tự cụ thể, không đảm bảo thứ tự của các phần tử.
- Trùng lặp:
	- List: Cho phép các phần tử trùng lặp.
	- Set: Không cho phép các phần tử trùng lặp; mỗi phần tử phải là duy nhất.
- Các lớp triển khai:
	- List: Các lớp phổ biến bao gồm ArrayList, LinkedList.
	- Set: Các lớp phổ biến bao gồm HashSet, TreeSet.
- Hiệu suất:
	- List: Thao tác như thêm, xóa, và truy cập phần tử có thể có hiệu suất khác nhau tùy thuộc vào loại List.
	- Set: Thao tác thêm, xóa có thể nhanh hơn với HashSet vì sử dụng bảng băm.

### 5. Can you explain the difference between ArrayList and LinkedList?

| Array List                                                    | LinkedList                                                                       |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Sử dụng bộ nhớ ít hơn                                         | Sử dụng bộ nhớ nhiều hơn ( do phải lưu các tham chiếu đến node trước và sau nó)  |
| Các thao tác như chèn, xoá chậm                               | Các thao tác chèn xoá rất nhanh                                                  |
| Truy cập các dữ liệu hiệu quả vì sử dụng chỉ mục              | Truy cập các dữ liệu chậm chạp do phải duyệt qua từng node                       |
| ArrayList chỉ có thể hoạt động như 1 list thông thường        | LinkedList có thể hoạt động như ArrayList, stack, queue                          |
| Nó được sử dụng để chỉ lưu trữ các loại dữ liệu tương tự.     | Nó được sử dụng để lưu trữ bất kỳ loại dữ liệu nào.                              |
| Lớp này sử dụng một mảng động để lưu trữ các phần tử trong đó | Lớp này sử dụng một danh sách được liên kết kép để lưu trữ các phần tử trong đó. |
ArrayList: Khi bạn cần truy cập nhanh đến các phần tử và số lượng phần tử không thay đổi nhiều. Thích hợp cho các tình huống cần tìm kiếm và truy cập thường xuyên.

LinkedList: Khi bạn cần thêm hoặc xóa phần tử thường xuyên, đặc biệt là ở đầu hoặc cuối danh sách. Thích hợp cho các tình huống cần thao tác với danh sách mà không quan tâm đến chỉ số.

### 6. What is a HashSet and how does it work?
HashSet sử dụng một đối tượng hashmap bên trong để lưu trữ phần tử, Khi  thêm một phần tử vào thì nó sẽ dùng phần tử đó làm key và một dummpy object làm value. Mã nguồn của hashset:
```java
private transient HashMap<E,Object> map; 
// tao dummy value de lien ket voi doi tuong map 
private static final Object PRESENT = new Object(); 
public boolean add(E e) { 
	return map.put(e, PRESENT)==null; 
}
```

HashSet trong Java là một lớp thuộc Java Collections Framework, được sử dụng để lưu trữ các phần tử duy nhất mà không có thứ tự cụ thể. 

### 7. What is the difference between HashMap and TreeMap?
**Cấu trúc dữ liệu:**
- HashMap: Sử dụng bảng băm (hash table) để lưu trữ các cặp key-value.
- TreeMap: Sử dụng cấu trúc red-black tree, một loại cây nhị phân tự cân bằng, để lưu trữ các cặp key-value.
**Thứ tự:**
- HashMap: Không đảm bảo thứ tự của các phần tử. Thứ tự có thể thay đổi khi các phần tử được thêm hoặc xóa.
- TreeMap: Đảm bảo thứ tự của các keys. Các keys sẽ được sắp xếp theo thứ tự tăng dần hoặc thứ tự do người dùng tự định nghĩa
**Hiệu suất:**
- HashMap:Thêm, xóa, và tìm kiếm có thời gian trung bình O(1).
- TreeMap:Thêm, xóa, và tìm kiếm có thời gian O(log n) do cần duy trì cấu trúc cây.
**Null Keys và Values:**
- HashMap: Cho phép một key null và nhiều values null.
- TreeMap: Không cho phép key null (nếu sử dụng thứ tự tự nhiên), nhưng cho phép nhiều values null.
**Tính năng bổ sung:**
- HashMap: Thích hợp cho các tình huống cần hiệu suất cao mà không cần quan tâm đến thứ tự.
- TreeMap: Thích hợp khi bạn cần duy trì thứ tự của các keys, chẳng hạn như khi cần duyệt qua các keys theo thứ tự.


### 8. What is a Queue and how is it different from a Stack?
Queue sử dụng nguyên tắc FIFO, trong khi Stack sử dụng nguyên tắc LIFO.

### 9. How do you convert a List to an array in Java?
Dùng toArray()

### 10. What are generics and how do they relate to collections?
Generics cho phép bạn tạo ra các cấu trúc dữ liệu có thể làm việc với nhiều kiểu dữ liệu khác nhau mà không cần phải ép kiểu (casting) khi sử dụng.

Ví dụ, bạn có thể định nghĩa một lớp Box<T.> mà có thể chứa bất kỳ kiểu dữ liệu nào (như Integer, String, v.v.) thông qua tham số kiểu T.

### 11. How do you sort a List in Java?
Collections.sort(), List.sort()

### 12. What is the difference between shallow copy and deep copy?

### 13. How can you remove duplicates from a List?
- Sử dụng Set: Dễ dàng và nhanh chóng để loại bỏ trùng lặp.
- Sử dụng Streams: Hiện đại và ngắn gọn, phù hợp với Java 8 trở lên.
- Sử dụng vòng lặp: Cung cấp kiểm soát nhiều hơn nhưng có thể kém hiệu quả hơn.

### 14. HashSet vs HashMap
HashSet stores unique elements, các phần tử k lưu theo thứ tự nào, hashset không cung cấp phương thức truy xuất qua index. Nếu thêm phần tử trùng lặp thì nó sẽ không được thêm vào

HashMap lưu key-value, unique key, value can duplicate. Nếu thêm một key trùng lặp thì value sẽ bị overwritten

VD:  
HashSet lưu list username 
HashMap lưu list username-profile


## IV. OOP, Class, Tính chất của OOP
> Các thuộc tính và phương thức private k thể kế thừa. Có thể truy cập thuộc tính private thông qua phương thức public
### 1. OOP là gì
là một phương pháp hay mô hình giúp tăng năng suất, đơn giản hóa việc bảo trì, dễ dàng mở rộng trong thiết kế phần mềm bởi việc cung cấp một vài khái niệm như:

- Đối tượng (Object)
- Lớp (Class)
- Kế thừa (Inheritance)
- Đa hình (Polymorphism)
- Trừu tượng (Abstraction)
- Đóng gói (Encapsulation)

### 2. Lập trình hướng đối tượng có mấy tính chất:
Có 4 tính chất:
- Kế thừa: Kế thừa cho phép một lớp (lớp con) kế thừa các thuộc tính và phương thức từ một lớp khác (lớp cha). Điều này giúp tái sử dụng mã nguồn.
- Đóng gói: Đóng gói là việc che giấu dữ liệu của đối tượng khỏi các đối tượng khác và chỉ cho phép truy cập thông qua các phương thức công khai (public methods).
- Trừu tượng: Trừu tượng là sự ẩn đi những chi tiết bên trong và hiển thị ra các chức năng, tính chất này gọi là trừu tượng. Trừu tượng là việc định nghĩa một lớp hoặc phương thức mà không cung cấp chi tiết cụ thể về việc thực hiện. Nó cung cấp một cách để làm việc với các đối tượng thông qua giao diện chung.
- Đa hình: Đa hình cho phép một phương thức có nhiều cách thực hiện khác nhau. Điều này có thể đạt được thông qua ghi đè phương thức (method overriding) hoặc nạp chồng phương thức (method overloading).

### 3. Access Modifier
- Public: tất cả phạm vi  
- Protected: Ngoài package bởi lớp con  
- default: Trong package  
- private: Trong lớp

### 4. super
Tham chiếu đến đối tượng lớp cha gần nhất. Ví dụ như A kế thừa B, Trong A overringding các variable và method của lớp cha r, nhưng nếu t muốn gọi các variable hoặc method của lớp cha thì t có thể dùng super.
1. Từ khóa super được sử dụng để tham chiếu trực tiếp đến biến instance của lớp cha gần nhất.
2. super() được sử dụng để gọi trực tiếp Constructor của lớp cha.
3. Từ khóa super được sử dụng để gọi trực tiếp phương thức của lớp cha.

### 5. Abstract vs Interface ( ly thuyet )
| Abstract class                                                                                                   | Interface                                                                                               |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| 1) Abstract class có phương thức **abstract** (không có thân hàm) và phương thức **non-abstract** (có thân hàm). | Interface chỉ có phương thức **abstract**. Từ java 8, nó có thêm **các phương thức default và static**. |
| 2) Abstract class **không hỗ trợ đa kế thừa**.                                                                   | Interface **có hỗ trợ đa kế thừa**                                                                      |
| 3) Abstract class có các biến **final, non-final, static and non-static**.                                       | Interface chỉ có các biến **static và final**.                                                          |
| 4) Abstract class **có thể cung cấp nội dung cài đặt cho phương thức của interface**.                            | Interface **không thể cung cấp nội dung cài đặt cho phương thức của abstract class**.                   |
| 5) Từ khóa **abstract** được sử dụng để khai báo abstract class.                                                 | Từ khóa **interface** được sử dụng để khai báo interface.                                               |
| 6) Ví dụ:  <br>public abstract class Shape {  <br>public abstract void draw();  <br>}                            | Ví dụ:  <br>public interface Drawable {  <br>void draw();  <br>}                                        |
### 6. Abstract vs Interface ( Cach dung )
- Khi chúng ta nói về abstract class có nghĩa là chúng ta đang mong muốn định nghĩa ra một nét đặc trưng của object đó, cho mọi người biết object đó là như thế nào  
  
- Interface : Khi chúng ta nói về Interface có nghĩa là chung ta muốn nói đến việc chúng ta hứa là object của chúng ta có thể làm gì(có method gì trong đó)

### 7. Phương thức equals() và hashCode() trong java

## VI. Exception, I/O

