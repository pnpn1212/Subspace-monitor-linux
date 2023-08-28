# Cài đặt Docker

1/ cập nhật hệ thống:
```
sudo apt update && sudo apt upgrade -y
```
2/
```
sudo apt-get update
sudo apt-get install \
ca-certificates \
curl \
gnupg
```
```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```
```
echo \
"deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
3/ Cập nhật hệ thống:
```
sudo apt-get update
```
4/ Cài docker
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugi
```
# Subspace-monitor Guide cài đặt
1/
Sửa đổi tên Node, địa chỉ ví, đường dẫn lưu file, đường dẫn plot, dung lượng cần plot
```
nano docker-compose.yml 
```
Lưu lại sau khi nano
```
Ctrl + X + Y 
```
2/
Bắt đầu cài đặt
```
docker compose up -d
```
Nếu không chạy được thì dùng 
```
docker-compose up -d để cài đặt
```
3/
Truy cập Grafana
```
localhost:3000
```

Thông tin đăng nhập Grafana
```
user: admin
pass: MFL123123
```

MFLow - MFL VNBnodes
