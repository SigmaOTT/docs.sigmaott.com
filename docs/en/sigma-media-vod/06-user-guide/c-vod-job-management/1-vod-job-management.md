---
title: Quản lí công việc (job)
order: 1
---

# Quản lí công việc (job)

Media VOD cho phép bạn quản lý và tổ chức nội dung video từ nhiều nguồn khác nhau. Nó hỗ trợ các chức năng như tạo danh mục nội dung, phân loại, gắn thẻ và tìm kiếm nhanh nội dung... Bạn có thể tải lên một hoặc nhiều nội dung đa phương tiện cùng một lúc.

## Xem danh sách công việc

Giao diện danh sách công việc (job) là một phần quan trọng trong việc quản lý nội dung. Giao diện trong danh sách bao gồm các thông tin cơ bản về kênh như ID, tên, trạng thái, tình trạng,... và cho phép tìm kếm, giúp người quản trị viên có cái nhìn tổng quan.

**Bước 1:** Tại sidebar menu bên tay trái, người dùng di chuyển con trỏ chuột vào **Product** và chọn **Media VOD**

Màn hình chính hệ thống hiển thị giao diện Dashboard (theo dõi được tổng quan những thông tin chỉ số liên quan đến Media VOD) [Xem chi tiết tại đây](../b-dashboard.md)

**Bước 2:** Người dùng chọn tab `VOD`

Màn hình hiển thị danh sách công việc (job), với các thông tin chính bao gồm:

![Danh sách job](/images/media-vod/job-management/view-job-list.png)

