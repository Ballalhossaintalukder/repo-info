## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:2b207212400e97771cd581b5394558bfaf325d7e238f8a14aea9ecfc70e4f8ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:42dd74ba57471ce890c53088c25d45a9ee9af377303f9c1072e4950928c898e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161250007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cee444f0d9e0f53736eb91cf51717497ca68995c0784ba3c5ff939d1ac4f5f`
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
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:ab27a9bef2a1d514f326cc1cdd824f02f6956dd1f8998f6e71b3cf42e5ed9c71`  
		Last Modified: Mon, 28 Sep 2026 20:15:19 GMT  
		Size: 106.6 MB (106620180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b960d0922d485a6e5f726eb32bcf4b81ddb6c6c90ee231a3e3de8868e108bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4aad3a6bb25ca7b4e299eb49d78ebdb9d84cbe67f6d757af9ae6a8d8e3ffa`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b68f1e8d4550061e551f31c19da4de089c858b6823f0f2425a3a82ce2ab06`  
		Last Modified: Mon, 28 Sep 2026 20:15:17 GMT  
		Size: 5.2 MB (5232464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4541c6902a24ee28e75d3971a07aa50f270b498d59ff702501a780d61c59e53f`  
		Last Modified: Mon, 28 Sep 2026 20:15:16 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1b9b18767998d9143648fa4fb0880e6a7a751f7a667b8eef6a49f238a12f82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159021740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeb9d1de522a2554f43f074efa719015a556636aaf8e8cff11e44acf2502b82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:14:51 GMT
ARG version=26.0.2.11-1
# Mon, 28 Sep 2026 20:14:51 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:14:51 GMT
# ARGS: version=26.0.2.11-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:14:51 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:14:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0129392086689d2e94445b3d46e9a609094a013e8773ba20dfec5259c0ace763`  
		Last Modified: Mon, 28 Sep 2026 20:15:12 GMT  
		Size: 105.5 MB (105523953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:43bd1190a50e35197f326cd41afea0c74fe9a19f73650bdb0136aa927f521bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a379fbb3dea55b298738267d104115c079cf0a22c270fd4b0c44720db90e6670`

```dockerfile
```

-	Layers:
	-	`sha256:a652ed976c21743b3d489b1384b38e480d88f90f63885151eb04c1297dae258e`  
		Last Modified: Mon, 28 Sep 2026 20:15:10 GMT  
		Size: 5.2 MB (5231277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93db4da0feb016a9e17d11608dc636b0aac0c5ae38f7a1c6fb74bbcfb430597a`  
		Last Modified: Mon, 28 Sep 2026 20:15:09 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
