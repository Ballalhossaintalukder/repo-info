## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:1a15a026421093fa86053b17b116ede95acfa28346e5cf3e154943bc01db7119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c02b9533db6aec9026c1c3c7669bf6ea64a0fb1f1bc3cddca43dbf7caeadc27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411875335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a278562d00db9a6ee2fcebd1a95ea694c704a7c13a8e0a4b8b7fe5e5b62937c4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 21:13:53 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 28 Sep 2026 21:13:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 21:13:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:13:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:13:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 21:13:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 21:13:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 21:13:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 21:13:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 21:13:53 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 21:13:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 21:13:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 21:13:53 GMT
CMD ["mvn"]
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
	-	`sha256:0a5ff59e96e8ab3b5a707f255900b9da727fa823e9b3d631984a748871ea3573`  
		Last Modified: Mon, 28 Sep 2026 21:14:11 GMT  
		Size: 158.4 MB (158395389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57c9ab8d5c73aa2d383fa8fcd6dd747c30adb5bd17790ab1460a48189338a81`  
		Last Modified: Mon, 28 Sep 2026 21:14:08 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c597d8f605ce2819840beaa63d9683103fbd4a46aa12be4f6e59ab0238d66895`  
		Last Modified: Mon, 28 Sep 2026 21:14:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0f2053075d0be517cae06ef179e88c84428af34dfce3f36506d31eaf88f5e`  
		Last Modified: Mon, 28 Sep 2026 21:14:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5181565d332acd5cb03e4fb45fc201f7dc790f91de32c81bc9f4b0564f8edcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6240701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c67223c667069f7fef9978e04ca5fb42328ab9b7798c1ec5f06d98c4db8f2ea`

```dockerfile
```

-	Layers:
	-	`sha256:1539040aee5b6771b1c2e10271796b4e3a9ddb97f5332bd2383f902c3bbcd69c`  
		Last Modified: Mon, 28 Sep 2026 21:14:08 GMT  
		Size: 6.2 MB (6223914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dcc3e60b8ca155d8159aae6a98ad96e7fb42610e9fae9328a620589585099f`  
		Last Modified: Mon, 28 Sep 2026 21:14:07 GMT  
		Size: 16.8 KB (16787 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:92babffc1a92a5bd15ddba0fed9b3b7686cc373d0d5f32753a4f9d118dcbe203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.4 MB (407361460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75313599c9dd616ed7a5ae8dfbfd442d53b6015efcc17bbc331615b374bde9ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 21:14:06 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 28 Sep 2026 21:14:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 21:14:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 21:14:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 21:14:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 21:14:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 21:14:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 21:14:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 21:14:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 21:14:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 21:14:06 GMT
CMD ["mvn"]
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
	-	`sha256:99dddc0f4d0d1a21ecce25ef1d11c9e8e0514840ce51a2ac4f0a3380e76d5927`  
		Last Modified: Mon, 28 Sep 2026 21:14:28 GMT  
		Size: 157.1 MB (157117313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad43827fca27b00a4925c23c602c96fc7815cf03ead789bcb5fdb5af0448cb91`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6d613dc9665932f33ef3326c8b8714f63e6ed106d31d931b3702f65ad8197f`  
		Last Modified: Mon, 28 Sep 2026 21:14:24 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417aacfa7d80c21f2c8f6a296417c270977242663c7aa572b5c30269b57ab124`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:71e89aa7eefe68d3cff0bafb0b7b91654c6982dac9220bb4fa6a07ed3227aa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6239947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e00d4214991803c787fe5edbddaced6acf1b7bb765bd8a275cebd67052252`

```dockerfile
```

-	Layers:
	-	`sha256:dbe5bc5bcc3297c0dd8fc10e015bf4e449c862ad5af13b123e515fbc2d4f4164`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 6.2 MB (6222943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cda871ff06f877a328a276b4e9804540a0672e56acb26bd671d3561a59d35b8`  
		Last Modified: Mon, 28 Sep 2026 21:14:24 GMT  
		Size: 17.0 KB (17004 bytes)  
		MIME: application/vnd.in-toto+json
