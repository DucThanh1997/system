# IPv4

## Định nghĩa 
- Là phiên bản thứ 4 trong quá trình phát triển giao thức Internet

- Là 1 giao thức của TCP/IP- thuộc tầng Internet 

## Cấu trúc
- Là 32 bit nhị phân chia thành 4 cụm 8 bit(gọi là các octet). Các octet biểu diễn dưới dạng nhị phân, tách nhau bởi dấu chấm 

- Có 2 phần là phần mạng và phần host

![image](https://user-images.githubusercontent.com/45547213/68546775-d3ef1080-040c-11ea-8866-a3076477bb6c.png)

### Nguyên tắc đặt địa chỉ IP
- Các bit phần mạng được phép đồng thời bằng 0

```
0.0.0.1 với 0.0.0 là phần mạng và 1 là phần host. Địa chỉ này không hợp lệ
```
- các bit ở phần host đồng thời bằng 0 ta có 1 địa chỉ mạng

```
192.168.1.1 là một địa chỉ có thể gán cho host nhưng địa chỉ 192.168.1.0 là một địa chỉ mạng, không thể gán cho host được.
```

- các bit ở phần host đồng thời bằng 1, ta có 1 địa chỉ broadcast
```
Địa chỉ 192.168.1.255 là địa chỉ broadcast cho mạng 192.168.1.0
```

## Các lớp của địa chỉ IP
### Lớp A
![image](https://user-images.githubusercontent.com/45547213/68558685-d2553500-046c-11ea-8f7e-1976e10cbf68.png)
- Địa chỉ lớp A sử dụng 1 octet đầu làm phần mạng, ba octet sau làm phần host

- Bit đầu của 1 địa chỉ lớp A gôm: 1.0.0.0 đến 126.0.0.0

- Mạng 127.0.0.0 được sử dụng làm mạng loopback

- Phần host có 24 bit => mỗi mạng lớp A có (2^24 – 2) host.

### Lớp B

![image](https://user-images.githubusercontent.com/45547213/68559110-5fe55480-046e-11ea-897b-d18b64ca97e5.png)
- Địa chỉ lớp B sử dụng 2 octet đầu làm phần mạng và 2 octet sau làm phần host

- Các địa chỉ mạng lớp B gồm: 128.0.0.0 -> 191.255.0.0.

- Có tất cả 2^14 mạng trong lớp B

- Phần host dài 16 bit do đó một mạng lớp B có (2^16 – 2) host.

### Lớp C
![image](https://user-images.githubusercontent.com/45547213/68561291-8e1b6200-0477-11ea-9720-50aa102dc65a.png)

- Ba octet đầu làm phần mạng, 1 octet sau làm phần host

- Ba bit đầu của một địa chỉ lớp C luôn được giữ là 1 1 0.

- Các địa chỉ mạng lớp C gồm: 192.0.0.0 -> 223.255.255.0. Có tất cả 2^21 mạng trong lớp C.

- Phần host dài 8 bit do đó một mạng lớp C có (2^8 – 2) host.

### Lớp D:
- Gồm các địa chỉ thuộc dải: 224.0.0.0 -> 239.255.255.255
- Được sử dụng làm địa chỉ multicast

### Lớp E:
- Từ 240.0.0.0 trở đi.
- Được dùng cho mục đích dự phòng.


### Địa chỉ private: 
- Dùng trong mạng lan

- Dải địa chỉ private (được quy định trong RFC 1918):

Lớp A: 10.x.x.x

Lớp B: 172.16.x.x -> 172.31.x.x

Lớp C: 192.168.x.x

- Kỹ thuật NAT (Network Address Translation) được sử dụng để chuyển đổi giữa IP private và IP public.


# IPv6

## Định nghĩa
- Địa chỉ IPv6 dài 128bit, được chia làm 8 nhóm, mối nhóm gồm 16bit, được ngăn cách với nhau bằng dấu hai chấm. Mỗi nhóm được biểu diễn bằng 4 số hexa

Ví dụ: 
```
FEDC:BA98:768A:0C98:FEBA:CB87:7678:1111
1080:0000:0000:0070:0000:0989:CB45:345F
```

## Đặc điểm của địa chỉ IP
- Cho phép bỏ các số 0 nằm trước mỗi nhóm (octet)
- Thay bằng số 0 cho nhóm có toàn toàn số 0`
- Thay bằng dấu "::" cho các nhóm liên tiếp nhau toàn số 0

## Phân loại địa chỉ IPv6
- Unicast: được định nghĩa duy nhất trên 1 cổng của 1 node IPv6. Một gói tin được gửi đến 1 địa chỉ unicast được đưa đến cổng được dịnh nghĩa bởi địa chỉ đó

- Multicast: được định nghĩa trên 1 nhóm các cổng IPv6. 1 gói tin gửi đến địa chỉ multicast được xử lí bởi tất cả những thành viên của nhóm multicast

- Anycast:  được đăng kí cho nhiều cổng (trên nhiều node). Một gói tin được gởi đến một địa chỉ anycast là được chuyển đến chỉ một trong số các cổng này, thường là gần nhất


## So sánh
