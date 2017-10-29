# Настраиваем TiDB:

```bash
docker run --restart always \
           --name tidb \
            -d \
            -p 3306:4000 \
        imkulikov/tidb:v1.0.0 \
        -path /db \
        -store boltdb
```