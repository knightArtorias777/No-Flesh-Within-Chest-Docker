# No-Flesh-Within-Chest-Docker
脆骨症整合包服务器端docker快速部署参考方案

整合包作者原地址 https://github.com/Yorunina/No-Flesh-Within-Chest

## linux云服务器部署方案

### 1. 拉取image  
    #dockerhub镜像源
    docker pull mikufans029/cgzserver:v0.1


### 2. 创建备份映射文件

    mkdir home/mc

### 3. 如果有服务器存档可以放在home/mc文件夹内
    注意:world内部文件放入即可 

### 4. 快速部署
    #docker 使用镜像快速部署命令

    #linux 运行指令 
    docker run -d  -v /home/mc:/server/world  \
    -p 25565:25565 \
    -p 25575:25575 \
    --name mc-server mikufans029/cgzserver:v0.1


## 其他
### 1. 如果你想更改服务器配置相关的 可以使用指令进入容器
    docker exec -it mc-server sh

### 2. 控制台
    内部使用rcon作为控制台手段 建议使用rcon工具连接服务器25575端口使用
