# Supported tags and respective `Dockerfile` links

-	[`1.5.4`, `1.5` (*1.5/Dockerfile*)](https://github.com/docker-library/golang/blob/d7e2a8d90a9b8f5dfd5bcd428e0c33b68c40cc19/1.5/Dockerfile)
-	[`1.5.4-onbuild`, `1.5-onbuild` (*1.5/onbuild/Dockerfile*)](https://github.com/docker-library/golang/blob/f1f65c0ab0097a5e3d079d5a74e2468e8d47563d/1.5/onbuild/Dockerfile)
-	[`1.5.4-wheezy`, `1.5-wheezy` (*1.5/wheezy/Dockerfile*)](https://github.com/docker-library/golang/blob/d7e2a8d90a9b8f5dfd5bcd428e0c33b68c40cc19/1.5/wheezy/Dockerfile)
-	[`1.5.4-alpine`, `1.5-alpine` (*1.5/alpine/Dockerfile*)](https://github.com/docker-library/golang/blob/f3768925fd0ebeb966c30bc64206b0e6020de66e/1.5/alpine/Dockerfile)
-	[`1.6.2`, `1.6`, `1`, `latest` (*1.6/Dockerfile*)](https://github.com/docker-library/golang/blob/0ce80411b9f41e9c3a21fc0a1bffba6ae761825a/1.6/Dockerfile)
-	[`1.6.2-onbuild`, `1.6-onbuild`, `1-onbuild`, `onbuild` (*1.6/onbuild/Dockerfile*)](https://github.com/docker-library/golang/blob/ce284e14cdee73fbaa8fb680011a812f272eae2e/1.6/onbuild/Dockerfile)
-	[`1.6.2-wheezy`, `1.6-wheezy`, `1-wheezy`, `wheezy` (*1.6/wheezy/Dockerfile*)](https://github.com/docker-library/golang/blob/0ce80411b9f41e9c3a21fc0a1bffba6ae761825a/1.6/wheezy/Dockerfile)
-	[`1.6.2-alpine`, `1.6-alpine`, `1-alpine`, `alpine` (*1.6/alpine/Dockerfile*)](https://github.com/docker-library/golang/blob/f3768925fd0ebeb966c30bc64206b0e6020de66e/1.6/alpine/Dockerfile)
-	[`1.7beta2`, `1.7` (*1.7/Dockerfile*)](https://github.com/docker-library/golang/blob/13b4447729b4367396148cc18745c9901e5fe4a8/1.7/Dockerfile)
-	[`1.7beta2-onbuild`, `1.7-onbuild` (*1.7/onbuild/Dockerfile*)](https://github.com/docker-library/golang/blob/2372c8cafe9cc958bade33ad0b8b54de8869c21f/1.7/onbuild/Dockerfile)
-	[`1.7beta2-wheezy`, `1.7-wheezy` (*1.7/wheezy/Dockerfile*)](https://github.com/docker-library/golang/blob/13b4447729b4367396148cc18745c9901e5fe4a8/1.7/wheezy/Dockerfile)
-	[`1.7beta2-alpine`, `1.7-alpine` (*1.7/alpine/Dockerfile*)](https://github.com/docker-library/golang/blob/13b4447729b4367396148cc18745c9901e5fe4a8/1.7/alpine/Dockerfile)

[![](https://badge.imagelayers.io/golang:latest.svg)](https://imagelayers.io/?images=golang:1.5.4,golang:1.5.4-onbuild,golang:1.5.4-wheezy,golang:1.5.4-alpine,golang:1.6.2,golang:1.6.2-onbuild,golang:1.6.2-wheezy,golang:1.6.2-alpine,golang:1.7beta2,golang:1.7beta2-onbuild,golang:1.7beta2-wheezy,golang:1.7beta2-alpine)

For more information about this image and its history, please see [the relevant manifest file (`library/golang`)](https://github.com/docker-library/official-images/blob/master/library/golang). This image is updated via [pull requests to the `docker-library/official-images` GitHub repo](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Fgolang).

For detailed information about the virtual/transfer sizes and individual layers of each of the above supported tags, please see [the `golang/tag-details.md` file](https://github.com/docker-library/docs/blob/master/golang/tag-details.md) in [the `docker-library/docs` GitHub repo](https://github.com/docker-library/docs).

# What is Go?

Go (a.k.a., Golang) is a programming language first developed at Google. It is a statically-typed language with syntax loosely derived from C, but with additional features such as garbage collection, type safety, some dynamic-typing capabilities, additional built-in types (e.g., variable-length arrays and key-value maps), and a large standard library.

> [wikipedia.org/wiki/Go_(programming_language)](http://en.wikipedia.org/wiki/Go_%28programming_language%29)

![logo](https://raw.githubusercontent.com/docker-library/docs/01c12653951b2fe592c1f93a13b4e289ada0e3a1/golang/logo.png)

# How to use this image

## Start a Go instance in your app

The most straightforward way to use this image is to use a Go container as both the build and runtime environment. In your `Dockerfile`, writing something along the lines of the following will compile and run your project:

```dockerfile
FROM golang:1.6-onbuild
```

This image includes multiple `ONBUILD` triggers which should cover most applications. The build will `COPY . /go/src/app`, `RUN go get -d -v`, and `RUN go install -v`.

This image also includes the `CMD ["app"]` instruction which is the default command when running the image without arguments.

You can then build and run the Docker image:

```console
$ docker build -t my-golang-app .
$ docker run -it --rm --name my-running-app my-golang-app
```

*Note:* the default command in `golang:onbuild` is actually `go-wrapper run`, which includes `set -x` so the binary name is printed to stderr on application startup. If this behavior is undesirable, then adding `CMD ["app"]` (or `CMD ["myapp"]` if a [Go custom import path](https://golang.org/s/go14customimport) is in use) will silence it by running the built binary directly.

## Compile your app inside the Docker container

There may be occasions where it is not appropriate to run your app inside a container. To compile, but not run your app inside the Docker instance, you can write something like:

```console
$ docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.6 go build -v
```

This will add your current directory as a volume to the container, set the working directory to the volume, and run the command `go build` which will tell go to compile the project in the working directory and output the executable to `myapp`. Alternatively, if you have a `Makefile`, you can run the `make` command inside your container.

```console
$ docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.6 bash -c make
```

## Cross-compile your app inside the Docker container

If you need to compile your application for a platform other than `linux/amd64` (such as `windows/386`):

```console
$ docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp -e GOOS=windows -e GOARCH=386 golang:1.6 go build -v
```

Alternatively, you can build for multiple platforms at once:

```console
$ docker run --rm -it -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.6 bash
$ for GOOS in darwin linux; do
>   for GOARCH in 386 amd64; do
>     go build -v -o myapp-$GOOS-$GOARCH
>   done
> done
```

# License

View [license information](http://golang.org/LICENSE) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.11.2.

Support for older versions (down to 1.6) is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.

# User Feedback

## Documentation

Documentation for this image is stored in the [`golang/` directory](https://github.com/docker-library/docs/tree/master/golang) of the [`docker-library/docs` GitHub repo](https://github.com/docker-library/docs). Be sure to familiarize yourself with the [repository's `README.md` file](https://github.com/docker-library/docs/blob/master/README.md) before attempting a pull request.

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/docker-library/golang/issues). If the issue is related to a CVE, please check for [a `cve-tracker` issue on the `official-images` repository first](https://github.com/docker-library/official-images/issues?q=label%3Acve-tracker).

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode](https://freenode.net).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/docker-library/golang/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
