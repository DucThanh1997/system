## Các câu lệnh làm việc với file và folder
1. pwd: chỉ ra thư mục bạn đang ở trong

![image](https://user-images.githubusercontent.com/45547213/68914124-2ecb9380-0790-11ea-9697-827f23f096de.png)

2. ls: liệt kê ra nội dung của file

![image](https://user-images.githubusercontent.com/45547213/68914240-97b30b80-0790-11ea-958d-586531ce7b8b.png)

3. ls -la: lấy ra cả file ẩn và quyền của từng người. Nói chung là chi tiết hơn

![image](https://user-images.githubusercontent.com/45547213/68915316-13fb1e00-0794-11ea-8d4e-1aafe9aa9a9c.png)

4. mkdir: tạo file

`mkdir example`: tạo folder có tên là example

5. mkdir -p: tạo folder trong folder
`mkdir -p example/hello`: vừa tạo folder example vừa tạo folder hello trong example

6. rmdir: xóa 1 folder nhưng nó file là folder trống
`rmdir hello`: xóa file trống có tên hello

7. cd: đột nhập vào thư mục
`cd example`: vào folder example
`cd ..`: thoát ra ngoài

8. touch filename: tạo file
`touch hello.txt`: tạo file hello.txt

9. rm filename: xóa file
`rm hello.txt`: xóa file hello.txt
`rm -f hello.txt`: xóa file nhưng lệnh này mạnh hơn
`rn -r directory`: xóa folder có trong directory

10. copy file1 file2: copy nội dung của file1 sáng file2
`cp hello.txt hi.txt`

11. cp -r dir1 dir2: copy nội dung từ thư mục 1 sáng thư mục 2 nếu thứ mục 2 đã tồn tại thì nó sẽ bị ghi đè

12. mv file1 file2: rename tên file

`mv hello.txt hi.txt`

13. Chúng ta cũng có thể dùng `mv` để di chuyển file hoặc thư mục

`mv /example/hello.txt /awesome/`: chúng ta di chuyển file `hello.txt` sang thư mục example

14. cat filename: in ra nội dung của file

`cat hello.txt`: in ra nội dung của file hello.txt

15. head filename: cái này sẽ in ra mười dòng đầu tiên

16. tail filename: lấy 10 dòng cuối

17. tail -f filename: lấy dữ liệu real time


## Cách sử dụng vim

Vim có 2 chế độ làm việc là command và insert


### Cách dùng
- Mở file dùng: `vim helloworld.txt`

Nếu file này tồn tại bạn sẽ thấy nội dung của nó còn nếu trống bạn sẽ tạo ra 1 file mới

- Thoát ra: `ESC :q Enter`

Phím q ở đây chả tương tự với quit nhưng nó sẽ thoát mà không lưu. 

- Lưu và thoát ra: `ESC :wq Enter`

- Chuyển sang chế độ insert: `i`

- Chuyển sang chế độ command: `ESC`





