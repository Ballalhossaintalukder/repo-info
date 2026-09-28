## `amazoncorretto:25-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:40938dac47cb8161e397f12d5ee2302a6190a005c59c28ab4b3b714d55c82388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fe7d17ffdc33143fa9dc302322b59d01cf4f17ef22d3cec084bd727a8585a29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185340586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff86476b2e3080d2e30319b8f74292bd66c8d0b0aa24840504d05ef1c05a26a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:33 GMT
ADD alpine-minirootfs-3.23.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:33 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:47 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:47 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:47 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d0c1d894c237d8192cbcd37e435031ad4eddec173299568a5a05869c2e40dfa3`  
		Last Modified: Thu, 17 Sep 2026 20:37:37 GMT  
		Size: 3.8 MB (3848507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47028c339dd553b7a4124c0a199646cf7b97cbf5076e83482f5b2b5493f1ae24`  
		Last Modified: Mon, 28 Sep 2026 18:05:06 GMT  
		Size: 181.5 MB (181492079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa07d90a27be70c33c931c4b6a6641cdbdfe88c91a7e1ae791c9818ddb59d29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.9 KB (600875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc30304b6588289051d76e8d58a8552a43db159b5db956dde442ef4f43c321`

```dockerfile
```

-	Layers:
	-	`sha256:bd7015dd4c9132da43395739500212590afa2b30a33062fceb2dd25064e5907c`  
		Last Modified: Mon, 28 Sep 2026 18:05:03 GMT  
		Size: 591.5 KB (591506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957fe8bddc817adedc22a74a2ab336a9a3eac0a358a65fb2c420fa39d808cf18`  
		Last Modified: Mon, 28 Sep 2026 18:05:02 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:025e6bfc76cd8ab243308fdd2d7617f94383e275d2bb44a64488965f665fb62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183284789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca7d334a2d44a899b10663cc64d1af084a80b0592e5ea3221666b206c70fcbd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:18 GMT
ADD alpine-minirootfs-3.23.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:18 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:40 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:40 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:40 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ace1621be7ff15b54252f68393ac33181df7f3e095e36a5d9a9892031b357d31`  
		Last Modified: Thu, 17 Sep 2026 20:37:23 GMT  
		Size: 4.2 MB (4186056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bd83be3033e234e52f4bd73c6fcd37267552d28fbd552865a1320910fce877`  
		Last Modified: Mon, 28 Sep 2026 18:05:01 GMT  
		Size: 179.1 MB (179098733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2286ddb2a3d86762bef1cc3a0144ed388d1fcefdea675002ada397c51c92cead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f89484d5a9242583c04b5d1a353bb257d5c4b55a2889e1680a10bd56ccc88`

```dockerfile
```

-	Layers:
	-	`sha256:587deabe85f3283337a4a791133b416af9000b62710ca154ddd885a28e3f20a4`  
		Last Modified: Mon, 28 Sep 2026 18:04:58 GMT  
		Size: 590.3 KB (590272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055ae7a1c53183c3b7db80a928ddf9151c713e2e2243d465d3936a15d990d403`  
		Last Modified: Mon, 28 Sep 2026 18:04:58 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
