# Module2-reflection
***
## Reflection.
#### Mô hình MVC.
1. Giới thiệu:
>
>- MVC là chữ viết tắt của Model - View - Controller, đây là một mô hình kiến phần mềm được tạo ra với mục đích quản lý và xây dựng dự án phần mềm có hệ thống hơn.
>- Mô hình này được dùng khá rộng rãi và đặc biệt là trong các ngôn ngữ lập trình web.
>- Trong PHP hiện tại có khá nhiều Framework và tất cả đều xây dựng từ mô hình MVC.
>- Mô hình MVC là mô hình cấu trúc gồm ba lớp : Model, View, Controller.
>>- Model: có nhiệm vụ thao tác với cơ sở dữ liệu, nghĩa là nó sẽ chứa tất cả các hàm, các phương thức truy vấn trực tiếp với dữ liệu và controller sẽ thông qua các hàm, phương thức đó để lấy dữ liệu rồi gửi qua View.
>>- View: có nhiệm vụ tiếp nhận dữ liệu từ controller và hiển thị nội dung sang các đoạn mã HTML, bạn có thể hiểu nôm na đây người ta còn gọi là thành phần giao diện.
>>- Controller: đóng vài trò trung gian giữa Model và View. Nó có nhiệm vụ tiếp nhận yêu cầu từ client sau đó xử lý request, load model tương ứng và gửi data qua view tương ứng rồi trả kết quả về cho client
>
2. Ưu Điểm.
>
>- Hệ thống phân ra từng phần nên dễ dáng phát triển
>- Chia thành nhiều modun nhỏ nên nhiều người có thể làm chung dự án
>- Vấn đề bảo trì dễ hơn và cũng dễ nâng cấp.
>- Dễ dàng debug trong quá trình xây dựng
>
3. Nhược điểm.
>
>- Đối với dự án nhỏ việc áp dụng mô hình MVC gây cồng kềnh, mất thời gian để xây dựng thư viện, cấu trúc.
>- Tốn thời gian trung chuyển dữ liệu của các thành phần. 
>- Phải có kiến thức vững và chuẩn, để tránh bị nhầm lẫn về các mô hình.

---
## Reflection 2/3/2021.
#### CRUD trong SQL.
1.INSERT.
>
>- Câu lệnh INSERT INTO được sử dụng để chèn một bản ghi mới vào bảng. 
>- Cú pháp: 
>>- Cách 1: Sử dụng khi bạn chỉ định một số cột sẽ chèn dữ liệu vào.

		INSERT INTO table_name (column1, column2, column3, ...) 
		VALUES (value1, value2, value3, ...) 
>>- Cách 2: Sử dụng khi bạn muốn chèn giá trị cho tất cả các cột.

		INSERT INTO table_name VALUES (value1, value2, value3, ...) 

>
2.Lệnh UPDATE.
>
>- Câu lệnh UPDATE để cập nhật lại dữ liệu trong bảng.
>- Cú pháp:
	
		UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition 

>
3.Lệnh DELETE
>
>- Câu lệnh delete để xóa dữ liệu trong bảng.

>- Cú pháp: 

		delete from table_name where condition

>
4. Lệnh SELECT
>
>- Câu lệnh SELECT để hiện thị dữ liệu trong bảng. Dữ liệu trả về lưu trong bảng kết quả.

>- Cú pháp: 

		select column1, column 2, ... from table_name

---
## Reflection 1/3/2021.
#### View.
1. Khái niệm.
>
>-  View là một loại bảng ảo cho phép người dùng thực hiện các thao tác sau:
>>- Cấu trúc dữ liệu theo cách mà người dùng tìm thấy tự nhiên hoặc trực quan.
>>- Hạn chế quyền truy cập vào dữ liệu theo cách mà người dùng có thể nhìn thấy và (đôi khi) sửa đổi chính xác những gì họ cần.
>>- Tóm tắt dữ liệu từ các bảng khác nhau có thể được sử dụng để tạo báo cáo.
>
2. Cú pháp.
>
>- Cú pháp tạo VIEW cơ bản như sau:
>>- CREATE VIEW view_name AS SELECT column1, column2..... FROM table_name WHERE [condition];
>
>- Truy vấn  tương tự như truy vấn một bảng thực tế.
>>- VD: SELECT * FROM VIEW_NAME;
>

