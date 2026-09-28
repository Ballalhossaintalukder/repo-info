## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:7fb62c70d0078aaa53cafaa66cc2af816f54c875afcd9d1b20679529a439ce97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d9604fe20e79350037fd86a7a68402586d9698c66416782e99b204394e9bd76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228612924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1d171eb8ec42b813bc2c9b33cf8cabeb041c366e7a77e3c655e2a9fe4b369b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:10 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 18:04:10 GMT
# ARGS: version=21.0.12.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 18:04:10 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260edf3d7e4fc4fe35821915385ed3f6b8bd6e5927b1ac8bc5e30b9248c8fbe`  
		Last Modified: Mon, 28 Sep 2026 18:04:32 GMT  
		Size: 165.6 MB (165648328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f531672a529d84cafff4a212b5b65e128d7192e72243244d525c7659d3249f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f06cf7c4321539af0644a7b7f113587f9dccfc0a6763ab09feb337306c451b`

```dockerfile
```

-	Layers:
	-	`sha256:45d515ec292ba4ce0a9b1ef854550e4c6826ddd711e8da4d38d5d286a06e9054`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 5.5 MB (5536242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5499b617eee63cc6e140aa97eaf79eacc05650b1875f6ce7fee620e1f5c16d30`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 10.9 KB (10905 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2f76022216d8992357a90f9501fd7d9fb96bf8933fa3cfd0a8979eaf10df233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228601006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b57d747673ed9c774316d0e37028b815bde5aeaa00d0959ce80e1eb918044b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:07 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 18:04:07 GMT
# ARGS: version=21.0.12.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 18:04:07 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca823c29fe9c09c0a7c95576bfed760f998f94a35924a3b2e780430d33b1beb0`  
		Last Modified: Mon, 28 Sep 2026 18:04:30 GMT  
		Size: 163.8 MB (163795905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f427666a2c648b42fd484245a56f8cc8e62eba1f9849684b13b0d1b847103ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c0af2a6fe4e7072b8096868ddc368e7328032a7af4c2cdb9d739c9865af2f9`

```dockerfile
```

-	Layers:
	-	`sha256:53f78a7b48de4660286a332915c17280305107e12e8f918c32b5f518231b006b`  
		Last Modified: Mon, 28 Sep 2026 18:04:27 GMT  
		Size: 5.5 MB (5534919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fed5f73de42bbd70e28bfc21c52fc6504b1aa8c96ccc96c5d661e71fe3c2aeb`  
		Last Modified: Mon, 28 Sep 2026 18:04:26 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json
