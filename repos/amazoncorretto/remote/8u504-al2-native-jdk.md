## `amazoncorretto:8u504-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:ff16fecb6576d2cff17a81ab30398cc26e7c426570e64eb90bc20fede9537801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u504-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6223195f21671a2437d772e8b6606c622ad8dae492ced54d57d0e399199fcf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138125545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dfd49970ec4ea69116185ba74c7b81ef51488091c55f3775cdef744a312f01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:31 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:13:31 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && yum install -y fontconfig     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:13:31 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbfc59704c898eeef48086ca1e4fd24739a25fea8b785cb85e5fde5cd87247d`  
		Last Modified: Mon, 28 Sep 2026 20:13:48 GMT  
		Size: 75.2 MB (75160173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u504-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:852647f244d4e78cf4c3720e703592b44c6e25632ad60061b4d3304c55091c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6333272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d82136c9eccdbbe34a226269977d8eeaf49959d29ec6603fd84b39317f68b2`

```dockerfile
```

-	Layers:
	-	`sha256:f3f6fc66781c8a30f077218a82cf8b665220c6e661a495c88c6ad8d4648fbc9f`  
		Last Modified: Mon, 28 Sep 2026 20:13:46 GMT  
		Size: 6.3 MB (6323435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c1ea1cec051f2abc7e95345ef15d265bac303c0ba729e8e133cb84b496ece7`  
		Last Modified: Mon, 28 Sep 2026 20:13:45 GMT  
		Size: 9.8 KB (9837 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u504-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:85bb0ba52bd5d6e6c8e04127cc400856a1ce3be2a8858b27436342f08f75fbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132777126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5ba2f3da764cebbbf85d36877ac7a52e5367df5fa7874cab407b47fe23aca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:12 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:13:12 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && yum install -y fontconfig     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 28 Sep 2026 20:13:12 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f8b85bade502ae57608a4bd6c122f06557d4277d27a04cded08d100fcd7a88`  
		Last Modified: Mon, 28 Sep 2026 20:13:29 GMT  
		Size: 68.0 MB (67970967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u504-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2fa5fdad1e2ee3ca2506dab9129fd9967b428eb4c23d596a1cc8f84ebf48ee79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f068df65b21bab8865545f562e8cbca0b82a7f9edd07e5f25f0780599da31`

```dockerfile
```

-	Layers:
	-	`sha256:b73c5d62211db7f85dbc67e504cd590b4eeca77848aaca132ce7e0a247caf915`  
		Last Modified: Mon, 28 Sep 2026 20:13:28 GMT  
		Size: 6.1 MB (6125937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ac83e2f832d1a8e9fc1f39c46ccc9752e5893b5fceb5e583f33498121d717c`  
		Last Modified: Mon, 28 Sep 2026 20:13:27 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.in-toto+json
