## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:034e1e0a5f37f57e7022d5ff1c8843b3ae2b2e9eafdbdffd24cb01bfae16a779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f8ad6eb33bfcb00de1ec7440fbaab71b1547e4ccc48ff94cff875b50e691ea19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130694367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8f17caaf9c8ff46bf5257aa794fd96667eeea0ae31ddba895a64cb010d29ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:34 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:34 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:34 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6662cc65415d96201fe29c0563475a38189c69e3d6b42e66ff80ab9959e527c`  
		Last Modified: Mon, 28 Sep 2026 20:13:51 GMT  
		Size: 76.1 MB (76064540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ff8267ade99f697f1dd66251fc1a0a217aea87158f2e276a6dbe8cd82595ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259fcc5fdc2a04a316c5818b80d0212535a5718219926eb2c04ade7592b5c062`

```dockerfile
```

-	Layers:
	-	`sha256:62a3b62524ce6718eaa12dfc1ef82b3fab01802dc38c0a9bbad2fe07b2a6cbaa`  
		Last Modified: Mon, 28 Sep 2026 20:13:49 GMT  
		Size: 5.2 MB (5210220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b673bf94de82a04547fe73044974548c34c0370c19a906d9dbd21e9cec077ae7`  
		Last Modified: Mon, 28 Sep 2026 20:13:48 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18d72ea56ab56265644c76965f3752baa806670750b23d9db1c8e55d603d6c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128803601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4435d5fd010fafdf811caf25bcd93f1ef6385c93c9fb2c8c995b73bc4e0997a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:22 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 20:13:22 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:22 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547dc1d60a8a9f69dd84772b2886d1bff4f296982abda7593bbe393244274c2e`  
		Last Modified: Mon, 28 Sep 2026 20:13:40 GMT  
		Size: 75.3 MB (75305814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4ad5a1185cd845e492205f80c1f24ff6d2cc8e0a6d964c773718e97820fb060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337d8732c41ac205d1bbf60b79f09a2b273c4e1d56ac6225a704a09515114187`

```dockerfile
```

-	Layers:
	-	`sha256:6935a45df95202084c502c1de935163f3b84c9e9391ec41116cf7f7c53162c63`  
		Last Modified: Mon, 28 Sep 2026 20:13:38 GMT  
		Size: 5.2 MB (5209850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2235c216d5b5bfe0c568b21a0f408341629064418ff9efbb7ce0b82a214dba47`  
		Last Modified: Mon, 28 Sep 2026 20:13:37 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.in-toto+json
