# centos4/i386 docker images.

野暮用でcentos4/i386のdocker imageが必要になった

dockerhubにも、centos4のイメージはあるが、作り方が若干不明瞭なため、採用しづらいので、作ることになった。

## build environment

- ubuntu yakkety
- docker 1.12.3

``` bash
# git clone https://github.com/docker/docker.git
# apt-get install rinse rpm rpm2cpio yum docker.io
# systemctl start docker
# cd docker/contrib
#### copy mkimage-yum.sh from this repository ####
#### copy docker-yum.conf from this repository ####
# ./mkimage-yum.sh -y docker-yum.conf -g "Core Base" centos4
```

## 参考

- http://qiita.com/udzura/items/e528fec48fa606750fff
- http://projects.tsuntsun.net/~nabeken/diary/Sysadmin/creating-centos5-ami-on-amazon-linux-1.html
- http://tatsushid.github.io/blog/2014/10/how-to-build-centos3-docker-image/

```
# git log --oneline ./mkimage-yum.sh | head -1
fa255c9 Add errexit to mkimage-yum.sh
```

