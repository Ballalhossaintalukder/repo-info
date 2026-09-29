## `amazoncorretto:8-jre`

```console
$ docker pull amazoncorretto@sha256:f33205181126364b507d3d77d98e3e80a0954669991f0dc9dfd393ec636fde55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7dd21c774b7caea83ec3641cb6edb116e222f4399053a87746fd5ffe885c0c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109337755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296e3c5c7ae2e3b9ec10e593c89717a212e14cb97942d0c48bc1e54cac51c36a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:11:52 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:11:52 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && alternatives --install /usr/lib/jvm/java-1.8.0-amazon-corretto java-1.8.0-amazon-corretto /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} 100     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:11:52 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f753279be250f467af0d213b944961456b85bc8f2693f5c949c70f617c40f2`  
		Last Modified: Mon, 28 Sep 2026 20:12:06 GMT  
		Size: 54.7 MB (54707928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6b974063502517230996fae4cdab4b5c236daf9f69b4aa06f9f575a393c61f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56a4c41947817134dd1722f399e5002a9a7ecd9ba63b9827ea9412ca5b3dbb3`

```dockerfile
```

-	Layers:
	-	`sha256:16145b97ee2d76cc98d54a776d1c2bcbfe3b10374d00ae17c1194f804cf64e53`  
		Last Modified: Mon, 28 Sep 2026 20:12:04 GMT  
		Size: 5.2 MB (5218261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33bec01ccfe731b459852481fbab665a5b8ee1d2300a94775c7010fca4842bb3`  
		Last Modified: Mon, 28 Sep 2026 20:12:04 GMT  
		Size: 9.8 KB (9787 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c774d101867e5ee5b1843afb5c16a67e29fcd6e6ebdaced031ef75f6075529c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107937001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b12010247821ac5c34eee30a255f94c5abe8b761307c3fb4668f7a9a01dc929`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:11:50 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:11:50 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && alternatives --install /usr/lib/jvm/java-1.8.0-amazon-corretto java-1.8.0-amazon-corretto /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} 100     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:11:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:11:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd3198b40dd38e57b6315f0e0a0369b420588de7e8d02b958b6d8847c2470fd`  
		Last Modified: Mon, 28 Sep 2026 20:12:05 GMT  
		Size: 54.4 MB (54439214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a77e6abece56dbc2a4afb16c0348c66cc2ceb164c9efdfab70d03cfaa0b26928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b895ff6ea6f44448922374aeb300d1a245c48cf6faf21d1cf2f3cd84e11972`

```dockerfile
```

-	Layers:
	-	`sha256:c66b303b1a71a508e126afa84d56d66bbbc8443239c7fa6a6ea30d18510e2fd2`  
		Last Modified: Mon, 28 Sep 2026 20:12:04 GMT  
		Size: 5.2 MB (5217954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9970c5a1bfa0da58afe1fba9fe8dbbeda5442bff61f8350d99ba090ee97f97`  
		Last Modified: Mon, 28 Sep 2026 20:12:04 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.in-toto+json
