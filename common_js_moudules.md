# CommonJS Module trong Node.js

## 1. Module trong Node.js

### Định nghĩa
Trong Node.js, mỗi file JavaScript được xem như là một module. Mỗi module có một phạm vi riêng biệt, giúp tránh xung đột biến toàn cục và hỗ trợ tái sử dụng mã nguồn.

### Xuất và nhập (Exports and Imports)
Node.js sử dụng hệ thống module dựa trên CommonJS. Để xuất các giá trị từ một module, bạn sử dụng `module.exports` hoặc `exports`. Để nhập các giá trị từ một module khác, bạn sử dụng `require()`.

## 2. `exports` và `module.exports`

### `exports`
`exports` là một biến đối tượng được cung cấp sẵn cho mỗi module. Bạn có thể gán các thuộc tính và phương thức cho `exports`, nhưng không thể gán trực tiếp một giá trị mới cho `exports` mà không ảnh hưởng đến `module.exports`.

**Ví dụ:**
```
// File math.js
exports.subtract = function(a, b) {
    return a - b;
};
```
### `module.exports`
`module.exports` là giá trị thực sự được xuất ra của module. Bạn có thể gán trực tiếp một giá trị mới cho module.exports,
ví dụ như một hàm, một đối tượng, hoặc một giá trị nguyên thủy để xuất ra từ module khi được yêu cầu.

```
// File math.js
module.exports = {
    add: function(a, b) {
        return a + b;
    }
};
```

### Lưu ý khi sử dụng `exports` và `module.exports`
- Sử dụng module.exports khi: Bạn muốn xuất ra một đối tượng, hàm, hoặc giá trị nguyên thủy nhất định từ module.
  Ví dụ, khi bạn muốn thay đổi hoặc ghi đè toàn bộ giá trị xuất ra của module.
    
- Tránh gán trực tiếp cho exports khi: Bạn cần xuất ra một giá trị mới hoặc thay đổi đáng kể module.exports.
  Nếu gán trực tiếp một giá trị mới cho exports, nó sẽ không thay đổi giá trị của module.exports.
