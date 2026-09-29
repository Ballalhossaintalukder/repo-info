## `amazoncorretto:27-headless`

```console
$ docker pull amazoncorretto@sha256:68d99e3d3ee8a0c4acd519dfdfd4d3e5aa16d1f679d88024e09a6b9a74635c3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:27-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4521a05517acb4f8168a76e9ee7f65a49aab1fb86a3d312dbb2af39caf0a3df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159659699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca24cd3c235a489cc480d1456415e53ac0ba51b0e9a9bec509119ed201fd145`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:14 GMT
ARG version=27.0.0.35-1
# Mon, 28 Sep 2026 20:15:14 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:15:14 GMT
# ARGS: version=27.0.0.35-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-27-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-27-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:15:14 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:15:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-27-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b1ca392fec51fa464c9be27d596f738418b79c1a8ff21b1e6b349f461b40c`  
		Last Modified: Mon, 28 Sep 2026 20:15:33 GMT  
		Size: 105.0 MB (105029872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:27-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d3950c940add06a190665192338ac8e455c2a81bd9a11a703d8aef651c805459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520f7c868f8f8db4dfe02e700f04aaec8dd0b9bdc2e3750054baecb26c362223`

```dockerfile
```

-	Layers:
	-	`sha256:61b1c1466a915e0b9a3aca50e13cf29094409a0378de6722c7ad63493d27c87d`  
		Last Modified: Mon, 28 Sep 2026 20:15:31 GMT  
		Size: 5.2 MB (5205390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de604aa35190942d043b9aef83b299a8529f1485f60b85265c908199d86f4053`  
		Last Modified: Mon, 28 Sep 2026 20:15:31 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:27-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:45ed346a44aac4f854275705e3a3ecc94b095101b0072f3a3c682bb4a43b56e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157422006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6eff28a65625639a4823fba7dabb4a38a9460f62afe55b2513755f1f49a146`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:03 GMT
ARG version=27.0.0.35-1
# Mon, 28 Sep 2026 20:15:03 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:15:03 GMT
# ARGS: version=27.0.0.35-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-27-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-27-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:15:03 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:15:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-27-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5939bbfc0cb12c2747cc8deee7cba37db82c544673aa49ec0d715922b3b65a`  
		Last Modified: Mon, 28 Sep 2026 20:15:24 GMT  
		Size: 103.9 MB (103924219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:27-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ddea8e2e732b57ac2626f3ad38c49218a3a720076d5c513fcf84bd842ef7c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768432eb424a6c648e537726af665469604fc5e04f7066fb89f08c06bb35c7cd`

```dockerfile
```

-	Layers:
	-	`sha256:a09dbb8f9a385563d19f2fd4ef4c3a667b5d22acc5ffe74c794a2b20d9aee9b2`  
		Last Modified: Mon, 28 Sep 2026 20:15:21 GMT  
		Size: 5.2 MB (5204198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b8daace5d1eaf2817a079be97c49b81dcf6dfa4f30d41b846231248ca39062`  
		Last Modified: Mon, 28 Sep 2026 20:15:21 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
