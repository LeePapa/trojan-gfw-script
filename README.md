![logo](https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/logo.png)
# Trojan-GFW Script
## This script will help you set up a [Trojan-GFW](https://github.com/trojan-gfw/trojan) and an Ultimate Offline download server in an extremely fast way.
### Read The Fucking Manual: https://www.johnrosen1.com/trojan/

### GUI Version (Everything has been included)
```
apt-get update && apt-get install sudo whiptail curl locales -y
```
```
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojangui.sh)"
```
![menu](https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/menu.png)
![choose](https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/options.png)

#### Friendly Reminder:
1. Please **[Purchase a domain](https://www.namesilo.com/?rid=685fb47qi)** and **[finish a dns resolve](https://dnschecker.org/)** before running this bash script!
2. Please **Open Tcp port [80](https://www.speedguide.net/port.php?port=80) and [443](https://www.speedguide.net/port.php?port=443)** in your vps firewall panel before running this bash script!
3. Please manually change system dns to frequently updated dns like [1.1.1.1](https://1.1.1.1/) instead of those who update slowly like aliyun lan dns !
```
echo "nameserver 1.1.1.1" > '/etc/resolv.conf'
```
4. Please **Change QBittorrent Download save path to /usr/share/nginx/qbt/ manually !**

#### [Telegram](https://telegram.org/) Channel And Group

### https://t.me/johnrosen1

### https://t.me/trojanscript

## If you found it useful , please give a star ,thanks!
#### Bash Features:

1. Auto install and config **[Trojan-GFW](https://github.com/trojan-gfw/trojan) and [NGINX](https://www.nginx.com/)**
3. Auto issue renew [let's encrypt certificate](https://letsencrypt.org/) and **auto reload Trojan-GFW after renewal**
4. Auto OS Detect **Support [Debian](https://www.debian.org/) [Ubuntu](https://ubuntu.com/)** (NO Centos Support!!!) 
5. Auto [domain resolve verification](https://en.wikipedia.org/wiki/Nslookup)
6. Auto [iptables](https://en.wikipedia.org/wiki/Iptables)(includes ipv6) firewall config and [iptables-persistent](https://github.com/zertrin/iptables-persistent)
7. Auto generate [client config](https://trojan-gfw.github.io/trojan/config) (includes both Trojan-GFW and V2ray )
9. Auto [TCP Turbo](https://github.com/shadowsocks/shadowsocks/wiki/Optimizing-Shadowsocks) enable ( **[TCP-BBR](https://github.com/google/bbr)** included)
10. Auto [Nginx Performance Optimization](https://www.johnrosen1.com/nginx1/)
11. Auto [Trojan-GFW ***trojan://*** share link and QR code generate](https://github.com/trojan-gfw/trojan-url)
12. Auto [V2ray ***vmess://*** share link generate](https://github.com/boypt/vmess2json)
13. Auto [https 301 redirect](https://en.wikipedia.org/wiki/HTTP_301) without affecting certificate renew
14. Auto enable [HSTS header](https://securityheaders.com/)
16. Auto ***Random Html Template Choose***
17. Auto enable [***Full IPv6 Support***](https://en.wikipedia.org/wiki/IPv6)
18. Auto enable ***[time sync](https://www.freedesktop.org/software/systemd/man/timedatectl.html)***
19. Auto enable ***Fail Restart*** 
20. Auto [uninstall Aliyun Aegis](https://www.johnrosen1.com/ali-iso/)
20. Support Auto install and config **[Dnsmasq](https://en.wikipedia.org/wiki/Dnsmasq) [V2ray](https://www.v2ray.com/index.html) [Shadowsocks](https://shadowsocks.org/en/index.html)([V2ray-plugin](https://github.com/shadowsocks/v2ray-plugin)) [Qbittorrent](https://www.qbittorrent.org/) and [Aria2](https://github.com/aria2/aria2)**
19. Support auto [***vmess or ss + tls + websocket + nginx*** config](https://guide.v2fly.org/advanced/wss_and_web.html)
20. Support ***[BBRPLUS](https://github.com/chiakge/Linux-NetSpeed)***
15. Support ***[TLS1.3 ONLY](https://wiki.openssl.org/index.php/TLS1.3)***
21. Support manually check for update include both Trojan-gfw and v2ray
23. Support Full Uninstall

**If you need more functions, please open a Github issue.(No Centos related issues or bugs allowed except pull requests)**

### VPS Recommendation (no personal aff included)

#### https://www.kamatera.com/

#### Related Links

https://www.johnrosen1.com/qbt/

### Debug Guide

```
sudo systemctl status trojan
sudo systemctl status nginx
sudo systemctl status v2ray
sudo systemctl status dnsmasq
sudo systemctl status qbittorrent
sudo systemctl status aria2
journalctl -e -u trojan.service
cat /var/log/v2ray/error.log
cat /usr/local/etc/trojan/config.json
cat /etc/nginx/conf.d/trojan.conf
cat /etc/v2ray/config.json
cat /etc/aria.conf
crontab -l
sudo ~/.acme.sh/acme.sh --cron
timedatectl
iptables -L -v
```
### Result Example
```
trojan://trojanscript@www.johnrosen.top:443
```
![Trojan-GFW QR code](https://raw.githubusercontent.com/johnrosen1/trojan-gfw-script/master/trojanscript.png)



