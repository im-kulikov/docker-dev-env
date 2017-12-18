# Настраиваем LicenseServer:

```bash
docker run --restart always \
           --name license-server \
            -d \
            -p 10086:10086 \
        imkulikov/license-server
```