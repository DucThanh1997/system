# Internet là gì
- Internet là 1 hệ thống thông tin toàn cầu có thể được truy nhâp công cộng gồm các mạng máy tính được liên kết với nhau.

- Hệ thống này truyền thông tin theo kiểu nối chuyển  gói dữ liệu dựa trên 1 giao thức liên mạng đã được chuẩn hóa

# Mô hình OSI

## Định nghĩa
- Mô hình OSI là mô hình căn bản về các tiền tình truyền thông

- Mô hình OSI tôt chức các giao thức truyền thống thành 7 tầng mỗi tầng giải quyết 1 vấn đề khác nhau.


## Các nguyên tắc 
- Mô hình phải có 7 tầng và phải có khả năng kết nối với các hệ thống khác nhau tương thích với các chuẩn OSI

- Qúa trình xử lý các ứng dụng được thực hiện trong các hệ thống mở, trong khi vẫn duy trù được các hoạt động kết nối giữa các hệ thống

## Các giao thức trong mô hình OSI

- Giao thức hướng liên kết: Trước khi truyền dữ liệu, các thực thể đồng tầng trong hai hệ thống cần phải thiết lập 1 liên kết logic. Chúng thương lượng với nhau về các tham số sẽ sử dụng trong giai đoạn truyền, hợp cắt dữ liệu. Sau khi xong thì các liên kêts sẽ được hủy bỏ. Thiết lập liên kết logic sẽ nâng cao độ tin cật và an toàn trong quá trình trao dồi dữ liệu

- Giao thức không liên kết: Dữ liệu được truyền độc lập trên các tuyến khác nhau. Với các giao thức không liên kết chỉ có giai đoạn duy nhất truyền dữ liệu

## Vai trò và chwucs năng chủ yêu các tầng

### Application Layer
- Nhiệm vụ của tần này là xác định giao diện giữa người dùng và môi trường OSI

- Tầng này gồm nhiều giao thức ứng dụng cung cấp các phương diện cho người sử dụng truy cập vào môi trường mạng và các dịch vụ phân tán

### Presentation Layer
- Tầng này giải quyết các vấn đề liên quan đến các cú pháp và ngữ nghĩa của thông tin được truyền. Biểu diễn thông tin người sử dụng phù hợp với thông tin làm việc của mạng và ngược lại

- Tầng trình bày phải chịu trách nhiệm chuyển đội dữ liệu gửi đi trên mạng từ 1 loại biểu diễn này sang 1 loại biểu diễn khác. Sẽ có form chung để truyển đổi sao cho chuẩn

### Session Layer
- Tầng này cho phép người sử dụng trên các máy tính thiết lập, duy trì và đồng bộ phiên truyền thông giữa họ với nhau. Nói cách khác tầng phiên thiết lập các giao dịch giữa các thực thể đầu cuối

- Nó cung cấp 1 liên kết giữa 2 đầu cuối sử dụng dịch vụ phiên sao cho việc trao đổi dữ liệu được thực hiện 1 cách đồng bộ và khi kết thức thì giải phóng liên kết

### Transport Layer
- Là tầng cao nhất liên quan đến các giao thức trao đổi dữ liệu giữa các hệ thống mở, kiểm soát việc truyền dữ liệu từ nút tới nút

- Chia nhỏ các gói tin ra, đánh số chúng và đảm bảo chúng chuyền theo đúng thứ tự.


### Network Layer
- Tầng mạng thực hiện các chức năng chọn đường đi cho các gói tin nguồn tới đích có thể trong cùng một mạng hoặc khác mạng nhau. Đường đi không cố định mà tùy từng trạng thái mạng

- Tầng này còn có khả năng điều khiển tắc nghẽn. Nếu có quá nhiều gói tin cùng lưu chuyển trên cùng 1 đường thì có thể xảy ra tình trạng tắc nghẽn. Nếu có quá nhiều gói tin cùng lưu chuyển trên cùng 1 đường có thể xảy ra tình trạn tắc nghẽn. Thực hiện chức năng giao tiếp giứa các mạng khi các gói tin đi từ mạng này sang mạng khác để tới đích


### Data Link Layer
- Thiết lập các liên kết giáp nối các gói tin lại theo thứ tự, kiểm soát luồng và lỗi


### Physical Layer
- Giao tiếp qua 1 đường truyền vật lý.

- Xác định các chức năng, thủ tục về điện, cơ, quang để kích hoạt, duy trì và giải phóng các kết nối vật lý giữa các hệ thống mạng
