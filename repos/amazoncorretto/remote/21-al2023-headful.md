## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8ca3314b8111de0bae489a868aa49907f0c11636d67efb94d571b9afab90b90d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e92302d48501e20b8b556534612fc8a6f79fb8169f6b1bfb07166b7d76ffa12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144675076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246e73c82b73f86d5f41aee8be603cfdfd8a62f3f9c1ba72dbf5fc046ac993f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:29 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 18:04:29 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:29 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:29 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f1654f600ebc1d7c7b167a48a38f4ddd091e056581012a70e4f5ae3cb3f55e`  
		Last Modified: Mon, 28 Sep 2026 18:04:47 GMT  
		Size: 90.1 MB (90088794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc41e3832ad81dcce5b20aefaab955c439fd6d4a1fd108c601997002d62da7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd8020930e67f77e0fcd82dcfa374db366e6442b1473f9f5f9dbd520ccded90`

```dockerfile
```

-	Layers:
	-	`sha256:6caff04964de16642b120710ee11bb9753617fd676198d7e4410aa2a57004816`  
		Last Modified: Mon, 28 Sep 2026 18:04:45 GMT  
		Size: 5.2 MB (5224166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed11f2bca1c1638c4639ed437e2d99b95cbc09f6a25bd09d51212fe9208ba32`  
		Last Modified: Mon, 28 Sep 2026 18:04:45 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0578c08edc15d5e8f01179892a8d0cd41af591d0eb79870ece874e754d020be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142670588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9339f8934de000370d1dbfbbabb250cbc37b9d0e07d955506fea3e745a2595`
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
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:9e421fca1ece7cd9264213ec441d4c7e3b00305aac8f0da6fbcf7a4f8b7fbf3a`  
		Last Modified: Mon, 28 Sep 2026 18:04:45 GMT  
		Size: 89.2 MB (89218015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aed48b7f05f2ad58e2df422b97ae3e36ea5f54d0a9a6edcc02c0b25def83e58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc9b4acba4d5f0241507fe545f443eaeeb35f758321cf8cfa449970887f210b`

```dockerfile
```

-	Layers:
	-	`sha256:44d8868cea71c45824dae177ffdec963a1b8c107cf7bbfe3c65a9f55955e79b7`  
		Last Modified: Mon, 28 Sep 2026 18:04:43 GMT  
		Size: 5.2 MB (5222972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4246ce3e9e3cbb0cbb20359e8f2455d17dfc38aacf31df19933349a381e160e`  
		Last Modified: Mon, 28 Sep 2026 18:04:43 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.in-toto+json
