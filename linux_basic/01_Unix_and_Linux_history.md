# Unix và nguồn gốc của Linux

## Unix

### Gốc gác
- Bắt đầu được phát triển vào năm 1969
- Phiên bản đầu tiên được ra đời vào 3 tháng sau đó
- Thực hiện bởi Ken Thompson và Dennis Ritchie, 2 nhà khoa học máy tính nổi tiếng tại phòng thí nghiệm Bell Labs của AT&T

### Phát triền 

Những năm sau của thập niên 70, AT&T chia sẻ Unix cho những tổ chức giáo dục, hay tổ chức thương mại bên ngoài, từ đó dẫn đến sự ra đời của nhiều phiên bản Unix khác nhau. Nổi bật nhất trong số đó là phiên bản giáo dục được xây dựng bởi Computer Systems Research Group thuộc đại học California, Berkeley. Phiên bản này được biết đến rộng rãi với cái tên Berkeley Software Distribution, hay BSD.

Mặc dù phiên bản chính thức của Unix, BSD đã dừng phát triển từ lâu, thế nhưng những di sản mà chúng để lại là rất lớn cho đến ngày hôm nay. Rất nhiều hệ điều hành, từ close source cho đến open source đựa dựa trên 2 nhánh này. Ví dụ: MacOS


## GNU

### Gốc gác
Tháng 9 năm 1983, Richard Stallman thông báo về sự ra đời của dự án GNU (GNU là viết tắt của từ GNU’s not Unix

Mục tiêu của dự án GNU là tạo ra được một hệ điều hành miễn phí, giống Unix, nơi mà mọi người có quyền tự do copy, phát triển, chỉnh sửa và phân phối phần mềm, và việc tái phân phối là không bị giới hạn.

### Phát triển 
Project GNU đã tạo ra được rất nhiều sản phẩm quan trọng như GNU Compiler Collection (gcc), GNU Debugger, GNU Emacs text editor (Emacs), GNU build automator (make) … Ngoài ra còn phải kể đến giấy phép nổi tiếng được sử dụng rộng rãi nhất hiện nay: GNU General Public License (GPL)

GNU Project đã đạt được nhiều thành tựu lớn, tạo ra được nhiều công cụ tương tự như những gì có trên Unix. Tuy nhiên, GNU vẫn thiếu một thành phần quan trọng, mảnh ghép cuối cùng để nó trở thành một hệ điều hành hoàn chỉnh. Đó chính là Kernel, phần thực hiện công việc điều khiển, giao tiếp với các thiết bị phần cứng (CPU, RAM, Devices …).

## Linux

### Gốc gác 
Ngày 25 tháng 8 năm 1991, một cậu sinh viên ở Phần Lan mang tên Linus Torvalds giới thiệu một sản phẩm cá nhân, sau này trở thành Linux Kernel.

Project của Linus nhanh chóng nhận được sự chú ý cùng với đó là những đóng góp của nhiều cá nhân, tổ chức.

Sự kết hợp giữa nhân Linux, với các phần mềm của GNU đã tạo ra một hệ điều hành hoàn chỉnh, hệ điều hành hoàn toàn miễn phí đầu tiên. Nó được mang tên GNU/Linux. Hay còn gọi là hệ điều hành linux


### Phân loại
Linux chỉ là phần Kernel, còn GNU cung cấp các công cụ cần thiết chạy trên Kernel đó. Tuy nhiên, việc config Kernel như thế nào, cài đặt, sử dụng các phần mềm nào thì ta có thể tự do quyết định.

Một số các tổ chức, công ty giúp chúng ta làm sẵn những việc đó với việc phối kết hợp Linux Kernel với các utilities, hay package manager để tạo ra một bản phân phối một hệ điều hành hoàn chỉnh. Chúng được gọi là Linux Distribution, hay Distro.

Ngày nay, có vô vàn các bản phân phối Linux, nhiều cái rất quen thuộc, phổ biến, và cũng có nhiều distro có thể bạn còn chưa được nghe tên bao giờ. Một số Distro được sử dụng nhiều nhất có thể kể ra như Ubuntu, Debian, CentOS, Fedora, Redhat, Linux Mint ….


## Sự khác biệt giữa linux và window
- Cấu trúc file: Không chia ổ C ổ D như windown mà chia ra theo cây thư như này
![image](https://user-images.githubusercontent.com/45547213/67263182-8f3d1d00-f4d1-11e9-871f-8a1e2c4b0e60.png)

- Không có registry nên không cần dọn dẹp 

- Gần như không có virus và tính bảo mật cao

- Linux cho phép bạn access source code còn Windown thì không