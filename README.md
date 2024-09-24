UPDATE lên bản crack:
```bashcurl https://bt.maxcdn.top/install/update_7.x_en.sh|bash```bash

Cài mới aapanel:
```bashURL=https://bt.maxcdn.top/install/install_7.0_en.sh && if [ -f /usr/bin/curl ];then curl -ksSO "$URL" ;else wget --no-check-certificate -O install_7.0_en.sh "$URL";fi;bash install_7.0_en.sh aapanel```bash

Gỡ aapanel:
```bashsudo bt stop &&sudo update-rc.d -f bt remove &&sudo rm -f /etc/init.d/bt &&sudo rm -rf /www/server/panel```bash
