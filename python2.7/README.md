# Installation

Image is based on Alpine Linux for purpose of being as small as possible (less than 60MB).

## Build image :

```
docker build -t <yourname/imagename> .
```

## Run python interpreter :

```
docker run --rm -it <yourname/imagename>
```

## Run python script :

```
docker run --rm -it -v `pwd`:/var/python -w /var/python <yourname/imagename> python your_script.py
```
