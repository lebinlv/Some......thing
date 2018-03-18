## Windows

- [MobaXterm](https://mobaxterm.mobatek.net/)
- [MarkDown: YuWriter](https://ivarptr.github.io/yu-writer.site/index.html)
- [Snipaste](https://zh.snipaste.com/index.html)
- FSCapture
- NetAssist 野人版

Windows App Store

- Snipaste
- ScreenToGif
- QuickLook

## Ubuntu

### GenPac

#### 安装

    pip install genpac

#### 或从github安装开发版本

    pip install https://github.com/JinnLynn/genpac/archive/master.zip

#### 更新

    pip install --upgrade genpac

#### 或从github更新开发版本

    pip install --upgrade https://github.com/JinnLynn/genpac/archive/master.zip

#### 卸载

    pip uninstall genpac

#### 从gfwlist生成代理信息为SOCKS5 127.0.0.1:1080的PAC文件

    genpac --format=pac --pac-proxy="SOCKS5 127.0.0.1:1080" -o autoproxy.pac

> 后期更新pac文件可使用

#### PAC格式 如果在线gfwlist获取失败使用本地文件，如果在线gfwlist获取成功更新本地gfwlist文件

    genpac --format=pac --pac-proxy="SOCKS5 127.0.0.1:1080" --gfwlist-local=~/gfwlist.txt --gfwlist-update-local -o autoproxy.pac

#### 最后

随后打开，系统代理→自动→配置URL user为你自己的用户名(不要花括号....)
    file:///home/{user}/autoproxy.pac

----

### Windows + Ubuntu 双系统时间不一致解决方法

#### 方法①：修改/etc/default/rcS文件

编辑```/etc/default/rcS``` 将```UTC=yes```改成```UTC=no``` ，这是以前的方法，新版本的Ubuntu使用systemd启动之后，时间也改成了由timedatectl来管理，此方法就不适用了

#### 方法②：执行下面命令

    timedatectl set-local-rtc 1 --adjust-system-clock

----

### openssh-server

    sudo apt-get install openssh_server
    sudo nano /etc/ssh/sshd_config

----

### 安装ubuntu后要做的事

    sudo apt-get remove --purge libreoffice-common unity-webapps-common thunderbird totem rhythmbox empathy brasero simple-scan gnome-mahjongg aisleriot gnome-mines cheese transmission-common gnome-orca webbrowser-app gnome-sudoku onboard deja-dup

> 清理系统