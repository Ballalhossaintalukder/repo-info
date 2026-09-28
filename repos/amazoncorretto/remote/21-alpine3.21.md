## `amazoncorretto:21-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:60172af831ac02a68feff99a4dc3e11bd8ad5048491d9b6cf7dda40c5af72eb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d1ebe6b6972800ed721176052fe8daeafb868bde1dbe6dcd994ddf07b44733e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165796870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56e972db3574ad71b507267616d5bce500f99de7760638b8f975bf5dadafd4b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:22 GMT
ADD alpine-minirootfs-3.21.8-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:22 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:11 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:11 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:11 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16333ee0c00fc65e025a2a4f839703ad37a74728832977fbdf080984de1b8e5a`  
		Last Modified: Thu, 17 Sep 2026 20:38:28 GMT  
		Size: 3.6 MB (3626020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596507111a7a3912791a8e69df3e648db7b87411f9ff65726c92afb1270b2919`  
		Last Modified: Mon, 28 Sep 2026 18:04:29 GMT  
		Size: 162.2 MB (162170850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5fc3da8854a49edc965ac9bd10cbd1c6a3437d484f80c00bc77db6355b97bce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a9035d2c60095fd95a23d64b1306da8dbf376f3652617dbd62c3d1fd4f7e9f`

```dockerfile
```

-	Layers:
	-	`sha256:b91f4c720b39a21a4b8b9235e0c9c2b439bcf3a0dc2797e1b845d0429b8c6a7d`  
		Last Modified: Mon, 28 Sep 2026 18:04:25 GMT  
		Size: 587.1 KB (587116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce71f6f32d786dab4f9f3528e8d154785d9b2961995da60c923e859bb0697cb`  
		Last Modified: Mon, 28 Sep 2026 18:04:25 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:82d9551f300bf208c2e839baf509d498d8a853d12ec194db79be84fc87a1ccdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164154759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74782e47d8449b1a13462cfb0749f45c8ea3f4c4ebfcd9796d06bd37bf17533c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:00 GMT
ADD alpine-minirootfs-3.21.8-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:00 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:03 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:03 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:03 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:248d4d6535e8932d2b51acdf49a4ca8d87629cd408a02bd59788b4c31e3d0c28`  
		Last Modified: Thu, 17 Sep 2026 20:38:06 GMT  
		Size: 4.0 MB (3974501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095c7db48ab5c6fa3942d667babd9bf51189776074f1ca344c66dbb33b5266fd`  
		Last Modified: Mon, 28 Sep 2026 18:04:22 GMT  
		Size: 160.2 MB (160180258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7af2e53db551390eb6d16ba7df8f251d6434f50d564c5e14033d6dd5dc6dd118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.0 KB (596018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2de5afc0e4be1437d519057d92ad20aceb501f284fd69562484567e4b893ef2`

```dockerfile
```

-	Layers:
	-	`sha256:ce2acd315c4927c87d0f21468fe9064c561c1a7ca97e617ce04a29273f5d10e0`  
		Last Modified: Mon, 28 Sep 2026 18:04:18 GMT  
		Size: 586.5 KB (586535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf090edf4fd88382ca8db92c8281d701d5162e69555afe9891a8b9406593f9b9`  
		Last Modified: Mon, 28 Sep 2026 18:04:18 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
