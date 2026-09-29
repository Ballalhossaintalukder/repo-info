## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5c4a6c7de00c2ac1e02869bbbea60632b92bd0e6a3f62036c823a70fe9c0526f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8acc6ed10800450656056207969ad83b986dfbf8585fc36ee86c5e4769bd4489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137821061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70504b042b44d60b994c0557ded7b4040a46088621bc52d3848e0f52957d6e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:53 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:53 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:53 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:53 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4db6d5a8bef07a8a151242d313cf412bb2a8e15a6f9683407a816a73c9c853`  
		Last Modified: Mon, 28 Sep 2026 20:14:11 GMT  
		Size: 83.2 MB (83191234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b6bdef0efb5c732a42ede25bca868cbc521533b9de4c108cc9a5637f215b133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103aed13d3a47c4531c877cb1ae0fc84b0719525489326425b7eb477f988c59`

```dockerfile
```

-	Layers:
	-	`sha256:ec455817408266bdb18ba182f6e9d0d06689d008b1bf2eb99dc695de2f305d4e`  
		Last Modified: Mon, 28 Sep 2026 20:14:09 GMT  
		Size: 5.2 MB (5222541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21c9a1812dae8d0b3908c0766be61d497d35a0977856e3774f0771a13b7fc74`  
		Last Modified: Mon, 28 Sep 2026 20:14:08 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d789acc877d6b25c3153c06eaa4e367dd7eb4a3abf769df373ebe77a56e560c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136113104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd78dc6a3b6569b6035620835e767f1900576ce3c46fb1213cd2e6c97872d383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:59 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:59 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:59 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:59 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcc062cee37379b8bea7520d448f05cd65c55cde2c8907510e15040cfefddb`  
		Last Modified: Mon, 28 Sep 2026 20:14:17 GMT  
		Size: 82.6 MB (82615317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c0bd1bace41c1ba25a25912474f0841f21366c424d0bd418ee6238930e52fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba21c167a903b9193971a7d5325315a6addbafaf6b3e1d4d437d9f1418061558`

```dockerfile
```

-	Layers:
	-	`sha256:bd7b3f6998aa98c54d4a4839143b534b2ae3dee84b12a6f2da6c3b5410f0352c`  
		Last Modified: Mon, 28 Sep 2026 20:14:15 GMT  
		Size: 5.2 MB (5221345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d40c3002fce9e628b658d2b767d80e76198b9b4f056ee0a6d2cfebc83c7144`  
		Last Modified: Mon, 28 Sep 2026 20:14:15 GMT  
		Size: 9.5 KB (9467 bytes)  
		MIME: application/vnd.in-toto+json
