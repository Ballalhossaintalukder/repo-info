<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.22`](#logstash81922)
-	[`logstash:9.4.6`](#logstash946)
-	[`logstash:9.5.3`](#logstash953)

## `logstash:8.19.22`

```console
$ docker pull logstash@sha256:fb58a8999d6f0b30e9125bd20ff112637b4ea444ca5dc9e514ea32d5eb972e02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.22` - linux; amd64

```console
$ docker pull logstash@sha256:b4296fd071691f79baa4de5c239cd8fc8730e56b5152f723a231cec85d6fe743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.0 MB (531013691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93099b7eab5c628b647cf3de08df3302cf49d396ab7b63cacd5ac66f9fb8f995`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Sep 2026 11:44:03 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:44:03 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:44:06 GMT
ADD file:43d479b270bbaf47965cfc86b37f4c517bda83ddefda6f708f98c3b2b7d15396 in / 
# Fri, 11 Sep 2026 11:44:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Sep 2026 16:59:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 23 Sep 2026 16:59:17 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 23 Sep 2026 16:59:38 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.22-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.22 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 23 Sep 2026 16:59:38 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Sep 2026 16:59:38 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 16:59:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 16:59:38 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 23 Sep 2026 16:59:38 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 23 Sep 2026 16:59:38 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Sep 2026 16:59:39 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 23 Sep 2026 16:59:39 GMT
USER 1000
# Wed, 23 Sep 2026 16:59:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 23 Sep 2026 16:59:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.22 org.opencontainers.image.version=8.19.22 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-09-18T17:29:07+00:00 org.opencontainers.image.created=2026-09-18T17:29:07+00:00
# Wed, 23 Sep 2026 16:59:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d13df5de6ae1ff0eff668f27e56a5d5c12c4fbc7e6c53782cbdee77b239c05`  
		Last Modified: Wed, 23 Sep 2026 17:00:15 GMT  
		Size: 50.0 MB (49979522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd64f64e0bec8cf621635f106f61a6dc6d3127bb63c21820eca73d486d543e6`  
		Last Modified: Wed, 23 Sep 2026 17:00:13 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b030ff8df38ab66b58e55c7c162068df6eacf2fdfd83502116e1844b1d59d1b`  
		Last Modified: Wed, 23 Sep 2026 17:00:21 GMT  
		Size: 451.0 MB (451002339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b52999974497b0f42e041f652f336899f7c94e21e8c5e089842f25c8c6a7`  
		Last Modified: Wed, 23 Sep 2026 17:00:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c52149ad3706a5a7ba6151e062059a045850a0ab1ba4200fed8739dc91f558`  
		Last Modified: Wed, 23 Sep 2026 17:00:14 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c389728fc1def34aa9371d5d1cbd737dba5582bd6eb3795b3702b213aec119ce`  
		Last Modified: Wed, 23 Sep 2026 17:00:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f4af3e355af09c1b48d74098ae5c7bbbb8cebcfc1ccaea85b2685ce19d1749`  
		Last Modified: Wed, 23 Sep 2026 17:00:16 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a0cf079e31e6c8fa9faa18777f5ce667c89cbaca1ae52cc195395ef43924be`  
		Last Modified: Wed, 23 Sep 2026 17:00:17 GMT  
		Size: 6.3 KB (6291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6919e91bd8320f74735698ea385e13122ec6a381c8d92c4eedf776583383e8b`  
		Last Modified: Wed, 23 Sep 2026 17:00:17 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2859f5f2714fc12a44b168188343488238ec295b5892b8a1d31e88af2da7cf`  
		Last Modified: Wed, 23 Sep 2026 17:00:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ca894abe64fd7871ae406e8d8ebb0135a03e0ab41bad795b460234cf679765`  
		Last Modified: Wed, 23 Sep 2026 17:00:18 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.22` - unknown; unknown

```console
$ docker pull logstash@sha256:7d639319eaa4d1c30f9c224f0a0177d38075d7ffe939525ac9be3ebe03e430c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3647143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4989193e576e1c9b34032208be2e5f2efb84d87a473c79012c88c21829f22523`

```dockerfile
```

-	Layers:
	-	`sha256:7aae0b5b39e54a3bd8b6973a6efe100a1fb66ea650bede4f157427301e306704`  
		Last Modified: Wed, 23 Sep 2026 17:00:13 GMT  
		Size: 3.6 MB (3611295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd72a775a763ce271f2362b993ec7c6c87f6aa4e2291b125451619805cceea5`  
		Last Modified: Wed, 23 Sep 2026 17:00:13 GMT  
		Size: 35.8 KB (35848 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.22` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:15c0729113ba8778039669d6a188afa9a90ee113e5fad25e1901f50b554869bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530415364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e7c21527ad931ed6c0f345795537ee2d0a0af900a950d1f2e7293eaa4ec398`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Sep 2026 11:53:33 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:53:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:53:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:53:37 GMT
ADD file:ff1ce8d2ee022926eb353ff9248358531fbe1661ef12d8784e68fbc52738ed34 in / 
# Fri, 11 Sep 2026 11:53:37 GMT
CMD ["/bin/bash"]
# Wed, 23 Sep 2026 16:59:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 23 Sep 2026 16:59:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.22-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.22 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Sep 2026 16:59:52 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 16:59:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 16:59:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Sep 2026 16:59:52 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 23 Sep 2026 16:59:52 GMT
USER 1000
# Wed, 23 Sep 2026 16:59:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 23 Sep 2026 16:59:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.22 org.opencontainers.image.version=8.19.22 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-09-18T17:29:07+00:00 org.opencontainers.image.created=2026-09-18T17:29:07+00:00
# Wed, 23 Sep 2026 16:59:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c650236275f3e15e02f7609b01f5b2c3c6c65c4c60fd53c987e8c0572a1da36`  
		Last Modified: Wed, 23 Sep 2026 17:00:35 GMT  
		Size: 51.9 MB (51906303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273e84ac78c16d8d9fdab0c0ca35327002983a4c38e6e85c8e1672da39be118`  
		Last Modified: Wed, 23 Sep 2026 17:00:32 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4d2c41583f3e067a021855027621e1235f6da7839534c95e00ea67df6d5f42`  
		Last Modified: Wed, 23 Sep 2026 17:00:49 GMT  
		Size: 449.3 MB (449299754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bdbd60907bbcfc29a48eef14e5b782d4f3d4b6e3ef456a04731319d9e9e182`  
		Last Modified: Wed, 23 Sep 2026 17:00:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44ddec6371790c7a7c89cd83d7839da36853051d8fcc7d158739711c51d9fec`  
		Last Modified: Wed, 23 Sep 2026 17:00:34 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5207f9c629467b518a848769f7f82075dec2958effc275418a093ee09261c`  
		Last Modified: Wed, 23 Sep 2026 17:00:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caca01d9e28144950343d9c415d21e7812a67afd0d5d717fc5086739174ac91`  
		Last Modified: Wed, 23 Sep 2026 17:00:35 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225bb2f216f431eed665a69b4964c701bf512a997ef1038d08edeb0c64ad75b1`  
		Last Modified: Wed, 23 Sep 2026 17:00:35 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd7be6f2adb846d8c82d7e970f36b5aeda01a9f2b131cecd50356747482d6f4`  
		Last Modified: Wed, 23 Sep 2026 17:00:36 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa572127d8b941064becb3770a719168cbc1d8eba856b2f458637c60cfd417a9`  
		Last Modified: Wed, 23 Sep 2026 17:00:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64036b378ead41c4241e672ec8eb87d49f394c3d1ac0476b83294d2f40037324`  
		Last Modified: Wed, 23 Sep 2026 17:00:37 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.22` - unknown; unknown

```console
$ docker pull logstash@sha256:c956799dfea1d1a8d3402c5e66a1fdba23ced99f9e3b805bd5032568ec055981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3647697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a7ff342adb79ab24bfa827e3524843aa1f1e1a246fd1f6bee4942fbef8646d`

```dockerfile
```

-	Layers:
	-	`sha256:f028f704028c12453ecd88cbd92e1e81a8f9dc73e0651de20827120d6e3bc241`  
		Last Modified: Wed, 23 Sep 2026 17:00:33 GMT  
		Size: 3.6 MB (3611720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef9857700a2566f99129962fae9e775cee60dfe06c0a195042c85b110ca776b`  
		Last Modified: Wed, 23 Sep 2026 17:00:32 GMT  
		Size: 36.0 KB (35977 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.6`

```console
$ docker pull logstash@sha256:c1becb3f85cbf33d1b5462623cdde29c7ea928b692c0568e3c52463a24385734
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.6` - linux; amd64

```console
$ docker pull logstash@sha256:a0b8ed86c2cac10e9ed742d589731edf8add4e72fed208f7f02591950da494f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.6 MB (526577206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4f38c19be2aea152d69dacf121087f43386eb9e2180e182173b06ff6c1f2a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:54:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:54:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 17:54:12 GMT
WORKDIR /usr/share
# Tue, 29 Sep 2026 17:54:14 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 29 Sep 2026 17:54:44 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:54:44 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Sep 2026 17:54:44 GMT
USER 1000
# Tue, 29 Sep 2026 17:54:44 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Sep 2026 17:54:44 GMT
LABEL org.label-schema.build-date=2026-08-24T15:51:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-24T15:51:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 29 Sep 2026 17:54:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bba90c648a84b499ffa65738ab3eb442c026ebbf351786eb5bf919a2acfa5`  
		Last Modified: Tue, 29 Sep 2026 17:55:23 GMT  
		Size: 4.8 MB (4768025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbda3e3a9657de94deb09bfd6b8471abab7af3f91755b4d55a133bb15c0e08c`  
		Last Modified: Tue, 29 Sep 2026 17:55:31 GMT  
		Size: 480.8 MB (480806395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa3c0f612039338a43873c663f9ab0160f86f03d8953e8bd03bc8cb66350cd`  
		Last Modified: Tue, 29 Sep 2026 17:55:23 GMT  
		Size: 6.4 KB (6365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e11118a24341488b5f0942beb0249e7ce5b30b2426f15ca2afbd8894558678`  
		Last Modified: Tue, 29 Sep 2026 17:55:23 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd4734bc163cc55b7405a5a525d86f128e6c77ff8f4d3f27f2648e8cd3be4be`  
		Last Modified: Tue, 29 Sep 2026 17:55:24 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4b731205e3281039388f1136fc55a63831f93c280db20ddcfce83477bbed9`  
		Last Modified: Tue, 29 Sep 2026 17:55:24 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555b118e8dbfef8353c2c023ac71db4605aa7e724550e0c9d2f8f17d192ec899`  
		Last Modified: Tue, 29 Sep 2026 17:55:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ec1a4187e744aeaf262f3e95e9a38a5129df915b8188879b063ce7ad131f9`  
		Last Modified: Tue, 29 Sep 2026 17:55:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322e6baf8863982685cb5a8fe9e61353fbb281eafda81c0a71803d2c8558a43`  
		Last Modified: Tue, 29 Sep 2026 17:55:25 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.6` - unknown; unknown

```console
$ docker pull logstash@sha256:61c73f855f892257adcf142068d26000027aab28c33d1f9190883a4d1c1726f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d6d5e7c7462cbbe1b541a6627fe609ba84a28baa77654af5de5f271eec71d4`

```dockerfile
```

-	Layers:
	-	`sha256:3956909a24dd2f6b9a003024441ef237de676ad9888ab5c17265e5b6da7d6ffc`  
		Last Modified: Tue, 29 Sep 2026 17:55:23 GMT  
		Size: 2.1 MB (2116751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c63fe9d2d30f71515badc8b0753e60b7d4040ec810badb0a05e06de9ef20dd`  
		Last Modified: Tue, 29 Sep 2026 17:55:22 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:510e82818cb64b20b63ff045fb2632f4e473924c3c7dbd5ebe664d8430d05fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.9 MB (522921491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e50cfea9d4289555407a4d2542ce4002df5be7e6cc6d5fada4754c07a91d1bb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:40:13 GMT
ENV container oci
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:26bad3d4d2596a56fa0052979d37eb15831e83f431a1beb342ce4d8a82c10ef9 in /      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:40:14 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /root/buildinfo/      
# Mon, 28 Sep 2026 00:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:39:53Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:39:53Z" "architecture"="aarch64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:39:53Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:53:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:53:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:40 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 17:53:40 GMT
WORKDIR /usr/share
# Tue, 29 Sep 2026 17:53:43 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:55:00 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Sep 2026 17:55:00 GMT
USER 1000
# Tue, 29 Sep 2026 17:55:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Sep 2026 17:55:00 GMT
LABEL org.label-schema.build-date=2026-08-24T15:51:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-24T15:51:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 29 Sep 2026 17:55:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e991a9df13ed4cd590c08fa1b132b2f33c6557741a4f2cb6cfcdf0e16b21cd`  
		Last Modified: Tue, 29 Sep 2026 17:55:39 GMT  
		Size: 4.8 MB (4758813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaec838f6e4485e9b1abf325b490d18d73197d4e649d8202de3dcb7623998490`  
		Last Modified: Tue, 29 Sep 2026 17:55:47 GMT  
		Size: 479.1 MB (479085173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92718e254d5abf1b892a3ad01d6160cadd412438a3b342bf29bb0f8a600c4986`  
		Last Modified: Tue, 29 Sep 2026 17:55:39 GMT  
		Size: 6.4 KB (6365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc735d71925f9e166feb8bbdad80ee754ba1e80d78926138ef701f5cafe6bded`  
		Last Modified: Tue, 29 Sep 2026 17:55:39 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3f870ca90bd478157c7b04f33519660a42bc574cbca5024f81ea07c5230b66`  
		Last Modified: Tue, 29 Sep 2026 17:55:40 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9bca9932e1987a75a8e37f037a1ea21d3c9a34450ccc61a6f31d79c727795`  
		Last Modified: Tue, 29 Sep 2026 17:55:40 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5a87216039182997dbd1f7cbfaa76427b393142f0f8a8e8aee003bf7022d3`  
		Last Modified: Tue, 29 Sep 2026 17:55:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670e33600d79825edf87f56bab22de98beffe3c3f00fe00fd7d85ea9715f07d`  
		Last Modified: Tue, 29 Sep 2026 17:55:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e67c579de959e5fd9a70905e3e8fc26a7466095defbf90aa430825f8caf26f1`  
		Last Modified: Tue, 29 Sep 2026 17:55:42 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.6` - unknown; unknown

```console
$ docker pull logstash@sha256:a2a980ca4badc6fb2b9b2943159df274c3b0e97e81711e9e1888cc629061c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce9c64a3057a6b23f82d01be6274f80cb08a0ecebd7575a1bd6102a321baa8a`

```dockerfile
```

-	Layers:
	-	`sha256:e3690ef7e58b695405a9d4d2b0e573728cdebfae0d09881af69b0e48309a1e7d`  
		Last Modified: Tue, 29 Sep 2026 17:55:39 GMT  
		Size: 2.1 MB (2115539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b21c06f794f7efbd143c839fdc6c5c239491e3fcd7b99b0cf5e577dd2f732e4`  
		Last Modified: Tue, 29 Sep 2026 17:55:39 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.5.3`

```console
$ docker pull logstash@sha256:e6b2959b8c87e9250e9d60f03e9ff322accc01b9f8632b12474d96925cbf9547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.5.3` - linux; amd64

```console
$ docker pull logstash@sha256:8f21e9b2545b0b343ae3866e3c54fdb930b6c28626833ce86cb0fcec89ba7d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.2 MB (536165910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dc96aa9291ecf8e33cf20dd1d669d79986bef8b3ededffdef163f6204dc630`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:54:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:54:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:25 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 17:54:25 GMT
WORKDIR /usr/share
# Tue, 29 Sep 2026 17:54:28 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.5.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.5.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 29 Sep 2026 17:55:27 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 29 Sep 2026 17:55:27 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 29 Sep 2026 17:55:27 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:55:27 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Sep 2026 17:55:27 GMT
USER 1000
# Tue, 29 Sep 2026 17:55:27 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Sep 2026 17:55:27 GMT
LABEL org.label-schema.build-date=2026-09-01T07:25:38+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T07:25:38+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 29 Sep 2026 17:55:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f8380f4c6aad3d74b32e0aebd38801fe80ccab96b940a316c8d5945a4d6aa`  
		Last Modified: Tue, 29 Sep 2026 17:56:03 GMT  
		Size: 4.8 MB (4768030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb1dfa2a9bda4304a965c49b45eaacb8eaaba8b7c278f9efd8e3ffe3e2ed28f`  
		Last Modified: Tue, 29 Sep 2026 17:56:12 GMT  
		Size: 490.4 MB (490394914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f74c1f29e0818d975b421290ada1a8b13224e0eb5c1d60aad0fb24b718479ec`  
		Last Modified: Tue, 29 Sep 2026 17:56:03 GMT  
		Size: 6.5 KB (6541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9327bb6181aa2bd565c6212de61354ac2153d24697bd2147e7bee3480ad89d`  
		Last Modified: Tue, 29 Sep 2026 17:56:03 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d6cf00a5a89a418cf56399a0cce6804055f8a3182c3c0d380650af6f838da0`  
		Last Modified: Tue, 29 Sep 2026 17:56:04 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b525af4064f0baf6bf09b31e551ae939a60f45b38d2ba7004348858b93495ef2`  
		Last Modified: Tue, 29 Sep 2026 17:56:04 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4cb9fcf645589e4509e205fb09006666b645d38b589ebfd2cc7cd644ff0ab`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe9a475e1df197780d2499b5ead0fef03e3cbbac9d136e0bef923206d8e9063`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822131ed7d5c9129b98e34db1dfdfef882a20496279930e46ad4fc6930054f95`  
		Last Modified: Tue, 29 Sep 2026 17:56:06 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.5.3` - unknown; unknown

```console
$ docker pull logstash@sha256:b69410a878d088c9db93de8a017d1fc4590e774808104b9e6da7052ff4d3e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b658048cd3bd4934b3fb91862492d24dd7e6429a20966a74d046ff9c46bf72d`

```dockerfile
```

-	Layers:
	-	`sha256:017e74e107da11e7de3149fc509ff2e98db845bfee1019657816ea1e9bd7a182`  
		Last Modified: Tue, 29 Sep 2026 17:56:03 GMT  
		Size: 2.1 MB (2144055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5e127edc2b277c04a5acff05b5fcae28fd1ce50cb94e638ed4c8c66b479e235`  
		Last Modified: Tue, 29 Sep 2026 17:56:03 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.5.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:6f43fccf4a25c3708f37b167f27f311af7322a4aa87979eba63cc8bf140469f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.5 MB (532494953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67643384cc83db40d21364d1b445b586b6993226c9b8668fbdb50d5ad1d162b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:40:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:40:13 GMT
ENV container oci
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:26bad3d4d2596a56fa0052979d37eb15831e83f431a1beb342ce4d8a82c10ef9 in /      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:40:14 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:40:14 GMT
COPY dir:adb47cddc344477b2a7b51aafbccce71f4da707d0f84c107b6a4bb1f2e37571a in /root/buildinfo/      
# Mon, 28 Sep 2026 00:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:39:53Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:39:53Z" "architecture"="aarch64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:39:53Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:53:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:53:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:53:43 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 17:53:43 GMT
WORKDIR /usr/share
# Tue, 29 Sep 2026 17:53:46 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.5.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.5.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:54:16 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Sep 2026 17:54:16 GMT
USER 1000
# Tue, 29 Sep 2026 17:54:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Sep 2026 17:54:16 GMT
LABEL org.label-schema.build-date=2026-09-01T07:25:38+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T07:25:38+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 29 Sep 2026 17:54:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f43882da3b6381cda08faf5d280977980fd354bcf6e75def8db3f6a6c1631b`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 4.8 MB (4758834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175c07ad3d96e944d8a6320ae3beb58d954632e59cc5b99d0531e0830b01844`  
		Last Modified: Tue, 29 Sep 2026 17:55:05 GMT  
		Size: 488.7 MB (488658433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f18d90896916d1047a5eded4c53c6fef981b47ce508bd175680c72a33a1c`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 6.5 KB (6542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3c00a908b3326a20a2c7897f87295e25ee74141b66c99ce2ab2cb29b461f56`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ecc3c84e52c51b5fc9d69f8b40dcae02e639d78df81417012afafc1c0f104a`  
		Last Modified: Tue, 29 Sep 2026 17:54:57 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818a52d3776ebda09b8caa47d94af40b7e754349e706d67f0efd3747a24d88e8`  
		Last Modified: Tue, 29 Sep 2026 17:54:57 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d441b9d9cdeb78334df9f6aa7399ecc58a7166b0133f208ab3b246c59a20d`  
		Last Modified: Tue, 29 Sep 2026 17:54:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e940b4d9df06236164b85564d4ae3d3893d681dfe9a9dacc971a5484c03cabb`  
		Last Modified: Tue, 29 Sep 2026 17:54:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bde2e583d0e3d40a9e0b57b815ac3a7308e791206753318ae5358ec0596e3f`  
		Last Modified: Tue, 29 Sep 2026 17:54:58 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.5.3` - unknown; unknown

```console
$ docker pull logstash@sha256:3a0ee39df94fc6db1dfd1d9ff895b709a77d7c50b9aadee2829bacb7ab422edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fbbe47d2c80297c36236429d9b9ffd980e7c375cacb6b641d22bf91f87ccbf`

```dockerfile
```

-	Layers:
	-	`sha256:b0fd5ba69d5e8b020cbee28967502b9957492bc7dfbe2687d09afc0cedbe9793`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 2.1 MB (2142843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e18fc93c43ff5ac6873a59d7db0d55bc2f0171d0bedcc02deb25c364236ac0`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
