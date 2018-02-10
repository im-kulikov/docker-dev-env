# Setup MongoDB:

```bash
docker run --restart always \
           --name mongodb \
            -d \
            -p 27017:27017 \
            -p 28017:28017 \
            -v /Users/kulikov/projects/Services/mongodb:/data/db \
        mvertes/alpine-mongo
```