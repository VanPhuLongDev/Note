## 1. Mức độ ưu tiên của properties và yaml
a. Properties
![](w.save/Basic-20241207093115595.webp)
- Ưu tiên theo thứ tự File bên trong folder config ở thư mục ngoài -> file ở thư mục ngoài -> file trong thư mục config bên trong resource -> file trong resource
- Cách sử dụng : dùng anotation value

b. So sánh properties và yaml:
- properties sử dụng key và value
- yaml cấu trúc phân cấp và thụt 

| Properties                   | Yaml                                      |
| ---------------------------- | ----------------------------------------- |
| Sử dụng key và value         | Cấu trúc phân nhánh và thụt lề            |
| Chỉ dùng được string         | Support nhiều kiểu ( string int bool map) |
| Được Spring boot ưu tiên hơn | Ít được ưu tiên hơn                       |

## 2. Chuyển đổi profile dev test prod
![](w.save/Basic-20241207094834816.webp)
Cú pháp application-{enviroment}.yaml/properties
Phải có file gốc application.yaml để config những cái chung

## 3. Folder structure 
![](w.save/Basic-20241207095354326.webp)
