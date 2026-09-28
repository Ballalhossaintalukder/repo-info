## `amazoncorretto:11-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:cfc2d8dd29e8a858e6fa1b315a867e992f051244f27f69f298510ffe87155e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32f63c8b55ad585f3c3c2db68ccd4a4e1e5e6005089989c25f809f805bf99182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147568832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089e5862f520bb16e0b7570b386b6da7e81d7f0269db017ad2b1f16df39f45eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:22 GMT
ADD alpine-minirootfs-3.21.8-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:22 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:02:31 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:02:31 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:02:31 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:02:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16333ee0c00fc65e025a2a4f839703ad37a74728832977fbdf080984de1b8e5a`  
		Last Modified: Thu, 17 Sep 2026 20:38:28 GMT  
		Size: 3.6 MB (3626020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ab9b324574d186478b78daaa60614ba727790fa1e905cd5d12576e589cca21`  
		Last Modified: Mon, 28 Sep 2026 18:02:47 GMT  
		Size: 143.9 MB (143942812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6dd02c1011307202f7e4e9a73c8755ba59d7e1560aee1060a80e2ba7e38e44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 KB (602748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30d8fdee5924e79549b96198a3cee9934c3d468a26c5941244c82ff6414c5b5`

```dockerfile
```

-	Layers:
	-	`sha256:3dc3c6067dee3893892d363834639031bc891d6f3f2c56d7a716d8b61b05490d`  
		Last Modified: Mon, 28 Sep 2026 18:02:44 GMT  
		Size: 593.4 KB (593369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da455c733b67a2a877e451c082b170b847a26970c6f80dfcb3cdfad674b2d05`  
		Last Modified: Mon, 28 Sep 2026 18:02:44 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ed035abdd60864720f20de5d19646ea280b3ea41cfc846c35b5067750182b232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146297789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8768ece95c069f2d6e7d4ff3960c5472b3f78d9ef712dc92afe98eb62ea9ac80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:00 GMT
ADD alpine-minirootfs-3.21.8-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:00 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:02:39 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:02:39 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:02:39 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:02:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:248d4d6535e8932d2b51acdf49a4ca8d87629cd408a02bd59788b4c31e3d0c28`  
		Last Modified: Thu, 17 Sep 2026 20:38:06 GMT  
		Size: 4.0 MB (3974501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522033859f1c2d951771ba37a5616f72555c1c03dc154dadc87083a106a3b5dd`  
		Last Modified: Mon, 28 Sep 2026 18:02:56 GMT  
		Size: 142.3 MB (142323288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e98d46ee545e4f9fc7a340ad24095e96c06fccdd4d8f4f3a4957f0af12ec7bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 KB (602906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c77e6ed2faab56cb4fdd0e56ac34b2a934ccac392bd27ed3dc38b20aee1af0d`

```dockerfile
```

-	Layers:
	-	`sha256:4fcee33e9fcf7f14a23dc13508f5aa223721ff48dcf847ec16eb4a1f6082ca6c`  
		Last Modified: Mon, 28 Sep 2026 18:02:52 GMT  
		Size: 593.4 KB (593425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392bd8f44fdfc86582bf9a521158083b15044463a1fbed2d3c0c5f77cc7cd0f7`  
		Last Modified: Mon, 28 Sep 2026 18:02:53 GMT  
		Size: 9.5 KB (9481 bytes)  
		MIME: application/vnd.in-toto+json
