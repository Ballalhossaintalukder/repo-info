## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:cd0addd1af243be32bb421ad8550ac603b860793ba47f22bd9dd47581c723cda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5f8ba1ef90ba6df92fa10b171708fe411f0e6047e703b3a25ef319768964e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208139217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b6adfcc68ac3abe2d8986ac52b9bc701f6442e8985f9512f4be4b77d62b8ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:54 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:54 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:54 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:54 GMT
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
	-	`sha256:0c470d9f3e7bb23017c7fcbbd3d2b12432db5ff01dd792bf5ead51de71014654`  
		Last Modified: Mon, 28 Sep 2026 18:04:10 GMT  
		Size: 149.0 MB (148962298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756474ded9f5f3703e8e2964e9e901163476dde62c24bd8e47212c4e93b5d3c2`  
		Last Modified: Mon, 28 Sep 2026 18:08:50 GMT  
		Size: 55.3 MB (55325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d12974c57c8f7cfbf49d446e9776c7d527dff9fb9a4ded078f5acc635cf0ad3`  
		Last Modified: Mon, 28 Sep 2026 18:08:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:48830782063ae83ec50fe10c3ef16ba9c66563fc0dcca160b6f084cfc58e098c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1033170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b06bca6a686f87d949a990c5240e7b05d9ba1254922e72e02a459b75f7868dc`

```dockerfile
```

-	Layers:
	-	`sha256:d5877fb421eff20fccfea0b18b01b2e93b4de6c00ae4630d2e186b6597ea162d`  
		Last Modified: Mon, 28 Sep 2026 18:08:48 GMT  
		Size: 1.0 MB (1015818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7169f9764c2a89b9f6e9ec0272d560319aa9b0ebe200593a14f70b767c85c7`  
		Last Modified: Mon, 28 Sep 2026 18:08:48 GMT  
		Size: 17.4 KB (17352 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4e3e1493f19140697a3f385b8b4508c249196d50456bac266478f853a9bc7a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206782256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5748a6d5386e94d64e79f02b6b9c1a2b74310cc4853d7e1c5de8583cac04843b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:35 GMT
ARG version=17.0.20.12.1
# Mon, 28 Sep 2026 18:03:35 GMT
# ARGS: version=17.0.20.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:46 GMT
ENV JETTY_VERSION=12.1.13
# Mon, 28 Sep 2026 18:08:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 28 Sep 2026 18:08:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 28 Sep 2026 18:08:46 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 28 Sep 2026 18:08:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:08:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.13/jetty-home-12.1.13.tar.gz
# Mon, 28 Sep 2026 18:08:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	716EE302674CDBB2E660E1B44DB5EA09F2E3C800 	CD38A1DADA3413BE96DF547F3D146A4A1C58367E 	75DE085F73C1223260663C245663FB7A8FF7E348
# Mon, 28 Sep 2026 18:08:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 28 Sep 2026 18:08:46 GMT
WORKDIR /var/lib/jetty
# Mon, 28 Sep 2026 18:08:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 28 Sep 2026 18:08:46 GMT
USER jetty
# Mon, 28 Sep 2026 18:08:46 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Sep 2026 18:08:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Sep 2026 18:08:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2874229cda9c9979aebf42074800618deeca0af610d920d425ca8bd919d9`  
		Last Modified: Mon, 28 Sep 2026 18:03:52 GMT  
		Size: 147.4 MB (147381446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c7eeafc58c1e00d15949399bdef1551d29409068ad77da6c10601c9209b7e3`  
		Last Modified: Mon, 28 Sep 2026 18:08:57 GMT  
		Size: 55.2 MB (55211274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a908187d746eabf47fd8ee5649bc61169b06b945ea64dd961bd12051dca822a`  
		Last Modified: Mon, 28 Sep 2026 18:08:56 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:eda39693de1238aaf36ecc0a04af15c418bb6c939fec242f33e2b62ed7e25421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1032020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fcacbbb2e5343a0100d9500b76430793126b023e78d3c0e11cc88814e1246c`

```dockerfile
```

-	Layers:
	-	`sha256:a6760f8621536ff271dba651c873d3c1056103fcd3e5ae9ad9824401c2d3e692`  
		Last Modified: Mon, 28 Sep 2026 18:08:56 GMT  
		Size: 1.0 MB (1014575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce892053750ca83f1f1f5cf6f5f1c8a2d55037027ce2730eedbba797d141c44e`  
		Last Modified: Mon, 28 Sep 2026 18:08:56 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
