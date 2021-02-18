# Module2-reflection
***
## Reflection 18/2/2021.
---
1.Giải thuật sắp xếp.
>
>- Giải thuật sắp xếp là xác định cách sắp xếp dữ liệu theo một thứ tự nào đó. Sắp xếp theo thứ tự ở đây là sắp xếp theo thứ tự dạng số hoặc dạng chữ cái.
>- Giải thuật sắp xếp có tác dụng cho việc tối ưu tìm kiếm dữ liệu và sử dụng để biểu diễn dữ liệu dễ đọc hơn.
>
>1.1.giải thuật sắp xếp In-place và not-in-place.
>
>>- Những giải thuật mà không yêu cầu thêm bộ nhớ phụ và việc sắp xếp được tiến hành trong bộ nhó đã khai báo trước đó thì được gọi là In-place (vd: bubble sort, Insertion sort, selection sort).
>>- Những giải thuật cần thêm bộ nhớ mà có thể lớn hơn hoặc bằng với số phần tử đang được sắp xếp thì gọi là not-in-place sorting (VD: merge sort).
>
>1.2.Giải thuật sắp xếp cố định và sắp xếp so sánh.
>
>>- Sau khi sắp xếp những phần tử có giá trị bằng nhau mà vị trí tương đối giữa chúng không thay đổi là sắp xếp cố định. và ngược lại thay đổi vị trí tương đối của 2 phần tử có giá trị bằng nhau thì là sắp xếp so sánh.
>
>1.3. Giải thuật sắp xếp Adaptive và Non-adaptive.
>
>>- khi sắp xếp nếu danh sách ban đầu có một số phần tử đã được sắp xếp, thì giải thuật dạng adaptive sẽ ghi nhận các phần tử này và sẽ cố gắng không thay đổi thứ tự của chúng.
>>- giải thuật dạng non-adaptive sẽ không ghi nhận các phần tử đã được sắp xếp trước đó. Giải thuật loại này sẽ vấn cố gắng sắp xếp lại từng phần tử trong danh sách ban đầu.
>
2. Bubble Sort (sắp xếp nổi bọt).
>
>-Giải thuật sắp xếp này được tiến hành dựa trên việc so sánh cặp phần tử liền kề nhau và tráo đổi thứ tự nếu chúng không theo thứ tự.
>-Giải thuật này không thích hợp sử dụng với các tập dữ liệu lớn khi mà độ phức tạp trường hợp xấu nhất và trường hợp trung bình là Ο(n2) với n là số phần tử.
>
3. Insertion Sort (sắp xếp chèn).
>
>-Với cấu trúc dữ liệu mảng, chúng ta tưởng tượng là: mảng gồm hai phần: một danh sách con đã được sắp xếp và phần khác là các phần tử không có thứ tự. Giải thuật sắp xếp chèn sẽ thực hiện việc tìm kiếm liên tiếp qua mảng đó, và các phần tử không có thứ tự sẽ được di chuyển và được chèn vào vị trí thích hợp trong danh sách con (của cùng mảng đó).
> - Giải thuật này không thích hợp sử dụng với các tập dữ liệu lớn khi độ phức tạp trường hợp xấu nhất và trường hợp trung bình là Ο(n2) với n là số phần tử.
> 
4. Selection Sort ( Sắp xếp chọn).
> 
> - Danh sách được chia thành hai phần, phần được sắp xếp (sorted list) ở bên trái và phần chưa được sắp xếp (unsorted list) ở bên phải.Phần tử nhỏ nhất được lựa chọn từ danh sách chưa được sắp xếp và được tráo đổi với phần bên trái nhất và phần tử đó trở thành phần tử của danh sách được sắp xếp. Tiến trình này tiếp tục cho tới khi toàn bộ từng phần tử trong danh sách chưa được sắp xếp đều được di chuyển sang mảng đã được sắp xếp.
> - Giải thuật này không phù hợp với tập dữ liệu lớn khi mà độ phức tạp trường hợp xấu nhất và trường hợp trung bình là O(n2) với n là số phần tử.
> 
---
## Reflection 17/2/2021.
---
1. Tìm kiếm tuyến tính (Linear Search).
>
>1.1. Khái niệm.
>
> - Tìm kiếm tuyến tính là hoạt động tìm kiếm liên tiếp được diễn ra qua tất cả từng phần tử. Mỗi phần tử đều được kiểm tra và trả về kết quả nếu tìm thấy phần tử đó nếu không thấy thì tìm kiếm đến hết dữ liệu.
>
>1.2. Đặc điểm.
>
>- Có thể áp dụng với đối với bất kỳ mảng dữ liệu nào mà không cần phải sắp xếp theo một trật tự nhất định.
>- Độ phức tạp thời gian là O(n).
>
2. Tìm kiếm nhị phân (Binary Search).
>
>2.1. Khái niệm.
>
> - Binary search tìm kiếm một phần tử cụ thể bằng cách so sánh phần tử tại vị trí giữ nhất của tập dữ liệu. Nếu tìm thấy thì trả về kết quả chỉ mục của phần tử đó. Nếu phần tử cần tìm lớn hơn phần tử gìữa thì phần tử cần tìm nằm bên mảng con bên phải của phần tử giữa, nếu không thì sẽ tìm ở trong mảng con nằm ở bên trái phần tử giữa. Quá trình lặp lại cho đến khi tìm hết mọi phần tử trên mảng con này.
>
>2.2. Đặc điểm.
>
> - Tìm kiếm nhị phân là một giải thuật tìm kiếm nhanh với độ phức tạp thời gian là O(log n).
> - Giải thuật tìm kiếm nhị phân làm việc trên nguyên tắc chia để trị (divide and conquer).
> - Dùng trong tìm kiếm dữ liệu đã được sắp xếp. 
---
## Reflection 5/2/2021.
---
> 1. Standard php library - SPL.
>
> 1.1. Khái niệm. 
>
>> - Là bộ thư viện chuẩn của PHP nhằm giải quyết các bài toán phổ biến.
>
> 1.2. Bao gồm.
>
>> - Perdifined constants Danh sách hằng số.
>> - Datastructures : Các cấu trúc dữ liệu khác nhau như LinkedList, Stack, Queue, Map....
>> - Interface : danh sách các Interface.
>> - Iterator : Các lớp có khả năng thực hiện phép lặp để duyệt qua các cấu trúc khác nhau.
>> - Exceptions : Danh sách lớp điều khiển ngoại lệ.
>> - File handling : Cung cấp các lớp làm việc với file hệ thống.
>> - Spl function : Các hàm hỗ trợ cần thiết.
>
> 2. Class SplDoublyLinkedList.
>
> 2.1. Khái niệm :
>> - cung cấp các chức năng chính của một danh sách liên kết đôi
>> - cung cấp các hàm để làm việc và thao tác với dữ liệu.


