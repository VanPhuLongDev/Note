
> [!NOTE] Quay lui và đệ quy là khác nhau
> - **Đệ quy** là một kỹ thuật lập trình cho phép một hàm gọi chính nó để giải quyết các bài toán con.
> - **Quay lui** là một phương pháp giải quyết vấn đề mà trong đó ta thử nghiệm các khả năng và quay lại khi phát hiện rằng một khả năng không dẫn đến giải pháp. Quay lui thường được cài đặt bằng cách sử dụng đệ quy để duyệt qua các lựa chọn.
> - **Quay lui** sử dụng **đệ quy**, nhưng không phải tất cả các hàm **đệ quy** đều là **quay lui**

Tóm lại, quay lui sử dụng đệ quy, nhưng không phải tất cả các hàm đệ quy đều là quay lui.

## 1. Liệt kê dãy số thập phân

![[Untitled-20240913214154619.webp]]
Sử dụng quay lui:
```java
public class M211 {  
    public static void generateBinarySequence(int n) {  
        int[] arr = new int[n];  
        backtrack(arr, 0, n);  
    }  
  
    private static void backtrack(int[] arr, int i, int n) {  
        if (i == n) {  
  
            printArray(arr);  
        } else {  
  
            arr[i] = 0;  
            backtrack(arr, i + 1, n);  
  
            arr[i] = 1;  
            backtrack(arr, i + 1, n);  
        }  
    }  
  
    private static void printArray(int[] arr) {  
        for (int num : arr) {  
            System.out.print(num);  
        }  
        System.out.println();  
    }  
  
    public static void main(String[] args) {  
        int n = 7;  
        generateBinarySequence(n);  
    }  
}
```

### Khởi tạo:

- `n = 2`, mảng `arr = [0, 0]` được tạo ra để lưu dãy nhị phân với độ dài 2.
- Hàm `generateBinarySequence(2)` được gọi và từ đó gọi `backtrack(arr, 0, 2)`.
### Lần gọi `backtrack(arr, 0, 2)`:
- Ở bước này, giá trị `i = 0`, tức là đang ở vị trí đầu tiên trong mảng `arr`. Chương trình sẽ thử 2 giá trị là `0` và `1` cho vị trí này.
#### Thử giá trị `0` ở vị trí `i = 0`:
- `arr[0] = 0`, sau đó gọi đệ quy `backtrack(arr, 1, 2)`.
###  Lần gọi `backtrack(arr, 1, 2)`:
- Bây giờ, `i = 1`, tức là đang ở vị trí thứ hai trong mảng. Chương trình sẽ lại thử 2 giá trị là `0` và `1`.
####  Thử giá trị `0` ở vị trí `i = 1`:
- `arr[1] = 0`, sau đó gọi đệ quy `backtrack(arr, 2, 2)`.
### Lần gọi `backtrack(arr, 2, 2)`:
- Ở bước này, `i = 2`, tức là đã điền đủ giá trị vào tất cả các vị trí trong mảng (vì `i == n`).
- Mảng hiện tại là `[0, 0]`, chương trình sẽ in ra `000`.
- Quay lui về bước trước (tức là quay về `i = 1`).
#### Thử giá trị `1` ở vị trí `i = 1`:
- Sau khi quay lui, `arr[1] = 1`, sau đó gọi đệ quy `backtrack(arr, 2, 2)`.
### Lần gọi `backtrack(arr, 2, 2)` (lần thứ hai):
- Lúc này, mảng là `[0, 1]`, chương trình sẽ in ra `01`.
- Quay lui về bước trước (tức là quay về `i = 0`).
### Quay lại `backtrack(arr, 0, 2)`:
- Bây giờ, sau khi đã thử với `arr[0] = 0`, chương trình thử tiếp giá trị `1` cho vị trí `i = 0`.
#### Thử giá trị `1` ở vị trí `i = 0`:
- `arr[0] = 1`, sau đó gọi đệ quy `backtrack(arr, 1, 2)`.
### Lần gọi `backtrack(arr, 1, 2)` (lần thứ hai):
- Giống như lần trước, chương trình sẽ thử 2 giá trị `0` và `1` cho `i = 1`.
#### Thử giá trị `0` ở vị trí `i = 1`:
- `arr[1] = 0`, sau đó gọi đệ quy `backtrack(arr, 2, 2)`.
### Lần gọi `backtrack(arr, 2, 2)` (lần thứ ba):
- Mảng hiện tại là `[1, 0]`, chương trình sẽ in ra `10`.
- Quay lui về bước trước (tức là quay về `i = 1`).
#### Thử giá trị `1` ở vị trí `i = 1`:
- Sau khi quay lui, `arr[1] = 1`, sau đó gọi đệ quy `backtrack(arr, 2, 2)`.
### Lần gọi `backtrack(arr, 2, 2)` (lần thứ tư):
- Mảng hiện tại là `[1, 1]`, chương trình sẽ in ra `11`.
- Quay lui về bước trước và kết thúc quá trình vì đã thử tất cả các giá trị.

