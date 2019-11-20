## Các toán tử điều khiển thực hiện command
1. Dấu chấm phẩy `;`
- Bạn có thể gõ hai hay nhiều lệnh trên 1 dòng, ngăn cách nhau bằng dấu chấm phẩy. Các lệnh sẽ được thực thi 1 cách tuần tự. Shell đợi lệnh trước thực thi xong mới thực thi lệnh sau

![image](https://user-images.githubusercontent.com/45547213/69128887-cc4ffb80-0adf-11ea-8800-2bad799c5291.png)

2. Kí hiệu và `&`
- Khi 1 câu lệnh kết thúc bằng kí hiệu `&`, shell sẽ chạy câu lệnh đó dưới dạng background. Bạn sẽ nhận được câu lệnh khi nó thực thi xong trong background

![image](https://user-images.githubusercontent.com/45547213/69133270-3a002580-0ae8-11ea-9674-820a22a2e80c.png)

3. Kí hiệu dollar hỏi chấm `$?`
- Exit code của câu lệnh được lưu ở trong biến `$?`. Thực ra `$?` không phải là biến mà nó là 1 tham số, bạn không thể gán giá trị cho `$?` Exit code bằng 0 nghĩa là lệnh đã thực thi thành công và khác 0 nghĩa là đã xảy ra lỗi

![image](https://user-images.githubusercontent.com/45547213/69133824-14275080-0ae9-11ea-892c-4570c05cdbae.png)

4. Hai dấu và
- Shell sẽ hiểu `&&` như là 1 toán từ AND