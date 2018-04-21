Docker commands and aliases explained
======================================
Brief version of [docker official documentation](https://docs.docker.com/engine/reference/commandline/cli/)

Commands
--------

**Dive into a bash shell** of currently running container:
```bash
docker exec -i -t <container-id> /bin/bash
# Or
dex <container-id> /bin/bash
```

**Commit changes of container** to its base image:  
Note that the changes of container do not overwrite existing image by default.
```bash
docker commit [OPTIONS] container [repository:tag]
```

**Fetch files** from container to local filesystem, or vise versa
```bash
docker cp [OPTIONS] container:src_path dest_path
docker cp [OPTIONS] src_path container:dest_path
```



### My aliases
You can find my example aliases at [My sample docker aliases](https://github.com/2sang/dotfiles/blob/master/.dockerrc)
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





How to commit 