#### INDEXES.
1. Đặc diểm.
>
>- Một chỉ mục (index) là một cấu trúc dữ liệu giúp cải thiện tốc độ hoạt động trong một bảng. Các chỉ mục có thể được tạo bằng cách sử dụng một hoặc nhiều cột, giúp tra cứu ngẫu nhiên các bản ghi nhanh chóng và sắp xếp các bản ghi hiệu quả.
>- Thực tế, các chỉ mục cũng là một loại bảng, giữ khóa chính hoặc trường chỉ mục và một con trỏ cho mỗi bản ghi vào bảng thực tế.
>- Người dùng không thể xem các chỉ mục, chúng chỉ được sử dụng để tăng tốc độ truy vấn và sẽ được công cụ tìm kiếm cơ sở dữ liệu sử dụng để định vị các bản ghi nhanh chóng.
>- Các câu lệnh INSERT và UPDATE mất nhiều thời gian hơn trên các bảng có chỉ mục. Lý do là trong khi thực hiện chèn hoặc cập nhật, cơ sở dữ liệu cũng cần chèn hoặc cập nhật các giá trị chỉ mục.
>
2. Cú pháp.
>
>- Bạn có thể tạo một chỉ mục duy nhất (unique index) trên một bảng. Một chỉ mục duy nhất có nghĩa là hai hàng không thể có cùng giá trị chỉ mục. Đây là cú pháp để tạo một chỉ mục duy nhất trên một bảng:
>>- CREATE UNIQUE INDEX index_name ON table_name ( column1, column2,...);
>
>- Câu lệnh này thêm một chỉ mục bình thường trong đó bất kỳ giá trị nào có thể xuất hiện nhiều hơn một lần.
>>- CREATE INDEX CUSTOMER_INDEX ON customers (customerNumber);
>
>- Primary key trong bảng cũng là một loại chỉ mục.
>

#### PROCEDURE.
1. Khái niệm.
>
>-  Stored Procedure được tạo ra nhằm thực hiện các lệnh của mysql theo một nhóm việc cụ thể thay vì thực hiện từng thao tác (insert,update,delete).Tương tự như khái niệm function trong các ngôn ngữ lập trình.
>
2. Đặc điểm.
>- Stored Procedure làm tăng hiệu xuất sử lý giữ liệu
>- Làm giảm thời gian giao tiếp giữa ứng dụng với hệ quản trị cơ sở giữ liệu. thay vì gửi từng câu truy vấn thì nay sẽ chỉ gửi một Stored Procedure.
>- Stored Procedure có thể lưu lại và sử dụng lại nhiều lần.
>- Nâng cao tính bảo mật dữ liệu: việc thao tác với database thông qua stored procedure mà không cho thao tác trực tiếp với database sẽ làm giảm các cuộc tấn công thông qua sql injection.
>- Tạo ra quá nhiều Procedure thì hệ quản trị sẽ sử dụng bộ nhớ để lưu trữ các thủ tục này khá nhiều.
>- Ngoài ra nếu bạn thực hiện quá nhiều xử lý trong mỗi thủ tục thì đồng nghĩa với việc CPU sẽ làm việc nặng hơn.
>- MYSQL thì không có tool hỗ trợ Debug Store.
>
3. cú pháp.
> 
>- Cú pháp tạo stored procedure.
>
			DELIMITER //
			BEGIN
			CREATE PROCEDURE  stored_procedure_name
			END //
			DELIMITER ;
		
>
>- Sử dụng.
>>- CALL stored_procedure_name;

---
## Reflection 26/2/2021.
#### Một số hàm thao tác với dữ liệu trong SQL.
---
1. Count()
>
>- Hàm COUNT() trả về số bản ghi phù hợp với tiêu chí đã chỉ định.
>-  cú pháp :
>>- SELECT COUNT(tên_cột) FROM tên_bảng WHERE điều_kiện;
>
2. AVG().
>
>- Hàm AVG() trả về giá trị trung bình của một cột số.
>- cú pháp : 
>> -SELECT AVG(tên_cột) FROM tên_bảng WHERE điều_kiện;
>
3. SUM()
>
>- Hàm SUM() trả về tổng số của một cột số.
>- cú pháp:
>>- SELECT SUM(tên_cột) FROM tên_bảng WHERE điều_kiện;
>
4. MIN().
>
>- Hàm MIN() trả về giá trị nhỏ nhất của cột đã chọn.
>- Cú pháp:
>>- SELECT MIN(tên_cột) FROM tên_bảng WHERE điều_kiện;
>
5. MAX()
>
>- Hàm MAX() trả về giá trị lớn nhất của cột được chọn.
>- cú pháp:
>>- SELECT MAX(tên_cột) FROM tên_bảng WHERE điều_kiện;



