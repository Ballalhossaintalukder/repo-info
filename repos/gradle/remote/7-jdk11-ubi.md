## `gradle:7-jdk11-ubi`

```console
$ docker pull gradle@sha256:9e6172723d405ed714905eb1af8e8d1276ccee39acf660e07651f5f544d0a46a
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

### `gradle:7-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:f7301d8d6158c673fa7788b661a5fd962eb54702410942c0ef9ff032f246f1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377104005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529237f33dae1251266a29ec383223f2a42183f7e4ddb35982dec05351576414`
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
# Tue, 29 Sep 2026 17:52:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:53 GMT
ENV JAVA_VERSION=jdk-11.0.32.1+1
# Tue, 29 Sep 2026 17:52:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f27033e6f7523c1b0b2565a78e9c0e0abe5596a854ce00ca04ec1b06ece7a935';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        ppc64le)          ESUM='bb84dc99346d66d5acd3610c4289b5d7c944559efe0d7a0004f9921866b16c97';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        s390x)          ESUM='4f51e08f4b0faa3c114c76ee4999bec81457713362b3c7208469e8c08cfbf89d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        x86_64)          ESUM='5c3f68887c325d36d852ba534303e1f5f1f5cae7d6cc1e951d73e0d8e98a058d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:01 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:07:57 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:07:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:07:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:07:57 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:07:57 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:08:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:08:02 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:08:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:08:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:08:04 GMT
USER gradle
# Tue, 29 Sep 2026 18:08:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:08:04 GMT
USER root
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990cbc8af404be434ff7a140c1bc500269586d1ae64860bb2bf02aed2c5cf9f5`  
		Last Modified: Tue, 29 Sep 2026 17:53:15 GMT  
		Size: 27.6 MB (27640001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc84dc98938e276749d57fadc6d3f02fea288420c9d260217c5eea8f502fc10`  
		Last Modified: Tue, 29 Sep 2026 17:53:18 GMT  
		Size: 142.3 MB (142324162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8746f82fbf8b932950363702489dadc3b5fbfccf74da7261384976a77e7788aa`  
		Last Modified: Tue, 29 Sep 2026 17:53:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3577270a28b5800b3c530ccb5766cc52bcd54df53ed1d86ef79ff741ff82e13a`  
		Last Modified: Tue, 29 Sep 2026 17:53:15 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c616dc126bbd994d7a02e7132b516ebc666450115ab18784f9a9fb4e8591143`  
		Last Modified: Tue, 29 Sep 2026 18:08:19 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3f11e2a43b79b675fdd66ace909e2e30fe6215858f6b725011c98e9d8dc1a6`  
		Last Modified: Tue, 29 Sep 2026 18:08:20 GMT  
		Size: 37.9 MB (37873233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025ecc850c63ef3af87f1e02fcbe3c85c5553570e4074b6fbf9062179896c73c`  
		Last Modified: Tue, 29 Sep 2026 18:08:22 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ad932a20c99014e4662df8fafae10e516223a6f66ef780c1fee9ec7fc9a813`  
		Last Modified: Tue, 29 Sep 2026 18:08:19 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:cc36c1fd77d19f01b806840853852b708514affe41d0f21918a541acaf207dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8d883c69325562311c0dccf8de9322eb34b09e5dda10537de803bbdcb199bd`

```dockerfile
```

-	Layers:
	-	`sha256:0c64d37ad312dd47f1ac2784e2df9ea1c8449891e7131a09b3d0a716346238d7`  
		Last Modified: Tue, 29 Sep 2026 18:08:19 GMT  
		Size: 5.3 MB (5337186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed8c964f0131825e4d1fc04e1f8118719af18d32595ac15c51b216942561f0b`  
		Last Modified: Tue, 29 Sep 2026 18:08:18 GMT  
		Size: 23.6 KB (23587 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9d5e4762b976d75911147887add8e1b9f9f4eb53f79f9dad8f9390236fa01319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371626228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6c4c8c7373488c14acb78e0e9db81a23fa84dc4157714bd4b919cc7caa33d6`
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
# Tue, 29 Sep 2026 17:52:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:29 GMT
ENV JAVA_VERSION=jdk-11.0.32.1+1
# Tue, 29 Sep 2026 17:52:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f27033e6f7523c1b0b2565a78e9c0e0abe5596a854ce00ca04ec1b06ece7a935';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        ppc64le)          ESUM='bb84dc99346d66d5acd3610c4289b5d7c944559efe0d7a0004f9921866b16c97';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        s390x)          ESUM='4f51e08f4b0faa3c114c76ee4999bec81457713362b3c7208469e8c08cfbf89d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        x86_64)          ESUM='5c3f68887c325d36d852ba534303e1f5f1f5cae7d6cc1e951d73e0d8e98a058d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:37 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:05:13 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:05:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:05:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:05:13 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:05:13 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:05:19 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:05:19 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:05:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:05:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:05:21 GMT
USER gradle
# Tue, 29 Sep 2026 18:05:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:05:22 GMT
USER root
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8705d0eeff6d80dc071fef4381a16995bad5b6f283b03b0d2b2011d9ad50fcaf`  
		Last Modified: Tue, 29 Sep 2026 17:52:54 GMT  
		Size: 28.1 MB (28079106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250aced88a47970b26c2fcee28b9ecfc99ec3ddfe721a1ab9d8e710ec60d374e`  
		Last Modified: Tue, 29 Sep 2026 17:52:56 GMT  
		Size: 139.0 MB (139035248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540c1bd160f49faf053d109855dba1a95177111878781dadcc0f3cb91614850`  
		Last Modified: Tue, 29 Sep 2026 17:52:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572e63d85c66af805f8cdda9fa660bfb9ab61e80df4fddd829c2b65c2bcf508`  
		Last Modified: Tue, 29 Sep 2026 17:52:28 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189a1d3003c4f5b51cf5d8e01661113d3880fa5679128e6d2a95597ad45a5f6f`  
		Last Modified: Tue, 29 Sep 2026 18:05:37 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694c436de0f56face7b711bb802f681c2071c6362207160ac6e7d4931ab219ed`  
		Last Modified: Tue, 29 Sep 2026 18:05:39 GMT  
		Size: 37.2 MB (37165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc65686d34600e44f96f655626ae2972e3a6f3397971dd72be335429f05e18f`  
		Last Modified: Tue, 29 Sep 2026 18:05:41 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3b1e0840e6d0a3cd10af197a7159a5897f05ff312c491f5440f772b1b00aa7`  
		Last Modified: Tue, 29 Sep 2026 18:05:37 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:41284dab5915d21dc39c08b658353ac0fbcaa304170974f39c28939f29131d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5359184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db44df5180bf2b909d0940e474d817d0e1ac85ee3732d14e67e8ba80cec171e5`

```dockerfile
```

-	Layers:
	-	`sha256:fb1d138286f8e9f0704510112802225fc6bb4b0a101267693e675419fbb089fd`  
		Last Modified: Tue, 29 Sep 2026 18:05:37 GMT  
		Size: 5.3 MB (5335424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5baa8c3a7f905b90d6c88faab5da65b0c6102fbccbbae52321dd427638ad5f78`  
		Last Modified: Tue, 29 Sep 2026 18:05:37 GMT  
		Size: 23.8 KB (23760 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:9816dd43ab71defc68823b3b8d48c81621fca35b53f3fcd0bfdb426b1eb2ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.4 MB (372431398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2ec4cbf04346c10ed33325e866621646319b8500ff29111708d99d8ad6c8b5`
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
ENV JAVA_VERSION=jdk-11.0.32.1+1
# Tue, 29 Sep 2026 17:53:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f27033e6f7523c1b0b2565a78e9c0e0abe5596a854ce00ca04ec1b06ece7a935';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        ppc64le)          ESUM='bb84dc99346d66d5acd3610c4289b5d7c944559efe0d7a0004f9921866b16c97';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        s390x)          ESUM='4f51e08f4b0faa3c114c76ee4999bec81457713362b3c7208469e8c08cfbf89d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        x86_64)          ESUM='5c3f68887c325d36d852ba534303e1f5f1f5cae7d6cc1e951d73e0d8e98a058d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:39 GMT
CMD ["jshell"]
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
# Tue, 29 Sep 2026 18:35:50 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:35:50 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:35:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:35:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:35:58 GMT
USER gradle
# Tue, 29 Sep 2026 18:36:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:36:00 GMT
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
	-	`sha256:b736683ed4ee3021b78d50a7fa660c550fb3c9761278d7905b981e9a791cd5e2`  
		Last Modified: Tue, 29 Sep 2026 17:54:34 GMT  
		Size: 129.6 MB (129596380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cddf9fe66b32b7d91c1f0d1f5e5b1700c55c0ce69da9e67763cb028a070c3c1`  
		Last Modified: Tue, 29 Sep 2026 17:54:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e568c90f09b7ca80e03e0ed10710201966c0b85cba2476dcf5318a6f58e8845`  
		Last Modified: Tue, 29 Sep 2026 17:54:31 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680d742ff146bb3150610df872ab23c289243637d994bccc9369514cfaecdbfd`  
		Last Modified: Tue, 29 Sep 2026 18:34:41 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713efa407b28a70682267a3f4a13e4b8f469c00430c528aab52fb86c86cee2a`  
		Last Modified: Tue, 29 Sep 2026 18:36:50 GMT  
		Size: 39.1 MB (39140114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5cb4fb44315abf2cdaa40571b1dd1ce366fad6af732fd45507ed1c340daaa4`  
		Last Modified: Tue, 29 Sep 2026 18:36:52 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0b9e6c6aaa6708bdb44e603302f8f794d24841352888cc538fa08080eb01c6`  
		Last Modified: Tue, 29 Sep 2026 18:36:48 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:2eded112bf3bd0ff11be0302bf7597802d8f61a7d04c475b7decb179f572fe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac76da8d21561c86ead437c307e6336b285b9900596c1c166ac6e9ddb3ee49f`

```dockerfile
```

-	Layers:
	-	`sha256:571cfcee832b2a000cd2b7bcdab5772d58d91e39c96775683054889039f8bec3`  
		Last Modified: Tue, 29 Sep 2026 18:36:48 GMT  
		Size: 5.3 MB (5332146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bcfa299e2648858ad9304d86fe7bb59b399ef1a79ec5c1e69c9206e4fa1916`  
		Last Modified: Tue, 29 Sep 2026 18:36:48 GMT  
		Size: 23.6 KB (23649 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:54fda96b3f78af0a20bb86d5621e15997c79d8885fc367cb9ca9e20e4c14197d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355439493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5042a9522e3ce670fdc0677b38dfeda167ac3a504a3ce325b160c9a2dccd4d`
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
ENV JAVA_VERSION=jdk-11.0.32.1+1
# Tue, 29 Sep 2026 17:50:43 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f27033e6f7523c1b0b2565a78e9c0e0abe5596a854ce00ca04ec1b06ece7a935';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        ppc64le)          ESUM='bb84dc99346d66d5acd3610c4289b5d7c944559efe0d7a0004f9921866b16c97';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        s390x)          ESUM='4f51e08f4b0faa3c114c76ee4999bec81457713362b3c7208469e8c08cfbf89d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        x86_64)          ESUM='5c3f68887c325d36d852ba534303e1f5f1f5cae7d6cc1e951d73e0d8e98a058d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.32.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.32.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:50:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:50:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:50:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:50:45 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:03:05 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:03:06 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:03:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:03:25 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 29 Sep 2026 18:03:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 29 Sep 2026 18:03:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:03:30 GMT
USER gradle
# Tue, 29 Sep 2026 18:03:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 29 Sep 2026 18:03:33 GMT
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
	-	`sha256:1dfa6d3fe52b4d0859e36b42a970fe47b3221cc359b98497ce5ba7cb8d5e9635`  
		Last Modified: Tue, 29 Sep 2026 17:51:09 GMT  
		Size: 123.0 MB (123048179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299b8ea8f1d44e33e0b8e1b71fcdff61c9b59638f7d3bf102fa68941ded00859`  
		Last Modified: Tue, 29 Sep 2026 17:51:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ad66dd96032efb26bb9aa5c87f4b17efbfb0f2fee544f06ece431e9c0dd3a`  
		Last Modified: Tue, 29 Sep 2026 17:51:04 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922328fb13e639ffe6b3720cd0df5a11dc3d8519f7184d1207ced4bb808a99b`  
		Last Modified: Tue, 29 Sep 2026 18:05:06 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647823044dacbebf192723964b6d3b86077d5cf4e578a3452173cdf6ec765a2`  
		Last Modified: Tue, 29 Sep 2026 18:05:16 GMT  
		Size: 37.5 MB (37476952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e182cd7178ab7f1eb3d13bb5b0318c660a5cb0d6e486d2565d3ce123254597`  
		Last Modified: Tue, 29 Sep 2026 18:05:20 GMT  
		Size: 128.5 MB (128469424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d494187cdc39bb577bb810cdc169ebb46423f793c2a1ccbfc95071fa0c9c2d`  
		Last Modified: Tue, 29 Sep 2026 18:05:10 GMT  
		Size: 35.0 KB (35017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:29cd77f4f4a08e65bbdf89e81aa65bb5bcc3a748d52fcbf0e4b3409aec4bed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095f6b2edb50bb020bfbd0b4cdc59b02857d6356744512d5ec77a958c2d7ebd2`

```dockerfile
```

-	Layers:
	-	`sha256:9153d9575b9b4525ebb596a193ffc8e80c5ac5ca956a451244058d0e71dfa343`  
		Last Modified: Tue, 29 Sep 2026 18:05:14 GMT  
		Size: 5.3 MB (5322009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8c4ee326ce02aa213b2eafb20c41fcf3615331267d8a736bea0d4e57023722`  
		Last Modified: Tue, 29 Sep 2026 18:05:13 GMT  
		Size: 23.6 KB (23587 bytes)  
		MIME: application/vnd.in-toto+json
