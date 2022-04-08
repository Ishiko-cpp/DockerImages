# Upload Instructions

```
docker build --no-cache .
docker tag <id> ishiko/alpine-ishiko-cpp-build-prerequisites:latest
docker tag <id> ishiko/alpine-ishiko-cpp-build-prerequisites:<version>
docker login
docker push ishiko/alpine-ishiko-cpp-build-prerequisites:latest
docker push ishiko/alpine-ishiko-cpp-build-prerequisites:<version>
```
