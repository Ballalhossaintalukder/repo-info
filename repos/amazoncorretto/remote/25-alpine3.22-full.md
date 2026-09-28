## `amazoncorretto:25-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:b22e63eec97c799c8fdad5c462421e88b6aad5ced26547b27aa53ef36fad08de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f4a1ad6225982418260f6841ec26d42d6f62daf9d90185e2478912d6c442dece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185285795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72684e69ac441e417a9326ef78c88a26a026d06cd4980c0e05e6670fb6b02d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:44 GMT
ADD alpine-minirootfs-3.22.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:44 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:43 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:43 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:43 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:53f8f5e03afd86ade91b7aa57a749f5a3d1419c113be5d8c10e7ee61bb5ab887`  
		Last Modified: Thu, 17 Sep 2026 20:37:49 GMT  
		Size: 3.8 MB (3792075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ff1a96b6b47da02a35e6f7d9f5d27b02ef2440e9630ae170a491288a70803`  
		Last Modified: Mon, 28 Sep 2026 18:05:04 GMT  
		Size: 181.5 MB (181493720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ced582415921389d27997cca7443b31719e813031ed8bae9c868af85a145d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 KB (602162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec06273b615b56bf67edf9602d9cd1b092e62c886153c68ce81355496b648a7f`

```dockerfile
```

-	Layers:
	-	`sha256:7650a55cf8af141fb32ea24816fbb07db661aa234cc4378bc68b9ed71746852d`  
		Last Modified: Mon, 28 Sep 2026 18:05:00 GMT  
		Size: 592.8 KB (592790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aadaa9fddcc51de8f61ccb4aae0c3ccfead550d8647308cce2e5fd2d0e58f484`  
		Last Modified: Mon, 28 Sep 2026 18:05:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a187c8ad9e6285fb406542b0cd2490809315b4fca8204c3ad6e19b3c6b0e1324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183220424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18707d8761cf72790b5ec0e7d145ff3a15e1edf3a6205d9cba383a2a7423adf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:30 GMT
ADD alpine-minirootfs-3.22.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:30 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:39 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:39 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:39 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16fc4f52163f03cd2189c3d6a4b3f28a605cfb7919af64b3da4562cca69d2306`  
		Last Modified: Thu, 17 Sep 2026 20:37:36 GMT  
		Size: 4.1 MB (4123084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac66ca4e2b368eec63b62edfc98f34beb7d9b22f5b9ab3d50f52b9a2505f23d`  
		Last Modified: Mon, 28 Sep 2026 18:05:00 GMT  
		Size: 179.1 MB (179097340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d170dee0200afb13370239aa6d6fa74e1944d436fc335fe744bff3dffd1c1a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 KB (601682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b355961e23dfba6a415c1d22b2f56ccf7583ec52a3eb2030bad1256a67879f03`

```dockerfile
```

-	Layers:
	-	`sha256:5a9f3b97c13e817dc756a66f98a30b1bb0c10c50510b0bed6c0a7a37ae11efc4`  
		Last Modified: Mon, 28 Sep 2026 18:04:56 GMT  
		Size: 592.2 KB (592206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c597aeff7fc96d058d22c426b7617bfe4dc29640267ad077dd71e70e5b256660`  
		Last Modified: Mon, 28 Sep 2026 18:04:56 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
