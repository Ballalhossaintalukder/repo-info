## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:3ae83a3f1a73bb69b9ec6aeba8701849ad8905542b23e272d3331617d91f6e0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9686f5288e61c8861e25cb61d42d0b4c2d477b1483dfd79e010055088ae279d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215517023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6059bfdd13f1ae7170ffe7fe8ae1d7454f96f78c8f5a8f3d87d916d28810552`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:26 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:26 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 20:13:26 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1325897e8aebac47624781c68faea24bc9b6271e96b4411f4e67572dda23db`  
		Last Modified: Mon, 28 Sep 2026 20:13:46 GMT  
		Size: 152.6 MB (152551651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d0eeb193154b4cf0973de4e62bf50a499140ecce37c77aaa3c6202e5646fd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4267dbc6c0ea988ae5441fd9d414d0b653c35e8ed3e6da0103a7f7c7c3aaba`

```dockerfile
```

-	Layers:
	-	`sha256:0017eee3aec0824bef9413ed1dc6164a584c11d7b01a7e46af98f8ce84990332`  
		Last Modified: Mon, 28 Sep 2026 20:13:43 GMT  
		Size: 5.5 MB (5536339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec2f245a94b0409c8b78de2e6959c862358ede493bdf6ce4387b351a53d6f1e`  
		Last Modified: Mon, 28 Sep 2026 20:13:42 GMT  
		Size: 10.9 KB (10905 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a92d113720dfeeaaa9b938d40445c8740aae877b3adcd657e3f6462eafa511e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215997604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c4ecd72ff6c6578c178d069991ae3fd800bcc5a7c797de908676156fdc445`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:09 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:09 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 20:13:09 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689e7dcf42b8bfa751b8c0193d052a33d57a2544ab39e3f926964aecdd8fb2ea`  
		Last Modified: Mon, 28 Sep 2026 20:13:30 GMT  
		Size: 151.2 MB (151191445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5619ed66be6820a52ba78c6f12ac70209aee9eefebdfa5529a647cf767db9306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb0d3cdf69a85070e9ad6c5790cab964e36947d79b4a6e10fdb09dc04cad5da`

```dockerfile
```

-	Layers:
	-	`sha256:aefa3980091649585253ddf6edaae6e61d7be2a69f95748b70bfba95f06512fa`  
		Last Modified: Mon, 28 Sep 2026 20:13:27 GMT  
		Size: 5.5 MB (5535016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5158365957a5a1aeeca0395b23a1b0d1b20fe3a322f34c0236b7be849bd39c4`  
		Last Modified: Mon, 28 Sep 2026 20:13:27 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json
