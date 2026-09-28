## `amazoncorretto:17-headful`

```console
$ docker pull amazoncorretto@sha256:cf1671fd7580f1e7b11babd133de850a5fc5b24fee7d6f6079b8080ca9f9cffc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ac0fdfcd5332082fd43d82606634440ec59844b9d38dbebf8de00dad4bc7f52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137772010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94ec29e94b8e125e879676086cda4df8aaee03723e6fc14328b89f25640cf7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:45 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:45 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:45 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:45 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453405d7ddb2e4761f327a2ace0f5f98f5fac3385cbcc1ef827e89ce70c3178f`  
		Last Modified: Mon, 28 Sep 2026 18:04:02 GMT  
		Size: 83.2 MB (83185728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8fe40b03df86088c6e5aee7f6f477b45759d413d7c921607713a4a9756750da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e599a342b50958831d533b861c36a1ae23ee9b4bcb6dd784a0d9496dfd2ea543`

```dockerfile
```

-	Layers:
	-	`sha256:ea72185aeb8947ca11be1172c9073e3468b2adaccb73262dcb58d1272d436a45`  
		Last Modified: Mon, 28 Sep 2026 18:04:00 GMT  
		Size: 5.2 MB (5222540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b668a5e57c712f0def4dd49de5d233421bbe8bd42cee159ef3e6c45213f6d0`  
		Last Modified: Mon, 28 Sep 2026 18:04:00 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:61d8023900576b59e08ad939712b63ada558e01a4fbc9967b518b7720d97232a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136065560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d402d1f124886d6486250117fd9b5e718688bbea2947abd323d14465cd32309`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:42 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:42 GMT
ARG package_version=1
# Mon, 28 Sep 2026 18:03:42 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:03:42 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ec02c1ef1aa090e8b377fc4e6f7e287d761f88a07d97bc1e2141aa5e6d408`  
		Last Modified: Mon, 28 Sep 2026 18:04:01 GMT  
		Size: 82.6 MB (82612987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e06da2d05f0b49f3dae477b44f749ab6e66a5ad83c7c40026c332a26f5163437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f7f9b91ac68af0669ae9645abcb0b045b04e0e1cb5a84524ce54459e1a7ec3`

```dockerfile
```

-	Layers:
	-	`sha256:788e2470c26a47f0f65480987d7df5be656734379d9a7758bd5c5b91a5bb7ad1`  
		Last Modified: Mon, 28 Sep 2026 18:03:59 GMT  
		Size: 5.2 MB (5221344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1852ad07e9bd6b513c9201f7438127574eab8c9ba7fddbe8ea0644bac8da5f`  
		Last Modified: Mon, 28 Sep 2026 18:03:58 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.in-toto+json
