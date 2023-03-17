# 使用CentOS 7作为基础镜像
FROM centos:7

# 安装必要的工具和依赖
RUN yum -y update && \
    yum -y install curl git && \
    yum clean all

# 下载并安装Go 1.18
ENV GOLANG_VERSION 1.18
RUN curl -sSL https://golang.org/dl/go${GOLANG_VERSION}.linux-amd64.tar.gz | tar -C /usr/local -xz

# 设置环境变量
ENV PATH $PATH:/usr/local/go/bin
ENV GOPATH /go
ENV GOBIN $GOPATH/bin

# 验证Go是否正确安装
RUN go version
