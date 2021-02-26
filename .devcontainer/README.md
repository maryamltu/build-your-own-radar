# Development inside a Docker container with Visual Studio Code

```bash
docker build --force-rm --tag tec-radar/dev:1 .

docker create --name tec-radar_dev --publish 8080:8080 --mount  type=bind,source="C:/Users/marpah/Desktop/Maryam/LTU/ML-Dev/build-your-own-radar/",target=/workspace tec-radar/dev:1

docker start tec-radar_dev
docker stop tec-radar_dev
```
docker rm tec-radar_dev
