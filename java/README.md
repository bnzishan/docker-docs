# Supported tags and respective `Dockerfile` links

-	[`6b38-jdk`, `6b38`, `6-jdk`, `6`, `openjdk-6b38-jdk`, `openjdk-6b38`, `openjdk-6-jdk`, `openjdk-6` (*6-jdk/Dockerfile*)](https://github.com/docker-library/openjdk/blob/89851f0abc3a83cfad5248102f379d6a0bd3951a/6-jdk/Dockerfile)
-	[`6b38-jre`, `6-jre`, `openjdk-6b38-jre`, `openjdk-6-jre` (*6-jre/Dockerfile*)](https://github.com/docker-library/openjdk/blob/89851f0abc3a83cfad5248102f379d6a0bd3951a/6-jre/Dockerfile)
-	[`7u101-jdk`, `7u101`, `7-jdk`, `7`, `openjdk-7u101-jdk`, `openjdk-7u101`, `openjdk-7-jdk`, `openjdk-7` (*7-jdk/Dockerfile*)](https://github.com/docker-library/openjdk/blob/a3f06bcbc86d16912a309cf4538a00caf9a6100c/7-jdk/Dockerfile)
-	[`7u91-jdk-alpine`, `7u91-alpine`, `7-jdk-alpine`, `7-alpine`, `openjdk-7u91-jdk-alpine`, `openjdk-7u91-alpine`, `openjdk-7-jdk-alpine`, `openjdk-7-alpine` (*7-jdk/alpine/Dockerfile*)](https://github.com/docker-library/openjdk/blob/f60edc7cfe9fa4d4473ef027c6fb2d5e1f6c17f9/7-jdk/alpine/Dockerfile)
-	[`7u101-jre`, `7-jre`, `openjdk-7u101-jre`, `openjdk-7-jre` (*7-jre/Dockerfile*)](https://github.com/docker-library/openjdk/blob/a3f06bcbc86d16912a309cf4538a00caf9a6100c/7-jre/Dockerfile)
-	[`7u91-jre-alpine`, `7-jre-alpine`, `openjdk-7u91-jre-alpine`, `openjdk-7-jre-alpine` (*7-jre/alpine/Dockerfile*)](https://github.com/docker-library/openjdk/blob/f60edc7cfe9fa4d4473ef027c6fb2d5e1f6c17f9/7-jre/alpine/Dockerfile)
-	[`8u91-jdk`, `8u91`, `8-jdk`, `8`, `jdk`, `latest`, `openjdk-8u91-jdk`, `openjdk-8u91`, `openjdk-8-jdk`, `openjdk-8` (*8-jdk/Dockerfile*)](https://github.com/docker-library/openjdk/blob/a0a4970a343a3c021dad760f2281d20f61931e3c/8-jdk/Dockerfile)
-	[`8u92-jdk-alpine`, `8u92-alpine`, `8-jdk-alpine`, `8-alpine`, `jdk-alpine`, `alpine`, `openjdk-8u92-jdk-alpine`, `openjdk-8u92-alpine`, `openjdk-8-jdk-alpine`, `openjdk-8-alpine` (*8-jdk/alpine/Dockerfile*)](https://github.com/docker-library/openjdk/blob/c6c90f5e09a5dc1a1ccd662de8210342f94c673e/8-jdk/alpine/Dockerfile)
-	[`8u91-jre`, `8-jre`, `jre`, `openjdk-8u91-jre`, `openjdk-8-jre` (*8-jre/Dockerfile*)](https://github.com/docker-library/openjdk/blob/a0a4970a343a3c021dad760f2281d20f61931e3c/8-jre/Dockerfile)
-	[`8u92-jre-alpine`, `8-jre-alpine`, `jre-alpine`, `openjdk-8u92-jre-alpine`, `openjdk-8-jre-alpine` (*8-jre/alpine/Dockerfile*)](https://github.com/docker-library/openjdk/blob/c6c90f5e09a5dc1a1ccd662de8210342f94c673e/8-jre/alpine/Dockerfile)
-	[`9-b116-jdk`, `9-b116`, `9-jdk`, `9`, `openjdk-9-b116-jdk`, `openjdk-9-b116`, `openjdk-9-jdk`, `openjdk-9` (*9-jdk/Dockerfile*)](https://github.com/docker-library/openjdk/blob/4427d56d00bbd05b6c7e0f5ce7a3a7a01b6d4177/9-jdk/Dockerfile)
-	[`9-b116-jre`, `9-jre`, `openjdk-9-b116-jre`, `openjdk-9-jre` (*9-jre/Dockerfile*)](https://github.com/docker-library/openjdk/blob/4427d56d00bbd05b6c7e0f5ce7a3a7a01b6d4177/9-jre/Dockerfile)

[![](https://badge.imagelayers.io/java:latest.svg)](https://imagelayers.io/?images=java:6b38-jdk,java:6b38-jre,java:7u101-jdk,java:7u91-jdk-alpine,java:7u101-jre,java:7u91-jre-alpine,java:8u91-jdk,java:8u92-jdk-alpine,java:8u91-jre,java:8u92-jre-alpine,java:9-b116-jdk,java:9-b116-jre)

For more information about this image and its history, please see [the relevant manifest file (`library/java`)](https://github.com/docker-library/official-images/blob/master/library/java). This image is updated via [pull requests to the `docker-library/official-images` GitHub repo](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Fjava).

For detailed information about the virtual/transfer sizes and individual layers of each of the above supported tags, please see [the `java/tag-details.md` file](https://github.com/docker-library/docs/blob/master/java/tag-details.md) in [the `docker-library/docs` GitHub repo](https://github.com/docker-library/docs).

# What is Java?

Java is a concurrent, class-based, object-oriented language specifically designed to have as few implementation dependencies as possible. It is intended to allow application developers to "write once, run anywhere", meaning that code that runs on one platform does not need to be recompiled to run on another.

Java is a registered trademark of Oracle and/or its affiliates.

> [wikipedia.org/wiki/Java_(programming_language)](http://en.wikipedia.org/wiki/Java_%28programming_language%29)

![logo](https://raw.githubusercontent.com/docker-library/docs/01c12653951b2fe592c1f93a13b4e289ada0e3a1/java/logo.png)

# How to use this image

## Start a Java instance in your app

The most straightforward way to use this image is to use a Java container as both the build and runtime environment. In your `Dockerfile`, writing something along the lines of the following will compile and run your project:

```dockerfile
FROM java:7
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
RUN javac Main.java
CMD ["java", "Main"]
```

You can then run and build the Docker image:

```console
$ docker build -t my-java-app .
$ docker run -it --rm --name my-running-app my-java-app
```

## Compile your app inside the Docker container

There may be occasions where it is not appropriate to run your app inside a container. To compile, but not run your app inside the Docker instance, you can write something like:

```console
$ docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp java:7 javac Main.java
```

This will add your current directory as a volume to the container, set the working directory to the volume, and run the command `javac Main.java` which will tell Java to compile the code in `Main.java` and output the Java class file to `Main.class`.

# Why is this only OpenJDK/OpenJRE?

As all of the major upstream Linux distributions are unwilling to redistribute Oracle Java in their own distribution channels, we have chosen to follow them. See references below on how each distribution does not distribute Oracle Java.

-	Ubuntu stopped distributing it in the `sun-java6` package when Oracle retired the "Operating System Distributor License for Java" ([lists.ubuntu.com](https://lists.ubuntu.com/archives/ubuntu-security-announce/2011-December/001528.html)).
-	Debian requires users to download the Java tar manually from oracle.com and then use `java-package` to install it ([wiki.debian.net](https://wiki.debian.org/Java/Sun)).
-	The webupd8 PPA for Ubuntu and Debian requires the user to accept the Oracle license in order for their software to download and install Oracle java ([webupd8.org](http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html)).
-	Gentoo has a *fetch-restriction* that requires the user to go to the Oracle website to download the Java tar manually which inclues accepting the license ([wiki.gentoo.org](https://wiki.gentoo.org/wiki/Java)).
-	CentOS requires users to go and download the rpm provided by Oracle at java.com and thus accept the Oracle license ([wiki.centos.org](https://wiki.centos.org/HowTos/JavaRuntimeEnvironment)).
-	RedHat provides instructions to add a repo that is maintained by Oracle ([access.redhat.com](https://access.redhat.com/solutions/732883)).

# License

View [license information](http://openjdk.java.net/legal/gplv2+ce.html) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.11.2.

Support for older versions (down to 1.6) is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.

# User Feedback

## Documentation

Documentation for this image is stored in the [`java/` directory](https://github.com/docker-library/docs/tree/master/java) of the [`docker-library/docs` GitHub repo](https://github.com/docker-library/docs). Be sure to familiarize yourself with the [repository's `README.md` file](https://github.com/docker-library/docs/blob/master/README.md) before attempting a pull request.

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/docker-library/java/issues). If the issue is related to a CVE, please check for [a `cve-tracker` issue on the `official-images` repository first](https://github.com/docker-library/official-images/issues?q=label%3Acve-tracker).

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode](https://freenode.net).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/docker-library/java/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
