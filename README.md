# IDCF Boathouse DevOpsBox 单机版DevOps工具链环境

单机版DevOps工具链环境，适合于开发者进行DevOps实践学习，开发，测试和实验。

重要说明：为了加速jenkins的安装过程，请从 Boathouse 网盘资源上下载插件 zip 包并解压至 /jenkins/jenkins_home/plugin 目录中
完成以后操作后 jenkins 启动时就不再需要单独下载插件，避免因为网络问题引起的安装失败

相信文档请参考：[IDCF Boathouse DevOps 实战训练营文档](http://idcf.org.cn/boat-house/#/)

复制完成后，运行以下命令即可启动 DevOpsBox 环境，注意docker-compose都需要先进入各个工具的子目录后执行

```shell
## 启动 gitea
cd devopsbox/gitea
docker-compose up -d

## 启动 wekan
cd devopsbox/wekan
docker-compose up -d

## 启动 jenkins
### 首先修正jenkins_home目录权限
cd devopsbox/jenkins
sudo chown -R 1000:1000 jenkins_home
docker-compose up -d
```

以上启动完成后，通过以下地址就可以访问环境

- 开源电子看板 wekan http://192.168.99.102:8081
- 开源Git服务器 Gitea http://192.168.99.102:3000
- 开源流水线 Jenkins http://192.168.99.102:8080

