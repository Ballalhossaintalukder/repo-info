## `amazoncorretto:26-headless`

```console
$ docker pull amazoncorretto@sha256:e06555a8a8b47f95e8d6648aa68e2eab4ce029d69dfe949d01e8f4e9cf50512f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:64025a71035f2a0ec8973398c1a189b9045b4f880a4b765ebd8ec4967decc32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160549978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1c9977417867b1d530646c0164f6e3e2d9084ad7b5080a4294a0e4dbaa1844`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:00 GMT
ARG version=26.0.2.11-1
# Mon, 28 Sep 2026 20:15:00 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:15:00 GMT
# ARGS: version=26.0.2.11-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:15:00 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:15:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1881a28c22ab869d111e560feb02c56a3ded12349cba40362fbe3e697c76b261`  
		Last Modified: Mon, 28 Sep 2026 20:15:19 GMT  
		Size: 105.9 MB (105920151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9198c88c4cc5173a13c407ace4d47a035883c6b3b0e4561aa70301324e9449a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6805dd429268c20692df9dc9bacc9f3c128b4dc14806b545f9733659eadb0836`

```dockerfile
```

-	Layers:
	-	`sha256:6c0846bf81e9c1fdde0f9662131b07f52e5dc4f8144e6acdd15c45ad35a19f42`  
		Last Modified: Mon, 28 Sep 2026 20:15:17 GMT  
		Size: 5.2 MB (5207037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648ceeaa91f6ecf8fafe46cc833fa702fb271157aa99eb4139f64d86c0368154`  
		Last Modified: Mon, 28 Sep 2026 20:15:17 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c9a234d1708fd033cca3ae98aee343ad4daec292e66fd301acd454bf16637800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158296248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e1c62c014528ed4dcb4585186dd291ed65eda9241df216ef136caaabf90be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:50 GMT
ARG version=26.0.2.11-1
# Mon, 28 Sep 2026 20:14:50 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:50 GMT
# ARGS: version=26.0.2.11-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b6ecbd9497f5b75a0abb2899da172e368be775302c8afad794afb83dd1e217`  
		Last Modified: Mon, 28 Sep 2026 20:15:11 GMT  
		Size: 104.8 MB (104798461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c24371f4f2125bd0240be63a77c961586002a45c3526c101dfd883bb79bc3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823b1ba07ea7c97a8145390523b0ddee75918ea840b5653fc8651923fc25b718`

```dockerfile
```

-	Layers:
	-	`sha256:d69e43f6d86cee18dc5795d2bd5e99dcb77601032d75c7b21e2bb2de7c357189`  
		Last Modified: Mon, 28 Sep 2026 20:15:09 GMT  
		Size: 5.2 MB (5205847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f936f6d0403cfdcbd555395ecb489d7cd06ae5646a0944718bffddf1a5e68259`  
		Last Modified: Mon, 28 Sep 2026 20:15:09 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
