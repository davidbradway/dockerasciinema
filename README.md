# ASCIINEMA via Docker Python 3 Alpine pip install

## Build new image from DOCKERFILE

- give it a tag 

```bash
docker build -t asciinema .  # Create image using this directory's Dockerfile
```

## Run container

- Remove container when it finishes
- Run interactive, tty mode
- Run default or other command
- Optionally, provide arguments

```bash
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema rec local.cast
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema play local.cast
docker run --rm -ti --mount src="$(pwd)",target=/app,type=bind asciinema asciinema upload local.cast
```

# more info

https://github.com/asciinema/asciinema
