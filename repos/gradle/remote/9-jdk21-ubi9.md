## `gradle:9-jdk21-ubi9`

```console
$ docker pull gradle@sha256:b2ac3bc5f173d21b716f8b8af3bd2c70afde96552202318a7ddbceb16e4a462f
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

### `gradle:9-jdk21-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:b9c9801731b11349bd08ada3f47331a505162fa9dcc733cffc289a0220c2cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415925398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a8b7f3e0015db3cc38781bea3f562f2d877209e0256d0dfd4afba727549842`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:53:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:53:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:53:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:30 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:53:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:40 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:06:58 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:06:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:06:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:06:58 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:06:58 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:07:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:07:03 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:07:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:07:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:07:07 GMT
USER gradle
# Tue, 29 Sep 2026 18:07:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:07:07 GMT
USER root
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89432a597dc1d92ca50427b943f2559c9258e50e626ea12837c5cc859d0c1fb`  
		Last Modified: Tue, 29 Sep 2026 17:53:58 GMT  
		Size: 27.6 MB (27639544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe92609f612d239bcbd469225927fe181d339ca787242cae6c07cf6c044563`  
		Last Modified: Tue, 29 Sep 2026 17:54:00 GMT  
		Size: 158.1 MB (158120100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32368d081ce9a4ada49e19e8746f3b8e917f559b0ef4042f84366abb5673101`  
		Last Modified: Tue, 29 Sep 2026 17:53:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40807e1882a25607241d62a350435e6ba2c551b9e03ac39c3e6aeb24bc099a2c`  
		Last Modified: Tue, 29 Sep 2026 17:53:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c47da5a40f1237e7b7ffb7792c4a2954fcd6cee8c630247e4c32b3e7dff7f`  
		Last Modified: Tue, 29 Sep 2026 18:07:24 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082e42c1d76d401d50aa78cd2c9718b28c6392f23331239813780db13751f782`  
		Last Modified: Tue, 29 Sep 2026 18:07:26 GMT  
		Size: 37.9 MB (37873593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83ff75212037a77394ac6400ec24f600d67ed98b937148cb9fb62aea3fc48c4`  
		Last Modified: Tue, 29 Sep 2026 18:07:29 GMT  
		Size: 151.5 MB (151524261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d88ee44ed36e90385442f5994c172685d278c2f7571720d78c13bb64f56fb0`  
		Last Modified: Tue, 29 Sep 2026 18:07:25 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:f8bb2a3252eaa957d85c24d825bc090abc96c8bfddf9222538cdf2a76ffbf3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5392ee00273f7b488c60f9a8dd6dd22c42d57c80ed1cfa59e8777b1c5315571`

```dockerfile
```

-	Layers:
	-	`sha256:747ed30ae4ad51ae7c9540bd1e59b6d82580ec582cadd0bcfcaefc415006b070`  
		Last Modified: Tue, 29 Sep 2026 18:07:24 GMT  
		Size: 5.4 MB (5440781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a689e5703e3354785cea15f223cb9abef57198c0d3dc524bb7b5a853c30d70`  
		Last Modified: Tue, 29 Sep 2026 18:07:24 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:01bd9ac8266d92e0765e24fe28bf23c5be970099cee703cbbf4b3e0e9e557d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412019046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d7fa3f799e08ed680b1c578f726f2250e15e514750d988947f21f995dd095`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:40:13 GMT
ENV container oci
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:26bad3d4d2596a56fa0052979d37eb15831e83f431a1beb342ce4d8a82c10ef9 in /      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:40:14 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /root/buildinfo/      
# Mon, 28 Sep 2026 00:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:39:53Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:39:53Z" "architecture"="aarch64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:39:53Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:53 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:04:14 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:04:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:04:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:04:14 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:04:14 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:04:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:04:17 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:04:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:04:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:04:21 GMT
USER gradle
# Tue, 29 Sep 2026 18:04:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:04:21 GMT
USER root
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f619e2e63c187339efdf8a47e421a9dea6029ef06ea1cf90c309d2d7eb6d43`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 28.1 MB (28078997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5fff03f99d2fde75a1db7e6e95bc146b6e9c0e0b3626c6a1ab36e721f75119`  
		Last Modified: Tue, 29 Sep 2026 17:53:15 GMT  
		Size: 156.4 MB (156403414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734987a8e799550a20eeadf097ecee9473e5000a2c09429e846d1b6d5bd946c`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bebfa1fe5f4e492064b7db416e522f347741eea3dfc51c07ed8131b0853a952`  
		Last Modified: Tue, 29 Sep 2026 17:53:03 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de05f7c8b8f640689386f68f97ed11ae8421d585aa5d683d86d1926172e1c57f`  
		Last Modified: Tue, 29 Sep 2026 18:04:38 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160e65b7aae2c9276360c3dcc8e53742d09a71bb9ba0a0ecf437eddd5611688`  
		Last Modified: Tue, 29 Sep 2026 18:04:40 GMT  
		Size: 37.2 MB (37165991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d34e039e5838ef8bcb323b6fdd5e33e6d9b4771f333282b6cf871dbe58cfc2`  
		Last Modified: Tue, 29 Sep 2026 18:04:42 GMT  
		Size: 151.5 MB (151524308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ead9553dfcfa770c675d6ebcb35e8b8d1c540e223ab4c55868153508ce934d`  
		Last Modified: Tue, 29 Sep 2026 18:04:39 GMT  
		Size: 29.3 KB (29331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:2e4a356b5bf2d2458045b8883118b61ba657cf9d50951bb1eb2d32ffaeae14ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5462088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d21ac4ba8281b977cbcc8765fbe397c189852e2d282c7de83a3af44a184175`

```dockerfile
```

-	Layers:
	-	`sha256:b777cc7842ebfd0c5cb43977aa9cda340adaceae817a18a7ad0641b5fd70a698`  
		Last Modified: Tue, 29 Sep 2026 18:04:39 GMT  
		Size: 5.4 MB (5438393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d69a4aac58453428c45b9dd274906ddb2750b717b15bdb10a4dccbbc326fe25`  
		Last Modified: Tue, 29 Sep 2026 18:04:38 GMT  
		Size: 23.7 KB (23695 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:dd0a623b7e1dd170953cd9b8875189c8d41c90c4ebc62822c720d58c71cf4387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424139670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230077514a1c8adbcbc2973a163561586d410e9d988152a7279faf4494ba1f38`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:40:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:40:37 GMT
ENV container oci
# Mon, 28 Sep 2026 00:40:37 GMT
COPY dir:39a9852bd8811363d9adcef96567534b6b5f1a8c97d6cc243c9f45695de7ae8b in /      
# Mon, 28 Sep 2026 00:40:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:40:37 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:40:38 GMT
COPY dir:afd56b8b048c17b04ea95c60710b6b00284b68368f9925aa7735791c04fa2f0b in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:40:38 GMT
COPY dir:afd56b8b048c17b04ea95c60710b6b00284b68368f9925aa7735791c04fa2f0b in /root/buildinfo/      
# Mon, 28 Sep 2026 00:40:38 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:40:16Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:40:16Z" "architecture"="ppc64le" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:40:16Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:50:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:50:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:50:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:50:56 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:58:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:59:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:59:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:59:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:59:01 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:28:14 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:28:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:28:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:28:14 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:28:15 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:28:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:28:34 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:28:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:28:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:28:40 GMT
USER gradle
# Tue, 29 Sep 2026 18:28:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:28:42 GMT
USER root
```

-	Layers:
	-	`sha256:b4df125287a99547a8c87e27b220bf4e6df4f08a66ea5ede742573191d7b131e`  
		Last Modified: Mon, 28 Sep 2026 06:22:55 GMT  
		Size: 45.1 MB (45125965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a0a0a18f7470307842be5fa42db2cab9bb1ea4f58d3d4eced99f0a7110d8a`  
		Last Modified: Tue, 29 Sep 2026 17:51:58 GMT  
		Size: 30.1 MB (30060202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85171de9cf1ecd50a44be3c9aa351c82c736024044efde3fd83a4ebae911e69`  
		Last Modified: Tue, 29 Sep 2026 17:59:58 GMT  
		Size: 158.3 MB (158284395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1691c5367ac7b9e7e35e5bc9b3f8afc3147fa2870c1fd4060898713869aa52e`  
		Last Modified: Tue, 29 Sep 2026 17:59:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa904bae841e032c5a73335d28b3031b26dd1127e727b866acc1609d1e9c1e`  
		Last Modified: Tue, 29 Sep 2026 17:59:55 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de2d7c9a8d9b27744f62bc5a2218b217c5addea894b668b3dfa41ed7bb7713`  
		Last Modified: Tue, 29 Sep 2026 18:29:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f065bb7e3981f78764b33044eb0b2965886b4dffa2433ed9ae92a590c13cb`  
		Last Modified: Tue, 29 Sep 2026 18:29:31 GMT  
		Size: 39.1 MB (39140158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62a1a89ba76345ea0943143527ca7b366cbe2866055e30544f727ac9d77495`  
		Last Modified: Tue, 29 Sep 2026 18:29:33 GMT  
		Size: 151.5 MB (151524262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9720dd34a68d39d7cf69b497ef168e5cc6116ab0394d43185791506fe4cd0f1b`  
		Last Modified: Tue, 29 Sep 2026 18:29:29 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:16797c4390a9db29695e27d65819e9283dbea1b12be77fa38b1589ae69cfc3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f7aa371cc89f763344ddc239bc3b4ba377fb1d9a4344311b999eb8c152f0e`

```dockerfile
```

-	Layers:
	-	`sha256:7c5e530c646940e0ae46d78bf25327493f867a1d1e724c3095a1c35f4ed6bcf6`  
		Last Modified: Tue, 29 Sep 2026 18:29:29 GMT  
		Size: 5.4 MB (5436354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd4d2bfa2939b632dddf288e5b6099af375f9d4b963cb3a124eef2210a3e5ef`  
		Last Modified: Tue, 29 Sep 2026 18:29:29 GMT  
		Size: 23.6 KB (23588 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:6a1a48847c9fd505370ed71d578fb89777f9d8a100ea8c333c3ef0e4fa31924f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402759100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de5823fee8efe1a64031f98bcdfff2f6ddbadd98fec6f2476e8560949ec002b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:42:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:42:30 GMT
ENV container oci
# Mon, 28 Sep 2026 00:42:31 GMT
COPY dir:f4f8a65b58a566dd7996007eacbffb4c58ae81b1c392bce06d1b27968c700fcb in /      
# Mon, 28 Sep 2026 00:42:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:42:31 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:42:31 GMT
COPY dir:a1c31666842e86648ae88c07e1757b471002e0fda0e035d2cc5b892683f0d5a7 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:42:31 GMT
COPY dir:a1c31666842e86648ae88c07e1757b471002e0fda0e035d2cc5b892683f0d5a7 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:42:31 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:41:49Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:41:49Z" "architecture"="s390x" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:41:49Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:50:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:50:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:50:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:50:38 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:17 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 17:59:13 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 17:59:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 17:59:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 17:59:13 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 17:59:13 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 17:59:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 17:59:20 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 17:59:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 17:59:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 17:59:24 GMT
USER gradle
# Tue, 29 Sep 2026 17:59:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 17:59:25 GMT
USER root
```

-	Layers:
	-	`sha256:268ba595443e8bbceff60eebc6529d0f7b6a9c579db7db802d5e32626c148b67`  
		Last Modified: Mon, 28 Sep 2026 06:22:50 GMT  
		Size: 38.7 MB (38736120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42cb079d4a5b467bfaef3f1841ca6a60a00d654483bff6f232edae3457c8ed`  
		Last Modified: Tue, 29 Sep 2026 17:51:07 GMT  
		Size: 27.7 MB (27669490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406d2fdf078d4c54d6678aef6a248f93858f7f23d22417e7786c51e6b4f20a0c`  
		Last Modified: Tue, 29 Sep 2026 17:52:45 GMT  
		Size: 147.3 MB (147347996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2fb38d229463c89fdd48e124ce0f551ca01ed4c9c4814e7b4cda29f998136a`  
		Last Modified: Tue, 29 Sep 2026 17:52:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ea167ecc8f05e92c5219c3675f907c81a0e37460409cbf9dfd79a9af4bb823`  
		Last Modified: Tue, 29 Sep 2026 17:52:42 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a201857455dc88b7b19767394bf4bc7ab6472235247ec83f47943f6c9eb6844a`  
		Last Modified: Tue, 29 Sep 2026 18:00:17 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549fdd451dcb4bf277046a36a024f5a21f6c7537acc1ace2319641f905609467`  
		Last Modified: Tue, 29 Sep 2026 18:00:20 GMT  
		Size: 37.5 MB (37476548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5dba14941fb6f4c0f56dd32dcaec5366b57e24d3d198b691dbbe2aa71200a6`  
		Last Modified: Tue, 29 Sep 2026 18:00:23 GMT  
		Size: 151.5 MB (151524262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1f1e8c5bc71bb2e3eee14e424e98b9e8bb6ce12f74bb50724e9270976eefec`  
		Last Modified: Tue, 29 Sep 2026 18:00:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b041235593c50e345fd7b86662fb515cc36786fdcb38e0ba278a46806c3dd160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f29d47f56ee7337456674e2b845e2ab1124fa265096d3e331fc1b54cc809ca`

```dockerfile
```

-	Layers:
	-	`sha256:2760c471c78cb53e7377b1e6ef60c3ba61da233ab1982dd3793a72331e8278bc`  
		Last Modified: Tue, 29 Sep 2026 18:00:17 GMT  
		Size: 5.4 MB (5425604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b56a544e9c20a00b3db2a6d8d5fc4b59d7eec99f666978b44693568b1f5b40`  
		Last Modified: Tue, 29 Sep 2026 18:00:17 GMT  
		Size: 23.5 KB (23532 bytes)  
		MIME: application/vnd.in-toto+json
