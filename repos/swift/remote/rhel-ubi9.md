## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:40bd2ed1652e7fd16c560081549437d8ff4728fa22ca868a195f0c832d100af4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:0e7f68eb785c136731683c34d8a1637b26d67e74e840c3be6645a952f1445bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1352621240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36f87ac3b4a1e81176896ba61680077416a13bd4da26856fc555e63f0aa35b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:45:28 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 28 Sep 2026 00:45:28 GMT
ENV container oci
# Mon, 28 Sep 2026 00:45:30 GMT
COPY dir:f2917551e891312aaca4bcf9138bb48e8b9206b9670618032c878c5d22066d06 in /      
# Mon, 28 Sep 2026 00:45:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:45:30 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:45:30 GMT
COPY dir:72c80b46e5a5b640f99cdd5a3335832534efca210bda281f77293460969a293e in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:45:30 GMT
COPY dir:72c80b46e5a5b640f99cdd5a3335832534efca210bda281f77293460969a293e in /root/buildinfo/      
# Mon, 28 Sep 2026 00:45:31 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:44:34Z" "org.opencontainers.image.revision"="de6cfebe750e57846d6201a17d331080b9df4a01" "build-date"="2026-09-28T00:44:34Z" "architecture"="x86_64" "vcs-ref"="de6cfebe750e57846d6201a17d331080b9df4a01" "vcs-type"="git" "release"="1790556197"org.opencontainers.image.created=2026-09-28T00:44:34Z,org.opencontainers.image.revision=de6cfebe750e57846d6201a17d331080b9df4a01
# Tue, 29 Sep 2026 17:57:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Sep 2026 17:57:18 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Sep 2026 17:57:18 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 29 Sep 2026 17:57:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 29 Sep 2026 17:57:18 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 29 Sep 2026 17:57:18 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Tue, 29 Sep 2026 17:57:18 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Tue, 29 Sep 2026 17:57:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:58 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 29 Sep 2026 17:57:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:e8c9a0e88256fffbb04d5a5244a0f9589a20c9306b564ae22802d12088908198`  
		Last Modified: Mon, 28 Sep 2026 02:13:27 GMT  
		Size: 80.5 MB (80503161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aa0cfc543a4f5e60b9e5565a01cad0e7d61795908eed19bfacc36960577e9c`  
		Last Modified: Tue, 29 Sep 2026 18:00:32 GMT  
		Size: 126.7 MB (126656035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63a07ce8196e061c10e51f879ee10c16c2b568108a5a5311a967e65e68773e1`  
		Last Modified: Fri, 18 Sep 2026 23:53:31 GMT  
		Size: 1.1 GB (1145461870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef6811e08b56ad408ae7c7857e4ec6f2ccf51b52ffcb96ea80732e7f3b78dd1`  
		Last Modified: Tue, 29 Sep 2026 18:00:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:9ceaffd44eaec346320b08c21457d30ead572ade9bddcb69746d6700c8f05834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13015425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12abc054c871d1421be662259d5afe523a5f7e76f3dac08b7d3b063e8c416fe0`

```dockerfile
```

-	Layers:
	-	`sha256:9d5b74652feb667b35944a71720101aec09bfff86429a5789f72c05bab1d4e89`  
		Last Modified: Tue, 29 Sep 2026 18:00:30 GMT  
		Size: 13.0 MB (13000983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:861b5303cca86638d46dcf48bfbb4222ace3595ec33b566b060a8be4334d3ebc`  
		Last Modified: Tue, 29 Sep 2026 18:00:28 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f6b9bcf48a4a0d337b7a8674c206a29ef8956bded58ca8f24ca5b434ab2f0655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1340206245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac3e7e59ed7e9e223ec3df7419de26cd034656d5d713017e199c82cde7fdee5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:46:50 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 28 Sep 2026 00:46:50 GMT
ENV container oci
# Mon, 28 Sep 2026 00:46:53 GMT
COPY dir:25f4f7fc7df514773d372a1f68c0af30996ba2d4f9c4e8cf58375978c545a0cd in /      
# Mon, 28 Sep 2026 00:46:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:46:53 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:46:53 GMT
COPY dir:c9178477311f84f36698f41037d6aa0dd4a51eb103b1abe34f85afa230ac6f9e in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:46:53 GMT
COPY dir:c9178477311f84f36698f41037d6aa0dd4a51eb103b1abe34f85afa230ac6f9e in /root/buildinfo/      
# Mon, 28 Sep 2026 00:46:54 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:46:24Z" "org.opencontainers.image.revision"="de6cfebe750e57846d6201a17d331080b9df4a01" "build-date"="2026-09-28T00:46:24Z" "architecture"="aarch64" "vcs-ref"="de6cfebe750e57846d6201a17d331080b9df4a01" "vcs-type"="git" "release"="1790556197"org.opencontainers.image.created=2026-09-28T00:46:24Z,org.opencontainers.image.revision=de6cfebe750e57846d6201a17d331080b9df4a01
# Tue, 29 Sep 2026 17:56:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Sep 2026 17:56:33 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Sep 2026 17:56:33 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 29 Sep 2026 17:56:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 29 Sep 2026 17:56:33 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 29 Sep 2026 17:56:33 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Tue, 29 Sep 2026 17:56:33 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Tue, 29 Sep 2026 17:56:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:56:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:14 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 29 Sep 2026 17:57:14 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b00ce0d58ccab760c4084393186e2e58086ad6cd256aac305ff159cb75455d3a`  
		Last Modified: Mon, 28 Sep 2026 02:37:20 GMT  
		Size: 78.2 MB (78187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f4930486c74defca2756dbf95cc6e39ab372a919a69cd1aa144247db906d8c`  
		Last Modified: Tue, 29 Sep 2026 17:59:33 GMT  
		Size: 120.0 MB (119973132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c718624100c98820206167ab755ac2b44f8e6956643eab861a60f6e2f106ffa`  
		Last Modified: Fri, 18 Sep 2026 23:53:21 GMT  
		Size: 1.1 GB (1142045503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b72faf89824a080f423edbb00eabd21cb42794af55dcd728265d9ce766d9e`  
		Last Modified: Tue, 29 Sep 2026 17:59:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:21a7833209ed4ff0f3da5b0fa306da562981195e275bf08e0a78bc2ec62a0c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12888239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f494dfb3ea2dd86f5b632af92931473d190f61bfecf37fec14bb5d4c414c9fc3`

```dockerfile
```

-	Layers:
	-	`sha256:805804542ad60fdb57c4a66618277807fb39773dfb796b733fff0fea63c8ed76`  
		Last Modified: Tue, 29 Sep 2026 17:59:31 GMT  
		Size: 12.9 MB (12873682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76741d7c6c1e520b91cf49dc1da93ac47721553d4bb571ca3f410f22d964da8`  
		Last Modified: Tue, 29 Sep 2026 17:59:30 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json
