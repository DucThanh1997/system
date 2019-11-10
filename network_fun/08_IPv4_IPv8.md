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