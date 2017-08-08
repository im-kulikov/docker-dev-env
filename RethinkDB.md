# Настраиваем RethinkDB:

```bash
docker run --restart always \
           --name rethink \
            -d \
            -h `'rethink-master'` \
            -p 9080:8080 \
            -p 28015:28015 \
            -p 29015:29015 \
            -v /Users/kulikov/projects/Services/rethink:/data \
        rethinkdb
```

# Cluster:

```yml
version: '2'
services:
  rdb1:
    image: rethinkdb
    restart: always
    ports:
      - "9080:8080"
      - "28015:28015"
      - "29015:29015"
    volumes:
      - /Users/kulikov/projects/Services/rethink:/data
    command: rethinkdb --bind all
  rdb2:
    image: rethinkdb
    restart: always
    depends_on:
      - rdb1
    command: rethinkdb --join rdb1:29015
  ...
  rdbN:
    image: rethinkdb
    restart: always
    depends_on:
      - rdb1
    command: rethinkdb --join rdb1:29015
```
