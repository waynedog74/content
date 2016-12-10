Title: How to delete Docker cache?
Date: 12-10-2016 13:00
Category: devops
Tags: docker
Authors: sedlav

Q. How to delete Docker cache?

A. Last time I checked, there wasn't a specific docker command for this

I use a few useful alias:

```bash
alias docker_clean_images='docker rmi $(docker images -a --filter=dangling=true -q)'
alias docker_clean_ps='docker rm $(docker ps --filter=status=exited --filter=status=created -q)'
```

[Link](https://forums.docker.com/t/how-to-delete-cache/5753/2)
