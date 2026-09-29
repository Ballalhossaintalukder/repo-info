## `gradle:6-jdk8-ubi9`

```console
$ docker pull gradle@sha256:84af4a848865425ef4721b651fa0c6ac4e926b634322e3949555de277119341e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:a4c19310ea5d955bbf54f4b7b811ffda9969eb83ddd66dd65029923a267bc2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269575647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13164925aca65b846a483adba0a8dc0c3a0984eb0353f82d7c41ecec9c7118f8`
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
# Tue, 29 Sep 2026 17:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:25 GMT
ENV JAVA_VERSION=jdk8u504-b01
# Tue, 29 Sep 2026 17:52:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='57b7ed8af9d48542bb49ff7894448040b17bea0a48b41677d11ecaec6129768d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u504b01.tar.gz';          ;;        ppc64le)          ESUM='9ab4f48f91c5e140c732cef76a332989aeef9df7a19b2436de7833ef9d7d8960';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u504b01.tar.gz';          ;;        x86_64)          ESUM='9c70e102f527ac674ac2fe9c7d47b9a04e2d19842ba5ab8e9b33f368bbadfaea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u504b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 18:08:07 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:08:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:08:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:08:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:08:07 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:08:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:08:12 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 29 Sep 2026 18:08:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 29 Sep 2026 18:08:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:08:14 GMT
USER gradle
# Tue, 29 Sep 2026 18:08:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:08:14 GMT
USER root
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e62118294e2a180ff63c4c86b42ffab9ce9afa17bc95793dd5305b4886c4a`  
		Last Modified: Tue, 29 Sep 2026 17:52:44 GMT  
		Size: 27.6 MB (27639795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b988bdc7398b33961d6e2438a9d1c741a2207fcdf2f75a1810b5106f0fed7f`  
		Last Modified: Tue, 29 Sep 2026 17:52:45 GMT  
		Size: 55.2 MB (55192703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9f7a4c66d8e02fabb3412090d7d92902ed4071ad507cf7c38266f130f51b8`  
		Last Modified: Tue, 29 Sep 2026 17:52:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a407f8251980dd98f1f6cd14c357db675871fe235dee608e9f80650d6597a87`  
		Last Modified: Tue, 29 Sep 2026 17:52:43 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1782c5cb51a2b10d4c189f6d697e1a5f562d529e1e0fa470c5e3c0d748c65a`  
		Last Modified: Tue, 29 Sep 2026 18:08:30 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111ce82ccf3ba26980cde53b7ddd2afe13c8d2c0fe7a61c572dd1919bfbf136`  
		Last Modified: Tue, 29 Sep 2026 18:08:31 GMT  
		Size: 37.9 MB (37872927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d1cab2bc93b5c4540767b8cec64e8d4542ec113dc2934713c9717d67d65a5e`  
		Last Modified: Tue, 29 Sep 2026 18:08:33 GMT  
		Size: 107.7 MB (107696648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405849af477fb1d71b9caa31fc4cf970ea5e823b9cb0806176f3bf50fb63cb7`  
		Last Modified: Tue, 29 Sep 2026 18:08:30 GMT  
		Size: 431.3 KB (431271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:408fb6a5eba48905497f5becc7163a93e6f4cff8ee46fa641ad2d36db19b9360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecdc9d8160ab0319488fe8761c5cf925b59d2571a1ee221bc44bdc9994bbe8a`

```dockerfile
```

-	Layers:
	-	`sha256:7e68130ffa1203c0eb394976fa1574c0c8d12b8ae12f6b3e180d9db7d52156b9`  
		Last Modified: Tue, 29 Sep 2026 18:08:30 GMT  
		Size: 5.4 MB (5420743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692f4f7ba11370e668e6eff2fbb85f6989d1789266ee5563eaca74fbbf4bf3f8`  
		Last Modified: Tue, 29 Sep 2026 18:08:30 GMT  
		Size: 23.6 KB (23555 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:447f6eab1c009b151836ff769a590625635f5281d4876d1e5de368b777ecee16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266438495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea23366564735ff540b2f9301c2a57bd947ffd7b45e539a6fe71f96aa543b94`
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
# Tue, 29 Sep 2026 17:52:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV JAVA_VERSION=jdk8u504-b01
# Tue, 29 Sep 2026 17:52:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='57b7ed8af9d48542bb49ff7894448040b17bea0a48b41677d11ecaec6129768d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u504b01.tar.gz';          ;;        ppc64le)          ESUM='9ab4f48f91c5e140c732cef76a332989aeef9df7a19b2436de7833ef9d7d8960';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u504b01.tar.gz';          ;;        x86_64)          ESUM='9c70e102f527ac674ac2fe9c7d47b9a04e2d19842ba5ab8e9b33f368bbadfaea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u504b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 18:05:32 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:05:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:05:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:05:32 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:05:32 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:05:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:05:37 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 29 Sep 2026 18:05:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 29 Sep 2026 18:05:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:05:40 GMT
USER gradle
# Tue, 29 Sep 2026 18:05:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:05:40 GMT
USER root
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d723a2fe2c8a61a8fbdff3bb72ebe20e8e741e31fa9fa405ee2a188d0fcc4cec`  
		Last Modified: Tue, 29 Sep 2026 17:52:23 GMT  
		Size: 28.1 MB (28079026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a523ef688ddddf382810c4cc96fe1cb8cff1f9d8499ff2b0f30a1b5093ce7`  
		Last Modified: Tue, 29 Sep 2026 17:52:24 GMT  
		Size: 54.3 MB (54254840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169900422bec84a160027e847f229ca072e20e149ea758cc7d30f2651d14bd0`  
		Last Modified: Tue, 29 Sep 2026 17:52:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20676f6bf979845981bbeea11dc862b30ac1a1c882053821f163ec1438a573b`  
		Last Modified: Tue, 29 Sep 2026 17:52:22 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198e0c907fe1c592ae2e546ecdce7dceec6de86d35e3aa82d6db6a8e669fd27`  
		Last Modified: Tue, 29 Sep 2026 18:05:55 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8639369b14fd9428edef986bd1d60d99f18fb3e4397cd53b06f8b1656c2f39`  
		Last Modified: Tue, 29 Sep 2026 18:05:56 GMT  
		Size: 37.2 MB (37165908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9850e3387d8381117a04cc6b4aad93aea036f99de78b1ab9a167d774708aad`  
		Last Modified: Tue, 29 Sep 2026 18:05:58 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280725503de48f96371b3bac940691ec0bbde05fab74fb533b3e100402dd5be1`  
		Last Modified: Tue, 29 Sep 2026 18:05:55 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:87d114046e2211d99ee533bb7bcd843a560a212d17bd571015aa25aedddc9639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea4a3af995a9a9de4b39a2e1f5bfc166b6e3a9b9ae73d1c37ebd2a3f14355cc`

```dockerfile
```

-	Layers:
	-	`sha256:6c9c9ec6aeb564ec828f6ac42b75ab7236800e42dba61350c8c99274df901c9a`  
		Last Modified: Tue, 29 Sep 2026 18:05:55 GMT  
		Size: 5.4 MB (5419067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95ff7e0c859e420e968cc80837f37ffd99ff459bb5af903e06489bbed354bfa`  
		Last Modified: Tue, 29 Sep 2026 18:05:55 GMT  
		Size: 23.7 KB (23728 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:01f592875437629adb88d8fb25023d9b6f15a22043c1581e71390db7ff70d437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274730088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac749c9838409df6907842652573576fca721b4938c9642d810f48a40a34e5`
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
ENV JAVA_VERSION=jdk8u504-b01
# Tue, 29 Sep 2026 17:51:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='57b7ed8af9d48542bb49ff7894448040b17bea0a48b41677d11ecaec6129768d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u504b01.tar.gz';          ;;        ppc64le)          ESUM='9ab4f48f91c5e140c732cef76a332989aeef9df7a19b2436de7833ef9d7d8960';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u504b01.tar.gz';          ;;        x86_64)          ESUM='9c70e102f527ac674ac2fe9c7d47b9a04e2d19842ba5ab8e9b33f368bbadfaea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u504-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u504b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 29 Sep 2026 17:51:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:51:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:51:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 18:33:36 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:33:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:33:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:33:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:33:37 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:37:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:37:41 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 29 Sep 2026 18:37:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 29 Sep 2026 18:38:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:38:36 GMT
USER gradle
# Tue, 29 Sep 2026 18:38:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:38:37 GMT
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
	-	`sha256:27c47916814e001f77c13ecf79f7279975821e0a560f8da48ee2327f1ea29c7b`  
		Last Modified: Tue, 29 Sep 2026 17:51:59 GMT  
		Size: 52.7 MB (52667662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272703467f95fca6a3e8fc1f8c6be51db1a1f2fdfbc4edfab624d0b2cdc17480`  
		Last Modified: Tue, 29 Sep 2026 17:51:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dac143a2d036f0b9070c272be4cb3f9334273e7bf297ebb53211cbb8090be5`  
		Last Modified: Tue, 29 Sep 2026 17:51:57 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680d742ff146bb3150610df872ab23c289243637d994bccc9369514cfaecdbfd`  
		Last Modified: Tue, 29 Sep 2026 18:34:41 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4625e15155d1728a9f8d01e29a9fa08fbf8fce3297d512073886a837972f0043`  
		Last Modified: Tue, 29 Sep 2026 18:38:32 GMT  
		Size: 39.1 MB (39140287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3819448e07c37af4d86ccf8e0b8fc09bb94cc4abcdcb902a5ed3ee183a51116b`  
		Last Modified: Tue, 29 Sep 2026 18:39:15 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ddeb565c311173d89f49ae7adf3e51111d0e0fcdececbcfef81f29752c568d`  
		Last Modified: Tue, 29 Sep 2026 18:39:12 GMT  
		Size: 35.0 KB (34980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:bef9f49449c4b716b0f0973ea3a3dac1f4cf4410e20f49381621e684534fa75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5440532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160007111dd91ac4a58d14622498689d34f1d6404585c35801feb0f136acb56`

```dockerfile
```

-	Layers:
	-	`sha256:07399ba7179880e38dd19eeecdbd4655f5fed1d13ff4caeecd4cf35b4e432f57`  
		Last Modified: Tue, 29 Sep 2026 18:39:12 GMT  
		Size: 5.4 MB (5416917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b110f2220a16427b8a61b93feedaae15613de6a40603569afd01ce04abf3366`  
		Last Modified: Tue, 29 Sep 2026 18:39:12 GMT  
		Size: 23.6 KB (23615 bytes)  
		MIME: application/vnd.in-toto+json
