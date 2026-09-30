## `swift:rhel-ubi10-slim`

```console
$ docker pull swift@sha256:4a732c4e8a56e8ae9a476a5b5e7eb9d90378c72e4e8743e8c911ea5cba3d95ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi10-slim` - linux; amd64

```console
$ docker pull swift@sha256:a501117b961c142970ba3070866e3b4db3dba9d2f1edd161d1fe1c8dcec3a35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a856268e5614649b584bd23c7e4c18a3f04a89c787961ffd62889a8172dafc68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."       url="https://catalog.redhat.com/en/search?searchType=containers"       com.redhat.component="ubi10-container"       name="ubi10/ubi"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       version="10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10"
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 05:11:58 GMT
LABEL io.openshift.tags="base rhel10"
# Mon, 28 Sep 2026 05:11:58 GMT
ENV container oci
# Mon, 28 Sep 2026 05:12:00 GMT
COPY dir:dc383c85e3ce34bea309318e722f2a7a1ad26588b3b62bba2eff4e1298e7559d in /      
# Mon, 28 Sep 2026 05:12:00 GMT
COPY file:7434e7ac38eae122961f7433f94f69681ae6b7673c89bc0a33c8831ed9c5dbfc in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 05:12:00 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 05:12:00 GMT
COPY dir:ef89a2a73e6e580b5c525eabfe3f2d25dda4c2d7c47ef4da8c840ea1447e1624 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 05:12:00 GMT
COPY dir:ef89a2a73e6e580b5c525eabfe3f2d25dda4c2d7c47ef4da8c840ea1447e1624 in /root/buildinfo/      
# Mon, 28 Sep 2026 05:12:01 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T05:11:36Z" "org.opencontainers.image.revision"="b9e72db13de86305a97286e2b2b6d031a9a31489" "build-date"="2026-09-28T05:11:36Z" "architecture"="x86_64" "vcs-ref"="b9e72db13de86305a97286e2b2b6d031a9a31489" "vcs-type"="git" "release"="1790572136"org.opencontainers.image.created=2026-09-28T05:11:36Z,org.opencontainers.image.revision=b9e72db13de86305a97286e2b2b6d031a9a31489
# Tue, 29 Sep 2026 17:57:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Sep 2026 17:57:47 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Sep 2026 17:57:47 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 29 Sep 2026 17:57:47 GMT
ARG SWIFT_PLATFORM=ubi10
# Tue, 29 Sep 2026 17:57:47 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Tue, 29 Sep 2026 17:57:47 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Tue, 29 Sep 2026 17:57:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:47 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi10 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi10 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && yum -y install gnupg2     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:1587de7096c53a0b9fd09d99828507d9d9217e2b7edf597bc375022a17d2b1b9`  
		Last Modified: Mon, 28 Sep 2026 06:48:42 GMT  
		Size: 81.0 MB (81023958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75a41a4e6a3c0362c8b0ce55522f9e9ad3ad76b8f8252640110f04d011ba892`  
		Last Modified: Tue, 29 Sep 2026 17:58:04 GMT  
		Size: 62.9 MB (62938071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi10-slim` - unknown; unknown

```console
$ docker pull swift@sha256:09a4d17c99951ccc7826bae3a7d63365de4dd646643d46fcf8ca65199a295cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5967642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fb7e350474ef9e21c4662f3585b933a7f31adba805a7c61380fb0362f62ba7`

```dockerfile
```

-	Layers:
	-	`sha256:40b45ea307fa900ef9a55d081f05a6f1c0c5c3102037c090e5c11b83c26c9d77`  
		Last Modified: Tue, 29 Sep 2026 17:58:02 GMT  
		Size: 6.0 MB (5955938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0691caa19d416a062fcfc0615d03372a2674aa6ce5408e8e3ce7e411123fd607`  
		Last Modified: Tue, 29 Sep 2026 17:58:02 GMT  
		Size: 11.7 KB (11704 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi10-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:9108ea204b7e048c14881eb6a660d7a349acfbf04475d44f778dd54996ffbc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140558174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4b145517882a9b27a5d01b4e2b9ecb670fd197d6ee8c6b4247f6a35a221e01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."       url="https://catalog.redhat.com/en/search?searchType=containers"       com.redhat.component="ubi10-container"       name="ubi10/ubi"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       version="10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10"
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 05:14:04 GMT
LABEL io.openshift.tags="base rhel10"
# Mon, 28 Sep 2026 05:14:04 GMT
ENV container oci
# Mon, 28 Sep 2026 05:14:07 GMT
COPY dir:a9341c941a671b6f8beeaf11ee8cab5c349edbb1101026a4d87e3056e05bee55 in /      
# Mon, 28 Sep 2026 05:14:07 GMT
COPY file:7434e7ac38eae122961f7433f94f69681ae6b7673c89bc0a33c8831ed9c5dbfc in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 05:14:07 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 05:14:07 GMT
COPY dir:a55c77a19eb90e208ba64817588d3a7231fcae72a65d5689303008a6b1422c57 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 05:14:07 GMT
COPY dir:a55c77a19eb90e208ba64817588d3a7231fcae72a65d5689303008a6b1422c57 in /root/buildinfo/      
# Mon, 28 Sep 2026 05:14:08 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T05:13:40Z" "org.opencontainers.image.revision"="b9e72db13de86305a97286e2b2b6d031a9a31489" "build-date"="2026-09-28T05:13:40Z" "architecture"="aarch64" "vcs-ref"="b9e72db13de86305a97286e2b2b6d031a9a31489" "vcs-type"="git" "release"="1790572136"org.opencontainers.image.created=2026-09-28T05:13:40Z,org.opencontainers.image.revision=b9e72db13de86305a97286e2b2b6d031a9a31489
# Tue, 29 Sep 2026 17:57:35 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Sep 2026 17:57:35 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Sep 2026 17:57:35 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 29 Sep 2026 17:57:35 GMT
ARG SWIFT_PLATFORM=ubi10
# Tue, 29 Sep 2026 17:57:35 GMT
ARG SWIFT_BRANCH=swift-6.4.0-release
# Tue, 29 Sep 2026 17:57:35 GMT
ARG SWIFT_VERSION=swift-6.4.0-RELEASE
# Tue, 29 Sep 2026 17:57:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:35 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi10 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Sep 2026 17:57:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi10 SWIFT_BRANCH=swift-6.4.0-release SWIFT_VERSION=swift-6.4.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && yum -y install gnupg2     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:59ff8e737acbcbe4f8c8b46341649bf94e54951735409b3f33ccd33bf8515c4c`  
		Last Modified: Mon, 28 Sep 2026 06:48:44 GMT  
		Size: 78.5 MB (78544181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ca83df1445ee87f2136f4b014a0d222fe389b24a83cf0876169a33522e9959`  
		Last Modified: Tue, 29 Sep 2026 17:57:54 GMT  
		Size: 62.0 MB (62013993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi10-slim` - unknown; unknown

```console
$ docker pull swift@sha256:54141ae560361a67d3fb635845681558385de9f5d4fbd49a3727c62e452a44ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5964129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8ba02a21f1cdeda6bc09b4ddee9ce6c0db2416b615d9a28fbd3b41664ecd0c`

```dockerfile
```

-	Layers:
	-	`sha256:26a878280ed4c3d01aeb16b2416b59c3058a06512e6c35393e53e53f3efeec1c`  
		Last Modified: Tue, 29 Sep 2026 17:57:51 GMT  
		Size: 6.0 MB (5952340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49569b326fa2cce0f373078742fe5e2b139b01eb3fa6223858b7acd636260c8e`  
		Last Modified: Tue, 29 Sep 2026 17:57:51 GMT  
		Size: 11.8 KB (11789 bytes)  
		MIME: application/vnd.in-toto+json
