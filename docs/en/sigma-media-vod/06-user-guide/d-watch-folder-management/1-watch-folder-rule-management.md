---
title: Quản lý cơ chế thư mục cần theo dõi
order: 1
---

# Quản lý cơ chế thư mục cần theo dõi (watch folder rule)

Media VOD cho phép bạn quản lý và tổ chức nội dung những điều kiện của thư mục để có thể theo dõi theo một cơ chế nhất định. Nó hỗ trợ các chức năng như tạo danh mục nội dung, phân loại, gắn thẻ và tìm kiếm nhanh nội dung...

## Xem danh sách cơ chế thư mục cần theo dõi (watch folder rule)

Giao diện danh sách quy tắc thư mục (watch folder rule) là một phần quan trọng trong việc quản lý nội dung. Giao diện trong danh sách bao gồm các thông tin cơ bản về kênh như tên, trạng thái, thư mục,... và cho phép tìm kếm, giúp người quản trị viên có cái nhìn tổng quan.

**Bước 1:** Tại sidebar menu bên tay trái, người dùng di chuyển con trỏ chuột vào **Product** và chọn **Media VOD**

Màn hình chính hệ thống hiển thị giao diện Dashboard (theo dõi được tổng quan những thông tin chỉ số liên quan đến Media VOD) [Xem chi tiết tại đây](../b-dashboard.md)

**Bước 2:** Người dùng chọn tab `Watch folder`

Màn hình chính hệ thống hiển thị giao diện màn hình danh sách quy tắc thư mục (watch folder rule) với các thông tin chính bao gồm:

![Xem danh sách quy tắc thư mục](/images/media-vod/watch-folder-rule/view-watch-folder-rule-list.png)

