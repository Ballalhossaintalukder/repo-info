## `amazoncorretto:17-jdk`

```console
$ docker pull amazoncorretto@sha256:114c4c07a5838b486a670c33f275ec40cae57a124f82c691d8ca7965934c7749
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8847cab847b1b7759b31f2d483f856e79d81086a22e5becf2162624d11601aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211727881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd37c5619e5f995f083783d924fa657f63f1c2e524b75a34372577d3e5f95d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:24 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:24 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:24 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:24 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b3549cbdba2cab379291d4084add9909d2dd84bb6dce6220c51bb9144303c`  
		Last Modified: Mon, 28 Sep 2026 18:03:44 GMT  
		Size: 157.1 MB (157141599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e53ac214d72617c6449a8a88392b8d18ee06055fa1ccb81eeda8aead04b44c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3301cc39212e7f29045a91605443f995ed31710282fab8e8e033a46b1f1be5`

```dockerfile
```

-	Layers:
	-	`sha256:6bd405a65b6ee368be01bc09786085aedafdf6e48ba9abbb8bf84559b897fcdc`  
		Last Modified: Mon, 28 Sep 2026 18:03:40 GMT  
		Size: 5.3 MB (5329484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e79db004c446e5cd046fed591d006cc47f09accb0c5756e7588797101e95cc`  
		Last Modified: Mon, 28 Sep 2026 18:03:40 GMT  
		Size: 10.7 KB (10660 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1d3ff21765637704e911e58f0955d0577cbd33a33f6fc409978ae1dbe3f20ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209402113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6762ebfd5bb634ad6ef84e70ac678fa2482774c28aff97abdf118085f52e69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:37 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:37 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:37 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:37 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b7213e1ba7ee9bfdb8cec80600e3a0fe686b42185e64d47d6ef9c77e1bd3b6`  
		Last Modified: Mon, 28 Sep 2026 18:03:59 GMT  
		Size: 155.9 MB (155949540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26b77e8f390ab773a9ea1a9918a30e479a4e83ceeba9ba092b9fe2ad20425156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81797898ac36b955957135fe768d2c6148141be06cf9cf27f414bd18b576f14e`

```dockerfile
```

-	Layers:
	-	`sha256:3564695d8da614e93cf0ff3d4897a01ce66e1da76915726e7667d5d4d3a5e75a`  
		Last Modified: Mon, 28 Sep 2026 18:03:56 GMT  
		Size: 5.3 MB (5328451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d3dc7fb150f3ddbe3ab452be7134fc4315125f108107a4d5b109e27323bcb0`  
		Last Modified: Mon, 28 Sep 2026 18:03:55 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.in-toto+json
