---
title: Kiến trúc hệ thống
order: 2
---

# Infrastructure of Sigma Live Streaming System

![about-2](/images/livestream/livestream-about-2.png)

## Broadcaster

Sigma live stream platform có sdk hỗ trợ cho các nền tảng như android, ios với những tính năng quan trọng:

- AAC audio encoding, H.264 video encoding (supports soft/hard editing, supports baseline/main/high profile)

- Multi-resolution encoding support

- Camera control (heading, flash, front and rear camera)

- Adaptively adjust the bit rate of the video according to the network bandwidth, the network adaptive mode can be configured

- Support RTMP protocol live streaming

- Support encode video in low latency mode

## Viewer playback

Trên các thiết bị mobile sử dụng hệ điều hành android và ios, Sigma live stream platform hỗ trợ player playback:

- Plugin SDK for Exoplayer (required version 2.6 or above)

- Plugin SDK for AVPlayer

- Support Low Latency HLS

- Preview thumbnail in livestream

- Support livestream DVR

- Support ABR (Adaptive bitrate) for Low Latency HLS

  - **Setting a suitable initial start position**: Chọn thời điểm start mong muốn để có thể có độ trễ thấp nhất só với luồng trực tiếp. Ví dụ ở chế độ ultra low latency, hệ thống cho bắt đầu luồng phát ở độ trễ 3 giây so với live

  - **Adjusting the playback speed**: Tốc độ của luồng phát được điều trỉnh trong khoảng từ 0.8-1.2 để người xem không phát hiện ra sự thay đổi. Mục đích nhắm kéo dãn buffer của luồng phát đạt đến được độ trễ mong muốn

## RTMP Server

Hệ thống RTMP Server được chia theo khu vực để kết nối với broadcast nhanh nhất có thể, với tính năng tự động scale, hệ thống có thể xử lý được hàng ngàn kết nối

## Sigma Live Server

Máy chủ xử lý dữ liệu media bao gồm các tính năng sau

- Hỗ trợ transmux & transcode kênh live stream với độ trễ thấp, hiệu năng cao

- Transcode resolution up to UltraHD (4K)

- Full Resolution Control: resize, crop, letterbox, and more

- Adjustable aspect ratio of the output video

- Video Filters: Rotate, Denoise, Deinterlace, sharpen, autolevel, deblock, flip, mirror

- Audio Controls: Normalize, Gain, Equalize, Fade-in, Fade-out, Karaoke, Advanced Audio Levels Control

- Advanced Audio Resampling

- Conditional Outputs (min/max size and duration)

- Support mode zero latency for optimize encoding time

## Api Server

Hệ thống Api Server cung cấp API giao tiếp với App Server live stream:

- Quản lý livestream event (create, update, remove ...)
- Quản lý livestream asset (DVR, catchup, thumbnail ... )
- Webhook livestream event

## Monitor

- Theo dõi hệ thống qua các thông số quan trọng
- Cảnh báo khi hệ thống gặp sự cố

## Streaming flow using Sigma Live Streaming platform

![livestream/about-3](/images/livestream/livestream-about-3.png)

- **Luồng dữ liệu từ người phát**:

  1. Đăng nhập hệ thống và yêu cầu tạo luồng phát

  2. Hệ thống sinh và trả về **RTMP Server** (tương ứng với vị trí của nguồn phát) và **token** xác thực nguồn phát

  3. Bắt đầu phát trực tiếp lên **RTMP Server**

  4. **RTMP Server** xác thực nguồn phát dựa trên token cập nhật metadata vào danh sách kênh

  5. Tương tác với người xem

- **Luồng dữ liệu từ người xem**:

  1. Đăng nhập hệ thống à liệt kê danh sách kênh đang phát hoặc đã phát phù hợp (dựa trên vị trí địa lý, độ ưu tiên của kênh, các kênh đã thích …)

  2. Chọn kênh muốn xem

  3. Hệ thống trả về Edge server (CDN) phù hợp với người xem

  4. Xem kênh và tương tác (tán gẫu, gửi quà …)
