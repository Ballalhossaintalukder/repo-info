## `swift:amazonlinux2023-slim`

```console
$ docker pull swift@sha256:2ae708ac7b8c975eea573163dbfd747010d664b98d169aabfe198bf88a492454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023-slim` - linux; amd64

```console
$ docker pull swift@sha256:5276960118c9e7752640d51902d8a8f7ae382465ec97805a5c69cf5bbae149a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286795746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b486d367ce22b02ca6b1c970f5b6217a547d6911d0d4d62d820798d15839c035`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Sep 2026 20:15:22 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Sep 2026 20:15:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Sep 2026 20:15:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 28 Sep 2026 20:15:22 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Mon, 28 Sep 2026 20:15:22 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Mon, 28 Sep 2026 20:15:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 28 Sep 2026 20:16:03 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe033e50f5f61dbae6a4fe74e51bbcfbf14854ec8bcbbbd0586bf4963ae46ce5`  
		Last Modified: Mon, 28 Sep 2026 20:16:25 GMT  
		Size: 176.0 MB (175954274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5074918fc5a9ac406e961d99f5cfb6c03de40d9a88e2f9a1bbe1dcae83d91b`  
		Last Modified: Mon, 28 Sep 2026 20:16:23 GMT  
		Size: 56.2 MB (56211645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d9f1e6267593d62948b36c32d3bd63112e371d24b72fcaa90228f3938331aaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c75542fdb745ad1b11a22005423d843d160bd713129ad1cd2b5e87f7e36416`

```dockerfile
```

-	Layers:
	-	`sha256:043d39308afb745f3a03818172676f7664f0d5eac68bd34ac8ba208191aea94b`  
		Last Modified: Mon, 28 Sep 2026 20:16:21 GMT  
		Size: 6.5 MB (6458562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b4343cfd5d056bacaf762e7e671b4757a85e12c5c7bcb4aa5cf7370a1da8de`  
		Last Modified: Mon, 28 Sep 2026 20:16:21 GMT  
		Size: 13.1 KB (13130 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c3b0d111992e24df171f96c34a0948aefdba9e99b9ec2acb44cdde45a3fa568d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283416689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62e1af64ed790cdbcbbb5c6f37f8e7eb2ed7083e80977cdc4b7111cd79f7b4c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Sep 2026 20:15:11 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Sep 2026 20:15:11 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Sep 2026 20:15:11 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 28 Sep 2026 20:15:11 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Mon, 28 Sep 2026 20:15:11 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Mon, 28 Sep 2026 20:15:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:11 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Sep 2026 20:15:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 28 Sep 2026 20:15:48 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81299081ef1910e193e6e1eb9544803874dd032c8049f5c8dc5cd5918f0b90e`  
		Last Modified: Mon, 28 Sep 2026 20:16:12 GMT  
		Size: 174.3 MB (174313842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c41360dbe2ad5aebd727dbf3c5dc77213312a03b363c60c6334524f50d6b3`  
		Last Modified: Mon, 28 Sep 2026 20:16:10 GMT  
		Size: 55.6 MB (55605060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0e889cc3bea18aae650452b58293df29c06b8d2852c8f57a8f284a101fb62785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4f216ff4978343b859dea58c696c561f3d435dd4041e569d88a45fe9717e50`

```dockerfile
```

-	Layers:
	-	`sha256:b2275c705a43c9820f2ec7253be58e30360536981928aefb71bce8c89ac452a1`  
		Last Modified: Mon, 28 Sep 2026 20:16:08 GMT  
		Size: 6.5 MB (6458069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef19f6639c27f2206da78740c4b6e09cb7b332d0096df29455e22b29e2ed7f56`  
		Last Modified: Mon, 28 Sep 2026 20:16:08 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json
