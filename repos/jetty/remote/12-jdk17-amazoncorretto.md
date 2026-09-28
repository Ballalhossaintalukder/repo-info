## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:813617f419d2cdb56079adaddbfe6dd3f1ff92d706739272846fa8696d92d91e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ebd52923474c48f1bc430daa7223fd82c49126cc82185d0354f7b52dffa65c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291195945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109ca51cc8953ede891550e4da6d622b93c26da3f235066d70a08bcb9d40517c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:36 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:42 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:42 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:42 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:42 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 28 Sep 2026 21:13:10 GMT
ENV JETTY_VERSION=12.1.13
# Mon, 28 Sep 2026 21:13:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 28 Sep 2026 21:13:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 28 Sep 2026 21:13:10 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 28 Sep 2026 21:13:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Sep 2026 21:13:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.13/jetty-home-12.1.13.tar.gz
# Mon, 28 Sep 2026 21:13:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	716EE302674CDBB2E660E1B44DB5EA09F2E3C800 	CD38A1DADA3413BE96DF547F3D146A4A1C58367E 	75DE085F73C1223260663C245663FB7A8FF7E348
# Mon, 28 Sep 2026 21:13:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 28 Sep 2026 21:13:10 GMT
WORKDIR /var/lib/jetty
# Mon, 28 Sep 2026 21:13:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 28 Sep 2026 21:13:10 GMT
USER jetty
# Mon, 28 Sep 2026 21:13:10 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Sep 2026 21:13:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Sep 2026 21:13:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3ee87b1055c51d2ac7dc8988b8fcd770985201b17d5a14a7907e4b854064f5ca`  
		Last Modified: Sat, 19 Sep 2026 02:22:41 GMT  
		Size: 54.6 MB (54629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e20413541bffa512131f03076ee98d97c707b46e08b4d72afe89841528e1763`  
		Last Modified: Mon, 28 Sep 2026 20:14:04 GMT  
		Size: 157.1 MB (157145930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecf94a15a7747fa1ce31cac99400d657cfc6772f8393f2bbace40ba3483daa6`  
		Last Modified: Mon, 28 Sep 2026 21:13:27 GMT  
		Size: 79.4 MB (79418312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb06669fdd44f873a46335008b87307b10073af78edf98d11cf86eadcaf7fc1d`  
		Last Modified: Mon, 28 Sep 2026 21:13:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:483dcaf6c818ca86ca0a5a5a26a899a3a9784b1c9de2a38049328728882f9751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b00c045a12e52d4fb92abf42c6263a04116c542a395f14ef5e6099baba604e2`

```dockerfile
```

-	Layers:
	-	`sha256:9a6d9468583c3cfb2c30c95d72b2f6993aaabbb2c0f0546bfd2f30f813156a3a`  
		Last Modified: Mon, 28 Sep 2026 21:13:25 GMT  
		Size: 7.4 MB (7443748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee88edbbbd1509a9094477a96ea9bda4a4b73292e50574dfb56912ce76ed4060`  
		Last Modified: Mon, 28 Sep 2026 21:13:25 GMT  
		Size: 18.7 KB (18701 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:79a5bbbd05cdb056695e531e783ccb7c7093e3af106d56bd299659fc555e0118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288746675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40af8c770e81157ef31bdd8dea5bc1beb696d3542f9c14989b8990abc16c97b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:13:27 GMT
ARG version=17.0.20.12-1
# Mon, 28 Sep 2026 20:13:27 GMT
ARG package_version=1
# Mon, 28 Sep 2026 20:13:27 GMT
# ARGS: version=17.0.20.12-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 28 Sep 2026 20:13:27 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 28 Sep 2026 21:13:24 GMT
ENV JETTY_VERSION=12.1.13
# Mon, 28 Sep 2026 21:13:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 28 Sep 2026 21:13:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 28 Sep 2026 21:13:24 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 28 Sep 2026 21:13:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Sep 2026 21:13:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.13/jetty-home-12.1.13.tar.gz
# Mon, 28 Sep 2026 21:13:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	716EE302674CDBB2E660E1B44DB5EA09F2E3C800 	CD38A1DADA3413BE96DF547F3D146A4A1C58367E 	75DE085F73C1223260663C245663FB7A8FF7E348
# Mon, 28 Sep 2026 21:13:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 28 Sep 2026 21:13:24 GMT
WORKDIR /var/lib/jetty
# Mon, 28 Sep 2026 21:13:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 28 Sep 2026 21:13:24 GMT
USER jetty
# Mon, 28 Sep 2026 21:13:24 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Sep 2026 21:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Sep 2026 21:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f009e1877a8ba7c389c4ac710ae4817f0017fbb8f3bb9e42058d4d18753a3319`  
		Last Modified: Sat, 19 Sep 2026 02:00:18 GMT  
		Size: 53.5 MB (53497787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf79a4629ec37c72d04a605aab54376cd8ce8387e70e9e56c187ffa77b7139`  
		Last Modified: Mon, 28 Sep 2026 20:13:49 GMT  
		Size: 156.0 MB (155952593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546fadb2b881e1ac78b0e5503e63502808fc099917bc94bea63cf403071ebb6a`  
		Last Modified: Mon, 28 Sep 2026 21:13:44 GMT  
		Size: 79.3 MB (79294421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c71f85ad4cef6f856f895fbaac6c8a6626f73aaee4e7f46267fb1c514fb46b`  
		Last Modified: Mon, 28 Sep 2026 21:13:36 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7bf925ea50443631164a9245947ef0845a98739029f123d1f9a128185a1f26c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7461544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cecf10c679526041ff1ac45a2a08c80c70f12820354963edd9a6c144846c80c`

```dockerfile
```

-	Layers:
	-	`sha256:efeb3828f942bf5bc41f7361dd437d76b36d217a1a187d37d8eec7fc76f04cf9`  
		Last Modified: Mon, 28 Sep 2026 21:13:42 GMT  
		Size: 7.4 MB (7442715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25fb162e01f132e554afde784f37688515573c70e8f2ed666a27f0263c11cf9c`  
		Last Modified: Mon, 28 Sep 2026 21:13:42 GMT  
		Size: 18.8 KB (18829 bytes)  
		MIME: application/vnd.in-toto+json
