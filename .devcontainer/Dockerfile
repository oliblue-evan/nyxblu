# 在 docker-compose.yml 中更新 NODE_VERSION 参数以选择 Node 版本: 18, 16, 14
ARG NODE_VERSION=16
FROM mcr.microsoft.com/devcontainers/javascript-node:${NODE_VERSION}

# VARIANT 可以是 'hugo'（标准版）或 'hugo_extended'（扩展版）
ARG VARIANT=hugo
# VERSION 可以是 'latest'（最新版）或特定版本号
ARG VERSION=latest

# 下载 Hugo
RUN apt-get update && apt-get install -y ca-certificates openssl git curl && \
    rm -rf /var/lib/apt/lists/* && \
    case ${VERSION} in \
    latest) \
    export VERSION=$(curl -s https://api.github.com/repos/gohugoio/hugo/releases/latest | grep "tag_name" | awk '{print substr($2, 3, length($2)-4)}') ;;\
    esac && \
    echo ${VERSION} && \
    case $(uname -m) in \
    aarch64) \
    export ARCH=ARM64 ;; \
    *) \
    export ARCH=64bit ;; \
    esac && \
    echo ${ARCH} && \
    wget -O ${VERSION}.tar.gz https://github.com/gohugoio/hugo/releases/download/v${VERSION}/${VARIANT}_${VERSION}_Linux-${ARCH}.tar.gz && \
    tar xf ${VERSION}.tar.gz && \
    mv hugo /usr/bin/hugo

# Hugo 开发服务器端口
EXPOSE 1313

# [可选] 取消注释此部分以安装您可能需要的其他操作系统包
#
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [可选] 如果要安装更多全局 node 包，请取消注释
# RUN sudo -u node npm install -g <your-package-list-here>
