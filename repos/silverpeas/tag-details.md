<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.3`](#silverpeas643)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:fd45078184d97696ba802540a10984ee0f33811768d9b91ed127ae33cb62d4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:e7a04cad16471c8d8613e4f8b25fbd153c6a247d9b75dfb4fcca6acc8cb6b187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1776301272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b766de7acc9aac8e10a20ef903e6712e1e08627f9c1f2d1ec883185cd1b8070`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 07 Feb 2025 13:19:10 GMT
ARG RELEASE
# Fri, 07 Feb 2025 13:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 07 Feb 2025 13:19:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 07 Feb 2025 13:19:10 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 13:19:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 07 Feb 2025 13:19:10 GMT
ENV TERM=xterm
# Fri, 07 Feb 2025 13:19:10 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV PING_ON=1
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 07 Feb 2025 13:19:10 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 07 Feb 2025 13:19:10 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 07 Feb 2025 13:19:10 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Fri, 07 Feb 2025 13:19:10 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=1
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 07 Feb 2025 13:19:10 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 07 Feb 2025 13:19:10 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9d292ebf7d7c8cc8d916ae591cc751e95bd0687d30dd7f0eea47fd6041f5e`  
		Last Modified: Fri, 11 Apr 2025 17:25:25 GMT  
		Size: 762.6 MB (762649442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cd56b849084c23ce23abbe3580033492dc42c22e5bf517d1b38987fd4a7657`  
		Last Modified: Fri, 11 Apr 2025 17:25:14 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd98c7412b53373ca88561f2bf76bc58954699af6b45782635f05fe319605b9`  
		Last Modified: Fri, 11 Apr 2025 17:25:14 GMT  
		Size: 7.1 MB (7146628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a5f3aeb3268f18f674a6b18504342a2d89cd7cade4fd9f1240c0c95b20e16`  
		Last Modified: Fri, 11 Apr 2025 17:25:14 GMT  
		Size: 2.5 MB (2534359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87df7b140611c5d1cfe8079fac5709cf41acdbb712fabf1baa2d50411b5615be`  
		Last Modified: Fri, 11 Apr 2025 17:25:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e489e89ad46a882374d347f7e4f0010061795382bc08ca2f13fc4e23b4e2ca`  
		Last Modified: Fri, 11 Apr 2025 17:25:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302f3e1794e044a114aec8980fdd8871ddf3294a2dc1cf925016082c1a9df6cf`  
		Last Modified: Fri, 11 Apr 2025 17:25:19 GMT  
		Size: 217.8 MB (217843308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4b9338e2b65e0c770919df1c4a4dab6737a93bfcc6ef66f75048ff05a5803`  
		Last Modified: Fri, 11 Apr 2025 17:25:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770fde9ba44a2910c06b8a2038f1fb9a47db9bd28d9d1bab88ac188636a41346`  
		Last Modified: Fri, 11 Apr 2025 17:25:16 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bb8081ae57930ececc71b2172534a9f6987e082aa7718d6ec10cfab89b516b`  
		Last Modified: Fri, 11 Apr 2025 17:25:17 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79609d21a65916615a6a87834278155ab53a9f275cedc52cb8f8bc08617bb28b`  
		Last Modified: Fri, 11 Apr 2025 17:25:17 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a0fea8d28c71e93be2754405385abe66b692767fe832bd3868340829bdcdf6`  
		Last Modified: Fri, 11 Apr 2025 17:25:30 GMT  
		Size: 754.6 MB (754620360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:0f8837349af75ff3cf15728640721965008a8e9b572366f0354bd7b1128ba2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27780373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46640cdd9950a6e500571667b7695956337dab06d3caa7527faacecd0267d9a`

```dockerfile
```

-	Layers:
	-	`sha256:0c89231b91ab0ff439cabf53bf437864083f8b8fe28f78915bd542bda8d6f24d`  
		Last Modified: Fri, 11 Apr 2025 17:25:14 GMT  
		Size: 27.7 MB (27739630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee73558331b89d201c25c0c24dc2f133f6c43954ae0bbe042f085be6d9c1bddd`  
		Last Modified: Fri, 11 Apr 2025 17:25:13 GMT  
		Size: 40.7 KB (40743 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.3`

```console
$ docker pull silverpeas@sha256:9412fb59b5548607e9fe7b8e81985868b0c1ac9c646a68ee7145bf9a5b0fe6b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:5bae490ff0f6f29282cfcdcd09383644cea2344ed75b79634276cceb25b0e290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817817627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d9d8e4592a6f86b5a4df9b386e0fad363bf74c9385bd5ede84334d6a6beecc`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Apr 2025 14:37:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 11 Apr 2025 14:37:01 GMT
ENV TERM=xterm
# Fri, 11 Apr 2025 14:37:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV PING_ON=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_VERSION=6.4.3
# Fri, 11 Apr 2025 14:37:01 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL name=Silverpeas 6.4.3 description=Image to install and to run Silverpeas 6.4.3 vendor=Silverpeas version=6.4.3 build=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 11 Apr 2025 14:37:01 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a901e7cb887059f1766e39f06f9694912ee91cc4021290d5ecc981d1b8fbbee7`  
		Last Modified: Fri, 11 Apr 2025 17:09:07 GMT  
		Size: 494.7 MB (494718846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef057eb838d7e6def8048ab2768b5d298ec0e46f867d517c7be6bf7647cf5b`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 4.0 MB (3994010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d58aff9f75183113c2432b4fbd6e3ce7d834d9c0275293456d40e488013afe2`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 7.1 MB (7146621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb1cef44636769cd21aebdd8c1ab1053f26528e6309eff98aaf7325e0cbfed8`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 2.5 MB (2538617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274510b31519ce8cfa944ee04399481ab657db6335c1aca6a44154539d280ee`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b7d8927a617fd2311fcfbe31e8e87311f2793199dda98eeb4f3407659fcdaf`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b658fd616d12590448a861a3f9a8173e046dbdc15856c6a98c6e4fa24ad81c95`  
		Last Modified: Fri, 11 Apr 2025 17:09:05 GMT  
		Size: 269.1 MB (269106201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe0d5fdd75d222d21cca39057e98b1dd76aa00eb26cac30836a01762cfa4f8`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f0a1579513046f138f9b0f807250f6a170606cb5c174b3d9280ca832501adc`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faae1c62f38bb0be289352592253378cef6d0eeb8404e5abdb31c3e45e6ce6f`  
		Last Modified: Fri, 11 Apr 2025 17:09:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c106e9dd84bf822f89af616e634f65dfc8f82558cde885ca9801113f5129c0`  
		Last Modified: Fri, 11 Apr 2025 17:09:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30fc9a522d6f48f738f9072e190824d58d95184a013921a1dfd82845ee935a`  
		Last Modified: Fri, 11 Apr 2025 17:09:18 GMT  
		Size: 1.0 GB (1010777694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.3` - unknown; unknown

```console
$ docker pull silverpeas@sha256:b8ded1a0c47b4e424a911b42db8efec45b965fbb46df2ec556cd8637715ee8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38637b1c6bb5ebbc91f18e342570415c130bdc69dd1896462b82214d47c4b4c6`

```dockerfile
```

-	Layers:
	-	`sha256:8fe5d7ffef955ec7467c4c047551f526927d16a2db863b36629914a0fc6b2486`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 15.7 MB (15703985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383a09a10581be73495c9ecc8b3344746206f772fe4eff0ab791078a180de8dc`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:9412fb59b5548607e9fe7b8e81985868b0c1ac9c646a68ee7145bf9a5b0fe6b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:5bae490ff0f6f29282cfcdcd09383644cea2344ed75b79634276cceb25b0e290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817817627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d9d8e4592a6f86b5a4df9b386e0fad363bf74c9385bd5ede84334d6a6beecc`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Apr 2025 14:37:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 11 Apr 2025 14:37:01 GMT
ENV TERM=xterm
# Fri, 11 Apr 2025 14:37:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV PING_ON=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_VERSION=6.4.3
# Fri, 11 Apr 2025 14:37:01 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL name=Silverpeas 6.4.3 description=Image to install and to run Silverpeas 6.4.3 vendor=Silverpeas version=6.4.3 build=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 11 Apr 2025 14:37:01 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a901e7cb887059f1766e39f06f9694912ee91cc4021290d5ecc981d1b8fbbee7`  
		Last Modified: Fri, 11 Apr 2025 17:09:07 GMT  
		Size: 494.7 MB (494718846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef057eb838d7e6def8048ab2768b5d298ec0e46f867d517c7be6bf7647cf5b`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 4.0 MB (3994010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d58aff9f75183113c2432b4fbd6e3ce7d834d9c0275293456d40e488013afe2`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 7.1 MB (7146621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb1cef44636769cd21aebdd8c1ab1053f26528e6309eff98aaf7325e0cbfed8`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 2.5 MB (2538617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274510b31519ce8cfa944ee04399481ab657db6335c1aca6a44154539d280ee`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b7d8927a617fd2311fcfbe31e8e87311f2793199dda98eeb4f3407659fcdaf`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b658fd616d12590448a861a3f9a8173e046dbdc15856c6a98c6e4fa24ad81c95`  
		Last Modified: Fri, 11 Apr 2025 17:09:05 GMT  
		Size: 269.1 MB (269106201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe0d5fdd75d222d21cca39057e98b1dd76aa00eb26cac30836a01762cfa4f8`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f0a1579513046f138f9b0f807250f6a170606cb5c174b3d9280ca832501adc`  
		Last Modified: Fri, 11 Apr 2025 17:09:01 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faae1c62f38bb0be289352592253378cef6d0eeb8404e5abdb31c3e45e6ce6f`  
		Last Modified: Fri, 11 Apr 2025 17:09:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c106e9dd84bf822f89af616e634f65dfc8f82558cde885ca9801113f5129c0`  
		Last Modified: Fri, 11 Apr 2025 17:09:02 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30fc9a522d6f48f738f9072e190824d58d95184a013921a1dfd82845ee935a`  
		Last Modified: Fri, 11 Apr 2025 17:09:18 GMT  
		Size: 1.0 GB (1010777694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:b8ded1a0c47b4e424a911b42db8efec45b965fbb46df2ec556cd8637715ee8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38637b1c6bb5ebbc91f18e342570415c130bdc69dd1896462b82214d47c4b4c6`

```dockerfile
```

-	Layers:
	-	`sha256:8fe5d7ffef955ec7467c4c047551f526927d16a2db863b36629914a0fc6b2486`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 15.7 MB (15703985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383a09a10581be73495c9ecc8b3344746206f772fe4eff0ab791078a180de8dc`  
		Last Modified: Fri, 11 Apr 2025 17:09:00 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json
