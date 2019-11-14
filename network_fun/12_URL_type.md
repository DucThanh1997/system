1. Bạn gõ url lên thanh địa chỉ của trình duyệt và nhấn enter

2. Trình duyệt của bạn sẽ tìm kiếm địa chỉ IP cho URL mà bạn gõ
- Đầu tiên, trình duyệt sẽ tìm kiếm địa chỉ IP trong file host của máy tính trước
- Nếu không có địa chỉ IP và url trong file host thì nó sẽ tìm kiếm trong cache của trình duyệt, của máy, của router
- Nếu vẫn không có thì trình duyệt sẽ gửi DNS query đến DNS Server để tìm địa chỉ IP cho URL mà bạn gõ

3. Sau khi có được địa chỉ IP thì trình duyệt sẽ thiết lập 1 kết nối TCP đến địa chỉ IP của server đó
- Trình duyệt sẽ thực hiện quá trình bắt tay ba bước để thiết lập kết nối giữa trình duyệt và server để bắt đầu quá trình truyền tải dữ liệu

4. Trình duyệt sẽ gửi HTTP request đến web server

5. Server xử lý request và trả về response

6. Trình duyệt hiện thỉ nọi dung HTML