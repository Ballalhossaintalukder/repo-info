## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:a4a6dd6858c0e92af773a6a1265341356938bc94ce43ab9ebdea41484b1c12a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:d272a9ba7c78fe2f9df65746c0e93a8ba987272c4cc75f81b42b00dd684ad14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397728380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99d067eb3b6632941d67cb4cb4fb142d0e9d2df78d50e264cbc270a97b89ce7`
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
# Mon, 28 Sep 2026 21:11:59 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:59 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:59 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 21:11:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 21:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:02 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:12:03 GMT
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
	-	`sha256:245f639e13937a153f16407f9fc7f008e1f360d1ef4f6f5def9b8b0c41844292`  
		Last Modified: Mon, 28 Sep 2026 21:12:33 GMT  
		Size: 86.9 MB (86879332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc550f3cf56c5220eb931a08e2cdf4e933c0e391656c8ca6e6092c9eb45682`  
		Last Modified: Mon, 28 Sep 2026 21:12:30 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe33daf146899f8ec5e7ec255ed8b9f251b7fd7cf01e257f0b0e995a0b9fc06`  
		Last Modified: Mon, 28 Sep 2026 21:12:34 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0afaa484afdb721e5c15ab2a3c47422550a3f1272bf0e9426a49621aea0280a`  
		Last Modified: Mon, 28 Sep 2026 21:12:30 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6063c6c18cb9f977412eb23ad3a2506263c5f73bde4d8ea8ce5ded475deff8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11755361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19a05cb4480140df041ab7a9529c7f1a08ef5e54a0d354840bf51ce701d3aae`

```dockerfile
```

-	Layers:
	-	`sha256:f8c1d7582cc8650256fdfdd4b6a8fb452bd5fc80db032728da67435ccd6cda8c`  
		Last Modified: Mon, 28 Sep 2026 21:12:31 GMT  
		Size: 11.7 MB (11733707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362a6e122b03e721e548306365b5092cc82b1fd9a014006dc6c5507743d3b561`  
		Last Modified: Mon, 28 Sep 2026 21:12:30 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:00b19452d0933170b95cb5aa2839253d00f90cfc36dd35be68416e1aec2fd885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395836033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccd4b0baf31331d75b375acd37ed133b4e83b334904128e81df81beae5be979`
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
# Mon, 28 Sep 2026 21:11:57 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:57 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:58 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:58 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 21:11:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 21:12:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:00 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:12:01 GMT
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
	-	`sha256:b820fc94d1939771bf88e262aa6ff59a5eca347f553d48f8d81c74a8545258b0`  
		Last Modified: Mon, 28 Sep 2026 21:12:33 GMT  
		Size: 86.2 MB (86235156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ba0bece29335649838340757fd6e2a26c272391bd9f8cf3d9c5980bc50027`  
		Last Modified: Mon, 28 Sep 2026 21:12:29 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9beb2d9ee4ecd970633e8a54d149564101b699e0323a46eeb84872a4ffc803`  
		Last Modified: Mon, 28 Sep 2026 21:12:34 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8c946d560d6041689811e61a04fc6f551efaa0cb508329a1a0a214e44657ac`  
		Last Modified: Mon, 28 Sep 2026 21:12:29 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:03563d542f7d316e0653f61c670e7bada1c86a46fc356578727cb69648ba6eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11755880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69104fdbc390e3cb1546993c53a6f729bd710eb66b5d2cbead5649b7a1ae3461`

```dockerfile
```

-	Layers:
	-	`sha256:c8a01398df829516ef9ba2abef581adfd32ca88d64d85d32ec6f9185952bd26c`  
		Last Modified: Mon, 28 Sep 2026 21:12:30 GMT  
		Size: 11.7 MB (11734030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f3e55c55f63d6f3d96a0818f253d85f1e763bda5c2c0d6c5a628895bb89141`  
		Last Modified: Mon, 28 Sep 2026 21:12:29 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json
