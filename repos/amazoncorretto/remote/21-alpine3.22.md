## `amazoncorretto:21-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:470dd903c0a952b543efb29954daff824ee7b304fc1d7de92c3bce9bc9b9f0f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e64d4999b38e605f4aa2585e31f6f87d9971c34df00630a385eab44d787974e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165971404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604ff98c85fe2ad7679f09bbe9ad23f5733602b2f03c8f041fa68b594eed07c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:44 GMT
ADD alpine-minirootfs-3.22.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:44 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:13 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:13 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:13 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:53f8f5e03afd86ade91b7aa57a749f5a3d1419c113be5d8c10e7ee61bb5ab887`  
		Last Modified: Thu, 17 Sep 2026 20:37:49 GMT  
		Size: 3.8 MB (3792075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a997e51e06539f7f4cff7ce866d76121525ce0777957874eb3866fdf6e1ac49b`  
		Last Modified: Mon, 28 Sep 2026 18:04:32 GMT  
		Size: 162.2 MB (162179329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c1a38f87c5a722ed04280a1ef7d1a1d92bfde6f4056986cc1661509368a82d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.1 KB (593073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bed2153505713b415985f8578401560cbd5729315eebe19c5853c6216aa2733`

```dockerfile
```

-	Layers:
	-	`sha256:e53f5b24351a812a5b0ed41c7a656e946c4696657a7da6db77c25079c776a1e8`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 583.7 KB (583694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9a813341aaf746f4d41d2c79d3aea16f1540d840a6b40efaa4ad661bbcf80d`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4a1980641fc8deb1b3d252bb77d9d10c9e5ba8251f8e135d218decd2f33483f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164314555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04b14ef3d99fec977652bccf90dd0e5d8b8701efc375b69f78bd58829d7282f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:30 GMT
ADD alpine-minirootfs-3.22.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:30 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:07 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:07 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:07 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16fc4f52163f03cd2189c3d6a4b3f28a605cfb7919af64b3da4562cca69d2306`  
		Last Modified: Thu, 17 Sep 2026 20:37:36 GMT  
		Size: 4.1 MB (4123084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b851fad8df14119e3805f374bfd1a289845bb586d15e6863d04637a671861`  
		Last Modified: Mon, 28 Sep 2026 18:04:26 GMT  
		Size: 160.2 MB (160191471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c2892a314dd507df39e6858b96cc1667ec4dfeea6b796fcfd237be6602f16c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 KB (592596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974c290d16677e3c884af6d474968912d4ba7a983e87b8129ff371aa3d13e4ab`

```dockerfile
```

-	Layers:
	-	`sha256:67e864896144061d6522f4139bc52acc5886794d5cb4bcd4cb12f7d15143b2d1`  
		Last Modified: Mon, 28 Sep 2026 18:04:22 GMT  
		Size: 583.1 KB (583113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92dddf92008195c64a56126aaf92863473c52902cbf7193da379b06e31edf76b`  
		Last Modified: Mon, 28 Sep 2026 18:04:22 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
