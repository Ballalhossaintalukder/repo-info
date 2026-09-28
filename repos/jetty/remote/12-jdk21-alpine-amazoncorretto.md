## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:ab80100f2b04d66c7f2fb48e3883d724c1a2526039c9585f8f26bd4b8da47096
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d3b15ea91115f99348e0fa5017bee01b4bfd762a0296ba29a5abd6cc2b98363d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221375487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12828fd060da61654056a826feb1bcbc9f3fb79ca9e0f7abf516fb1eab890502`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:22 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:22 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:22 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:38 GMT
ENV JETTY_VERSION=12.1.13
# Mon, 28 Sep 2026 18:08:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 28 Sep 2026 18:08:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 28 Sep 2026 18:08:38 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 28 Sep 2026 18:08:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.13/jetty-home-12.1.13.tar.gz
# Mon, 28 Sep 2026 18:08:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	716EE302674CDBB2E660E1B44DB5EA09F2E3C800 	CD38A1DADA3413BE96DF547F3D146A4A1C58367E 	75DE085F73C1223260663C245663FB7A8FF7E348
# Mon, 28 Sep 2026 18:08:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 28 Sep 2026 18:08:38 GMT
WORKDIR /var/lib/jetty
# Mon, 28 Sep 2026 18:08:38 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 28 Sep 2026 18:08:38 GMT
USER jetty
# Mon, 28 Sep 2026 18:08:38 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Sep 2026 18:08:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Sep 2026 18:08:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d781ee64e4e37cbd7e17b1fbd2abe312c76056972c450befcd138ec81aaf579`  
		Last Modified: Mon, 28 Sep 2026 18:04:41 GMT  
		Size: 162.2 MB (162198681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279ff2750d9ba343ce8d0c447193dd17f51652d94b012607dcf69afb04036ecf`  
		Last Modified: Mon, 28 Sep 2026 18:08:50 GMT  
		Size: 55.3 MB (55325191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dae71436ecc0e1b5bf3b17a51269755c0311dcdfb8125aeeed46f76da85c02`  
		Last Modified: Mon, 28 Sep 2026 18:08:48 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e68117b8669949f551c62fa67c93d126a5770887b0893c1e41c1b443f543f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1033075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bda9d14b1a8136b141957702b2b06e32ce6d64b045b3b92e8eb94bee303716`

```dockerfile
```

-	Layers:
	-	`sha256:e0fc058e54b449277bc0d667d4bff4080b71aedb2e7b2c1a3acc6e7b1c480b37`  
		Last Modified: Mon, 28 Sep 2026 18:08:48 GMT  
		Size: 1.0 MB (1015721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d21d46ee1c4518720cf9ed09297ce6e9a853becac50a0096936413907e628cc`  
		Last Modified: Mon, 28 Sep 2026 18:08:49 GMT  
		Size: 17.4 KB (17354 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0f8d8553c5348300e083f4e0a91cce244436926927e048b74b1a9b07703e7c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219603811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5654f1ce93b80d55ee63b0603f2840960616220648c7ff652abc45065250b0f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:10 GMT
ARG version=21.0.12.12.1
# Mon, 28 Sep 2026 18:04:10 GMT
# ARGS: version=21.0.12.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:10 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:42 GMT
ENV JETTY_VERSION=12.1.13
# Mon, 28 Sep 2026 18:08:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 28 Sep 2026 18:08:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 28 Sep 2026 18:08:42 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 28 Sep 2026 18:08:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.13/jetty-home-12.1.13.tar.gz
# Mon, 28 Sep 2026 18:08:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	716EE302674CDBB2E660E1B44DB5EA09F2E3C800 	CD38A1DADA3413BE96DF547F3D146A4A1C58367E 	75DE085F73C1223260663C245663FB7A8FF7E348
# Mon, 28 Sep 2026 18:08:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 28 Sep 2026 18:08:42 GMT
WORKDIR /var/lib/jetty
# Mon, 28 Sep 2026 18:08:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 28 Sep 2026 18:08:42 GMT
USER jetty
# Mon, 28 Sep 2026 18:08:42 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Sep 2026 18:08:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Sep 2026 18:08:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36b47c418118fc77b81a192eaef2c0ffc98cddb4396f0a502240598153735b`  
		Last Modified: Mon, 28 Sep 2026 18:04:28 GMT  
		Size: 160.2 MB (160202971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01185a909d5823c7c4d7894972ba9e8c8445412c723d02c4bdabdff5a4c19a0`  
		Last Modified: Mon, 28 Sep 2026 18:08:54 GMT  
		Size: 55.2 MB (55211305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dcbe1d0c840a4a169ec2e416cdb5bdccf29062f19fef7edef6550eb63b463`  
		Last Modified: Mon, 28 Sep 2026 18:08:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:12832dc3269f86d459fe97957aabaec5799a4b8945dad1d72991a29dfed98b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0609fb036b8fde1ea4e672874fbc796336671ac59010d51d5b8b9c807a07af`

```dockerfile
```

-	Layers:
	-	`sha256:731d011d10427506e5a01014c6fbdbb7bd0fcb57dfa354c3974c7b993fb0bcab`  
		Last Modified: Mon, 28 Sep 2026 18:08:53 GMT  
		Size: 1.0 MB (1014478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c2f83187b29014eb124f55cea69534e5fc442e563c20c3ca33c7e4d8168102`  
		Last Modified: Mon, 28 Sep 2026 18:08:53 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json
