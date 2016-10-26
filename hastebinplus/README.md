## Build image :

```
docker build -t <yourname/imagename> .
```

## Run container from image :

```
docker run -p 8080:8080 -v /var/docker/hastebin/data:/opt/haste/data --name hastebin <yourname/imagename>
```

## Notes:

Difference between the two Dockerfiles is their base image.
The one using Debian Jessie that yields a 413.8 MB image while the other one
using Alpine Linux that yields a 48.82 MB image.
