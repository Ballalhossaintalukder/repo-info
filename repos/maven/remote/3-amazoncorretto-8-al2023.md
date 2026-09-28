## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:52fd13f93704912f90017cfa4c6a082ce649bdd56051b1b150eeef01281be6c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:64dc7a1276dd4a5fc10d2e271242ed57938c8986ef3b877118306f8bfe718760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343162338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f83a09095a4b8d743a3aa9edea9219f4db94dd2517a54cdb2ae98a311e4ed7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 21:14:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 28 Sep 2026 21:14:07 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 28 Sep 2026 21:14:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 21:14:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 21:14:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 21:14:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 21:14:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 21:14:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 21:14:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 21:14:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 21:14:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 21:14:08 GMT
CMD ["mvn"]
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
	-	`sha256:4b6bed9a326b0519853726490ce9446acb64e3cc01b2b47d5b4cf545197e10b7`  
		Last Modified: Mon, 28 Sep 2026 21:14:28 GMT  
		Size: 147.6 MB (147565307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841c79454bfabf0f3da54d7248ec3177e734a834e843d2a08beef994d4acc3d`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 13.5 MB (13512124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86efe553960d449f6c9f037f1334be54bf9c95130f148928a0ce786855b3e54`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e85f191f66379849d44d350019e7ec4d170cb2b4e32f29089e5743391130ee`  
		Last Modified: Mon, 28 Sep 2026 21:14:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e69c9608970aadc0fe326e8e4e384e43f71bf70712ad7f2e0678b4205cd6b3`  
		Last Modified: Mon, 28 Sep 2026 21:14:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:36c54afbe75be1785ce93274ad2885a7e1faf8647a66333e64fc60c2e86415fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6640588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa88ba11620e52dbb2a5cba4cfbae1998fbb5d2029b267fbab31c5defa796ad`

```dockerfile
```

-	Layers:
	-	`sha256:9d0a886e0b3a306ff325589b0bfb60e5ec784e7f4182c26ae46d648fceccf827`  
		Last Modified: Mon, 28 Sep 2026 21:14:24 GMT  
		Size: 6.6 MB (6623303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19bfd88797a6956f60d17eaa1dedecb825c1ad403f8e3973479d00ba69c5d89e`  
		Last Modified: Mon, 28 Sep 2026 21:14:24 GMT  
		Size: 17.3 KB (17285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bd3dce28d7bf8262a00f861ac3a494bfd787e94842777bfaab23199c9fb52c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340622435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eb45ff03342dfda72bbde59c295e8f3c613e5e5451565c7da80d7eb1cf3199`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 21:14:14 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 28 Sep 2026 21:14:16 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 28 Sep 2026 21:14:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 21:14:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 21:14:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 21:14:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 21:14:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 21:14:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 21:14:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 21:14:16 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 21:14:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 21:14:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 21:14:16 GMT
CMD ["mvn"]
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
	-	`sha256:15a2bc545c2c7e3cba2431fa0680f5f93eca06d7ffad2452585c00bb1fc29b42`  
		Last Modified: Mon, 28 Sep 2026 21:14:37 GMT  
		Size: 146.0 MB (146035968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ea21de291120d5aa9567964c476ca2574137843a851bca3dff04f72fa50b39`  
		Last Modified: Mon, 28 Sep 2026 21:14:34 GMT  
		Size: 13.8 MB (13754350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c9fd5cd0b628b337dc96a0a200f76dec58cfb94fef6304478c2662c6c4912`  
		Last Modified: Mon, 28 Sep 2026 21:14:34 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0024dc6f9074a1e687b87f73abfbaa7f50b773dabf2a09acb37edbcc688be4`  
		Last Modified: Mon, 28 Sep 2026 21:14:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943361ffe8746fb035f7442ecc57ee6fccf824063ef6a0c62ff44b0148ff360a`  
		Last Modified: Mon, 28 Sep 2026 21:14:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ddd8430f20b0320b18262ab9e15f5ef4d8667b2cd887a5cd595506e08da619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93afc42cd8b9977d5f114935e2f861ae637ef00c89ae91af7bb4844be7c6d26a`

```dockerfile
```

-	Layers:
	-	`sha256:5442b8d339969706bb3fa0ec76d20858217adb890fae9b72b18de283e95d49e0`  
		Last Modified: Mon, 28 Sep 2026 21:14:34 GMT  
		Size: 6.6 MB (6623593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70499b8e445668af3445a3c270ba66af957c75f2d77dd27a66976536c9b59071`  
		Last Modified: Mon, 28 Sep 2026 21:14:34 GMT  
		Size: 17.5 KB (17469 bytes)  
		MIME: application/vnd.in-toto+json
