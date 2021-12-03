# Example python docker application

This is an example application using the [Docker docs for python](https://docs.docker.com/language/python/) to build a Docker image and run it locally inside a container. 

## Prerequisites

- Python version 3.8 or later. You can download Python [here](https://www.python.org/downloads/), although I recommend using [pyenv](https://formulae.brew.sh/formula/pyenv) to install the python version that you need.
- Docker running locally. You can install Docker Desktop [here](https://www.docker.com/products/docker-desktop).
- An IDE or a text editor to edit files.

## How to get application running locally

- Build an image for the python application:
```bash
docker build --tag python-docker .
```

- Run the image in a container:
```bash
docker run --publish 5000:5000 python-docker
```

- You can then see that the server is up and running by executing the command (and you should receive 'Hello World!'):
```bash
curl localhost:5000
```