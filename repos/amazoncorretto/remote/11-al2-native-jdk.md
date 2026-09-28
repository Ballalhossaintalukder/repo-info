## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:25e2a983bd72b9ae8a0b1b765f93534aa216d6e1b93af9dfa39edb66233bf35c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:626f7fb9477466e11e751289bdb660579747744e539113a8350228c2f5cdd102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224645169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a9c06a2938f7612bf457785cdb2f216df4cc7db603ac66b22905f9cb78d439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:20 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:03:20 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:20 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d12fa93b1cbe12a6b7791f624d0cd6ce2e361ba6281e2e4496fce532a63a7c`  
		Last Modified: Mon, 28 Sep 2026 18:03:43 GMT  
		Size: 161.7 MB (161680573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd6f5d90db1ce3ebff32e96efe122619830a6735d48b29e8868a90fa1b4a0618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9e98e7724465c052a8799f576c7c071ea282e87635122a12b16b21c8001e42`

```dockerfile
```

-	Layers:
	-	`sha256:286169380d5743149ac8365ee26644590970320a0e1cf326a7582eb519b886ce`  
		Last Modified: Mon, 28 Sep 2026 18:03:39 GMT  
		Size: 6.0 MB (5995223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1a50348f1f715986ae6dafbad765ffbbf1fad452e6e1fc5f29bf8f59f7545b5`  
		Last Modified: Mon, 28 Sep 2026 18:03:39 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2b6f51a193d7da25f3ca21dca580e8e7e72b73a96e1a590596d50a02a0d25ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216514104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f0681e7e7057b9a3f5080c28a7fc496bdd0a0fc9de156b82f3f33bf58eafa3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:03 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:03:03 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:03 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1fb6bb65515cb6c0bcc38eb8f5a669404e2ca8939996d6cd1e2594383ca6ce`  
		Last Modified: Mon, 28 Sep 2026 18:03:24 GMT  
		Size: 151.7 MB (151709003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e8f2a55b7eaef86298a6fcfb2ad5c46bd39a8b664ff47fb77d2aefe3fb8eca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa0f68df462350405e9a7d1dfdb652d52e62fc02dcbe78bceb11df4117cc6cd`

```dockerfile
```

-	Layers:
	-	`sha256:1b428c12d084bb299dfbeadc661b02d0f9397f24f4ddb9f5d9efd51542d41d36`  
		Last Modified: Mon, 28 Sep 2026 18:03:21 GMT  
		Size: 5.8 MB (5787937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7996daef9e08899b8cbc6c5c27dfac73cd3451159f6571ba38badbbd3376cc5`  
		Last Modified: Mon, 28 Sep 2026 18:03:20 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
