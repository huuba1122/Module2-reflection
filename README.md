# Module2-reflection
# reflection lesson 4 ngày 28-1-2021
***
<dl>
1. namespace.
<dt>
- Namespace (tên miền không gian) là một hình thức để đóng gói các hạng mục có liên quan lại với nhau. 
</dt>
<dt>
- Namespace trong PHP giúp chúng ta nhóm các lớp, các interface, các hàm, các hằng có liên quan đến nhau vào trong cùng một nơi.
</dt>
<dt>
- Trong PHP, namespace được thiết kế để giải quyết 2 vấn đề mà các tách giả của các thư viện và ứng dụng thường gặp phải khi cố gắng tạo ra các đối tượng hoặc hàm có thể tái sử dụng được.
</dt>
<dd>
+ Các tên gọi bị trùng nhau giữa những lớp/hàm được tạo ra, so với các lớp/hàm có sẵn của PHP, hoặc các lớp/hàm do một người khác viết.
</dd>
<dd>
+ Khả năng để rút ngắn tên gọi thông qua việc đặt các bí danh (alias) nhằm giữ cho mã nguồn ngắn gọn.
</dd>
2. Khai báo namespace:
<dt>
- Để khai báo namespace trong PHP chú ta sử dụng cú pháp sau:
</dt>
<dd>
namespace Name;
</dd>
<dt>
- Khi mà một class đã được một namespace định danh thì bạn sẽ không thể gọi theo cách thông thường được nữa mà phải gọi với cú pháp:
</dt>
<dd>
new tenNamespace\tenClass();
</dd>
-VD:
<dt>
b1. Tạo một file human.php có nội dung như sau:
</dt>
<dd>
< ?php
<br>
namespace Human;
<br>
class Person
<br>{
<br>private $name = 'name person';

    public function getName()
        {
            return $this->name;
        }
}
</dd>
<dt>
b2. Tiếp đó tạo một file index.php cùng cấp với file human.php và lúc này chúng ta sẽ phải gọi class Person như sau:
</dt>
<dd>
-cach1: 
<br>    < ?php

		include 'human.php';

		$person = new Human\Person();

		echo $person->getName();
		//kết quả: name person
</dd>
<dd>
-cách 2: sử dụng use.
<br>		< ?php

		include 'human.php';

		use Human\Person;

		$person = new Person();

		echo $person->getName();
		//kết quả: name person
</dd>
</dl>


# reflection 27-1-2021
***
<dl>
1. Access modifier.
<dt>
    - Access modifier là các từ khóa được sử dụng để quy định mức độ truy cập đến lớp và các thành phần của lớp
</dt>
<dt>
- Các mức truy cập:
</dt>
<dd>
+ public: có thể truy cập từ bất cứ đâu
</dd>
<dd>
+ private : các phương thức và thuộc tính chỉ được phép truy xuất trong cùng một lớp.
</dd>
<dd>
+ protected : các phương thức và thuộc tính được phép truy xuất trong cùng một lớp vf ở các lớp con kế thừa
</dd>
2. static.
<dt>
- Từ khóa static được để sử dụng khai báo các thuộc tính và phương thức của lớp 
</dt>
<dd>
VD: class languages {
<br>pulic static $name = "php";
<br> }
</dd>
<dt>
- Không cần khởi tạo đối tượng vẫn có thể sử dụng các thành phần static
</dt>
<dd>
VD: echo "language one: " + languages::$name;
	<br> // result: language one: php

</dd>
</dl>

### Reflection 26-1

1.Mảng trong php có 3 loại:
- mảng 1 chiều và mảng đa chiều theo chỉ số index giống với javascript
- Mảng liên kết (associative array) là mảng sử dụng các key là tên thay cho chỉ số thông thường
	VD: $age = array("Peter"=>"35", "Ben"=>"37","Joe"=>"43");
		dùng: foreach($age as $key => $value){
			echo $key. ":". $value;
			}
	để duyệt tất cả phần tử ( các cặp key và value tương ứng) của mảng.
2. Nhúng trang php
- nhúng nội dung của một trang php vào một trang php kh
- có một số cơ chế khác nhau:
	+ include "filename.php";
	+ require "filename.php";
	+ include_once "filename.php";
	+ require_once "filename.php";
-sự khách nhau giữa các cơ chế khi xảy ra lỗi:
	+ include, include_once thì tung ra cảnh báo (E-WARNING) và tiếp tục thực thi.
	+ require, require_once thì tung ra lỗi nghiêm trọng (E_COMPIE_ERROR) và dừng thực thi.
- sự khác nhau giữa include, require và include_once, require_once :
	+ include, require thì có thể nhúng trang php nhiều lần ở nhiều nơi.
	+ include_once, require_once chỉ có thể nhúng trang php một lần duy nhất.Nếu lần sau sử dụng lại thì php tự bỏ qua 
3. các kiểu lỗi hay xảy ra:
- lỗi cú pháp (Syntax Error) xảy ra tại thời gian biên dịch trong các ngôn ngữ truyền thống và trong thời gian thông dịch trong js, php
	VD thiếu dấu ngoặc tròn trong biểu thức điều kiện.
- Fatal Error là loại lỗi khi biên dịch code PHP và hiểu những gì mình viết, tuy nhiên nó nhận ra trong đó có một hàm không được khai báo. Điều này có nghĩa là hàm được gọi nhưng hàm đó lại không được định nghĩa. Và dừng thực thi chương trình.
- Warning Errors là lỗi cảnh báo và không dừng việc thực thi chương trình. Lý do chính cho các lỗi cảnh báo là bao gồm một file nào đó bị thiếu hoặc sử dụng tham số không chính xác trong một chức năng.
-Notice Error là một lỗi giống như Warning Errors, tức là những lỗi nhỏ, không nghiêm trọng mà PHP gặp phải khi thực thi tập lệnh 
	 VD: truy cập vào một biến chưa được xác định.

### reflection 25/1/2021

1. Mô hình client - server là khi một máy khách (client) gửi một cái yêu cầu đến máy chủ (server) thì máy chủ sẽ xử lý phía sever và trả về kết quả trong thời gian ngắn nhất.Máy khách và máy chủ giao tiếp được với nhau thông qua giao thức( ở đây học HTTP) và yêu cầu gửi đi từ máy khách gọi là HTTP request và kết quả trả về từ máy chủ là HTTP reponsive
2. máy chủ (server) học trong phần này là LAMP nó bao gồm Linux, Apache, MySQL và PHP các thành phần này được sắp xếp theo các lớp hỗ trợ lẫn nhau gọi là stack phần mềm
-Linux: hệ điều hành nền tảng cho các lớp phần mềm khác
-Apache là webserver dùng để đón nhận các request (yêu cầu) của người dùng, xử lý và trả về kết quả
- MySQL là hệ quản trị CSDL có chức năng lưu trữ dữ liệu, bảo mật, cung cấp công cụ để truy xuất dữ liệu và nhiều tính năng khác
- PHP là ngôn ngữ lập trình phía sever. Xử lý các nhiệm vụ cần thiết hoặc kết nối với CSDL MySQL để lấy thông tin cần thiết sau đó trả về cho Apache.

3. Có loại wedsite
- Web tĩnh (static website) giống như một tờ báo người dùng chỉ có thể xem và không thể tương tác được với nó
- Web động ( dynamic website) có thêm xử lý thông tin và truy xuất dữ liệu nên nội dung của trang web sẽ thay đổi khi khác hàng yêu cầu hoặc theo ngày giờ.
