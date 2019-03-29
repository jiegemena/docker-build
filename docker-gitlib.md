# docker gitlib 搭建

## 1、docker 命令构建

```
sudo docker run -v /etc/localtime:/etc/timezone:rw -v /etc/localtime:/etc/localtime:rw -d -p 8443:443 -p 8081:8081 -p 8022:22 --name gitlab --restart always --volume /home/gitlab/config:/etc/gitlab --volume /home/gitlab/logs:/var/log/gitlab --volume /home/gitlab/data:/var/opt/gitlab gitlab/gitlab-ce:latest
```

## 2、访问并测试 
1. 首次启动比较慢（等待十分钟），
2. 然后在对应http://xxx.xxx.xxx:8081 链接中访问到页面。
3. 初次使用时，需要我们创建默认的管理员密码。当登录之后，
4. 创建项目 bug，
> 在项目clone的路径中，本来应该是:8081的地方，变成了主机名。

## 3、修改配置(修复bug) 

> 修改external_url   
>```
>sudo docker exec -it gitlab /bin/bash
>vim /etc/gitlab/gitlab.rb
>```
> vim 查找命令  /external_url   
>修改external_url为   
>external_url "http://xxx.xxx.xxx:8081"

## 4、重新构建镜像

```
sudo docker stop gitlab
sudo docker rm gitlab
sudo docker run -v /etc/localtime:/etc/timezone:rw -v /etc/localtime:/etc/localtime:rw -d -p 8443:443 -p 8081:8081 -p 8022:22 --name gitlab --restart always --volume /home/xinfu189/gitlab/config:/etc/gitlab --volume /home/xinfu189/gitlab/logs:/var/log/gitlab --volume /home/xinfu189/gitlab/data:/var/opt/gitlab gitlab/gitlab-ce:latest
```

## 5、进入网站
