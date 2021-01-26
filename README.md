# Module2-reflection
# reflection 26-1-2021
***
<br>
1.Mảng trong php có 3 loại:
<br>
- Mảng 1 chiều và mảng đa chiều theo chỉ số index giống với javascript
<br>
- Mảng liên kết (associative array) là mảng sử dụng các key là tên thay cho chỉ số thông thường
<br>
&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp VD: $age = array("Peter"=>"35", "Ben"=>"37","Joe"=>"43");
<br>
&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp Dùng: foreach($age as $key => $value){
<br>	&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp		echo $key. ":". $value;
<br> &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp			}
<br> &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp để duyệt tất cả phần tử ( các cặp key và value tương ứng) của mảng.
<br>
2. Nhúng trang php.
<br> 
- nhúng nội dung của một trang php vào một trang php.
<br>
- có một số cơ chế khác nhau:
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + include "filename.php";
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + include_once "filename.php";
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + require "filename.php";
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + require_once "filename.php";
<br> -sự khách nhau giữa các cơ chế khi xảy ra lỗi:
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + include, include_once thì tung ra cảnh báo (E-WARNING) và tiếp tục thực thi.
<br> &nbsp&nbsp&nbsp&nbsp&nbsp + require, require_once thì tung ra lỗi nghiêm trọng (E_COMPIE_ERROR) và dừng thực thi.
<br> - sự khác nhau giữa include, require và include_once, require_once :
<br> &nbsp&nbsp&nbsp&nbsp&nbsp  + include, require thì có thể nhúng trang php nhiều lần ở nhiều nơi.
<br> &nbsp&nbsp&nbsp&nbsp&nbsp  + include_once, require_once chỉ có thể nhúng trang php một lần duy nhất.Nếu lần sau sử 
dụng lại thì php tự bỏ qua 
<br> 
<br>
3. các kiểu lỗi hay xảy ra:
<br> - lỗi cú pháp (Syntax Error) xảy ra tại thời gian biên dịch trong các ngôn ngữ truyền thống và trong thời gian thông dịch trong js, php
<br> &nbsp&nbsp&nbsp&nbsp&nbsp VD: thiếu dấu ngoặc tròn trong biểu thức điều kiện.
<br> - Fatal Error là loại lỗi khi biên dịch code PHP và hiểu những gì mình viết, tuy nhiên nó nhận ra trong đó có một hàm không được khai báo. Điều này có nghĩa là hàm được gọi nhưng hàm đó lại không được định nghĩa. Và dừng thực thi chương trình.
<br> - Warning Errors là lỗi cảnh báo và không dừng việc thực thi chương trình. Lý do chính cho các lỗi cảnh báo là bao gồm một file nào đó bị thiếu hoặc sử dụng tham số không chính xác trong một chức năng.
<br> -Notice Error là một lỗi giống như Warning Errors, tức là những lỗi nhỏ, không nghiêm trọng mà PHP gặp phải khi thực thi tập lệnh 
<br> &nbsp&nbsp&nbsp&nbsp&nbsp 	 VD: truy cập vào một biến chưa được xác định.


