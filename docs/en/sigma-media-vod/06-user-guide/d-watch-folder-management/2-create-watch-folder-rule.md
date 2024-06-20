---
title: Tạo cơ chế theo dõi thư mục
order: 1
---

# Tạo cơ chế theo dõi thư mục (watch folder rule)

Chức năng này cho phép người dùng tạo những điều kiện để theo dõi thư mục. Bất kì tập tin nào được tải lên đúng với những điều kiện được mô tả của thư mục này sẽ tự động kích hoạt quy trình chuyển mã.

## Tổng quan về chức năng

Chức năng tạo cơ chế theo dõi thư mục (watch folder rule) cho phép người dùng:

- Bất kì tập tin nào được tải lên đúng với những điều kiện được mô tả của thư mục này sẽ tự động kích hoạt quy trình chuyển mã.
- Người dùng có khả năng định nghĩa (mô tả) điều kiện một hoặc nhiều tệp tin hoặc thư mục cụ thể.
- Cho phép người dùng chọn đầu ra cho các tệp tin đầu ra được tạo từ cơ chế theo dõi thư mục.
- Cấu hình chung cho tất cả profile trong video on demand giúp bảo vệ bản quyền, tăng tính chuyên nghiệp và giá trị thương hiệu của video, cũng như ngăn chặn việc sửa đổi hoặc sao chép không được phép.
- Chuyển mã âm thanh và video nguồn thành định dạng **DASH, HLS, Multiple-mp4, Mp4, Mp3** để phát lại trên nhiều loại thiết bị.
- Điều chỉnh tốc độ bit đầu ra cho phù hợp với các băng thông mạng khác nhau.
- Tùy chỉnh các mẫu chuyển mã, chẳng hạn như loại chuyển mã, tốc độ bit video, độ phân giải, tốc độ khung hình.

## Lưu ý

- Sử dụng máy chủ và không sử dụng dịch vụ đám mây (cloud).
- Mỗi máy chủ chỉ được tạo tối đa 10 cơ chế theo dõi thư mục.

## Luồng

Quá trình tạo cơ chế theo dõi thư mục (watch folder rule) người dùng cần thực hiện:

![Quá trình tạo cơ chế theo dõi thư mục](/images/media-vod/watch-folder-rule/create-watch-folder-flow.png)

## Tạo cơ chế theo dõi thư mục (watch folder rule)

Để tạo mới một video VOD, người dùng cần khởi tạo một công việc mới (job) theo các bước sau:

1. Truy cập vào trang quản lý sigma VOD (Video on Demand).
2. Hiển thị trang Dashboard (theo dõi được tổng quan những thông tin chỉ số liên quan đến Media VOD) [Xem chi tiết tại đây](../b-dashboard.md)
3. Người dùng chọn tab **Watch folder**. Màn hình hiển thị danh sách cơ chế theo dõi thư mục (watch folder rule)
4. Nhấp vào nút `Thêm mới` để bắt đầu tạo watch folder rule
5. Chuyển đến trang Tạo mới watch folder rule

### **Bước 1:** Điền thông tin tên của watch folder rule

1. Hệ thống hiển thị cửa sổ pop-up Tạo mới watch folder rule, với thông tin bắt buộc điền: **Tên của quy tắc thư mục**

![Tên của quy tắc thư mục](/images/media-vod/watch-folder-rule/name-wfr.png)

1. Người dùng thực hiện điền thông tin bắt buộc tại pop-up, sau đó nhấn vào nút **"Xác nhận"** tại cuối cửa sổ pop-up
2. Hệ thống hiển thị màn hình Tạo mới watch folder rule với bước tiếp theo

### **Bước 2:** Lựa chọn máy và thư mục

Người dùng nhấn vào lựa chọn đầu vào, hệ thống hiển thị cửa sổ pop-up, với thông tin sau:

- **Máy:** lựa chọn máy để thực hiện chọn tập tin

![Lựa chọn máy](/images/media-vod/watch-folder-rule/select-server.png)

- **Thư mục:** Sau khi lựa chọn máy, hệ thống hiển thị các thư mục tương ứng với máy (chỉ cho phép lựa chọn thư mục)

![Lựa chọn thư mục](/images/media-vod/watch-folder-rule/select-folder.png)

### **Bước 3 (không bắt buộc):** Mô tả điều kiện theo dõi thư mục

Tiếp theo, người dùng sẽ được dẫn sang bước tiếp theo trong quá trình

1. Nhấp vào mô tả điều kiện để theo dõi thư mục
2. Hệ thống hiển thị cửa sổ pop-up với các thông tin sau:

