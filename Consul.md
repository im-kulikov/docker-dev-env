# Настраиваем Consul:

```bash
docker run --restart always \
           --name consul \
            -d \
            -p 8301-8302:8301-8302 \
            -p 8400:8400 \
            -p 8500:8500 \
            -p 8600:8600 \
        consul:latest
```