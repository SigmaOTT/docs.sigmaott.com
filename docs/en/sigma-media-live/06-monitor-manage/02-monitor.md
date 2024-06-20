---
title: Supervise
order: 2
---

## Channel Monitoring

For each channel on the system, there will be 1 or more **jobs** that perform channel transcoding or encapsulation. The status of the channel will be the sum of the status of the **job** corresponding to the corresponding channel

- The number of jobs of the channel will correspond to the corresponding output of the channel, besides, if the output has the catchup and timeshift feature enabled, the system will create 1 more **job catchup** corresponding to this output (splitting this job helps the system operate stably when 1 of the jobs may have problems)
- When configuring to create a new channel, the system will automatically create the necessary jobs for the channel
  ::: warning
  Changing the channel configuration can change the number of jobs in the channel and may result in the loss of necessary jobs
  :::

### Channel status

The channel system has the following statuses

- **live**: channel is on
- **stop**: The channel is being turned off
- **error**: Channel is failing
  - The channel may encounter an error status when there is 1 job executing the task in the channel that is experiencing the error

### Status of job

For each Job in the channel, there will be 1 service running separately on different specified servers, receiving inputs and outputs according to the requirements of the job. In which Job will have the corresponding types as follows:

1. **Transcode**: This is the job that performs the transcoding of channel content for the transcode channel. For each transcoding channel, there will only be this job.
2. **Package**: Job packing, quantity corresponding to the number of output installed
3. **Catchup**: Job packing for catchup content, timeshift, quantity corresponding to the number of output settings

For each job, we will have the following job statuses:

| Condition     | Depict                                                                                                                                                                |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **starting**  | Job is in the process of initial launch                                                                                                                               |
| **preparing** | Job is in the process of preparing resources such as obtaining information of input, obtaining output information ... |
| **started**   | Job successfully launched                                                                                                                                             |
| **error**     | Job is faulty. Please see the job error code below to detect the cause                                                                                |
| **Stop**      | Job has been stopped                                                                                                                                                  |

The operation with the system job provides pushing all \*\*\*\* actions such as **start**, **stop**, **reset**, done through the **action** list of the job

- You can manipulate Jobs from outside of the channel list under Jobs or from the channel monitoring page

### Channel Monitoring

From the list of channels, clicking \*\*\*\* on the name of the channel, the detailed channel interface will appear:

![Thông tin chi tiết kênh](/images/media-live/general/channel-detail.png)

Monitoring components include:

- **job Speed**: A timed string chart showing the speed of the **job**
  - The speed of **job** is calculated according to the 100% mark
    - With values less than 90% of jobs are having problems in processing such as input source, output problem
- **INPUTS**: Channel input list
- **TRANSCODE**: Information about Transcode Processing System (Transcode)
  - Includes: details about Job transcode
  - Transcode Profile Information
- **PACKAGES**: Channel's packaged output information
  - List of outputs along with job attachments
  - For each output list, there will be up to 2 jobs including **package job** and **catchup job**

### Job Supervisor

- Note:
  - **Job** monitoring panel can be tracked in the channel list or in the channel detail page

![Thông tin chi tiết job](/images/media-live/general/job-detail.png)

Job error log structure

```
[05-26 02:32:55] Input timeout (code: INPUT_TIMEOUT)
```

Where:

- **[05-26 02:32:55]**: Time value, in UTC
- **Input timeout** : Error message
- **(code: INPUT_TIMEOUT)** : Error code

A few common error codes and accompanying annotations

