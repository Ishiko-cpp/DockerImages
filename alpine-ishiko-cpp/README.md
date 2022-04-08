# Upload Instructions

```
docker build --no-cache .
docker tag <id> ishiko/alpine-ishiko-cpp:latest
docker tag <id> ishiko/alpine-ishiko-cpp:<version>
docker login
docker push ishiko/alpine-ishiko-cpp:latest
docker push ishiko/alpine-ishiko-cpp:<version>
```
