# My favorite Tips & Tricks (Cheat Sheet)

## Table of Contents
- [My favorite Tips \& Tricks (Cheat Sheet)](#my-favorite-tips--tricks-cheat-sheet)
  - [Table of Contents](#table-of-contents)
    - [Chạy engine cờ tướng Pikafish trên cloud shell.segfault.net](#chạy-engine-cờ-tướng-pikafish-trên-cloud-shellsegfaultnet)
    - [Chạy engine cờ tướng Pikafish trên cloud lightning.ai](#chạy-engine-cờ-tướng-pikafish-trên-cloud-lightningai)


### Chạy engine cờ tướng Pikafish trên cloud shell.segfault.net

**Bài viết này chỉ cho mục đích học tập. Vui lòng không lạm dụng dịch vụ.**

1. Vào <https://shell.segfault.net> và làm theo hướng dẫn.
2. Chạy lệnh `info` trong Terminal để lấy khóa (private key) và cấu hình config kết nối SSH.
3. Lưu tệp khóa SSH vào thư mục `~/.ssh/` trên máy **Windows**.
4. Sao chép cấu hình kết nối SSH vào tệp `~/.ssh/config` trên máy **Windows**.
5. Mở Terminal trên **Windows**, kết nối SSH tới **Server**:
    ```cmd
    ssh giga
    ```

6. Cài đặt engine Pikafish trên **Server** bằng lệnh sau:
    ```bash
    cd
    wget -O pika https://github.com/vinhgiga/archive/releases/download/xiangqi-engine/pikafish-vnni512
    wget -O pikafish.nnue https://github.com/vinhgiga/archive/releases/download/xiangqi-engine/pikafish.nnue
    chmod +x pika
    ```

7. (Tùy chọn) Kiểm tra xem engine đã hoạt động chưa:
    ```bash
    ./pika
    ``` 

8. Tạo tệp `cloud.bat` trên máy **Windows** với nội dung sau:
    ```bat
    @echo off
    ssh giga "pkill -9 pika; cd; ./pika"
    ```
  
9. Nạp tệp `cloud.bat` vào GUI Pengfei hoặc [chuyển đổi sang exe](https://bat-to-exe-converter-x64.en.softonic.com/download). Thưởng thức 🫖

### Chạy engine cờ tướng Pikafish trên cloud lightning.ai

**Bài viết này chỉ dành cho mục đích học tập. Vui lòng không lạm dụng dịch vụ.**

1. Tạo tài khoản [Lightning AI](https://lightning.ai).

    **Lưu ý**: Email edu sẽ được xác minh ngay lập tức, email thông thường cần chờ 2-3 ngày. Sau khi xác minh email, bạn sẽ phải xác minh số điện thoại. Việt Nam không được hỗ trợ, bạn có thể mua mã xác thực giá 5k trên [SMS activate](https://sms-activate.guru/?ref=12121940), hoặc liên hệ mình sẽ mua hộ bạn với giá 10k.
    
    Messenger: [Nguyễn Quang Vinh](https://www.facebook.com/vinhgiga)
    
    Email: <vinhgiga@gmail.com>
2. Nhấp vào `+ New Studio` > `Prep data` > `Start`. Mỗi tháng bạn sẽ được 15 lượng miễn phí, tương đương 5 tiếng/tháng chạy engine 32U. Không giới hạn nếu chạy 4U.
3. Mở `Terminal` trên **Server** và cài đặt engine Pikafish bằng lệnh sau:
    ```bash
    cd
    wget -O pika https://github.com/vinhgiga/archive/releases/download/xiangqi-engine/pikafish-vnni512
    wget -O pikafish.nnue https://github.com/vinhgiga/archive/releases/download/xiangqi-engine/pikafish.nnue
    chmod +x pika
    ```
4. (Tùy chọn) Kiểm tra xem engine đã cài đặt chưa:
    ```bash
    ./pika
    ```
5. Nhấp vào icon `Terminal` > `Connect via SSH` > `Windows` > sao chép lệnh Powershell tạo kết nối SSH.
6. Trên máy **Windows**, mở Powershell hoặc Terminal với quyền quản trị và chạy lệnh đã sao chép.
7. Sao chép lệnh kết nối SSH.
8. Trên máy **Windows**, tạo tệp `cloud.bat` với nội dung sau:
    ```bat
    @echo off
    ssh xxx@ssh.lightning.ai "pkill -9 pika; cd; ./pika"
    ```
9. Nạp tệp `cloud.bat` vào GUI Pengfei hoặc [chuyển đổi sang exe](https://bat-to-exe-converter-x64.en.softonic.com/download). Thưởng thức 🫖
