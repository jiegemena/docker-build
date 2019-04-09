
```
docker run -p 6379:6379 -v /home/apps/redis/redis.windows.conf:/usr/local/etc/redis/redis.conf -d --restart always --name myredis  redis redis-server /usr/local/etc/redis/redis.conf

```


- 连接密码 

redis123
