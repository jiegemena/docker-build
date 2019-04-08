# docker jenkins 搭建


## 1、 docker 命令

```
docker run -v /etc/localtime:/etc/timezone:rw -v /etc/localtime:/etc/localtime:rw --name jenkins -d -p 10080:8080 docker.io/jenkins/jenkins
```

## 2、 复制密码出主机，激活系统

```
docker cp  jenkins:/var/jenkins_home/secrets/initialAdminPassword /home/initialAdminPassword
cat /home/initialAdminPassword
```

## 3、 访问网站
- http://localhost:10080
