## `eclipse-temurin:21-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:4c79c3e27ee5a5f8fa2aa1650d7bb74f56b87d8c39ea1a0face846181fbca391
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fca85ad1bee1996ae8324d027a7d06154b49392d7aab6938f596e819750386e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125876808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6c7dcd701e6c5c93b7c24ed20fcc070787bc42625993aaf1cdfddf4565526a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 00:57:55 GMT
ENV container oci
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:c94af32992a1c8563dae2c41b7cbae240915b79b6cafaf819ca86a1c2db6bfb3 in /      
# Mon, 28 Sep 2026 00:57:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:57:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:2ced94c8bcf5dc4ee352fe2c68f9c259358bc1a6ec5d2ce9613e5d90666c4655 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:2ced94c8bcf5dc4ee352fe2c68f9c259358bc1a6ec5d2ce9613e5d90666c4655 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:57:32Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T00:57:32Z" "architecture"="x86_64" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T00:57:32Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:53:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:53:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:53:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:00 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:53:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='14be1f35ebdbd1f6e8d57eb911a3ffb74d6d9aa255abc5daf2b1302002cf2cf2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='d2f07f1d97faab23b3add1af92db402b721b5b251cedab7144fdd4b2bf2e2f13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='df43dc82a935868915a4b76227e2c63ffeb32868b608980dc67312a3d6217e1e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='2413149700df0f7d440500a84a8f764c535f21e5a5e87d38328b64eec2c5b500';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 29 Sep 2026 17:53:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a34145e205c19dadb74ed940321031a946571a492b3cf835b60f57003df2bdee`  
		Last Modified: Mon, 28 Sep 2026 02:11:46 GMT  
		Size: 34.9 MB (34929005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66472a2d5cdfc24f33db1b7c3502c00c7952e6d2c6579a20a5b6a00141b987`  
		Last Modified: Tue, 29 Sep 2026 17:53:17 GMT  
		Size: 37.9 MB (37852415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f5afd68b722c242bbe8259a474e26ba08beafe25b71517f06b6ada17907a2`  
		Last Modified: Tue, 29 Sep 2026 17:53:41 GMT  
		Size: 53.1 MB (53092788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa05ec0dc339932cfa1df5b0733111a5b385b28a3c2e9a1635defb39c61bc6`  
		Last Modified: Tue, 29 Sep 2026 17:53:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40807e1882a25607241d62a350435e6ba2c551b9e03ac39c3e6aeb24bc099a2c`  
		Last Modified: Tue, 29 Sep 2026 17:53:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:567ac9e939b4050a567b77a92d022adc3fd14007dc12489fd0a39676636640f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d518aeea944204da1900cd93daac4054107b5fcb7c38f975b68dc86a53511798`

```dockerfile
```

-	Layers:
	-	`sha256:d846bfbff21fab47441f102940412ae8e839f5817375e7f397de279ab7e5c20d`  
		Last Modified: Tue, 29 Sep 2026 17:53:39 GMT  
		Size: 3.7 MB (3709281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8878c1d6ef9ba7af91840c86ca6cabd5518f63faf5b8bb60ab016255555a22`  
		Last Modified: Tue, 29 Sep 2026 17:53:39 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:53e26d95c584156de0a3d6199e4a6b1f5b51316f8e8403e54e0d920d19886bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123188320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2854071c6e5a8eb765caae58efdaeb9b545f262abbe8f70950a80018be4e6b1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:00:40 GMT
ENV container oci
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:ab0c5d24ca1747829dc1e0e979790e14bee66df400e8e4d271a15d552af407bf in /      
# Mon, 28 Sep 2026 01:00:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:00:41 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:7aacb9dad5ed908942374b1668501c386999af28176419b212897b761c97da4e in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:7aacb9dad5ed908942374b1668501c386999af28176419b212897b761c97da4e in /root/buildinfo/      
# Mon, 28 Sep 2026 01:00:41 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:00:17Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:00:17Z" "architecture"="aarch64" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:00:17Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:52:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='14be1f35ebdbd1f6e8d57eb911a3ffb74d6d9aa255abc5daf2b1302002cf2cf2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='d2f07f1d97faab23b3add1af92db402b721b5b251cedab7144fdd4b2bf2e2f13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='df43dc82a935868915a4b76227e2c63ffeb32868b608980dc67312a3d6217e1e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='2413149700df0f7d440500a84a8f764c535f21e5a5e87d38328b64eec2c5b500';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 29 Sep 2026 17:52:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:842ae2bcf67a61456b432d1f1a94bcb7d69f0613459a34bb97404ab26399ad66`  
		Last Modified: Mon, 28 Sep 2026 02:12:22 GMT  
		Size: 33.1 MB (33124832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58d851c2a3e9c7ff80385d5468a23bace59ac39ea6840594441870f624816d`  
		Last Modified: Tue, 29 Sep 2026 17:53:04 GMT  
		Size: 37.8 MB (37792412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5ddf6381422133f30b4c2694095c8255e198a4672a16995ecc585291a73a28`  
		Last Modified: Tue, 29 Sep 2026 17:53:05 GMT  
		Size: 52.3 MB (52268478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa3ab2458e402582edf7df35dcca9d305866db43505f86005d34417aab18d7`  
		Last Modified: Tue, 29 Sep 2026 17:53:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bebfa1fe5f4e492064b7db416e522f347741eea3dfc51c07ed8131b0853a952`  
		Last Modified: Tue, 29 Sep 2026 17:53:03 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b019f6931636086fc3ea60507be130382c385c60adac3bfc21d013d1277b3971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea10370dd275111c38f70c8429dc582b7e164fd6d0c6858c4a3051ace933768`

```dockerfile
```

-	Layers:
	-	`sha256:f7a1b9bec47dc23b8168ae97772a8ebe2cced19bced9eb07266b0af3064aa91a`  
		Last Modified: Tue, 29 Sep 2026 17:53:03 GMT  
		Size: 3.7 MB (3708695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702eefa60d1d8da9b43e897ff2c738d59e4729d823912f482ef8dd2f4e12638c`  
		Last Modified: Tue, 29 Sep 2026 17:53:03 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c1abda72934b1784916e608217658b53ee1204012eaab78ce7f78da97a6c17d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131846825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6786157210ed08a8a01d39f13e14d6bf8bc091468b52b6ed29a3c18e8ed689f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:00:57 GMT
ENV container oci
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:15640a8bb09c7ee6c64cb6dd35f25cbd39908e3326f3c8d28382a9522b129d54 in /      
# Mon, 28 Sep 2026 01:00:58 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:00:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:9e1e6cef5a4091efaa305feea8bbd3feed428affc645bb8ad805c85f218842d6 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:9e1e6cef5a4091efaa305feea8bbd3feed428affc645bb8ad805c85f218842d6 in /root/buildinfo/      
# Mon, 28 Sep 2026 01:00:58 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:00:35Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:00:35Z" "architecture"="ppc64le" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:00:35Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:51:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:51:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:51:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:51:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:51:02 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 18:01:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='14be1f35ebdbd1f6e8d57eb911a3ffb74d6d9aa255abc5daf2b1302002cf2cf2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='d2f07f1d97faab23b3add1af92db402b721b5b251cedab7144fdd4b2bf2e2f13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='df43dc82a935868915a4b76227e2c63ffeb32868b608980dc67312a3d6217e1e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='2413149700df0f7d440500a84a8f764c535f21e5a5e87d38328b64eec2c5b500';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 18:01:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:01:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:869c2426a34dac9af44481336945ab2a560ef9817565e34bc71e3f7d2128897b`  
		Last Modified: Mon, 28 Sep 2026 06:28:56 GMT  
		Size: 39.1 MB (39116127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f01e13405a632fb5996f569fa1fef3486a6651e3352462ab69afd5239becfb`  
		Last Modified: Tue, 29 Sep 2026 17:52:01 GMT  
		Size: 39.6 MB (39616201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628d3cceab4d2023a8b713ccfac4a3b0b74162090a175c4901aa5ce7e2193a1`  
		Last Modified: Tue, 29 Sep 2026 18:01:49 GMT  
		Size: 53.1 MB (53111897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee8193bd1226d4dbc7d87d9b509ad8e6786bdc7285a3833576d43b8c5c19b7`  
		Last Modified: Tue, 29 Sep 2026 18:01:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ff7223662580d24d3b697a339fdd13297b3ba0d0fdce4aaf69bfcc7e9caf97`  
		Last Modified: Tue, 29 Sep 2026 18:01:48 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:97afb7e350c09acac477c69d9977e54e414e632bcd035f6ede516abf62aa7659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a75cc33bf77256d8513d26e9593c41610b9167ceeeadd8d5ed69ee399d3431d`

```dockerfile
```

-	Layers:
	-	`sha256:4ca9ef70a479c84c5b48ef1eebedafa4bbb11291e2be0a11854f72411c504d57`  
		Last Modified: Tue, 29 Sep 2026 18:01:48 GMT  
		Size: 3.7 MB (3698026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1784858703dbfd068d494f24ed3d91339f7edb8a99d99a5f837f81201fa4c3`  
		Last Modified: Tue, 29 Sep 2026 18:01:48 GMT  
		Size: 20.4 KB (20432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7a6e4447d83d1e21a54103dd6f63b84464eaa513ad54e2e7c98e237254033400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122707038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351db52c0332242f069d1f806ccc0b6dd09bcc5e8e4a712b3d193ba6bf3d4ae2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:27:23 GMT
ENV container oci
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:627ae3085e2bde6038f6671100fa887f782801ff3b2f6b6d06098a5bbfa348e3 in /      
# Mon, 28 Sep 2026 01:27:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:27:23 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:a5fd2ac24b6a4404a3524023e09e42dbddc24c5636dee74d1cd2462add8a5608 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:a5fd2ac24b6a4404a3524023e09e42dbddc24c5636dee74d1cd2462add8a5608 in /root/buildinfo/      
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:26:09Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:26:09Z" "architecture"="s390x" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:26:09Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:50:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:50:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:50:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:50:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:50:39 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='14be1f35ebdbd1f6e8d57eb911a3ffb74d6d9aa255abc5daf2b1302002cf2cf2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='d2f07f1d97faab23b3add1af92db402b721b5b251cedab7144fdd4b2bf2e2f13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='df43dc82a935868915a4b76227e2c63ffeb32868b608980dc67312a3d6217e1e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='2413149700df0f7d440500a84a8f764c535f21e5a5e87d38328b64eec2c5b500';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jre_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 29 Sep 2026 17:52:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3e51340b5abee43447a0b1bfecbe6d76485a0883aea31b7aec7aa8f604d00e2f`  
		Last Modified: Mon, 28 Sep 2026 06:28:51 GMT  
		Size: 34.8 MB (34837868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea521d436996441d82bb612e80404ef21f6eb511b209f354a6d3b919ce813e2c`  
		Last Modified: Tue, 29 Sep 2026 17:51:05 GMT  
		Size: 38.2 MB (38231841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19452da8f550f93f6a075d35293e3d9a9fc95462d6f99b28bc40651a43b30525`  
		Last Modified: Tue, 29 Sep 2026 17:52:38 GMT  
		Size: 49.6 MB (49634730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b8210e4192e12b2f40d4a7fba3fc4ee7c4f622266e60dcb1d56c6e1f64ea7e`  
		Last Modified: Tue, 29 Sep 2026 17:52:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572e63d85c66af805f8cdda9fa660bfb9ab61e80df4fddd829c2b65c2bcf508`  
		Last Modified: Tue, 29 Sep 2026 17:52:28 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a68c2c645b8a70071bbd8eb2568e66c3f175ab0b37c3cf1520093ab35a73078e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36512caedecef58a2eaea7fe5a45f08ea2de936ee4b2ffec524722036ac261f8`

```dockerfile
```

-	Layers:
	-	`sha256:eb1e36c0e2c9576233b340b76baa0daa2f9ef659f609ba9f08bac4bb93390448`  
		Last Modified: Tue, 29 Sep 2026 17:52:37 GMT  
		Size: 3.7 MB (3699271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e3e82ae6dc6807a9de74891e517774bfbc9ac6f5c58a46a691d0b03f4a9865`  
		Last Modified: Tue, 29 Sep 2026 17:52:36 GMT  
		Size: 20.4 KB (20402 bytes)  
		MIME: application/vnd.in-toto+json
