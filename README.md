# Alpine GNU C library (glibc) Docker image for arm

Contains only builds for ARM, see https://github.com/frol/docker-alpine-glibc for x64 images.

This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make glibc work side by
side with musl libc (default in Apline Linux).

Uses glibc builds from https://github.com/mischnic/alpine-pkg-glibc

Download size of this image is only:

[![](https://images.microbadger.com/badges/image/mischnic/alpine-glibc-arm.svg)](http://microbadger.com/images/mischnic/alpine-glibc-arm "Get your own image badge on microbadger.com")


Usage Example
-------------

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM mischnic/alpine-glibc-arm

COPY ./my_app /usr/local/bin/my_app
```

```sh
$ docker build -t alpine-glibc-arm .
```

