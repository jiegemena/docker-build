```
mkdir /home/apps/mysqldata
cd /home/apps/mysqldata
docker run -p 3306:3306 --restart always --name mymysql -v /etc/localtime:/etc/timezone:rw -v /etc/localtime:/etc/localtime:rw -e MYSQL_ROOT_PASSWORD=asdf@#123 -d  mysql:5.6 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci

docker stop mymysql
dcoker rm mymysql

```
