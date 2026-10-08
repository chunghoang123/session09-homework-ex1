# Bài 1: Kiểm tra cài đặt Docker Engine và chạy Container Hello-World

## Môi trường thực hiện
- OS: Windows 11 + Docker Desktop 4.87.0 (Engine 29.7.2)
- Daemon: đã khởi động Docker Desktop (trước đó `docker version` báo lỗi `dockerDesktopLinuxEngine ... cannot find the file specified` vì Docker Desktop chưa chạy)
- Không cần tiền tố `sudo` (Windows không dùng `sudo`; tương đương với việc user đã có quyền kết nối Docker Daemon)

## 1. `docker version`

```
Client:
 Version:           29.7.2
 API version:       1.55
 Go version:        go1.26.5
 Git commit:        a7dcaa6
 Built:             Wed Aug  5 18:31:33 2026
 OS/Arch:           windows/amd64
 Context:           desktop-linux

Server: Docker Desktop 4.87.0 (236836)
 Engine:
  Version:          29.7.2
  API version:      1.55 (minimum version 1.40)
  Go version:       go1.26.5
  Git commit:       6a43e3d
  Built:            Wed Aug  5 18:28:36 2026
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          v2.2.5
  GitCommit:        e53c7c1516c3b2bff98eb76f1f4117477e6f4e66
 runc:
  Version:          1.3.6
  GitCommit:        v1.3.6-0-g491b69ba
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

## 2. `docker info` (rút gọn)

```
Server Version: 29.7.2
Storage Driver: overlayfs
Kernel Version: 6.18.33.2-microsoft-standard-WSL2
Operating System: Docker Desktop
OSType: linux
Architecture: x86_64
CPUs: 12
Total Memory: 5.643GiB
```

## 3. `docker run hello-world`

```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
Digest: sha256:5e23090353324d887c48ad5e5c56d294eab81588df9605b07d1afe895f9cc8f8
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.
```

## Kết luận
- Đã kết nối tới Docker Daemon không cần `sudo`.
- Đã chạy đủ 3 lệnh `docker version`, `docker info`, `docker run hello-world`.
- Kết quả đạt yêu cầu: Terminal xuất hiện dòng `Hello from Docker! This message shows that your installation appears to be working correctly.`
