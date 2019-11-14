## Các bản phân phối của linux

### CentOS/Red Hat Enterprise Linux
Red Hat Enterprise Linux là một bản phân phối Linux thương mại dành cho máy chủ và máy trạm. Nó được phát triển dựa trên dự án nguồn mở Fedora, nhưng được thiết kế để trở thành một nền tảng ổn định với sự hỗ trợ lâu dài hơn.

CentOS là một dự án cộng đồng lấy mã Red Hat Enterprise Linux, xóa tất cả các nhãn hiệu của Red Hat và được cung cấp cũng như phân phối miễn phí. Nói cách khác, đây là một phiên bản miễn phí của RHEL, vì vậy sẽ rất phù hợp nếu bạn muốn một nền tảng ổn định sẽ được hỗ trợ trong một thời gian dài. 

### Ubuntu
Ubuntu là một hệ điều hành mã nguồn mở xây dựng xung quanh nhân Linux, được cộng đồng cùng phát triển. Bản phát hành đầu tiên của Ubuntu là vào 20 tháng 10 năm 2004, bắt đầu bằng việc tạo ra một nhánh tạm thời của dự án Debian Linux. Bằng việc để cho Ubuntu tự do và mở mã nguồn, Canonical có thể tận dụng tài năng của những nhà phát triển ở bên ngoài trong các thành phần cấu tạo của Ubuntu mà không cần phải tự mình phát triển.

### Debian

Debian là một tập hợp các tiện ích và các chương trình cơ bản giúp máy tính hoạt động. Phần cốt lõi của một hệ điều hành chính là hạt nhân. Nhân là thành phần cốt yếu nhất bên trong máy tính và nó thực hiện tất cả các nhiệm vụ cơ bản và còn giúp khởi động các chương trình khác.

Hiện tại các hệ thống Debian sử dụng nhân Linux hoặc nhân FreeBSD. Linux là một phiên bản phần mềm được viết đầu tiên bởi Linus Torvalds và tiếp sau đó được hỗ trợ bởi hàng ngàn lập trình viên trên toàn thế giới. FreeBSD là một hệ điều hành bao gồm một nhân và phần mềm khác.


## Cấu trúc hệ điều hành Linux
Bao gồm 3 phần Kernel, Shell, và áp lai cây sần

![image](https://user-images.githubusercontent.com/45547213/67267259-2018f600-f4dc-11e9-847e-d2a89c2011fe.png)

### Kernel
- Nằm giữa phần cứng và phần mềm 
- Quản lí các tài nguyên của máy tính và cho phép các phần mềm sử dụng chúng

Có 3 loại Kernel
- MicroKernel: quản lí bộ vi xử lý, bộ nhớ và IPC. Loại này có tính linh hoạt cao, thích ứng với nhiều loại phần cứng nên không lo khi thay đổi phần cứng. Chúng còn có tính bảo mật khá cao vì chỉ định rõ ràng những tiến trình nào hoạt động trong chế độ user mode , mà không được cấp quyền như trong chế độ giám sát - supervisor mode.

- Monolithic Kernel: Bao quát hơn Micro, ngoài quản lí bộ vi xử lý, bộ nhớ và IPC, chúng còn can thiệp vào trình điều khiển driver, tính năng điều phối file hệ thống , các giao tiếp qua lại giữa server... Monolithic tốt hơn khi truy cập tới phần cứng và đa tác vụ , bởi vì nếu 1 chương trình muốn thu thập thông tin từ bộ nhớ và các tiến trình khác , chúng cần có quyền truy cập trực tiếp và không phải chờ đợi các tác vụ khác kết thúc . Nhưng đồng thời , chúng cũng là nguyên nhân gây ra sự bất ổn vì nhiều chương trình chạy trong chế độ supervisor mode hơn , chỉ cần 1 sự cố nhỏ cũng khiến cho cả hệ thống mất ổn định . Linux sử dụng kernel này .

- Hybrid Kernel : Khác với 2 loại kernel trên , Hybrid có khả năng chọn lựa và quyết định những ứng dụng nào được phép chạy trong chế độ user hoặc supervisor . Thông thường, những thứ như driver và file hệ thống I/O sẽ hoạt động trong chế độ user mode trong khi IPC và các gói tín hiệu từ server được giữ lại trong chế độ supervisor . Tính năng này thực sự rất có ích vì chúng đảm bảo tính hiệu quả của hệ thống , phân phối và điều chỉnh công việc phù hợp, dễ quản lý . Windows và Mac OS X sử dụng kernel này .

Câu lệnh kiểm tra Kernel hiện tại: `uname -r`

### Shell
- Nằm trên Kernel
- Là cái để giao tiếp giữa áp lai cây sần với kernel
- Nhận command từ người dùng hoặc áp lai cây sần rồi chuyển cho kernel xử lí

Có 3 loại shell 
- sh (the Bourne Shell): đây là shell nguyên thủy của UNIX được viết bởi Stephen Bourne vào năm 1974. Đến nay shell sh vẫn sử dụng rộng rãi.
- bash(Bourne-again shell): Bash được cải tiến từ sh , nó hỗ trợ nhiều câu lệnh hơn.
- csh (C shell): shell được viết bằng ngôn ngữ lập trình C

Lưu ý: với tài khoản thường dấu nhắc shell là `$` còn với root là `#`

### Applications
Lớp applications, utilities là các ứng dụng, tiện ích, công cụ trên hệ điều hành ví dụ như trình duyệt, game,... các ứng dụng chạy trên shell, dùng shell để giao tiếp với kernel, phần cứng.