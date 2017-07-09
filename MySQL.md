# Настраиваем MySQL:

```bash
docker run --restart always \
           --name mysql \
            -d \
            -p 3306:3306 \
            -e MYSQL_ALLOW_EMPTY_PASSWORD=yes \
            -v /Users/kulikov/projects/Services/mysql:/var/lib/mysql \
        mariadb
```