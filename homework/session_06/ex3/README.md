# Bài 3: Cấu hình tường lửa UFW và chuẩn đoán cổng mạng

## 1. Cấu hình tường lửa UFW
Các lệnh cấu hình:
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing

sudo ufw allow 22/tcp
sudo ufw allow 8080/tcp

sudo ufw enable
```

## 2. Kiểm tra
Lệnh kiểm tra:
```bash
sudo ufw status verbose
```

Kết quả:
```text
Status: active
Logging: on (low)
Default: deny (incoming), allow (outgoing), disabled (routed)
New profiles: skip

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW IN    Anywhere
8080/tcp                   ALLOW IN    Anywhere
22/tcp (v6)                ALLOW IN    Anywhere (v6)
8080/tcp (v6)              ALLOW IN    Anywhere (v6)
```

Lệnh kiểm tra cổng đang lắng nghe:
```bash
ss -tlnp
```
