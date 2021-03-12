# Development inside a Docker container with Visual Studio Code

```bash

# you must be in the .devcontainer directory to execute the commands
cd .devcontainer

# build the image for the development container
docker build --force-rm --tag tec-radar/dev:1 .

# create the development container   *** in Windows:  source="path", the full path *** in Mac&Linux source="$(pwd)"/.., 
docker create --name tec-radar_dev --publish 8080:8080 --mount  type=bind,source="$(pwd)"/..,target=/workspace tec-radar/dev:1

# start/stop
docker start tec-radar_dev
docker stop tec-radar_dev
```
# remove container
docker rm tec-radar_dev
