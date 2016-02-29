# Supported tags and respective `Dockerfile` links

-	[`1.24.1-glibc`, `1.24-glibc`, `1-glibc`, `glibc` (*glibc/Dockerfile*)](https://github.com/docker-library/busybox/blob/1cf3ff5b2bdf332e6ecff8c4aaaa94172f693332/glibc/Dockerfile)
-	[`1.24.1-musl`, `1.24-musl`, `1-musl`, `musl` (*musl/Dockerfile*)](https://github.com/docker-library/busybox/blob/1cf3ff5b2bdf332e6ecff8c4aaaa94172f693332/musl/Dockerfile)
-	[`1.24.1-uclibc`, `1.24.1`, `1.24-uclibc`, `1.24`, `1-uclibc`, `1`, `uclibc`, `latest` (*uclibc/Dockerfile*)](https://github.com/docker-library/busybox/blob/1cf3ff5b2bdf332e6ecff8c4aaaa94172f693332/uclibc/Dockerfile)

[![](https://badge.imagelayers.io/busybox:latest.svg)](https://imagelayers.io/?images=busybox:1.24.1-glibc,busybox:1.24.1-musl,busybox:1.24.1-uclibc)

For more information about this image and its history, please see [the relevant manifest file (`library/busybox`)](https://github.com/docker-library/official-images/blob/master/library/busybox). This image is updated via pull requests to [the `docker-library/official-images` GitHub repo](https://github.com/docker-library/official-images).

For detailed information about the virtual/transfer sizes and individual layers of each of the above supported tags, please see [the `busybox/tag-details.md` file](https://github.com/docker-library/docs/blob/master/busybox/tag-details.md) in [the `docker-library/docs` GitHub repo](https://github.com/docker-library/docs).

# What is BusyBox? The Swiss Army Knife of Embedded Linux

Coming in somewhere between 1 and 5 Mb in on-disk size (depending on the variant), [BusyBox](http://www.busybox.net/) is a very good ingredient to craft space-efficient distributions.

BusyBox combines tiny versions of many common UNIX utilities into a single small executable. It provides replacements for most of the utilities you usually find in GNU fileutils, shellutils, etc. The utilities in BusyBox generally have fewer options than their full-featured GNU cousins; however, the options that are included provide the expected functionality and behave very much like their GNU counterparts. BusyBox provides a fairly complete environment for any small or embedded system.

> [wikipedia.org/wiki/BusyBox](https://en.wikipedia.org/wiki/BusyBox)

![logo](https://raw.githubusercontent.com/docker-library/docs/8b984f7fe2aadc3e42ed2bbb89f0a72fff36d819/busybox/logo.png)

# How to use this image

## Run BusyBox shell

```console
$ docker run -it --rm busybox
```

This will drop you into an `sh` shell to allow you to do what you want inside a BusyBox system.

## Create a `Dockerfile` for a binary

```dockerfile
FROM busybox
COPY ./my-static-binary /my-static-binary
CMD ["/my-static-binary"]
```

This `Dockerfile` will allow you to create a minimal image for your statically compiled binary. You will have to compile the binary in some other place like another container. For a simpler alternative that's similarly tiny but easier to extend, [see `alpine`](https://hub.docker.com/_/alpine/).

## Image Variants

This image contains BusyBox built against various "libc" variants (for a comparison of "libc" variants, [Eta Labs has a very nice chart](http://www.etalabs.net/compare_libcs.html) which lists many similarities and differences).

-	`busybox:glibc`: [glibc from Debian](https://packages.debian.org/jessie/libc6) (which is then included in the image)
-	`busybox:musl`: [musl from Alpine](https://pkgs.alpinelinux.org/package/main/x86_64/musl) (statically compiled)
-	`busybox:uclibc`: [uClibc](https://uclibc.org) via [Buildroot](https://buildroot.org) (statically compiled)

For more information about the specific particulars of the build process for each variant, see `Dockerfile.builder` in the same directory as each variant's `Dockerfile` (see links above).

# License

View [license information](http://www.busybox.net/license.html) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.10.2.

Support for older versions (down to 1.6) is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.

# User Feedback

## Documentation

Documentation for this image is stored in the [`busybox/` directory](https://github.com/docker-library/docs/tree/master/busybox) of the [`docker-library/docs` GitHub repo](https://github.com/docker-library/docs). Be sure to familiarize yourself with the [repository's `README.md` file](https://github.com/docker-library/docs/blob/master/README.md) before attempting a pull request.

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/docker-library/busybox/issues).

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode](https://freenode.net).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/docker-library/busybox/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
