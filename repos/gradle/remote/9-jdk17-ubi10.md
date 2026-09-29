## `gradle:9-jdk17-ubi10`

```console
$ docker pull gradle@sha256:e16ba903331e1062f2d90f3d933297935ddb8cdb59abfbd2c73d24a11748da98
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

### `gradle:9-jdk17-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:b06c718eeb38f71461aba6e44fc2219ec99d14a37787f74a2fc610c213810dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 MB (410264428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d12392c95b34c7bc14c702da2b989f72c8bbaa1e1d035ec28f14f302c51ef7`
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
# Tue, 29 Sep 2026 17:53:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:53:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:53:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:03 GMT
ENV JAVA_VERSION=jdk-17.0.20.1+1
# Tue, 29 Sep 2026 17:53:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='457b57af8f9c93ec39080bb8c764f559dc8c89a6da1a39d718a400b7890d3e41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        ppc64le)          ESUM='7e3abe98a131e1e914d0cf50f3435f92c1723e4583377edb5cf8e63c8d125ca8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        s390x)          ESUM='f3710814283eea156d1397dc399957789d022b899a791f18bc6805b55b82207f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        x86_64)          ESUM='3808d1d15e3ec6bd5b84057fb5d84c33d8a1536a258146bcea2e603fc726e08e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:10 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:06:54 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:06:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:06:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:06:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:06:54 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:06:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:06:59 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:06:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:07:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:07:02 GMT
USER gradle
# Tue, 29 Sep 2026 18:07:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:07:02 GMT
USER root
```

-	Layers:
	-	`sha256:a34145e205c19dadb74ed940321031a946571a492b3cf835b60f57003df2bdee`  
		Last Modified: Mon, 28 Sep 2026 02:11:46 GMT  
		Size: 34.9 MB (34929005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f593884ecb80eb0d9f8e427fbae9d37998b537b3607fa366ce9c04f517633ab2`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 37.9 MB (37851810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bfb06dc3687e04a062982fafea73323cb7faa621d2a1bbb72f6474ec812ef5`  
		Last Modified: Tue, 29 Sep 2026 17:53:29 GMT  
		Size: 145.8 MB (145832730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68961f258abd33cb1ace9ae003bb0a24bdfb15a8a089cccc696a8449f10d14bb`  
		Last Modified: Tue, 29 Sep 2026 17:53:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a425427bcac6b69852a8e3fd009784220bb42cf7555026b73fe40f11d7bdbd6b`  
		Last Modified: Tue, 29 Sep 2026 17:53:25 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae24623f8ddd759f64f9b8a6ff468670b402aa3e1957b3a7728e93487bfa12d`  
		Last Modified: Tue, 29 Sep 2026 18:07:18 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9433c8811fd2590eda9d5c304bfd1d7c88107561f468a32dc640365d6333db1c`  
		Last Modified: Tue, 29 Sep 2026 18:07:20 GMT  
		Size: 40.1 MB (40096791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720e2cf8b3624336f6d11e203106b4f5be16abe8297671ab40d4814cdb4617c`  
		Last Modified: Tue, 29 Sep 2026 18:07:22 GMT  
		Size: 151.5 MB (151524265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e5cad4f08e116e37fb1534725ae21be3d8ef5510def28b2717492faef5701`  
		Last Modified: Tue, 29 Sep 2026 18:07:19 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:ac988306d0e23c47663155f0de84aef989f192d2740fa859ad153492ccac36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7118116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586b81f577052fe677c5591e35f3eb17ead1b2f05bb4a2ff2667eb501117fda2`

```dockerfile
```

-	Layers:
	-	`sha256:d3db6d45bfe944489490e5009a8c8453f8aefb151edbb1f413b988c1f6d93ecc`  
		Last Modified: Tue, 29 Sep 2026 18:07:19 GMT  
		Size: 7.1 MB (7093658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79abb9cc16dec051c191563d291419d914bded854797dfe54beba3db25b64db9`  
		Last Modified: Tue, 29 Sep 2026 18:07:18 GMT  
		Size: 24.5 KB (24458 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:00eaab217abb7216ba9b17ec958a2a9ab3a831183d7ecfe14ff6e4701ecf6574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406677096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d437a1e3205b245b765d59698e23deb4a7707a143abe4cdc450e85bfd705c0`
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
# Tue, 29 Sep 2026 17:52:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:35 GMT
ENV JAVA_VERSION=jdk-17.0.20.1+1
# Tue, 29 Sep 2026 17:52:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='457b57af8f9c93ec39080bb8c764f559dc8c89a6da1a39d718a400b7890d3e41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        ppc64le)          ESUM='7e3abe98a131e1e914d0cf50f3435f92c1723e4583377edb5cf8e63c8d125ca8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        s390x)          ESUM='f3710814283eea156d1397dc399957789d022b899a791f18bc6805b55b82207f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        x86_64)          ESUM='3808d1d15e3ec6bd5b84057fb5d84c33d8a1536a258146bcea2e603fc726e08e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:43 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:04:27 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:04:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:04:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:04:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:04:27 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:04:32 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:04:32 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:04:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:04:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:04:36 GMT
USER gradle
# Tue, 29 Sep 2026 18:04:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:04:36 GMT
USER root
```

-	Layers:
	-	`sha256:842ae2bcf67a61456b432d1f1a94bcb7d69f0613459a34bb97404ab26399ad66`  
		Last Modified: Mon, 28 Sep 2026 02:12:22 GMT  
		Size: 33.1 MB (33124832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b803dbdb351ce5081a6e996f2b915357caefe46046b85fa3eb97f2dc3cf5f6a`  
		Last Modified: Tue, 29 Sep 2026 17:53:02 GMT  
		Size: 37.8 MB (37792245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857b548947eaa5934085b316243487811106534c7a1c65a8e242d680b037e51`  
		Last Modified: Tue, 29 Sep 2026 17:53:04 GMT  
		Size: 144.7 MB (144652023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab11f503373f00a478977b1efce790341e87cef5d3fa0708de82f4af07084b4`  
		Last Modified: Tue, 29 Sep 2026 17:53:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba721dabbd4428a17d07c9add5a0d366ab6f3bdd1de20d8af7c76e4316326f`  
		Last Modified: Tue, 29 Sep 2026 17:53:00 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da0bea7bab4c2d52b559b41b50df0708ee63320266f8831203ac0f99a4b0bc8`  
		Last Modified: Tue, 29 Sep 2026 18:04:55 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a42873f443eb091b9db2681144abe86844b8274e37d6e72fe2f1bb655369be`  
		Last Modified: Tue, 29 Sep 2026 18:04:57 GMT  
		Size: 39.6 MB (39550158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04714d3e02d43ab339adad2de27cd211163445faccad50a50527c7b8622193e`  
		Last Modified: Tue, 29 Sep 2026 18:05:00 GMT  
		Size: 151.5 MB (151524291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bafbc48611d23714e53f7e3e4ddc8a67863abc24e4c3d28924bb3b9aaee3de`  
		Last Modified: Tue, 29 Sep 2026 18:04:55 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:6cf1d541d1ac19bc61e17f8622b10d6af84b3497bb652ae8f44450b24119db37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7116570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e16707a3d2c828350f052270a6aa51f50513e50a153cecc055ddccf151cb099`

```dockerfile
```

-	Layers:
	-	`sha256:28d0c67770b5f6c3b532c2a065502638b3b48f6b5e0969add91778f29daa6fbf`  
		Last Modified: Tue, 29 Sep 2026 18:04:56 GMT  
		Size: 7.1 MB (7091914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d15acbdbe7206b18a349e870b46f756c2af3d6ca1081f3bc1d90f8599fbdc8`  
		Last Modified: Tue, 29 Sep 2026 18:04:55 GMT  
		Size: 24.7 KB (24656 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:6c3fa26d0f435795bcdcb54f8ef2bd15ce208d9eb9f8506d80fd3592e0c9b169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.8 MB (417806742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3386773f2328d17ddf1cab4508e4519c28d350de7ae1efcdfcaa2345b35f86a`
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
ENV JAVA_VERSION=jdk-17.0.20.1+1
# Tue, 29 Sep 2026 17:56:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='457b57af8f9c93ec39080bb8c764f559dc8c89a6da1a39d718a400b7890d3e41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        ppc64le)          ESUM='7e3abe98a131e1e914d0cf50f3435f92c1723e4583377edb5cf8e63c8d125ca8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        s390x)          ESUM='f3710814283eea156d1397dc399957789d022b899a791f18bc6805b55b82207f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        x86_64)          ESUM='3808d1d15e3ec6bd5b84057fb5d84c33d8a1536a258146bcea2e603fc726e08e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:56:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:56:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:56:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:56:36 GMT
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
	-	`sha256:869c2426a34dac9af44481336945ab2a560ef9817565e34bc71e3f7d2128897b`  
		Last Modified: Mon, 28 Sep 2026 06:28:56 GMT  
		Size: 39.1 MB (39116127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f01e13405a632fb5996f569fa1fef3486a6651e3352462ab69afd5239becfb`  
		Last Modified: Tue, 29 Sep 2026 17:52:01 GMT  
		Size: 39.6 MB (39616201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec3024a70c8a892622d41dbb481a4500881effa459c4ba9cd266be82fdee01`  
		Last Modified: Tue, 29 Sep 2026 17:57:25 GMT  
		Size: 145.7 MB (145687512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7846d1c25d283f706e8b04628a49db0784677b3e95774405ddc4cd5443514df4`  
		Last Modified: Tue, 29 Sep 2026 17:57:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5ca5863e873df5c9720e1b367272c15384f107fc03b7efd5dbeeaf86f19432`  
		Last Modified: Tue, 29 Sep 2026 17:57:21 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c69b736d505cad981325e292f52966abf1ed99fdc389ce67919f0af9a72b8d4`  
		Last Modified: Tue, 29 Sep 2026 18:29:33 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf791a66890220eead7181ec35b8c0beaef039cf45797ffc0b1240643f39ce2`  
		Last Modified: Tue, 29 Sep 2026 18:29:35 GMT  
		Size: 41.9 MB (41858047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd357834063ef9cf73de6207c6bb88221dc431de9c0b771e90f5349350cf37f`  
		Last Modified: Tue, 29 Sep 2026 18:29:37 GMT  
		Size: 151.5 MB (151524265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d488b3bfbf9ead58cb293570d3efcb2eed159b49297c32d86af677b794f34e01`  
		Last Modified: Tue, 29 Sep 2026 18:29:33 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:e891ac8b84282770aef17274b4b257e7fecbc57b17fd85c48ba00f9fcfcde11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7109607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09345ccc26bb89bf0addac46390162715b8123adc816417f203ceef3db0af165`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc9beb014c1f0ba4d5653774c451e08670b4a48e7c31979d6c63731952fbd3`  
		Last Modified: Tue, 29 Sep 2026 18:29:33 GMT  
		Size: 7.1 MB (7085076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c19dfe7a8920ba754a24c1442ea0b8ac0406101606ead9cad530bf3f901303`  
		Last Modified: Tue, 29 Sep 2026 18:29:33 GMT  
		Size: 24.5 KB (24531 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:d36a543871ccd34a935e0516102976a17259f169701244e043e824e7d7bb9c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402706950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78dbcb52d03680bfda0d3b2896a2282b3f4cc9428e80d06774799492811b2a5`
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
ENV JAVA_VERSION=jdk-17.0.20.1+1
# Tue, 29 Sep 2026 17:51:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='457b57af8f9c93ec39080bb8c764f559dc8c89a6da1a39d718a400b7890d3e41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        ppc64le)          ESUM='7e3abe98a131e1e914d0cf50f3435f92c1723e4583377edb5cf8e63c8d125ca8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        s390x)          ESUM='f3710814283eea156d1397dc399957789d022b899a791f18bc6805b55b82207f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        x86_64)          ESUM='3808d1d15e3ec6bd5b84057fb5d84c33d8a1536a258146bcea2e603fc726e08e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.20.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:51:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:51:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:51:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:51:22 GMT
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
# Tue, 29 Sep 2026 17:59:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 17:59:21 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 17:59:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 17:59:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 17:59:26 GMT
USER gradle
# Tue, 29 Sep 2026 17:59:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 17:59:27 GMT
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
	-	`sha256:6efb1f027b9e55fc30aac437d63b01fe6a24c2c5ccbbd483ee7d870122bfe02e`  
		Last Modified: Tue, 29 Sep 2026 17:51:50 GMT  
		Size: 135.9 MB (135878815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd19f0ed64dfdbef563671afa1133121483d197da1ce8bd1716c30543cf9ccb`  
		Last Modified: Tue, 29 Sep 2026 17:51:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e28810379b16945dd37296b52d2dd0e8b63ab22e48c6224bfe36846e3e7224`  
		Last Modified: Tue, 29 Sep 2026 17:51:48 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbafabc2abd4a9be689ed854525ab9c707111a65efd976c637477d1d84e1af8`  
		Last Modified: Tue, 29 Sep 2026 18:00:17 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e469afe736726d8c3870beda87053774206f978b55330db980bdaeebe8ee4b`  
		Last Modified: Tue, 29 Sep 2026 18:00:19 GMT  
		Size: 42.2 MB (42229217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfff153e1b8ad5dd6b1ecd15af6f3bb5f36c6e5cc9b0799c50b529397fd651e5`  
		Last Modified: Tue, 29 Sep 2026 18:00:22 GMT  
		Size: 151.5 MB (151524268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddca45ac846aaeba045a2e4f4cf8bc8c9a72e518955afff4eb867a4de2215505`  
		Last Modified: Tue, 29 Sep 2026 18:00:17 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:77bd8056128fb376465f9adef4020ebf1d1505a5ff32d95cdc4d5a556cada932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7098762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac6638c5ebd75c930ca4d691a8afc2f88adcdfdae391e932a9a696a2b2725c0`

```dockerfile
```

-	Layers:
	-	`sha256:ae84203adf594ce052719df7b17fb5bb0b751aa5041b4c278baea74f3787b000`  
		Last Modified: Tue, 29 Sep 2026 18:00:16 GMT  
		Size: 7.1 MB (7074305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b584ee6ffc990c8242abe72304566a8e1d7ecf65db54016cd3a8b826d5b7e22b`  
		Last Modified: Tue, 29 Sep 2026 18:00:15 GMT  
		Size: 24.5 KB (24457 bytes)  
		MIME: application/vnd.in-toto+json
