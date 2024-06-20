---
title: Giả lập live
order: 6
---

# Giả lập live

Pseudo-live streaming là một phương pháp giả lập luồng trực tiếp từ các video có sẵn trong hệ thống Video-On-Demand (VOD). Cho phép hiển thị các video đã được ghi trước phát trực tiếp theo thời điểm thực. Quá trình chuyển đổi video VOD thành video trực tiếp (live) có thể được thực hiện trước và sau khi video được tạo.

## Điều kiện

- Phải có ít nhất một công việc (job) đã được tạo trong danh sách, với trạng thái transcode đã hoàn thành `completed`
- Mỗi công việc này cho phép người dùng nhấp vào chi tiết để xem thông tin, trong đó có ít nhất một mục tiêu (target).
- Đối với mỗi công việc tạo ra, điểm đến (destination) để tạo công việc VOD là loại thư mục (folder).

## Tạo giả lập live

Quá trình tạo giả lập live được thực hiện theo các bước sau:

**Bước 1:** Người dùng nhấp vào công việc có trạng thái `completed` để mở trang chi tiết của công việc đó.

**Bước 2**: Tại trang chi tiết công việc, người dùng click vào biểu tượng tạo pseudo-live ở cột hành động (action) với mục tiêu tương ứng.

**Bước 3:** Một hộp thoại (pop-up) hiển thị để tạo pseudo-live, bao gồm:

![pop-up-pseudo-live](/images/media-vod/job-management/pop-up-pseudo-live.png)

- Hiển thị ô nhập link HLS, DASH: Không cho phép sửa, đã có dữ liệu link target mặc định tương ứng.

- Cho phép người dùng chọn thời gian bắt đầu (start-time).

  - Không cho phép chọn trùng thời gian start-time của các mục tiêu trong cùng một công việc.

  - Cho phép chọn start-time trong khoảng thời gian từ (current time - 1h) đến (start time + 7 ngày). Các khoảng thời gian không hợp lệ sẽ bị vô hiệu hóa từ phía giao diện người dùng vào thời điểm người dùng thực hiện hành động.

  - Giới hạn chọn start-time tối đa 7 ngày trong tương lai:

Ví dụ:

```
Tính từ thời điểm tạo 10:00:00 ngày 12/03/2024 đến 10:00:00 ngày 19/03/2024
```

- Lặp lại:
  - Chọn Vĩnh viễn: hệ thống tự tính toán số lần lặp lại tới giới hạn 7 ngày tự động dừng case.
  - Tổng thời lượng phát sóng (total duration) phải lớn hơn hoặc bằng 30 phút.

```
Tổng thời lượng = thời lượng video x số lần lặp lại (repeat).
```

**Bước 4**: Sau khi đã thiết lập các thông số cần thiết, người dùng nhấn vào nút `Tạo pseudo-live`.

Hiển thị pop-up view pseudo-live:

![view](/images/media-vod/job-management/view-pseudo-live.png)

- Xử lý video VOD theo định dạng HLS hoặc DASH đã cho và tạo thành dạng Pseudo-live streaming. Sau khi chuyển đổi thành công, hiển thị URL của video Pseudo-live streaming cho người dùng
  - URL được hiển thị để sao chép, trường hợp đường dẫn nhiều ký tự sẽ được hiển thị theo định dạng: [đầu link]....
  - Người dùng có thể phát lại video từ URL này.
- Thời gian bắt đầu của video Pseudo-live streaming được áp dụng chính xác như người dùng đã thiết lập.
- Thời lượng video.
- Lặp lại: hiển thị lựa chọn người dùng cấu hình.
- Cho phép xem trước video.

:::Lưu ý
Quá trình tạo pseudo-live cho phép tạo nhiều luồng pseudo-live trong cùng một công việc (job). Khi pop-up view pseudo-live được đóng, người dùng sẽ không thể xem lại luồng giả lập live và thực hiện tạo một luồng pseudo-live mới.
:::
