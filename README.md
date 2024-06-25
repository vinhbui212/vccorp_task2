
Spring Boot là một dự án phát triển bởi JAVA (ngôn ngữ java) trong hệ sinh thái Spring framework. Nó giúp cho các lập trình viên chúng ta đơn giản hóa quá trình lập trình một ứng dụng với Spring, chỉ tập trung vào việc phát triển business cho ứng dụng.
Để phát triển một ứng dụng web cơ bản HelloWorld sử dụng Spring framework bạn sẽ cần ít nhất 5 công đoạn sau;

Tạo một project sử dụng Maven với các dependency cần thiết của Spring MVC và Servlet API.
Một tập tin web.xml để khai báo DispatcherServlet của Spring MVC.
Một tập tin cấu hình của Spring MVC.
Một class Controller trả về một trang “Hello World” khi có request đến.
Cuối cùng là phải có một web server dùng để triển khai ứng dụng lên chạy.
Trong các công đoạn này, chỉ có công đoạn tạo một class Controller thì có thể khác cho các ứng dụng khác nhau vì mỗi ứng dụng có một yêu cầu khác nhau. Còn các công đoạn khác thì như nhau.

Giờ đây với Spring Boot, chúng ta có thể tạo dự án Spring một cách nhanh chóng và cấu hình cũng đơn giản dùng Sublime Text để phát triển luôn khỏi cần cài đặt eclipse hay netbean nặng bỏ bà.
Dưới đây là một số tính năng nổi bật của Spring Boot:

Tạo các ứng dụng Spring độc lập
Nhúng trực tiếp Tomcat, Jetty hoặc Undertow (không cần phải deploy ra file WAR)
Các starter dependency giúp việc cấu hình Maven đơn giản hơn
Tự động cấu hình Spring khi cần thiết
Không sinh code cấu hình và không yêu cầu phải cấu hình bằng XML …

![image](https://github.com/vinhbui212/vccorp_task2/assets/100837872/d5db9641-972b-49e6-825a-733b95a20f52)
Các thành phần của Spring
- Lớp Controller:
Lớp này nằm trên cùng của kiến trúc Spring Boot. Nó chịu trách nhiệm:
Thực hiện authentication (xác thực).
Chuyển đổi dữ liệu JSON thành đối tượng (và ngược lại).
Xử lý các HTTP request
Truyền authentication tới lớp bussiness
 Class Controller xử lý tất cả các REST API request (GET, POST, PUT, DELETE, PATCH) đến từ client
 - Lớp Service:
Lớp này chịu trách nhiệm:
Thực hiện validation.
Thực hiện authorization (uỷ quyền).
Xử lý các logic và quy tắc nghiệp vụ.
 là nơi xử lý logic nghiệp vụ. Ngắn gọn thì logic nghiệp vụ trong kỹ nghệ phần mềm là những gì mà chúng ta xác định phần mềm cần phải làm. 
 Một ví dụ là validation. Nếu bạn muốn validate gì đó, nó phải được thực hiện trong class Service.
- Interface repository
Lớp này chịu trách nhiệm:
Chứa các logic lưu trữ
Lấy các đối tượng và chuyển đổi thành các hàng trong database (và ngược lại).
 Chúng ta viết các truy vấn tới database trong interface này.Giao tiếp với lớp Service và database
- Lớp model
 Tượng trưng cho 1 bảng trong database thường dùng hibernate để dễ dàng tạo bảng trong database.
* Ưu điểm
  - Tự động cấu hình một cách mạnh mẽ được nhúng sẵn server khác với java web cũ phải tải và cài đặt cấu hình rất nhiều
  - Ghi đè các bean cũ để sử dụng lại nếu cần
 *Nhược điểm
-Thiếu kiểm soát. Spring Boot tạo ra rất nhiều dependency không được sử dụng, dẫn đến file triển khai có dung lượng lớn.
-Quá trình phức tạp và tốn thời gian để chuyển đổi một dự án Spring cũ hoặc hiện có thành các ứng dụng Spring Boot.
