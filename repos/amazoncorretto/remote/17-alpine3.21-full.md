## `amazoncorretto:17-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:8a22f92b2262eeae6f7f63bd0b325fe0b56a2c3134717f3ea55eed4a1b3bfd46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbd8bffa0b2ced74ae9286492d15a7ca0d94cfcf45b36272910131670db224e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152561904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e83ff41d5ebcac228f1ec887e17224e7ca737f016ef7f59165402654471dae1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:22 GMT
ADD alpine-minirootfs-3.21.8-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:22 GMT
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
	-	`sha256:16333ee0c00fc65e025a2a4f839703ad37a74728832977fbdf080984de1b8e5a`  
		Last Modified: Thu, 17 Sep 2026 20:38:28 GMT  
		Size: 3.6 MB (3626020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422be4bbfd5a85932c250a79c38f0402ab05d13eac15b90b8dc41a7000f01f68`  
		Last Modified: Mon, 28 Sep 2026 18:03:49 GMT  
		Size: 148.9 MB (148935884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:02a08f9f74286df2a93a6033bdd246318c1ed3d3ac330e2bfcb27787c5f18d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 KB (596592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534de4d5a2d15e90047b3ad7319ac279b272f3fc79776801146f06341baa21d2`

```dockerfile
```

-	Layers:
	-	`sha256:4ac8577dc49ebf253556434792723156e85d0a4ff4f2298360b8cb14e7bbd05d`  
		Last Modified: Mon, 28 Sep 2026 18:03:46 GMT  
		Size: 587.2 KB (587213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654f8fa7ccf46312e46170ad0bacbc19686501e1a21fcb25d498fb71217661fc`  
		Last Modified: Mon, 28 Sep 2026 18:03:46 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1ed344e3a851459cb0089b160e33423685fe8284594cb76395fa4d7b960dbb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151332353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957f2214706631cf4979d1a3d9b577bedb4f61339371c071825dd69dc26f03ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:38:00 GMT
ADD alpine-minirootfs-3.21.8-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:38:00 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:26 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:26 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:26 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:248d4d6535e8932d2b51acdf49a4ca8d87629cd408a02bd59788b4c31e3d0c28`  
		Last Modified: Thu, 17 Sep 2026 20:38:06 GMT  
		Size: 4.0 MB (3974501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1264229a99586bc21f832709de0bb4d219cfa0cf2dd00fcaa26f345b2af1a52f`  
		Last Modified: Mon, 28 Sep 2026 18:03:45 GMT  
		Size: 147.4 MB (147357852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26cd9e5747ffdffd0151713905b911e3be899975d4576f4ddfaf0e764f4ba7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 KB (596115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb610bab5f113801a053c8343b1f5b9d66cebef97ab4a8cd4f03b788a9dfc36`

```dockerfile
```

-	Layers:
	-	`sha256:bde45cc585b09b73fa8714a25488d07345e0c4d611fa7d244d774795fb5f5ce4`  
		Last Modified: Mon, 28 Sep 2026 18:03:42 GMT  
		Size: 586.6 KB (586632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7057133253ebc27a1cd6f8ed1290ee4d07f5ba6d52f6e06590b01f6b43ace084`  
		Last Modified: Mon, 28 Sep 2026 18:03:42 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
