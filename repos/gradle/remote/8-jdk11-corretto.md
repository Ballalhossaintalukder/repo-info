## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:e32a7d8ca3de147c112ca03bd5175460534c72bc44268b8e2bd99bccebb5c9cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:38582b98ce58125988652c284516b9ac5885e52d478cd0c263fe19b165e001bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.1 MB (433130726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3b4a4a3c1a7411168489054188d95d4dc08a41ca8dbc755d8be4f8ec592c1`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:35 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:35 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 28 Sep 2026 21:11:53 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:53 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:53 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:53 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 21:11:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 21:11:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:55 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:56 GMT
USER root
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6aa6ac938182a2e6679350ef0a0252a2c30730743f67b9352d63516654bfc4`  
		Last Modified: Mon, 28 Sep 2026 20:13:55 GMT  
		Size: 153.5 MB (153487184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491117fa94cb477ba15b554b8f2ba9ea368ea3442c2a18ed7f8b9cb32c1ff953`  
		Last Modified: Mon, 28 Sep 2026 21:12:26 GMT  
		Size: 86.9 MB (86888605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1fe3daa65b82c9e727f2de50af3a51148e3a9684274d88d27510595cc0bb6`  
		Last Modified: Mon, 28 Sep 2026 21:12:22 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b9dff1322c8deb9c515fca521cc71d066b68f6807325be38a67337ceeb1640`  
		Last Modified: Mon, 28 Sep 2026 21:12:27 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7d35ab00fd5a78065c27eb051fbd2fbd38b39317a8a342cc10f065407941b9`  
		Last Modified: Mon, 28 Sep 2026 21:12:22 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:54729f0bae60184c8a03a4f2dd09add252e2de6c15518a7238f12a2971df6057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72c663e6cec28ea7a2e334b1452e3921c3178d4a827cb2c91313b30c8789aa4`

```dockerfile
```

-	Layers:
	-	`sha256:d741750e7b64093cbdb02df98d2835cba37c96b1ae1c8776a0de3f93d8dd9c1f`  
		Last Modified: Mon, 28 Sep 2026 21:12:23 GMT  
		Size: 11.4 MB (11381979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b8c1d02ccf62209474ce79fbb1f085c50f22a90a4715d25a74aa12e656fd13`  
		Last Modified: Mon, 28 Sep 2026 21:12:22 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ef45750a3803fde5f6d7a3b8e162056013d691b593fe066de5c2928e910184c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429940615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61af75335e1d621ebdc7d3e9bb0919e195b9c1fe074be44f76dccd8446a4026`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:23 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:23 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:23 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 28 Sep 2026 21:11:48 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:49 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:49 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:49 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 28 Sep 2026 21:11:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 28 Sep 2026 21:11:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:51 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:52 GMT
USER root
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf43adb086c58caa9ace08d3db7dae5ffbadd3b50bd5f6998c6106f0e1032b75`  
		Last Modified: Mon, 28 Sep 2026 20:13:44 GMT  
		Size: 152.1 MB (152062610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e6cc64e51c75e8e2df785bbe1b931d6a29b462caea62bf2f1aa4d4b38906ea`  
		Last Modified: Mon, 28 Sep 2026 21:12:23 GMT  
		Size: 86.3 MB (86250472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1888ec1f76a9e56d9d0d85aa6a4ea8e421ddb14141ffe678b04b8f4fb22311`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19a3bf589e38425e552eddf30839b1b1ed6932d30ede1beb43f106eb9465d32`  
		Last Modified: Mon, 28 Sep 2026 21:12:24 GMT  
		Size: 138.1 MB (138068532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e238d4a37e4f76c216a88068662e19856811fa09ff2aef2b65a299cf23fdc2d`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e134593ae0b61c107f659dbbb579059df217258324056b65fd514385f97ee780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9901cb9b6cd40463d73d4e9ea222efd74b9b657a2afaa128d9b16be68b20da`

```dockerfile
```

-	Layers:
	-	`sha256:f8ecd50c3a9676a1187bfd0537a030d1cb9efe9051eb2dbb9def66b52bad849d`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 11.4 MB (11381822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c59a0843d7dee511ef39df839e5335e4043c31759d8614e57c04101c44fc157`  
		Last Modified: Mon, 28 Sep 2026 21:12:20 GMT  
		Size: 21.9 KB (21861 bytes)  
		MIME: application/vnd.in-toto+json
