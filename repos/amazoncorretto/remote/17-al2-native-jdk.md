## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:732dd472325cfec5deda2693f063ca920d2d6ab652a45ccc0b0c3945d3873559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70ce2fe439d162cb23bf3542cf9dae88038db7a803c40d3db15e343a9e32db0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228787447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422b307e70ba11329782d13081181cec50531040066573558202f130557bbb24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:58 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:58 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:58 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f31d1fce1dda0c9a2775f71f278a80f752c07ac8026cd44ad345d9d5c45de7e`  
		Last Modified: Fri, 04 Sep 2026 16:19:27 GMT  
		Size: 63.0 MB (62964596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f83b5985a967345b3589d0f442f523388eb29ee5beb843a8d086b955b921f2`  
		Last Modified: Mon, 28 Sep 2026 18:04:20 GMT  
		Size: 165.8 MB (165822851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2305ef53a8664c781cb442dcf5c3b849bd6f849921e9351e534e5ef001256349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5982838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775cb7d173140d10431a68ba95504530b7ccc576b762c70e4f995458f998a84`

```dockerfile
```

-	Layers:
	-	`sha256:de5131c0e3145e918a9d0a300850632040999486e9ee52473645baf4515bb4ea`  
		Last Modified: Mon, 28 Sep 2026 18:04:17 GMT  
		Size: 6.0 MB (5972778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f80c210c9599ccdde042b9db62b58f71438926883ce8552b70f1785eca0854aa`  
		Last Modified: Mon, 28 Sep 2026 18:04:17 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b960b35409eadfc068eec831eb0fc3c4e10bba6cf1c6ab86eec197e6a3a65ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221071590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774127ad6bf00f2c671438ca370bf7ba85def816707a9cc39ecddda01486d660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:18 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:03:48 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 18:03:48 GMT
# ARGS: version=17.0.20.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 18:03:48 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17ad0bfad52234371433d04d036616a4bd4db51019fc530e40379ee1fcd6957a`  
		Last Modified: Fri, 04 Sep 2026 16:20:29 GMT  
		Size: 64.8 MB (64805101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfd4fbb01b49ae1358325bb175a203639dbc93108fbde0ae31faeb98bebe87`  
		Last Modified: Mon, 28 Sep 2026 18:04:10 GMT  
		Size: 156.3 MB (156266489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:49b10de116231eeeda45431069101a51b7d3415f6218c921c4cea13c7f8d1d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9ed0437f9d1eadb3067ced24a83d7fbfb7d21eb13cb3e7a27c3220a9ac6c1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae39e1cc40a4b4c7fc9b7cf497cbde4cc75278d3af57f7e6c8920160c68293ba`  
		Last Modified: Mon, 28 Sep 2026 18:04:07 GMT  
		Size: 5.8 MB (5764649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbddc8c42f3f1c2112109fca05dab316fc6469354b84d4a1aa9d637c2cc320c`  
		Last Modified: Mon, 28 Sep 2026 18:04:07 GMT  
		Size: 10.1 KB (10140 bytes)  
		MIME: application/vnd.in-toto+json
