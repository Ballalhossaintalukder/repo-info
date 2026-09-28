## `amazoncorretto:17-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:ad4d379fbe06290df748b9bc36e140686f8c15ebd725b8451970d625f84bbd16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:00efd9d8ca0f117043e9a32951dae94497099f6efe0527cd8fbad6e5af17cbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152735821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd403a35a4d00bfa4b7f4ff1030f445248d3f311878c6d6a255894a6aa766dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:44 GMT
ADD alpine-minirootfs-3.22.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:44 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:34 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:34 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:34 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:53f8f5e03afd86ade91b7aa57a749f5a3d1419c113be5d8c10e7ee61bb5ab887`  
		Last Modified: Thu, 17 Sep 2026 20:37:49 GMT  
		Size: 3.8 MB (3792075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb4f8e414d5f3a161ba3bef37b844a40f1707fa8700473891332d63195c24d`  
		Last Modified: Mon, 28 Sep 2026 18:03:50 GMT  
		Size: 148.9 MB (148943746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25f8086205c6cacc309342fa106c72981987a4157011e05123b5218c84149ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.2 KB (593169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0afa2aff0d065e7b70ad911b3f7ff4063857513e4a428f978483e8d2cf5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:40a771db369d5539d9854607f41531a32a85aa66b60dad70e1750a1c6b5b2dc8`  
		Last Modified: Mon, 28 Sep 2026 18:03:47 GMT  
		Size: 583.8 KB (583791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd7300346bd4b984a50511f84f9e8f6e62f1834106e6dd3849e7e39a4ea59c4`  
		Last Modified: Mon, 28 Sep 2026 18:03:47 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:32b33b8144daa2b90335462fdca90dd7f921982d5bebbc583a71ca0c4631f62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151490211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a890fc84468bfc0f9dd9a78acfb5853179b86ef27fed74867e69e833cfb0f97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:30 GMT
ADD alpine-minirootfs-3.22.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:30 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:29 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:29 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:29 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16fc4f52163f03cd2189c3d6a4b3f28a605cfb7919af64b3da4562cca69d2306`  
		Last Modified: Thu, 17 Sep 2026 20:37:36 GMT  
		Size: 4.1 MB (4123084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdbc7e679532a825daf333e3ec20b7c42cd27828972a449000e7f2bb0014331`  
		Last Modified: Mon, 28 Sep 2026 18:03:47 GMT  
		Size: 147.4 MB (147367127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2c5867d67b6f7d213d0e5143c6191e4e07754868f61e6bb04beed971d9ccdd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54a8f9c2ece838159608e0365354515d67133891783ed9cb97bff1de0641a54`

```dockerfile
```

-	Layers:
	-	`sha256:8eb6114245e3a049ba62fcda2a0dc339af05b529fff694c5b99671a0938a2f4d`  
		Last Modified: Mon, 28 Sep 2026 18:03:43 GMT  
		Size: 583.2 KB (583210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed591efc133b1b32bdbb9e2f72fd1bf71a3dc567e6dbdd14f85dc86f508b4ccc`  
		Last Modified: Mon, 28 Sep 2026 18:03:43 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
