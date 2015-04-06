# 说明

> 采用 wushuyi/centos7-python 为基础镜像

> 运行 shadowsocks 服务器

##使用方法：

> 例子：

> docker run -d -p -t -i -p 5002:3000 wushuyi/centos7-shadowsocks -s 0.0.0.0 -p 3000 -k yourpasswd -m aes-256-cfb
