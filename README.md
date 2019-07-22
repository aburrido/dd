本项目来自于萌咖博客：https://moeclub.org/2017/11/19/483/

因为萌咖大佬把脚本放在自己的服务器，怕哪天失效了，所以就放在git上面，防止失效

如有侵犯到萌咖大佬的权益，请联系我删除。

感谢大佬提供的脚本！！！

# 简介：

无限制全自动dd安装Windows

突破没有VNC,没有救援模式,内存比dd包小的限制.

使用Debian Live CD中的busybox做中间媒介,经过复杂的处理,

使本机的网络参数传进Windows操作系统中,

即使没有DHCP能够让Windows获取网络参数,

也能让Windows操作系统在开机的第一时间能够连通网络.

## 需求:

1.Debian/Ubuntu/CentOS 系统(由GRUB引导)； 

2.wget 用来下载文件，获取公网IP; 

3.ip 获取网关，掩码等; 

4.sed awk grep 处理文本流； 

5.VNC 安装系统(此项为可选)。

## 确保安装了所需软件:

```shell
#Debian/Ubuntu:
apt-get install -y gawk sed grep

#RedHat/CentOS:
yum install -y gawk sed grep
```

## 如果出现了错误,请运行:

```shell
#Debian/Ubuntu:
apt-get update

#RedHat/CentOS:
yum update
```

## 安装:

```shell
wget --no-check-certificate -qO InstallNET.sh 'https://raw.githubusercontent.com/vipxkw/dd/master/InstallNET.sh' && bash InstallNET.sh -dd '[Windows dd包直连地址]'
```

## 使用栗子：

```shell
#在你的机器上全新安装,如果你有VNC,可以看到全部过程.
#在dd的过程中,会卡在分区的界面上,不会走进度条.完成后将会自动重启.

wget --no-check-certificate -qO InstallNET.sh 'https://raw.githubusercontent.com/vipxkw/dd/master/InstallNET.sh' && bash InstallNET.sh -dd 'http://pan.i8l.net/%E9%95%9C%E5%83%8F/DD%E9%95%9C%E5%83%8F/Win/win7emb_x86.tar.gz'
```

这里我保存了3个镜像，win7 X86、win8.1 X64、WIN10 X64使用的onedrive

win7 X86：

http://pan.i8l.net/%E9%95%9C%E5%83%8F/DD%E9%95%9C%E5%83%8F/Win/win7emb_x86.tar.gz

win8.1 X64:

http://pan.i8l.net/%E9%95%9C%E5%83%8F/DD%E9%95%9C%E5%83%8F/win8.1emb_x64.tar.gz

win10 X64:

http://pan.i8l.net/%E9%95%9C%E5%83%8F/DD%E9%95%9C%E5%83%8F/win10ltsc_x64.tar.gz

以上镜像也是来自于萌咖博客

## 注意事项:

远程登陆账号为: Administrator

远程登陆密码为: Vicer

仅修改了主机名,可放心使用.(建议自己制作.)

使用的公用网盘,如需长期/大量使用此包请自行备份.

如果因此违反了TOS,萌咖不负任何责任.