---
## Reflection 4/2/2021.
---
#### 1. Stack.
> 
> 1.1. khái niệm.
>> - Là một loại cấu trúc dữ liệu tuyến tính hoạt động theo cơ chế first in/last out tức là dữ liệu vào trước thì sẽ lấy ra sau.
>
> 1.2. Ứng dụng trong thực tế.
>> - Hiển thị nội dung history của trình duyệt.
>> - Nội dung cập nhật ứng dụng.
>
#### 2. Queue.
>1.1.Khái niệm.
> - Là một cấu trúc dữ liệu tuyến tính dạng danh sách trong đó việc thêm và lấy các phần tử được thực hiện theo quy tắc FIFO (first in/first out) tức là phần tử nào thêm trước thì sẽ được lấy ra trước.
>
>1.2.Ứng dụng trong thực tế.
>> - Danh sách khám bệnh ở bệnh viện.
>> - Thứ tự đặt vé ở sân bay, rạp chiếu phim..
>
#### 3. Tree.
>
> 1.1. Khái niêm.
> - Là cấu trúc dữ liệu phi tuyến hoạt động theo nguyên tắc phân cấp, trong đó có mối quan hệ cha con giữa các node.
>- cấu trúc :
>> - Root là nốt gốc tức là ko có cha.
>> - Node mà ko có con thì gọi là leaf (nút lá).
>> - Những node có chung cha gọi là sibling.
>> - Đường kết nối giữa các node gọi là edges.
>
> 1.2. Đặc điểm.
> - Tốc độ truy xuất ở mức trung bình nó sẽ nhanh hơn dạng linked list và chậm hơn dạng Array list.
> - Tốc độ xử lý dữ liệu như thêm phần tử, xóa phần tử thì nhanh hơn dạng array list và chậm hơn linked list.
> - sử dụng tài nguyên bộ nhớ tốt hơn dạng list. 