----
## Reflection 25/2/2021.
---
#### Một số câu lệnh truy vấn trong SQL với MySQL.
---
1.1 And và OR.
>
>- Toán tử AND trả về false nếu một trong hai biểu thức kết hợp được đánh giá là sai. 
>> - cú pháp: WHERE boolean_expression_1 AND boolean_expression_2
>
>- Toán tử OR kết hợp hai hay nhiều biểu thức dạng boolean, chỉ cần một trong các điều kiện kết hợp là đúng thì kết quả là true. 
>> - cú pháp: WHERE boolean_expression_1 OR boolean_expression_2
>
1.2. Group by và mệnh đề HAVING.
>
>- mệnh đề group by là một phần không bắt buộc của câu lệnh SELECT, được sử dụng để nhóm các tập các hàng có cùng một giá trị vào thành một nhóm, mỗi nhóm đó chỉ trả về một hàng.
>> - cú pháp : SELECT column1 FROM table-name GROUP BY column1;
>
>- Mệnh đề HAVING thay cho WHERE để hạn chế dữ liệu trả về trong tập kết quả. Mệnh đề WHERE dùng với các cột của bảng, tuy nhiên không dùng được với các hàm tập hợp. Mệnh đề HAVING dùng với các hàm tập hợp và đi sau GROUP BY.
>> - Cú pháp : SELECT columnname(s) FROM tablename WHERE conditional GROUP BY column... HAVING conditional
>
1.3. JOIN.
>
>- Mệnh đề JOIN được sử dụng để kết hợp các hàng từ hai hay nhiều bảng, dựa trên cột liên quan giữa chúng. JOIN gồm 3 loại cơ bản INNER JOIN, LEFT JOIN, RIGHT JOIN trong MySQL không hỗ trợ FULL JOIN.
>> - cú pháp : SELECT column_name(s) FROM table1 INNER|LEFT|RIGHT JOIN table2 ON join_condition1 INNER|LEFT|RIGHT  JOIN table3 ON join_condition2 … WHERE conditions;
>- INNER JOIN khớp các hàng trong một bảng với các hàng trong các bảng khác và cho phép bạn truy vấn các hàng có chứa các cột từ cả hai bảng. 
>- LEFT JOIN cho phép bạn chọn các hàng từ cả hai bảng bên trái và bên phải khớp với tất cả các hàng từ bảng bên trái (table1) ngay cả khi không có kết quả tìm thấy trong bảng bên phải (table2).
>- RIGHT JOIN cho phép bạn chọn các hàng từ cả hai bảng bên trái và bên phải khớp với tất cả các hàng từ bảng bên phải (table2) ngay cả khi không có kết quả tìm thấy trong bảng bên phải (table1).
>
---
## Reflection 24/2/2021.
---
#### Thiết kế và tạo cơ sở dữ liệu.
1 Mục đích :
>
> - Tìm ra một mô hình CSDL phù hợp với yêu cầu của khách hàng.
> 
2 Các bước thực hiện.
>
> - b1: Xác định mục đích của CSDL.
> - b2: Tìm hiểu và tổ chức các thông tin cần lưu trữ.
> - b3: chia thông tin vào trong các bảng.
> - b4: Xác định trường dữ liệu của từng bảng.
> - b5: Khóa chính của các bảng.
> - b6: Mối quan hệ giữa các bảng.
> - b7: Làm mịn thiết kế.
> - b8: Áp dụng các quy tắc chuẩn hóa.
> 
3. Khóa chính (Primary key).
>
> - Dùng để xác định mẫu tin trong bảng là duy nhất.
> - Mỗi bảng chỉ tồn tại duy nhất một khóa chính.
> - Mỗi khóa chính có thể là một hay một nhóm các trường.
> - Giá trị khóa chính không được phép để null và giá trị đó là duy nhất trong bảng.
> 
4. Khóa ngoại (foreign key). 
>
> - Là tập hợp các thuộc tính trong bảng tham chiếu đến bảng khác.
> - bảng chứa khóa ngoại là bảng con còn bảng nó tham chiếu đến nó là bảng cha.
> - Giá trị của khóa ngoại nó cùng kiểu, cùng độ dài, cùng giá trị với cột của bảng nó tham chiếu đến.
> 
5. CHuẩn hóa dữ liệu.
>
5.1. Khái niệm.
>
> - Là kỹ thuật thiết kế CSDL tổ chức vào các bảng theo cách làm giảm dư thừa và phụ thuộc vào dữ liệu.
> 
5.2. Quy tắc 1NF.
>
> - Mỗi ô bảng chứa giá trị là nguyên tử (tức là không chia nhỏ hơn nữa).
> - Mỗi bản ghi trong bảng là duy nhất.
> - Không có giá trị của thuộc tính nào có thể tính toán được từ giá trị của thuộc tính khác.
>
5.3. Quy tắc 2NF.
> 
> - Phải là 1NF.
> - Loại bỏ những thuộc tính không khóa phụ thuộc vào một bộ phận khóa chính và tách chúng ra một bảng riêng có khóa chính là khóa mà chúng phụ thuộc vào.
> 
5.4. Quy tắc 3NF.
>
> - Phải là 2NF.
> - Không có phụ thuộc chức năng bắc cầu tức là khi thay đổi một cột không khóa thì không có cột nào trong bảng giá trị bị thay đổi.
> 


