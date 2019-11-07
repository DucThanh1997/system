# TCP
## Định nghĩa
- Nó là giao thức điều khiển truyền vận thuộc giao thức cốt lõi của bộ giao thức TCP/IP
- Thông qua TCP, các ứng dụng trên các máy chủ được nối mạng có thể liên lạc với nhau, qua đó chúng có thể trao đổi dữ liệu hoặc các gói tin
- Giao thức này đảm bảo việc chuyển giao dữ liệu tới nhận 1 cách đáng tin cậy và đúng thứ tự

## Các tính năng
- TCP là giao thức hướng kết nối, có nghĩa là buộc phải thiết lập kết nối trước đó rồi mới đến tiến tình truyền dữ liệu
- Cung cấp cơ chế đánh số thứ tự gói tin
- Có khả năng truyền và nhận dữ liệu cùng lúc
- Có cơ chế báo nhận
- Tính năng phục hồi dữ liệu bị mất trên đường truyền

# UDP
## Định nghĩa
- Là loại giao thức không trạng thái, không cần thiếp lập các kết nối trước khi gửi gói tin

## Tính năng
- UDP chỉ quan tâm tới việc truyền gói tin đi và không nhận lại — bán song công (half-duplex).

- UDP không quan tâm tới việc có gửi chính xác gói tin tới đúng địa chỉ hay không, không có cơ chế phục hồi dữ liệu bị mất.

- Giao thức UDP nhanh và hiệu quả hơn đối với các mục tiêu kích thước nhỏ và yêu cầu khắt khe về thời gian.