- **Biểu thức chính quy (regex pattern)**: Không bắt buộc điền, nhập các kí tự được cho phép của regrex

![Regex pattern](/images/media-vod/watch-folder-rule/CWF-condition-regex.png)

1. Người dùng điền thông tin (không bắt buộc) và nhấn nút **"Tiếp theo"**
2. Hệ thống chuyển sang màn hình lựa chọn điều kiện tiếp theo
3. Nhấn vào nút **"Thêm rule"** để chọn các trường điều kiện theo mong muốn của người dùng, bao gồm

![Mô tả điều kiện](/images/media-vod/watch-folder-rule/WF-condition.png)

| **Tên cột**                       | **Mô tả**                                                                      | **Yêu cầu**                                                                              |
| --------------------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Bitrate (mpbs) | Dùng để đo lường tốc độ truyền dữ liệu hoặc tốc độ bit trong một luồng dữ liệu | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |
| Width (px)     | Chiều rộng của khung hình video                                                | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |
| Height (px)    | Chiều cao của khung hình video                                                 | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |
| FPS (fps)      | Tốc độ khung hình mỗi giây                                                     | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |
| Size (byte)    | Kích thước của video                                                           | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |
| Codec                             | Bộ chuyển mã                                                                   | Không bắt buộc, cho phép các lựa chọn sau: **H264, H265, AV1, VP9, VP8** |
| Duration (s)   | Thời lượng mã hóa video                                                        | Không bắt buộc, chỉ cho phép nhập  kí tự số                                              |

1. Người dùng điền thông tin ứng với các điều kiện và nhấn nút **"Áp dụng"**
2. Hệ thống lưu thông tin mô tả điều kiện theo dõi của thư mục và hiển thị bước tiếp theo

### Bước 4: Chọn đầu ra (destination)

Tiếp theo, người dùng sẽ được dẫn sang bước tiếp theo trong quá trình, cấu hình nơi lưu trữ VOD job (Job được tạo ra khi thỏa mãn điều kiện theo dõi của thư mục).

1. Chọn điểm đích (destination) để lưu trữ VOD job.

![Nơi lưu trữ VOD job](/images/media-vod/watch-folder-rule/destination.png)

Hỗ trợ các loại đầu ra:

\- Lưu vào folder ở máy chủ: [Xem chi tiết tại đây](../c-vod-job-management/4-destination/4.1-folder-storage.md)

\- Lưu vào bên thứ 3: hỗ trợ FTP, Generic S3. [Xem chi tiết tại đây](../c-vod-job-management/4-destination/4.2-third-party-storage.md)

2. Hệ thống quay trở lại màn hình tạo mới để thực hiện các bước tiếp theo.

Hệ thống đánh dấu loại đầu ra.

Cho phép chỉnh sửa hoặc xoá lựa chọn.

### Bước 5: Cấu hình job

Tiếp theo, người dùng sẽ được dẫn sang bước cuối cùng trong quá trình, cấu hình thông tin job (Job được tạo ra khi thỏa mãn điều kiện theo dõi của thư mục)

1. Hiển thị mặc định là danh sách các profile với trạng thái chưa áp dụng bất kỳ mẫu (template) nào. Nút **Tạo quy tắc** không thể sử dụng.

![Cấu hình job](/images/media-vod/watch-folder-rule/config-job.png)

- Cấu hình profile chung: Chưa có dữ liệu.
- Nút `cấu hình mặc định`: xoá dữ liệu do người dùng cấu hình profile, hiển thị prodile mặc định
- Danh sách profile mặc định gồm: 1080, 720, 480, 360, 240, 144
  ( cho phép sửa, xoá)
- Cấu hình mục tiêu

1. Lựa chọn thao tác:

- Chọn cấu hình mẫu
- Tuỳ chỉnh cấu hình:
  - Cấu hình profile: [Xem chi tiết tại đây](../c-vod-job-management/5-config-job/5.1-profile.md)
  - Cấu hình target: [Xem chi tiết tại đây](../c-vod-job-management/5-config-job/5.2-target-job.md)

### Bước 6: Hoàn thành tạo quy tắc thư mục

1. Hoàn tất cấu hình các bước trước đó (người dùng có thể chỉnh sửa tên của quy tắc)
2. Nhấn vào nút `Tạo quy tắc`
3. Hệ thống thực hiện tạo mới quy tắc, hiển thị thông báo **Đã tạo quy tắc thành công!** ở giữa màn hình để thông báo quá trình tạo đã được thực hiện thành công.
