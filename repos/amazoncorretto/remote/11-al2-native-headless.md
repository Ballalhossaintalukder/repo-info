## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:b65426534eb5f50d6764d11681b67dc4be6b2e1d309f083d8c066d6ebd8c3d64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:800873e326222fcdc168d852565f70fe525bba38a1ffafaadf8897f0a5ff35f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217376299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b1e864af8884c03d520ca307a20096ea2bad378336626fc929ca73c8fc9a82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:36 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:36 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:13:36 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304fcb648e957ddbd0d1df543939e0b435866d186ad091f31cf318d9eb38bb9`  
		Last Modified: Mon, 28 Sep 2026 20:13:56 GMT  
		Size: 154.4 MB (154410927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:02782575879ddc29d9e695a5f34e015c9e2058a3bea0921527b68e32b0fcaa18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d680ee475b27b8848a9a2387a7803b11b7a7a2e1fd0bd2b87dc757ba491957a5`

```dockerfile
```

-	Layers:
	-	`sha256:465d30ddac23e1fe2e1f20b5d6e33778b681da2681548b81f973a37398888c95`  
		Last Modified: Mon, 28 Sep 2026 20:13:53 GMT  
		Size: 5.7 MB (5683436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7816ccda5f9a9f07120a3f61890aedee9e0e09387708aabb06f10195dadf042`  
		Last Modified: Mon, 28 Sep 2026 20:13:53 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1f14584de670b33308d27f7d9e7dd02fee466ab4ec2e650fd02970c325e4c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211426425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6497b2f985cf705ae860d2f5ac4d12234608119f4d9b3b1e2c23997dae4542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:14 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:14 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:13:14 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfec9ae54f2b3c93a12eb0ac17982fe44ea2b5727392990edfc5e19e53b6fa1`  
		Last Modified: Mon, 28 Sep 2026 20:13:34 GMT  
		Size: 146.6 MB (146620266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4297fb132c4db28f83a352577991e3710c77fdd43be7215d47a45e37c9e72322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3941137032dee3cfc8a075aa56a6c7156279775af15dac70413afbd136972f`

```dockerfile
```

-	Layers:
	-	`sha256:4cb3fa2befdf8e4fd8754986c00fd1b6cc8c4ffbc19d66033a1c770546b3ce71`  
		Last Modified: Mon, 28 Sep 2026 20:13:32 GMT  
		Size: 5.5 MB (5501904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb08a464c10d6d0012253c2e54bcd7712dd100b378c9f54aad70d3ad6e6393b5`  
		Last Modified: Mon, 28 Sep 2026 20:13:31 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
