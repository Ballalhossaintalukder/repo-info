## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a76d395710d4abda54bee89f63b5b99e0a1000bdedd4639d7a4319c2bcd2fb3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:001dd87dbe741912e84b79da6c5563f0d29a5525bc31a7d77a531bbed62e1e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143941933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914cdb3e5fa192cca4125bc192d3115b3cacd7b1b453a829ba7ae9caf642acd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:19 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 18:04:19 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:19 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:19 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa6bf4e826376c1db0548e0ce451adf859661efbb0352359f9308c8dd339f7b`  
		Last Modified: Mon, 28 Sep 2026 18:04:36 GMT  
		Size: 89.4 MB (89355651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ae8cbf01ef7c202e5f4df2c3fba716970106f8fea5c5afac6842c4bbb7fa2166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865eab6be0c94099c6ec72dfae241c205fa4e7809dc05dad2f93c591d57f118f`

```dockerfile
```

-	Layers:
	-	`sha256:f285770fca03a2543be0ff448abaf8ef164acc9be9cb3271e648b76723872b49`  
		Last Modified: Mon, 28 Sep 2026 18:04:34 GMT  
		Size: 5.2 MB (5198737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c57fc8d281a67bf2e627c1b5d4f46ee1fdf057ef8be7d891fe417813116bce6`  
		Last Modified: Mon, 28 Sep 2026 18:04:34 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7dafff7277d354d06ceec359acc01a4a9f7cd7eff0ba340ea27d862a750048fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141935605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cff87c059c9efa628aca50b7a05f125d74fd775c43ee55e856225856a043e4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:26 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 18:04:26 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:26 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:26 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36cd3b4886f6ced71199b78cc9a1619206f11c9ae5bfb4e43ae13674cc4f89`  
		Last Modified: Mon, 28 Sep 2026 18:04:46 GMT  
		Size: 88.5 MB (88483032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cacc5b9cacb66304641abcd471efcfc86f0de18d0535dc9fd8643aaf52fe116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6b952d5e7a9cabadd4ed29768d533f5824ebf3dd632c987f9d4f6e074952d7`

```dockerfile
```

-	Layers:
	-	`sha256:f06a42957e06b7117de0cf384fff7c5f1b12e4da66793247b8b6ebb675f19db5`  
		Last Modified: Mon, 28 Sep 2026 18:04:44 GMT  
		Size: 5.2 MB (5197540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4088dec879410c7f71fb690c78d0773ce9e8807eafecb0851c93941b15e4b9d3`  
		Last Modified: Mon, 28 Sep 2026 18:04:43 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
