## `amazoncorretto:27-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9dbaa754ceae1ab78cfa704e977b6d59f824c4c14b7b52991d2e426ac81dd1fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:27-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:333441e2b4a74acbff8cba98c202062ef5380e87e7da2b7418a0f1aae611d576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160363883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f268a0a0978271d2db77dc0cc177edea9190a0c4d2a84e66ddc620d9f4e7c28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:12 GMT
ARG version=27.0.0.35-1
# Mon, 28 Sep 2026 20:15:12 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:15:12 GMT
# ARGS: version=27.0.0.35-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-27-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-27-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-27-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:15:12 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:15:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-27-amazon-corretto
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdef4126cc5a849ff4886ab7e0c6b18f48f845056f2df6c4d363d56dda31d1b`  
		Last Modified: Mon, 28 Sep 2026 20:15:30 GMT  
		Size: 105.7 MB (105734056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:27-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e77fc30530a0ace926520e385ab4ecb8f6be4ee3c0e4bfdaf347fa213613160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3409858ba2683fac7d673c0a2d4f6cdae3789ae753b6f6b47022e68e1e46aee`

```dockerfile
```

-	Layers:
	-	`sha256:af49eda02b6b5dc42dcdd5907db0f13471bf3a97dc8a5bbbaa41964c0daae190`  
		Last Modified: Mon, 28 Sep 2026 20:15:28 GMT  
		Size: 5.2 MB (5230817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a979c963bae8c3e7bbed6a896812196a6923df038d64de8820c947d0dae3520a`  
		Last Modified: Mon, 28 Sep 2026 20:15:27 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:27-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5af7c577f0e91cd3cbade6ada7f1d50b3bacdbe2fb7fa71ced2a3856466127a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158152344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1d60862552d8c4ead4279fb89219eb11ecc673477265647fbb2d4939b169bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:15:05 GMT
ARG version=27.0.0.35-1
# Mon, 28 Sep 2026 20:15:05 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:15:05 GMT
# ARGS: version=27.0.0.35-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-27-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-27-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-27-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:15:05 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:15:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-27-amazon-corretto
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82610cc971b4ac4271b4a1bea983c54de42501e6ee52078f958984720b70b27c`  
		Last Modified: Mon, 28 Sep 2026 20:15:25 GMT  
		Size: 104.7 MB (104654557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:27-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d5c6ac04f9a0492780fa4aea8fed3700e4516fa7ddb70654e968e135748504c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b1ee555b62a62aced5d1fce070b93f33f88100762a0db09d20b6db569befa`

```dockerfile
```

-	Layers:
	-	`sha256:b421c29aca076eb553c9880af6a21f116ed22523057ab4197ecbb653e22cf009`  
		Last Modified: Mon, 28 Sep 2026 20:15:23 GMT  
		Size: 5.2 MB (5229628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024eb6a35ea304ef544c3eb7a539d40fe044e4be16c6e22bcd204a650f11f222`  
		Last Modified: Mon, 28 Sep 2026 20:15:23 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
