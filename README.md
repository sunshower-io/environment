## Environment

This project includes common scripts, base docker containers, etc.


## docker-base-build

### To build and push
```bash 
docker build -t "sunshower-base" -f docker/images/docker-base-build . && docker run -it --rm --name sunshower-base sunshower-base
docker tag "sunshower-base" sunshower/sunshower-base:$VERSION
docker push sunshower/sunshower-base:$VERSION
```

### To use
```dockerfile
FROM sunshower/sunshower-base:$VERSION
# your dockerfile (maven and gradle installed)
```

### Build Status

[![Build Status](https://semaphoreci.com/api/v1/josiahhaswell/environment/branches/frapper/badge.svg)](https://semaphoreci.com/josiahhaswell/environment)