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
3/
```
sudo apt-get update
```
4/ Cài docker
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugi
```
# Subspace Guide cài đặt (dành cho docker trên linux)
1/ Tải thư mục Subspace về
```
git clone https://github.com/pnpn1212/Subspace-monitor-linux.git
```
```
cd subspace-monitor-linux
```
Sửa đổi tên Node, địa chỉ ví, đường dẫn lưu file, đường dẫn plot, dung lượng cần plot
```
nano docker-compose.yml 
```
Lưu lại sau khi nano
```
Ctrl + X + Y + enter
```
2/
Bắt đầu cài đặt
```
docker compose up -d
```
Nếu không chạy được thì dùng 
```
docker-compose up -d
```
3/Truy cập Grafana
Nếu là VPS thì thay localhost bằng địa chỉ IP
```
localhost:3000
```

Thông tin đăng nhập Grafana
```
user: admin
pass: MFL123123
```
Ảnh minh họa

![image](https://github.com/pnpn1212/Subspace-monitor-linux/assets/76662222/cb17be13-2e60-4a98-a978-8d5e631dcd9a)
![image](https://github.com/pnpn1212/Subspace-monitor-linux/assets/76662222/977ef134-b3b5-458e-a4f6-5e7e3ba1a562)
![image](https://github.com/pnpn1212/Subspace-monitor-linux/assets/76662222/ac7b4031-42ec-4e99-9b22-85f8d5a69e5a)

Bản quyền của MFLow - MFL VNBnodes
