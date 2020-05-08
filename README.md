# swarmkit-binaries
编译过后的docker/swarmkit 二进制文
通过docker编译swarmkit

1. 下载golang镜像
```docker
docker pull golang
```

2.下载swarmkit源码
```git
git clone https://github.com/docker/swarmkit.git git clone https://github.com/docker/swarmkit.git
```

3.启动编译
```docker
docker run --rm -it -v `pwd`/swarmkit:/go/src/github.com/docker/swarmkit -w /go/src/github.com/docker/swarmkit golang:latest make binaries
```
编译后的文件在swarmkit/bin中
