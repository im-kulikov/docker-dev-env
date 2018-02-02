# Настраиваем RabbitMQ:

```bash
docker run --restart always \
           --name amq \
            -d \
            -p 4369:4369 \
            -p 5671:5671 \
            -p 5672:5672 \
            -p 25672:25672 \
        rabbitmq:alpine
```