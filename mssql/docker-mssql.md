```
 docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=asdf@#123' -v /home/jieguone/data/sql/:/var/opt/mssql/data/data1/ -p 1433:1433 --name sql2 --restart always -d microsoft/mssql-server-linux


```
