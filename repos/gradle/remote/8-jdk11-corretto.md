## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:97d06087ba8b3431237e33299498fb58cd4ef66754db33dea98aa173cf785077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:130e224964279525fa15d9a6438f97917f5cfc49ecf675f3886ddc4bf54744c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.1 MB (433086936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb4c5e1c5bbdc502bdd52b9dc692d85346a4ca569252cf07f0bd18f6d5c7dd0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:02:56 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:02:56 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:02:56 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 28 Sep 2026 18:07:42 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:42 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:42 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:42 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 18:07:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 18:07:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:45 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:45 GMT
USER root
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3ce59e99ed4a938db66a55a48a3d31fe569bfb174bd28526ffaaaa4db8b73e`  
		Last Modified: Mon, 28 Sep 2026 18:03:17 GMT  
		Size: 153.5 MB (153486568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1840698c3ec1d28d25ce066c5647bd981740745c92f968261e9d2859fa34a4bd`  
		Last Modified: Mon, 28 Sep 2026 18:08:12 GMT  
		Size: 86.9 MB (86888954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301f7a8ccde5e95774bc08782f3ed91c99d91626634c778e2799690dd5c1b557`  
		Last Modified: Mon, 28 Sep 2026 18:08:09 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465e194ed27a88f6255fa53a5eacb43585af69c05db12d5dcfd7a535f62db438`  
		Last Modified: Mon, 28 Sep 2026 18:08:14 GMT  
		Size: 138.1 MB (138068550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c318becbd79092c95531ec0031e1e388ac5f899d06f508f7647fb9c2bbc28152`  
		Last Modified: Mon, 28 Sep 2026 18:08:09 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5857fe956e981130f2d90afa3cc92035d640406f6d45b7cde55db3b29fd5640e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bd72fb3e6f77e574c8cfe5c2314cc809a53b67d68ae68c13fde94cc76d2154`

```dockerfile
```

-	Layers:
	-	`sha256:e087092431554fc7174c57933d66745d075054abb9d6558dd739fc12d84cbd19`  
		Last Modified: Mon, 28 Sep 2026 18:08:10 GMT  
		Size: 11.4 MB (11381978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48724e884d2489a5130da6b92f6b0a546190a7554d1b1f27ee2c0367adeeb9e8`  
		Last Modified: Mon, 28 Sep 2026 18:08:09 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dcacb2eb8bd9ddd854a099ed5645fd34f3075b0f951660bfebd66ff5f94ea3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429890387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2ec5181178c3019ae362aa4f860c72227eff517b9ca37904a7e1bec8b101e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:02:56 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:02:56 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:02:56 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 28 Sep 2026 18:07:47 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:47 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:47 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:47 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 18:07:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 18:07:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:50 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:50 GMT
USER root
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a884244aa95f165bfbdc013b93fbdbfd02b538ad5b952e7167e94c574ecd6e`  
		Last Modified: Mon, 28 Sep 2026 18:03:18 GMT  
		Size: 152.1 MB (152057178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a4c01b3b59c4df736793916ed9ee8d8e103d7e759c4ce07a1c0f7125279e73`  
		Last Modified: Mon, 28 Sep 2026 18:08:21 GMT  
		Size: 86.3 MB (86250887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bc9afa8bd31a32ce2b7ec11a20fa3cf2f07642af250c728939d60e0f887b`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4ebcad4d45559e13ba4f8cc11f4bbf42a203aa3e36d09f16fe5949b566d127`  
		Last Modified: Mon, 28 Sep 2026 18:08:22 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9ee946a6f72f56a47996b60f28eed2fe3c275e5b4010c4c6cc03c09ce4fc0c`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bd2ee495db03e1f5eccbdd591be60f8edd28ed2ffdd7a7d490ac9b2d2a0b2ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa29c7eec2fdbca6bdb534684cf881ab87cff935121760ca268af8b536361d2`

```dockerfile
```

-	Layers:
	-	`sha256:88a424e9a660c903e04369bddcd933ec22580c8af98bfccf596e8049f066a4b2`  
		Last Modified: Mon, 28 Sep 2026 18:08:18 GMT  
		Size: 11.4 MB (11381821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377ff292df5c7b9b37164704832ac3ebc85ca5a695fad17a6fb2203bcf27903e`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
