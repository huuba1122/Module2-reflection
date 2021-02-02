# Module2-reflection
***
## Reflection  2/2/2021.
----
#### 1. clean code.
> clean code là những thuật ngữ chỉ những mã nguồn tốt.
>
> 1.1.Mã nguồn tốt là :
>> - Đơn giản (giải quyết vấn đề một cách ngắn gọn).
>> - Trực tiếp ( giải quyết vấn đề chính xác không lòng vòng).
>> - Dễ đọc.
>> - Dễ cải tiến.
>> - Các định danh thể hiện rõ nghĩa.
>> - Không có mã bị trùng lặp.
>> - Thể hiện được ý tưởng thiết kế.
>
> 1.2.Mục đích :
>> - Giúp ích cho việc cộng tác nhóm.
>> - Dễ dàng hơn cho việc thực hiện thay đổi mở rộng sản phẩm.
>
> 1.3.Các cách thực hành clean code.
>> - Áp dụng coding conventions trong việc đặt tên (biến, hàm, class), số lượng (dòng trong một hàm, số kí tự trong một dòng, số hàm trong một class,..), sử dụng comment, thực hiện xuống dòng..
>> - Sử dụng nguyên lý SOLID.
>> - Sử dụng Seperation of Concern và các mô hình phổ biến như MVC, MVVM để phân tách code thành nhiều thành phần nhỏ, dễ quản lý.
>> - Áp dụng design pattern để giải quyết các vấn đề trong code.
>
> 1.4. Nguyên lý SOLID.
>Hiểu một cách đơn giản SOLID là 5 nguyên lý giúp lập trình viên phát triền phần mềm với kiến trúc tốt 
>> - Single responsibility principle  là một class chỉ nên thực hiện một nhiệm vụ.
>> - Open/closed principle là Có thể thoải mái mở rộng 1 class, nhưng không được sửa đổi bên trong class đó tức là mỗi khi ta muốn thêm chức năng,.. cho chương trình, chúng ta nên viết class mới mở rộng class cũ ( bằng cách kế thừa hoặc sở hữu class cũ) không nên sửa đổi class cũ.
>> - Liskov Substitution Principle là trong một chương trình, các object của class con có thể thay thế class cha mà không làm thay đổi tính đúng đắn của chương trình
>> - Interface Segregation Principle là thay vì dùng 1 interface lớn, ta nên tách thành nhiều interface nhỏ, với nhiều mục đích cụ thể.
>> - Dependency inversion principle là các module cấp cao không nên phụ thuộc vào các modules cấp thấp và Interface (abstraction) không nên phụ thuộc vào chi tiết, mà ngược lại. (phần này hơi triết học).
>
#### 2. Refactoring.
> 2.1.Khái nieemj: Là việc thay đổi cấu trúc bên trong mà không làm thay đổi hành vi với bên ngoài hệ thống.
>
> 2.2.Các mức độ thực hiện: 
>> - Hệ thống.
>> - Chức năng.
>> - File/class.
>> - Method/function.
>
> Tùy theo mức độ mà cấu trúc bên trong hay hành vi bên ngoài sẽ được hiểu khác nhau
>> - VD: Refactoring class thì cấu trúc bên trong ở đây là các method và property còn hành vi bên ngoài là nhiệm vụ class đó thực hiện như vậy việc refactoring class là viết lại các thuộc tính và phương thức sao cho không làm thay đổi nhiệm vụ của class đó.
>
>2.3.Khi nào thì thực hiện refactoring:
>> - Thêm chức năng mới vào source code cũ thì đây là thời điểm đọc lại source code cũ để hiểu và thêm vào một phần mới có thể phần mới này sẽ ảnh hưởng đến phần cũ thì đây là thời điểm thích hợp để refactoring.
>> - Khi tiến hành review code
>> - Khi cần handover (bàn giao code).
>
#### 3. coding conventions.
>3.1.Khái niệm :
>> - Là những tập hợp các quy tắc chung khi lập trình nhằm làm code dễ đọc dễ hiểu do đó dễ quản lý và bảo trì.
>
>3.2.Một số quy tắc :
>3.2.1. Quy tắc đặt tên :
>> - Tên class theo PascalCase và là một danh từ hoặc cụm danh từ
>> - Tên biến theo camelCase hoặc snack_case dùng các danh từ hoặc cụm danh từ, tính từ (isNumber).
>> - Tên hàm theo camelCase hoặc snack_case dùng các động từ để bắt đầu.
>> - Tên hằng thì đặt theo UPPER_CASE (tất cả ký tự đều viết hoa).
>> - Tên phải có nghĩa không viết tắt.
>> - Tránh đặt tên chung chung tối nghĩa hoặc có những ký tự gây nhẫm lẫn.
>
>3.2.2. Quy tắc về số lượng :
>> - Hàm thì không quá 30 dòng.
>> - Lớp thì không nên quá 500 dòng.
>> - Một hàm thì không nên quá 5 tham số.
>> - Một hàm thì chỉ nên làm duy nhất một việc.
>> - Khi khai báo biến thì một dòng chỉ chứa một biến.
>> - Một dòng không nên quá 80 ký tự.
>> - Câu lệnh lồng nhau thì tối đa 4 cấp.
>
>3.2.3. Quy tắc xuống hàng.
>> - Xuống hàng sau dấu phẩy "," hoặc trước các toán từ.
>> - Những cấp lồng nhau thì theo từng cấp.
>
>3.2.4. Comment.
>> - Hạn chế dùng comment để giải thích code mà hãy cải thiện đoạn code của mình.
>> - Chỉ dùng comment khi viết documentation cho thư viện, thông tin đính kèm cho class.










