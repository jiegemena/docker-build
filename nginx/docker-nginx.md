构建命令
```
mkdir /home/apps/jslogsnginx
chmod 777 /home/apps/jslogsnginx
docker run --name tmp-nginx-container -d nginx
docker cp tmp-nginx-container:/etc/nginx/ /home/apps/jslogsnginx/
docker rm -f tmp-nginx-container
docker run -p 80:80 --name jslogsnginx -v /home/apps/jslogsnginx/nginx:/etc/nginx --restart=always -d nginx
```


### 删除命令
```
docker stop jslogsnginx
docker rm jslogsnginx
```
