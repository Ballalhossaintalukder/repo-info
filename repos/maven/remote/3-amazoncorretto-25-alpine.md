## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:5efcc6faba78451290a355763d260f990361e21084ea2125a81ba1d7b5f545f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:70e08a2ef745f145d362dfe408000a54103a1f82ce04b91617641225688c3b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196944413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36994e3cd499c20cfc17f487504fa11b02d269fcc8ce1c03b557343111d0142`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:49 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:49 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:49 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:09:44 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 28 Sep 2026 18:09:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 18:09:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 18:09:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 18:09:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 18:09:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 18:09:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 18:09:44 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 18:09:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 18:09:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 18:09:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17350f39c8bbe142c6bf23e285e398c0421e05929dfbdfb8305fb1ffe6cc10`  
		Last Modified: Mon, 28 Sep 2026 18:05:09 GMT  
		Size: 181.5 MB (181515906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cf6ed80ed0fad5fee5f8975704753fcc6a9a0b5059ac61c3999e59f70d566c`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 2.2 MB (2217791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6d687ea19018df0be0fca14a693505ee0df7b836738f0427e8ee9de3fed42f`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8ff8209bc7e7a3a63ad89000c7fecc7c0a3382d3ff026aab3a07c8f221abd`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275c4bc60485b30cfd889b4c48befe057b1fa4b92e89f4c58b07c60156b1c2d5`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:58c647438fe1563fffdc54fa3e7e925c27d391e2d0192cfe384160b2783ace78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd60766a1544a065f0d440126a34b7f93368f8ff8458e6083938174e2f8fddc`

```dockerfile
```

-	Layers:
	-	`sha256:ad91e283414ded422d542133e23c0ca378f7f2876021f8b02e82d5a6aead02b8`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 737.4 KB (737431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09c3e35ce927af82520ae9a50dbaea258dd3f6735db2445d92ffef8238c997c`  
		Last Modified: Mon, 28 Sep 2026 18:09:50 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2ce4b32a96dda250ba6ed657a6edc417e48795ba0f1a5d7af152551da72758b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194920080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eacf8d786886886be4249bf82e6f0c45400f6e17bb98e6c8624277ab999717b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:04:41 GMT
ARG version=25.0.4.10.1
# Mon, 28 Sep 2026 18:04:41 GMT
# ARGS: version=25.0.4.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:04:41 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:04:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:04:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 28 Sep 2026 18:09:59 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 28 Sep 2026 18:09:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 18:09:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 18:09:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 18:09:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 18:09:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 18:09:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 18:09:59 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 18:09:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 18:09:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 18:09:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ec7c5cf6b0f026b01470e3c9dc538b6ad52b752f2bc4d3560e5b87520a65cd`  
		Last Modified: Mon, 28 Sep 2026 18:05:02 GMT  
		Size: 179.1 MB (179114849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85413393514cd546a31aabcb1ce7f2946da1b923c4400ea743d558e5c6be36`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 2.3 MB (2256587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55611ae1f4e7d1aa7b34e80ca19810cf7306b298fdaf362c5afea62a1fe9dcb5`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 9.4 MB (9359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c7f20eda9c20124f93f10858abee715b83b17eb728b80df8da7b38a905001d`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366a5cd0ab6ee3a3b433b9fb57c9f7e752c867c1b54fd7c3f0afdd2d954708f3`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7bccab2a216fbdc9df41dcbad9b5ed93b5210074139d00678ea851e1e2c96ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.8 KB (750844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcc2dbeb17b493cda08d357d0be371361091b2d0c418cf95574f1e9959cbdc3`

```dockerfile
```

-	Layers:
	-	`sha256:901468c401bf0699af510cbe05addd65e9bf3fc84194d6779b5bd487b131555e`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 736.2 KB (736185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82f816f1f99571cd3f80c3a3a8156569b47350766e525e19e0fbe4bba948528`  
		Last Modified: Mon, 28 Sep 2026 18:10:07 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
