# Setup Redis:

```bash
docker run --restart always \
           --name redis \
            -d \
            -p 6379:6379 \
            -v /Users/kulikov/projects/Services/redis:/data \
        redis:alpine
```