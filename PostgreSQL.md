# Настраиваем PostgreSQL:

```bash
docker run --restart always \
           --name postgres \
            -d \
            -p 5432:5432 \
            -e POSTGRES_PASSWORD=postgres \
            -v /Users/kulikov/projects/Services/postgres:/var/lib/postgresql/data \
        postgres:alpine
```