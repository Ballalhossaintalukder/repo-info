## `amazoncorretto:11-headless`

```console
$ docker pull amazoncorretto@sha256:39d2f7c0ee8242360c00cdea44d5cfb39e818c62e8ce1dc5d52158e60f081e5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f2fe070c5c50a3513f8866233c81d0d76666e7d14800279186a91a12f226e6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130649403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9edeebafa263a5acf3f6876f45ad5781ec9bb520b0e8e541b397362cffb7b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:13:04 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:13:04 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:02:57 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:02:57 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:02:57 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f0cc63a5845e28f771c9fceda4decc68b806470b009dae4085b441df0329b69`  
		Last Modified: Mon, 31 Aug 2026 23:14:18 GMT  
		Size: 54.6 MB (54586282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42cf711ce24248a6941a5ef7bf3821495098f29486dc1f3c2883349cc7cb534`  
		Last Modified: Mon, 28 Sep 2026 18:03:15 GMT  
		Size: 76.1 MB (76063121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e77ba258c09f7f905c945f9409d3c17437e8a0d6c046c1e4323390dfdcabda61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca31be4932d80cb570847be805b399aa5670beaec80706a7d4657b6894286b1e`

```dockerfile
```

-	Layers:
	-	`sha256:0e0f0cbbdfdcb96f6d1873e3a67c4933aa25167c1ed1d50e3275d887fb284cec`  
		Last Modified: Mon, 28 Sep 2026 18:03:13 GMT  
		Size: 5.2 MB (5210219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0498ba5b0dd876a85a2ff3576ef4ab060c6b06e1514822bbe31f729332d879`  
		Last Modified: Mon, 28 Sep 2026 18:03:12 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:250fb021dda3f04b2cddd0f4756b285dfa2af66d843e0a7080684dc5c34f03f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128757479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ee3d8c23b55b5735617bf45f1057e44e6bd1da5ce2fa6f54e9c4aec792239d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:12:44 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Sep 2026 21:12:44 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:02:56 GMT
ARG version=11.0.32.12-1
# Mon, 28 Sep 2026 18:02:56 GMT
# ARGS: version=11.0.32.12-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 18:02:56 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6b98cf5afd5c5e1a58de351abf0b1ec3a4a61b63fd5a86c62edc6367d59ac249`  
		Last Modified: Mon, 31 Aug 2026 23:14:33 GMT  
		Size: 53.5 MB (53452573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cfc941c014b722da650d79ab11a7a5158424feaf2bb2dd700bd746fba81626`  
		Last Modified: Mon, 28 Sep 2026 18:03:13 GMT  
		Size: 75.3 MB (75304906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e03816252ad6dacf4b4c297162df56d3455caa1ed8cb808dbbc3182bb9d66b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cda2972d2a1ff47a10a61cbe54fe03ca4037d6e3ff811de8ad6f367b7d25e8`

```dockerfile
```

-	Layers:
	-	`sha256:80269982daaf5740450d7a4d0715dddc737d10f4a7bfc76c21d598298d613618`  
		Last Modified: Mon, 28 Sep 2026 18:03:11 GMT  
		Size: 5.2 MB (5209849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5a6e618880486eb81c2db3cfac186407338d47c134b1589e9dd409384e0f58`  
		Last Modified: Mon, 28 Sep 2026 18:03:11 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json
