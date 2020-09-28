# Cấu trúc source

## The App Directory (Thư mục ứng dụng)

Chứa mã core 

## The Bootstrap Directory (Thư mục khởi động)

Chứa file khởi động ứng dụng -> **app.php**
Chứa thư mục **cache** -> tối ưu hoá hiệu xuất

## The Config Directory (Thư mục cấu hình)

Chứa tất cả các file cấu hình ứng dụng

## he Database Directory (Thư mục cơ sở dữ liệu)

* database migrations -> version control của database -> quản lý tất cả phiên bản -> cho phép thay đổi db, trạng thái db.(Đọc thêm [migrations](https://viblo.asia/p/migration-trong-laravel-va-nhung-dieu-can-biet-ByEZkyEy5Q0))
* model factories -> Tạo dữ liệu với số lượng bản ghi lớn, tối ưu code. Dễ thay đổi số lượng bản ghi  (Đọc thêm [factory](https://viblo.asia/p/seeder-va-model-factory-trong-laravel-ban-da-thu-chua-ByEZkvoAKQ0))
* seeds -> Tạo dữ liệu mẫu (Đọc thêm [seeds](https://viblo.asia/p/seeder-va-model-factory-trong-laravel-ban-da-thu-chua-ByEZkvoAKQ0))
