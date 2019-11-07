# Mô hình TCP/IP
## Định nghĩa
- TCP/IP là một bộ giao thức trao đổi thông tin được sử dụng để truyền tải và kết nối các thiết bị trong mạng Internet.
- TCP/IP được phát triển để mạng được tin cậy hơn cùng với khả năng phục hồi tự động

## Chức năng của các tầng trong mô hình TCP/IP
- Bao gồm 4 lớp được chồng lên nhau, bắt đầu từ tầng thấp nhất là Tầng Vật lý và cuối cùng là tần ứng dụng dụng

### Tầng ứng dụng
- Đảm nhận vai trò giap tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau

- Dữ liệu khi đến đây sẽ được định dạng theo kiểu Byte nối Byte, cùng với đó là các thông tin định tuyến giúp xác định đường đi đúng của 1 gói tin 

### Tầng giao vận
- Xử lí các vần đề giao tiếp giữa các máy chủ trong cùng 1 mạng hoặc khác mạng được kết nối với nhau thông qua bộ định tuyến.

- Trước khi chuyển đi dữ liệu sẽ được phân đoạn có thể không bằng nhau nhưng chắc chắn nhỏ hơn 64kb. Gói là 1 Segment

- 1 Segment bao gồm phần header chứa thông tin điều khiển và sau đó là dữ liệu

- Trong tầng này còn bao gồm 2 giao thức cốt lõi là TCP và UDP. Trong đó, TCP đảm bảo chất lượng gói tin nhưng tiêu tốn thời gian khá lâu để kiểm tra đầy đủ thông tin từ thứ tự dữ liệu cho đến việc kiểm soát vấn đề tắc nghẽn lưu lượng dữ liệu. Trái với điều đó, UDP cho thấy tốc độ truyền tải nhanh hơn nhưng lại không đảm bảo được chất lượng dữ liệu được gửi đi.

### Tầng network
- Đóng gói dữ liệu và tìm đường đi cho các gói tin

- Giao thức chính là IP, ICMP và ARP

### Tầng vật lý
- Chịu trách nhiệm việc truyền dữ liệu

# So sánh
- TCP/IP được nhiều người tin cậy hơn vì TCP/IP cho phép nới lỏng các quy tắc và cung cấp các nguyên tắc chung

- Sự kết hợp giữa các tầng với nhau. TCP/IP có tầng phiên và tầng trình diễn kết hợp với nhau trong tầng ứng dụng còn OSI mỗi tầng khác nau sẽ thực hiện một nhiệm vụ khác nhau

