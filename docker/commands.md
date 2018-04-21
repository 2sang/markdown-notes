Docker commands and aliases explained
======================================
Brief version of [docker official documentation](https://docs.docker.com/engine/reference/commandline/cli/)

### My aliases
Check out example aliases at [My docker aliases](https://github.com/2sang/dotfiles/blob/master/.dockerrc)
```bash
# Basic aliases
da - docker attach

# Container status check:
dps - docker ps
dl - docker ps --latest --quite(only display numeric id)
dpa - docker ps -a (include stopped container)
dip - docker inspect --format '{{ .NetworkSettings.IPAddress }}'

# docker 
di - docker images

```


Commands
--------

**Dive into a bash shell** of currently running container:
```bash
docker exec -i -t <container-id> /bin/bash
# Or
dex <container-id> /bin/bash
```

**Commit changes** of container to its base image:
```bash
docker commit
```




How to commit 
