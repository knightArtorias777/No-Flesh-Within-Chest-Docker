FROM openjdk:17-alpine

# 定义环境变量
RUN mkdir /server

#把当前文件夹下的所有文件复制到/server目录下
COPY ./ /server

# 工作目录设置为 /server
WORKDIR /server

# 设置启动脚本的权限，以便可以执行
RUN chmod +x run.sh

# 开放 Minecraft 服务器默认端口
EXPOSE 25565 25575 

# 设置容器启动时执行的命令 会失败
ENTRYPOINT ["./run.sh"]

