## Movie Picker from IMDB using Python Docker

- Mini project to learn the basics of docker
- `main.py` taken from [patrickloeber/python-fun](https://github.com/patrickloeber/python-fun/blob/master/moviepicker/main.py)

### Usage

- Build with `docker build -t docker-movie-picker .`
- Run with `docker run docker-movie-picker`

### Some issues that came up

- "Docker: Got permission denied...". To solve this we just need to add the non-root user to the docker group with:

```
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ newgrp docker
```

