## `gradle:9-jdk21-ubi10`

```console
$ docker pull gradle@sha256:5c2f8bd1b28419f6fd49f0c30ae3d761692932184ff8aea26e20da3afed6488b
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

### `gradle:9-jdk21-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:08e602a22f163b0db0eca81a233eaa30f4a1f4c8d17c8701a7ff8aea0aa86775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422553011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743a164025a334e8e82d8845dae7963de439db33c952599d5bd51299f816c945`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Tue, 29 Sep 2026 17:53:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:53:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:31 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:53:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:38 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:06:38 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:06:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:06:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:06:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:06:38 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:06:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:06:43 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:06:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:06:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:06:46 GMT
USER gradle
# Tue, 29 Sep 2026 18:06:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:06:47 GMT
USER root
```

-	Layers:
	-	`sha256:a34145e205c19dadb74ed940321031a946571a492b3cf835b60f57003df2bdee`  
		Last Modified: Mon, 28 Sep 2026 02:11:46 GMT  
		Size: 34.9 MB (34929005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed89f00e0f0f2af2500d702c4f1270592c12c2b354de9e81bb0c4bc7a06b382`  
		Last Modified: Tue, 29 Sep 2026 17:53:58 GMT  
		Size: 37.9 MB (37852308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd77e1872cee3dff3af3b374c9cbb9c647dc17bd7cf240f55dcd1974cf76fd3`  
		Last Modified: Tue, 29 Sep 2026 17:54:00 GMT  
		Size: 158.1 MB (158120081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c75f096c3b373098c045aff569dfc242ce0f978feffc2a94936056f69705ce`  
		Last Modified: Tue, 29 Sep 2026 17:53:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9eda10f7bfe62a7a9bb0bdfe4dda464317f3ba7cfd92d7acddc984f0f04ac6`  
		Last Modified: Tue, 29 Sep 2026 17:53:43 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13c1e25856512b7166a5558afdf823ddea394c10a96eb718ad90b68501b7f5`  
		Last Modified: Tue, 29 Sep 2026 18:07:07 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b4aad713e98934a1d11875dcd1b1e22b40de8bc74a942e5dc120d0649ead18`  
		Last Modified: Tue, 29 Sep 2026 18:07:09 GMT  
		Size: 40.1 MB (40097524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ef4cd77d99beb4df09ea25f6cd1b4c2037ea0a1f1b936d533488b223fe975`  
		Last Modified: Tue, 29 Sep 2026 18:07:11 GMT  
		Size: 151.5 MB (151524265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e12eed8a9762e3b93f1229e8065d6ccc2b724d415a386b75584a5ed45261b33`  
		Last Modified: Tue, 29 Sep 2026 18:07:08 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:582e757ac6a2aea18374ac314feef95c6e68cc93818dd1b0adb3f5d9e5ab9963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edd59141ebe7b3270fc9a96145b52134d89eded6f2d95c30f6b30d7a4c1640d`

```dockerfile
```

-	Layers:
	-	`sha256:8e08c72b55f5069248df9a265735dbc9673600abdaf391d373775e981743506b`  
		Last Modified: Tue, 29 Sep 2026 18:07:07 GMT  
		Size: 7.1 MB (7095510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4974f379d5aef5567dfbf3e35badfce91d6fa7c454cc8143e031a8569f21df`  
		Last Modified: Tue, 29 Sep 2026 18:07:07 GMT  
		Size: 24.5 KB (24459 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7acbd9e30542ed19c96d15a2879e2c97491396db1ccc62768ba9daa47c7bfe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418428551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a3c837b602077241145ff4b5b5e44d0ddaa6b0d83e3258fe22add032c5e17`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Tue, 29 Sep 2026 17:52:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:38 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:46 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:04:09 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:04:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:04:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:04:09 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:04:09 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:04:13 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:04:13 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:04:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:04:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:04:18 GMT
USER gradle
# Tue, 29 Sep 2026 18:04:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:04:18 GMT
USER root
```

-	Layers:
	-	`sha256:842ae2bcf67a61456b432d1f1a94bcb7d69f0613459a34bb97404ab26399ad66`  
		Last Modified: Mon, 28 Sep 2026 02:12:22 GMT  
		Size: 33.1 MB (33124832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c47233bd9892826d6fe723af34e05f66b4c7876f8042959a68bb62fd0f74ec`  
		Last Modified: Tue, 29 Sep 2026 17:53:06 GMT  
		Size: 37.8 MB (37792242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122d9cc288cc435a7ab0145b14c8c658827782ec1107c241d7348667c69ffd78`  
		Last Modified: Tue, 29 Sep 2026 17:53:08 GMT  
		Size: 156.4 MB (156403444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5198afafd9dbcd6b07739d21bd08a7fa0bfc49c58a2ae3731331cc81f9ec67`  
		Last Modified: Tue, 29 Sep 2026 17:53:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d306c7c7a6658a8258a717856c77f80ad6774bf3d1c8c5bc9dc785602ca6cba5`  
		Last Modified: Tue, 29 Sep 2026 17:52:53 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd339ff2bb74abf0971cb6c2834b7791839dfa212f234cc79a795c93c8fba83`  
		Last Modified: Tue, 29 Sep 2026 18:04:37 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac837e02d5b2557e0b6e0753076aff6ceac128aaa4deb84738e9dccf8ea6670`  
		Last Modified: Tue, 29 Sep 2026 18:04:40 GMT  
		Size: 39.6 MB (39550218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed611d1debdb029dd4b9e7ae6c701f0a3f7974ea487e27193b69c359a2f5f9cc`  
		Last Modified: Tue, 29 Sep 2026 18:04:41 GMT  
		Size: 151.5 MB (151524264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897b9f312dcb8ee2b61402b4799294b4e881e6e741d5c84ca2d8ae7bfc6865a`  
		Last Modified: Tue, 29 Sep 2026 18:04:38 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:68e6501994e6cbbc992778eb335ac122f16642573506901bf8991e1dde2f089a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7118422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9617dd24411bd2056be2bfd6f86562028591e264872dad0ca1fa9ae040fc3437`

```dockerfile
```

-	Layers:
	-	`sha256:f698fb6f8d60172d84e458c1b6e4ec8c6726f580615f5ea1d673439ada9b7a29`  
		Last Modified: Tue, 29 Sep 2026 18:04:38 GMT  
		Size: 7.1 MB (7093766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8217b81b27d6bd23b5e797c522177919bcbefc4c62187b08047fc22947f25aad`  
		Last Modified: Tue, 29 Sep 2026 18:04:37 GMT  
		Size: 24.7 KB (24656 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:deabae1f96e19eb657970cc38a5432e4891bb351d67bdac1a501b55e3fc62cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.4 MB (430403649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6029cb675b849d6e2c99d701e6f4c9b5ff8d09cfe587774d8b092dbbd8b66ee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Tue, 29 Sep 2026 18:26:01 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:26:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:26:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:26:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:26:02 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:26:22 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:26:22 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:26:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:26:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:26:28 GMT
USER gradle
# Tue, 29 Sep 2026 18:26:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:26:30 GMT
USER root
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
	-	`sha256:dc1702e7c67177bb4282cbd459b3bfd35c2181fb0a1046dcf1e2d999912d6786`  
		Last Modified: Tue, 29 Sep 2026 18:00:01 GMT  
		Size: 158.3 MB (158284463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1691c5367ac7b9e7e35e5bc9b3f8afc3147fa2870c1fd4060898713869aa52e`  
		Last Modified: Tue, 29 Sep 2026 17:59:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa904bae841e032c5a73335d28b3031b26dd1127e727b866acc1609d1e9c1e`  
		Last Modified: Tue, 29 Sep 2026 17:59:55 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336dbd358de7f1499cfda2f78327e1bd32153264bbe1681f79d8e39e8a3adfd6`  
		Last Modified: Tue, 29 Sep 2026 18:27:28 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ced09232910d045786375837dce26536b64c11db959b7d06b5ea65b5198bff`  
		Last Modified: Tue, 29 Sep 2026 18:27:32 GMT  
		Size: 41.9 MB (41857993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436d6cad8c7b624f9d3cfc3f9ff7ab4243b4971db7467a74fc0d187c440125d9`  
		Last Modified: Tue, 29 Sep 2026 18:27:35 GMT  
		Size: 151.5 MB (151524265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14e8dbd41ebb8ab3f7a4cf0d4cf9b2cc20567c064db3be7b53902eb0d38c786`  
		Last Modified: Tue, 29 Sep 2026 18:27:30 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:362afc497bfe2d13b1a062c0054a47828a18125afe4898fad41838e8c68de288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7111459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69761a73ea845cc1b357c50adc22b139b144c06a3858426c3849ee4c5d563f37`

```dockerfile
```

-	Layers:
	-	`sha256:61326e09beefb53985352066ec838825d10c05bb76bc74f9551261fdc57a4f40`  
		Last Modified: Tue, 29 Sep 2026 18:27:30 GMT  
		Size: 7.1 MB (7086928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90fad5cc40d78f863b9ef0294ab42636f7798738883fc6ff1d3a1af6cdb9955`  
		Last Modified: Tue, 29 Sep 2026 18:27:30 GMT  
		Size: 24.5 KB (24531 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:a087037d1415dec46119bfcd63ca9f081d2b164bb313e75addc2249ce162cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414176300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c93033148cb7090ab5ae500218e780d6ae7d44fb4ccd10db9ab203f7146c37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Tue, 29 Sep 2026 17:50:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:50:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:50:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:50:33 GMT
ENV JAVA_VERSION=jdk-21.0.12.1+1
# Tue, 29 Sep 2026 17:52:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='23e37e026f12f3e706f18938ff611db3032d075b09d0879a25d06718c773e223';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        ppc64le)          ESUM='042482fa372f12741ceb721397e277b4e69672182aaa45a1bf7af55d9ba876d6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        s390x)          ESUM='806bb29b0d408eb6312cda0a1e756bc91e554ef9ed6a5863f6004e502f6c789a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        x86_64)          ESUM='ce79869e1307ed8ee1e2baa86a412b1eb5b75d10a01006d788a6f968bcfaee94';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.12.1%2B1/OpenJDK21U-jdk_x64_linux_hotspot_21.0.12.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:14 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 17:59:18 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 17:59:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 17:59:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 17:59:18 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 17:59:18 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 17:59:23 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 17:59:23 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 17:59:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 17:59:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 17:59:27 GMT
USER gradle
# Tue, 29 Sep 2026 17:59:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 17:59:28 GMT
USER root
```

-	Layers:
	-	`sha256:3e51340b5abee43447a0b1bfecbe6d76485a0883aea31b7aec7aa8f604d00e2f`  
		Last Modified: Mon, 28 Sep 2026 06:28:51 GMT  
		Size: 34.8 MB (34837868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df02050e6e06b5d4f43278dd18365dc4c753f3c4104825a5076ca38c7553985`  
		Last Modified: Tue, 29 Sep 2026 17:51:03 GMT  
		Size: 38.2 MB (38232190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1956e064fe11b2049863e31b1d99d8722ae2497d9a151f9a7d9a6ab4ed346527`  
		Last Modified: Tue, 29 Sep 2026 17:52:42 GMT  
		Size: 147.3 MB (147348022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ae2081cf705ae2368cb87a4cdb15b8f278be236347c8818b1a18921174236`  
		Last Modified: Tue, 29 Sep 2026 17:52:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad420a1c471a8c2b7681ee02bc044645c1d7a691f7ae6123b2bbf049e81ceb09`  
		Last Modified: Tue, 29 Sep 2026 17:52:40 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e509f4699e20c27477e405db71d8aa7b377db74963c3700d703593651695ef4a`  
		Last Modified: Tue, 29 Sep 2026 18:00:22 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257ee4431570ea3ac49c7e912217c78986200d082e51ef22b98646e5458bd9e`  
		Last Modified: Tue, 29 Sep 2026 18:00:26 GMT  
		Size: 42.2 MB (42229338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37b28d19ef1d4c65425e4e22c6246df124428cbeddbf225bb0fc1c41b763ea9`  
		Last Modified: Tue, 29 Sep 2026 18:00:29 GMT  
		Size: 151.5 MB (151524289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fdcd7ebbfa5ddd18eb4a1a46348bc567d68658f081462b53fca9b1fe1b5729`  
		Last Modified: Tue, 29 Sep 2026 18:00:22 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:fdac89f5e5f3c7198397429cee3945f46029e8fff10244ea9a17e805751fd3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7100614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c147486fa4d701a0f85706b2df6b47fa8e5aaf64e4beb7b59512d2bbbba26f9`

```dockerfile
```

-	Layers:
	-	`sha256:44a7d6766f355ec25a07a759817e9873c547228bd0f0e9b85aba231596b468f4`  
		Last Modified: Tue, 29 Sep 2026 18:00:23 GMT  
		Size: 7.1 MB (7076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd67f3eb47a7b7bb5c1a827b3915946def2c1abb10ce51e90cbf7eaefa8cb41`  
		Last Modified: Tue, 29 Sep 2026 18:00:22 GMT  
		Size: 24.5 KB (24457 bytes)  
		MIME: application/vnd.in-toto+json
