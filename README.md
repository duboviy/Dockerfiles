# Dockerfiles
Dockerfiles I use. These are all automated builds (with Docker hub usage).

To build an image with docker run in directory with Dockerfile:
```bash
docker build -t <your_image_name_for_example_gcc> .
```
Then to run that image and attach to it at the same time:
```bash
docker run -i -t vagrant
```
Or to run it in the background:
```bash
docker run -d -t vagrant
```

### To remove all images and containers:
You use Docker, but working with it created lots of images and containers. You want to remove all of them to save disk space.

```
Warning: This will destroy all your images and containers. It will not be possible to restore them!
```

Execute those commands in a shell:

```bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
```