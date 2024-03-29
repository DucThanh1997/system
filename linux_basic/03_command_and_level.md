# Init
## Định nghĩa
Khi máy tính khởi động trải qua nhiều bước, kernel sẽ chạy chương trình đầu tiên với PID 1 (ProcessID). Gọi là init.

Chường trình này sẽ đảm nhận công việc bật, tắt, restart các chương tình cần bật lên cùng máy tính.

## Các loại phần mềm init
- SysV: có từ lâu, giờ ít được dùng
- Upstart: viết bởi ubuntu, đã bị thay thế bằng Systemd
- Systemd: chương trình init làm nhiều hơn những gì các init truyền thống thường làm. Được dùng trong các OS phổ biến Debian, Ubun16.04 trở đi, Fedora
- OSX có Launchd

Khi khởi động SysV và Upstart chia các nhóm chương trình thành các `runlevel` khác nhau

## 7 runlevel
Có tổng là 7 run level chạy trên linux từ 0 đến 6
- Halt
- Single-user text mode
- Not used (user-definable)
- Full multi-user text mode
- Not used (user-definable)
- Full multi-user graphical mode (with an X-based login screen)
- Reboot

Có 3 level tiêu chuẩn
- level 0: halt (tắt máy)
- level 1: single user textmode
- level 6: reboot

Tuy nhiên với ubuntu 16.04 trở đi họ dùng systemd. Systemd không có khái niệm "runlevel", nó chỉ tồn tại ở đó với mục đích đối chiếu, tương thích 1 phần với SysV


Để kiểm tra bạn đang ở level nào thì chạy lênh này `runlevel`

![image](https://user-images.githubusercontent.com/45547213/68826887-66740600-06d2-11ea-99c6-c1bb02524976.png)

# command

## Định nghĩa
- 1 command là 1 yêu cầu từ 1 người dùng bảo máy tính làm 1 cái gì đó
- Các command được ban hành bằng cách gõ chúng vào terminal (phần mềm liên kết với shell)


## Các bước xử lí của 1 câu lệnh 
- Lấy input từ đầu vào: Khi bạn nhập vào 1 lệnh, shell sẽ đọc dữ liệu nhập vào của bạn bằng cách sử dụng getline(). Getline() đọc dữ liệu STDIN - luồng dữ liệu đầu vào và lưu trữ đầu vào ở bộ nhớ đệm dưới dạng string. Ví dụ lệnh `ls -l` sẽ được lưu là `{"ls", "-l", "NULL"}`

- Kiểm tra regex và alias: Trước khi tìm kiếm lệnh, shell sex kiểm tra các kí tự đặc biệt mà cần được làm rõ. Ví dụ: `(.,$,/,...)`. Shell cũng sẽ kiểm tra các alias. Alias là các phím tắt. Ví dụ `alias apple="cat"` thì khi gõ apple, shell sẽ hiểu đó là lệnh cat.

- Kiểm tra lệnh builtin. Nếu câu lệnh không phải là 1 alias thì shell sẽ kiểm tra xem lệnh đó có phải là builtin ko. Lệnh builtin là lệnh được tích hợp và chạy trong chính shell. Ví dụ: `cd, echo, alias, help, read, type`

- Sau đó nó sẽ kiểm tra xem lệnh có là PATH hay không: Ví dụ 1 PATH là `python, mongo, go, mysql`

- Sao chép và chạy chương trình trong tiến trình con Sau khi tìm thấy lệnh trong PATH, shell sẽ chạy file đó bằng fork(). fork() là một system call để tạo một bản sao cho tiến trình hiện tại. Tất cả các tiến trình của người dùng trên linux đều là kết quả của fork().

    + Shell(parent process) sẽ gọi fork để tạo bản sao của chính nó (child process). Tiến trình con có pID riêng. Chạy một chương trình trong một tiến trình riêng biệt đảm bảo sẽ bảo vệ quy trình cha nếu chương trình gây ra lỗi khi thực hiện.
    + Tiến trình con sau đó được gọi là exec() để chạy câu lệnh của người dùng. exec() sẽ thay thế tiến trình con bằng chương trình mà người dùng yêu cầu.
    + Tiến trình cha sẽ đợi tiến trình con hoàn thành quá trình thực thi của nó qua hàm wait().


## Các loại command trong linux
Có hàng ngìn các câu lênh trong linux. Tất cả chúng đều được chia thành 4 loại. Mỗi loại có đặc điểm và mức độ ưu tiên riêng trong mỗi trường linux

Vậy làm thế nào để phân biệt các loại command bằng `type`

![image](https://user-images.githubusercontent.com/45547213/68910829-bd86e300-0785-11ea-82ab-72f84cb2816b.png)

Và có những loại command nào

- Built-in Shell Commands: những loại lệnh này được xử lí ngay trong shell. Điều này khiến chúng trở nên tất nhanh vì lệnh này không sử dụng 1 phần mềm nào để chạy. Những lệnh builtin này thường đơn giản và làm những công việc bình thường chẳng hạn liệt kê file. 1 vài câu lệnh điển hình `cd, bg, jobs, kill, local, logout, echo`

- Shell function: thường là các câu lệnh script được liên kết với linux. Shell function thường là các methods hoặc function trong các ngôn ngữ khác. Ví dụ ` while, else, do, case` thường được dùn trong shell script

- Alias: Kiểu lối tắt. Bạn tạo ra để gõ cho nhanh

- Excutable Programs: Là các lệnh có nguồn gốc từ các chương trình bên ngoài. Chẳng hạn `zip, wget, vlc, mplayer`. Miễn là bạn tải nó và nó ở trong $PATH thì bạn có thể dùng được

## Đường dẫn tương đối và đường dẫn tuyệt đối
- Đường dẫn tuyệt đối là đường dẫn của 1 tệp tin bắt đầu từ thư mục gốc(root) Ví dụ: `/usr/local`

- Đường dẫn tương đối là đường dẫn đến 1 tệp tin hoặc thư mục mà ko cần phải qua thư mục gốc. Ví dụ: `cd ../cat`

