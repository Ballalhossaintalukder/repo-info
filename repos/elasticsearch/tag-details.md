<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.22`](#elasticsearch81922)
-	[`elasticsearch:9.4.6`](#elasticsearch946)
-	[`elasticsearch:9.5.3`](#elasticsearch953)

## `elasticsearch:8.19.22`

```console
$ docker pull elasticsearch@sha256:d071f96fab6c11db8fbf8cd23ac296bf96fdb71f4b56c23b1b4da88c7057c991
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.22` - linux; amd64

```console
$ docker pull elasticsearch@sha256:1841fda6970f84073525a239179c3e129352de11eb56986074a3db1cd3301d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725408264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb399745e739c1994b9dad3a9b5559f420f7a5a5815919cb5458192ac8847eb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Wed, 23 Sep 2026 16:58:19 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 23 Sep 2026 16:58:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 23 Sep 2026 16:58:19 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 16:58:19 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 23 Sep 2026 16:59:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 16:59:14 GMT
ENV SHELL=/bin/bash
# Wed, 23 Sep 2026 16:59:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 23 Sep 2026 16:59:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 23 Sep 2026 16:59:14 GMT
LABEL org.label-schema.build-date=2026-09-18T10:10:07.018982263Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3b2a41103de35e0af4064d647974032fcc1bcde9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.22 org.opencontainers.image.created=2026-09-18T10:10:07.018982263Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3b2a41103de35e0af4064d647974032fcc1bcde9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.22
# Wed, 23 Sep 2026 16:59:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 23 Sep 2026 16:59:14 GMT
CMD ["eswrapper"]
# Wed, 23 Sep 2026 16:59:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a55029dfff8380214adc9b28e1e1a8aa4037e1778fc10bea025eb0f1a49d540`  
		Last Modified: Wed, 23 Sep 2026 17:00:06 GMT  
		Size: 6.9 MB (6871563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9857b496e248614d06a359046046a710c88ea006b828eae2e5dfc1938fdceace`  
		Last Modified: Wed, 23 Sep 2026 17:00:05 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0704c66e48f1cc70c044590278de33e4d3e051bf744029f37c654314bf4fe8b0`  
		Last Modified: Wed, 23 Sep 2026 17:00:26 GMT  
		Size: 688.5 MB (688496088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc173b856685369451186575a71be9d999d6d4a019e1517da906f902baa4a6`  
		Last Modified: Wed, 23 Sep 2026 17:00:05 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199e786a6640405c3927c9ab58986a159365994aed65fc6c196c376241a524d8`  
		Last Modified: Wed, 23 Sep 2026 17:00:07 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c375a1db484c443b46a44f45aa144ac6f25db2d3f6384084c0e41fe34f3f17c`  
		Last Modified: Wed, 23 Sep 2026 17:00:07 GMT  
		Size: 164.2 KB (164184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a5a64337f1183d7819e21475b935cdfb11af57fb4cb97b5a73435a15ce8926`  
		Last Modified: Wed, 23 Sep 2026 17:00:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad1a1ad516da0e072735f9de93f32a6431ae2544967320d6344003682a1a76`  
		Last Modified: Wed, 23 Sep 2026 17:00:10 GMT  
		Size: 97.1 KB (97100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.22` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4e865f9c1bafc3f0b2d08fc8110ed37cbed0827add6ad7eb683c4b50cbcd524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3223786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0960a5337196ac3a9641ade185c14161658cfa70f043bf6da6b1e76f61b130`

```dockerfile
```

-	Layers:
	-	`sha256:adaee96d258a30c29dcaba1dca2aa8d61e4d49d2999aeed20ff30c886f33b933`  
		Last Modified: Wed, 23 Sep 2026 17:00:05 GMT  
		Size: 3.2 MB (3186971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65dd430fdc6e14e6af8abf0211ee1f8d5b0981bf92b79ac18b1541c83dd4249a`  
		Last Modified: Wed, 23 Sep 2026 17:00:04 GMT  
		Size: 36.8 KB (36815 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.22` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b8c54cec6cfcde3c121d7aa1ab4cd2081a27607aedd5b05c37c5b9e28cd02711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573402696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9854de34303c24c3e02d9e2b30e6ae4fcc18a6f772bd6c8bb38c76adf49c2fa1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Wed, 23 Sep 2026 16:58:34 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 23 Sep 2026 16:58:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 23 Sep 2026 16:58:34 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 16:58:34 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 23 Sep 2026 16:59:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 16:59:12 GMT
ENV SHELL=/bin/bash
# Wed, 23 Sep 2026 16:59:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 23 Sep 2026 16:59:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 23 Sep 2026 16:59:12 GMT
LABEL org.label-schema.build-date=2026-09-18T10:10:07.018982263Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3b2a41103de35e0af4064d647974032fcc1bcde9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.22 org.opencontainers.image.created=2026-09-18T10:10:07.018982263Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3b2a41103de35e0af4064d647974032fcc1bcde9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.22
# Wed, 23 Sep 2026 16:59:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 23 Sep 2026 16:59:12 GMT
CMD ["eswrapper"]
# Wed, 23 Sep 2026 16:59:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578203ec482f38ad3b224c027db0549f8372a283a800d9aa6cefc8f1ffc0bc41`  
		Last Modified: Wed, 23 Sep 2026 16:59:52 GMT  
		Size: 6.8 MB (6831154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d085bc0da3b02f7cf0092c55217d75d0e4ca2a60b585bdff588bffd9abbaa5f`  
		Last Modified: Wed, 23 Sep 2026 16:59:51 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc846240fc76ba0f2d426d0b200288238c1a42ceea07889b1656dbcf951f9e6`  
		Last Modified: Wed, 23 Sep 2026 17:00:02 GMT  
		Size: 537.4 MB (537357392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165d772af50ec723b3ce3ef1946e3f17a79122db970c7aeab1b3e0beae5044d0`  
		Last Modified: Wed, 23 Sep 2026 16:59:52 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a3d9ca10bd849fd6e918f78f643489eaff44685c7c2dc0a183701a7918b754`  
		Last Modified: Wed, 23 Sep 2026 16:59:53 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116a667dc092f2f7fdbb62b7fbc23924f26c12b3bb385f9ae215af92ffcaef14`  
		Last Modified: Wed, 23 Sep 2026 16:59:53 GMT  
		Size: 160.7 KB (160688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ceb8d95c160b107af52eec832dd8d906cf8e9a6402a4a4158b4517e6a47b3c`  
		Last Modified: Wed, 23 Sep 2026 16:59:53 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a7fc71f0b6c68c0712b1cd310b296f14d2ea5fb667e09847174863d780af3`  
		Last Modified: Wed, 23 Sep 2026 16:59:54 GMT  
		Size: 97.1 KB (97099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.22` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:edfa7d51f3a58345e4856d5d8ab19e36e056ced0230e43890672e56aaff07020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3224402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ccb455b2c99b52ee5a7a328c5295b9f09eee27ebb78e4ae34ae45764f49eaa`

```dockerfile
```

-	Layers:
	-	`sha256:753e8bdd696ccb6454dc4e8296046dca572a04e476d76ba1c2767e65678ffbb7`  
		Last Modified: Wed, 23 Sep 2026 16:59:52 GMT  
		Size: 3.2 MB (3187384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d02058a86a815a5cf7c23a5e958eec5fd633351cca4f5092bcd58e47fe120a`  
		Last Modified: Wed, 23 Sep 2026 16:59:51 GMT  
		Size: 37.0 KB (37018 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.6`

```console
$ docker pull elasticsearch@sha256:84c19e9a0e048f6078d2427dc37ea8e8044950f0c68ed80b60ceb9d98c5fc023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:1308b63fa753c22aa70986c233b6273021f2b671d4c4985aa80b5d900162ed23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.9 MB (868949874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c13f923e778e044125bf9a02317c61e5cd30a76c3479a3eb97d341ef42b3f5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 29 Sep 2026 17:53:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 29 Sep 2026 17:55:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:55:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 17:55:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 29 Sep 2026 17:55:31 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 29 Sep 2026 17:55:31 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 29 Sep 2026 17:55:31 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:55:31 GMT
ENV SHELL=/bin/bash
# Tue, 29 Sep 2026 17:55:31 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:55:31 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 29 Sep 2026 17:55:31 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 29 Sep 2026 17:55:31 GMT
LABEL org.label-schema.build-date=2026-08-26T22:12:16.859701616Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=10011cbc74640115d0ffac0cef7c925aec4754f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-26T22:12:16.859701616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=10011cbc74640115d0ffac0cef7c925aec4754f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6
# Tue, 29 Sep 2026 17:55:31 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 29 Sep 2026 17:55:31 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 17:55:31 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:55:31 GMT
CMD ["eswrapper"]
# Tue, 29 Sep 2026 17:55:31 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011d766d3f79cd48843aae7a2488ce38942654f5cb91e49393ed701ac57702fd`  
		Last Modified: Tue, 29 Sep 2026 17:56:27 GMT  
		Size: 4.1 MB (4105768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c7641b8c795e854c956fb9e4e13a4b323cccf760028e66d3c09e1c3b493b7d`  
		Last Modified: Tue, 29 Sep 2026 17:56:27 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26a0824a8a3f62c9067dd9ebc7072fe6a7ba8f2f663c9ef3d31dc8068115545`  
		Last Modified: Tue, 29 Sep 2026 17:56:26 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b739502e9f006f83587b747c27749ad1f1fdb933231ae02ce73bade63e679fa`  
		Last Modified: Tue, 29 Sep 2026 17:56:41 GMT  
		Size: 824.0 MB (824016163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0925f965d0e25bdc1ab0dde14ec5d6978cf6b04a23ea41daa07a2dc2611fe3e`  
		Last Modified: Tue, 29 Sep 2026 17:56:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d50bf7f76b5ae1f101fa4f707bdc629d3b91586ae7ffebd50f6c4d3c042b11`  
		Last Modified: Tue, 29 Sep 2026 17:56:28 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca1a7019ca46385b837fda2ba2843610e15cbdd4cc13389fceffcab11ec1302`  
		Last Modified: Tue, 29 Sep 2026 17:56:28 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b76ffeeb9ebb5a380f5af8a5c904e72de06e5fa4dafe078a039aeacd3d1996`  
		Last Modified: Tue, 29 Sep 2026 17:56:29 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:59ebc924d8962d3da95e3f28cb6ac55b34d63f5288a811be2c2023085988dbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a3a3c5aff7638d68accdd025f1e18d775a660a6df3f42d4a07c3bcd58597b`

```dockerfile
```

-	Layers:
	-	`sha256:b37263c560c0b294706c15c0339ccc02b0b02d6cf04f8965d448bd23496d283b`  
		Last Modified: Tue, 29 Sep 2026 17:56:27 GMT  
		Size: 2.4 MB (2389013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f02be10b6e994dd6a666904a33bff4c8efd170d7daf4a1fd242cc9e569afbd`  
		Last Modified: Tue, 29 Sep 2026 17:56:27 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e54d2aab5dc72a6121c2692cf8cb094848f30236ee9032c70c6f3762306756fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.5 MB (713497700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d831c0067e6d1312e8a7366e15cdfbe0951a9bea770676a7c4a878b6d936916`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 29 Sep 2026 17:53:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:21 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 29 Sep 2026 17:54:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:54:40 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 17:54:40 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 29 Sep 2026 17:54:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 29 Sep 2026 17:54:47 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 29 Sep 2026 17:54:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:47 GMT
ENV SHELL=/bin/bash
# Tue, 29 Sep 2026 17:54:48 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:54:48 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 29 Sep 2026 17:54:48 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 29 Sep 2026 17:54:48 GMT
LABEL org.label-schema.build-date=2026-08-26T22:12:16.859701616Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=10011cbc74640115d0ffac0cef7c925aec4754f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-26T22:12:16.859701616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=10011cbc74640115d0ffac0cef7c925aec4754f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6
# Tue, 29 Sep 2026 17:54:48 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 29 Sep 2026 17:54:48 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 17:54:48 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:54:48 GMT
CMD ["eswrapper"]
# Tue, 29 Sep 2026 17:54:48 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ee3f79c83f9efe49c068127601145413f13b016faddee26533940b94c5ae3`  
		Last Modified: Tue, 29 Sep 2026 17:55:34 GMT  
		Size: 4.1 MB (4103862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f973a73ae94742a4ada677c02a9a6b00ad7ba300b8fd5ed43fb9febdcdeb46`  
		Last Modified: Tue, 29 Sep 2026 17:55:33 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3692165b1dc6f1b7bb0d712a037904749675cb8451177e6c9391616ccd011`  
		Last Modified: Tue, 29 Sep 2026 17:55:34 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef51f6e20de4b7d0925c303ff90c7a9036671ea6c73357773574785fa872cd`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 670.5 MB (670492687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f2f0ff14d951f375b8b2c6210e6fdffc4f0e31cf2fd012cd10adf7ed4291dd`  
		Last Modified: Tue, 29 Sep 2026 17:55:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca94e01101833f7d9ab331ef81498214155544096100e85f76883f80c59c20c`  
		Last Modified: Tue, 29 Sep 2026 17:55:35 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25097f3edcb3605e344d5e693d22a16ffd4051af7d817cb8a8e0f5374166147b`  
		Last Modified: Tue, 29 Sep 2026 17:55:35 GMT  
		Size: 74.1 KB (74103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dca3dc33b13d145c33fd24f2fa6fe8d38a62fd377e529239d237d52453836a`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c34812769747a335382fad0e70ec8d7bf1826e98e1a08e83a3dad42213a3f9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2421751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d6733d28c26e7e085d15fed2023968fba6e2a5be22fd50832cee06e1ab7c8e`

```dockerfile
```

-	Layers:
	-	`sha256:70a64078e48c5a4f26ef17e3b232d5c6ae200da91796cb004e2b1e93d99ebe4b`  
		Last Modified: Tue, 29 Sep 2026 17:55:34 GMT  
		Size: 2.4 MB (2387793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ebbbcabeafd5238411d5e7491145bfea3a976cf7ace205632865d87d5879933`  
		Last Modified: Tue, 29 Sep 2026 17:55:33 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.5.3`

```console
$ docker pull elasticsearch@sha256:2d19e09b145bca2de1572e79b67c2b6be494c4a9943e2ebcb1ce393e7964cc44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.5.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e54c206ed8f03c526b70144a76f5aee0ee25d13a3f606607868f092077493f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **894.6 MB (894639493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb6e076654c82a7125415b03cdba29306cadfd39611b0b9bbb29ab7bf2bdc44`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 29 Sep 2026 17:53:51 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 29 Sep 2026 17:54:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:54:38 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 17:54:38 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 29 Sep 2026 17:54:50 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:50 GMT
ENV SHELL=/bin/bash
# Tue, 29 Sep 2026 17:54:50 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 29 Sep 2026 17:54:50 GMT
LABEL org.label-schema.build-date=2026-09-01T16:11:59.322249404Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=367ec317ec5f668dd864d41be06052a567102fec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T16:11:59.322249404Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=367ec317ec5f668dd864d41be06052a567102fec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3
# Tue, 29 Sep 2026 17:54:50 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.5.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 29 Sep 2026 17:54:50 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:54:50 GMT
CMD ["eswrapper"]
# Tue, 29 Sep 2026 17:54:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ceb8ff89103d953085ca587925ef19c6539f6fc35d970f65249012e13821a`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 4.1 MB (4105772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0b8a698a7745a1be4ef9298947e8af7616ccafcb3151000185ad6fe34c0d38`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12455de95bbaf50ed1784096f8e744d5980447060f3b01580c7503ecbb9518`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd3570fc15254701a9524cf694ff8ea37cce5bb49e9224ea22becaf0daaecaf`  
		Last Modified: Tue, 29 Sep 2026 17:56:00 GMT  
		Size: 849.7 MB (849705780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c491e0f6a84ae729cd7758a2edb0a049e2591c4c6c89762481ce2939373d45f`  
		Last Modified: Tue, 29 Sep 2026 17:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebf63437a2d206c0b139408f420113aa30cbe0a09d7f25019ea8435a9c3e5fe`  
		Last Modified: Tue, 29 Sep 2026 17:55:47 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fd5ff7782f1fd5cdd48a10aa29d4edda95efca876820e349d0617375afc4b2`  
		Last Modified: Tue, 29 Sep 2026 17:55:47 GMT  
		Size: 75.2 KB (75186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6e7851b172847673382dabe04063afdfffe648ebb8f625e4ffef9acf80af4d`  
		Last Modified: Tue, 29 Sep 2026 17:55:38 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.5.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:eec84712a3f2afb788475e8ba8a4e310bec090cd2139379d4aa5465cdb965e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145e7c531c398e899e0404e1f8b598c061acad9502c2022f3a605887958146c`

```dockerfile
```

-	Layers:
	-	`sha256:86bee01e6d4c5b03c05e767680a146fbba5f54af88ecec53a88daf9e076adb34`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 2.4 MB (2442094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc29f9687b8fc3a2b5de7dd39086986d6d18f73de5e986c9c761792130ff957`  
		Last Modified: Tue, 29 Sep 2026 17:55:45 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.5.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8be242cf84998db563dd7fe29642d733dfe7d04917c6acf23d2b88574f8b1936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **739.1 MB (739116120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289e9d81ebacf59697e39e5ab4526469259a4c35b1f3576c7e018cb9494e3a76`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 29 Sep 2026 17:53:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:21 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 29 Sep 2026 17:54:41 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 17:54:41 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 17:54:42 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 29 Sep 2026 17:54:49 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 29 Sep 2026 17:54:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 29 Sep 2026 17:54:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:49 GMT
ENV SHELL=/bin/bash
# Tue, 29 Sep 2026 17:54:49 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:54:49 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 29 Sep 2026 17:54:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 29 Sep 2026 17:54:49 GMT
LABEL org.label-schema.build-date=2026-09-01T16:11:59.322249404Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=367ec317ec5f668dd864d41be06052a567102fec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T16:11:59.322249404Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=367ec317ec5f668dd864d41be06052a567102fec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3
# Tue, 29 Sep 2026 17:54:49 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.5.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 29 Sep 2026 17:54:50 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 17:54:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:54:50 GMT
CMD ["eswrapper"]
# Tue, 29 Sep 2026 17:54:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5533dc1bd46b23ef04f722bee9b935ec69fd5260b2972f9c51e8e0d5489ec014`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 4.1 MB (4103967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f973a73ae94742a4ada677c02a9a6b00ad7ba300b8fd5ed43fb9febdcdeb46`  
		Last Modified: Tue, 29 Sep 2026 17:55:33 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e0c9e4fadafa431f9eb2d7149a8d7ee8eba7837d62453c2813ce3d1a1df1a`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa3353cf5e21c84349ddede148eccde63590ef989968a87b199a9191794be36`  
		Last Modified: Tue, 29 Sep 2026 17:55:50 GMT  
		Size: 696.1 MB (696111009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10b000efc344a113a388ab5548a1ac3b212e5b8fb9e781d747454f7a7133eea`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a15ba316c00f9c32758e6445d471a6b35a637ee80f81b14f471f9e500f4e0f`  
		Last Modified: Tue, 29 Sep 2026 17:55:37 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248f82639c83ad7440841b5e9812254a75ec9a762a8ea920cbe28c2114eeb40`  
		Last Modified: Tue, 29 Sep 2026 17:55:37 GMT  
		Size: 74.1 KB (74101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6e7851b172847673382dabe04063afdfffe648ebb8f625e4ffef9acf80af4d`  
		Last Modified: Tue, 29 Sep 2026 17:55:38 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.5.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e4e09c5ec566ff1e19af2c487adf6c4c6bad2b4ec5eadd45194b06feb9692de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17245fb5776e1f24122d566bd322788d74f7ac4622ca1b5c2c1242e60f56a6a3`

```dockerfile
```

-	Layers:
	-	`sha256:49eeffcf5856f16549d0a3813d5a7445d4df5536ded0e593749ce7220ff3e0af`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 2.4 MB (2440874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ab2d6465defe3b94d83d34b91adc23591c6b29545d59abb25d006f6b81606c`  
		Last Modified: Tue, 29 Sep 2026 17:55:36 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
