## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:63616d83f2591683443f9784d55a167a3d0ed8b916271bc388f5bd18c51f4f82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:254943d2ecee2183b7a31b30c8559f395e2c2efc329e55078dd76c48e1d5b3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 MB (388128989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db12fb8fabda03381c6e419e0dafc0b381b88ad3f37ebc2b068c0e7dbd1fe22`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:11:08 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:11:08 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:11:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 28 Sep 2026 21:12:24 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:12:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:12:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:12:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:12:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:12:24 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:12:24 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 28 Sep 2026 21:12:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 28 Sep 2026 21:12:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:27 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 28 Sep 2026 21:12:27 GMT
USER root
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc8cd43d570dce234a0f21ec799a55fafbb9ace038e2e55ece45223379ea981`  
		Last Modified: Mon, 28 Sep 2026 20:11:27 GMT  
		Size: 118.1 MB (118094099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9bc40377359ecfcb2543b1c3ed0a0088b9f7a3feebb5b48fe428ca42624692`  
		Last Modified: Mon, 28 Sep 2026 21:12:53 GMT  
		Size: 86.9 MB (86879060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314975eade500f5c9857b2ad3358dbf4c2955935aa968e117704a62b9d277065`  
		Last Modified: Mon, 28 Sep 2026 21:12:50 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496f068cd734378caa08628d3c1f8dedf689988feb6db34352dff662e216973`  
		Last Modified: Mon, 28 Sep 2026 21:12:54 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9ad565ce0f4177d4df111ffe54b6ac5b540b33885e8ff5b638ac32bc4d0758`  
		Last Modified: Mon, 28 Sep 2026 21:12:50 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:cd3345f8d9393dc7d263662e189c94e2cf626b85432881c544d3b008872840c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11664586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e83ddf96a77d97b26a5a086f891acba040659236b898e6a7490c1120484ffd`

```dockerfile
```

-	Layers:
	-	`sha256:3b804d124fe1107f89fa44406e481454f814b72e0e601cbe26bc4a1080d9bc97`  
		Last Modified: Mon, 28 Sep 2026 21:12:51 GMT  
		Size: 11.6 MB (11643722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53240a41f7e5c87bed7ac6ba4d8d961bc20436182011a9f697728bd3208322c5`  
		Last Modified: Mon, 28 Sep 2026 21:12:50 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d85275012d78110623a4cb7a89bb195568cb6f98ac506ee312f1878567cb5865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386237012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeeeb4837242709e268a4b4179c2555f8604540c81afef59e4554d10eb48661`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:11:01 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:11:01 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:11:01 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 28 Sep 2026 21:12:36 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:12:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:12:36 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:12:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:12:36 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:12:36 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:12:36 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 28 Sep 2026 21:12:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 28 Sep 2026 21:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:39 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 28 Sep 2026 21:12:39 GMT
USER root
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529fb78f2c2c1ab9f5505c5e791591f1c150085aee877d1ce423618c3414f01f`  
		Last Modified: Mon, 28 Sep 2026 20:11:21 GMT  
		Size: 118.0 MB (117973351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e87637f7b3c36acd6364ab28f9bd3c25c5db85b71d206d37c8636445c8188`  
		Last Modified: Mon, 28 Sep 2026 21:13:10 GMT  
		Size: 86.2 MB (86235271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662767d0384c585b01fdcff98acd510f33798e4f088cd1a2163b2c8b5fa60bbe`  
		Last Modified: Mon, 28 Sep 2026 21:13:06 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8317ebfab434b057f5a08e84c281e8ed626099c528c6547f06cd310cbc070c32`  
		Last Modified: Mon, 28 Sep 2026 21:13:11 GMT  
		Size: 128.5 MB (128469404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f03f755170aa6c8dde1630a57d00580a2857b59598a0837dfee17a86d9d63`  
		Last Modified: Mon, 28 Sep 2026 21:13:07 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9b5c318b96c6663c0beea4b0d74b1ea09b039a0bed4b06b6cded40815903fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11665062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e183b727ad7f73ea5dac98ce411503eb910c401a522e2d1ff01765b9f7c552`

```dockerfile
```

-	Layers:
	-	`sha256:1109dab4bda07dabacd922cec2e044ff3d4c59174da0befff7d25eb6673c9dc5`  
		Last Modified: Mon, 28 Sep 2026 21:13:07 GMT  
		Size: 11.6 MB (11644025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7dc55c087547b994588017c0d6db0954ed8a08ca7256bb9b3cc4b304ed50e50`  
		Last Modified: Mon, 28 Sep 2026 21:13:06 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
