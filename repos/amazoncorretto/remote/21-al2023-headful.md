## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f6d4baf6ffcc2f5ae389599bf0be85c7b047c0e2825286d79aa9d7523f159981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d1d5904fc324909ac0fad42a1c24e80b0370802d8a22df9ac2f62f753fba8bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144721776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b2468d55d9c0785d85db3e224c2673829092f26d578919b22c5cb0bce7c712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:26 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:26 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:26 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:26 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9b2dd986931050b7acf7fa48e0a3b96418e544a8dc5f21bc2f1300d62c0d2d`  
		Last Modified: Mon, 28 Sep 2026 20:14:44 GMT  
		Size: 90.1 MB (90091949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2e0daa3603b5b66a0dff84a63d4c44c874f73623096c0786b4722226b3fa7f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d11b867fe2790b5d208de438447583d022300a68dc6e17ee851a8bb9526cff`

```dockerfile
```

-	Layers:
	-	`sha256:002e095e48cd79c452415470ba3fba396922393754152499b5b3613091a133a9`  
		Last Modified: Mon, 28 Sep 2026 20:14:42 GMT  
		Size: 5.2 MB (5224167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021ce676b74272bebf3712a52a5d8dfcc915f1c38fe0b35498e33fae63da4f9b`  
		Last Modified: Mon, 28 Sep 2026 20:14:41 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:925882ed1e81ee15e325565f8bc301dfc4cdf3c5073c64405eeab49fb7383c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142717730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3287e35d3b88b2f8518fff525f2ba2bab3197aacb82c8c8a026f9d2e9a78fe0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:14 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:14 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:14 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:14 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860b3d5759ef94f227e81fa60b67ebf488b95314c3137ac13a64c67428b6931`  
		Last Modified: Mon, 28 Sep 2026 20:14:32 GMT  
		Size: 89.2 MB (89219943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e4137481049e9e6ce0799aa7c3cb61c1d3367a506c6d88c146b50c9a12659e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256bd2ac69179d8f0a853810ec0d188ce5419b2d67b3d15a0e4e48480eb06428`

```dockerfile
```

-	Layers:
	-	`sha256:4b807c081618e303f008e7e01ed83777d31b5e38a05172d1fd02b3d3ee2440c4`  
		Last Modified: Mon, 28 Sep 2026 20:14:30 GMT  
		Size: 5.2 MB (5222973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d96b53e5d392a8f2bb379a43934bcc90bc2a6c4d791620f25f4e22c7e0d1d60`  
		Last Modified: Mon, 28 Sep 2026 20:14:30 GMT  
		Size: 9.5 KB (9467 bytes)  
		MIME: application/vnd.in-toto+json