| Code                                                                                                          | description                                                                                                                 | Input Error | Output Error | Processing Error | Config Error |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ----------- | ------------ | ---------------- | ------------ |
| TIMEOUT                                                                                                       | Job is timed out (The input source loses video waves)                                                    | x           |              |                  |              |
| **PACKET_QUEUE_IS_FULL**                       | Packets in the queue cannot be processed in time (lack of resources)                                     | x           | x            | x                |              |
| MEMORY_IS_FULL                                                      | Out of Ram memory                                                                                                           |             |              | x                |              |
| **INPUT_TIMEOUT**                                                                        | Input Timeout (loss of input wave)                                                                       | x           |              |                  |              |
| **OUTPUT_TIMEOUT**                                                                       | Đầu ra Timeout (phụ thuộc vào từng luồng đầu ra)                                                         |             | x            |                  |              |
| **TRANSCODE_TIMEOUT**                                                                    | The Processing Server encountered a problem                                                                                 |             |              | x                |              |
| GOP_INVALID                                                                              | GOP cache error of input                                                                                                    | x           |              |                  |              |
| ASYNC_STREAM                                                                             | Asynchronous input streams (ABR streaming)                                                               | x           |              |                  |              |
| **ASYNC_PROFILE**                                                                        | ABR streaming                                                                                                               | x           |              |                  |              |
| INPUT_OUTPUT_ERROR                                                  | Input and output streams crash                                                                                              | x           | x            |                  |              |
| IO_ERROR                                                                                 | Errors during read and write                                                                                                | x           | x            |                  |              |
| **CONNECTION_REFUSED**                                                                   | Kết nối bị đầu vào hoặc đầu ra bị refused (Lỗi thường xảy ra khi không thể kết nối đến manifest service) | x           | x            |                  |              |
| CONNECTION_TIMEOUT                                                                       | Kết nối đầu vào hoặc đầu ra timeout                                                                                         | x           | x            |                  |              |
| CANNOT_OPEN_CONNECTION                                              | Failed to create connection                                                                                                 | x           | x            |                  |              |
| URL_READ_ERROR                                                      | URL data reading errors                                                                                                     | x           | x            |                  |              |
| OPTION_NOTFOUND'\*'                                                                      | Incorrect upload configuration                                                                                              |             |              |                  | x            |
| PROTOCOL_NOTFOUND'\*'                                                                    | Protocol Not Found                                                                                                          |             |              |                  | x            |
| STREAM_NOT_FOUND'\*'                                                | Input stream not found                                                                                                      | x           |              |                  |              |
| UNABLE_TO_OPEN_RESOURCE                        | Unable to initialize resource                                                                                               |             | x            |                  |              |
| NO_ROUTE_TO_HOST'\*'                           | Failed to open connection                                                                                                   | x           | x            |                  |              |
| INVALID_ARGUMENT \*\*\*\*\*                                                              | Wrong parameter                                                                                                             |             |              |                  | x            |
| INITIALIZING_OUTPUT_STREAM'\*'                                      | Error Initializing output stream                                                                                            |             | x            |                  |              |
| CONNECTION_RESET_BY_PEER                       | Connection reset                                                                                                            | x           | x            |                  |              |
| BROKEN_PIPE                                                                              | Broken pipe                                                                                                                 | x           | x            |                  |              |
| NO_AUDIO_DATA'\*'                                                   | Initialization flow without AUDIO data                                                                                      | x           |              |                  |              |
| NO_VIDEO_DATA'\*'                                                   | Initialization flow without VIDEO data                                                                                      | x           |              |                  |              |
| FEATURE_NOT_ENABLED                                                 | Tính năng không được hỗ trợ                                                                                                 |             |              |                  | x            |
| CANT_START_OVERLAY                                                  | Không thể bật được overlay                                                                                                  |             |              |                  | x            |
| NO_SUCH_FILE_OR_DIRECTORY | Không mở được file hoặc thư mục                                                                                             | x           | x            |                  |              |
| END_OF_FILE                                                         | End of file                                                                                                                 |             | x            |                  |              |
| FAILED_TO_RESOLVE_HOSTNAME                     | Không phân giải được tên miền                                                                                               |             | x            |                  |              |
| INVALID_INPUT_DATA                                                  | Dữ liệu cầu vào không hợp lệ                                                                                                | x           |              |                  |              |
| CANT_SYNC_INPUT                                                     | Không đồng bộ được đầu vào                                                                                                  | x           |              |                  |              |
| STREAM_MISSING                                                                           | Luồng đầu vào bị thiếu                                                                                                      | x           |              |                  |              |
| OPEN_ERROR                                                                               | Lỗi Mở đầu vào hoặc đầu ra                                                                                                  | x           | x            |                  |              |
| CLOSE_ERROR                                                                              | Lỗi đóng đầu vào hoặc đầu ra                                                                                                | x           | x            |                  |              |
| SYNC_SEQUENCE                                                                            |                                                                                                                             |             |              | x                |              |
| INPUT_PACKET_TOO_SMALL                         | Gói tin đầu vào không đúng định dạng                                                                                        | x           |              |                  |              |
| AAC_PACKET_TOO_SHORT                           | Gói tin đầu vào của AAC quá nhỏ                                                                                             | x           |              |                  |              |
| PPS_ID_NOT_FOUND                               | Không tìm thấy PPS_ID                                                                                  | x           |              |                  |              |

::: info

- Bold errors are more likely to occur when **job** has run successfully than other errors
- Với các lỗi liên quan đến đầu ra: kiểm tra luồng đầu ra tương ứng (Ổ cứng, Ram, ... )
- Errors '\*\*' only occur when creating new **job**
- When encountering an error, the system will automatically retry the faulty **job** until the error is resolved
  - Đối với các lỗi xảy ra khi khởi tạo job sẽ cần khởi động lại job để xử lý
    :::
