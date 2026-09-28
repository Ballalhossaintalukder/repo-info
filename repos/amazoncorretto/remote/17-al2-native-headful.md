## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:e325e84ae8d1cf59ac0bb9c5361985c5eef6e01679ddd600fe5f7c1c0b0f9c1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:611308a0c813bf5469701760834b05ae367e17befdf6e5863758d7264df6cb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154277854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7b0711332d21a199fc1653a0c4512e9a89e57ba39af040dbdd4190b1679afe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:52 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:52 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:52 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0089daad992072580ebeb88e801394af4592c07fe1bbfbf67a62f00c367136`  
		Last Modified: Mon, 28 Sep 2026 18:04:11 GMT  
		Size: 91.3 MB (91313258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:30a11ff8d813bd39d13e1206ae26a9688f5ea93416b18862c0ee63eb3d1b5019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1176ca5dcd1555daa73eb2069ec35dbab1388dcdcd97167bddfb03f4a28334c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d72a7368533b7dce2a964e82eb9965b8e789c86636dea0991074c468a903598`  
		Last Modified: Mon, 28 Sep 2026 18:04:09 GMT  
		Size: 5.9 MB (5866778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de68c1b6fc72dad755df09275936fcafba3f95dcf3b6a9b455ea26ac6930e58`  
		Last Modified: Mon, 28 Sep 2026 18:04:09 GMT  
		Size: 9.6 KB (9590 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b71e3ba0d667e63f363260215eead95b457d362caa306c2f08c67f953b97779b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146746071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d1ca2a2d397ba875825153ba996dca502d5bb7c6f81694ebe9b0123e08200c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:40 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:40 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:40 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39361efb4cdf88edf4ba2975b4014a44e64ff4bae90ef77a1424a33bfa5d3e20`  
		Last Modified: Mon, 28 Sep 2026 18:03:57 GMT  
		Size: 81.9 MB (81940970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3a990fda50900a872526f23ac78a58b6073104fba29a929b93e10b8e8f3cbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099ff0c535f9d7a7eb8a7f347b1b6b092b63211304ed8b0611810dc679c39968`

```dockerfile
```

-	Layers:
	-	`sha256:2f09a44019e052c384d6055a1ac1df5c46e6ec26d44d91f3c92fc5c849ceb250`  
		Last Modified: Mon, 28 Sep 2026 18:03:56 GMT  
		Size: 5.7 MB (5658522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4751108ff0499ad63956b0c44f084f171f88502ed506bcd5440ead2efe58d1`  
		Last Modified: Mon, 28 Sep 2026 18:03:55 GMT  
		Size: 9.7 KB (9670 bytes)  
		MIME: application/vnd.in-toto+json
