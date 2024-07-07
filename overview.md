# Nodejs vs Browser

## Differenciens between the NodeJS and Browse
  - NodeJS
    - Không có giao diện người dùng, chạy trên V8 chạy trên Linux, Windowns, ... được dùng làm server side
    - Không có sandboxing (có thể truy cập file hệ thống, ghi đọc ....)
    - Sử dụng các common module JS (export, require, ...)
    - Sử dụn các API , module có sẵn như http, chil_process, https, file, path ...
    - Không có thao tác với DOM (Document Object Model)
  - Browser
    - Thao tác với DOM (Dọcumnet Object Model)
    - Bị giới hạn Sandboxed (quyền truy cập vào file hệ thống bị hạn chế) -> bảo mật
    - Không sử dụng được các common module JS (export, require) mà sử dụng ES6
    - Sử dụng làm client side
