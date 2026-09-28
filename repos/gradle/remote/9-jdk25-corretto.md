## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:043789e46e035bd2d946afc252a092507517679d6de937e3662531989782f5cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:4a82d1442b87536ed85edde8ea443e8026c10d82a797ab6a2ec7aa0ea0d0efc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.5 MB (482506000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a796873c5d7f703ad5ea10fea164fd9fe0a819ca929c0dd093b099f8c105acb`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:52 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 18:04:52 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:52 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:52 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 18:07:38 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:38 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:38 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:38 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 18:07:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 18:07:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:41 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:41 GMT
USER root
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a688003377dd94e1bb22328d02a22fa951f30e76699aebb7660300095395b4`  
		Last Modified: Mon, 28 Sep 2026 18:05:17 GMT  
		Size: 189.5 MB (189483982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b3866d1e33e1ed16647120cbe727d02980a87d343436a45b0ea0da99367601`  
		Last Modified: Mon, 28 Sep 2026 18:08:12 GMT  
		Size: 86.9 MB (86884189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c754a44ca35a415431b26b1a99e60042d73f746bb41f182bebc849e66e5107`  
		Last Modified: Mon, 28 Sep 2026 18:08:08 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c995511dec5c490b7cc89ab552c236372eccb2966e7bc89f3c2b8c4f4db83f5`  
		Last Modified: Mon, 28 Sep 2026 18:08:14 GMT  
		Size: 151.5 MB (151524261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb91cc99c14f2b032667184f93982f52e699e8bb37a12d18b589e726ddc31e82`  
		Last Modified: Mon, 28 Sep 2026 18:08:08 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:657c38a5bf6fe2ab30cde64d4b7a3b189ae3ab2ab2af118bc448e2494a4df8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11425788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d424375504fbfde32f808bfff87cacc55b6d6defd0b2eb3be61bd2522a7908be`

```dockerfile
```

-	Layers:
	-	`sha256:c5f803b8cf08883822bb5b74315518425f79643d349571dbf86384131f3eded5`  
		Last Modified: Mon, 28 Sep 2026 18:08:09 GMT  
		Size: 11.4 MB (11403519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c381669184a9a84fa691e794941efd38f61d567f8193795151c86095e2033d46`  
		Last Modified: Mon, 28 Sep 2026 18:08:08 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c5c254d980daaf221a75219a688a25cd325049b9067521154ed612bb957f812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478642210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc77f18270cf5a670c601c6b4019a7e4aa872c17650cded5c9f70e77b018366`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:41 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 18:04:41 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:41 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:41 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 18:07:30 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:30 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:30 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:30 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 18:07:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 18:07:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:34 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:34 GMT
USER root
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa1b8103f5363a82e55aa8e83e858545fb906962651b549a2b51b9601efde9f`  
		Last Modified: Mon, 28 Sep 2026 18:05:06 GMT  
		Size: 187.4 MB (187384302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3640603f95fe8634add8f0a2329c984f12949356b40e66caaa3bdd734acc0add`  
		Last Modified: Mon, 28 Sep 2026 18:08:05 GMT  
		Size: 86.3 MB (86250065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4c0c719f2631a59ee8ba00e5f3d91fc1a682b85b9ce246da17e6291dbe062`  
		Last Modified: Mon, 28 Sep 2026 18:08:01 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac199956167dc59407ca6702d0b9f84722cd353147b204c6ba94dd106de8483`  
		Last Modified: Mon, 28 Sep 2026 18:08:06 GMT  
		Size: 151.5 MB (151524259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e06ea40ceb373d45d11e1f5b7b6bc98c308713f3176c0cb53052cfeda00a4f`  
		Last Modified: Mon, 28 Sep 2026 18:08:01 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d6c56c58f4c930fb1d6b5bfd26572205c194fc084bb65f145724198ca8d64308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11425047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe64ddcd40199c9dbe1964f86207941fe577052f00786d9b369f29c700fab2b`

```dockerfile
```

-	Layers:
	-	`sha256:953990116c86a96fd85c3fbd39c266668c9080b651e0e15a8a05412bca18ca70`  
		Last Modified: Mon, 28 Sep 2026 18:08:02 GMT  
		Size: 11.4 MB (11402557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d9a9f54ebf8f2f1001f983f732da14626397743ee38bdf1875c68d1cd6060e`  
		Last Modified: Mon, 28 Sep 2026 18:08:01 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
