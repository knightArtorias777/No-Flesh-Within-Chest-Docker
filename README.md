# No-Flesh-Within-Chest-Docker
脆骨症整合包服务器端docker快速部署参考方案


## linux云服务器部署方案

### 1. 拉取image
    #国内镜像源
    docker pull registry.cn-beijing.aliyuncs.com/object_mikufans/object_gumi:v1
    
    #dockerhub镜像源
    docker pull mikufans029/cgzserver:v0.1


### 2. 创建备份映射文件

    mkdir home/mc

### 3. 如果有服务器存档可以放在home/mc文件夹内
    注意:world内部文件放入即可 

### 4. 快速部署
    #docker 使用镜像快速部署命令

    #linux 部署指令 
    docker run -d  -v /home/mc:/server/world  \
    -p 25565:25565 \
    -p 25575:25575 \
    --name mc-server mikufans029/cgzserver:v0.1
