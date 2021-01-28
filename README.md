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
