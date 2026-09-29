## `amazoncorretto:17-headless`

```console
$ docker pull amazoncorretto@sha256:8d71d5ea314e79280926a8d70d16ed0d5984348a680e80dfa4c68080e470d274
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ac8ed2ad5fb1adf0f297ab7cc4641fedac73b1a53d9b363210839428f3158c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137097024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbed763222050c909efa5a7afe3ed629fbe6e4bd672069dde6af31a38ae84758`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:08 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:08 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:08 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:08 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230541a8a4e4c457ba4d382cf7dca46b184a8a1f1eb83db96a8d5e2c1b558a1c`  
		Last Modified: Mon, 28 Sep 2026 20:13:25 GMT  
		Size: 82.5 MB (82467197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0a525770a578e21e947dac9fb5cf6f8eed9d63f32e9512f43cdc3826e397b31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800ca66c01837aecd5cbd01d8afbfcc5e3d0aa1c4e4c67250df4b1a90a546692`

```dockerfile
```

-	Layers:
	-	`sha256:35eee0585b2c93cc7c832f25f8ed2135ba3eb183a5995276520e7c99f607dab7`  
		Last Modified: Mon, 28 Sep 2026 20:13:23 GMT  
		Size: 5.2 MB (5197112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1834971f0bfc30420f9d1caa3297d775c1c5c8a80263b3738b3f7b31edc560dd`  
		Last Modified: Mon, 28 Sep 2026 20:13:23 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:86af5f1b99e885f2ffc76839cf231f1f90ae2ade3fa3b28e19c612a14a46f99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135372950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6555c1b6715cc052b1fd8565a5efc2a2ebb25477c79dfcc93df00b3b0f852f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:09 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:09 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:09 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:09 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db34ed28dba608578eab3e551184209d4fbd2f11528427b8130163aabfd1b684`  
		Last Modified: Mon, 28 Sep 2026 20:13:27 GMT  
		Size: 81.9 MB (81875163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6631bff08e040aa07222f7d70c26176b17e9b273085710813379079e60057acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3448b310c11501e55f65b4b91b8123d7f809d92cc2f9c220150aa7c49857e93a`

```dockerfile
```

-	Layers:
	-	`sha256:cc0b778f0b31cfdc7f568ec73b165595810fe85d1018aae33f87b67bd9ec400b`  
		Last Modified: Mon, 28 Sep 2026 20:13:25 GMT  
		Size: 5.2 MB (5195913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a258219059c52785f1077c3498a495250290d1b059448d235594a539383ea9e`  
		Last Modified: Mon, 28 Sep 2026 20:13:25 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
