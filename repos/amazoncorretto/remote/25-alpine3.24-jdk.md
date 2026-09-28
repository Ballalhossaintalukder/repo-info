## `amazoncorretto:25-alpine3.24-jdk`

```console
$ docker pull amazoncorretto@sha256:19f1e2198abaaf201f5b9faa39222412da3fad66415e9dfe253bd6763415097e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6f66f6ac4de9840a3c5cf85e2612be9b8a8567c10dbdd27b5350811dfb616bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185365644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5803db6b455f1f0821ce9e0c11e1d15278c408df7ddbb3bf59fe0c7eb18e0848`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:49 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:49 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:49 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17350f39c8bbe142c6bf23e285e398c0421e05929dfbdfb8305fb1ffe6cc10`  
		Last Modified: Mon, 28 Sep 2026 18:05:09 GMT  
		Size: 181.5 MB (181515906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e3d850199408eed4237f2c84e024e72e11dbb7671ea1767efa97eb867466db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.6 KB (603561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966ae9321e5e0e41bed62d9bcedf02d5a04d97061aca9f4d6e448e4fd290dc8f`

```dockerfile
```

-	Layers:
	-	`sha256:9000f311f97ea45ba49c734d73cfa7f01a6df8470d8e8d2621bfdd459f838037`  
		Last Modified: Mon, 28 Sep 2026 18:05:05 GMT  
		Size: 592.9 KB (592883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9a5c2c000b580c10e7bc1fd19d1595d8b796b7972edd7c3e71bab6a2a1a8ac`  
		Last Modified: Mon, 28 Sep 2026 18:05:05 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9b146109c2c0f2b8d5f8507c0e7428c920ba45472afd4a8c942564fa01a8efaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183302508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537f37f13b057132e861effa7a7225a628e01dde21147c57108c2609dc8a012b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:41 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:41 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:41 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ec7c5cf6b0f026b01470e3c9dc538b6ad52b752f2bc4d3560e5b87520a65cd`  
		Last Modified: Mon, 28 Sep 2026 18:05:02 GMT  
		Size: 179.1 MB (179114849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:979d2eb262bb43775f2f942a2e228f8f0c70ab5ec0bc4ac6e3559e54af92f6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 KB (602527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b282c0f906ba132ee7341046964ef0dc56fd69f8d5a277fcca97a3fd3fc99dc`

```dockerfile
```

-	Layers:
	-	`sha256:55d946af8d6aee3ff404e8b451f216c5ce16ab1825e89bc2e88a48a409bd9f6f`  
		Last Modified: Mon, 28 Sep 2026 18:04:59 GMT  
		Size: 591.7 KB (591697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9f0f21f4cbfa8762c763f0518b78a543ebc30cc66c41f896f382765bc2b933`  
		Last Modified: Mon, 28 Sep 2026 18:04:59 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json
