UPDATE lên bản crack:

```bash
curl https://raw.githubusercontent.com/ThemeWayOut/btpanel-v7.7.0/refs/heads/main/install/update_7.x_en.sh|bash
```

Cài mới aapanel:

```bash
URL=https://raw.githubusercontent.com/ThemeWayOut/btpanel-v7.7.0/refs/heads/main/install/update_7.x_en.sh && if [ -f /usr/bin/curl ];then curl -ksSO "$URL" ;else wget --no-check-certificate -O install_7.0_en.sh "$URL";fi;bash install_7.0_en.sh aapanel
```

Gỡ aapanel:

```bash
sudo bt stop &&sudo update-rc.d -f bt remove &&sudo rm -f /etc/init.d/bt &&sudo rm -rf /www/server/panel
```
