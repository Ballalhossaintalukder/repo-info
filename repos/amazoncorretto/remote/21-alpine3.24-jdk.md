## `amazoncorretto:21-alpine3.24-jdk`

```console
$ docker pull amazoncorretto@sha256:b7451ecea0f2a02b9597493bb57c4014f43c41db4b470a8aee7228d7a0279025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b724c944370e9d60671f48236a4d82d843ef941183b41e9caf8cfe9b45ae26a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166048419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9abcfa46e382b2791c428cc533d8523dcba241d0f580673a69335edb17c8ca7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:22 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:22 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:22 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d781ee64e4e37cbd7e17b1fbd2abe312c76056972c450befcd138ec81aaf579`  
		Last Modified: Mon, 28 Sep 2026 18:04:41 GMT  
		Size: 162.2 MB (162198681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fd6d217888106b263d590cb094f236be44b8ac93feabae1808779d0fd861576f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.5 KB (594476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c4297ae4bac5ec3dd32e1daa48c6c4b833d5eab3715427da9d847185705ded`

```dockerfile
```

-	Layers:
	-	`sha256:9bb807ef679bbf1ffcb83b696128011caee9cc3e0f3f300635c4a288f9c3d482`  
		Last Modified: Mon, 28 Sep 2026 18:04:38 GMT  
		Size: 583.8 KB (583789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd86ad4c5df85ed549116ee002090627eec9a1357f49dfc3be8da8a324cbd40`  
		Last Modified: Mon, 28 Sep 2026 18:04:38 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8458edc559ca901ffc0206707910272dbdf0f79d09e403d4be18b5c7caf04ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164390630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4463b0a44dbe792441b09121a9e0b006544d7b32ac7e3de2241858e648e1fbe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:10 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:10 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:10 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36b47c418118fc77b81a192eaef2c0ffc98cddb4396f0a502240598153735b`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 160.2 MB (160202971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3be7b8822989060111c6d3fb8afb1a8fbcca1ddf0019ca152ffe83b567e13925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 KB (593445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c49660a52160d761b371a1c54c703fa4c46a72beb342c36cdb0030220eb1c0`

```dockerfile
```

-	Layers:
	-	`sha256:cc54a9f491894efb223513da07b71f99b1e5423b19c19d2add849e18220deb26`  
		Last Modified: Mon, 28 Sep 2026 18:04:25 GMT  
		Size: 582.6 KB (582606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0feef0069b089a33451c8870fd86c8d7c7da8bf26ef7e414fc023348ac3834`  
		Last Modified: Mon, 28 Sep 2026 18:04:25 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
