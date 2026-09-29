<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.22`](#kibana81922)
-	[`kibana:9.4.6`](#kibana946)
-	[`kibana:9.5.3`](#kibana953)

## `kibana:8.19.22`

```console
$ docker pull kibana@sha256:35544f1ff28abc0ec3547ca0e81089f2e1640f0f5c6c657fd39f921c217673a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.22` - linux; amd64

```console
$ docker pull kibana@sha256:58027b66e2bce45fbbd038fe91bd39450594259446fff97bc41fdf3bb9e46505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595774732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09fa15f2170c3e61ed01cc412799aa66401250eefcd098853be5bd45fb20ccc`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 23 Sep 2026 16:59:08 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 23 Sep 2026 16:59:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Sep 2026 17:12:42 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 23 Sep 2026 17:12:42 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 23 Sep 2026 17:12:42 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 23 Sep 2026 17:12:43 GMT
RUN fc-cache -v # buildkit
# Wed, 23 Sep 2026 17:12:43 GMT
WORKDIR /usr/share/kibana
# Wed, 23 Sep 2026 17:12:43 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 23 Sep 2026 17:12:43 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 17:12:43 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 17:12:43 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 23 Sep 2026 17:12:43 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 23 Sep 2026 17:12:44 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 23 Sep 2026 17:12:45 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 23 Sep 2026 17:12:45 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 23 Sep 2026 17:12:45 GMT
LABEL org.label-schema.build-date=2026-09-18T12:10:48.807Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=fd8e6f336cd7a18d0fd805de4608e1e38e0da163 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.22 org.opencontainers.image.created=2026-09-18T12:10:48.807Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=fd8e6f336cd7a18d0fd805de4608e1e38e0da163 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.22
# Wed, 23 Sep 2026 17:12:45 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 23 Sep 2026 17:12:45 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 23 Sep 2026 17:12:45 GMT
USER 1000
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb928839cbb23f3ce5746513ea012bf8d049eb717eb30c60769d6ab68e78114`  
		Last Modified: Wed, 23 Sep 2026 17:14:06 GMT  
		Size: 9.4 MB (9410140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c262190f5e5f7431ae79bb3bab4e1720ab88443433b5d1135add61f05e4848`  
		Last Modified: Wed, 23 Sep 2026 17:14:16 GMT  
		Size: 540.0 MB (539956498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae50bbef001406511f9df082469e08441b242a14a7464148d057d0b02baa188`  
		Last Modified: Wed, 23 Sep 2026 17:14:05 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493ae575cb101bf3dfa81055a4feb368bc238a63280b00b53e67daf5c85314d`  
		Last Modified: Wed, 23 Sep 2026 17:14:07 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d78c8e75a6ae5e0599451b37da9da5b0d9b7c2cbc8e3bd45a4b0f0a3453e63`  
		Last Modified: Wed, 23 Sep 2026 17:14:07 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfde8880478fb99729cb07e3547fe8c3428e5ab8baafdea0463522141c48ad0`  
		Last Modified: Wed, 23 Sep 2026 17:14:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579aebeef798654faf5fc13dc79b281ceec612c50dcb7b2b2fd492f6b2b2a7a6`  
		Last Modified: Wed, 23 Sep 2026 17:14:08 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb44c6465f8421ec2288fac471476b4e144b945870f1a3c0d53c27a8a8f07f7`  
		Last Modified: Wed, 23 Sep 2026 17:14:08 GMT  
		Size: 4.8 KB (4820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2444486a3fb980bbdbd8879489e9b53a2497651cca70d87db38151ae30f17540`  
		Last Modified: Wed, 23 Sep 2026 17:14:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8312f51ddbc28f13a3633fe25c61b550df3d2474a78f23fe3327a85e1d12242`  
		Last Modified: Wed, 23 Sep 2026 17:14:09 GMT  
		Size: 161.7 KB (161735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0543c77cc4f5838e0e808899ffdd7ed2019cc466045e5f2651950c5c9f78ec`  
		Last Modified: Wed, 23 Sep 2026 17:14:09 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.22` - unknown; unknown

```console
$ docker pull kibana@sha256:b2fff67cae52d9ae16a3a6237614c35c9194c88f43438c5255c41a5123aa5607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4856847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33203d5e18a24f162989787a6e56a394df60f403af39f1d1aa6a41945e4d307`

```dockerfile
```

-	Layers:
	-	`sha256:13dd58a2cc117a88eb1ba5ada01ef209754895243a2f14a090903169a29a0419`  
		Last Modified: Wed, 23 Sep 2026 17:14:06 GMT  
		Size: 4.8 MB (4815932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8d3d9892cb8a561e3d81b5a8abbab9f566083bc386eb1364eb0fa3ea33b4c3`  
		Last Modified: Wed, 23 Sep 2026 17:14:05 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.22` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9124a8214c6d41cb82929db4b11a7d71b35ffe8347e5f6235cbfdb7789499101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.4 MB (608448516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db0c07034039b4860676f6b778d7ec88d6534cd0163d53268ce6f10be25ab17`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 23 Sep 2026 16:59:27 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 23 Sep 2026 16:59:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Sep 2026 17:10:03 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
RUN fc-cache -v # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
WORKDIR /usr/share/kibana
# Wed, 23 Sep 2026 17:10:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Sep 2026 17:10:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Sep 2026 17:10:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 23 Sep 2026 17:10:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 23 Sep 2026 17:10:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 23 Sep 2026 17:10:07 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 23 Sep 2026 17:10:07 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 23 Sep 2026 17:10:07 GMT
LABEL org.label-schema.build-date=2026-09-18T12:10:48.807Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=fd8e6f336cd7a18d0fd805de4608e1e38e0da163 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.22 org.opencontainers.image.created=2026-09-18T12:10:48.807Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=fd8e6f336cd7a18d0fd805de4608e1e38e0da163 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.22
# Wed, 23 Sep 2026 17:10:07 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 23 Sep 2026 17:10:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 23 Sep 2026 17:10:07 GMT
USER 1000
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6230dab5ce0cb59eb6e65408abac252df54242700640ec205998ddee9475`  
		Last Modified: Wed, 23 Sep 2026 17:11:42 GMT  
		Size: 9.4 MB (9431204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cabcb87fcf2842ee5850937f8b53942793a82669f47aa625ca7379c1b7fd8c6`  
		Last Modified: Wed, 23 Sep 2026 17:11:52 GMT  
		Size: 553.4 MB (553435646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41469c368cbb24fd9c36d7b552a5078b7dc41517dd0051957372c1560a0bbd`  
		Last Modified: Wed, 23 Sep 2026 17:11:41 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3c65497dda25d0c03f3fe0a37dcc9ff44bec25966fa8c5e264832b71f01e7`  
		Last Modified: Wed, 23 Sep 2026 17:11:42 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda3e09911518a460c9ae62a3c3ab6f65993f001dfe34833ef5f53d149ede0ec`  
		Last Modified: Wed, 23 Sep 2026 17:11:42 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f6deba96718caada8a2c4da273724a6d7c8bb425fc4b7c885b38d603a0969`  
		Last Modified: Wed, 23 Sep 2026 17:11:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d74b29431b48e793069d9b9b52b3de880895152cf0dcd6bddb10df399e221d`  
		Last Modified: Wed, 23 Sep 2026 17:11:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee66c972eb3b573ab2338a9cad35e7ad1f0fcddae2052f5260ef37ebe6cee0e`  
		Last Modified: Wed, 23 Sep 2026 17:11:44 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c4520e6a62868549e2c9fc1eac387e5c51156e9e84ce7fb1287d0551a417d`  
		Last Modified: Wed, 23 Sep 2026 17:11:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d4e5ca677cc4fcd6d607df39788cb844773285304af01fd62640faffc402d`  
		Last Modified: Wed, 23 Sep 2026 17:11:45 GMT  
		Size: 158.3 KB (158253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ae8320375adafb5af0e64cf06f31ce924521b8dcc3ba3c7adf3e199d5581c`  
		Last Modified: Wed, 23 Sep 2026 17:11:45 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.22` - unknown; unknown

```console
$ docker pull kibana@sha256:50b2a7bff21ffcc0c655a2025714eac661fd918668b9e0aa7f51caa112e5c058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4858159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af4c7adb7693673f80f9c980fdc18d8069ae7018dd343d1f63d253cf4e13776`

```dockerfile
```

-	Layers:
	-	`sha256:c018f250dd39d0757c7752b410e604626184afdc7d57cce2b63cd54d9f9c0c7a`  
		Last Modified: Wed, 23 Sep 2026 17:11:42 GMT  
		Size: 4.8 MB (4816996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e64dd34fc09fee31105207cf5307e9d41e1be906f645a3835ffd411eb5affa5`  
		Last Modified: Wed, 23 Sep 2026 17:11:41 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.6`

```console
$ docker pull kibana@sha256:7942efa58fe6ca5dabfc4dfe3603cb9a4ebcf9c5850833d514b9ece2b4070417
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.6` - linux; amd64

```console
$ docker pull kibana@sha256:5dcae40d8918b2fb4142b278ed0737d08da975432b9eaeea67750c89adc9cef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.8 MB (565846191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7933e854a985c69e52537816bd7b775c2bda2332a0b88223cc740902408b9c14`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 29 Sep 2026 17:54:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 29 Sep 2026 17:54:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:03:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
RUN fc-cache -v # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
WORKDIR /usr/share/kibana
# Tue, 29 Sep 2026 18:03:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 18:03:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:03:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 29 Sep 2026 18:03:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:03:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 29 Sep 2026 18:03:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 29 Sep 2026 18:03:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 29 Sep 2026 18:03:57 GMT
LABEL org.label-schema.build-date=2026-08-26T20:30:47.515Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=692551ad493ed71169e295e2160446428ee00b15 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-26T20:30:47.515Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=692551ad493ed71169e295e2160446428ee00b15 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6
# Tue, 29 Sep 2026 18:03:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 29 Sep 2026 18:03:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 18:03:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 29 Sep 2026 18:03:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 29 Sep 2026 18:03:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd27c4902d47e51ba5c33d37f392d021cf6c2ac45e0aa69bdda3e6a95d133d55`  
		Last Modified: Tue, 29 Sep 2026 18:05:08 GMT  
		Size: 19.3 MB (19315600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee51433d4617dfe107f271ef22a519da544aef7f4fc1416e301df4aaf5b4e9`  
		Last Modified: Tue, 29 Sep 2026 18:05:15 GMT  
		Size: 489.2 MB (489234175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b18b38f313f1053f7a8bdd6493d20e43818bfc81b00fb15f817e4607457f1df`  
		Last Modified: Tue, 29 Sep 2026 18:05:08 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113d91bc1e40d94ae1ecd23866c5baac414860296f6a9f290488d3976fd37fc7`  
		Last Modified: Tue, 29 Sep 2026 18:05:07 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7357bcdce01bdf236a499777a295a2e2ee64933e32f422718b368b4128a60c69`  
		Last Modified: Tue, 29 Sep 2026 18:05:09 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b18502dd65770f1bb77de9e3603130bcf5f235d31254a05166339241a61b89`  
		Last Modified: Tue, 29 Sep 2026 18:05:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b676309efb95fb48973e0c4232a22d81be8d3e8e093f36d51a51ad7e7215d9`  
		Last Modified: Tue, 29 Sep 2026 18:05:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b9992f0c9c0ab402b817dfba77b498249810cc48fec029080d2513b979328`  
		Last Modified: Tue, 29 Sep 2026 18:05:11 GMT  
		Size: 4.9 KB (4927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73a472ff18766ad85c07793dffa0e53f89035883bb928cf21bad24f82ec650f`  
		Last Modified: Tue, 29 Sep 2026 18:05:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a6899a97fdef2c7b878e1219351ff0a955cf984d3f6e1c8397f2cb7dcdb39`  
		Last Modified: Tue, 29 Sep 2026 18:05:12 GMT  
		Size: 74.5 KB (74545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7ac54c69679c5847ddb43274826055babab058ec7055b58acf787341d9a50b`  
		Last Modified: Tue, 29 Sep 2026 18:05:12 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a71c7747eb2ec904bb2841267737928effad99f94217e933a116f8343b9388`  
		Last Modified: Tue, 29 Sep 2026 18:05:13 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.6` - unknown; unknown

```console
$ docker pull kibana@sha256:52d36015eafdceaffc08a240bc6b21869e30dc124ab15944a3458e62cef868c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5949496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced9439a868dc7cb1d8fec9e1b675b76538015967f3195ffd0eb93182b6b520`

```dockerfile
```

-	Layers:
	-	`sha256:51979199d6986146b44c4b898cb9f24a332356e9aced64e9e16f8b0099d61d6f`  
		Last Modified: Tue, 29 Sep 2026 18:05:07 GMT  
		Size: 5.9 MB (5906270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2a44b64acb4916cd335f844dfc18b8cf7a72fe7af32119c53a30462439f94c`  
		Last Modified: Tue, 29 Sep 2026 18:05:06 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8f15f774df6ce8f37252a707be84aadef7595214896385cab7c1426dd0ef482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.3 MB (577349310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389cb64e0b16d8fbfe43a348e55425194d12eb357a778532fdb4b35a2fac4e2c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 29 Sep 2026 17:53:32 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 29 Sep 2026 17:53:32 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:01:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
RUN fc-cache -v # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
WORKDIR /usr/share/kibana
# Tue, 29 Sep 2026 18:01:28 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 18:01:28 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:01:28 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 29 Sep 2026 18:01:28 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:01:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 29 Sep 2026 18:01:30 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 29 Sep 2026 18:01:30 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 29 Sep 2026 18:01:30 GMT
LABEL org.label-schema.build-date=2026-08-26T20:30:47.515Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=692551ad493ed71169e295e2160446428ee00b15 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.6 org.opencontainers.image.created=2026-08-26T20:30:47.515Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=692551ad493ed71169e295e2160446428ee00b15 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.6
# Tue, 29 Sep 2026 18:01:30 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 29 Sep 2026 18:01:30 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 18:01:30 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 29 Sep 2026 18:01:30 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 29 Sep 2026 18:01:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e027723bd56e0f66789ead024e6e733e125fff482553acb879fdb15f3f0838b`  
		Last Modified: Tue, 29 Sep 2026 18:02:56 GMT  
		Size: 19.3 MB (19258083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0ba87d432790cb8056154703e48d551e0ddc8cce3eb743c2bc5510e83be797`  
		Last Modified: Tue, 29 Sep 2026 18:03:05 GMT  
		Size: 502.7 MB (502721626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fd49bb8aa5a3c10d8b4454cb04c8bd8e556c2640a69059f5f3c00d659cfc8d`  
		Last Modified: Tue, 29 Sep 2026 18:02:55 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef665e53fd707bcfc911d1d94f93cbf2d8c8a63732b9a97f851cc987245644d4`  
		Last Modified: Tue, 29 Sep 2026 18:02:56 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98998a739134907c2a8b7828bf6d3e5c36d93ba2306bb5838eda57a7daeabffe`  
		Last Modified: Tue, 29 Sep 2026 18:02:56 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc9be0e8b2beb6979246220454140a533a8d66081f1f5721a055c4cb3fe8ff`  
		Last Modified: Tue, 29 Sep 2026 18:02:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa43a591f13d77782dcee9ce81612792d52c11f6cad075d3af79ad975acb551`  
		Last Modified: Tue, 29 Sep 2026 18:02:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195f2aa15872dd6368649195dd1f36ba3da16286034612cdcbb1d45570c5e4a5`  
		Last Modified: Tue, 29 Sep 2026 18:02:58 GMT  
		Size: 4.9 KB (4924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57653fc197a002a45a152d059c70a7ac218f19339283df669596648399a79d`  
		Last Modified: Tue, 29 Sep 2026 18:02:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b76b69a109fd7854e3014660f88f563dd125e9d3e0a4ea9cf8afcc70e2cd56`  
		Last Modified: Tue, 29 Sep 2026 18:02:59 GMT  
		Size: 73.5 KB (73454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46302f34b81a5bc5887f4b6ddeada064f4e1fd99f25639537dfdace77889532d`  
		Last Modified: Tue, 29 Sep 2026 18:02:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7661b7b0732c8481ff9a833db028951f8803710a45ad58338ead9a25d69c23d`  
		Last Modified: Tue, 29 Sep 2026 18:03:00 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.6` - unknown; unknown

```console
$ docker pull kibana@sha256:8c4b0895e0d5a9bd84bdea5bd05d6c3a076c9c207a964d34056d1f8c0ff97dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdac1f3b3558085d27ff1746bfa18826b4f042e59d8a0ddf2695549cdac915b`

```dockerfile
```

-	Layers:
	-	`sha256:2542ea55fe47512e3955a59419450ae916c1e217b26be76038d8ac656af0ee42`  
		Last Modified: Tue, 29 Sep 2026 18:02:55 GMT  
		Size: 5.9 MB (5903160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722aaed26f39f6e1b953e9f18b514aee699e7bc85092be3258607bc4813e4ca6`  
		Last Modified: Tue, 29 Sep 2026 18:02:55 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.5.3`

```console
$ docker pull kibana@sha256:75d0ce6d1d179063267dd7cd158beffa75ced49303349ed938f99636c05bd07e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.5.3` - linux; amd64

```console
$ docker pull kibana@sha256:f612b274447de51e8fec7072f0f2fe3901849e4390530020fa72b7d1ebcd641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.9 MB (560852506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1072381cf69ac480699588276690fe4c1acea2a63cac510e6faf1feb3a3093b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 29 Sep 2026 17:54:17 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 29 Sep 2026 17:54:17 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:03:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
RUN fc-cache -v # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
WORKDIR /usr/share/kibana
# Tue, 29 Sep 2026 18:03:23 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 18:03:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:03:23 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 29 Sep 2026 18:03:23 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:03:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 29 Sep 2026 18:03:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 29 Sep 2026 18:03:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 29 Sep 2026 18:03:25 GMT
LABEL org.label-schema.build-date=2026-09-01T14:33:18.580Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2169f1de4c917fce03905cc3110f3f523e2184d2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T14:33:18.580Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2169f1de4c917fce03905cc3110f3f523e2184d2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3
# Tue, 29 Sep 2026 18:03:25 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.5.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 29 Sep 2026 18:03:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 18:03:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 29 Sep 2026 18:03:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 29 Sep 2026 18:03:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b975988476af2735f98dbd09a463d18ac23671c2bf6d68d28fffe44e5ff80ea8`  
		Last Modified: Tue, 29 Sep 2026 18:04:41 GMT  
		Size: 19.3 MB (19315717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df35ea4cde18449dc678c7cfd4f4f9383589ea72d3b047509ce23d9ecc04b8`  
		Last Modified: Tue, 29 Sep 2026 18:04:50 GMT  
		Size: 484.2 MB (484240312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4b4275b3695c80a2630713cbe6647ed5974d6f7530c4f62a05c14c364655e`  
		Last Modified: Tue, 29 Sep 2026 18:04:40 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524383e2ed8bf56b7954e2381a31809a900102411b881fef78e0cd01497ed56f`  
		Last Modified: Tue, 29 Sep 2026 18:04:41 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5020fee3f1c0a48ed82f959674beb6885412780e937b5505cd680d674eb8078e`  
		Last Modified: Tue, 29 Sep 2026 18:04:41 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1265cb30d9eed99c3dfbe3992f89ea1c5ac1b13fcefa08eede07922612f0be5c`  
		Last Modified: Tue, 29 Sep 2026 18:04:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977c647e1af2404bf98124851e5172401e2727e80974f1ff22f10318c0bfce5a`  
		Last Modified: Tue, 29 Sep 2026 18:04:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ce8e4f15c65261dc5289d61f9afccb54cefdf1193c8b8f0c112538076f5058`  
		Last Modified: Tue, 29 Sep 2026 18:04:43 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712fcb16c702f4e6cb49a88900374d0bde5510c14feb2b3047c14d44da3ef9f5`  
		Last Modified: Tue, 29 Sep 2026 18:04:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d169af3c53b1d3f2e41e75c61c6b31a97eca207016fc8faa347be612d137a5b`  
		Last Modified: Tue, 29 Sep 2026 18:04:44 GMT  
		Size: 74.5 KB (74546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52eb4aab3c158be2397e6f6f27f9fd04365a8207f18c134470f455628e140a38`  
		Last Modified: Tue, 29 Sep 2026 18:04:44 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66f07f03ae230f79523b6a6665a0b0889d1c07c449f5ccb33e904708cdbc06a`  
		Last Modified: Tue, 29 Sep 2026 18:04:46 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.5.3` - unknown; unknown

```console
$ docker pull kibana@sha256:86e3a31db19b3d7939050c64bd93d53f03120d3eefabf81710272a92b34c5017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6141072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ef3c194a4639b4ce4f9abc4f4e88c20a3117a431d37eaeaf6700b6de46063a`

```dockerfile
```

-	Layers:
	-	`sha256:30dbe345b141a1181a0ea5dec89767b88816fa333a5d215396cc0eedb2436ba5`  
		Last Modified: Tue, 29 Sep 2026 18:04:41 GMT  
		Size: 6.1 MB (6097846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91794e62d5c0988125523f92037ab1903b85047a8e55a6d01f5e0e60c65aa532`  
		Last Modified: Tue, 29 Sep 2026 18:04:40 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.5.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:821e91cbea5fea73a47875d816bac2385c0de5719dec108baae9972f93781dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.3 MB (572341819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bba518c37bd9207e444b761429795341b16bae77555a128a3828d0901ad8d7a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 29 Sep 2026 17:53:45 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 29 Sep 2026 17:53:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:01:00 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 29 Sep 2026 18:01:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 29 Sep 2026 18:01:00 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 29 Sep 2026 18:01:01 GMT
RUN fc-cache -v # buildkit
# Tue, 29 Sep 2026 18:01:01 GMT
WORKDIR /usr/share/kibana
# Tue, 29 Sep 2026 18:01:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 29 Sep 2026 18:01:01 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Sep 2026 18:01:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:01:01 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 29 Sep 2026 18:01:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:01:02 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
LABEL org.label-schema.build-date=2026-09-01T14:33:18.580Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2169f1de4c917fce03905cc3110f3f523e2184d2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.5.3 org.opencontainers.image.created=2026-09-01T14:33:18.580Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2169f1de4c917fce03905cc3110f3f523e2184d2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.5.3
# Tue, 29 Sep 2026 18:01:03 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.5.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 29 Sep 2026 18:01:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 29 Sep 2026 18:01:03 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 29 Sep 2026 18:01:03 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 29 Sep 2026 18:01:03 GMT
USER 1000
```

-	Layers:
	-	`sha256:b4d392f98c3fbb6bd1e4b1a1f0fc436f57b975ddeeec92d383d84aa9a3aa5e2a`  
		Last Modified: Mon, 28 Sep 2026 01:41:38 GMT  
		Size: 38.8 MB (38812699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab13acf94fda503db72ebd8a7edf17bd6c2b66d7634d5fb19e511aebcd9f07`  
		Last Modified: Tue, 29 Sep 2026 18:02:26 GMT  
		Size: 19.3 MB (19258096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4d5a8963a10ad0fe163cf336c94968056f2986ae3823f6f47cc25f99bebca`  
		Last Modified: Tue, 29 Sep 2026 18:02:35 GMT  
		Size: 497.7 MB (497714052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298343260c2d162270fc85c290f62203ccce941fd700024632dc4d8038d66af7`  
		Last Modified: Tue, 29 Sep 2026 18:02:25 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c90f17e4c2f0f6c4d359363b5390e96c8a848789b597859b393d258a64081`  
		Last Modified: Tue, 29 Sep 2026 18:02:26 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bffb08adef19569970016efca8c505bd83f8974e88d148d80c236f62c85c49a`  
		Last Modified: Tue, 29 Sep 2026 18:02:26 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84041ab07fe9c251c3182273db863f5bcd90bbc6fbdeb6d5db98dd421d0e929a`  
		Last Modified: Tue, 29 Sep 2026 18:02:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fade13d94b1b1defe221bdd16ca5dbadaa54ee9eb6d80a009db6140b3c91983e`  
		Last Modified: Tue, 29 Sep 2026 18:02:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d8200b8473db7164f4bb2dc8f06cc97da3253aea2611eb545bb5d6bb488891`  
		Last Modified: Tue, 29 Sep 2026 18:02:28 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a8997e3eb31c77c1f63559aea5bff855d2f1618ba8b466545e3fa1c8e2147`  
		Last Modified: Tue, 29 Sep 2026 18:02:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f899430eea4b9ab76db8d0c3c7af349da492536ea82b859653aedd2f171da26`  
		Last Modified: Tue, 29 Sep 2026 18:02:29 GMT  
		Size: 73.5 KB (73454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0401b630b15ef3c1dcd4bbd902a9a02bbaab48853e0198e8926271e3700ba4`  
		Last Modified: Tue, 29 Sep 2026 18:02:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e001b3244c64797903a85fc5918d689d0a18b958b84f02abd3faa108e9edc8`  
		Last Modified: Tue, 29 Sep 2026 18:02:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.5.3` - unknown; unknown

```console
$ docker pull kibana@sha256:a75c45a1e20dc797b17f046cc2477586d36e185717e0aac461ae876179971ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6138219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e48acc3c045b96c51dc72e89a66af547c2135a33bc87bd4c366246a408ef16`

```dockerfile
```

-	Layers:
	-	`sha256:749154234418fa8357efb6cbf70e0e717c0632c56c3e1962b8f8574f9b82c46c`  
		Last Modified: Tue, 29 Sep 2026 18:02:26 GMT  
		Size: 6.1 MB (6094736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb325e994db173acbe1dee8930cc7be1c914742927076d10149f50afa3de4ccc`  
		Last Modified: Tue, 29 Sep 2026 18:02:25 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
