# btpanel-v7.7.0
btpanel-v7.7.0-backup 官方原版v7.7.0版本面板备份

Centos/Ubuntu/Debian安装命令 独立运行环境（py3.7）
```bash
curl -sSO https://raw.githubusercontent.com/8838/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```
备用安装链接，适用于不能访问GitHub的服务器。文件公开存放在d.moe.ms


```bash 
curl -sSO http://d.moe.ms/AAAAA/btpanel-v7.7.0/install/install_panel.sh && bash install_panel.sh
```
手动破解：

1，屏蔽手机号

```bash
sed -i "s|bind_user == 'True'|bind_user == 'XXXX'|" /www/server/panel/BTPanel/static/js/index.js
```
2，删除强制绑定手机js文件

```bash
rm -f /www/server/panel/data/bind.pl
```
3，手动解锁宝塔所有付费插件为永不过期

文件路径：/www/server/panel/data/plugin.json

搜索字符串："endtime": -1全部替换为"endtime": 999999999999

4，给plugin.json文件上锁防止自动修复为免费版
```bash 
chattr +i /www/server/panel/data/plugin.json
```

============================

！！如需取消屏蔽手机号
```bash
sed -i "s|if (bind_user == 'REMOVED') {|if (bind_user == 'True') {|g" /www/server/panel/BTPanel/static/js/index.js
```

修改后保存文件，重启VPS即可。

===============================================================================================

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
