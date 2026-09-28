## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:8735543cf71147ce46f97293dc0c0b2eea3a755dc3f79f728cab042856691d80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:a55c30316a1d0f1ea5d4142348d15c0efbc6afacf4ea4e2df005f7bbcb47ab59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177626084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb347e1cb6e1635799b6f4103fea3b74625611853a1b1c8c96ec331c9f06e0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 18:09:37 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 28 Sep 2026 18:09:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 18:09:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 18:09:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 18:09:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 18:09:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 18:09:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 18:09:37 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 18:09:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 18:09:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 18:09:37 GMT
CMD ["mvn"]
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
	-	`sha256:dfd9593197d94d5e056ac98eff127706bca3fd19b6cfe4d05cf7497f8dc9da4d`  
		Last Modified: Mon, 28 Sep 2026 18:09:45 GMT  
		Size: 2.2 MB (2216683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b0973151cffa03f4f34ed5c000c385305eb5ee02faadf36a68291bfc41f38`  
		Last Modified: Mon, 28 Sep 2026 18:09:45 GMT  
		Size: 9.4 MB (9359976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f66005181296381fd6df52f8ed1e5677adf9405b3b03ac6a33c838f72d690da`  
		Last Modified: Mon, 28 Sep 2026 18:09:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65e4872385efedad262c146c0c58c027112d953f73175bc21c0d739eb78589c`  
		Last Modified: Mon, 28 Sep 2026 18:09:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:73fceb27cf24a1570f4e41729bfe9d4d80e3d6f20941b6aeb8fea5b949796d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d56be0578cb907cfef154be406d2587ca8dcf14f305605af6485719e96e89`

```dockerfile
```

-	Layers:
	-	`sha256:321fbed4a2b18b4d860a4fb54f92ecca88cac9cbde953dc13ea62fbfef962b64`  
		Last Modified: Mon, 28 Sep 2026 18:09:45 GMT  
		Size: 728.3 KB (728333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf82d653776a0e18b81c6735c96e25ea374528e5772c043dc4444493fe1637cf`  
		Last Modified: Mon, 28 Sep 2026 18:09:44 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5a9bf2558f7643ce780d7b6f74c7d54c41ac3b86372536f4ca314987f285a20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (176007737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79efde2e565c972c60351621967c79503c3d86c34d32250df5ea26ad9ddb3f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 28 Sep 2026 18:09:47 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 28 Sep 2026 18:09:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 28 Sep 2026 18:09:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 28 Sep 2026 18:09:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 28 Sep 2026 18:09:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Sep 2026 18:09:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Sep 2026 18:09:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Sep 2026 18:09:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Sep 2026 18:09:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Sep 2026 18:09:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Sep 2026 18:09:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Sep 2026 18:09:48 GMT
CMD ["mvn"]
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
	-	`sha256:9b093a0e60f66b9c4bbce4ee89810d346e673acec27d343c074d10d7ffaa136d`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 2.3 MB (2256127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbe261f890b0d78bbc99edbed9703271f67220e30e4b91f65bcf91b8b717373`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbc20a1d1def3334c07a4e3f657321e00f1a9bf65b9b88747eb438c7c2fb60`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826efbc39ff95062e8ddbf5b852a924c9d90f03d8b2c7392d4e09ce1fd9683f6`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:1fda5331de57cfe206f4aad03fd70b007905cdecdd5c49688992402b8e2b90bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.7 KB (741749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81792fe0d0960c3f4d9b6be0a77f2023a0c21a259c69fa9aa961f144289eece`

```dockerfile
```

-	Layers:
	-	`sha256:eb58272cda68ec4c95309e31b14107f39e66de0ffe84c171fc3028c61cc5c706`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 727.1 KB (727090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3cfb4d15a1c5cbbdeef889f62c20acbd318df83723ce97c09c2db12835688a`  
		Last Modified: Mon, 28 Sep 2026 18:09:55 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
