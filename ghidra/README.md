## Dependencies

- [openjdk:jdk-slim](https://hub.docker.com/_/openjdk)

## Building image

```bash
docker build -t ghidra:9.0 .
```

## Getting Started

### Client
Starting up Ghidra

```bash
$ sudo xhost +
```

```bash
$ docker run -it --rm \
             --network none
             --name ghidra \
             -e DISPLAY=$DISPLAY \
             -v /tmp/.X11-unix:/tmp/.X11-unix
             -v /path/to/samples:/samples \
             -v /path/to/projects:/root \
             ghidra
```

## Credits

- NSA Research Directorate [https://www.ghidra-sre.org/](https://www.ghidra-sre.org/)

### License

Apache License (Version 2.0)
