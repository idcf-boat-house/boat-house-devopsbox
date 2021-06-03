# IDCF Boathouse DevOpsBox 单机版DevOps工具链环境

单机版DevOps工具链环境，适合于开发者进行DevOps实践学习，开发，测试和实验。

为了加速jenkins的安装过程，请从 Boathouse 网盘资源上下载插件 zip 包并解压至 /jenkins/jenkins_home/plugin 目录中
完成以后操作后 jenkins 启动时就不再需要单独下载插件，避免因为网络问题引起的安装失败

启动方式

```shell
cd gitea
docker-comopse up -d

cd wekan
docker-compose up -d

cd jenkins
docker-compose up -d
```