# Reflection 1/2/2021.
***
#### 1.Abstract Class.
> - Nó là một class có tính trừu tượng rất cao đến mức không thể tạo được các đối tượng ở lớp đó thì gọi là abstract class.
> - Bắt buộc phải chứa abstract method và có thể có method thông thường.
>> + abstract method là method chỉ có khai báo (tên và tham số đầu vào).
> - Mức truy cập các abstract method phải ở public hoặc protected để lớp kế thừa có thể định nghĩa lại.
> - Không dùng từ khóa final cho khai báo abstract class và abstract method.
***
#### 2. Interface.
> - Có thể hiểu đây là một dạng bảng thiết kế cho chức năng mà bất kỳ Class nào cũng có thể có. Một interface chứa các hành vi mà một class triển khai.
> - Interface không phải là một lớp đối tượng .
> - Tất cả các hàm trong interface đều ở dạng khai báo và không được định nghĩa (giống lớp abstract).
> - Interface không thể khởi tạo.
***
#### 3. Ưu điểm.
> - Abstract class
>> + Có thể linh động các method. giống như một class thông thường.
>> + Các class extend có thể override hoặc không override các method thường.
>
> - Interface.
>> + Có thể implements nhiều interface(tính đa hình).
>> + Xây dựng được bộ khung mẫu mà các lớp phải follow theo.
>> + Giúp quản lý tốt, nắm bắt được các chức năng phải có cho một đối tượng nào đó.
***
#### 4. Nhược điểm:
> - Abstract class:
>> + Không thể extend nhiều abstract class.
>
> - Interface:
>> + Mỗi khi định nghĩa thêm tính năng, các class impelement nó đồng lọat phải thêm tính năng đó.
***
#### 5. Tại sao lại sử dụng abstract class và interface.
> - Sử dụng abstract để tránh tình trạng khai báo nhiều lớp mà mỗi lớp có những thuộc tính và phương thức tương tự nhau.
> - Sử dụng interface để giải quyết vấn đề đa kế thừa.
> - Sử dụng abstract class và interface giúp dễ mở rộng ứng dụng cũng như bảo trì code.
***
### 6. Khi nào sử dụng.
> - Khi một nhóm đối tượng có cùng bản chất kế thừa từ một class thì sử dụng abstract class.
> - Khi một nhóm đối tượng không có cùng bản chất nhưng chúng có hành động giống nhau thì sử dụng interface.
***



***
# Reflection 29/1/2021
***
#### 1.kế thừa trong php
>- cú pháp: 
>> `class nameChild extents nameParent{
 		// code
 	}`
>- class có tên là "nameChild" được gọi là lớp con.
>- class có tên là "nameParent" được gọi là lớp cha.
>- Lớp con có mọi thuộc tính và phương thức mà lớp cha có (trừ những phương thức và thuộc tính có mức truy xuất "private"). và có thể định nghĩa thêm thuộc tính và phương thức mới.
---
####  2. Các loại kế thừa trong php.
> Trong php có 3 loại kế thừa không hỗ trợ đa kế thừa:
>>- Single Một lớp con chỉ kế thừa từ chỉ một lớp cha.
>>- Multilevel: Một lớp kế thừa từ một lớp cha, lớp cha lại kế thừa từ lớp
khác ở trên nó.
>>- Hierarchical: Một lớp cha có nhiều lớp con với nhiều level khác nhau.
---
#### 3.Method overriding.
>- Method Overriding (ghi đè phương thức) là cơ chế cho phép lớp con định nghĩa lại các phương thức đã được định nghĩa trước đó ở lớp cha.
>- Phương thức override ở lớp con có cùng tên, cùng danh sách tham số và kiểu dữ liệu trả về so với phương thức ở lớp cha.
>- Phương thức ở lớp con phải có access modifier có level bằng hoặc cao hơn so với phương thức ở lớp cha.
>- VD: 
>> Khai bao class lop cha:  
>>	`Class A {  
		function add($num1,$num2){  
		return $num1 + $num2;  
		}  
	}`  
>> khai báo lớp con:
	`class B extents A{  
		function add($num1,$num2){  
			return ($num1 + $num2)*2;  
		}  
	}`
