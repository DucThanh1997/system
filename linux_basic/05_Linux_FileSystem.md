# FileSystem
## Định nghĩa
Nói đơn giản FileSystem là thứ xác định các cách thức tổ chức, quản lí dữ liệu hay có thể nói là quản lý cách thức quản lý dữ liệu được đọc và lưu trên thiết bị. 

Những loại FileSystem được Linux hỗ trợ:

- FileSystem cơ bản: ext2, ext3, ext4, XFS, Btrfs, JFS, NTFS v.v.
- FileSystem dành cho dạng lưu trữ: ubifs, JFFS2, YAFFS 
- FileSystem dành cho cơ sở dữ liệu

Hệ điều hành linux coi tất cả đều là các tệp tin thậm chí cả các thiết bị cũng nư ổ đĩa. Nó quản lý tất cả trên 1 hệ thoonngs tệp tin duy nhất, bắt đầu ở gốc là 1 thư mục root và đây là thư mục ở mức cao nhất. Cấu trúc cơ bản của hệ thống tệp tin này được mô tả như sau

![image](https://user-images.githubusercontent.com/45547213/69019771-9da12a80-09e4-11ea-9c4a-e49ccc07b6df.png)


## Thư mục root
- Mỗi file hay thư mục trong linux đều bắt đầu bằng thư mục `/`
- Chỉ có tài khoản root mới cò quyền ghi trong thư mục này
- Thư mục gốc được đại diện bởi dấu `/` chứ không phải là `/root`.
- Thư mục root là thư mục cá nhân của tài khoản root

## Thư mục binary
- Binary là các file chứa toàn bộ mã nguồn hoặc mã máy. Các file binary có thể được thực thi trên máy tính

- `./bin`: là thư mục chứa các binary được thực thi bởi tất cả người dùng
- `./sbin`: là thư mục chứa các file thực thi binary để cấu hình hệ điều hành. Nhiều file thực thi yêu cầu quyển root để thực thi: `Iptables`, `reboot`, `fdisk`,`ifconfig`
- `./lib`: các file binary ở bin và sbin thường sử dụng thư viên được chia sẽ ở trong lib. Tên file thư viện có thể là lib*.so.*

![image](https://user-images.githubusercontent.com/45547213/69019771-9da12a80-09e4-11ea-9c4a-e49ccc07b6df.png)

- `./opt`: là thư mục để chứa các phần mềm tùy chọn, phần mềm bên thứ 3. Nó là các phần mềm không được cài từ những repo của các bản phân phối
- `./opt`: các gói phần mềm lớn có thể cài đặt các file ở `./bin`, `./lib` và `./etc` và cả `./otp`

## Các thư mục chứa cấu hình
### ./boot
- Thư mục ./boot chứa tất cả các file cần cho quá trình boot máy tính
- Những file này thường ít thay đổi
- Trong thư mục này có thể tìm thấy thư mục `/boot/grub`, nơi chứa file `/boot/grub/gurb.cfg`. File grub.cfg là file xác định boot menu mà hiển thị trước khi kernel khởi động

### ./etc
- Tất cả các file cấu hình dành cho máy được lưu ở `/etc`
- Etc là viết tắt của Editable Text Configuration.
- Rất nhiều file cấu hình của các ứng dụn, daemon, hoặc giao thức đều sử dụng .conf làm phần mở rộng

- `etc/init.d`: Rất nhiều bản phân phối Linux/Unix có 1 thư mục `etc/init.d` để chứa các scripts để chạy và dừng các daemon
- `etc/skel`: là copy của thư mục home của 1 user mới tạo. Nó thường chứa các file ẩn như .bashrc
- `etc/sysconfig`: chứa rất nhiều file cấu hình của RHEL

## Các thư mục chứa dữ liệu
### ./home
- Người dùng có thể lữu trữ dữ liệu cá nhân trong thư mục/home
- Thư mục của người dùng thường được đặt là `/home/$USERNAME nhưng điều này không bắt buộc
- Bên cạnh việc cho người dùng thư mục riêng để lưu trữ file thì thư mục home của người dùng cũng được sử dụng làm nơi lưu trữ hồ sơ người dùng. Hồ sơ của người dùng bao gồm rất nhiều file ẩn được bắt đầu bởi dấu chấm. Các file ẩn này chứa các cấu hình dành riêng cho user đó

### ./root
- trên hệ thống thư mục `/root` là vị trí mặc định để lưu trữ dữ liệu và hồ sơ của user root.

### ./media
- Là thư mục để chứa các mount point cho các thiết bị lưu trữ di động như usb, đĩa cd, thẻ nhớ sd,

### ./mnt
- Thư mục này nên chống và chỉ chứa các mount point tạm thời

### ./tmp
- Ứng dụng và người dùng thường sử dụng thư mục `/tmp` để lưu tữ dữ liệu tạm thời khi cần. Dữ liệu trong `/tmp` có thể sử dụng ổ cứng hoặc RAM

## Những thư mục trong bộ nhớ RAM
### ./dev
- File thiết bị trong `/dev` là các file thông thường, nhưng thực tế nó không nằm trên ổ đĩa cứng.
Những file này được thêm vào `/dev` khi mà kernel nhận ra các phần cứng

- Những phần cứng như là ổ đĩa cứng được đại diện bởi file thiết bị trong `/dev`

- Ngoài đại diện cho các thiết bị phân cứng thì có 1 số file thiết bị là trường hợp đặc biệt

- `/dev/tty` và `/dev/pts`: là 1 đại diện cho 1 terminal hay console kết nối đến hệ thóng

- `dev/null`: là 1 thư mục đặc biệt được coi như là hố đen trong linux. Mọi thứ được ghi vào đây đều biến mất và không thể lấy lại

### /proc
- Là 1 thư mục đặc biệt nhwung nó không lưu trữ ở ổ cứng. Nó như là cái nhìn cho kernel, hay những gì mà kernel quản lý và tương tác trực tiếp với nó

- `/proc` là 1 proc filesystem

- Những file trong `proc` được cập nhật liên tục

- Hầu hết các file có 0 bytes, nhưng nó lại chứa dữ liệu, có thể là rất nhiều dữ liệu. Ví dụ: `/proc/cpuinfo`


### /sys
- Thư mục `/sys` được sử dụng cho phiển bản kernel 2.6. Từ 2.6, Linux sử dụng sysfs để hỗ trợ usb
- `/sys` lưu trữ thông tin kernel về phần cứng

## /usr - Unix System Resource
- `/usr` phát âm giống user nhưng nó là viết tắt của unix System Resource

- `/usr` thường chứa dữ liệu có thể chia sẻ và chỉ đọc

- `/usr/bin`: thư mục này chứa rất nhiều file thực thi được coi là các lệnh

- `/usr/include`: chứa các thư viện cho c

- `usr/lib`: Là thư mục chứa thư viện mà không được sử dụng trực tiếp từ người dùng hay scripts

- `usr/local`: Dùng để người quản trị cài đặt các phần mềm local

- `usr/share`: là thư mục chứa dữ liệu độc lập

## var
- Những file có kích thước không thể tính toán được như log, cache và spool thườn được lưu ở `/var`

- `var/log`: chứa file log

- `var/cache`: chứa file cache

- `var/lib`: chứa thông tin trạng thái của ứng dụng


