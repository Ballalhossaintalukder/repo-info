## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:428fa1647d8231cdcbb41036bb31e93019f752e21b748b5623721e08e5cd2d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:04d1145db7cd72380101a918518b80d7dc2c12ed29d60f5556e8c699fa11d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123533179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba42c2b32c12a1af5cc27891a20bfbd31a5b4237d287b5d2ce8fe67afb95a83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:12:26 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:12:26 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && yum install -y fontconfig     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:12:26 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:12:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da37fbfabad29c753d59e988dd724fbd43d425ca48e4cee1a18ea3fe9bfdbc5`  
		Last Modified: Mon, 28 Sep 2026 20:12:40 GMT  
		Size: 60.6 MB (60567807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8491c4306f41ad13a3f639a5760edb42769cb9bb195e83b3f504c42f223de044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aedb42eeb1d7bd3e651c65147d7b4b5db05dddabde600794af2e71fb48cf65`

```dockerfile
```

-	Layers:
	-	`sha256:c491d9c6f3fc8b899934eb35cf7aeba03276cad6381d25f91c0972da2f2386a1`  
		Last Modified: Mon, 28 Sep 2026 20:12:39 GMT  
		Size: 5.9 MB (5859918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf77dd51f329e935c6fbfee91696fd5437aa4f57669785f3edf92dfb1c428b3`  
		Last Modified: Mon, 28 Sep 2026 20:12:38 GMT  
		Size: 9.8 KB (9800 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:be898cbd5a869deb2f14e40f22a42db82a3f266529c41ad63f0cb6a0bd0ebed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118023533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c2ec6270a367bca078691315d111812bed47bc7870238bf1595396c7505e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:12:24 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:12:24 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && yum install -y fontconfig     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:12:24 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:12:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f7f49ca5cc42eb71bc2a6b394e6203a8eb187d10964fb54237323557633324`  
		Last Modified: Mon, 28 Sep 2026 20:12:38 GMT  
		Size: 53.2 MB (53217374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d959569745272f3a55c07972c54d889512b7bb085820663c0d179c0c8953eed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4177290edaf119f97f7f004a4602bd0e0eb13aa17b5912799185a86eb26eaba`

```dockerfile
```

-	Layers:
	-	`sha256:373761222985a111aa4ec7ea70543e227f1ba15cd0e9d104c7fb92d4f601ce0c`  
		Last Modified: Mon, 28 Sep 2026 20:12:36 GMT  
		Size: 5.7 MB (5661887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6130d8fa5c14d967fafd3ed6d22dd94660a00ea454965116a61f448f953d78b`  
		Last Modified: Mon, 28 Sep 2026 20:12:36 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json
