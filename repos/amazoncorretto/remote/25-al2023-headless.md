## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:04859e30f1e327c3e6d7c138a6298f8992fb44c3d4d690824625e20c2e92a10d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:699ded5f0757bfbf436cd29ce1cb57abdd1d35bdf30a7249d8b47d8f9232347a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158332650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d32855b22426325fad23c76c0e71ce388f33bafc63fe2b5a3047e879f9136e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:51 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 18:04:51 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:51 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:51 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6fcbcc9996ac4468253bfd0fa12a8b61b965f972e9ebfb2d9f63f50fdaa0e`  
		Last Modified: Mon, 28 Sep 2026 18:05:11 GMT  
		Size: 103.7 MB (103746368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ea3b476b1ca7a686e1a344acabb9607fa441e05a5309b6751be59ba381fbdb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b3f8ef67156a8119565b37abea73415a331a899082e75b656d26f188a30630`

```dockerfile
```

-	Layers:
	-	`sha256:7c86f56258f28bf52ee25c9dbf1a5c6196ef643a315f9f94d9dea3833a02e200`  
		Last Modified: Mon, 28 Sep 2026 18:05:09 GMT  
		Size: 5.2 MB (5208678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa9b0e1aa6356d71ad9d31629c9fcdb7b018a1a5e0a837b044e0000036f5a5e`  
		Last Modified: Mon, 28 Sep 2026 18:05:08 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:512fdf4276295b2ef651494359da853f7696862f1e3d89b2447695f5063ef9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562a65802eed56af820a186a86e0d28e6b4ccc78e1141c82885fb247ca4b895b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:04:46 GMT
ARG version=25.0.4.10-1
# Mon, 28 Sep 2026 18:04:46 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:04:46 GMT
# ARGS: version=25.0.4.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:04:46 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46cbeaa66cd6bf6bb260b19197e703908e45b7193236c7908b848dbbe6a4f5`  
		Last Modified: Mon, 28 Sep 2026 18:05:08 GMT  
		Size: 102.7 MB (102674969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9605c9d6bc66dbe08f41e0d0d678f918e1bde49dd7720cc84cb8332fe821168d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b756e7861a203d85af833870b1c6d0b7a5f5170545915dd7e4e636af8fbe464`

```dockerfile
```

-	Layers:
	-	`sha256:d9266aba4f7c3803d674665dd962396c2f03f859bad651cba7e2e26a65c1bb70`  
		Last Modified: Mon, 28 Sep 2026 18:05:05 GMT  
		Size: 5.2 MB (5207490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2009e46bc04317db989c04ca1ce90bd3dc66a356854d400ac7e4803058fae6f7`  
		Last Modified: Mon, 28 Sep 2026 18:05:05 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
