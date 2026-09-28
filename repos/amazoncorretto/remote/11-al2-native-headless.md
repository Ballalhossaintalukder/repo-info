## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:0dc6b62ee1e93e2a1929647ad49abd2d4443eaeb48859065e76bc6f0d267206f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2079d14e9fbe70f029d07c7311436eff31f86a2c7b5876e04109710ee85d44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217375793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfca706fe909892320c95ab811ef6506e92c9ea4ca144254030448034dce0391`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:04 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:03:04 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:04 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc37382f1f1328e6b3a883889ff8fa2564234e704b7fbfa944df6c1bee13de`  
		Last Modified: Mon, 28 Sep 2026 18:03:24 GMT  
		Size: 154.4 MB (154411197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42a80fce0a70b99a7d0cdbf685032baa8c927300abc5cca50dcd14520faff5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab0f3a80570cbacd40f19344fa4d6da5c6abe4c2dd146132ba17f37a02d353`

```dockerfile
```

-	Layers:
	-	`sha256:a01c741d1ba12d2d36127c075a21c8a63c777d2bb2a2c3c85031113c1caea58e`  
		Last Modified: Mon, 28 Sep 2026 18:03:20 GMT  
		Size: 5.7 MB (5683436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b809f0ba1e60116d54dd59d5bc9ce2116fa68a752ba0570d239b21b6c106727f`  
		Last Modified: Mon, 28 Sep 2026 18:03:20 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a3b61c4dbf1da4de28e7ba1a8314fdae559e7faa9c3b6b232672cd6fe913bf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211425530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1007018119e9ab744ffb0fef2011b22de32671173d74055f3f2a045b92efcd95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:00 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:03:00 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:00 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b48fe24dd8e0d585ef0dc5324ac73b6739a2e4547e0cc09cc4f927d0a6ba904`  
		Last Modified: Mon, 28 Sep 2026 18:03:21 GMT  
		Size: 146.6 MB (146620429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9cb9b9799491893c3b6c6031898d8cb71868408b49a456aa98d2175390177389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea2df39234c6d72173d903dd65b4af63b0d304ccbe4d5770310deb659500de0`

```dockerfile
```

-	Layers:
	-	`sha256:d91ef2b0d66d897dcf2be15823e548bb8206df6f3c37a49efd143f0a53fb6ee9`  
		Last Modified: Mon, 28 Sep 2026 18:03:18 GMT  
		Size: 5.5 MB (5501904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c8edd4da9f9bae735d23c818314065688ac781fd44f7bfda1e76ff8820f5aa`  
		Last Modified: Mon, 28 Sep 2026 18:03:18 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
