## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:28fe65bda7bb6384a19d1aca0697414078d1610df7bfd10e6c0656b5203a740f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:600c32c5014b719be8533163f3060aad2820e4954d8b58127ef15aa23694cad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150590146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6709b1c5d0a5b5f3cb3d0cfe6cc5e4434a87215507888e2d8c39920b23d6111`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:07 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:14:07 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:14:07 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f487fc49b68de040679ad3831678741c424935a5f98b616cc9fa2f58fde23db`  
		Last Modified: Mon, 28 Sep 2026 20:14:23 GMT  
		Size: 87.6 MB (87624774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0860529115eaaab3762ce57ab2f2dbd3ebb0df8be763a68b35bc932d8963ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78f22ed31d139f21754f700e997b2b9c1172fb6de813ebf2ad10c639692923`

```dockerfile
```

-	Layers:
	-	`sha256:80fd951a0150111ae76c5d8ebd8bbdb356eb8706318bbe5ca2e0cf6e7e806873`  
		Last Modified: Mon, 28 Sep 2026 20:14:22 GMT  
		Size: 5.6 MB (5632717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125b88b59ef9db238c92245ec4e025cd6ec7bcf4823ade7390cb32bc096fcdb5`  
		Last Modified: Mon, 28 Sep 2026 20:14:21 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9117147cf8a2a09b082f5d61cdf05034d17707f09ffbf3c351c7376fcb7ff1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144591553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914e0d16cb7b659cc0a9f019cc13ca37b75916b29756cff15c1071c7049213da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:47 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:47 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:13:47 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb59842b21b1940c6dd439edbcc5610df3d37c5e873fc0bf6f5764d14f7e1af9`  
		Last Modified: Mon, 28 Sep 2026 20:14:04 GMT  
		Size: 79.8 MB (79785394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e6668564938344042a048a41c5c481a1584b85536febf51c8426c5085112520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ada5c41ba5c4b2b8b6f46769851e5ff7e8e9019944bb013830441e4ce78c0d`

```dockerfile
```

-	Layers:
	-	`sha256:109c0897e5fd921b88b566b37884d7dfc3fcde83ad391fb053ed51bc25c730cd`  
		Last Modified: Mon, 28 Sep 2026 20:14:02 GMT  
		Size: 5.4 MB (5448994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d0f155be10ead50622796dc98e643ac8603ec6441fcc3c378d5de2066b460b`  
		Last Modified: Mon, 28 Sep 2026 20:14:02 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json