| Tên cột                         | Chức năng                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ID**                          | Sau khi người dùng tạo mới job, hệ thống sinh ra ID riêng cho mỗi job với mục đích nhận diện. <br/>Hiển thị dưới dạng nút, cho phép hover để xem ID và bấm vào để sao chép                                                                                                                                                                                                                                                                                                                                           |
| **Tên**                         | Tên của tệp đầu vào                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Tiến độ mã hóa**              | Tiến độ thực hiện của quá trình chuyển mã                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Trạng thái**                  | Trạng thái của job, bao gồm: _**Created, Queued, Encoding, Completed, Error**_<br/>- **Created**: Job sẽ ở trạng thái này ngay sau khi bấm nút "Tạo job"<br/>- **Queued**: sau đó job sẽ chuyển sang trạng thái chờ quá trình chuyển mã<br/>- **Encoding**: job đang ở trạng thái chuyển mã<br/>- **Completed**: kết thúc quá trình chuyển mã, hoàn thành quá trình tạo job<br/>- **Error**: Phát sinh lỗi trong quá trình chuyển mã |
| **Thời gian chuyển mã**         | Tổng thời gian chuyển mã của tệp đầu vào                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Thời gian chuyển mã còn lại** | Thời gian chuyển mã còn lại của tệp đầu vào                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Kích cỡ**                     | Kích cỡ của tệp đầu vào                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Máy**                         | Máy đang được chỉ định thực hiện job                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Thời gian tạo**               | Thời gian khởi tạo job                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Hành động**                   | _**Thử lại job:**_ Cho phép người dùng khởi động lại quá trình chuyển mã khi job có lỗi. [Xem chi tiết tại đây](#thử-lại-job)<br/>_**Nhân bản job:**_ Cho phép người dùng tạo ra một bản sao job mới [Xem chi tiết tại đây](#nhân-bản-job)<br/>_**Xoá job:**_ Cho phép người dùng CMS thực hiện xoá job [Xem chi tiết tại đây](#xóa-job)                                                                                                                             |

- Các nút khác

| Tên nút          | Chức năng                                                                                                                                                                                                                                                                                                                                |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nút **"Thêm"**   | Thực hiện tạo job để chuyển mã cho video [Xem chi tiết tại đây](2-create-job.md)                                                                                                                                                                                                                                                         |
| Nút **Lọc**      | Thực hiện lọc các thông tin chi tiết hơn, bao gồm: _**Tên, Thời gian tạo, Trạng thái, Thời gian chuyển mã (s)**_                                                                                                                                                                                      |
| **Quick filter** | Bộ lọc nhanh hỗ trợ tìm kiếm thông tin gồm: _**Tên, Job ID, Máy, Trạng thái**_                                                                                                                                                                                                                                           |
| **Phân trang**   | Góc trái bên dưới giao diện<br/>Bao gồm các thông tin: Tổng số trang, lựa chọn số items/1 trang (mặc định 10 items/1 trang), trang hiện tại, nhảy tới trang mong muốn tìm kiếm.                                                                                                       |
| **Icon đồng bộ** | Góc phải bên dưới giao diện, thực hiện thiết lập đồng bộ cho hệ thống:<br/>- Các thiết lập để hệ thống tự động đồng bộ (_**mặc định:**_ tắt tự động)<br/>- Chủ động đồng bộ cho hệ thống (bằng cách nhấn vào biểu tượng)<br/>- Thời gian hệ thống đồng bộ gần nhất |

## Các hành động

### Tạo công việc (job)

Tạo một công việc (job) từ video thành Video on Demand (VOD) là quá trình transcode video để tối ưu hóa cho streaming trực tuyến, thiết bị di động, bảo mật, quản lý nội dung, đa nền tảng, hoặc quảng cáo.

[Xem chi tiết tại đây](2-create-job.md)

### Xem chi tiết công việc (job)

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một job đã được tạo trước đó và hiển thị trong danh sách.

1. Tại giao diện Danh sách job, nhấn vào `[Tên job]` mong muốn xem thông tin chi tiết job

2. Hiển thị giao diện chi tiết job với các thông tin sau:

![Chi tiết công việc](/images/media-vod/job-management/view-detail-job.png)

- **Mã công việc**: hệ thống sinh ra ID riêng cho mỗi job với mục đích nhận diện. Cho phép thực hiện hành động sao chép
- **Máy**: máy được chỉ định thực hiện job
- **Thời gian chuyển mã còn lại**: hiển thị thời gian chuyển mã còn lại của tệp đầu vào
- **Thanh trạng thái của job**: thể hiện trạng thái hiện tại của job
- Thông tin của tập tin đầu vào, bao gồm:
  - **Liên kết**: là đường dẫn để tải về tệp video
  - **Định dạng**: hệ thống nhận diện định dạng tập tin đầu vào
  - **Bộ giải mã video**: loại video codec của tập tin
  - **Bộ giải mã audio**: loại audio codec của tập tin
  - **Độ phân giải**: độ phân giải của tập tin đầu vào
  - **Kích cỡ**: kích cỡ của tập tin đầu ra
  - **Thời lượng**: thời lượng của tập tin đầu vào
- Thông tin của tập tin đầu vào, bao gồm:
  - **Tên**: Tên của cấu hình mục tiêu
  - **Liên kết**: là đường dẫn để tải về tệp video
  - **Xem trước (preview)**: Xem video ngay trên giao diện [Xem chi tiết tại đây](#preview)
  - **Định dạng**: hệ thống nhận diện định dạng tập tin đầu vào
  - **Bộ giải mã video**: loại video codec của tập tin đầu ra
  - **Bộ giải mã audio**: loại audio codec của tập tin đầu ra
  - **Độ phân giải**: độ phân giải của tập tin đầu ra
  - **Kích cỡ**: kích cỡ của tập tin đầu ra
  - **Thời lượng**: thời lượng của tập tin đầu ra
  - **Hành động**: Tạo giả lập live [Xem chi tiết tại đây](5-pseudo-live.md)

### Thử lại job

Người dùng muốn tạo khởi động lại quá trình tạo job bắt đầu từ trạng thái Queued

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một job đã được tạo trước đó và hiển thị trong danh sách.
>
> **Chỉ thực hiện được khi job đang ở trạng thái Error**

**Bước 1:** Trong danh sách, di chuột vào biểu tượng **Thử lại** ở cột Hành động tại trường bạn muốn khởi động lại quá trình tạo job, hiển thị tooltip text **Thử lại job**, nhấp vào biểu tượng.

![Thử lại job](/images/media-vod/job-management/retry-job.png)

Hệ thống sẽ hiển thị một cửa sổ pop-up xác nhận ở trung tâm màn hình

**Bước 2** : Người dùng nhấn nút **Xác nhận** để khởi động lại quá trình tạo job

Hệ thống hiển thị một thông báo **Đã thử lại thành công!** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

### Nhân bản job

Người dùng muốn tạo một bản sao job với thông tin đã có trước đó, giữ các cài đặt bắt buộc và thông tin của kênh sự kiện.

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một job đã được tạo trước đó và hiển thị trong danh sách.

**Bước 1:** Trong danh sách, di chuột vào biểu tượng **nhân bản** ở cột Hành động tại trường bạn muốn tạo bản sao, hiển thị tooltip text **nhân bản**, nhấp vào biểu tượng.

![Nhân bản job](/images/media-vod/job-management/duplicate-job.png)

Sau đó hiển thị màn hình thông tin cấu hình job với thông tin đã được thiết lập trước đó. **Cho phép** chỉnh sửa tất cả các trường.

**Bước 2:** Người dùng nhập thông tin cần thiết và người dùng nhấn nút **Tạo công việc (sao chép)**

Hệ thống hiển thị thông báo thực hiện **Sao chép công việc thành công** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

### Xóa job

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một job đã được tạo trước đó và hiển thị trong danh sách.
>
> Chỉ thực hiện được khi job đang ở trạng thái **Completed hoặc Error**

**Bước 1** : Trên màn hình danh sách kênh sự kiện, tại job mà bạn muốn xoá, di chuột vào biểu tượng **Xoá** ở cột Hành động, và sau đó nhấn vào biểu tượng **Xoá**.

![Xóa job](/images/media-vod/job-management/delete-job.png)

Hệ thống sẽ hiển thị một cửa sổ pop-up xác nhận ở trung tâm màn hình

**Bước 2** : Người dùng nhấn nút **Xác nhận** để xoá thông tin kênh sự kiện.

Hệ thống hiển thị một thông báo **Đã xoá thành công!** ở góc phải màn hình và tự động đóng thông báo sau 5 giây.

Đồng thời, hệ thống thực hiện **xoá toàn bộ thông tin job**

## Các hành động khác

### Giả lập live

Pseudo-live streaming là một phương pháp giả lập luồng trực tiếp từ các video có sẵn trong hệ thống Video-On-Demand (VOD). Cho phép hiển thị các video đã được ghi trước phát trực tiếp theo thời điểm thực. Quá trình chuyển đổi video VOD thành video trực tiếp (live) có thể được thực hiện trước và sau khi video được tạo.

[Xem chi tiết tại đây](5-pseudo-live.md)

### Preview

> [!NOTE]
> Để thực hiện quá trình này, cần phải có ít nhất một job đã được tạo trước đó và hiển thị trong danh sách.
>
> Job được chuyển mã thành công với trạng thái **completed.**

**Bước 1** : Trên màn hình danh sách job, nhấn vào **[Tên kênh job]** mong muốn xem thông tin chi tiết job dõi.

Hiển thị giao diện chi tiết job

**Bước 2:** Tại mục thông tin của tập tin đầu ra, nhấn nút ở cột Preview (xem trước) để thực hiện xem video

![Preview ](/images/media-vod/job-management/icon-preview.png)

Hệ thống hiển thị cửa sổ pop-up, trong đó chứa video tương ứng

![Xem video](/images/media-vod/job-management/playvideo1.png)

Đối với tập tin đầu ra có định dạng là Multi-MP4, người dùng có thể xem video từ tập tin _**smil**_ dưới hai dạng là _**HLS và DASH**_.

**Bước 3:** Người dùng nhấn vào nút `Play`, hệ thống phát video tương ứng, đúng với nội dung và cấu hình
