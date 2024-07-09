# Global trong NodeJS
 - Là một object có tên là global. Gồm các giá trị:
   <img width="552" alt="image" src="https://github.com/system01no2l/noteNode/assets/86253573/fa1c435e-bd8f-416d-b7b3-ace68f8aca0c">

 - Mỗi tệp tương ứng với một module và có 1 Module Scope riêng
 - Truy cập biến global trực tiếp từ các tệp khác mà không sử dụng các cơ chế như module.exports hoặc require

# Global trong Browser
 - Là đối tượng window
 - Truy cập thông qua thuộc tính window
```
   // Định nghĩa biến toàn cục
window.myGlobalVariable = "Hello, world!";

// Truy cập biến toàn cục
console.log(window.myGlobalVariable); // Output: Hello, world!
```
- Định nghĩa một biến không thuộc hàm hay đối tượng nào thì nó thuộc quản lý của window

```
// Định nghĩa biến toàn cục
var myGlobalVariable = "Hello, world!";

// Truy cập biến toàn cục
console.log(window.myGlobalVariable); // Output: Hello, world!
```
