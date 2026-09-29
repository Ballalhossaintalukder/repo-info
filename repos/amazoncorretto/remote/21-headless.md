## `amazoncorretto:21-headless`

```console
$ docker pull amazoncorretto@sha256:26f4ff28f9214a2b32a99e824d9375f5669bfa47d3a1f0b07b3afb60de9c0281
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1903b6d9edf888dc9f6392037de05a7dadbd686d458d7b52badf090fb954a7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143987667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168d8fd311e64ae02ac57f43ad927c21fff6e6e15b6f8c2a9d1b4063896c6f9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:23 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:23 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:23 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:23 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c240cc0d4d27be740bad075a34aa558692f0492ac19a2c765a8af8a9dd4ca6`  
		Last Modified: Mon, 28 Sep 2026 20:14:40 GMT  
		Size: 89.4 MB (89357840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f136c272dde02ade260a5527d5d9c31ff379d6193ebbd4082745030ce96b9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141fbda3d7724a1f3a6230a52e72462f7c2a17e7ed6a72d7dc8053b6cb46e5c0`

```dockerfile
```

-	Layers:
	-	`sha256:acdbe766f440ae66a83bd541f079abb22f6edfdaa3c69fb5b64788e34aefe07f`  
		Last Modified: Mon, 28 Sep 2026 20:14:38 GMT  
		Size: 5.2 MB (5198738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd09cf3c538521ccacde3957d1659f53f76b1cb8f09739ab24ec8cdd3898ec5`  
		Last Modified: Mon, 28 Sep 2026 20:14:38 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dc9c639455466d6a219e883a80517e5f08b0ea98d61c66b7fb18b22e53270a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141981631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226e678596d34d0f6dac1c847d631c5da313cfebc782e5a5a2eb410024defef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:11 GMT
ARG version=21.0.12.12-1
# Mon, 28 Sep 2026 20:14:11 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:11 GMT
# ARGS: version=21.0.12.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:11 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e89fa9e067a82ed148e40b0a0f9346aade5195cc42d1fe0118778d7db7125c`  
		Last Modified: Mon, 28 Sep 2026 20:14:31 GMT  
		Size: 88.5 MB (88483844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0bee014a30e2622355e485cfd8d8768cee55875d7df38516acc96525f5279b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379dbb1a03f277255b87ee773b11cf4f40451dfcf21d6d6f5e3243b0590ff642`

```dockerfile
```

-	Layers:
	-	`sha256:7107b42c55bd05772d1ffb53f80b5af811e2d8954c2edb3c00afc2fbe29b84d5`  
		Last Modified: Mon, 28 Sep 2026 20:14:28 GMT  
		Size: 5.2 MB (5197541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6278a3262bb585dd3c04daa3efa1e71667cd381adb4b54830c205727508255c5`  
		Last Modified: Mon, 28 Sep 2026 20:14:28 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
