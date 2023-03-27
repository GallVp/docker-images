# docker-images

## Build commands

```bash
docker buildx build -f Dockerfile -t gallvp/repo:tag --platform linux/amd64,linux/arm64 --push .
```

To setup buildx, do

```bash
docker buildx create --name multiarch
docker buildx use multiarch && docker buildx inspect --bootstrap
```
