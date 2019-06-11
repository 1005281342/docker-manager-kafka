# docker-manager-kafka

https://blog.51cto.com/536410/2322056


### kafka

- `COMPOSE_PROJECT_NAME=kafkatest docker-compose -f kafka.yml up -d`

- 查看进程情况`docker ps`

### manager
- `docker-compose -f kafka-manager.yml up -d`
- docker启动后，登陆到docker容器里 `docker exec -it 容器ID bash`
- `vi conf/application.conf` 将后面一条注释掉，然后将zk的地址写入
  ```text
    kafka-manager.zkhosts="zoo1:2181,zoo2:2182,zoo3:2183"
    #kafka-manager.zkhosts=${?ZK_HOSTS}
  ```