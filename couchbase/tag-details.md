<!-- THIS FILE IS GENERATED VIA '.template-helpers/generate-tag-details.pl' -->

# Tags of `couchbase`

-	[`couchbase:latest`](#couchbaselatest)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:4.1.0`](#couchbase410)
-	[`couchbase:enterprise-4.1.0`](#couchbaseenterprise-410)
-	[`couchbase:4.0.0`](#couchbase400)
-	[`couchbase:enterprise-4.0.0`](#couchbaseenterprise-400)
-	[`couchbase:community-4.0.0`](#couchbasecommunity-400)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:3.1.0`](#couchbase310)
-	[`couchbase:enterprise-3.1.0`](#couchbaseenterprise-310)
-	[`couchbase:3.0.3`](#couchbase303)
-	[`couchbase:enterprise-3.0.3`](#couchbaseenterprise-303)
-	[`couchbase:3.0.2`](#couchbase302)
-	[`couchbase:enterprise-3.0.2`](#couchbaseenterprise-302)
-	[`couchbase:community-3.0.1`](#couchbasecommunity-301)
-	[`couchbase:2.5.2`](#couchbase252)
-	[`couchbase:enterprise-2.5.2`](#couchbaseenterprise-252)
-	[`couchbase:community-2.2.0`](#couchbasecommunity-220)

## `couchbase:latest`

```console
$ docker pull library/couchbase@sha256:6085676a8f37ecdd83c7fcbe6a445c8dc6067181b0ccf09287c160df1dc75949
```

-	Total Virtual Size: 374.8 MB (374824220 bytes)
-	Total v2 Content-Length: 139.4 MB (139444495 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`

```dockerfile
ENV CB_VERSION=4.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.1.0-ubuntu12.04_amd64.deb CB_SHA256=38b92711a52cbb0f8d4ab977e0ea2fb4e25022a0660dacc26fd7a60031eb70d2 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:03:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:03:20 GMT
-	Parent Layer: `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:10f0979b6cbd4810fb98e2e511970ef5004849868a12f0a849f5d272e52c54f2`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:55 GMT

#### `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:03:37 GMT
-	Parent Layer: `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`
-	Docker Version: 1.8.3
-	Virtual Size: 214.0 MB (213957142 bytes)
-	v2 Blob: `sha256:9be3d8460ed2e26d3df1a722f92026e70660db0245eb12bff429dcf29f6ccd62`
-	v2 Content-Length: 87.8 MB (87750715 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:49 GMT

#### `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:03:39 GMT
-	Parent Layer: `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:59e718ec07e9dab09011fb2c80ae2ad526fcb7cba7a962b1fd1215b21ae9f866`
-	v2 Content-Length: 336.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:11 GMT

#### `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:a0b9aa29408d824e135537eec0585e4108f2347bf095d3662a09edfd5f5ac5f6`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:08 GMT

#### `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0cb81f5cc79b4c2092b84060253e0de85b562aee25459bcee10657331f33b460`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:03:42 GMT
-	Parent Layer: `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise`

```console
$ docker pull library/couchbase@sha256:240039643a39572f404ae6d536eb283f2c7a29861598de4ca9930fdead68f704
```

-	Total Virtual Size: 374.8 MB (374824220 bytes)
-	Total v2 Content-Length: 139.4 MB (139444495 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`

```dockerfile
ENV CB_VERSION=4.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.1.0-ubuntu12.04_amd64.deb CB_SHA256=38b92711a52cbb0f8d4ab977e0ea2fb4e25022a0660dacc26fd7a60031eb70d2 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:03:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:03:20 GMT
-	Parent Layer: `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:10f0979b6cbd4810fb98e2e511970ef5004849868a12f0a849f5d272e52c54f2`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:55 GMT

#### `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:03:37 GMT
-	Parent Layer: `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`
-	Docker Version: 1.8.3
-	Virtual Size: 214.0 MB (213957142 bytes)
-	v2 Blob: `sha256:9be3d8460ed2e26d3df1a722f92026e70660db0245eb12bff429dcf29f6ccd62`
-	v2 Content-Length: 87.8 MB (87750715 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:49 GMT

#### `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:03:39 GMT
-	Parent Layer: `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:59e718ec07e9dab09011fb2c80ae2ad526fcb7cba7a962b1fd1215b21ae9f866`
-	v2 Content-Length: 336.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:11 GMT

#### `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:a0b9aa29408d824e135537eec0585e4108f2347bf095d3662a09edfd5f5ac5f6`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:08 GMT

#### `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0cb81f5cc79b4c2092b84060253e0de85b562aee25459bcee10657331f33b460`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:03:42 GMT
-	Parent Layer: `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:4.1.0`

```console
$ docker pull library/couchbase@sha256:f37004754abe94c2b71c0705ef552a9fe87c4ceba61a068fedfb5535e72818bb
```

-	Total Virtual Size: 374.8 MB (374824220 bytes)
-	Total v2 Content-Length: 139.4 MB (139444495 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`

```dockerfile
ENV CB_VERSION=4.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.1.0-ubuntu12.04_amd64.deb CB_SHA256=38b92711a52cbb0f8d4ab977e0ea2fb4e25022a0660dacc26fd7a60031eb70d2 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:03:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:03:20 GMT
-	Parent Layer: `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:10f0979b6cbd4810fb98e2e511970ef5004849868a12f0a849f5d272e52c54f2`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:55 GMT

#### `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:03:37 GMT
-	Parent Layer: `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`
-	Docker Version: 1.8.3
-	Virtual Size: 214.0 MB (213957142 bytes)
-	v2 Blob: `sha256:9be3d8460ed2e26d3df1a722f92026e70660db0245eb12bff429dcf29f6ccd62`
-	v2 Content-Length: 87.8 MB (87750715 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:49 GMT

#### `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:03:39 GMT
-	Parent Layer: `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:59e718ec07e9dab09011fb2c80ae2ad526fcb7cba7a962b1fd1215b21ae9f866`
-	v2 Content-Length: 336.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:11 GMT

#### `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:a0b9aa29408d824e135537eec0585e4108f2347bf095d3662a09edfd5f5ac5f6`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:08 GMT

#### `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0cb81f5cc79b4c2092b84060253e0de85b562aee25459bcee10657331f33b460`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:03:42 GMT
-	Parent Layer: `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-4.1.0`

```console
$ docker pull library/couchbase@sha256:a688d1a63c28e039b3cd8f10f61b48a7ae07d1eda7fe118012dad367c2b9648f
```

-	Total Virtual Size: 374.8 MB (374824220 bytes)
-	Total v2 Content-Length: 139.4 MB (139444495 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`

```dockerfile
ENV CB_VERSION=4.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.1.0-ubuntu12.04_amd64.deb CB_SHA256=38b92711a52cbb0f8d4ab977e0ea2fb4e25022a0660dacc26fd7a60031eb70d2 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:03:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:03:20 GMT
-	Parent Layer: `646c3d5ebb71c01bae39e5ae4923fb2a79394b723fb26ddc4392cc279fda36ac`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:10f0979b6cbd4810fb98e2e511970ef5004849868a12f0a849f5d272e52c54f2`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:55 GMT

#### `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:03:37 GMT
-	Parent Layer: `864cbabd77addfd783f6d58976ff61bd039bb4a51669096adeede1464b56b531`
-	Docker Version: 1.8.3
-	Virtual Size: 214.0 MB (213957142 bytes)
-	v2 Blob: `sha256:9be3d8460ed2e26d3df1a722f92026e70660db0245eb12bff429dcf29f6ccd62`
-	v2 Content-Length: 87.8 MB (87750715 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:49 GMT

#### `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:03:39 GMT
-	Parent Layer: `8c327c6d4e432d731e0fb4009315ef8c3ab78c2fbd336af237882c97dc1d4d4c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:59e718ec07e9dab09011fb2c80ae2ad526fcb7cba7a962b1fd1215b21ae9f866`
-	v2 Content-Length: 336.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:11 GMT

#### `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `8592c697ab61b03bb097b5714b25e7920a38e20a8bb469495ea42807e7cea192`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:a0b9aa29408d824e135537eec0585e4108f2347bf095d3662a09edfd5f5ac5f6`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:38:08 GMT

#### `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:03:40 GMT
-	Parent Layer: `7734f4a832d45ee82b812d15fe86050c134d1c9c55f24199ac8a5eb1f0cc0767`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `35edb38ebc172a167637a6fc0d701f9b97126ef21cb8e1a01189b4cd4ad6295b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:03:41 GMT
-	Parent Layer: `99f3eb6fb46f6b7a456968ff49b95d9bcdfb73b7011be402025a2109ccd264f1`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0cb81f5cc79b4c2092b84060253e0de85b562aee25459bcee10657331f33b460`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:03:42 GMT
-	Parent Layer: `91e5fad693c2a5c8b5ead3e4a52534c570afedf0d524397ced3b31ad8cbf392e`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:4.0.0`

```console
$ docker pull library/couchbase@sha256:73da75f41c12e7db9261d1669946f1c4bb1e83490be985398bbacdad052c4c5e
```

-	Total Virtual Size: 372.9 MB (372912561 bytes)
-	Total v2 Content-Length: 139.1 MB (139074055 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `b90d6d7baad2f9c13982023adab95cffe5db00e9ea6c52c962dd55fa6e28205f`

```dockerfile
ENV CB_VERSION=4.0.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.0.0-ubuntu12.04_amd64.deb CB_SHA256=30c4e6711d8619bfd432b7b2d4db6a07aac753c45f1f5feabd630d8dd1cbfecc PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:05:34 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `71c2823f9fbee4a243e5dafc41e6a75106f79a7084470f6e2a252cf4743385f0`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:05:36 GMT
-	Parent Layer: `b90d6d7baad2f9c13982023adab95cffe5db00e9ea6c52c962dd55fa6e28205f`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:cd15b90804ace7fc76f1b5ac0dbe21c74a79e6374b7012632e64fb65a8719183`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:43:01 GMT

#### `45d48b41a3d268beb690c2d8457e80ea04003b074f85a12f7b959580ac8dec23`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:05:51 GMT
-	Parent Layer: `71c2823f9fbee4a243e5dafc41e6a75106f79a7084470f6e2a252cf4743385f0`
-	Docker Version: 1.8.3
-	Virtual Size: 212.0 MB (212045483 bytes)
-	v2 Blob: `sha256:9016da98c228207874e607c6f156fdea680ba1112684f29c4ca1255cdada2954`
-	v2 Content-Length: 87.4 MB (87380275 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:42:54 GMT

#### `18f7ce2970b1944e28b113eaf1e5c9234b9e564bd70bb8fcfa08b5e1f2e6e299`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:05:53 GMT
-	Parent Layer: `45d48b41a3d268beb690c2d8457e80ea04003b074f85a12f7b959580ac8dec23`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a3603a09a859a260e57104c51e6d0e6ac13ca77a399ce7fb09e30f7990889d61`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:42:14 GMT

#### `33183b13abff88dfcaed43249ecaa14f261f46c91dde391f42795ec6bcc2449c`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:05:54 GMT
-	Parent Layer: `18f7ce2970b1944e28b113eaf1e5c9234b9e564bd70bb8fcfa08b5e1f2e6e299`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:2b0577d10daafd953271cf331ee983fd0383ecaaedd75f5360bb65b307b08fa1`
-	v2 Content-Length: 251.0 B
-	v2 Last-Modified: Fri, 02 Oct 2015 21:51:53 GMT

#### `f0b645f93a972bc6a33a37f452b5a6d11de5e9d53a4684ab8a12062e14bfb434`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:05:54 GMT
-	Parent Layer: `33183b13abff88dfcaed43249ecaa14f261f46c91dde391f42795ec6bcc2449c`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `6ba322b3186da612b060f3add40072c604c5a43f1c96e7f0afc962d9e3ea8c60`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:05:55 GMT
-	Parent Layer: `f0b645f93a972bc6a33a37f452b5a6d11de5e9d53a4684ab8a12062e14bfb434`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b0214f1e6452c7cc07c06af688d02a1e8046ff8ff0f45d5442073eb4d759b0a5`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:05:55 GMT
-	Parent Layer: `6ba322b3186da612b060f3add40072c604c5a43f1c96e7f0afc962d9e3ea8c60`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e5cf477f8929397f9d2e42ac043e0c511e16d928d01b671c9dd905b1ebc2caaf`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:05:56 GMT
-	Parent Layer: `b0214f1e6452c7cc07c06af688d02a1e8046ff8ff0f45d5442073eb4d759b0a5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-4.0.0`

```console
$ docker pull library/couchbase@sha256:27c3bb51df8bf19c66b18a94d347ec6f51169da5a329d1796b88500b7593d807
```

-	Total Virtual Size: 372.9 MB (372912561 bytes)
-	Total v2 Content-Length: 139.1 MB (139074055 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `b90d6d7baad2f9c13982023adab95cffe5db00e9ea6c52c962dd55fa6e28205f`

```dockerfile
ENV CB_VERSION=4.0.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_4.0.0-ubuntu12.04_amd64.deb CB_SHA256=30c4e6711d8619bfd432b7b2d4db6a07aac753c45f1f5feabd630d8dd1cbfecc PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:05:34 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `71c2823f9fbee4a243e5dafc41e6a75106f79a7084470f6e2a252cf4743385f0`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:05:36 GMT
-	Parent Layer: `b90d6d7baad2f9c13982023adab95cffe5db00e9ea6c52c962dd55fa6e28205f`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:cd15b90804ace7fc76f1b5ac0dbe21c74a79e6374b7012632e64fb65a8719183`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:43:01 GMT

#### `45d48b41a3d268beb690c2d8457e80ea04003b074f85a12f7b959580ac8dec23`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:05:51 GMT
-	Parent Layer: `71c2823f9fbee4a243e5dafc41e6a75106f79a7084470f6e2a252cf4743385f0`
-	Docker Version: 1.8.3
-	Virtual Size: 212.0 MB (212045483 bytes)
-	v2 Blob: `sha256:9016da98c228207874e607c6f156fdea680ba1112684f29c4ca1255cdada2954`
-	v2 Content-Length: 87.4 MB (87380275 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:42:54 GMT

#### `18f7ce2970b1944e28b113eaf1e5c9234b9e564bd70bb8fcfa08b5e1f2e6e299`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:05:53 GMT
-	Parent Layer: `45d48b41a3d268beb690c2d8457e80ea04003b074f85a12f7b959580ac8dec23`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a3603a09a859a260e57104c51e6d0e6ac13ca77a399ce7fb09e30f7990889d61`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:42:14 GMT

#### `33183b13abff88dfcaed43249ecaa14f261f46c91dde391f42795ec6bcc2449c`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:05:54 GMT
-	Parent Layer: `18f7ce2970b1944e28b113eaf1e5c9234b9e564bd70bb8fcfa08b5e1f2e6e299`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:2b0577d10daafd953271cf331ee983fd0383ecaaedd75f5360bb65b307b08fa1`
-	v2 Content-Length: 251.0 B
-	v2 Last-Modified: Fri, 02 Oct 2015 21:51:53 GMT

#### `f0b645f93a972bc6a33a37f452b5a6d11de5e9d53a4684ab8a12062e14bfb434`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:05:54 GMT
-	Parent Layer: `33183b13abff88dfcaed43249ecaa14f261f46c91dde391f42795ec6bcc2449c`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `6ba322b3186da612b060f3add40072c604c5a43f1c96e7f0afc962d9e3ea8c60`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:05:55 GMT
-	Parent Layer: `f0b645f93a972bc6a33a37f452b5a6d11de5e9d53a4684ab8a12062e14bfb434`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b0214f1e6452c7cc07c06af688d02a1e8046ff8ff0f45d5442073eb4d759b0a5`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:05:55 GMT
-	Parent Layer: `6ba322b3186da612b060f3add40072c604c5a43f1c96e7f0afc962d9e3ea8c60`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e5cf477f8929397f9d2e42ac043e0c511e16d928d01b671c9dd905b1ebc2caaf`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:05:56 GMT
-	Parent Layer: `b0214f1e6452c7cc07c06af688d02a1e8046ff8ff0f45d5442073eb4d759b0a5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:community-4.0.0`

```console
$ docker pull library/couchbase@sha256:02d0caab304b5862b79e2897b10e5075a25bc372f8d08474365afdd46e2bae23
```

-	Total Virtual Size: 372.9 MB (372881322 bytes)
-	Total v2 Content-Length: 139.1 MB (139066432 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `0468ae09390e99dc69fbfdfa34645e9088f5489138dbd7ae63b6fba20e829c62`

```dockerfile
ENV CB_VERSION=4.0.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-community_4.0.0-ubuntu12.04_amd64.deb CB_SHA256=404007eaedc3d01997eea800fcce0d0a0339bc3ab79c1c48741210f435c719f0 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:07:22 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `d7bacfc5350290a917b724a8eab1b99bf28bc3ce3c448a42b7e713638c6cb524`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:07:23 GMT
-	Parent Layer: `0468ae09390e99dc69fbfdfa34645e9088f5489138dbd7ae63b6fba20e829c62`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:58d143b7b12746889dec7f4e5950e3840c5a1956178b2d57576f8a5f851d39d8`
-	v2 Content-Length: 1.7 KB (1695 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:45:22 GMT

#### `c918cfc389e2daca2c60e01def7eb068bb64f44a753961435e820d3c8a93c4a0`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:07:43 GMT
-	Parent Layer: `d7bacfc5350290a917b724a8eab1b99bf28bc3ce3c448a42b7e713638c6cb524`
-	Docker Version: 1.8.3
-	Virtual Size: 212.0 MB (212014244 bytes)
-	v2 Blob: `sha256:6eff6949618fbd0505f1061c2f913b5641a4369916201bcbb8698110770e0f64`
-	v2 Content-Length: 87.4 MB (87372651 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:45:16 GMT

#### `ca58c031c23966b9c6dd62d01e29a5a2a166ecf01bd2fef9bf59e4423a7cda19`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:07:46 GMT
-	Parent Layer: `c918cfc389e2daca2c60e01def7eb068bb64f44a753961435e820d3c8a93c4a0`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:dc663f718893427e056db0c88b0af798aa21d28d194a370fef5e5819920fa8cb`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:44:37 GMT

#### `8ea9b56e2046c06886759aa734d98fad8ad14019a934006bc372933c49031566`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:07:46 GMT
-	Parent Layer: `ca58c031c23966b9c6dd62d01e29a5a2a166ecf01bd2fef9bf59e4423a7cda19`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:2b0577d10daafd953271cf331ee983fd0383ecaaedd75f5360bb65b307b08fa1`
-	v2 Content-Length: 251.0 B
-	v2 Last-Modified: Fri, 02 Oct 2015 21:51:53 GMT

#### `4c45b0cdb9a2f56e69121298031e47fdfcc30b2efbeb364a434576f78497bdc0`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:07:47 GMT
-	Parent Layer: `8ea9b56e2046c06886759aa734d98fad8ad14019a934006bc372933c49031566`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `8015286e15ef466f9df6d9109b01a20e8cd51050f5410dd4396a08797c8129dd`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:07:47 GMT
-	Parent Layer: `4c45b0cdb9a2f56e69121298031e47fdfcc30b2efbeb364a434576f78497bdc0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32a1292116d7246fa8bdbde80f02abc983e698ad288976cf7c1255fee2dd46cc`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:07:48 GMT
-	Parent Layer: `8015286e15ef466f9df6d9109b01a20e8cd51050f5410dd4396a08797c8129dd`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `968dedac60e40af6c5724ef3d9722a9f5327213e060e2b8be08b1233d98521ef`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:07:49 GMT
-	Parent Layer: `32a1292116d7246fa8bdbde80f02abc983e698ad288976cf7c1255fee2dd46cc`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:community`

```console
$ docker pull library/couchbase@sha256:4b97abdf93c3b6087f29ff2af01a7021be4e38066dfe32c1cd0f330545c6bfba
```

-	Total Virtual Size: 372.9 MB (372881322 bytes)
-	Total v2 Content-Length: 139.1 MB (139066432 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `0468ae09390e99dc69fbfdfa34645e9088f5489138dbd7ae63b6fba20e829c62`

```dockerfile
ENV CB_VERSION=4.0.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-community_4.0.0-ubuntu12.04_amd64.deb CB_SHA256=404007eaedc3d01997eea800fcce0d0a0339bc3ab79c1c48741210f435c719f0 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:07:22 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `d7bacfc5350290a917b724a8eab1b99bf28bc3ce3c448a42b7e713638c6cb524`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:07:23 GMT
-	Parent Layer: `0468ae09390e99dc69fbfdfa34645e9088f5489138dbd7ae63b6fba20e829c62`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:58d143b7b12746889dec7f4e5950e3840c5a1956178b2d57576f8a5f851d39d8`
-	v2 Content-Length: 1.7 KB (1695 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:45:22 GMT

#### `c918cfc389e2daca2c60e01def7eb068bb64f44a753961435e820d3c8a93c4a0`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:07:43 GMT
-	Parent Layer: `d7bacfc5350290a917b724a8eab1b99bf28bc3ce3c448a42b7e713638c6cb524`
-	Docker Version: 1.8.3
-	Virtual Size: 212.0 MB (212014244 bytes)
-	v2 Blob: `sha256:6eff6949618fbd0505f1061c2f913b5641a4369916201bcbb8698110770e0f64`
-	v2 Content-Length: 87.4 MB (87372651 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:45:16 GMT

#### `ca58c031c23966b9c6dd62d01e29a5a2a166ecf01bd2fef9bf59e4423a7cda19`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:07:46 GMT
-	Parent Layer: `c918cfc389e2daca2c60e01def7eb068bb64f44a753961435e820d3c8a93c4a0`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:dc663f718893427e056db0c88b0af798aa21d28d194a370fef5e5819920fa8cb`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:44:37 GMT

#### `8ea9b56e2046c06886759aa734d98fad8ad14019a934006bc372933c49031566`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:07:46 GMT
-	Parent Layer: `ca58c031c23966b9c6dd62d01e29a5a2a166ecf01bd2fef9bf59e4423a7cda19`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:2b0577d10daafd953271cf331ee983fd0383ecaaedd75f5360bb65b307b08fa1`
-	v2 Content-Length: 251.0 B
-	v2 Last-Modified: Fri, 02 Oct 2015 21:51:53 GMT

#### `4c45b0cdb9a2f56e69121298031e47fdfcc30b2efbeb364a434576f78497bdc0`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:07:47 GMT
-	Parent Layer: `8ea9b56e2046c06886759aa734d98fad8ad14019a934006bc372933c49031566`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `8015286e15ef466f9df6d9109b01a20e8cd51050f5410dd4396a08797c8129dd`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:07:47 GMT
-	Parent Layer: `4c45b0cdb9a2f56e69121298031e47fdfcc30b2efbeb364a434576f78497bdc0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32a1292116d7246fa8bdbde80f02abc983e698ad288976cf7c1255fee2dd46cc`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:07:48 GMT
-	Parent Layer: `8015286e15ef466f9df6d9109b01a20e8cd51050f5410dd4396a08797c8129dd`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `968dedac60e40af6c5724ef3d9722a9f5327213e060e2b8be08b1233d98521ef`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:07:49 GMT
-	Parent Layer: `32a1292116d7246fa8bdbde80f02abc983e698ad288976cf7c1255fee2dd46cc`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:3.1.0`

```console
$ docker pull library/couchbase@sha256:9b36fa3b52984574f4266dae595cf99e246891a494407406c56368ae0cd510b2
```

-	Total Virtual Size: 806.0 MB (805955032 bytes)
-	Total v2 Content-Length: 264.8 MB (264809415 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `520c3e9613b210079c5e632efce721a8d42a9459d5f0c5709767c883dba3faa8`

```dockerfile
ENV CB_VERSION=3.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.1.0-ubuntu12.04_amd64.deb CB_SHA256=8eed4c768816ac22f6627d05516fa8a6975571b32b354c4f16185d8654f5bc1c PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:08:38 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `338708940ac4f3de29a80d103465be449a80010dd6aebbeff9b48c0a02264e6d`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:08:39 GMT
-	Parent Layer: `520c3e9613b210079c5e632efce721a8d42a9459d5f0c5709767c883dba3faa8`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:0683b7a71c75ce0ab3e54fc41f8c004104ec2341e24a766ba40f59d11af3f421`
-	v2 Content-Length: 1.7 KB (1696 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:48:37 GMT

#### `14823282ecd8a4678109f6fa923d1b75d865789ddd0bae325045974dc586b69f`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:09:05 GMT
-	Parent Layer: `338708940ac4f3de29a80d103465be449a80010dd6aebbeff9b48c0a02264e6d`
-	Docker Version: 1.8.3
-	Virtual Size: 645.1 MB (645087954 bytes)
-	v2 Blob: `sha256:38d6081ea125979a4c1f9b6922d7ed870f7be6b14c56a73e1fb5198273d91d92`
-	v2 Content-Length: 213.1 MB (213115628 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:48:23 GMT

#### `fac81895bdc5d91e8c13593e112d1e7ba007557f2cde81f5ff0204dd3fc6e0d3`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:09:12 GMT
-	Parent Layer: `14823282ecd8a4678109f6fa923d1b75d865789ddd0bae325045974dc586b69f`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a05b753a13dce2ee91632c6d3a169c16c24a991bbaccf110c68fc0088a36a64e`
-	v2 Content-Length: 341.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:46:48 GMT

#### `85aa55e90418dcd1d774b65f710a45abb41a71e3e950042069be17cc09e3c84c`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:09:12 GMT
-	Parent Layer: `fac81895bdc5d91e8c13593e112d1e7ba007557f2cde81f5ff0204dd3fc6e0d3`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `e29d29962acd2fd05956fcf62c0d2a30b4665e0cbd801d7ff1d64d96f3cb0503`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:09:13 GMT
-	Parent Layer: `85aa55e90418dcd1d774b65f710a45abb41a71e3e950042069be17cc09e3c84c`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `37c3792146da1811cb800adcc464549502c0dcb52c71831602193d6c73df07a4`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:09:13 GMT
-	Parent Layer: `e29d29962acd2fd05956fcf62c0d2a30b4665e0cbd801d7ff1d64d96f3cb0503`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f1829ce8cf3d129fd392d86a50d01d5416093181867f697312323d7392e8190a`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:09:14 GMT
-	Parent Layer: `37c3792146da1811cb800adcc464549502c0dcb52c71831602193d6c73df07a4`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `ef46d4294cc49b2759359f22202c829668c6946be4d39955b2d58da4e5a481c2`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:09:15 GMT
-	Parent Layer: `f1829ce8cf3d129fd392d86a50d01d5416093181867f697312323d7392e8190a`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-3.1.0`

```console
$ docker pull library/couchbase@sha256:fd44d4320872fd1339c443f5b31132941adc291f9aea3912d8673f6c2f018c04
```

-	Total Virtual Size: 806.0 MB (805955032 bytes)
-	Total v2 Content-Length: 264.8 MB (264809415 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `520c3e9613b210079c5e632efce721a8d42a9459d5f0c5709767c883dba3faa8`

```dockerfile
ENV CB_VERSION=3.1.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.1.0-ubuntu12.04_amd64.deb CB_SHA256=8eed4c768816ac22f6627d05516fa8a6975571b32b354c4f16185d8654f5bc1c PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:08:38 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `338708940ac4f3de29a80d103465be449a80010dd6aebbeff9b48c0a02264e6d`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:08:39 GMT
-	Parent Layer: `520c3e9613b210079c5e632efce721a8d42a9459d5f0c5709767c883dba3faa8`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:0683b7a71c75ce0ab3e54fc41f8c004104ec2341e24a766ba40f59d11af3f421`
-	v2 Content-Length: 1.7 KB (1696 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:48:37 GMT

#### `14823282ecd8a4678109f6fa923d1b75d865789ddd0bae325045974dc586b69f`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:09:05 GMT
-	Parent Layer: `338708940ac4f3de29a80d103465be449a80010dd6aebbeff9b48c0a02264e6d`
-	Docker Version: 1.8.3
-	Virtual Size: 645.1 MB (645087954 bytes)
-	v2 Blob: `sha256:38d6081ea125979a4c1f9b6922d7ed870f7be6b14c56a73e1fb5198273d91d92`
-	v2 Content-Length: 213.1 MB (213115628 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:48:23 GMT

#### `fac81895bdc5d91e8c13593e112d1e7ba007557f2cde81f5ff0204dd3fc6e0d3`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:09:12 GMT
-	Parent Layer: `14823282ecd8a4678109f6fa923d1b75d865789ddd0bae325045974dc586b69f`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a05b753a13dce2ee91632c6d3a169c16c24a991bbaccf110c68fc0088a36a64e`
-	v2 Content-Length: 341.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:46:48 GMT

#### `85aa55e90418dcd1d774b65f710a45abb41a71e3e950042069be17cc09e3c84c`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:09:12 GMT
-	Parent Layer: `fac81895bdc5d91e8c13593e112d1e7ba007557f2cde81f5ff0204dd3fc6e0d3`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `e29d29962acd2fd05956fcf62c0d2a30b4665e0cbd801d7ff1d64d96f3cb0503`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:09:13 GMT
-	Parent Layer: `85aa55e90418dcd1d774b65f710a45abb41a71e3e950042069be17cc09e3c84c`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `37c3792146da1811cb800adcc464549502c0dcb52c71831602193d6c73df07a4`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:09:13 GMT
-	Parent Layer: `e29d29962acd2fd05956fcf62c0d2a30b4665e0cbd801d7ff1d64d96f3cb0503`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f1829ce8cf3d129fd392d86a50d01d5416093181867f697312323d7392e8190a`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:09:14 GMT
-	Parent Layer: `37c3792146da1811cb800adcc464549502c0dcb52c71831602193d6c73df07a4`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `ef46d4294cc49b2759359f22202c829668c6946be4d39955b2d58da4e5a481c2`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:09:15 GMT
-	Parent Layer: `f1829ce8cf3d129fd392d86a50d01d5416093181867f697312323d7392e8190a`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:3.0.3`

```console
$ docker pull library/couchbase@sha256:4728e014cdb1be12481af3cfe47c7062dc624d4e7590d841cd832b89492df5ed
```

-	Total Virtual Size: 805.1 MB (805148886 bytes)
-	Total v2 Content-Length: 264.5 MB (264536516 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `40707879edb3a1028fc91c7b75aa8ad681b30393f8f687d118ba626e38090780`

```dockerfile
ENV CB_VERSION=3.0.3 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.0.3-ubuntu12.04_amd64.deb CB_SHA256=13e925fa8b806aecd09751bdb7be1f8cfa188ad894e266108e8c44785c08e474 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:09:59 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `44a4a35a1977ce65ae8b8b93fe6ddda6ad9540e480c5d38c419ec67e771e52c9`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:10:00 GMT
-	Parent Layer: `40707879edb3a1028fc91c7b75aa8ad681b30393f8f687d118ba626e38090780`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:3ff5d016dc73d4c0b60defc0ec3df79289083f411f593f21176ef18072d2ed92`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:52:53 GMT

#### `06691b1574d86a88e68cd364dd9f333656b59646b464c4ddf531ba13646f5d8c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:11:19 GMT
-	Parent Layer: `44a4a35a1977ce65ae8b8b93fe6ddda6ad9540e480c5d38c419ec67e771e52c9`
-	Docker Version: 1.8.3
-	Virtual Size: 644.3 MB (644281808 bytes)
-	v2 Blob: `sha256:81bc5dc96a0609dfda460587918a8a688bc7e34609325cdeca6676840d9ac50a`
-	v2 Content-Length: 212.8 MB (212842730 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:52:45 GMT

#### `d8e71227f95166f55468bd195f3f8e66a966536a13a5937feef37deaf53c5c46`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:11:28 GMT
-	Parent Layer: `06691b1574d86a88e68cd364dd9f333656b59646b464c4ddf531ba13646f5d8c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:0e3d711bdec62970474a12cefdbeb0dd1f83875070c4c85b82c6185930a2e4c5`
-	v2 Content-Length: 342.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:50:58 GMT

#### `28d59e1a0b00fddf8a89fb8dabc78108e1648ab8d8e15c86daec20d3165f87c2`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:11:28 GMT
-	Parent Layer: `d8e71227f95166f55468bd195f3f8e66a966536a13a5937feef37deaf53c5c46`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `599133ae5b35083742107b953fb61c677bb326fd04179df3dccbb4e9a3bde2a5`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:11:29 GMT
-	Parent Layer: `28d59e1a0b00fddf8a89fb8dabc78108e1648ab8d8e15c86daec20d3165f87c2`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `8e81b7162aca4f0f90ee351a46aab9dc2b72a0e75dab306f8a5783122b3e8f8d`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:11:29 GMT
-	Parent Layer: `599133ae5b35083742107b953fb61c677bb326fd04179df3dccbb4e9a3bde2a5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `421b046713efbd5d5e5ad5c5205111beca05d4f48cb4d276a23d10950b308116`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:11:30 GMT
-	Parent Layer: `8e81b7162aca4f0f90ee351a46aab9dc2b72a0e75dab306f8a5783122b3e8f8d`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a412a4b0622627d3e87a3641c57c6701c5ec6e1452479b45832c4100ef8c272`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:11:30 GMT
-	Parent Layer: `421b046713efbd5d5e5ad5c5205111beca05d4f48cb4d276a23d10950b308116`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-3.0.3`

```console
$ docker pull library/couchbase@sha256:0943b0d5c82dc63cda7ec53a334d6807a9cab37f40d7a0f49fe53f3462418497
```

-	Total Virtual Size: 805.1 MB (805148886 bytes)
-	Total v2 Content-Length: 264.5 MB (264536516 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `40707879edb3a1028fc91c7b75aa8ad681b30393f8f687d118ba626e38090780`

```dockerfile
ENV CB_VERSION=3.0.3 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.0.3-ubuntu12.04_amd64.deb CB_SHA256=13e925fa8b806aecd09751bdb7be1f8cfa188ad894e266108e8c44785c08e474 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:09:59 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `44a4a35a1977ce65ae8b8b93fe6ddda6ad9540e480c5d38c419ec67e771e52c9`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:10:00 GMT
-	Parent Layer: `40707879edb3a1028fc91c7b75aa8ad681b30393f8f687d118ba626e38090780`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:3ff5d016dc73d4c0b60defc0ec3df79289083f411f593f21176ef18072d2ed92`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:52:53 GMT

#### `06691b1574d86a88e68cd364dd9f333656b59646b464c4ddf531ba13646f5d8c`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:11:19 GMT
-	Parent Layer: `44a4a35a1977ce65ae8b8b93fe6ddda6ad9540e480c5d38c419ec67e771e52c9`
-	Docker Version: 1.8.3
-	Virtual Size: 644.3 MB (644281808 bytes)
-	v2 Blob: `sha256:81bc5dc96a0609dfda460587918a8a688bc7e34609325cdeca6676840d9ac50a`
-	v2 Content-Length: 212.8 MB (212842730 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:52:45 GMT

#### `d8e71227f95166f55468bd195f3f8e66a966536a13a5937feef37deaf53c5c46`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:11:28 GMT
-	Parent Layer: `06691b1574d86a88e68cd364dd9f333656b59646b464c4ddf531ba13646f5d8c`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:0e3d711bdec62970474a12cefdbeb0dd1f83875070c4c85b82c6185930a2e4c5`
-	v2 Content-Length: 342.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:50:58 GMT

#### `28d59e1a0b00fddf8a89fb8dabc78108e1648ab8d8e15c86daec20d3165f87c2`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:11:28 GMT
-	Parent Layer: `d8e71227f95166f55468bd195f3f8e66a966536a13a5937feef37deaf53c5c46`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `599133ae5b35083742107b953fb61c677bb326fd04179df3dccbb4e9a3bde2a5`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:11:29 GMT
-	Parent Layer: `28d59e1a0b00fddf8a89fb8dabc78108e1648ab8d8e15c86daec20d3165f87c2`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `8e81b7162aca4f0f90ee351a46aab9dc2b72a0e75dab306f8a5783122b3e8f8d`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:11:29 GMT
-	Parent Layer: `599133ae5b35083742107b953fb61c677bb326fd04179df3dccbb4e9a3bde2a5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `421b046713efbd5d5e5ad5c5205111beca05d4f48cb4d276a23d10950b308116`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:11:30 GMT
-	Parent Layer: `8e81b7162aca4f0f90ee351a46aab9dc2b72a0e75dab306f8a5783122b3e8f8d`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a412a4b0622627d3e87a3641c57c6701c5ec6e1452479b45832c4100ef8c272`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:11:30 GMT
-	Parent Layer: `421b046713efbd5d5e5ad5c5205111beca05d4f48cb4d276a23d10950b308116`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:3.0.2`

```console
$ docker pull library/couchbase@sha256:1f9780963227bc714290f9dbf34b1209427970facb9af1cdf668be73fee0fb36
```

-	Total Virtual Size: 805.2 MB (805163751 bytes)
-	Total v2 Content-Length: 264.5 MB (264544349 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `dc7cb462e31fe962d9d8a4bab558add11012ed999c08ca9afa9daacb0424b452`

```dockerfile
ENV CB_VERSION=3.0.2 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.0.2-ubuntu12.04_amd64.deb CB_SHA256=29490c49f4ba5e25fe68db9abe7a78f884a0ea47c7825813b50fd5b9c2bf691c PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:12:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `78f60a3df3caa12d497f1a80d4bf209b55515829a81b6c44fc4555fef1850c06`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:12:21 GMT
-	Parent Layer: `dc7cb462e31fe962d9d8a4bab558add11012ed999c08ca9afa9daacb0424b452`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:f7d775496cba1a0541d173db367e64d55cd1802ad09e4575a7bbccee356237ff`
-	v2 Content-Length: 1.7 KB (1697 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:57:02 GMT

#### `78dabfd50f2b4bd8952b23d45491adc2c83f3c3d5cfd5bdb544b3097bfdd8aaa`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:12:59 GMT
-	Parent Layer: `78f60a3df3caa12d497f1a80d4bf209b55515829a81b6c44fc4555fef1850c06`
-	Docker Version: 1.8.3
-	Virtual Size: 644.3 MB (644296673 bytes)
-	v2 Blob: `sha256:e69b55ba9273f80128494154dd853a0a4f9ecf407b248cff59f411bd0042e38c`
-	v2 Content-Length: 212.9 MB (212850564 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:56:50 GMT

#### `d33b7dc696a25f76cffc15b0a689e9bdad081113c5296a53e789afb7a786232e`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:13:08 GMT
-	Parent Layer: `78dabfd50f2b4bd8952b23d45491adc2c83f3c3d5cfd5bdb544b3097bfdd8aaa`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:447164feb1586ef089d23e01086041daefccb9bb20b37c25ca42525fd02ec977`
-	v2 Content-Length: 338.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:55:13 GMT

#### `1fa04497004bf9499c667a6253b288e631e20a91cc4af64292915d537b11577b`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:13:09 GMT
-	Parent Layer: `d33b7dc696a25f76cffc15b0a689e9bdad081113c5296a53e789afb7a786232e`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `c215b03aad68fd687f96d4384c811c2aa9ffda4c6f99707199b8ae7245b0e2f3`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:13:09 GMT
-	Parent Layer: `1fa04497004bf9499c667a6253b288e631e20a91cc4af64292915d537b11577b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `58396904a2358bee51ec07918b5b1129bf2b12616b88d49ea102e95513d15c63`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:13:10 GMT
-	Parent Layer: `c215b03aad68fd687f96d4384c811c2aa9ffda4c6f99707199b8ae7245b0e2f3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `3ce6403eb2c65cb0c73ce50da3152c3d2e21537c236ca1a2df9c450f481ef912`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:13:10 GMT
-	Parent Layer: `58396904a2358bee51ec07918b5b1129bf2b12616b88d49ea102e95513d15c63`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `6e66e9ec26b357ed5ca7b98344da5ec60395cc9c792fffa45f92a073861a2f0c`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:13:11 GMT
-	Parent Layer: `3ce6403eb2c65cb0c73ce50da3152c3d2e21537c236ca1a2df9c450f481ef912`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-3.0.2`

```console
$ docker pull library/couchbase@sha256:e07d90ec470c9b5ad6dec00713f2d8335329a12dce3d8b1296ac2dd95483ed98
```

-	Total Virtual Size: 805.2 MB (805163751 bytes)
-	Total v2 Content-Length: 264.5 MB (264544349 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `dc7cb462e31fe962d9d8a4bab558add11012ed999c08ca9afa9daacb0424b452`

```dockerfile
ENV CB_VERSION=3.0.2 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_3.0.2-ubuntu12.04_amd64.deb CB_SHA256=29490c49f4ba5e25fe68db9abe7a78f884a0ea47c7825813b50fd5b9c2bf691c PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:12:19 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `78f60a3df3caa12d497f1a80d4bf209b55515829a81b6c44fc4555fef1850c06`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:12:21 GMT
-	Parent Layer: `dc7cb462e31fe962d9d8a4bab558add11012ed999c08ca9afa9daacb0424b452`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:f7d775496cba1a0541d173db367e64d55cd1802ad09e4575a7bbccee356237ff`
-	v2 Content-Length: 1.7 KB (1697 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:57:02 GMT

#### `78dabfd50f2b4bd8952b23d45491adc2c83f3c3d5cfd5bdb544b3097bfdd8aaa`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:12:59 GMT
-	Parent Layer: `78f60a3df3caa12d497f1a80d4bf209b55515829a81b6c44fc4555fef1850c06`
-	Docker Version: 1.8.3
-	Virtual Size: 644.3 MB (644296673 bytes)
-	v2 Blob: `sha256:e69b55ba9273f80128494154dd853a0a4f9ecf407b248cff59f411bd0042e38c`
-	v2 Content-Length: 212.9 MB (212850564 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:56:50 GMT

#### `d33b7dc696a25f76cffc15b0a689e9bdad081113c5296a53e789afb7a786232e`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:13:08 GMT
-	Parent Layer: `78dabfd50f2b4bd8952b23d45491adc2c83f3c3d5cfd5bdb544b3097bfdd8aaa`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:447164feb1586ef089d23e01086041daefccb9bb20b37c25ca42525fd02ec977`
-	v2 Content-Length: 338.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:55:13 GMT

#### `1fa04497004bf9499c667a6253b288e631e20a91cc4af64292915d537b11577b`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:13:09 GMT
-	Parent Layer: `d33b7dc696a25f76cffc15b0a689e9bdad081113c5296a53e789afb7a786232e`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `c215b03aad68fd687f96d4384c811c2aa9ffda4c6f99707199b8ae7245b0e2f3`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:13:09 GMT
-	Parent Layer: `1fa04497004bf9499c667a6253b288e631e20a91cc4af64292915d537b11577b`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `58396904a2358bee51ec07918b5b1129bf2b12616b88d49ea102e95513d15c63`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:13:10 GMT
-	Parent Layer: `c215b03aad68fd687f96d4384c811c2aa9ffda4c6f99707199b8ae7245b0e2f3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `3ce6403eb2c65cb0c73ce50da3152c3d2e21537c236ca1a2df9c450f481ef912`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:13:10 GMT
-	Parent Layer: `58396904a2358bee51ec07918b5b1129bf2b12616b88d49ea102e95513d15c63`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `6e66e9ec26b357ed5ca7b98344da5ec60395cc9c792fffa45f92a073861a2f0c`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:13:11 GMT
-	Parent Layer: `3ce6403eb2c65cb0c73ce50da3152c3d2e21537c236ca1a2df9c450f481ef912`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:community-3.0.1`

```console
$ docker pull library/couchbase@sha256:b8a58f9801d55810188e00fe8ffe88886bf490e4fb9417e91b8fd4ab3a2e1fbb
```

-	Total Virtual Size: 806.0 MB (806023878 bytes)
-	Total v2 Content-Length: 264.9 MB (264879657 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2  &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:03:18 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 23.6 MB (23571059 bytes)
-	v2 Blob: `sha256:0bc56fd185bdf82fa5d1e40f91e527e6ffe9e060c34413441a5c98d79671eafb`
-	v2 Content-Length: 7.5 MB (7496733 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 18:39:05 GMT

#### `cd1fff9ea0e4faf50e8c46aa4781eebbc76a91b6464ac76d9a26a56c03e92bad`

```dockerfile
ENV CB_VERSION=3.0.1 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-community_3.0.1-ubuntu12.04_amd64.deb CB_SHA256=59efbd8924969f71c9a6b438afea94d974db51607464c55d7a2d527368026150 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:14:00 GMT
-	Parent Layer: `32132a7c82e99edf9b1f929d52e9faaeb13571d28f464f6058ad6ddbcce762e0`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1c9b5a56deeb8c8d69d656dc53f5ab07ac6e248614024b7e4d623f7985da4601`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:14:01 GMT
-	Parent Layer: `cd1fff9ea0e4faf50e8c46aa4781eebbc76a91b6464ac76d9a26a56c03e92bad`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:8bf3c1c0302fefe42e0d2e21de6466f3e61cf8579a60598d6ed0dd38bd8d76cf`
-	v2 Content-Length: 1.7 KB (1696 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:01:09 GMT

#### `e16365e3ef8bcd3101123c8ea9fe6d8a1cea130e93f31fe70f5755153005539f`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:15:16 GMT
-	Parent Layer: `1c9b5a56deeb8c8d69d656dc53f5ab07ac6e248614024b7e4d623f7985da4601`
-	Docker Version: 1.8.3
-	Virtual Size: 645.2 MB (645156800 bytes)
-	v2 Blob: `sha256:dc076fb6052f6c327397673f91f15a90495ea0cf376956d05f4336ce8c38e0f8`
-	v2 Content-Length: 213.2 MB (213185874 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:00:56 GMT

#### `61f84ae45caaecf6d2e3825b22a399695e8222dcef053d6cb4001a970e3e63b4`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:15:26 GMT
-	Parent Layer: `e16365e3ef8bcd3101123c8ea9fe6d8a1cea130e93f31fe70f5755153005539f`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:abb178a9a5f15bfa2575b74a03251c64479f5851f86cc9882930b7951f00fb13`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 18:59:22 GMT

#### `5e28e6c2980f0942e30f20031e75f97f89b5bfbb28d9521286ebee080fc58dfd`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:15:26 GMT
-	Parent Layer: `61f84ae45caaecf6d2e3825b22a399695e8222dcef053d6cb4001a970e3e63b4`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `3cdba7609a7042c91a82d0a27975a6c20449a3a610740da1b077ef0a6633d727`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:15:27 GMT
-	Parent Layer: `5e28e6c2980f0942e30f20031e75f97f89b5bfbb28d9521286ebee080fc58dfd`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `972fc599726f8d5a0301262cbfd74f4d56374fc9f5e1b7ecc384f79caf7ce4aa`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:15:27 GMT
-	Parent Layer: `3cdba7609a7042c91a82d0a27975a6c20449a3a610740da1b077ef0a6633d727`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `16030775c946b0f89e7d2a6450c101016d897611e6308ff323fad0174afe5f6f`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:15:28 GMT
-	Parent Layer: `972fc599726f8d5a0301262cbfd74f4d56374fc9f5e1b7ecc384f79caf7ce4aa`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `27e10d86d75b9622b19b82d96aab190afd5ecc22956afb09a7d1d4225aaeae01`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:15:29 GMT
-	Parent Layer: `16030775c946b0f89e7d2a6450c101016d897611e6308ff323fad0174afe5f6f`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:2.5.2`

```console
$ docker pull library/couchbase@sha256:6e5dfef50d7396a8fb6392d2874326fc5e19ffca5bd6ade659242e26ea57d22e
```

-	Total Virtual Size: 585.5 MB (585531067 bytes)
-	Total v2 Content-Length: 194.0 MB (194048165 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2 librtmp0 &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:15:57 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 25.4 MB (25365920 bytes)
-	v2 Blob: `sha256:9a241bd5ce98351780c4b7a3fd547f88402d06d4c0edb8666f239b74f6f50756`
-	v2 Content-Length: 8.4 MB (8386912 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:41 GMT

#### `4bbf51940cd0475549678c9915570534509732166cdb4809e6a30ccad410b832`

```dockerfile
ENV CB_VERSION=2.5.2 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_2.5.2_x86_64.deb CB_SHA256=27a79a65758023c34ed900e8ef8c54bab4a65f4c84b7c94359cba910800a4b19 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:15:59 GMT
-	Parent Layer: `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `d2e95089851c4c035efa10c82d3da985bd9bc4cad0754ac898e528c681c95265`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:16:00 GMT
-	Parent Layer: `4bbf51940cd0475549678c9915570534509732166cdb4809e6a30ccad410b832`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:42dd735f2dfea75646f8318be5c6492c77c376aa0bb88d9e2ba44de5aad96315`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:30 GMT

#### `fa508966e818bfccf7cda3a6b5fcd724f7c410326930e9d8f298727dd0a67784`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:16:53 GMT
-	Parent Layer: `d2e95089851c4c035efa10c82d3da985bd9bc4cad0754ac898e528c681c95265`
-	Docker Version: 1.8.3
-	Virtual Size: 422.9 MB (422869128 bytes)
-	v2 Blob: `sha256:42438c1c114b021314e26f2fd8327aaf8367a98e75feb5a43b8513e7de2ab1be`
-	v2 Content-Length: 141.5 MB (141464201 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:22 GMT

#### `c56940286fcbf838b0b92822407fc25615ae60a3dd274985d2dd9c626082e844`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:16:58 GMT
-	Parent Layer: `fa508966e818bfccf7cda3a6b5fcd724f7c410326930e9d8f298727dd0a67784`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a9ebdb0f37e56ee4577599096bc8687fa0689a6251376f6c8de71b7d386db5b7`
-	v2 Content-Length: 341.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 19:03:15 GMT

#### `40e272771ca9c790d27ae4158a6bde108c7420d7de338d19bf1b8a037a7616bd`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:16:58 GMT
-	Parent Layer: `c56940286fcbf838b0b92822407fc25615ae60a3dd274985d2dd9c626082e844`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `662ca364b8e9be2230c3ea6cd5793f8287b6ff79154ac71d3c8cb5c4fba752c2`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:16:59 GMT
-	Parent Layer: `40e272771ca9c790d27ae4158a6bde108c7420d7de338d19bf1b8a037a7616bd`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `006efe790ff4860cea3ebbd4dd8f666ac4c13e714943796908db9e4c59c8eff3`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:16:59 GMT
-	Parent Layer: `662ca364b8e9be2230c3ea6cd5793f8287b6ff79154ac71d3c8cb5c4fba752c2`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `fd4281c914a7369269befabf5e9ab93bb79bd0a07c1cbc3128b2de4a32592df5`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:17:00 GMT
-	Parent Layer: `006efe790ff4860cea3ebbd4dd8f666ac4c13e714943796908db9e4c59c8eff3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f9a31a1060a97d7e7bc754f0486fef6e51f390d7a79fa9187f29816ee04babc0`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:17:00 GMT
-	Parent Layer: `fd4281c914a7369269befabf5e9ab93bb79bd0a07c1cbc3128b2de4a32592df5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:enterprise-2.5.2`

```console
$ docker pull library/couchbase@sha256:1b5f8540bed6ab402dfaedbb5a33ed01901eb7f1533c702531c6d33fa52abd73
```

-	Total Virtual Size: 585.5 MB (585531067 bytes)
-	Total v2 Content-Length: 194.0 MB (194048165 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2 librtmp0 &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:15:57 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 25.4 MB (25365920 bytes)
-	v2 Blob: `sha256:9a241bd5ce98351780c4b7a3fd547f88402d06d4c0edb8666f239b74f6f50756`
-	v2 Content-Length: 8.4 MB (8386912 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:41 GMT

#### `4bbf51940cd0475549678c9915570534509732166cdb4809e6a30ccad410b832`

```dockerfile
ENV CB_VERSION=2.5.2 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-enterprise_2.5.2_x86_64.deb CB_SHA256=27a79a65758023c34ed900e8ef8c54bab4a65f4c84b7c94359cba910800a4b19 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:15:59 GMT
-	Parent Layer: `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `d2e95089851c4c035efa10c82d3da985bd9bc4cad0754ac898e528c681c95265`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:16:00 GMT
-	Parent Layer: `4bbf51940cd0475549678c9915570534509732166cdb4809e6a30ccad410b832`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:42dd735f2dfea75646f8318be5c6492c77c376aa0bb88d9e2ba44de5aad96315`
-	v2 Content-Length: 1.7 KB (1694 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:30 GMT

#### `fa508966e818bfccf7cda3a6b5fcd724f7c410326930e9d8f298727dd0a67784`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:16:53 GMT
-	Parent Layer: `d2e95089851c4c035efa10c82d3da985bd9bc4cad0754ac898e528c681c95265`
-	Docker Version: 1.8.3
-	Virtual Size: 422.9 MB (422869128 bytes)
-	v2 Blob: `sha256:42438c1c114b021314e26f2fd8327aaf8367a98e75feb5a43b8513e7de2ab1be`
-	v2 Content-Length: 141.5 MB (141464201 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:22 GMT

#### `c56940286fcbf838b0b92822407fc25615ae60a3dd274985d2dd9c626082e844`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:16:58 GMT
-	Parent Layer: `fa508966e818bfccf7cda3a6b5fcd724f7c410326930e9d8f298727dd0a67784`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:a9ebdb0f37e56ee4577599096bc8687fa0689a6251376f6c8de71b7d386db5b7`
-	v2 Content-Length: 341.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 19:03:15 GMT

#### `40e272771ca9c790d27ae4158a6bde108c7420d7de338d19bf1b8a037a7616bd`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:16:58 GMT
-	Parent Layer: `c56940286fcbf838b0b92822407fc25615ae60a3dd274985d2dd9c626082e844`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `662ca364b8e9be2230c3ea6cd5793f8287b6ff79154ac71d3c8cb5c4fba752c2`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:16:59 GMT
-	Parent Layer: `40e272771ca9c790d27ae4158a6bde108c7420d7de338d19bf1b8a037a7616bd`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `006efe790ff4860cea3ebbd4dd8f666ac4c13e714943796908db9e4c59c8eff3`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:16:59 GMT
-	Parent Layer: `662ca364b8e9be2230c3ea6cd5793f8287b6ff79154ac71d3c8cb5c4fba752c2`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `fd4281c914a7369269befabf5e9ab93bb79bd0a07c1cbc3128b2de4a32592df5`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:17:00 GMT
-	Parent Layer: `006efe790ff4860cea3ebbd4dd8f666ac4c13e714943796908db9e4c59c8eff3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f9a31a1060a97d7e7bc754f0486fef6e51f390d7a79fa9187f29816ee04babc0`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:17:00 GMT
-	Parent Layer: `fd4281c914a7369269befabf5e9ab93bb79bd0a07c1cbc3128b2de4a32592df5`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `couchbase:community-2.2.0`

```console
$ docker pull library/couchbase@sha256:c8ad33132c11c89f018063ab8d663b8b9069c76c40d49e8e45d8e03f46030a7e
```

-	Total Virtual Size: 575.9 MB (575941585 bytes)
-	Total v2 Content-Length: 190.6 MB (190599529 bytes)

### Layers (15)

#### `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`

```dockerfile
ADD file:229d73f889fbb1411ffecab12ab25e0a52a96c69cb958bb85867283ef6f42c3e in /
```

-	Created: Tue, 08 Dec 2015 18:37:30 GMT
-	Docker Version: 1.8.3
-	Virtual Size: 136.8 MB (136808666 bytes)
-	v2 Blob: `sha256:a50d2b3f7efa86e3b168a2bedc4f3ab29f98dd07eeaa20f197bd23f8e9cfef6d`
-	v2 Content-Length: 44.1 MB (44135998 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:01:15 GMT

#### `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`

```dockerfile
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d \
	&& echo 'exit 101' >> /usr/sbin/policy-rc.d \
	&& chmod +x /usr/sbin/policy-rc.d \
		&& dpkg-divert --local --rename --add /sbin/initctl \
	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl \
	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl \
		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup \
		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean \
	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean \
	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean \
		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages \
		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes
```

-	Created: Tue, 08 Dec 2015 18:37:35 GMT
-	Parent Layer: `62baed0d0de51dde3ecbee4eda961d0115fc811fde3ebb36decc182c7786a8dd`
-	Docker Version: 1.8.3
-	Virtual Size: 156.2 KB (156213 bytes)
-	v2 Blob: `sha256:27e1b0c788a28af594d2023dc2f3e1552158f935ceed119389463ff8a58b65b4`
-	v2 Content-Length: 57.9 KB (57863 bytes)
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:48 GMT

#### `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`

```dockerfile
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
```

-	Created: Tue, 08 Dec 2015 18:37:36 GMT
-	Parent Layer: `39387babd60fd7a982016cf8dc7b60b7866394f42df755e4d917771d11869bf5`
-	Docker Version: 1.8.3
-	Virtual Size: 1.9 KB (1911 bytes)
-	v2 Blob: `sha256:622b8fa00f815b90439859cc2202b493383761bd3eaf942462282ba1f2dbf5a5`
-	v2 Content-Length: 680.0 B
-	v2 Last-Modified: Tue, 08 Dec 2015 19:00:42 GMT

#### `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Tue, 08 Dec 2015 18:37:37 GMT
-	Parent Layer: `6a2bc8404be06fedbfaf2a865ca8a5d0373b3dd97f3ec708b4c05a488fdb0558`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`

```dockerfile
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
```

-	Created: Mon, 14 Dec 2015 18:02:56 GMT
-	Parent Layer: `bad926a6fb50d7421fb0aea77dddf7b1f6b9fa8fdb7aaf47644a662371a188a3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`

```dockerfile
RUN apt-get update &&\
     apt-get install -yq runit wget python-httplib2 librtmp0 &&\
     apt-get autoremove && apt-get clean &&\
     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```

-	Created: Mon, 14 Dec 2015 18:15:57 GMT
-	Parent Layer: `1a86c4c907e0a72e0874d1c526e3f877fc6d0fc8bab275ab4c75bf4d89ebaccc`
-	Docker Version: 1.8.3
-	Virtual Size: 25.4 MB (25365920 bytes)
-	v2 Blob: `sha256:9a241bd5ce98351780c4b7a3fd547f88402d06d4c0edb8666f239b74f6f50756`
-	v2 Content-Length: 8.4 MB (8386912 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:04:41 GMT

#### `6e1c021cd64dea7cf77029dd393f772286a23a9e1f0971aebc51c93c01e5839e`

```dockerfile
ENV CB_VERSION=2.2.0 CB_RELEASE_URL=http://packages.couchbase.com/releases CB_PACKAGE=couchbase-server-community_2.2.0_x86_64.deb CB_SHA256=051b0905e13241de19fbd9efb1e22a421f33429a1db3e4b5e3ae8756b9e4d6a2 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install LD_LIBRARY_PATH=:/opt/couchbase/lib
```

-	Created: Mon, 14 Dec 2015 18:17:45 GMT
-	Parent Layer: `25d20a0bab1edcfade8de6764e60ff24d66f7847a8ad6ca1a9cf8277dcd4f098`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `eda07b768897cb8372e2c0de7e3c1fe50ff3c744e9961341d37d08d23de9393c`

```dockerfile
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
```

-	Created: Mon, 14 Dec 2015 18:17:46 GMT
-	Parent Layer: `6e1c021cd64dea7cf77029dd393f772286a23a9e1f0971aebc51c93c01e5839e`
-	Docker Version: 1.8.3
-	Virtual Size: 328.7 KB (328658 bytes)
-	v2 Blob: `sha256:5641fd14b2749e1e11b353bdceb97314d98748cccb0f679535ee8e337a8fd5fd`
-	v2 Content-Length: 1.7 KB (1695 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:08:06 GMT

#### `4448d656fe4af74ebe90b67f5d24fa330160975eb97d1ca56d0245836e701042`

```dockerfile
RUN wget -N $CB_RELEASE_URL/$CB_VERSION/$CB_PACKAGE &&\
     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&\
     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
```

-	Created: Mon, 14 Dec 2015 18:18:35 GMT
-	Parent Layer: `eda07b768897cb8372e2c0de7e3c1fe50ff3c744e9961341d37d08d23de9393c`
-	Docker Version: 1.8.3
-	Virtual Size: 413.3 MB (413279646 bytes)
-	v2 Blob: `sha256:d4160ffca79a996b496935c66374ecbab59cb5d00d98125906e4e1562687ea85`
-	v2 Content-Length: 138.0 MB (138015568 bytes)
-	v2 Last-Modified: Mon, 14 Dec 2015 19:08:01 GMT

#### `c960f978a6c82310974e3c815fa5eddcb092246d38d4f95eb022b249451e769c`

```dockerfile
COPY file:34e32c52f0895191f5207176abf9876bf2bee271ec6128f045d81f53761b200e in /etc/service/couchbase-server/run
```

-	Created: Mon, 14 Dec 2015 18:18:39 GMT
-	Parent Layer: `4448d656fe4af74ebe90b67f5d24fa330160975eb97d1ca56d0245836e701042`
-	Docker Version: 1.8.3
-	Virtual Size: 389.0 B
-	v2 Blob: `sha256:c697f1f467ad86dd24ca2d89aaace3d1c32d111c2f3d2c65e9290fdf291d4bec`
-	v2 Content-Length: 337.0 B
-	v2 Last-Modified: Mon, 14 Dec 2015 19:06:57 GMT

#### `7968016e1749df556796b0c44446d76f3b8b12fa8d719829c1d28b56c9fbab22`

```dockerfile
COPY file:cbb44c9c65b64a9dc11725b8c88c04651718b0cc93d3a0a473856754d1d9fbd9 in /
```

-	Created: Mon, 14 Dec 2015 18:18:40 GMT
-	Parent Layer: `c960f978a6c82310974e3c815fa5eddcb092246d38d4f95eb022b249451e769c`
-	Docker Version: 1.8.3
-	Virtual Size: 182.0 B
-	v2 Blob: `sha256:3e075545d7c19a0cffcc0817160ca7fd4edb2fb3714daa26a00242c796276b09`
-	v2 Content-Length: 252.0 B
-	v2 Last-Modified: Thu, 03 Sep 2015 23:35:11 GMT

#### `6526b767d67a844946345aaf56e35d6701970084820a94db591a0c2223e732c3`

```dockerfile
ENTRYPOINT &{["/entrypoint.sh"]}
```

-	Created: Mon, 14 Dec 2015 18:18:40 GMT
-	Parent Layer: `7968016e1749df556796b0c44446d76f3b8b12fa8d719829c1d28b56c9fbab22`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `4e263b0dc20c10973a0583542368f4c1c5b767ad102764798e0e5dc6295b57e2`

```dockerfile
CMD ["couchbase-server"]
```

-	Created: Mon, 14 Dec 2015 18:18:41 GMT
-	Parent Layer: `6526b767d67a844946345aaf56e35d6701970084820a94db591a0c2223e732c3`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `41da4d95ee84c70c441a7aa23c326dc9963df338c3040a8e3ab216e6d91543fc`

```dockerfile
EXPOSE 11207/tcp 11210/tcp 11211/tcp 18091/tcp 18092/tcp 8091/tcp 8092/tcp 8093/tcp
```

-	Created: Mon, 14 Dec 2015 18:18:42 GMT
-	Parent Layer: `4e263b0dc20c10973a0583542368f4c1c5b767ad102764798e0e5dc6295b57e2`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `61f7375123be31604aba32addbdbbf3a912c19002f1935366edb0ffd3ebbfa87`

```dockerfile
VOLUME [/opt/couchbase/var]
```

-	Created: Mon, 14 Dec 2015 18:18:42 GMT
-	Parent Layer: `41da4d95ee84c70c441a7aa23c326dc9963df338c3040a8e3ab216e6d91543fc`
-	Docker Version: 1.8.3
-	Virtual Size: 0.0 B
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT
