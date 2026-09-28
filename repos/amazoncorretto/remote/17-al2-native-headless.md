## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:4a2cec31a216a3516d792473947545ad9b7d916ed744bd483e810217a2620300
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b26265426cdccb04c985086e33b75c000774873dd640df958273c8a8ca04817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150589358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce3d0b8aae763bf10595f21d85e47e16c02924a0635690a4618d3dff7503eae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:43 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:43 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:43 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e52b88c053b1cb994693c0a8b6e9e0b4a44c19c92ed465abfaecac17073cf90`  
		Last Modified: Mon, 28 Sep 2026 18:04:00 GMT  
		Size: 87.6 MB (87624762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82f295ee80d7a8eed6f49c82550821ccc0b48bc2e754062b3b87fdfafcc6b0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840d8e15742fb83a053f7ad19ead8f59cbe030e64b991ec32a76b867cf8cf8ed`

```dockerfile
```

-	Layers:
	-	`sha256:1a548c8feafbd22256beca7e4bf0ec35f52844f48ce963a1ff488942abbe13a6`  
		Last Modified: Mon, 28 Sep 2026 18:03:58 GMT  
		Size: 5.6 MB (5632717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628c7affb6be0abfdd291e858ffb63cfb0b3e0cf5f2650c77ad2e3830c4161ea`  
		Last Modified: Mon, 28 Sep 2026 18:03:58 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:29885e7baf260cf5c21103bd768dbea5b60abc7f8c75a5480e42dcb2eda3b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144590650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639343e3b7061ad446a1b0577b165a8481d7ff5291745796f4f8fbacab9e663e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:35 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:35 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2352dabf3810cb6f1ff4de3fd3775c89d5d23b584f7ccecb194b2426e47ea427`  
		Last Modified: Mon, 28 Sep 2026 18:03:52 GMT  
		Size: 79.8 MB (79785549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:230ca98a9369968d64ed6cac0d161345324de63911830861df5f9254b0f2d5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08736df975378a9d862f2d0844fb77a46ca86e01bef6ff38e7867b45604b90fd`

```dockerfile
```

-	Layers:
	-	`sha256:470baab8f7c34bbdebd0834a15bfaee797999ddf9beaa370c649cc1ee36b281e`  
		Last Modified: Mon, 28 Sep 2026 18:03:50 GMT  
		Size: 5.4 MB (5448994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e073fd9b7328b2a2611eadb2572ac753a94280736a858c8f3224fac050ab3b7`  
		Last Modified: Mon, 28 Sep 2026 18:03:50 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json
