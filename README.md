# gnuguix-docker
Dockerfile for GNU Guix


https://hub.docker.com/r/zaoqi/guix

GNU Guix requires `--privileged` to run.

```
docker run -it --rm --privileged zaoqi/guix
# (inside Docker)
guix pull
```

[Guix pull](https://www.gnu.org/software/guix/manual/html_node/Invoking-guix-pull.html) takes a while and [cannot be added to the Dockerfile](https://github.com/docker/docker/issues/1916) since it requires ```--privileged```. 

However, you can fetch a Docker image built by Gitlab CI with this step performed.

Dockerfile: https://gitlab.com/zaoqi/gnu-guix-docker

Docker hub: [zaoqi0gitlab0ci/guix](https://hub.docker.com/r/zaoqi0gitlab0ci/guix)
