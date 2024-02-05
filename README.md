# btpanel-v7.7.0
btpanel-v7.7.0-backup sao lưu bảng điều khiển phiên bản v7.7.0 gốc chính thức

**Lệnh cài đặt Centos/Ubuntu/Debian Môi trường hoạt động độc lập (py3.7):**

```Bash
curl -sSO https://raw.githubusercontent.com/ThemeWayOut/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```
Crack

```Bash
sed -i "s|bind_user == 'True'|bind_user == 'XXXX'|" /www/server/panel/BTPanel/static/js/index.js
```
```Bash
rm -f /www/server/panel/data/bind.pl
```
Host 'xxx.xx.xxx.xxx' is not allowed to connect to this MySQL server
```Bash
mysql -u root -h localhost -p123456
CREATE USER 'root'@'localhost' IDENTIFIED BY '123456';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost'
WITH GRANT OPTION;
CREATE USER 'root'@'%' IDENTIFIED BY '123456';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%'
WITH GRANT OPTION;
```
