## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:27572895e308eee6cdeae31211c3cab63f000df034374eceb6ec00b9521147d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:92a79e36c81d54b486b3aa679b8a4bf21758954a448e4e2735a23b7f1601fe9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215516331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9845d6950a11216120e4b19e5604dd497e2cf0365eaac0a8e8abbc5616b93049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:27 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:27 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 18:03:27 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f748bf994eabcfe723ea9e45ce931c1d50eac46c5f4250f5de72d0c1a4004f9d`  
		Last Modified: Mon, 28 Sep 2026 18:03:50 GMT  
		Size: 152.6 MB (152551735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6907295d613c5b992a05c9782b90b94bfc15f72af95262f81bce1fb486c70239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cd0aabf7b3166d8c6115e523d06b83ae42faf7dee1642ac642ae2e8604b639`

```dockerfile
```

-	Layers:
	-	`sha256:db2a3a5404339e16c1050b696e5a3457ea6c65a4e3fcc9eda6e001d8f5f6e2d5`  
		Last Modified: Mon, 28 Sep 2026 18:03:45 GMT  
		Size: 5.5 MB (5536339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b23b3779fddb5a340d3f53d73cb51770fe0882558b47c5da6f7c905c18a9a68`  
		Last Modified: Mon, 28 Sep 2026 18:03:45 GMT  
		Size: 10.9 KB (10905 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dcfcdbc3c52ea66a5734e2eb971995e97b3805b20dd9bd8f819c883b75792cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215993048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68a42e5ecf5b829ddbd6492924b89e75dc21513c34a76d1b32e06834767b2ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:02:51 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:02:51 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 18:02:51 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d52e9d8e99a057648924586cb4818a88d5069b2be63b141aa605ea7d22802`  
		Last Modified: Mon, 28 Sep 2026 18:03:12 GMT  
		Size: 151.2 MB (151187947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97d680d8b71c081a7ed091f28414dbf2ad23d8842c08ca0c9e5c68b3b4c4da6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bb9f878ac062cc265ee1ccd46a50e955903c5c807550e9979dc28c38bf7a5c`

```dockerfile
```

-	Layers:
	-	`sha256:43c362f9b9fe832884357929f53c8c834c949459efe2686a0ff993511f414363`  
		Last Modified: Mon, 28 Sep 2026 18:03:09 GMT  
		Size: 5.5 MB (5535016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31172c1399a74bdc9120171e3c9bd1e6562c99988bfd93df36b8b1ff292e8a70`  
		Last Modified: Mon, 28 Sep 2026 18:03:09 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json
