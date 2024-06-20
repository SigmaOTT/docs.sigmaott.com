---
title: Quick Start
order: 1
---

# {{ $frontmatter.title }}

<!-- ## Connect to the Controller

1. Mở trình duyệt web.

2. Nhập đường dẫn truy cập, và nhấn **Enter**.

    

    Ví dụ: Http: **http://[IP-Address]:80/portal**

    **Kết quả**: Trang **đăng nhập** hiện ra, người dùng nhập thông tin đăng nhập vào hệ thống

![login](/images/media-live/um-login/main.png){ width=400px }


Sau đó, hệ thống sẽ xử lý thao tác đăng nhập.

- Nếu thành công, điều hướng người dùng về trang **Quản trị** hoặc trang người dùng đã truy cập trước khi bị điều hướng sang trang Đăng nhập.

- Nếu thất bại, hệ thống sẽ hiển thị thông báo lỗi và giữ nguyên giao diện hiện tại của người dùng.


## Thay đổi mật khẩu

Cho phép thực hiện thao tác đổi mật khẩu tài khoản người dùng.

Giao diện form thay đổi mật khẩu

![Change Password](/images/media-live/um-change-pwd/main.png)

Thực hiện đổi mật khẩu theo các bước:

1. Nhập giá trị mật khẩu mới vào ô `Password`.
2. Nhập lại giá trị mật khẩu mới một lần nữa vào ô `Re-password` để đảm bảo người dùng không nhập sai mật khẩu mới.

---

::: tip NOTE

Giá trị mật khẩu mới chỉ **hợp lệ** khi thỏa mãn **toàn bộ** những tiêu chí sau:

- Mật khẩu mới phải có độ dài tối thiểu 8 ký tự, chứa các chữ cái a-z, A-Z, chữ số 0-9 và ký tự đặc biệt.
- Giá trị mật khẩu trong hai trường `Password` và `Repassword` phải trùng khớp nhau.

Nếu chỉ một trong các tiêu chí trên không hợp lệ thì sẽ hiển thị thông báo lỗi.

![Message Change Password](/images/media-live/um-change-pwd/validation-msg.jpg){ width=400px }

:::

---

Người dùng xác nhận việc thay đổi mật khẩu mới bằng cách nhấn nút `Submit`.

![Submit Button](/images/media-live/um-change-pwd/submit-btn.png){ width=300px }

Sau đó, hệ thống sẽ hiện thị thông báo đổi mật khẩu thành công hay thất bại.

- Nếu thành công, hệ thống hiển thị thông báo thành công và điều hướng người dùng về trang **Đăng nhập**.

  ![Success Message](/images/media-live/um-change-pwd/success-msg.jpg)

- Nếu thất bại, hệ thống sẽ hiển thị thông báo lỗi và giữ nguyên giao diện hiện tại của người dùng.

  ![Error Message](/images/media-live/um-change-pwd/error-msg.jpg) -->

## Basic service configuration

This is a service configuration guide at the most basic level, excluding advanced configurations

Basic steps:

Step 1: [Signal flow settings](./b-step1.md)

Step 2: [Create new input](./c-step2.md)

Step 3(optional): [Create DRM Credential](./d-step3-drm.md)

Step 4: [Create the desired channel and run it](./e-step4.md)

Step 5: [Channel Management and Monitoring](./f-step5.md)

Step 6: [Delete channel.] (./g-step6.md)