---
#### 4. method overloading:
>-Nạp chồng (Overloading): Việc khai báo trong một lớp có nhiều thuộc tính, nhiều phương thức có cùng tên nhưng với các tham số khác nhau (khác kiểu dữ liệu,khác số lượng tham số). 
> VD:
>> `class A{  
	function area($width){  
		return $width*$width;  
	}  
	function area($width, $height){  
		return $width*$height;  
	}  
}`  
---
#### 5. Final.
>- final class:
>>Khi một class được khai báo là final thì không lớp nào có thể kế thừa nó và nó chỉ có thể khởi tạo được thôi.
>>Cú pháp: Khai báo final class.
>>`final class ClassName
		{
    			//code;
		}`
>>Khi cố tình khai báo một lớp con sẽ thông báo lỗi fatal error. 
>- Final Phương thức:
>>Khi chúng ta khai báo một phương thức là final thì không có một phương thức nào có thể override(ghi đè lại được).
>>Cú pháp: khai báo một phương thức final.
>>`class ClassName
		{
   			 final public function methodName()
    			{
       			 //
   			}
		}`
---
#### 6. Hàm khởi tạo.
>- Hàm khởi tạo cũng là một hàm bình thường nhưng có điểm đặc biệt là nó luôn luôn được gọi tới khi ta khởi tạo một đối tượng.
>- Hàm khởi tạo có thẻ có tham số hoặc không có tham số, có thể có giá trị trả về hoặc không.

>- Hàm khởi tạo trong kế thừa:
>>+ TH1: Nếu lớp Con có hàm khởi tạo và lớp cha cũng có hàm khởi tạo thì hàm khởi tạo của lớp con sẽ được chạy, còn hàm khởi tạo ở lớp cha không được chạy.
>>+ TH2: Nếu lớp con không có hàm khởi tạo, lớp Cha có hàm khởi tạo thì hàm khởi tạo ở lớp cha sẽ được chạy.
>>+ TH3: Nếu lớp Con có hàm khởi tạo, lớp cha không có hàm khởi tạo thì hàm khởi tạo lớp con sẽ được chạy.
>- Trong PHP, hàm khởi tạo không cho phép chúng ta thực hiện việc overload, nó chỉ cho phép khởi tạo 1 đối tượng duy nhất ứng với method `__contructs()` được khai báo trong class(không khai báo mặc định là không truyền gì).
>
>- Trong PHP có hai cách khai báo tên hàm khởi tạo. 
>>+ Cách thứ nhất là khai báo tên trùng với tên lớp: 
>>`class SinhVien
		{
   			function SinhVien() {
        			echo 'Lớp Sinh Viên vừa được khởi tạo';
   			}
		}`
>>+ Cách thứ hai là khai báo với tên (_ _construct).
>>`class SinhVien
		{
		    function __construct() {
			echo 'Lớp Sinh Viên vừa được khởi tạo';
		    }
		}`
>
---
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

# Reflection 26-1

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

# reflection 25/1/2021

1. Mô hình client - server là khi một máy khách (client) gửi một cái yêu cầu đến máy chủ (server) thì máy chủ sẽ xử lý phía sever và trả về kết quả trong thời gian ngắn nhất.Máy khách và máy chủ giao tiếp được với nhau thông qua giao thức( ở đây học HTTP) và yêu cầu gửi đi từ máy khách gọi là HTTP request và kết quả trả về từ máy chủ là HTTP reponsive

2. máy chủ (server) học trong phần này là LAMP nó bao gồm Linux, Apache, MySQL và PHP các thành phần này được sắp xếp theo các lớp hỗ trợ lẫn nhau gọi là stack phần mềm

-Linux: hệ điều hành nền tảng cho các lớp phần mềm khác

-Apache là webserver dùng để đón nhận các request (yêu cầu) của người dùng, xử lý và trả về kết quả

- MySQL là hệ quản trị CSDL có chức năng lưu trữ dữ liệu, bảo mật, cung cấp công cụ để truy xuất dữ liệu và nhiều tính năng khác

- PHP là ngôn ngữ lập trình phía sever. Xử lý các nhiệm vụ cần thiết hoặc kết nối với CSDL MySQL để lấy thông tin cần thiết sau đó trả về cho Apache.

3. Có loại wedsite

- Web tĩnh (static website) giống như một tờ báo người dùng chỉ có thể xem và không thể tương tác được với nó

- Web động ( dynamic website) có thêm xử lý thông tin và truy xuất dữ liệu nên nội dung của trang web sẽ thay đổi khi khác hàng yêu cầu hoặc theo ngày giờ.

# Reflection module 2:

MỤC TIÊU

1. Nắm vững về cấu trúc dữ liệu và thuật toán.

2.Thiết kế được wedsite và các ứng dụng wedsite bằng ngôn ngữ lập trình PHP dựa trên mô hình lập trình hướng đối tượng.

3. thiết kế và quản lý được cơ sở dữ liệu bằng SQL

4. sử dụng thành thạo CSS và framework bootstrap để phát triển wedsite chuẩn reponsive
