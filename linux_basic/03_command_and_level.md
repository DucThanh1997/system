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
- Các command được ban hành bằng cách gõ chun