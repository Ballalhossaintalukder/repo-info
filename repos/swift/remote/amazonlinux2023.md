## `swift:amazonlinux2023`

```console
$ docker pull swift@sha256:7645e195b544abf4a8bd5bf31ee73dfad51fea61ce7445fbe6d9c7a580b3290c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023` - linux; amd64

```console
$ docker pull swift@sha256:f289fd31507bd062b907ef668c862010cc2010b2f27b0dd7e877b74e8554d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1564207455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c7fdaaebbfbe3f2a0245a4f72b7ac97ffe2452ec98d1c17036af5058ef6a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:16 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Sep 2026 20:15:16 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Sep 2026 20:15:16 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Mon, 28 Sep 2026 20:15:19 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:19 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:16:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Sep 2026 20:16:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63b60e57df2613bc0cb1022dfd5413346ec3c7e0209395d9e14835e596cf97`  
		Last Modified: Mon, 28 Sep 2026 20:18:36 GMT  
		Size: 305.2 MB (305150584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c2d9973393e91d025099c4507cade9414d9b29eb1ce67bd2baee1365170597`  
		Last Modified: Mon, 28 Sep 2026 20:18:31 GMT  
		Size: 24.2 MB (24163569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810528431880b42643bf278b88c399ba216f30669345fbce3d35ad675e85c08e`  
		Last Modified: Fri, 18 Sep 2026 23:53:37 GMT  
		Size: 1.2 GB (1180263301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bcc9bca41a43e38531524dbe10350e4da7663fe2a790eb01bbd14d098739cf`  
		Last Modified: Mon, 28 Sep 2026 20:18:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:104bfd1861ed070029fa8cb2160a50b36442a2ff7373c33d4ca293118928a4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13818147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90180763d71e5ccdbc97dd971b4ccbf2a607e764caca9fe22ea737b3f16c67a0`

```dockerfile
```

-	Layers:
	-	`sha256:f0623eb7c2438344618c723fe4d52bda616b0e57144fea5b7229d0fad01a88f7`  
		Last Modified: Mon, 28 Sep 2026 20:18:30 GMT  
		Size: 13.8 MB (13801920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c764a889bc3a17d24340f605c0e1b5f6068aa46ca5eca8827c7d99180bfbbb`  
		Last Modified: Mon, 28 Sep 2026 20:18:29 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:443116445d76ca4a3b0823fa6a445040a81d1e8aa2feac28efaf2347d789fc95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1546863700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f51962c386846ab6d4a3d93c8e4d90a0a0ef583696df0c29b8d47cfdb8b3aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:17 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Sep 2026 20:15:17 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Sep 2026 20:15:17 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Mon, 28 Sep 2026 20:15:19 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Mon, 28 Sep 2026 20:15:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:19 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:58 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Sep 2026 20:15:58 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc98597faaf94292a51eb8201d8812ee079f0dd32ceadb8e178fc8037ae8064`  
		Last Modified: Mon, 28 Sep 2026 20:18:34 GMT  
		Size: 296.4 MB (296420511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b31297b199da8d702e495f2d55091b63d5d6046a8e749b4f37fc377906ffc46`  
		Last Modified: Mon, 28 Sep 2026 20:18:28 GMT  
		Size: 23.8 MB (23754340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc92733721620898d7ca8d6998c1f4d8e02c5afa896765af2a942061e690c846`  
		Last Modified: Fri, 18 Sep 2026 23:53:07 GMT  
		Size: 1.2 GB (1173190889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26a2c536b22288a65c54c25b1eef82eb9565f7ce3e33401cda66b36a1343e2a`  
		Last Modified: Mon, 28 Sep 2026 20:18:27 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:e294378d87b94e467a3e99a7f6370a5e7cf2b0c7a857acad5da641fc2c75f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13688337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff253c0b548355570c7e294aa70c49478b86193c9ea704d345b126c988f55c59`

```dockerfile
```

-	Layers:
	-	`sha256:379138f406b4e9ac8f89ae33f871c16ecad657beade33dbcd8458cb16cb406a4`  
		Last Modified: Mon, 28 Sep 2026 20:18:27 GMT  
		Size: 13.7 MB (13671973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65403fd9b588009ac31d5c0a40da2bafcb0339b754464f9aff487d081597275f`  
		Last Modified: Mon, 28 Sep 2026 20:18:27 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
