# Cấu trúc source

## The Root Directory (Thư mục gốc)

The Root Directory
* The app Directory
* The bootstrap Directory
* The config Directory
* The database Directory
* The public Directory
* The resources Directory
* The routes Directory
* The storage Directory
* The vendor Directory

The App Directory
* The Broadcasting Directory
* The Console Directory
* The Exceptions Directory
* The Http Directory
* The Providers Directory

### The App Directory (Thư mục ứng dụng)

Chứa mã core 

### The Bootstrap Directory (Thư mục khởi động)

Chứa file khởi động ứng dụng -> **app.php**
Chứa thư mục **cache** -> tối ưu hoá hiệu xuất

### The Config Directory (Thư mục cấu hình)

Chứa tất cả các file cấu hình ứng dụng

### The Database Directory (Thư mục cơ sở dữ liệu)

* database migrations -> version control của database -> quản lý tất cả phiên bản -> cho phép thay đổi db, trạng thái db.(Đọc thêm [migrations](https://viblo.asia/p/migration-trong-laravel-va-nhung-dieu-can-biet-ByEZkyEy5Q0))
* model factories -> Tạo dữ liệu với số lượng bản ghi lớn, tối ưu code. Dễ thay đổi số lượng bản ghi  (Đọc thêm [factory](https://viblo.asia/p/seeder-va-model-factory-trong-laravel-ban-da-thu-chua-ByEZkvoAKQ0))
* seeds -> Tạo dữ liệu mẫu (Đọc thêm [seeds](https://viblo.asia/p/seeder-va-model-factory-trong-laravel-ban-da-thu-chua-ByEZkvoAKQ0))

### The Public Directory (Thư mục công cộng)

* Entry point cho tất cả requests entering ứng dụng và tự động tải cấu hình, chứ ảnh, JavasScript, CSS

### The Resources Directory (Thư mục tài nguyên)

* Chứa các views, raw (nội dung chưa qua xử lý), chưa được biên dich như LES, SASS hoặc JavaScript. 
* Chức file languages

### The Routes Directory ( Thư mục tuyên đường)

* Định nghĩa các tuyến đường ứng dụng
* Mặc định
    * web.php
        - Middleware group -> session state (trạng thái phiên), CSRF protection (Bảo vệ phiên), and cookie encryption (Mã hoá cookie). Nếu app không cung cấp stateless, RESTful API => có thể xác định các file routes ở đây.
    * api.php
        - Middleware group -> rate limiting (hạn chế tốc độ). Xác thực requests thông qua token và không có quyền truy cập sesstion state (trạng thái phiên)

### The Storage Directory (Thư mục lưu trữ)

Chứa Blade templates đã biên dịch, file based sessions, file caches, và một vài file khác được tạo bởi framework

* **app** -> Chứa bất kỳ file do ứng dụng tạo ra
* **framework** -> Lưu files và caches do framework tạo ra
* **log** -> Chứa files nhật ký do ứng dụngt tạo ra

Thư mục app/public -> Lưu file do người dùng tạo (ảnh,...).

## The Vendor Directory (Thư mục nhà cung cấp)

Chứa **Composer** dependencies:

## The App Directory (Thư mục ứng dụng)

### The Broadcasting Directory (Thư mục phát sóng)

Chứa bradcast channel classes (các lớp kênh quản bá) cho ứng dụng (Đọc thêm [event broadcasting](https://laravel.com/docs/8.x/broadcasting))

### The Console Directory (Thư mục bảng điều khiển)

Chứa, đăng ký Artisan commands(các lệnh), xác định tác vụ đã lên lịch -> dùng lệnh **make:command** (Đọc thêm [scheduled task](https://laravel.com/docs/8.x/scheduling))

### The Events Directory (Thư mục sự kiện)

### The Exceptions Directory (Thư mục ngoại lệ)

Đặt và tuỳ chỉnh ngoại lệ được ghi lại, hiển thị do ứng dụng tạo ra -> Sửa trong **Handler** class

### The HTTP Directory (Thư mục HTTP)

Chứa controllers, middleware, form request -> Logic xử lý requests entering (yêu cầu nhập) 

### The Mail Directory (Thư mục thư)

Quản lý logic xây dựng email  -> phương thức **Mail::send** 

### The Providers Directory (Thư mục nhà cung cấp)

Chứa tất cả [service proviers](https://laravel.com/docs/8.x/providers). Có thể thêm nếu cần
