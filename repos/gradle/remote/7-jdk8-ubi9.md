## `gradle:7-jdk8-ubi9`

```console
$ docker pull gradle@sha256:22bf8c4a7660af9c0497e9bf6d4ff74caeb3d2efab96d34f2540a86e2d8cd0d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:5d64cb463c84fef9517599e949561e53cc26cb62540a5eb2d0d5d84d9ca3d27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289972824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1243f633e153828442b96920970aee875d9f6bef4e3dd07cd35bbd7adf598a2`
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
# Tue, 29 Sep 2026 18:08:00 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:08:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:08:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:08:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:08:00 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:08:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:08:05 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:08:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:08:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:08:08 GMT
USER gradle
# Tue, 29 Sep 2026 18:08:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:08:08 GMT
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
	-	`sha256:f55c57402d76c5a0b3cf088bd4dddd4d5942c96fb24ff21762bef1d93ad6483c`  
		Last Modified: Tue, 29 Sep 2026 18:08:22 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fed0ace287f0252c9f65a50601b4f4595963c8945b0ce20dddc9655cdec615`  
		Last Modified: Tue, 29 Sep 2026 18:08:24 GMT  
		Size: 37.9 MB (37873705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521614bed8531f08edb8594e201f899f69d62d6c6fa193fa13f1fed78647410`  
		Last Modified: Tue, 29 Sep 2026 18:08:26 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad60ee4ccb78ea73aadab640655043d0b6a7c63e2d551da624357311c61cec3f`  
		Last Modified: Tue, 29 Sep 2026 18:08:22 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:8e7a198b75f2007c3a71d2293005769ab092b14fe5ba3941646d199a54d894bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5462193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37521d4142f74baca4537f546468dff4fe0ab9b3773ca2dd66e41ee45f4f192d`

```dockerfile
```

-	Layers:
	-	`sha256:3651b9535329eef72ac093afdc14ec116dbd84d2f91c3453cc35d5082d18e2bf`  
		Last Modified: Tue, 29 Sep 2026 18:08:23 GMT  
		Size: 5.4 MB (5438639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb379ec7f56d4b97f0865f60b81e567581f30269c5af41b3f1417a03ddc76dd`  
		Last Modified: Tue, 29 Sep 2026 18:08:22 GMT  
		Size: 23.6 KB (23554 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c043971b4d192b1d0efc9673cb0c373da26a251a6f8234a44fada3273328dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286845820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90e2653cfbf922e4a92838dff3af940407bf6f2037c99b1fbc25feab002ae7a`
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
# Tue, 29 Sep 2026 18:05:12 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:05:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:05:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:05:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:05:12 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:05:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:05:17 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:05:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:05:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:05:20 GMT
USER gradle
# Tue, 29 Sep 2026 18:05:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:05:20 GMT
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
	-	`sha256:0f970b2f3123fe9b9f81da22a1d3feabb119ef35c1f313797b1c50568342d6e7`  
		Last Modified: Tue, 29 Sep 2026 18:05:35 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf41e67e27a674edc82db43e255baed6ffbecdd325847913f5d8819596eba1b`  
		Last Modified: Tue, 29 Sep 2026 18:05:37 GMT  
		Size: 37.2 MB (37165987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df51899e9051c4ec4cfbfa13adc8f6ca56726855ae05c0ee4e94ffa05391718`  
		Last Modified: Tue, 29 Sep 2026 18:05:38 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6833eea36757dbdce998d6aa2bed5dfe27e165d681b15ab3f9f25c83ea59cd`  
		Last Modified: Tue, 29 Sep 2026 18:05:35 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:6e7399f3b54361e616edbf9a8f26761d2122a0b2ecf241cfd38383b52faafb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81adcbb42fa778cd5deedfaa70198cf905c88f94c0479ec885803790d8fdd6d`

```dockerfile
```

-	Layers:
	-	`sha256:0697e6b2f770c5d32b1cc37c7728b6828868a47b74733a58cdbc1acda4f023d7`  
		Last Modified: Tue, 29 Sep 2026 18:05:35 GMT  
		Size: 5.4 MB (5436963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d8707a7f857837b66f9ed1b77921262d1cdc4e60142e388bdbd446506ab35f`  
		Last Modified: Tue, 29 Sep 2026 18:05:35 GMT  
		Size: 23.7 KB (23691 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:b5d6fe146ba35d9afc4bbe09086e4a8ef1d278d4075b83a989efb35e36fdfef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295502869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff6f868d2b6c6bd4441a8afd9024bfa020f240bbc25f94d8374fdce1be664f6`
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
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:37:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:37:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:37:46 GMT
USER gradle
# Tue, 29 Sep 2026 18:37:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:37:48 GMT
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
	-	`sha256:59ae58d6da087dc0c404fbbbb9e4a4515107e04c2af0dbe1069eefcc20c5e216`  
		Last Modified: Tue, 29 Sep 2026 18:38:34 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d32d0a3b03b2bbbcd0815b8ee545d5c971eea60e5cfed62e38f9a46d532395`  
		Last Modified: Tue, 29 Sep 2026 18:38:30 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:97a1268513f048400e2b63a3a92f2b1cef50c33b53c6a574451b4742a55a0378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3468ff75f92a33297c280d0d4c3dda414f60823ef81c3d458e06a27def0e08b7`

```dockerfile
```

-	Layers:
	-	`sha256:c41482cf7018b778c19e1229bd4e22827e6c4789801cec2593d18a00a233ae86`  
		Last Modified: Tue, 29 Sep 2026 18:38:30 GMT  
		Size: 5.4 MB (5434813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796d5adb1d5233a71479e97a37926d7bd61cf1da2e5cae37c354577eeadd2578`  
		Last Modified: Tue, 29 Sep 2026 18:38:30 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
