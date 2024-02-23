---
title: Tạo mới đầu vào
order: 1
---

# Tạo mới đầu vào

Tính năng **Quản lý đầu vào** giúp người dùng quản lý dữ liệu đầu vào một cách hiệu quả và dễ dàng hơn. Người dùng có thể thêm, chỉnh sửa và xóa các đầu vào, tạo ra các bản ghi dữ liệu đầu vào. Mỗi đầu vào được tạo có thể thêm 1 máy hoặc 1 cluster cụ thể thuận tiện cho việc điều phối và xử lý Job khi kênh được tạo.

Có 2 loại đầu vào: Đầu vào kênh Transcode và đầu vào kênh Package

## Tạo mới đầu vào kênh Transcode

Chức năng này cho phép người dùng CMS tạo mới Đầu vào loại Transcode

**Bước 1**: Truy cập sản phẩm Media Live, người dùng chọn tab Inputs.

Hệ thống hiển thị mặc định với tab Transcode, giao diện màn hình danh sách đầu vào loại Transcode.

![Tạo mới đầu vào kênh Transcode](/images/media-live/input/create-transcode-input.png)

**Bước 2**: Tại giao diện màn hình danh sách Đầu vào Transcode (Tab Transcode), người dùng bấm nút **Thêm**

Hệ thống hiển thị pop-up thêm mới đầu vào Transcode ở bên phải màn hình.

Với các thông tin chung:

| Tên                  | Chức năng                                                                                                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên**              | Tên của đầu vào Transcode                                                                                                                                                  |
| **Mô tả**            | Mô tả của đầu vào Transcode                                                                                                                                                |
| **Based on Machine** | Cho phép kích hoạt Based on machine                                                                                                                                        |
| **Loại**             | Loại của nguồn đầu vào bao gồm UDP, RTMP_PUSH, RTMP_PULL, SRT_PUSH, SRT_PULL, HLS, SDI |
| **Loại máy**         | Loại máy để sử dụng bao gồm: Sigma Machine, Sigma Machine cluster, Sigma Component Cluster                                                                                 |
| **Máy**              | Máy cụ thể phù hợp để thực hiện nhiệm vụ                                                                                                                                   |
| **Redundancy**       | Input Class: _**Single**_ (1 nguồn đầu vào chính), _**Redundancy**_ (Nguồn đầu vào chính + nguồn đầu vào phụ)                        |
| **Nguồn chính**      | Thông tin nguồn đầu vào chính                                                                                                                                              |
| **Nguồn phụ**        | Thông tin nguồn đầu vào thứ 2 (Chọn **Nguồn phụ** nếu **Loại** là UDP, RTMP Pull, SRT Pull)                                                             |

- Các thông tin đối với loại của nguồn đầu vào là UDP (Trường loại = "UDP"):

| Tên                             | Chức năng                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Primary Network Interface**   | Network Interface chính đối với nguồn đầu vào loại UDP                                            |
| **Secondary Network Interface** | Network Interface phụ đối với nguồn đầu vào loại UDP, cho phép nhập khi Input Class là Redundancy |

- Nút **Hủy**: Hủy bỏ thao tác thêm mới Đầu vào Transcode
- Nút **Cài lại**: Cài lại toàn bộ dữ liệu đã nhập, form trở về mặc định
- Nút **Xác nhận**: Xác nhận lưu cấu hình của Đầu vào Transcode

**Bước 3**: Người dùng nhập các thông tin cần thiết

**Bước 4**: Sau khi hoàn tất, nhấn vào nút **Xác nhận** tại cuối cửa sổ pop-up.

Hệ thống thực hiện tạo mới đầu vào Transcode với các thông tin vừa được nhập, hiển thị Pop-up thông báo **Tạo đầu vào Transcode thành công** ở giữa màn hình để thông báo quá trình tạo đã được thực hiện thành công.

## Tạo mới đầu vào Package

Chức năng này cho phép người dùng CMS tạo mới Đầu vào loại Transcode

**Bước 1**: Truy cập sản phẩm Media Live, người dùng chọn tab Inputs.

Tại đây hệ thống hiển thị mặc định với tab Transcode, người dùng lựa chọn tab Package để chuyển sang giao diện màn hình danh sách đầu vào loại Package.

**Bước 2**: Tại giao diện màn hình danh sách Đầu vào Package (Tab Package), người dùng bấm nút **Thêm**

Hệ thống hiển thị pop-up thêm mới đầu vào Package ở bên phải màn hình

![Tạo mới đầu vào kênh Package](/images/media-live/input/create-package-input.png)

Với các thông tin chung:

| Tên                  | Chức năng                                                                                                                                                        |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên**              | Tên của đầu vào Package                                                                                                                                          |
| **Mô tả**            | Mô tả của đầu vào Package                                                                                                                                        |
| **Based on Machine** | Cho phép kích hoạt Based on machine                                                                                                                              |
| **Loại**             | Loại của nguồn đầu vào bao gồm UDP, RTMP_PUSH, RTMP_PULL, SRT_PUSH, SRT_PULL |
| **Loại máy**         | Loại máy để sử dụng bao gồm: Sigma Machine, Sigma Machine cluster, Sigma Component Cluster                                                                       |
| **Máy**              | Máy cụ thể phù hợp để thực hiện nhiệm vụ                                                                                                                         |
| **Redundancy**       | Input Class: _**Single**_ (1 nguồn đầu vào chính), _**Redundancy**_ (Nguồn đầu vào chính + nguồn đầu vào phụ)              |
| **Nguồn chính**      | Thông tin nguồn đầu vào chính                                                                                                                                    |
| **Nguồn phụ**        | Thông tin nguồn đầu vào thứ 2 (Chọn **Nguồn phụ** nếu **Loại** là UDP, RTMP Pull, SRT Pull)                                                   |

- Các thông tin đối với loại của nguồn đầu vào là UDP (Trường loại = "UDP"):

| Tên                             | Chức năng                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Primary Network Interface**   | Network Interface chính đối với nguồn đầu vào loại UDP                                            |
| **Secondary Network Interface** | Network Interface phụ đối với nguồn đầu vào loại UDP, cho phép nhập khi Input Class là Redundancy |

- Nút **Xóa** tại các nguồn: Cho phép xóa nguồn đã thêm
- Nút **Hủy**: Hủy bỏ thao tác thêm mới Đầu vào Transcode
- Nút **Cài lại**: Cài lại toàn bộ dữ liệu đã nhập, form trở về mặc định
- Nút **Xác nhận**: Xác nhận lưu cấu hình của Đầu vào Transcode

**Bước 3**: Người dùng nhập các thông tin cần thiết

**Bước 4**: Sau khi hoàn tất, nhấn vào nút **Xác nhận** tại cuối cửa sổ pop-up.

Hệ thống thực hiện tạo mới đầu vào Package với các thông tin vừa được nhập, hiển thị Pop-up thông báo **Tạo đầu vào Package thành công** ở giữa màn hình để thông báo quá trình tạo đã được thực hiện thành công.
