<!-- THIS FILE IS GENERATED VIA '.template-helpers/generate-tag-details.pl' -->

# Tags of `orientdb`

-	[`orientdb:2.0.18`](#orientdb2018)
-	[`orientdb:2.1.19`](#orientdb2119)
-	[`orientdb:2.2.3`](#orientdb223)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:d1168f6e58d6b9a2009f6fa975f7076ca3c9d108807d6930e4ce1c3c889921a7
```

-	Platforms:
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

-	Docker Version: 1.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e88db60bcaee0cf04983f1a3f434f6a3fb8c5c3c75eb30050421a3847637e`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 09 Jun 2016 21:28:42 GMT
ADD file:76679eeb94129df23c99013487d6b6bd779d2107bf07d194a524fdbb6a961530 in /
# Thu, 09 Jun 2016 21:28:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Jun 2016 21:35:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Jun 2016 21:37:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Jun 2016 22:05:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Jun 2016 22:10:09 GMT
RUN echo 'deb http://httpredir.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Thu, 09 Jun 2016 22:10:09 GMT
ENV LANG=C.UTF-8
# Thu, 09 Jun 2016 22:10:10 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 09 Jun 2016 22:10:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
# Thu, 09 Jun 2016 22:10:11 GMT
ENV JAVA_VERSION=8u91
# Thu, 09 Jun 2016 22:10:11 GMT
ENV JAVA_DEBIAN_VERSION=8u91-b14-1~bpo8+1
# Thu, 09 Jun 2016 22:10:11 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20140324
# Thu, 09 Jun 2016 22:12:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 09 Jun 2016 22:12:23 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Fri, 10 Jun 2016 22:06:25 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 10 Jun 2016 22:06:26 GMT
ENV ORIENTDB_VERSION=2.0.18
# Fri, 10 Jun 2016 22:06:26 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Fri, 10 Jun 2016 22:06:26 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Fri, 10 Jun 2016 22:06:31 GMT
RUN mkdir /orientdb &&   wget  "http://central.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 10 Jun 2016 22:06:31 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jun 2016 22:06:32 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 10 Jun 2016 22:06:32 GMT
WORKDIR /orientdb
# Fri, 10 Jun 2016 22:06:32 GMT
EXPOSE 2424/tcp
# Fri, 10 Jun 2016 22:06:33 GMT
EXPOSE 2480/tcp
# Fri, 10 Jun 2016 22:06:33 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5c90d4a2d1a8dfffd05ff2dd659923f0ca2d843b5e45d030e17abbcd06a11b5b`  
		Last Modified: Thu, 09 Jun 2016 21:30:47 GMT  
		Size: 51.4 MB (51352535 bytes)
	-	`sha256:ab30c63719b10dd434ddbe896879bd9b637fe4e16749a94d3dc827450dc2a437`  
		Last Modified: Thu, 09 Jun 2016 21:46:24 GMT  
		Size: 18.5 MB (18547219 bytes)
	-	`sha256:c6072700a24252bd71f6c5d2cabf5978ddf324a959b05bad417d8b3789f8df33`  
		Last Modified: Thu, 09 Jun 2016 21:46:52 GMT  
		Size: 42.5 MB (42525371 bytes)
	-	`sha256:5f444d0704271a846e0b83af62071bc825052d6eabba96121bc0acda9c8f9e64`  
		Last Modified: Thu, 09 Jun 2016 22:17:38 GMT  
		Size: 622.3 KB (622260 bytes)
	-	`sha256:620b5227cf380167d746f024d97b53f26fafcbd253df4cf56b3b3a056bf12ae1`  
		Last Modified: Thu, 09 Jun 2016 22:20:33 GMT  
		Size: 219.0 B
	-	`sha256:3cfd33220efaaad496080e9fdb124ddb9ba07742852c2db816c9870fe2e10c2a`  
		Last Modified: Thu, 09 Jun 2016 22:20:33 GMT  
		Size: 241.0 B
	-	`sha256:864a98a84dd2bba52cf57d13161517ee01e2966e72c3ac842c6a3d49c07dcb37`  
		Last Modified: Thu, 09 Jun 2016 22:21:03 GMT  
		Size: 130.0 MB (130020091 bytes)
	-	`sha256:734cc28150de3e42c9e581aa1d7da3f378fcde2a00719a2d42ec376519050365`  
		Last Modified: Thu, 09 Jun 2016 22:20:34 GMT  
		Size: 284.4 KB (284370 bytes)
	-	`sha256:889c466800a29eb4c4be9fcbdd0432ee96e297f1ad4023988876258a5b043a62`  
		Last Modified: Tue, 14 Jun 2016 21:48:42 GMT  
		Size: 46.5 MB (46544855 bytes)

## `orientdb:2.1.19`

```console
$ docker pull orientdb@sha256:7cfbe017c53f7430162fce3726f4a36d201f1d3baf2eb06e986b368fdaaf9286
```

-	Platforms:
	-	linux; amd64

### `orientdb:2.1.19` - linux; amd64

-	Docker Version: 1.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82939795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d3e8818f69f9ffaa5cf3e4a6b9ad348bc1914972e0de2a5c425b67978dc9b9`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 23 Jun 2016 19:55:18 GMT
ADD file:852e9d0cb9d906535af512a89339fc70b2873a0f94defbcbe41cd44942dd6ac8 in /
# Thu, 23 Jun 2016 20:34:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2016 20:34:55 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 23 Jun 2016 20:38:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Thu, 23 Jun 2016 20:38:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_VERSION=8u92
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Thu, 23 Jun 2016 20:39:07 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Jun 2016 22:21:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 23 Jun 2016 22:21:58 GMT
ENV ORIENTDB_VERSION=2.1.19
# Thu, 23 Jun 2016 22:21:58 GMT
ENV ORIENTDB_DOWNLOAD_MD5=11942093675c32b9341658bd56f191f0
# Thu, 23 Jun 2016 22:21:59 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=289b5d0950254e90531e65a3f4ef530bb4193f32
# Thu, 23 Jun 2016 22:22:02 GMT
RUN apk add --update tar     && rm -rf /var/cache/apk/*
# Thu, 23 Jun 2016 22:22:06 GMT
RUN mkdir /orientdb &&   wget  "http://central.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 23 Jun 2016 22:22:06 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 22:22:07 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 23 Jun 2016 22:22:08 GMT
WORKDIR /orientdb
# Thu, 23 Jun 2016 22:22:08 GMT
EXPOSE 2424/tcp
# Thu, 23 Jun 2016 22:22:09 GMT
EXPOSE 2480/tcp
# Thu, 23 Jun 2016 22:22:09 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e110a4a1794126ef308a49f2d65785af2f25538f06700721aad8283b81fdfa58`  
		Last Modified: Thu, 23 Jun 2016 19:56:16 GMT  
		Size: 2.3 MB (2310286 bytes)
	-	`sha256:5726fbb708f0cfe4f045a0616cde707fb6bcc4e579926a29863ba422c0d86839`  
		Last Modified: Thu, 23 Jun 2016 20:35:22 GMT  
		Size: 230.0 B
	-	`sha256:edeb4344937fef0e7604839f9af5e0cfaedfa6d88d8ee0000534e9b424b9e4be`  
		Last Modified: Thu, 23 Jun 2016 20:39:26 GMT  
		Size: 49.3 MB (49325233 bytes)
	-	`sha256:74ad2652d6402897358ea7a846ba611dd21d01895bd6162276515ea1a5c16160`  
		Last Modified: Thu, 23 Jun 2016 22:22:16 GMT  
		Size: 261.8 KB (261820 bytes)
	-	`sha256:4e8df945f697f0b7e543e3c7411993a1a478df8dbd976f1f9b37062ca04762e9`  
		Last Modified: Thu, 23 Jun 2016 22:22:19 GMT  
		Size: 31.0 MB (31042226 bytes)

## `orientdb:2.2.3`

```console
$ docker pull orientdb@sha256:b0897e9357339cb3bf50de9a4f1bd00f0dc47eecec631a63f696442b4f5cf309
```

-	Platforms:
	-	linux; amd64

### `orientdb:2.2.3` - linux; amd64

-	Docker Version: 1.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86351818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2591bdbcabb3f59ab2279329b2be89b0156fa14b6000c676ee21a72aac1871`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 23 Jun 2016 19:55:18 GMT
ADD file:852e9d0cb9d906535af512a89339fc70b2873a0f94defbcbe41cd44942dd6ac8 in /
# Thu, 23 Jun 2016 20:34:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2016 20:34:55 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 23 Jun 2016 20:38:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Thu, 23 Jun 2016 20:38:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_VERSION=8u92
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Thu, 23 Jun 2016 20:39:07 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Jun 2016 22:21:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 23 Jun 2016 22:22:27 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 23 Jun 2016 22:22:28 GMT
ENV ORIENTDB_VERSION=2.2.3
# Thu, 23 Jun 2016 22:22:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb001911d3be9915bc64bcf4140535d1
# Thu, 23 Jun 2016 22:22:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8756b6e41baae7608eff154b5bbbde80b61d929e
# Thu, 23 Jun 2016 22:22:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.3/orientdb-community-2.2.3.tar.gz
# Thu, 23 Jun 2016 22:22:33 GMT
RUN apk add --update tar     && rm -rf /var/cache/apk/*
# Thu, 23 Jun 2016 22:22:36 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 23 Jun 2016 22:22:37 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 22:22:37 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 23 Jun 2016 22:22:38 GMT
WORKDIR /orientdb
# Thu, 23 Jun 2016 22:22:38 GMT
EXPOSE 2424/tcp
# Thu, 23 Jun 2016 22:22:39 GMT
EXPOSE 2480/tcp
# Thu, 23 Jun 2016 22:22:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e110a4a1794126ef308a49f2d65785af2f25538f06700721aad8283b81fdfa58`  
		Last Modified: Thu, 23 Jun 2016 19:56:16 GMT  
		Size: 2.3 MB (2310286 bytes)
	-	`sha256:5726fbb708f0cfe4f045a0616cde707fb6bcc4e579926a29863ba422c0d86839`  
		Last Modified: Thu, 23 Jun 2016 20:35:22 GMT  
		Size: 230.0 B
	-	`sha256:edeb4344937fef0e7604839f9af5e0cfaedfa6d88d8ee0000534e9b424b9e4be`  
		Last Modified: Thu, 23 Jun 2016 20:39:26 GMT  
		Size: 49.3 MB (49325233 bytes)
	-	`sha256:aa428c627ee13734b158c502f25fa406833807f88bda4075888a0aed92af74fd`  
		Last Modified: Thu, 23 Jun 2016 22:22:46 GMT  
		Size: 261.8 KB (261820 bytes)
	-	`sha256:be37f447f9fbfb6541ae706127587286b05f982f5fe646a05397cd18ee0252b5`  
		Last Modified: Thu, 23 Jun 2016 22:22:50 GMT  
		Size: 34.5 MB (34454249 bytes)

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:b0897e9357339cb3bf50de9a4f1bd00f0dc47eecec631a63f696442b4f5cf309
```

-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

-	Docker Version: 1.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86351818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2591bdbcabb3f59ab2279329b2be89b0156fa14b6000c676ee21a72aac1871`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 23 Jun 2016 19:55:18 GMT
ADD file:852e9d0cb9d906535af512a89339fc70b2873a0f94defbcbe41cd44942dd6ac8 in /
# Thu, 23 Jun 2016 20:34:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2016 20:34:55 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 23 Jun 2016 20:38:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Thu, 23 Jun 2016 20:38:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_VERSION=8u92
# Thu, 23 Jun 2016 20:38:57 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Thu, 23 Jun 2016 20:39:07 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Jun 2016 22:21:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 23 Jun 2016 22:22:27 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 23 Jun 2016 22:22:28 GMT
ENV ORIENTDB_VERSION=2.2.3
# Thu, 23 Jun 2016 22:22:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb001911d3be9915bc64bcf4140535d1
# Thu, 23 Jun 2016 22:22:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8756b6e41baae7608eff154b5bbbde80b61d929e
# Thu, 23 Jun 2016 22:22:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.3/orientdb-community-2.2.3.tar.gz
# Thu, 23 Jun 2016 22:22:33 GMT
RUN apk add --update tar     && rm -rf /var/cache/apk/*
# Thu, 23 Jun 2016 22:22:36 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 23 Jun 2016 22:22:37 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 23 Jun 2016 22:22:37 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 23 Jun 2016 22:22:38 GMT
WORKDIR /orientdb
# Thu, 23 Jun 2016 22:22:38 GMT
EXPOSE 2424/tcp
# Thu, 23 Jun 2016 22:22:39 GMT
EXPOSE 2480/tcp
# Thu, 23 Jun 2016 22:22:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e110a4a1794126ef308a49f2d65785af2f25538f06700721aad8283b81fdfa58`  
		Last Modified: Thu, 23 Jun 2016 19:56:16 GMT  
		Size: 2.3 MB (2310286 bytes)
	-	`sha256:5726fbb708f0cfe4f045a0616cde707fb6bcc4e579926a29863ba422c0d86839`  
		Last Modified: Thu, 23 Jun 2016 20:35:22 GMT  
		Size: 230.0 B
	-	`sha256:edeb4344937fef0e7604839f9af5e0cfaedfa6d88d8ee0000534e9b424b9e4be`  
		Last Modified: Thu, 23 Jun 2016 20:39:26 GMT  
		Size: 49.3 MB (49325233 bytes)
	-	`sha256:aa428c627ee13734b158c502f25fa406833807f88bda4075888a0aed92af74fd`  
		Last Modified: Thu, 23 Jun 2016 22:22:46 GMT  
		Size: 261.8 KB (261820 bytes)
	-	`sha256:be37f447f9fbfb6541ae706127587286b05f982f5fe646a05397cd18ee0252b5`  
		Last Modified: Thu, 23 Jun 2016 22:22:50 GMT  
		Size: 34.5 MB (34454249 bytes)
