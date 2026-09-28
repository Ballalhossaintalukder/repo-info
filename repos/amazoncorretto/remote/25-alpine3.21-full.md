## `amazoncorretto:25-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:9a907a1f1ab9578908d94bb5c954063303e45b4a55bf2a76a452ada3d7ececa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a36314c05670aad2d89490291c694d1ffa19f44078ceeddafb8467f84893b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185115446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee8f86cab30bce4ac81ddd97b1d1e1439554d558f77434712f8ea43e8e0371c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:22 GMT
ADD alpine-minirootfs-3.21.8-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:22 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:42 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:42 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:42 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16333ee0c00fc65e025a2a4f839703ad37a74728832977fbdf080984de1b8e5a`  
		Last Modified: Thu, 17 Sep 2026 20:38:28 GMT  
		Size: 3.6 MB (3626020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c938271b9ff12ca4793b317997cc58ae2664cd051b3573ea8bda15e9bc9578`  
		Last Modified: Mon, 28 Sep 2026 18:05:03 GMT  
		Size: 181.5 MB (181489426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:edb4f98eeb5c2d0472d0127d40dfb23289dc1d4c2c5482c638dbde694b130ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 KB (605584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729c6ddd5ea04b59d90bc5ea8b71b2fe6c0b98f6a107991261eb5e876d4feb03`

```dockerfile
```

-	Layers:
	-	`sha256:c0f1581373880301510dcb7709eb3cb58b9eec8fad250eda8b6023e39026be40`  
		Last Modified: Mon, 28 Sep 2026 18:04:59 GMT  
		Size: 596.2 KB (596212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7415cf0be7d97ccf834ea1985a68ebb7f4fdccc4af00d4e0f80cae4598a12a19`  
		Last Modified: Mon, 28 Sep 2026 18:04:59 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b7fdfeaf42643399d5bef602d685655e0a77112d01a24cbab78bb449e2c3b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183065222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a749435e0c75ede4e8e38ec82a4096f8775682e0df34ab9af5f5f038da8836d5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:00 GMT
ADD alpine-minirootfs-3.21.8-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:00 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:38 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:38 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:38 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:248d4d6535e8932d2b51acdf49a4ca8d87629cd408a02bd59788b4c31e3d0c28`  
		Last Modified: Thu, 17 Sep 2026 20:38:06 GMT  
		Size: 4.0 MB (3974501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122bae5934a1cb59fad96a4512b21e61a934b47353de4d09d6516bc992e430fe`  
		Last Modified: Mon, 28 Sep 2026 18:05:00 GMT  
		Size: 179.1 MB (179090721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03455ae5b42f951df3634d410c06cc489fc20cdedfe451ccd96c43e48ea571ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 KB (605104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d9043a3d2ea369d520215b7b6f15b666935f348c488cccf5b8634b18db922d`

```dockerfile
```

-	Layers:
	-	`sha256:3562811aee1bc4a02d921156d05d20738779f256d54eb3cccc2df17ed646f3fd`  
		Last Modified: Mon, 28 Sep 2026 18:04:56 GMT  
		Size: 595.6 KB (595628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04119ac9bc5f9e806a75d01eb36dae481e30340fb30b06d2d82fc9ee925b45fe`  
		Last Modified: Mon, 28 Sep 2026 18:04:56 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
