# srs ����
[�ĵ���Դ](https://ossrs.io/lts/zh-cn/docs/v5/doc/getting-started-build)
## Live Streaming
ֱ����SRS�ĵ��ͳ�����֧����ֱ��������ֹۿ���ʽ��

����Դ�룬�Ƽ���Ubuntu20��
```shell
git clone -b develop https://gitee.com/ossrs/srs.git
```
���룬ע����Ҫ�л���srs/trunkĿ¼��
```shell
cd srs/trunk
./configure
make
```
������������
```shell
./objs/srs -c conf/srs.conf
```
���SRS�Ƿ�ɹ����������Դ� http://localhost:8080/ ������ִ�����

# �鿴SRS��״̬
```shell
./etc/init.d/srs status
```

# ���߿�SRS����־
```shell
tail -n 30 -f ./objs/srs.log

```
���磬�����������ʾSRS�������У�
```shell
MB0:trunk $ ./etc/init.d/srs status
SRS(pid 90408) is running.                                 [  OK  ]

MB0:trunk $ tail -n 30 -f ./objs/srs.log
[2021-08-13 10:30:36.634][Trace][90408][12c97232] Hybrid cpu=0.00%,0MB, cid=1,1, timer=61,0,0, clock=0,22,25,0,0,0,0,1,0

```
ʹ�� FFmpeg(�������) �� OBS(�������) ������
```
ffmpeg -re -i ./doc/source.flv -c copy -f flv rtmp://localhost/live/livestream
```
Note: ʵ���ļ�./doc/source.flv��SRS��Դ����Ŀ¼���С�

�������ҳ�沥��������SRS���ڱ������뽫localhost�����ɷ�����IP��:

RTMP (by VLC): rtmp://localhost/live/livestream
H5(HTTP-FLV): http://localhost:8080/live/livestream.flv
H5(HLS): http://localhost:8080/live/livestream.m3u8