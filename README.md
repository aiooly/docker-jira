# build jira docker image


### 这是一个用于构建JIRA image的工程（已经破解了）

可以拉取公共的images

```
docker pull daocloud.io/marcus_li/docker-jira:latest
```

### 启动数据库
```
docker run --name mysql -p 3306:3306 -v LOCAL_PATH/mysqldata:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -idt mysql:5.7 
```
创建jira_db

```
create database jira_db character set utf8 collate utf8_bin;
```

### 启动JIRA 

```
docker run --name jira -p 8080:8080 daocloud.io/marcus_li/docker-jira:latest
```

访问 http://localhost:8080 选择手动配置，配置本地数据库，生成使用秘钥（官方秘钥）


![](https://kekekeke.sh1a.qingstor.com/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20180528150248.png)
