## `amazoncorretto:11-alpine3.24`

```console
$ docker pull amazoncorretto@sha256:3115a3799c70a63247fc13c23e707f92f3e6db54fd7b8d28f4b0bf116b3c39d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.24` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dfb933304a143117eba08cd664a69c783f8a6010d9bffc2b0d47b3be34200ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147822727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a81033366ec282f4bab98bb2789b01e4446476aef08deb46de3abb6056a26f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:03 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:03:03 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:03 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76b865d353ee02c78d12f14c520fe6a05cde2e44f4a1ea1f4a17c4ca832b56`  
		Last Modified: Mon, 28 Sep 2026 18:03:20 GMT  
		Size: 144.0 MB (143972989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.24` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2aaab011c48f20e442d0946aac77fb342e344d948c33878dd2ebc6704a5fc622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f95ab63b7f156cdfdb57b6ef951ec66e02ccc5213914d638ab57d87fbaf360`

```dockerfile
```

-	Layers:
	-	`sha256:2315c411c6fd1da376e6d670f2587a560bd0cca1398183a285f6bc603548a145`  
		Last Modified: Mon, 28 Sep 2026 18:03:17 GMT  
		Size: 589.0 KB (589034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216a3822d9615bb1fa43d860d516eb6c979887a0577dffb9aa9864179388bcc3`  
		Last Modified: Mon, 28 Sep 2026 18:03:16 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fef3156ef92419368bffcc3bce4c57f6c9ce7a7a1d07f3fa1bf10ad5158a3cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146534234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ca0b7e5d6405af4e61d456b56d11bddda05c29ce2ffe8d45b825ba8fb1e65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:02:57 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:02:57 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:02:57 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:02:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7458ae3ef813635d38c802fedf1cc6a5346d19f30bcfa1f6589949fd3c32021`  
		Last Modified: Mon, 28 Sep 2026 18:03:14 GMT  
		Size: 142.3 MB (142346575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.24` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20f4e614e50517a8ec5a716b861c39fc88b6da1280d698d2944014e937dd8a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 KB (599327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73def8c0585ae9d640ebb4cf30711d2a30cb83ceb7026545d84a42e02e509a`

```dockerfile
```

-	Layers:
	-	`sha256:bc97e0ce9c7d564f35711b441396ff54d94c2d624c8dc79ee8b647a0952f739a`  
		Last Modified: Mon, 28 Sep 2026 18:03:11 GMT  
		Size: 588.5 KB (588488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7456bf6356a510365614c82382616b7521003f0c4d7d70c43f8334dd0984c0`  
		Last Modified: Mon, 28 Sep 2026 18:03:11 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
