## `amazoncorretto:21-alpine3.23`

```console
$ docker pull amazoncorretto@sha256:a9e31e8d7d04e3fbea58815b8e30ea1b8d310fa41b004d2fdbfdd1a2307df375
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.23` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6baa1ef2c0e0fcc6d1d37abd1103b0cb5ae932e387d902e27bea7b764a952623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166022836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f949fa5af8eb82cfe195431a5b8510779c7939d7c8de7d805311b9fd41de63`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:33 GMT
ADD alpine-minirootfs-3.23.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:33 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:21 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:21 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:21 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d0c1d894c237d8192cbcd37e435031ad4eddec173299568a5a05869c2e40dfa3`  
		Last Modified: Thu, 17 Sep 2026 20:37:37 GMT  
		Size: 3.8 MB (3848507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550113a218371250281b61ea803ea4c9a5de3306e54aa33941a606052d6ed6f`  
		Last Modified: Mon, 28 Sep 2026 18:04:39 GMT  
		Size: 162.2 MB (162174329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e072d4c1c82a622d5d21a766f326bc0e7797b615feb4e57eddd0669c1e1f0b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 KB (591788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725ea43ed3ed9250e1541f5adb812b25300779ad2e65c3a783c793f4356eb9e0`

```dockerfile
```

-	Layers:
	-	`sha256:f998bd8eee837880cf7c9b66862b92ececbc0cd6567dbc431e67a6df9557e787`  
		Last Modified: Mon, 28 Sep 2026 18:04:35 GMT  
		Size: 582.4 KB (582410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16561c0e323be13eb7b0d41218af9c304965150896ee0404b802f9fd4d91f808`  
		Last Modified: Mon, 28 Sep 2026 18:04:35 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f0c09cbdb70dabf61ae114e8b6d27b3dd605299829288d1fad859e2b43d8a0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164376458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38598dbab1a2ea21dad4a3fd1c6e829bfc114f990c01f05f93b38b0f2bdd85`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:18 GMT
ADD alpine-minirootfs-3.23.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:18 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:08 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:08 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:08 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ace1621be7ff15b54252f68393ac33181df7f3e095e36a5d9a9892031b357d31`  
		Last Modified: Thu, 17 Sep 2026 20:37:23 GMT  
		Size: 4.2 MB (4186056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22294ba58a96ff3d81fdd699c83e4571b66fda2d9dee5b43f73fea4c4640c858`  
		Last Modified: Mon, 28 Sep 2026 18:04:27 GMT  
		Size: 160.2 MB (160190402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b6cb5403350a6151631f90883db46c6612fc1474b28726889d60c1e4075678f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 KB (590662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994a93dc3f0ffff6fee946eadebd8df06c9c97031a0373de0726c6a6f01f0349`

```dockerfile
```

-	Layers:
	-	`sha256:debfadc2cf2a392c1672c558210b6043e59bada4d0a2379ee38c33622b0ddf32`  
		Last Modified: Mon, 28 Sep 2026 18:04:24 GMT  
		Size: 581.2 KB (581179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99cb7d8f1654447047a0922ee6faa2d2d3997627f9fbc306c26779fa9c1e600f`  
		Last Modified: Mon, 28 Sep 2026 18:04:24 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
