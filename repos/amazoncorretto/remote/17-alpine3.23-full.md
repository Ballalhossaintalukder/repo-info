## `amazoncorretto:17-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:c64fad43303602f2e76d217496df660837f84da2444cdab0414db85c25fe512e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a8d3e61165097b93ba5d2ba117a9436087eb4ab1d53a28935b300de6f404fac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152788028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d435399311374e1084e9ccff30c44481b1ed76f940e9186fac832e5dacf07a55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:33 GMT
ADD alpine-minirootfs-3.23.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:33 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:53 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:53 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:53 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d0c1d894c237d8192cbcd37e435031ad4eddec173299568a5a05869c2e40dfa3`  
		Last Modified: Thu, 17 Sep 2026 20:37:37 GMT  
		Size: 3.8 MB (3848507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c6db18a8f12095a6483640b3d3b695b6b1cd8211aa6ddd75bdc3451b038228`  
		Last Modified: Mon, 28 Sep 2026 18:04:11 GMT  
		Size: 148.9 MB (148939521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b7f2e5813922c98de798c45e14a563667fcf106cfe0f316cc69910ae4913009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 KB (591886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a298debd706f3bb093ce627d98f598d073a3c5cc64141e0bab05c49752e2c6`

```dockerfile
```

-	Layers:
	-	`sha256:72c81ec64dcc283a79fcf5401316093dde151a3ddc6cd2107ce431f5594351b5`  
		Last Modified: Mon, 28 Sep 2026 18:04:08 GMT  
		Size: 582.5 KB (582507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b346195cda05a21c438c17b5b2e9ed9a1e29453eab093a6fe695d9e69cf21e`  
		Last Modified: Mon, 28 Sep 2026 18:04:08 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57ea8a7bfc4edf293c4747f12e10686a83926c8c6967373f8415ee55c6d73065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151552728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e499694207a810c79f184c2842f588e617ebf4fa874dd55cafd6449c66b15ac5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:18 GMT
ADD alpine-minirootfs-3.23.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:18 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:32 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:32 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:32 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ace1621be7ff15b54252f68393ac33181df7f3e095e36a5d9a9892031b357d31`  
		Last Modified: Thu, 17 Sep 2026 20:37:23 GMT  
		Size: 4.2 MB (4186056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8533b25c79101f35a4b018f83437ba86e6c2f3c8a628758c21cfb950345c93`  
		Last Modified: Mon, 28 Sep 2026 18:03:51 GMT  
		Size: 147.4 MB (147366672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f76ba41b51af7ac44536337269bddf3319991895753e8855e0b3b279b11f5636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.8 KB (590759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f387cf48100d996ce36072dd6448b73763fd285e14c1dcd9680f66876eed6a61`

```dockerfile
```

-	Layers:
	-	`sha256:362ea6e14d033f2c14f6e63f6b2009722a43813f3196c60d6619f7fa1df2f04a`  
		Last Modified: Mon, 28 Sep 2026 18:03:47 GMT  
		Size: 581.3 KB (581276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864e9342c12be8bb6f252e05cd6beca155c80f3be259dceca726ba7022c2452b`  
		Last Modified: Mon, 28 Sep 2026 18:03:47 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