---
## Reflection 3/2/2021.
---
#### 1. Cấu trúc dữ liệu (data structures):
> 1.1. Khái niệm :
>> - là hình thức tổ chức dữ liệu để sử dụng một cách hiệu quả.
>
> 1.2. Chức năng :
>> - Lữu trữ dữ liệu.
>> - Cung cấp các phương thức để thao tác với dữ liệu.
>
> 1.3. Thành phần chính trong một cấu trúc dữ liệu.
>> - Container: là lớp chứa dữ liệu và cung cấp các phương thức để thao tác với dữ liệu.
>> - Elements là các phần tử của dữ liệu.
>
> 1.4. Khi nào dùng và dùng như thế nào.
>> -  Tùy vào yêu cầu của mỗi bài toán mà có những cách chọn cấu trúc dữ liệu khác nhau.
>
> 1.5. Tại sao phải dùng.
>> - Liên quan đến hiệu năng của hệ thống.
>> - VD: khi dữ liệu chứa cả triệu thông tin sản phẩm và các khách hàng search theo tên một sản phẩm bất kỳ với một số lượng thông tin lớn như thế làm sao để trả về sản phẩm mà khách hàng muốn tìm kiếm trong thời gian cho phép. Như vậy nếu việc cấu trúc dữ liệu của mình tốt thì mất ít thời gian trả về hơn so với một cấu trúc dữ liệu chưa tốt.
>
>1.6. Một số loại cấu trúc dữ liệu thông dụng.
>> - Set nhóm phần tử không trùng nhau.
>> - List Nhóm các phần tử có thể trùng nhau.
>> - Stack Nhóm các phần tử theo trật tự vào trước ra sau.
>> - Queue Nhóm các phần tử theo trật tự vào trước ra trước
>> - Map Lưu dữ liệu theo cặp key - Value.
>> - Tree Lưu dữ liệu theo quan hệ cha con
>> - Grap lưu dữ liệu theo quan hệ mạng lưới.

---
#### 2. ArrayList.
> 2.1 Khái niệm. 
>> - Là một cấu trúc dữ liệu danh sách sử dụng mảng để lưu trữ dữ liệu.
>
> 2.2.Đặc điểm.
>> - Truy xuất nhanh đến các phần tử (truy xuất theo index).
>> - Các thao tác thêm sửa xóa không hiệu quả vì phải dịch chuyển lại các phần tử của mảng.
>
> 2.3. Hoạt động.
>> - Thêm, sửa, xóa, tìm kiếm, duyệt..
---
#### 3. Linked List
>
> 3.1 Khái niệm.
>> - Là cấu trúc dữ liệu danh sách chứa các phần tử trong đó mỗi phần tử liên kết với phần tử tiếp theo của nó.
>> - Mỗi phần tử bao gồm : Trường dữ liệu chứa giá trị thực sẽ được lưu trữ, xử lý và Trường liên kết giữ địa chỉ mục dữ liệu tiếp theo trong danh sách liên kết.
>
> 3.2. Đặc điểm.
>
>- Ưu điểm.
>> - Thao tác thêm xóa phần tử nhanh hơn loại Array list vì chỉ cần xác định phần tử trước đó và phần tử sau nó sau đó xóa trường liên kết của nó và cho trường liên kết của phần tử trước nó trỏ đến phần tử sau nó là xong.
>> - Tốn ít tài nguyên bộ nhớ.
> - Nhược điểm.
>> - vì các phần tử liên kết với nhau thành chuỗi như thế nên việc tìm kiếm một phần tử bất kỳ cũng đều phải duyệt từ phần tử đầu tiên trở đi làm mất nhiều thời gian
>
> 3.3. Các loại linked List.
>> - Simple linked list chỉ duyệt các phần tử theo chiều về phía trước tức là các phần tử phía trước chỉ trỏ đến thằng sau nó.
>> - Double linked list các phần tử có thể duyệt cả về trước lẫn về sau do các phần tử đều trở về cả phần tử trước nó và cả phần tử sau nó.
>> - Circular linked list phần tử cuối cùng thì trỏ về phần tử đầu tiên.
>
> 3.4. Các hoạt động.
>> - Thêm 1 phần tử.
>> - Xóa một phần tử.
>> - Duyệt.
>> - Tìm kiếm.


---
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
>
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
