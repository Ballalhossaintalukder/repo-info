## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:96a61986ad7c75b7674be4dd15b48a43678778ba4dbc662df37dec59cf7c8e80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:1c7cb566cbcebd64079a67295809acaa2f70a73d898b20848f49598a21ed0889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.5 MB (463509519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c227ca94806c6e5505fdc85d5490f32338c7077f9342e4837eb6979078c9b28`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:23 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:23 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:23 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:23 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 28 Sep 2026 21:11:23 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:24 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:24 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 21:11:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 21:11:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:26 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:27 GMT
USER root
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276e101fcea16b2382c692d72d82fd032ba00e7d50c18a8e8b683e36787f10a`  
		Last Modified: Mon, 28 Sep 2026 20:14:45 GMT  
		Size: 170.4 MB (170443738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f9e9715d29ebca325e4f235d07598c7115e296610cd18e109e2ab1e66a0a7a`  
		Last Modified: Mon, 28 Sep 2026 21:11:57 GMT  
		Size: 86.9 MB (86884405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8f8c7ec352c7d2185e371b049695bc8783272c396b68a5071ffbbc94067c26`  
		Last Modified: Mon, 28 Sep 2026 21:11:53 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a05c6df5254c24676661a70483da0b5a45ccdb5c2ee1e15ae214d88a78171`  
		Last Modified: Mon, 28 Sep 2026 21:11:58 GMT  
		Size: 151.5 MB (151524260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea270fc64f671d6aff0c872512aa6a11b376ea377f291bded2936c574c08e852`  
		Last Modified: Mon, 28 Sep 2026 21:11:54 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ef3ec71eb5918221deefb255f7037d49e33632e9cf6fc75759d23d703eb73d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11412992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72605c2771aad95a3e00985d8631874b087c6b5a3a6d00f929e166a6730cc9eb`

```dockerfile
```

-	Layers:
	-	`sha256:21a5ee25f69a3421ad642557b3ef59e62602322e6c0e3cc72552800394dc98bd`  
		Last Modified: Mon, 28 Sep 2026 21:11:54 GMT  
		Size: 11.4 MB (11391341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5720c093df01edf740e184dbd58d1e819511b8a38df43292fd898eb2e42cad38`  
		Last Modified: Mon, 28 Sep 2026 21:11:53 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:34eca4ed14dc6dba87c54ada2e81b9e8f62f3579a3615d313e74760afea23c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.0 MB (460023579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329223b09041fa20ed945e4f53a50ffa1968e54ba6be4411e540288d40d20278`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:14 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:14 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:14 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:14 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 28 Sep 2026 21:11:20 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 21:11:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 21:11:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 21:11:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 21:11:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 21:11:20 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 21:11:20 GMT
ENV GRADLE_VERSION=9.8.0
# Mon, 28 Sep 2026 21:11:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
# Mon, 28 Sep 2026 21:11:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 21:11:23 GMT
USER gradle
# Mon, 28 Sep 2026 21:11:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafd5ce9cfaea0fbccfdc8439a1ac42fbd4cd9c89dc9a988228d8a2639a58e6c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 28 Sep 2026 21:11:24 GMT
USER root
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f43cd5000810c2bac413d5deb5c95086aaeb30eab21e01ae69fdc61ebfbfd1`  
		Last Modified: Mon, 28 Sep 2026 20:14:38 GMT  
		Size: 168.7 MB (168715995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8065e2651a7712fa2e4a0b4d1f0e2f0e2020935508395a4183eb0121af849b`  
		Last Modified: Mon, 28 Sep 2026 21:11:56 GMT  
		Size: 86.3 MB (86254498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cc2f129195a0748c0b744f049e5f2329b015421d416a536bdbb027c688d2e2`  
		Last Modified: Mon, 28 Sep 2026 21:11:52 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5f611cec5fb0a72ecc4d0fda82794cc4943fa0977e6ebfd0d13ce1888349d`  
		Last Modified: Mon, 28 Sep 2026 21:11:58 GMT  
		Size: 151.5 MB (151524286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e6e5c4ec9aa8638d39be613192a449001a52eeaf1f4cfc40d98941fe8d927`  
		Last Modified: Mon, 28 Sep 2026 21:11:53 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:57dac1235f5448d351aaceb6cc62fb1206d2ec1d58c3f6fee90deabeb511ffa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11412192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd261cdda5b9025fae453897d1519c65eb5c0354018d360ac5a6dfa1abca5cb`

```dockerfile
```

-	Layers:
	-	`sha256:016e97ac16db09bc5e245d4f24be26734c8a33004b9ca8c3e36df454296b0d10`  
		Last Modified: Mon, 28 Sep 2026 21:11:53 GMT  
		Size: 11.4 MB (11390344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c0361df4b012e6d8510dc836ee975058a7a21dac046b7b5d08c675a005b132`  
		Last Modified: Mon, 28 Sep 2026 21:11:52 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
