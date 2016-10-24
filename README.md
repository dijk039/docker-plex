# docker plex
Dockerfile to set up a Plex Media Server

## Instructions
### Getting the docker image
Build from docker file

```
git clone git@github.com:dijk039/docker-plex.git
cd docker-plex
docker build -t dijk039/plex .
```

You can also obtain it via:

```
docker pull dijk039/plex
```

### Running the docker image
Instructions to run:

```
docker stop plex && docker rm plex
docker run --restart=always -d --name plex -h *your_host_name* -v /*your_config_location*:/config -v /*your_videos_location*:/data -p 32400:32400 dijk039/plex
```
