## `gradle:jdk-lts-and-current-corretto-al2023`

```console
$ docker pull gradle@sha256:2188976f887216b76b18551b5c411aa89707fde5f6f3740d79b828f51e82f2e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:33548e0708fd924b0ab435fd8c0adafb6abd53c950455b8ad70f2eaabe183100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 MB (661983158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa90382b5f5d434a3650211d87f09393f34e300b808c290720672ba8af29d2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:37 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 20:14:37 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:37 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:37 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 21:11:20 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 28 Sep 2026 21:11:40 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 21:11:40 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 28 Sep 2026 21:11:40 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 28 Sep 2026 21:11:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:41 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:41 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 21:11:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 21:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:43 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:44 GMT
USER root
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4caa8b206ad40c8a8fc8a38eb6297864961bf2ab57f9c89bd496b5ee4ec65ef`  
		Last Modified: Mon, 28 Sep 2026 20:15:02 GMT  
		Size: 189.5 MB (189489140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77ec5e57ea7c42a17b4bb27ff3f43fb12516ce722f0160bcda140fc9cd8862b`  
		Last Modified: Mon, 28 Sep 2026 21:12:21 GMT  
		Size: 179.4 MB (179421788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73639b04fc68bb1a014e357f75806aa2f765c133a00f908c79b5ecdae8ba9112`  
		Last Modified: Mon, 28 Sep 2026 21:12:18 GMT  
		Size: 86.9 MB (86890717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe057efc7cfab40aa3741a880845fb506732ce778b4c83c0a28ac8fb7db0125`  
		Last Modified: Mon, 28 Sep 2026 21:12:13 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a19147e475b565f744dbd4cec2728e72fd5b0bad6cf2309577183b9c5e0a5eb`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 151.5 MB (151524288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de118703eae0e5007fd9cd753b9b777609eaaa3af30aedc25d810fa6c6caccbb`  
		Last Modified: Mon, 28 Sep 2026 21:12:14 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:517090e240f98f789fb46f47f7f03c8deff3504c3abd70459d4a289c88622a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11597428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feda01b67ddadbc6566943ecbfac6b8d5cc751f75c3f3d2909bb88d38e0e2793`

```dockerfile
```

-	Layers:
	-	`sha256:833a1b17931fce525dfba7b1464650d86041c0060e15137435a8a316ef79a526`  
		Last Modified: Mon, 28 Sep 2026 21:12:13 GMT  
		Size: 11.6 MB (11567918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc2ec27341cb2422e616b2110d8172b137b3c9a91a98afddc616394197a8905`  
		Last Modified: Mon, 28 Sep 2026 21:12:12 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dc31d38e888a0a458023fd51c35b12aaa3762c71ecdb59ce66d3cabcf7daff73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 MB (655991337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6bafece42213af5ff7f6fb5dfbc53aeecf9a7a6312a2b2c1f3e498a702b578`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:20 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 20:14:20 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:20 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:20 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 21:11:17 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 28 Sep 2026 21:11:43 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 28 Sep 2026 21:11:43 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 28 Sep 2026 21:11:43 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 28 Sep 2026 21:11:43 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:43 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:43 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 21:11:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 21:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:46 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:46 GMT
USER root
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded607820c2b9d0a6d49edb49e811c59122c8973f18e518f733a929847ae3e3e`  
		Last Modified: Mon, 28 Sep 2026 20:14:47 GMT  
		Size: 187.4 MB (187385381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcbf7e9bc652151e25558b83bc6a8c56d9ba320a8337311b0d76349e111c78d`  
		Last Modified: Mon, 28 Sep 2026 21:12:25 GMT  
		Size: 177.3 MB (177298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361f6b458e71e77e240a52c76d42fa61c0b3f754cb9f592369c6ec4f0b75dc9`  
		Last Modified: Mon, 28 Sep 2026 21:12:23 GMT  
		Size: 86.3 MB (86254591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092793c038bfe6f58989a2648d63ce27d203b38362973ff3ed71e05044537b39`  
		Last Modified: Mon, 28 Sep 2026 21:12:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45ee2c71cf63d994ba6f175db413c666a8c1bdfce7a614c3408dee3439326`  
		Last Modified: Mon, 28 Sep 2026 21:12:25 GMT  
		Size: 151.5 MB (151524256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68a565331ea51447e4973a07d052f58e4f4fabd2480ddb40a9766106bf9c97b`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 29.3 KB (29328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a4ffd235f7c8ff24a6aae16dfddb8ac359bd4b654f2613d7a403e7eee4f3fd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11596217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e633d677d9db2db411b4fcc9b9620eacebef37def8664dfdef053606b13b7f1`

```dockerfile
```

-	Layers:
	-	`sha256:461e6f1ab826a18303377755eeeaa864a5bc55a9da3d2e69316d6ac27f49c84c`  
		Last Modified: Mon, 28 Sep 2026 21:12:19 GMT  
		Size: 11.6 MB (11566388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4706de03cc09467b73f5c2673e8af1dee1e0abe92b8a639c878922d3a9e04a`  
		Last Modified: Mon, 28 Sep 2026 21:12:18 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