| Tên cột                | Chức năng                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên**                | Tên của quy tắc theo dõi thư mục                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Máy**                | Máy được chỉ định để thực hiện chuyển mã khi có kích hoạt tự động                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Thư mục**            | Thư mục được theo dõi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Trạng thái**         | Trạng thái hoạt động của quy tắc thư mục, bao gồm: **Active** (đang hoạt động) và **Inactive** (không hoạt động)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Mô tả**              | Bao gồm các thông tin sau: <br/>- _**Điều kiện**_: hiển thị các đầu mục điều kiện được mô tả, (quy tắc không có điều kiện - hiển thị N/A) <br/>- _**Đầu ra**_: Mô tả nơi lưu trữ của đầu ra - số lượng profile - số lượng mục tiêu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Thời gian tạo**      | Thời gian tạo thành công quy tắc thư mục                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Thời gian cập nhật** | Thời gian cập nhật thành công quy tắc thư mục                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Hành động**          | _**Xem lịch sử công việc:**_ Cho phép người dùng theo dõi các job được tạo ra bởi quy tắc thư mục [Xem chi tiết tại đây](#xem-lịch-sử-công-việc-job-được-tạo-ra-từ-quy-tắc-thư-mục)<br/>_**Chỉnh sửa quy tắc thư mục:**_ Cho phép người dùng chỉnh sửa, cập nhật thông tin của quy tắc thư mục [Xem chi tiết tại đây](#chỉnh-sửa-cơ-chế-thư-mục-cần-theo-dõi-watch-folder-rule)<br/>_**Dừng theo dõi thư mục:**_ Cho phép người dùng dừng theo dõi thư mục (quy tắc thư mục hoạt động) [Xem chi tiết tại đây](#dừng-theo-dõi-thư-mục)<br/>_**Tiếp tục theo dõi thư mục:**_ Cho phép người dùng tiếp tục theo dõi thư mục (quy tắc thư mục không hoạt động) [Xem chi tiết tại đây](#tiếp-tục-theo-dõi-thư-mục)<br/>_**Xoá:**_ Cho phép người dùng CMS thực hiện xoá quy tắc thư mục [Xem chi tiết tại đây](#xóa-quy-tắc-thư-mục) |

- Các nút khác

| Tên nút          | Chức năng                                                                                                                                                                                                                                                                                                                                |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nút **"Thêm"**   | Thực hiện tạo watch folder rule [Xem chi tiết tại đây](2-create-watch-folder-rule.md)                                                                                                                                                                                                                                                    |
| Nút **Lọc**      | Thực hiện lọc các thông tin chi tiết hơn, bao gồm: _**Tên, Thư mục, Thời gian tạo, Thời gian cập nhật**_                                                                                                                                                                                                                 |
| **Quick filter** | Bộ lọc nhanh hỗ trợ tìm kiếm thông tin gồm: _**Tên, Máy, Trạng thái**_                                                                                                                                                                                                                                                   |
| **Phân trang**   | Góc trái bên dưới giao diện<br/>Bao gồm các thông tin: Tổng số trang, lựa chọn số items/1 trang (mặc định 10 items/1 trang), trang hiện tại, nhảy tới trang mong muốn tìm kiếm.                                                                                                       |
| **Icon đồng bộ** | Góc phải bên dưới giao diện, thực hiện thiết lập đồng bộ cho hệ thống:<br/>- Các thiết lập để hệ thống tự động đồng bộ (_**mặc định:**_ tắt tự động)<br/>- Chủ động đồng bộ cho hệ thống (bằng cách nhấn vào biểu tượng)<br/>- Thời gian hệ thống đồng bộ gần nhất |

## Các hành động

### Tạo cơ chế thư mục cần theo dõi (watch folder rule)

Chức năng tạo cơ chế theo dõi thư mục (watch folder rule) cho phép người dùng định nghĩa (mô tả) điều kiện một hoặc nhiều tệp tin hoặc thư mục cụ thể. Bất kì tập tin nào được tải lên đúng với những điều kiện được mô tả của thư mục này sẽ tự động kích hoạt quy trình chuyển mã.

[Xem chi tiết tại đây](2-create-watch-folder-rule.md)

### Chỉnh sửa cơ chế thư mục cần theo dõi (watch folder rule)

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một quy tắc thư mục đã được tạo ra trước đó và hiển thị tại danh sách quy tắc thư mục

**Bước 1**: Tại màn hình danh sách quy tắc thư mục, người dùng bấm biểu tượng _**Chỉnh sửa**_ ở cột Hành động đối với quy tắc thư mục cần chỉnh sửa

![Chỉnh sửa](/images/media-vod/watch-folder-rule/update-watch-folder-rule-1.png)

Hệ thống sẽ mở màn hình **Chỉnh sửa quy tắc thư mục** với các thông tin đã được nhập trước đó, **cho phép chỉnh sửa tất cả các trường**

![Chỉnh sửa quy tắc thư mục](/images/media-vod/watch-folder-rule/update-watch-folder.png)

**Bước 2**: Người dùng thực hiện chỉnh sửa thông tin và sau đó nhấn nút `Cập nhật quy tắc`

Hệ thống sẽ lưu lại thông tin mới và hiển thị thông báo **Đã cập nhật quy tắc thành công** ở giữa màn hình, sau đó tự động đóng trong vòng 5 giây.

### Xem lịch sử công việc (job) được tạo ra từ quy tắc thư mục

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một quy tắc thư mục đã được tạo ra trước đó và hiển thị tại danh sách quy tắc thư mục

Trên màn hình danh sách quy tắc thư mục, nhấn vào biểu tượng **Xem lịch sử công việc** ở cột Hành động với quy tắc thư mục mà bạn muốn theo dõi.

![Xem lịch sử công việc](/images/media-vod/watch-folder-rule/view-job-history.png)

Hệ thống sẽ chuyển sang màn hình [danh sách Job](../c-vod-job-management/1-vod-job-management.md#xem-danh-sách-công-việc) với bộ lọc theo quy tắc thư mục tương ứng

Tại đây người dùng có thể theo dõi danh sách job  được kích hoạt quá trình chuyển mã khi có tập tin phù hợp với điều kiện được mô tả của quy tắc thư mục

### Dừng theo dõi thư mục

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một quy tắc thư mục đã được tạo ra trước đó và hiển thị tại danh sách quy tắc thư mục
>
> Trạng thái của quy tắc thư mục **Active** (đang hoạt động)

**Bước 1** : Trên màn hình danh sách quy tắc thư mục, nhấn vào biểu tượng **Dừng theo dõi thư mục** ở cột Hành động với quy tắc thư mục mà bạn muốn dừng theo dõi.

![Dừng theo dõi thư mục](/images/media-vod/watch-folder-rule/pause-WF.png)

Hệ thống sẽ hiển thị một cửa sổ pop-up xác nhận ở trung tâm màn hình

**Bước 2** : Người dùng nhấn nút **Xác nhận** để dừng theo dõi thư mục

Hệ thống hiển thị một cửa sổ pop-up thông báo **Đã tạm dừng thành công!** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

Đồng thời, hệ thống thực hiện việc dừng theo dõi thư mục, **quy tắc thư mục không còn hoạt động** (chuyển về trạng thái Inactive - không hoạt động)

### Tiếp tục theo dõi thư mục

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một quy tắc thư mục đã được tạo ra trước đó và hiển thị tại danh sách quy tắc thư mục
>
> Trạng thái của quy tắc thư mục **Inactive** (không hoạt động)

**Bước 1** : Trên màn hình danh sách quy tắc thư mục, nhấn vào biểu tượng **Tiếp tục theo dõi thư mục** ở cột Hành động với quy tắc thư mục mà bạn muốn tiếp tục theo dõi.

![Tiếp tục theo dõi thư mục](/images/media-vod/watch-folder-rule/resume-WF.png)

Hệ thống sẽ hiển thị một cửa sổ pop-up xác nhận ở trung tâm màn hình

**Bước 2** : Người dùng nhấn nút **Xác nhận** để tiếp tục theo dõi thư mục

Hệ thống hiển thị một cửa sổ pop-up thông báo **Đã tiếp tục thành công!** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

Đồng thời, hệ thống thực hiện việc tiếp tục theo dõi thư mục, **quy tắc thư mục chuyển về trạng thái hoạt động**

### **Xóa quy tắc thư mục**

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một quy tắc thư mục đã được tạo ra trước đó và hiển thị tại danh sách quy tắc thư mục

**Bước 1** : Trên màn hình danh sách quy tắc thư mục, nhấn vào biểu tượng **Xoá** ở cột Hành động với quy tắc thư mục mà bạn muốn xoá.

![Xóa quy tắc thư mục](/images/media-vod/watch-folder-rule/delete-WF.png)

Hệ thống sẽ hiển thị một cửa sổ pop-up xác nhận ở trung tâm màn hình

**Bước 2** : Người dùng nhấn nút **Xác nhận** để xoá thông tin quy tắc thư mục

Hệ thống hiển thị một cửa sổ pop-up thông báo **Đã xoá thành công!** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

Đồng thời, hệ thống thực hiện **Xóa toàn bộ thông tin của quy tắc thư mục**, không còn hiển thị thông tin tại danh sách quy tắc thư mục.
