一个apache的日志分析工具

据说nginx也可以，未测试

安装

apt install goaccess -y

官网

https://goaccess.io/get-started

指定日志文件，导出成html

goaccess access.log -o report.html --log-format=COMBINED

或者实时更新的html

goaccess access.log -o /var/www/html/report.html --log-format=COMBINED --real-time-html

中文版

apt update -y
apt install libgeoip-dev -y
apt install libncursesw5-dev -y
git clone https://github.com/wylbjia/goaccess.git
cd goaccess
./configure --enable-utf8 --enable-geoip=legacy
make
make install

然后使用上面的命令生成html

------------

GoAccess 中文版，此中文版基于官方 goaccess 1.2 版本汉化，绝对原汁原味。如有翻译瑕疵，可以联系我们 typefo@qq.com 或者 736589354@qq.com

### GoAccess 中文界面

![screenshots](screenshots.png)

### GoAccess 安装方法

编译安装之前需要安装 geoip 开发包，下载地址 https://github.com/maxmind/geoip-api-c

```
$ yum install -y git
$ git clone https://github.com/wylbjia/goaccess.git
$ cd goaccess-1.2
$ ./configure --enable-utf8 --enable-geoip=legacy
$ make
$ make install
```

