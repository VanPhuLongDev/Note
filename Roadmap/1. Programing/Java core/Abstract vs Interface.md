Abstract class : Khi chúng ta nói về abstract class có nghĩa là chúng ta đang mong muốn định nghĩa ra một <span style="background:#affad1">nét đặc trưng</span> của object đó, cho mọi người biết object đó là như thế nào
 
Interface : Khi chúng ta nói về Interface có nghĩa là chung ta muốn nói đến việc chúng ta hứa là object của chúng ta <span style="background:#affad1">có thể làm gì</span> (có method gì trong đó)
 
Giả sử như chúng ta có một class là Car (ô tô) extend từ abstract class FourWheelsVehicle (phương tiện 4 bánh), trong FourWheelsVehicle mình sẽ có vài method là startup() run() chẳng hạn, thì khi Car extend FourWheelsVehicle thì cũng sẽ có các method đó luôn, có nghĩa là nếu bạn đã là một FourWheelsVehicle thì bạn phải có method run() startup() (đã là xe 4 bánh thì phải khởi động lên được - Startup và chạy được - Run()) đó là nét đặc trưng, vậy như đã nói ở trên thì abstract class sử dụng khi chúng ta muốn định nghĩa nét đặc trưng của class.
*** 
Tiếp tục với interface, có thể là bạn tạo nên một interface là ICar đi, và trong đó bạn định nghĩa vài method là PlayMusic() Fly(). Thì nếu Car mà implement interface ICar thì Car phải bắt buộc có method PlayMusic() và Fly(), đó là "lời hứa" mà chúng ta phải làm như đã nói ở trên. Tuy nhiên đây không
