## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:160c5be358149675f8acb1ba49f9abd67b1b984b88d4818e2f7729a5dcab4bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:98cc945fcd65eb991758697b46c3dd760bd6beaa8ec250475f48290ff663a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.2 MB (427189564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc119de42188d8ca725d1bd9bccd4053c679514d217b117e331806782f8e486`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:42 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:42 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:42 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:42 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 28 Sep 2026 21:12:08 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:12:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:12:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:12:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:12:09 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:12:09 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:12:09 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 28 Sep 2026 21:12:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 28 Sep 2026 21:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:11 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 28 Sep 2026 21:12:12 GMT
USER root
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e20413541bffa512131f03076ee98d97c707b46e08b4d72afe89841528e1763`  
		Last Modified: Mon, 28 Sep 2026 20:14:04 GMT  
		Size: 157.1 MB (157145930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540392e9787abae86e2c2bcc8b89bf05790621354ce15b105378e7ae538e733b`  
		Last Modified: Mon, 28 Sep 2026 21:12:43 GMT  
		Size: 86.9 MB (86887826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e390a76adad7b47c746e2f899cf8ef5eff2550d0f6b848790f6d457061e3da3c`  
		Last Modified: Mon, 28 Sep 2026 21:12:39 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397aa227a15809e1ddaf330c32132f8383bc38bc45c57ddf113c5a1f73424570`  
		Last Modified: Mon, 28 Sep 2026 21:12:44 GMT  
		Size: 128.5 MB (128469405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541d1fb35ca0e879909fbb4ca94fe88e572e816c23a981ffabe3b2d992d8f4e`  
		Last Modified: Mon, 28 Sep 2026 21:12:39 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:765f7307e2c8be68f86c58785496eff23fc83d8cc17f47ba54f57fa672d3e2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db4f4870f0050ac040cca167322279725dec0fe7a0a6483f88bd7cebcbb7e41`

```dockerfile
```

-	Layers:
	-	`sha256:76abd94683468c7802fdc6c4f6f4a93d1a3b684ce7cab13e8c6335d901defd63`  
		Last Modified: Mon, 28 Sep 2026 21:12:40 GMT  
		Size: 11.3 MB (11267299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47a80d8ca8c72e22e037ac99bd0992c0c95d3c2297d431f2e43162290323326`  
		Last Modified: Mon, 28 Sep 2026 21:12:39 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8de8532d60f76119e1a90f4aa12a72c41de2d0794ffd9e2dc64ce96eea79b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424235172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3df0bd29335d322522fdd4b28a8fcdf3720b16777981f228bdd6ace7303c634`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:27 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:27 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:27 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:27 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 28 Sep 2026 21:12:00 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:12:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:12:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:12:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:12:00 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:12:00 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:12:00 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 28 Sep 2026 21:12:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 28 Sep 2026 21:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:12:03 GMT
USER gradle
# Mon, 28 Sep 2026 21:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 28 Sep 2026 21:12:03 GMT
USER root
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf79a4629ec37c72d04a605aab54376cd8ce8387e70e9e56c187ffa77b7139`  
		Last Modified: Mon, 28 Sep 2026 20:13:49 GMT  
		Size: 156.0 MB (155952593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10823df41a0f0ed542c7ec265e5219efff99fa2049756d3196974226dddf4295`  
		Last Modified: Mon, 28 Sep 2026 21:12:35 GMT  
		Size: 86.3 MB (86254179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bd68411eda2d343423da4bf2e5733a32c55eccc18e8d6ab35d3d37f625f15`  
		Last Modified: Mon, 28 Sep 2026 21:12:31 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c0a051d919f9d72130e16bf83f1918b123431fa53c6f162645b7277fb734d`  
		Last Modified: Mon, 28 Sep 2026 21:12:36 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cfe9e327634dbcf4a76c19b01883a0189c746b6e69884d494ecdbd07972f6b`  
		Last Modified: Mon, 28 Sep 2026 21:12:31 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1a013d2e562715e690a4e2f38fbbf0d6c6a2dec222d6cb32d45fa8c046e4b35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11287161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bf6a15b13ed819573ce690d0e4918cd2411541ae29c68d216a36ea1bdbac05`

```dockerfile
```

-	Layers:
	-	`sha256:17cd81ccfee0b70e4aca70c43f8cec44299e0e3085bb2da8770aa86194b97879`  
		Last Modified: Mon, 28 Sep 2026 21:12:32 GMT  
		Size: 11.3 MB (11266275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4826434c1c82475681f98179ecf9d8ed7c87ee6aa3bd6764d1d68b5b6d7f3fe7`  
		Last Modified: Mon, 28 Sep 2026 21:12:31 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
