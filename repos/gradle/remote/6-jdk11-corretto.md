## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:ad5f5221383461ddd55a0882f4ba94cc3997f17c2d6dd8782f2d81924cccdc35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:edfebd139b5d062e82cffb8b906aee2d46d32c894ac5504de9e1d2cea09d2eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19793824220c37facac08ef8d3520b0336e92cf603f00cf84130c1165646f16`
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
# Mon, 28 Sep 2026 18:07:48 GMT
CMD ["gradle"]
# Mon, 28 Sep 2026 18:07:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 28 Sep 2026 18:07:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:48 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:48 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 28 Sep 2026 18:07:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 28 Sep 2026 18:07:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:50 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 28 Sep 2026 18:07:51 GMT
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
	-	`sha256:f00f2c63ffad8b7583b2b88855c6ff6c8e3f33cb9cb99824690b216f8d0c80aa`  
		Last Modified: Mon, 28 Sep 2026 18:08:20 GMT  
		Size: 86.9 MB (86888860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5234c92caa3cffa6ed1c010025aa6f61ea903501e264d244c32e5338f48ecc6c`  
		Last Modified: Mon, 28 Sep 2026 18:08:16 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0458cd5885443046db3af6e81b2e7635657569b175a023480251432e284eba1e`  
		Last Modified: Mon, 28 Sep 2026 18:08:20 GMT  
		Size: 107.7 MB (107696636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a79775a0bd8142358f5925d217feaeaa7e889fa868fbf73c0f231ba83033da`  
		Last Modified: Mon, 28 Sep 2026 18:08:16 GMT  
		Size: 431.3 KB (431274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4bc5a84d4d8eec88099541593623a8a031225a709b3a69ffb7384f5bce43683e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11294965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c68b1801b7906934d4cfda997a345853b4981e2d75c401c53c260d3a601af8e`

```dockerfile
```

-	Layers:
	-	`sha256:4b260b37aacfdc3b4ed9537e54fc99050e1512c6a44575a776c4f2d4ff51d701`  
		Last Modified: Mon, 28 Sep 2026 18:08:16 GMT  
		Size: 11.3 MB (11274093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c88214275e9850344b7b01656280818fe340fadf179db292c5f4f2497bbc8c2`  
		Last Modified: Mon, 28 Sep 2026 18:08:16 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5943342cb741714d56266d47d90954a791a2efa7759c7d41f2f53a7eb6e27f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399884034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22d4141f7ca63a636ca5fa15a743acb2ec55c316f159a3414b25a09d5e52269`
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
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 28 Sep 2026 18:07:48 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 28 Sep 2026 18:07:48 GMT
WORKDIR /home/gradle
# Mon, 28 Sep 2026 18:07:48 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 28 Sep 2026 18:07:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 28 Sep 2026 18:07:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 28 Sep 2026 18:07:50 GMT
USER gradle
# Mon, 28 Sep 2026 18:07:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
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
	-	`sha256:98fd4755ac59a8272eff3ab888981f4f6518a4413fc443273a25fdafd6f4df6a`  
		Last Modified: Mon, 28 Sep 2026 18:08:20 GMT  
		Size: 86.3 MB (86250946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5234c92caa3cffa6ed1c010025aa6f61ea903501e264d244c32e5338f48ecc6c`  
		Last Modified: Mon, 28 Sep 2026 18:08:16 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e6b511994b0fb855b59f9e9237b0f6a5709fe0b75b986c37555136bca8dd08`  
		Last Modified: Mon, 28 Sep 2026 18:08:21 GMT  
		Size: 107.7 MB (107696636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b80c8933690c455723502524f2109ebb5de49fd2bce408a91d6a2ddb1a9506`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7b7fb64065f59bc1f38ebeac7c20f6da50a65daa2757b423aa9aa364a96ab8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11294956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4e10836353fb2be151cbc7c52da1cf347be793a260ababe58822029971018b`

```dockerfile
```

-	Layers:
	-	`sha256:6f8e831228ca0c8742350ddd91e21612a4dc8c10d7234e0cccea6e797eec950c`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 11.3 MB (11273912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15cbeebce74634f4cc7de1c96f9f2123abcea8252708cfd87f0e00d0f3d686d9`  
		Last Modified: Mon, 28 Sep 2026 18:08:17 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