---
## Reflection 23/2/2021.
---
#### 1. Cơ sở dữ liệu (database)
1.1 Khái niệm.
> - Cơ sở dữ liệu là một tập hợp các dữ liệu có tổ chức, thường được lưu trữ và truy cập từ hệ thống máy tính.
>
1.2. Mô hình dữ liệu.
>
> - Là cơ chế lưu trữ quản lý và truy vấn dữ liệu.
> - Một số mô hình.
> 
>> - CSDL phân cấp 
>> - CSDL mạng.
>> - CSDL đồ thị.
>> - CSDL quan hệ.
>> - CSDL đối tượng.
>> - ...
>
#### 2. Hệ quản trị cơ sở dữ liệu (Database Management System - DBMS).
2.1. Khái niệm.
> - là phần mềm để quản lý cơ sở dữ liệu.
> 
2.2. Chức năng.
>
> -Các DBMS hiện tại cung cấp các chức năng khác nhau cho phép quản lý cơ sở dữ liệu và dữ liệu có thể được phân loại thành bốn nhóm chức năng chính: 
>> - Định nghĩa dữ liệu: xác định kiểu, ràng buộc của dữ liệu.
>> - Cập nhật dữ liệu : Chèn, sửa đổi và xóa dữ liệu thực tế.
>> - Truy xuất : Cung cấp thông tin dữ liệu dưới dạng có thể sử dụng trực tiếp hoặc để xử lý thêm bởi các ứng dụng khác.
>> - Quản lý dữ liệu : Bảo mật dữ liệu, theo dõi, sao lưu và có thể khôi phục thông tin đã bị hỏng do lỗi.
>
2.3. Hệ quản trị cơ sở dữ liệu quan hệ (RDBSM).
> 
> - Hệ quản trị cơ sở dữ liệu quan hệ là hệ thống quản lý cơ sở dữ liệu dựa trên mô hình quan hệ hay hệ quản trị CSDL dùng để tạo lập, cập nhật và khai thác CSDL quan hệ là hệ quản trị CSDL quan hệ.
> 
#### 3. SQL (structured query language).
> - Ngôn ngữ truy vấn có cấu trúc là một loại ngôn ngữ máy tính để thao tác với hệ quản trị cơ sở dữ liệu quan hệ (RDBMS).
> 
---
## Reflection 22/2/2021.
---
### Biểu thức chính quy (regular Expression).
---
1. Khái niệm.
>
> - Miêu tả một chuỗi theo những quy tắc cú pháp nhất định.
> - là biểu thức được sử dụng để chỉ định một chuỗi các chuỗi cần thiết cho một mục đích cụ thể.
> 
2. Tác dụng.
>
> - Tìm kiếm và thay thế một chuỗi con trong một chuỗi lớn.
> - Xác thực form (validate form).
> - Tiết kiệm thời gian lập trình.
>
3. Một số hàm thao tác với biểu thức chính quy trong php.
>
> - preg_match() : được dùng để kiểm tra, so khớp và lấy kết quả của việc so sánh chuỗi dựa vào biểu thức chính quy.
> - preg_match_all(): cũng tương tự hàm preg_match() ở trên , tuy nhiên hai hàm này khác nhau ở chỗ , hàm preg_match_all() sẽ trả về toàn bộ các giá trị được so sánh khớp, còn hàm preg_match() chỉ trả về giá trị đầu tiên được so sánh khớp.
> - pre_split: để chia nhỏ chuỗi thành mảng chứa các chuỗi con. 
> - preg_replace dùng để tìm kiếm và thay thế một chuỗi nào đó khớp với đoạn Regular Expression truyền vào. 
> 
---
## Reflection 19/2/2021.
---
#### Xử lý ngoại lệ.
---
1.Khái niệm.
>
> - Xử lý ngoại lệ được sử dụng để thay đổi luồng chương trình khi xảy ra một lỗi bất thường mà người lập trình không kiểm soát được.
> - VD:
>> - Không tìm thấy file cần mở.
>> - Kết nối mạng bị ngắt trong quá trình thực hiện thao tác.
>> - Nhập dữ liệu không hợp lệ.
>> - Tràn bộ nhớ.
>> - Truy cập ngoài chỉ số của mảng.
>> - ...
>
2. Exception.
>
> - Là một giải pháp quản lý lỗi kiểu hướng đối tượng.
> - Là một lớp có sẵn trong PHP.
> - chứa thông tin về nơi xảy ra lỗi.
> - Một số hàm trong Exception.
>> - getMessage() : Hiển thị tin nhắn ngoại lệ
>> - getCode() : Hiển thị các mã số là đại diện của các loại ngoại lệ.
>> - getFile() : Hiển thị tên các tập tin và đường dẫn nơi xảy ra ngoại lệ.
>> - getLine() : Hiển thị các dòng xảy ra ngoại lệ.
>> - toString(): Hiển thị toàn bộ ngoại lệ như một chuỗi.
>
3. Lớp ngoại lệ tùy chỉnh.
>
> - Là một đặc biệt với các hàm có thẻ được gọi khi một ngoại lệ xảy ra trong php. Lớp này kế thừa từ lớp Exception.
> - Lớp ngoại lệ tùy chỉnh kế thừa các thuộc tính từ lớp Exception của PHP và có thể thêm các hàm tùy chỉnh vào nó.
> - Mục Đích.
> 
>> - thay đổi nội dung thông báo.
>> - Thông báo một nghiệp vụ đang bị lỗi được chỉ định trước.
>
4. Sử dụng try - throw - catch để xử lý ngoại lệ.
>
> - try: chứa đoạn mã có khả năng xảy ra ngoại lệ. Nếu không có ngoại lệ xảy ra thì mã tiếp tục chạy như bình thường. Tuy nhiên nếu có xảy ra ngoại lệ thì mộ ngoại lệ sẽ bị ném ra bằng từ khóa throw.
> - throw: Ngoại lệ được kích hoạt. Mỗi throw phải bao gồm ít nhất một khối catch.
> - catch: lấy ra một ngoại lệ và tạo ra một đối tượng chứa thông tin ngoại lệ. và trong khối catch ta có thể viết chương trình xử lý ngoại lệ đó.
> - cú pháp.
> 
		try 
		{
		    //Khối lệnh mà có thể phát sinh Exception
		} 
		catch (Exception $e) 
		{    
		    //Khối lệnh bắt được Exception
		}
>
---
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
>- Giải thuật sắp xếp này được tiến hành dựa trên việc so sánh cặp phần tử liền kề nhau và tráo đổi thứ tự nếu chúng không theo thứ tự.
>-Giải thuật này không thích hợp sử dụng với các tập dữ liệu lớn khi mà độ phức tạp trường hợp xấu nhất và trường hợp trung bình là Ο(n2) với n là số phần tử.
>
3. Insertion Sort (sắp xếp chèn).
>
>- Với cấu trúc dữ liệu mảng, chúng ta tưởng tượng là: mảng gồm hai phần: một danh sách con đã được sắp xếp và phần khác là các phần tử không có thứ tự. Giải thuật sắp xếp chèn sẽ thực hiện việc tìm kiếm liên tiếp qua mảng đó, và các phần tử không có thứ tự sẽ được di chuyển và được chèn vào vị trí thích hợp trong danh sách con (của cùng mảng đó).
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
