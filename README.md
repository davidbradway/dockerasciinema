# asciinema via a Docker Python 3 Alpine image 

## Build new image from DOCKERFILE

- give it a tag 

```bash
docker build -t asciinema .  # Create image using this directory's Dockerfile
```

## Run container

- Remove container when it finishes
- Run interactive, tty mode
- Mount pwd to app to save files
- Record, Play, and Upload commands

```bash
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema rec local.cast
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema play local.cast
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema upload local.cast
```

## More info

https://github.com/asciinema/asciinema
