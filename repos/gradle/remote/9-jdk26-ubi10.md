## `gradle:9-jdk26-ubi10`

```console
$ docker pull gradle@sha256:0ddc0467e178c97f53b889eac9a9ff442564c0bdf5b69e2721991c93d4f5c4ac
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

### `gradle:9-jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:28d3698741dc4731ee7e241a3429b29f833d94ce58b4e8998975bb1b142b4be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358996323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5037c6d957df4a02464dcbb9c3d8cadd464f0b4226fc4e2a33368e5f113ce12b`
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
ENV JAVA_VERSION=jdk-26.0.2.1+1
# Tue, 29 Sep 2026 17:53:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9f6ad9856a7dd880061adaf88db3c4da0642113d59b7960a892f0e551c0c948c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        ppc64le)          ESUM='34e0030c9b972b93cd11c3fb77211ae64c6a7d9c2ba10665730ee9f56ab29722';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        s390x)          ESUM='165602f7c4c3daeb8a71fa0dc1d1437f4707b702b8c3d3876d399e11241db34a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        x86_64)          ESUM='451c12e68747bcfa2fb5a2c16b00483fedb9fa6d77bc962d30957f76ac17044d';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_x64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:42 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:07:21 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:07:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:07:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:07:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:07:21 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:07:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:07:26 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:07:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:07:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:07:29 GMT
USER gradle
# Tue, 29 Sep 2026 18:07:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:07:30 GMT
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
	-	`sha256:d77eba74c07ce11ca83f260756414e03c2153aac85e39406fed5ddf7e1bc32cb`  
		Last Modified: Tue, 29 Sep 2026 17:53:59 GMT  
		Size: 94.6 MB (94563849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e3ec254c6c12b2937e2f05d9251215138773d7a6d3d75b286999c2d1bb44`  
		Last Modified: Tue, 29 Sep 2026 17:53:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041c03370231eafef05e58fde468f6f24b0c4b11b2c0965172759e33b1745c21`  
		Last Modified: Tue, 29 Sep 2026 17:53:53 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918dd433bb3a332997d8c44becd6b0abee8a34d70cb740f98daad6c14ddab438`  
		Last Modified: Tue, 29 Sep 2026 18:07:49 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfb34ab655a6ce17a9ea07f25e3f8413278ccdd140df992a7627f5b04636b9d`  
		Last Modified: Tue, 29 Sep 2026 18:07:50 GMT  
		Size: 40.1 MB (40097543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c19e2a80165b20d5908e58b753796c598f3b18943ad5ccbfcde52795250c53`  
		Last Modified: Tue, 29 Sep 2026 18:07:53 GMT  
		Size: 151.5 MB (151524268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ef0c4ef51860a1332c5ee11da239bda642604c58488e393ce7ebc9f38c0365`  
		Last Modified: Tue, 29 Sep 2026 18:07:49 GMT  
		Size: 25.6 KB (25630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:802ea9b28fdbed7b5afdd4f8500333e23190b0521650c340a75c8e10e672e2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7082980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd17cd5309d86f58ebc7d77dd35b606f79e00148d40231728b5b2c8549225fc5`

```dockerfile
```

-	Layers:
	-	`sha256:9e35947ceabad8fa17f8840bf41a4d5f6d575b4f6e2edd609b024e845d69341f`  
		Last Modified: Tue, 29 Sep 2026 18:07:49 GMT  
		Size: 7.1 MB (7058551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2691e5a3037ea4760fceb10982f1ad62d55bffe449f6f3c5735c3be8b6a094f5`  
		Last Modified: Tue, 29 Sep 2026 18:07:49 GMT  
		Size: 24.4 KB (24429 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c1d9c3e8ed115490201f7bfd073bed4c4e94ab8afc64a4214a3e778b032669a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355568616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b548343101b14e3b1ab6525f0458467c950cfcfda33f10de5ebf822a27efa0`
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
# Tue, 29 Sep 2026 17:52:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Sep 2026 17:52:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:52:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Sep 2026 17:52:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:52:05 GMT
ENV JAVA_VERSION=jdk-26.0.2.1+1
# Tue, 29 Sep 2026 17:53:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9f6ad9856a7dd880061adaf88db3c4da0642113d59b7960a892f0e551c0c948c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        ppc64le)          ESUM='34e0030c9b972b93cd11c3fb77211ae64c6a7d9c2ba10665730ee9f56ab29722';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        s390x)          ESUM='165602f7c4c3daeb8a71fa0dc1d1437f4707b702b8c3d3876d399e11241db34a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        x86_64)          ESUM='451c12e68747bcfa2fb5a2c16b00483fedb9fa6d77bc962d30957f76ac17044d';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_x64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:10 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:04:29 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:04:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:04:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:04:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:04:29 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:04:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:04:34 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:04:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:04:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:04:37 GMT
USER gradle
# Tue, 29 Sep 2026 18:04:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:04:38 GMT
USER root
```

-	Layers:
	-	`sha256:842ae2bcf67a61456b432d1f1a94bcb7d69f0613459a34bb97404ab26399ad66`  
		Last Modified: Mon, 28 Sep 2026 02:12:22 GMT  
		Size: 33.1 MB (33124832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b0f77c11a069000fc53eeb8b974b095092b45d1cf0fd5eea17acbf74207e0d`  
		Last Modified: Tue, 29 Sep 2026 17:52:23 GMT  
		Size: 37.8 MB (37792269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb6aae5ab8c684c8a1d19a617f2a94ffbe3186cc91a4a87c474d66d5ff10b4`  
		Last Modified: Tue, 29 Sep 2026 17:53:30 GMT  
		Size: 93.5 MB (93543500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68961f258abd33cb1ace9ae003bb0a24bdfb15a8a089cccc696a8449f10d14bb`  
		Last Modified: Tue, 29 Sep 2026 17:53:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2416d44a225693434bc1e1382143f79e2d02f474260e2d07e1a2cc479bb15a`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a025c1457bc9515be960bd46ecd4643d32452d7f6ac69c9c4e660cb4ea6f062`  
		Last Modified: Tue, 29 Sep 2026 18:04:58 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7acd60c3d2a56bb839a8ea5583b0863e12670e64b6db52a3d1ccbb780947bb`  
		Last Modified: Tue, 29 Sep 2026 18:04:59 GMT  
		Size: 39.6 MB (39550192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892eb99596da468fd29bdad366ea6aa08299119d90c0acb408da3ce97345ffc3`  
		Last Modified: Tue, 29 Sep 2026 18:05:02 GMT  
		Size: 151.5 MB (151524266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6679c58d4b1cedfef738ccccd2fde66085b64510453bbaa92f6944b653060866`  
		Last Modified: Tue, 29 Sep 2026 18:04:58 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:15d1a6426f0056df8b5927934a764a7c0cebf8cca19085281eb9bbd97f37785a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae154aa2c9d9129a6e5cc78fc5b63cf5a51e2623f75764e35347958b527a1106`

```dockerfile
```

-	Layers:
	-	`sha256:2a53f8caf04015af10a0ae79327b937c88df2eb2b8149bb3807e3d426a284386`  
		Last Modified: Tue, 29 Sep 2026 18:04:59 GMT  
		Size: 7.1 MB (7056804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9784f869b8d6713f89293f7459e95c097fedd9e7824f012ff46fdd5a4a5005`  
		Last Modified: Tue, 29 Sep 2026 18:04:58 GMT  
		Size: 24.6 KB (24626 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:ad582d7eeaccfee3979e739e645fd27760d64acdf93fee6fd50f7239641a9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365469716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bb17e8aae11dc8a6eb1bc2db8cc5e371eae38e2d67d921c7b013cf29d5796`
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
ENV JAVA_VERSION=jdk-26.0.2.1+1
# Tue, 29 Sep 2026 18:03:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9f6ad9856a7dd880061adaf88db3c4da0642113d59b7960a892f0e551c0c948c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        ppc64le)          ESUM='34e0030c9b972b93cd11c3fb77211ae64c6a7d9c2ba10665730ee9f56ab29722';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        s390x)          ESUM='165602f7c4c3daeb8a71fa0dc1d1437f4707b702b8c3d3876d399e11241db34a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        x86_64)          ESUM='451c12e68747bcfa2fb5a2c16b00483fedb9fa6d77bc962d30957f76ac17044d';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_x64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 18:04:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 18:04:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:04:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 18:04:03 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:30:00 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:30:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:30:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:30:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:30:01 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:30:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:30:27 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:30:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:30:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:30:34 GMT
USER gradle
# Tue, 29 Sep 2026 18:30:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:30:37 GMT
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
	-	`sha256:5472560d44587d679e16ec6f75627448066049d299cdc453c8e0160bd3172ce5`  
		Last Modified: Tue, 29 Sep 2026 18:05:00 GMT  
		Size: 93.4 MB (93350483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1867e360b48c9d8d120a6b1df8bd6c7e66d5fe81da0392211b926cf8dbf30e`  
		Last Modified: Tue, 29 Sep 2026 18:04:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5553cb8814a15775b67b7563bbde21d81443c929beb6ab2285b4e1001cce12`  
		Last Modified: Tue, 29 Sep 2026 18:04:57 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360b24633bf355698647ca764eb066b886ca52cd2a3f4ae9930d34fb47aaffbb`  
		Last Modified: Tue, 29 Sep 2026 18:31:30 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd0c6e0b955756c6c96157f7d2c3b1be6a655b66a9a2cf88bc3aa9cd481fc03`  
		Last Modified: Tue, 29 Sep 2026 18:31:32 GMT  
		Size: 41.9 MB (41858036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a34d86d7b37956e705432b06a518f0368c05b6ec233951820dc1811e031aa72`  
		Last Modified: Tue, 29 Sep 2026 18:31:35 GMT  
		Size: 151.5 MB (151524267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b39b1423bad806a0da9dfba2c7778a1bdb7456a01ac2db552e1923f86b54df`  
		Last Modified: Tue, 29 Sep 2026 18:31:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:17e8e5bc2b4baae97bacfc9e813369b3f5cb11fcd9b0c376b9e293421fd0a9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7058406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189afa37bb0695aeee620cecbd538ea712a232ff711e9496516f85301e1d53f7`

```dockerfile
```

-	Layers:
	-	`sha256:94598914219b4ca8169ea7ebfafab27117d6172297bb181f0a4b4d14e78f74bc`  
		Last Modified: Tue, 29 Sep 2026 18:31:30 GMT  
		Size: 7.0 MB (7033905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6551933f1bfe77a77b4fabee1f2d8b2513aa8143763fca22b75ddf70a63c0733`  
		Last Modified: Tue, 29 Sep 2026 18:31:30 GMT  
		Size: 24.5 KB (24501 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:da5cec386495e04301a6648851933d30551be9aeefcb9bd33b099356defae75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357419224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca2a304ebf960745530c65fb1368f36e9ae52d333d5e9468267d274b89a931`
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
ENV JAVA_VERSION=jdk-26.0.2.1+1
# Tue, 29 Sep 2026 17:53:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9f6ad9856a7dd880061adaf88db3c4da0642113d59b7960a892f0e551c0c948c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        ppc64le)          ESUM='34e0030c9b972b93cd11c3fb77211ae64c6a7d9c2ba10665730ee9f56ab29722';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        s390x)          ESUM='165602f7c4c3daeb8a71fa0dc1d1437f4707b702b8c3d3876d399e11241db34a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        x86_64)          ESUM='451c12e68747bcfa2fb5a2c16b00483fedb9fa6d77bc962d30957f76ac17044d';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.2.1%2B1/OpenJDK26U-jdk_x64_linux_hotspot_26.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 29 Sep 2026 17:53:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Sep 2026 17:53:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:53:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Sep 2026 17:53:08 GMT
CMD ["jshell"]
# Tue, 29 Sep 2026 18:01:03 GMT
CMD ["gradle"]
# Tue, 29 Sep 2026 18:01:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 29 Sep 2026 18:01:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 29 Sep 2026 18:01:04 GMT
WORKDIR /home/gradle
# Tue, 29 Sep 2026 18:01:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 29 Sep 2026 18:01:17 GMT
ENV GRADLE_VERSION=9.8.0
# Tue, 29 Sep 2026 18:01:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Tue, 29 Sep 2026 18:01:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 29 Sep 2026 18:01:22 GMT
USER gradle
# Tue, 29 Sep 2026 18:01:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 29 Sep 2026 18:01:22 GMT
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
	-	`sha256:176f149bb33a6807196d4a79e2eeac96dd4e43f4c3ca7fca5c0b250ef832eb58`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 90.6 MB (90590741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37e1b359774fac7faade347940d3d5e919a226fe2db86bb2a36b61ffb7079`  
		Last Modified: Tue, 29 Sep 2026 17:53:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d712ba52bd7d76137b3ef09ad754a91ab1c2a7376b17ff51570c9e7f58b75c0`  
		Last Modified: Tue, 29 Sep 2026 17:53:32 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a4e9f37b5b088e73ac7b631672c2a63c8e2de8ce60c843a5ecf3fc46e2c6d2`  
		Last Modified: Tue, 29 Sep 2026 18:02:01 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ee865487c80a4d2015edc6c0675cfad737a7170e919732c25887d493226c8`  
		Last Modified: Tue, 29 Sep 2026 18:02:03 GMT  
		Size: 42.2 MB (42229569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235bc833341f9a4f872db3706e784b0eb242a3ff95c8e2917491221f2241d184`  
		Last Modified: Tue, 29 Sep 2026 18:02:05 GMT  
		Size: 151.5 MB (151524267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db71d1ebc6038575cbb306258f56c466a9245588601a2248b6e5bf9320bf73b`  
		Last Modified: Tue, 29 Sep 2026 18:02:01 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:7f5800869bea4dab54cbacaf20ad683136230cc2efa822d298173c04b09e6a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7048811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efda7d79c8d79c4b141c4f4c022512f17da1712bd6cedec6142ec1541c74c7d`

```dockerfile
```

-	Layers:
	-	`sha256:f161879a7c7564db6469225c8e109b4276d2b68940369a23e62ce0c7382dad51`  
		Last Modified: Tue, 29 Sep 2026 18:02:01 GMT  
		Size: 7.0 MB (7024384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b43ece34ca87603b23147f2cfd3f3f30829bc8c8f0a8381fc6805a9443f709`  
		Last Modified: Tue, 29 Sep 2026 18:02:01 GMT  
		Size: 24.4 KB (24427 bytes)  
		MIME: application/vnd.in-toto+json
