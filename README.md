kafka的docker-compose一键部署
修改docker-compose文件中的kafka的环境
    environment:
        - KAFKA_ADVERTISED_LISTENERS=INTERNAL://127.0.0.1:9093,CLIENT://106.13.216.62:9092
修改106.13.216.62为本机外网ip

保存后，在docker-compose.yml下执行
docker-compose up -d  一键启动kafka