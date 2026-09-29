## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6ea653460f2aafbb6b89785778e7da5d830c4c8cee17355fc4b1514350eb3c24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:746153197fdb5eaaa2f0b4a519042cae18a78a00a53c84a49164f5a5e20774cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131387491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582ba5b6e321c9c4a17476795554e8ea5a1d07167686a9e8841f5b01c872d4fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:34 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:34 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:34 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a650056215eb2a6301b2ae3e3cd2f6c0364a68c88a1aa2baab6bfff7b92549d5`  
		Last Modified: Mon, 28 Sep 2026 20:13:51 GMT  
		Size: 76.8 MB (76757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:afed281ea2d39c63c2ed37f5ce6db37ea4b2eab441a162d9c7aca92e1747e1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f818239b837b3154abb2c7bb758ae57d61c7d083489183e571339a75281727`

```dockerfile
```

-	Layers:
	-	`sha256:8ed7bb2eb0c79921dfc38a40fc4683203348b4e29e064deb307d06b04548ab11`  
		Last Modified: Mon, 28 Sep 2026 20:13:49 GMT  
		Size: 5.2 MB (5235645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3984c3a4437f6bdecc8935acfbf294c552df14ebc823ac1c970ca82f8852b1c8`  
		Last Modified: Mon, 28 Sep 2026 20:13:49 GMT  
		Size: 9.2 KB (9228 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3fcf548a4ca2070d250ecd8c98a8f6cf2d8842153c0653fc7218711aadaf54f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129512732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf09dcdac65cc84b46f84ba0e7b2fae046af57c40d8600bc14deab5b201c7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:23 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:23 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:23 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4922e7c5e6f11bfe5ab910917b1ef3bc56a42427774d75d21b040deb242f8f35`  
		Last Modified: Mon, 28 Sep 2026 20:13:41 GMT  
		Size: 76.0 MB (76014945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35780a13d1124f40eea355380330636a8f9adcda457a6caa37866ab40f5e5fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c976e15a98d4857d20ececf779cf951241f617477de5a00a84b8ae0c07dd38`

```dockerfile
```

-	Layers:
	-	`sha256:fcbd334d3c577de2500eaa83f3b595bad6d79f10e7c12b2b15caf68163bc7151`  
		Last Modified: Mon, 28 Sep 2026 20:13:39 GMT  
		Size: 5.2 MB (5235278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360b618191194fea31361071f3f4810f690e626a390b72878d44ff285f4a865a`  
		Last Modified: Mon, 28 Sep 2026 20:13:39 GMT  
		Size: 9.3 KB (9321 bytes)  
		MIME: application/vnd.in-toto+json
