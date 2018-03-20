# docker部署步骤
# 1: 搭建centos系统ruby环境镜像
   ```
     cd images/base
     docker build -t base/centos
   ``` 
# 2: 构建项目镜像 
  ```
  cd images/fuxiong
   docker build -t fuxiong/api
  ```
# 3:  构建elasticsearch镜像
   ```
   cd images/elasticsearch
    docker build -t elasticsearch/fuxiong
   ```
# 启动服务    
~/docker-compose up -d    
