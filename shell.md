## 后台启动容器

方案一
docker run -d <image_name> tail -f /dev/null

方案二
docker run -i -t <image_name> [command]

然后Ctrl+P+Q即可退出控制台，但是容器没有退出，可使用命令查看：
docker ps

example:
docker run -i -t centos /bin/bash