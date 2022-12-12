kafka和zookeeper高可用集群部署
的docker-compose一键部署
修改docker-compose文件中的kafka的环境
    environment:
             - KAFKA_CFG_ADVERTISED_LISTENERS=PLAINTEXT://106.13.216.62:9094

修改106.13.216.62为本机外网ip

保存后，在docker-compose.yml下执行
docker-compose up -d  一键启动kafka集群

首次运行因为数据持久化，kafka容器的挂载目录需要赋权
chmod -R 777 data