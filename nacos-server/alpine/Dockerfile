FROM openjdk:8-jre-alpine

ENV NACOS_SERVER_VERSION 0.9.0

# -f 连接失败不显示错误
# -s 不显示错误
# -S 显示错误
# -L 跟随链接重定向
# -o 保存为命令行中文件名
# -O 保存为链接中文件名，链接末尾必须包含文件名
#RUN curl -fSL https://github.com/alibaba/nacos/releases/download/$NACOS_SERVER_VERSION/nacos-server-$NACOS_SERVER_VERSION.tar.gz -o nginx.tar.gz

# -O 指定文件名
RUN wget -O nacos.tar.gz https://github.com/alibaba/nacos/releases/download/$NACOS_SERVER_VERSION/nacos-server-$NACOS_SERVER_VERSION.tar.gz

# -x 解压
# -z gzip
# -v 显示进程
# -f 必须参数
RUN tar -xvf nacos.tar.gz

EXPOSE 8848

ENTRYPOINT sh nacos/bin/startup.sh -m standalone