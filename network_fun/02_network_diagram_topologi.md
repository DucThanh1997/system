# Network diagram 
1. Định nghĩa
Network diagram là một biểu đồ trực quan của máy tính hoặc mạng viễn thông. Nó hiển thị các thành phần tạo nên một mạng và cách chúng tương tác, bao gồm bộ định tuyến, thiết bị, trung tâm, tường lửa, v.v. Sơ đồ mạng này hiển thị một mạng cục bộ (LAN):

![image](https://user-images.githubusercontent.com/45547213/68084767-bbab4e80-fe6c-11e9-9449-d00fb09e3f87.png)

2. Ứng dụng
- Quy hoạch cấu trúc của một mạng gia đình hoặc chuyên nghiệp
- Điều phối cập nhật vào mạng hiện có
- Báo cáo và xử lý sự cố mạng
- Để tuân thủ PCI hoặc các yêu cầu khác
- Là tài liệu cho giao tiếp nội bộ hoặc nơi khác vv
- Để theo dõi các thành phần
- Gửi thông tin liên quan đến nhà cung cấp cho RFP (yêu cầu đề xuất) mà không tiết lộ thông tin bí mật
- Bán một đề xuất mạng cho các bên liên quan tài chính
- Đề xuất thay đổi cơ sở hạ tầng cấp cao, kiểm tra nhật ký hệ thống

3. Các loại
- Có 2 loại: logic và vật lý


# Sơ đồ logic
Mô tả cách thức truyền tin qua môi trường truyền dẫn. Có 2 loại
- Broadcast: có ý nghĩa đơn giản là mỗi host gửi dữ liệu của nó đến tất cả các host khác trên môi trường truyền. Không có sự đăng ký trạm kế tiếp sử dụng môi trường truyền, thay vì vậy đến trước phục vụ trước.

- Token passing: điều khiển truy xuất mạng bằng một token điện tuần tự đến mỗi host. Khi một host nhận token có nghĩa là host đó có thể truyền dữ liệu lên mạng.

![image](https://user-images.githubusercontent.com/45547213/68085259-a84eb200-fe71-11e9-8bbc-f8c189f46f41.png)


# Sơ đô vật lý
Sơ đồ vật lý định nghĩa cách thức các máy tính liên kết với nhau bằng các thiết bị vật lý môi trường truyền dẫn hiện thực. Có nhiều loại cấu hình vật lý được sử dụng như

- Bus: dữ liệu truyền đi qua từng máy nếu chùng địa chỉ thì chạy vào cái đầu cuối hứng và xóa thông tin tự do

![image](https://user-images.githubusercontent.com/45547213/68085285-f6fc4c00-fe71-11e9-8f84-f78305e96b18.png)

- Ring: mỗi máy là 1 trạm chuyển thông tin, thông tin sẽ đi qua từng máy 1 và được khuếch đại lên

![image](https://user-images.githubusercontent.com/45547213/68085394-23649800-fe73-11e9-8de8-bc4cbccbb36b.png)

- Star: Gửi hết qua thiết bị trung tâm là hub, hub sẽ phân giải xem cái nào đi tiếp đến cái nào

![image](https://user-images.githubusercontent.com/45547213/68085409-5d359e80-fe73-11e9-9ad0-cb6271500037.png)

- Mesh: có nhiều đường để từ máy này đến máy khác nhưng như này hay bị thừa

![image](https://user-images.githubusercontent.com/45547213/68085413-6cb4e780-fe73-11e9-99e6-7318c670ac5b.png)

- Hồn hợp: Sự kết hợp của bus ring và star, là chuẩn của nhiều mạng lan

![image](https://user-images.githubusercontent.com/45547213/68085419-87875c00-fe73-11e9-9d33-5762520a8de4.png)

