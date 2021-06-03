# IDCF Boathouse DevOpsBox 单机版DevOps工具链环境

单机版DevOps工具链环境，适合于开发者进行DevOps实践学习，开发，测试和实验。

重要说明：为了加速jenkins的安装过程，请从 Boathouse 网盘资源上下载插件 zip 包并解压至 /jenkins/jenkins_home/plugin 目录中
完成以后操作后 jenkins 启动时就不再需要单独下载插件，避免因为网络问题引起的安装失败

相信文档请参考：[IDCF Boathouse DevOps 实战训练营文档](http://idcf.org.cn/boat-house/#/)

启动方式

```shell
cd boat-house-devopsbox
## 启动 gitea
docker-compose -f devopsbox/gitea/docker-compose.yml up -d
## 启动 wekan
docker-compose -f devopsbox/wekan/docker-compose.yml up -d
## 启动 jenkins
### 首先修正jenkins_home目录权限
sudo chown -R 1000:1000 devopsbox/jenkins/jenkins_home
docker-compose -f devopsbox/jenkins/docker-compose.yml up -d
```