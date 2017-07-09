# Настраиваем RethinkDB:

```bash
docker run --restart always \
           --name rethink \
            -d \
            -p 9080:8080 \
            -p 28015:28015 \
            -p 29015:29015 \
            -v /Users/kulikov/projects/Services/rethink:/data \
        rethinkdb
```