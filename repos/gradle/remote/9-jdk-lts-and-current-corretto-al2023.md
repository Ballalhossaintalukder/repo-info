## `gradle:9-jdk-lts-and-current-corretto-al2023`

```console
$ docker pull gradle@sha256:ed2d2ac138318b4802b9de0ee68e91571acaec66079432b1c0225daa4a7c6df1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:82f719973250d26b6fd332dd6cfdc692cc612a3b87809bdd088c06cffc723e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.9 MB (661928054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14efb65aacb9c275e83ab7ad6ad55b2862b02388d46d320fb1556746eb33c45`
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
# Mon, 28 Sep 2026 18:07:23 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 28 Sep 2026 18:07:45 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 18:07:45 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 28 Sep 2026 18:07:45 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 28 Sep 2026 18:07:45 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:45 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:45 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 18:07:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 18:07:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
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
	-	`sha256:53b92cd8322665f13503a083ecfa571a4c47cb7a7b19820cd6a36449600f7634`  
		Last Modified: Mon, 28 Sep 2026 18:08:27 GMT  
		Size: 179.4 MB (179421770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5a75b876c0f554455736c90a4301166e0c27b285399b8858ba7e8a052c630b`  
		Last Modified: Mon, 28 Sep 2026 18:08:24 GMT  
		Size: 86.9 MB (86884372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a9c60c8b9c78ae503704db08411f93e783ec7061c35ca241d865481ca234f0`  
		Last Modified: Mon, 28 Sep 2026 18:08:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16ebe971af15dd0234426b9d16f953d8b2a94ad369e06dc5b6227990dfd30d`  
		Last Modified: Mon, 28 Sep 2026 18:08:26 GMT  
		Size: 151.5 MB (151524260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc5ec5322d9eab0b73e4f7b2799a5570ba8f810144984417a2b4313b60d03a4`  
		Last Modified: Mon, 28 Sep 2026 18:08:20 GMT  
		Size: 25.6 KB (25603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d061908ac4a2e9eb62c25c1bd7d5a358957d1739dcde03cbe8590cdfa8deff6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11597427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129e008471a323b06f43c1b402181e3f78c08187a78219cbe92197bdb80ae0fe`

```dockerfile
```

-	Layers:
	-	`sha256:54acae09f83a5b37afe66e48a7c41b7ecc0cd60fe781241a4a6ec2e9d1c620ed`  
		Last Modified: Mon, 28 Sep 2026 18:08:20 GMT  
		Size: 11.6 MB (11567917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9952846da31b9556dcfffc6813fe817d1a28bd8aff59c763f3a137fb74eeeefe`  
		Last Modified: Mon, 28 Sep 2026 18:08:19 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:88183a3dc664d493f744d985773e8344efe03cec9ebf4d86f8f2f3ae9551540f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 MB (655939945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbc7cd6049be2f20d3049e4cb80a94e3cd1c344055e07c373b58d91b594cc9`
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
# Mon, 28 Sep 2026 18:07:25 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 28 Sep 2026 18:07:50 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 18:07:50 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 28 Sep 2026 18:07:50 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 28 Sep 2026 18:07:51 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:51 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:51 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 18:07:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 18:07:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:54 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 18:07:54 GMT
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
	-	`sha256:1bac0c34977dcd05c5915ced9116dd5291aaf6b9baf0373ba58bb2feceb084ff`  
		Last Modified: Mon, 28 Sep 2026 18:08:34 GMT  
		Size: 177.3 MB (177298264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dce990b6fab2da1dc06b2eab75593855817bf6653ae316220b5e15202da2a40`  
		Last Modified: Mon, 28 Sep 2026 18:08:31 GMT  
		Size: 86.2 MB (86249423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f198f6a5734a31ae03795d7c775eb4b43e26ac635c48890da7425b630c003a`  
		Last Modified: Mon, 28 Sep 2026 18:08:25 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f742b8b8d7ef4f213b62ea5c4daf1c16457f5a2a4d0efe5b699bf22dbc1d2a`  
		Last Modified: Mon, 28 Sep 2026 18:08:33 GMT  
		Size: 151.5 MB (151524265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ef6462cf3f3946ed027dea246662e9af536259f0b54a1beea6cccadf08410f`  
		Last Modified: Mon, 28 Sep 2026 18:08:27 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:59ee1a0b36a271e391cc1199d4bc992de96eac60a662278db339150b10dcd2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11596216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96d692116df52e4d50ad393414792f7f3aafb45f8ed982fc0aae1be5e865a18`

```dockerfile
```

-	Layers:
	-	`sha256:48db3a4fd276dac69a75eba24beb0bee9d6be6c652145aea47d442a65bd65393`  
		Last Modified: Mon, 28 Sep 2026 18:08:27 GMT  
		Size: 11.6 MB (11566387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514d72a00c7996a3470fda63d85e6931f646f5461745caa120cff8be78b1a5b6`  
		Last Modified: Mon, 28 Sep 2026 18:08:25 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
