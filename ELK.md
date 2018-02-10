# Setup ELK-stack:

```bash
docker run --restart always \
           --name elk \
            -d \
            -p 5044:5044 \
            -p 5601:5601 \
            -p 9200:9200 \
            -v /Users/kulikov/projects/Services/elk:/var/lib/elasticsearch \
        sebp/elk
```