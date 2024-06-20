---
title: Get started with Media Video On Demand (Media VOD)
order: 2
---

# Get started with Media Video On Demand (Media VOD)

## Luồng thực hiện

Để bắt đầu nhanh chóng làm quen với Media Video On Demand (Media VOD), người dùng cần thực hiện các bước sau:

![Luồng thực hiện làm quen với Media VOD](/images/media-vod/introduce/get-started-flow.png)

## Truy cập vào hệ thống Sigma Streaming

1. Thực hiện [Đăng kí tài khoản](../../sigma-streaming-platform/02-user-management/a-sign-up.md) hoặc [đăng nhập](../../sigma-streaming-platform/02-user-management/c-sign-in.md) để truy cập hệ thống quản lý của **Sigma Streaming Platform** `https://portal.sigma.video`
2. Hiển thị Danh sách ứng dụng, **chọn ứng dụng** cần truy cập.
3. Hiển thị mặc định vào trang **tổng quan ứng dụng**.

## Set up server operation

Đảm bảo rằng trong quá trình sử dụng sản phẩm VOD, máy chủ phải đang trong **trạng thái hoạt động**

Nếu bạn chưa kích hoạt cho hoạt động của máy chủ, bạn nên thực hiện cài đặt máy trên máy của người dùng (local)

![Cài đặt máy chủ](/images/media-vod/introduce/add-server.png)

1. Tại sidebar, chọn mục **Server**
2. Hiển thị danh sách máy chủ, **chọn thêm máy chủ**
3. Hiển thị thông tin cài đặt máy, trong đó bao gồm _**Registation Token**_
4. Sao chép `Registation Token` và thực hiện cài máy trên máy của người dùng (local) [Xem chi tiết tại đây](../../sigma-media-server/04-getting-started/04-install-new-machine.md)
5. Successfully installed machines display at the top of the list of machines
6. Thêm giấy phép (license) để kích hoạt hoạt động của máy chủ [Xem chi tiết tại đây](../../sigma-media-server/04-getting-started/05-add-license.md)

## Tạo mới VOD job

Để tạo mới một video VOD, người dùng cần khởi tạo một công việc mới (job) theo các bước sau:

1. Truy cập vào trang quản lý sigma VOD (Video on Demand).
2. Hiển thị trang danh sách các job (công việc).
3. Nhấp vào nút `Thêm mới` để bắt đầu tạo job.
4. Chuyển đến trang Tạo mới Job.
5. Thực hiện điền đầy đủ thông tin

- [Chọn máy chủ](../06-user-guide/c-vod-job-management/2-create-job.md#bước-1-chọn-máy-chủ)
- [Chọn đầu vào](../06-user-guide/c-vod-job-management/2-create-job.md#bước-2-chọn-đầu-vào)
- [Chọn đầu ra](../06-user-guide/c-vod-job-management/2-create-job.md#bước-3-chọn-đầu-ra-destination)
- [Thiết lập cấu hình job](../06-user-guide/c-vod-job-management/2-create-job.md#bước-4-cấu-hình-job)

6. Nhấp vào nút `Tạo job`
7. Hệ thống sẽ tiến hành tạo job để chuyển mã video và sau đó hiển thị người dùng trở lại danh sách các job.

## Quản lý VOD job

Tại danh sách job, người dùng có thể xem được thông tin về tiến độ mã hóa, trạng thái, thời gian chuyển mã, thời gian chuyển mã còn lại, kích cỡ của file và máy chủ được chỉ định để tiến hành chuyển mã.

[Xem chi tiết tại đây](../06-user-guide/c-vod-job-management/1-vod-job-management.md#xem-danh-sách-công-việc)

![Xem danh sách VOD job](/images/media-vod/job-management/view-job-list.png)

Nhấp vào **"Tên job"** để xem thông tin chi tiết bao gồm:

- **Máy**: máy được chỉ định thực hiện job
- **Thời gian chuyển mã còn lại**: hiển thị thời gian chuyển mã còn lại của tệp đầu vào
- **Thanh trạng thái của job**: thể hiện trạng thái hiện tại của job
- **Thông tin của tập tin đầu vào**, bao gồm: Liên kết, định dạng, bộ giải mã video, bộ giải mã audio, độ phân giải, kích cỡ và thời lượng
- **Thông tin của tập tin đầu ra**, bao gồm: Tên, liên kết, xem trước (preview), định dạng, bộ giải mã video, bộ giải mã audio, độ phân giải, kích cỡ, thời lượng và các hành động được phép.

[Xem chi tiết tại đây](../06-user-guide/c-vod-job-management/1-vod-job-management.md#xem-chi-tiết-công-việc)

![Xem thông tin chi tiết job](/images/media-vod/job-management/view-detail-job.png)

## Xóa VOD job

Once you have created and launched the job. Sau đó, job hoàn thành (trạng thái Complete) hoặc quá trình xảy ra lỗi (trạng thái Error) để đóng các job không cần thiết, bạn cần thực hiện thao tác xoá job

[Xem chi tiết tại đây](../06-user-guide/c-vod-job-management/1-vod-job-management.md#xóa-job)
