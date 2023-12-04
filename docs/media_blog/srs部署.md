# srs 部署
[文档来源](https://ossrs.io/lts/zh-cn/docs/v5/doc/getting-started-build)
## Live Streaming
直播是SRS的典型场景，支持推直播流后多种观看方式。

下载源码，推荐用Ubuntu20：
```shell
git clone -b develop https://gitee.com/ossrs/srs.git
```
编译，注意需要切换到srs/trunk目录：
```shell
cd srs/trunk
./configure
make
```
启动服务器：
```shell
./objs/srs -c conf/srs.conf
```
检查SRS是否成功启动，可以打开 http://localhost:8080/ ，或者执行命令：

# 查看SRS的状态
```shell
./etc/init.d/srs status
```

# 或者看SRS的日志
```shell
tail -n 30 -f ./objs/srs.log

```
例如，下面的命令显示SRS正在运行：
```shell
MB0:trunk $ ./etc/init.d/srs status
SRS(pid 90408) is running.                                 [  OK  ]

MB0:trunk $ tail -n 30 -f ./objs/srs.log
[2021-08-13 10:30:36.634][Trace][90408][12c97232] Hybrid cpu=0.00%,0MB, cid=1,1, timer=61,0,0, clock=0,22,25,0,0,0,0,1,0

```
使用 FFmpeg(点击下载) 或 OBS(点击下载) 推流：
```
ffmpeg -re -i ./doc/source.flv -c copy -f flv rtmp://localhost/live/livestream
```
Note: 实例文件./doc/source.flv在SRS的源代码目录中有。

打开下面的页面播放流（若SRS不在本机，请将localhost更换成服务器IP）:

RTMP (by VLC): rtmp://localhost/live/livestream
H5(HTTP-FLV): http://localhost:8080/live/livestream.flv
H5(HLS): http://localhost:8080/live/livestream.m3u8