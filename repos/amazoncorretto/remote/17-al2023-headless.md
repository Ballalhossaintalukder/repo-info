## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ef3b38ea38214693f336ec10136c71d94628ceec5511bed1d3ccc9f0c06f9107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:996ecc425461e4afbcb164d6eb1a830e6534d8b8310d61e67242eee06f595c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137051686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73e6b6a3410f683a14200418991144ebb5e2cfe183bf07c053ef6321942611c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:43 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:43 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:43 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:43 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85434a888900d8fca5b1acccb6d7dd47af3370f54dd3e5584ce9e8b43c7a7926`  
		Last Modified: Mon, 28 Sep 2026 18:04:00 GMT  
		Size: 82.5 MB (82465404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:666344dede3cc87c1d169196a075a6a66413832730b97a5d2a3b613cd478dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e5d82096a8bcd3dcfec5a8b210ff5d8c2812dd298d6b26b9fc62d924e5f291`

```dockerfile
```

-	Layers:
	-	`sha256:83b48adca0b0d1761edab3203eaf238ebccab5a0fd2e898275ff671c866a9b33`  
		Last Modified: Mon, 28 Sep 2026 18:03:58 GMT  
		Size: 5.2 MB (5197111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513dd4979f7ed6e068a3af32a24280697298bee52a7ec98a6474f99f470f58fe`  
		Last Modified: Mon, 28 Sep 2026 18:03:58 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6e9a86bf2970d6b89541c3d066c7fe6779251d4fb4cb5433369c79e22e56023e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135326547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332434c997f9ed3498de137edd7aa917909074d21547870cd05d69602deeaab1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:39 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:39 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:39 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:39 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040be5d6bc6e752f4e19412bc6e50e8aaa1cdc0a3f0faa352fbddb88e3f683e`  
		Last Modified: Mon, 28 Sep 2026 18:03:56 GMT  
		Size: 81.9 MB (81873974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78e622b4193499eb88247b7b75bf0472cecec863c8f9c6ebeb3580025d84b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a637adb62b72b0d0ca8602a88a33359015cda63af6ee1795235d440bd38f9902`

```dockerfile
```

-	Layers:
	-	`sha256:924ed7913f6766e2cf7c85a4826897b0ffc7699bba12eac7e71074c6e5ae2813`  
		Last Modified: Mon, 28 Sep 2026 18:03:54 GMT  
		Size: 5.2 MB (5195912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6219b0937588a9cd3b2dab9c75d208ed3bed498f1b09bbeb11e2a0bebd3a1e94`  
		Last Modified: Mon, 28 Sep 2026 18:03:54 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
