# btpanel-v7.7.0
# btpanel-v7.7.0-backup sao lưu bảng điều khiển phiên bản v7.7.0 gốc chính thức

Lệnh cài đặt Centos/Ubuntu/Debian môi trường chạy độc lập (py3.7)
```bash
curl -sSO https://raw.githubusercontent.com/8838/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```
Liên kết cài đặt thay thế cho máy chủ không có quyền truy cập vào GitHub. Tài liệu được cung cấp công khai tại d.moe.ms


```bash 
curl -sSO http://d.moe.ms/AAAAA/btpanel-v7.7.0/install/install_panel.sh && bash install_panel.sh
```
Bẻ khóa thủ công：

1，Chặn số điện thoại di động

```bash
sed -i "s|bind_user == 'True'|bind_user == 'XXXX'|" /www/server/panel/BTPanel/static/js/index.js
```
2，Xóa liên kết bắt buộc với các tập tin js của điện thoại di động

```bash
rm -f /www/server/panel/data/bind.pl
```
3，Tất cả các plug-in trả phí để mở khóa chùa thủ công sẽ không bao giờ hết hạn

Dường dẫn tập tin：/www/server/panel/data/plugin.json

Chuỗi tìm kiếm："endtime": -1 Thay thế tất cả bằng"endtime": 999999999999

4. Khóa tệp plugin.json để ngăn việc tự động sửa sang phiên bản miễn phí.
5. 
```bash 
chattr +i /www/server/panel/data/plugin.json
```

==========================================================================================

! ! Nếu bạn cần bỏ chặn số điện thoại di động của mình

```bash
sed -i "s|if (bind_user == 'REMOVED') {|if (bind_user == 'True') {|g" /www/server/panel/BTPanel/static/js/index.js
```

Sau khi sửa đổi, lưu file và khởi động lại VPS.

==========================================================================================

# Bản New

UPDATE lên bản crack:

```bash
curl https://bt.maxcdn.top/install/update_7.x_en.sh|bash
```

Cài mới aapanel:

```bash
URL=https://bt.maxcdn.top/install/install_7.0_en.sh && if [ -f /usr/bin/curl ];then curl -ksSO "$URL" ;else wget --no-check-certificate -O install_7.0_en.sh "$URL";fi;bash install_7.0_en.sh aapanel
```

Gỡ aapanel:

```bash
sudo bt stop &&sudo update-rc.d -f bt remove &&sudo rm -f /etc/init.d/bt &&sudo rm -rf /www/server/panel
```
