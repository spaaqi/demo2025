# demo2025

1 модуль

ISP
```bash
hostnamectl set-hostname isp;exec bash
mkdir /etc/net/ifaces/ens19 (сеть Интернет)
mkdir /etc/net/ifaces/ens20 (сеть в сторону офиса HQ)
mkdir /etc/net/ifaces/ens21 (сеть в сторону офиса BR)
```
ens19
```bash
vim /etc/net/ifaces/ens19/options
TYPE=eth
DISABLED=no
NM_CONTROLLED=no
BOOTPROTO=dhcp
IPV4_CONFIG=yes
```
ens20
```bash
vim /etc/net/ifaces/ens20/options
TYPE=eth
DISABLED=no
NM_CONTROLLED=no
BOOTPROTO=static
IPV4_CONFIG=yes
```
ens21
```bash
 cp /etc/net/ifaces/ens20/options /etc/net/ifaces/ens21/
```
