```
 docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=asdf@#123' -v /home/jieguone/data/sql/:/var/opt/mssql/data/data1/ -p 1433:1433 --name sql2 --restart always -d microsoft/mssql-server-linux


```
```
docker exec -it sql2 "bash"

root@sql2:/# /opt/mssql/bin/mssql-conf set sqlagent.enabled true 
SQL Server needs to be restarted in order to apply this setting. Please run
'systemctl restart mssql-server.service'.
root@sql2:/# exit
exit
[root@localhost ~]# 
[root@localhost ~]# docker stop sql1
sql1
[root@localhost ~]# docker start sql1
sql1

```
