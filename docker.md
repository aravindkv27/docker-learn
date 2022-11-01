# Docker

## Image

The image is the blueprint of the container and the container is created from it.

## Container

Container is an instance of the image. Which simulates the required environment with the use of the Linux kernel packaged in it.

## Docker Ecosystem

__Docker Registry:__

Docker maintains all the images in the registry and they can be pulled from the registry too.

__Docker Hub:__

This is the repository for all your custom-built images. Images can be pushed and accessed from the Hub

__Docker Client:__

The CLI tool used to interact with the Docker server

__Docker Daemon:__

The Docker server process responsible for pulling, pushing, and building the images. It is also used for running the container

## Docker Commands Lookup Table

![Docker Commands](/images/dc-commands.png)

## Permission Issues

```
WARNING: Error loading config file: /home/user/.docker/config.json -
stat /home/user/.docker/config.json: permission denied
```

To solve the error
```
＄ sudo groupadd docker
＄ sudo usermod -aG docker ＄USER
```