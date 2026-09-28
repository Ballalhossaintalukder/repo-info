<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260926`](#odoo180-20260926)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260926`](#odoo190-20260926)
-	[`odoo:20`](#odoo20)
-	[`odoo:20.0`](#odoo200)
-	[`odoo:20.0-20260926`](#odoo200-20260926)
-	[`odoo:latest`](#odoolatest)

## `odoo:18`

```console
$ docker pull odoo@sha256:eea33387602b203a834d60eee027fcc0d9fcdfd47e310a2d1740ea82322445d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:a9eada112e803de11a194504d5ae9de6ef0afd677d8364f80ad5df16180e5a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676952190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d504569fbae059a5733bab8a203b989a90580cbc7bdec6d1b72456530c42fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 19:03:11 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 19:03:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 19:03:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 19:03:11 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 19:03:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 19:03:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:05:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
USER odoo
# Mon, 28 Sep 2026 19:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e52320e6bbcdb3b726baa3213ee22984d03419bda875abd7143d0899963c5f7`  
		Last Modified: Mon, 28 Sep 2026 19:06:56 GMT  
		Size: 238.7 MB (238710998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f55e436c0a915933330ef40735940a368e4f633045e13b89a28067b5afa19`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 16.6 MB (16632467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0efd6f88f093eced4ae663f8bc9a1989b091d038b7ef75b8f5d7754172d51ea`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 868.9 KB (868944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7721a157cb0a9f9891c4ad130cf4f23db2e4356ff4f25b5e4f38cae5e427`  
		Last Modified: Mon, 28 Sep 2026 19:06:58 GMT  
		Size: 391.0 MB (390972868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def6101e5a65adcf6f3626a3afaa5c47a33c89b93374d40147932f2f5e6379b0`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3e841f5ad2fa5bd0382ed2fcf852fa2ee50c082fb96bd1dbe48b3d76b0550`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5255dbb6cb56a3cd381c421d7f1cb66e3b935c6d09a78fd46f12ee69fb71acf`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efade5de673bdb9a7fa46fbb7eeef6451bb5f699b8b10a440ccec23abaa6523`  
		Last Modified: Mon, 28 Sep 2026 19:06:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:10aa6038a2a0fb292f6393bdd9e440b35bb21b0ff704e09d73613dec6415d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eee7da665ee8b62973b0f7268c52cebfe8ebcd9f6b26dacebed25969fb2b29`

```dockerfile
```

-	Layers:
	-	`sha256:dc0a7dfa1b9739f0f2734a19fe1025208a01fe5aab704acbfa38276354b644a1`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 43.9 MB (43913957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6f894fc02c89a45d8828bbbe867f50305810131982fe7013af378237bf6ef1`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a2b6043e560370180a63b6e66ae6cc204f447a58314d65d23a6c4ec2e54565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.4 MB (673384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3acad16c0342067c1a32c6ba6a9519108937b63930c2f38d72b3dd07021345c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:53 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:53 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:53 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:55:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42186fec15c084ceef02b4d9ddc208a31838b22574863f227085a8c5498e38`  
		Last Modified: Mon, 28 Sep 2026 18:58:39 GMT  
		Size: 236.2 MB (236178684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd53a482f1d980b203018a47eb49cd9b4de2d32a47cf25a0190f3fe5895626`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 16.6 MB (16576206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee66bf3f1a0ee8c343caef54f84b7bba6c0bc4987b341cadac25c2943c578f11`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 868.9 KB (868894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8e9228d42a49405a2998ca95cd2833e7927cb13d1b719f6dad0d15f0e0467`  
		Last Modified: Mon, 28 Sep 2026 18:58:42 GMT  
		Size: 390.8 MB (390816495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3efcc8facb7499680130043932522cf65d9aa576536786c67d13cc453bd5900`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc8d042b37e03bed021258878e2623f71a5634b7869ef6cfb8e0651bc77145`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d878762d6bd34fbd285f73a688284516dcd88c46675a3c870b531f74e05202`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d74ba628b7e4e8d753293d83538865507d235eb65696df26be8799e8208b04`  
		Last Modified: Mon, 28 Sep 2026 18:58:34 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:91bacfc84adb0b76c8369366664226a573923a654911a4e5b9ad0613f06f9652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43948578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43a085d363f65ec49f98ee79e5f1c246333143663c4e019394d69561231208c`

```dockerfile
```

-	Layers:
	-	`sha256:6a3392238e70a366d24d924c881bede8b198f5f0eeba5135a425243fcdc6ef8f`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 43.9 MB (43921229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed38f306d46a533882c67972223be4c8ffa2472d319c93b7bd32f5be54cd1b4e`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 27.3 KB (27349 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:699c703b1f1490f4115f14f733157c2a0d2c2a6edfaedd82b416a7307b27112b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 MB (693470484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bee23e46d1f8d6fca4e840a93b205bcfda78443995ac0f86bf9fa7f99a87b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:11:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:11:55 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:11:56 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:11:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:11:56 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
USER odoo
# Mon, 28 Sep 2026 19:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fdae333ddb2ba70f98cde185d6156f7be171425c4c2b0c05c3d7ff0b6ba0fa`  
		Last Modified: Mon, 28 Sep 2026 19:16:35 GMT  
		Size: 391.5 MB (391502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dca079dd1ad2c115c66b4645611c9122a93401087763f24c24d7450209e11`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d537c2483176795a82c0ea979575370ed8dc8aa12955176e58df4440912af3`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb71b3731ffb3477c77bb67aa067c12af40d851a739518fcb9378bb4cc4023a1`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234cdfd4ab13a2f30e7622775be373d1eccfca147777cc25d7ab907a1d22126`  
		Last Modified: Mon, 28 Sep 2026 19:16:27 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:417c04b74386af4c45d663c8d19f8a2c578f73dfd9087b7b7156f1407ffe2f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43949574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa88779743faf36751c011eb358b24982a0fed0bc14da4a88515fb55cd9a5dc`

```dockerfile
```

-	Layers:
	-	`sha256:cd3ee16aee4b551fbbb7fe55c27bbaafb8dd6d8af1cab4323d0c412e4fcc3a15`  
		Last Modified: Mon, 28 Sep 2026 19:16:28 GMT  
		Size: 43.9 MB (43922321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39be6e77fdd57557566968b000482e5988f1cae8b0f930619d812461331ba064`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 27.3 KB (27253 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:eea33387602b203a834d60eee027fcc0d9fcdfd47e310a2d1740ea82322445d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:a9eada112e803de11a194504d5ae9de6ef0afd677d8364f80ad5df16180e5a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676952190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d504569fbae059a5733bab8a203b989a90580cbc7bdec6d1b72456530c42fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 19:03:11 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 19:03:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 19:03:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 19:03:11 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 19:03:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 19:03:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:05:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
USER odoo
# Mon, 28 Sep 2026 19:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e52320e6bbcdb3b726baa3213ee22984d03419bda875abd7143d0899963c5f7`  
		Last Modified: Mon, 28 Sep 2026 19:06:56 GMT  
		Size: 238.7 MB (238710998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f55e436c0a915933330ef40735940a368e4f633045e13b89a28067b5afa19`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 16.6 MB (16632467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0efd6f88f093eced4ae663f8bc9a1989b091d038b7ef75b8f5d7754172d51ea`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 868.9 KB (868944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7721a157cb0a9f9891c4ad130cf4f23db2e4356ff4f25b5e4f38cae5e427`  
		Last Modified: Mon, 28 Sep 2026 19:06:58 GMT  
		Size: 391.0 MB (390972868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def6101e5a65adcf6f3626a3afaa5c47a33c89b93374d40147932f2f5e6379b0`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3e841f5ad2fa5bd0382ed2fcf852fa2ee50c082fb96bd1dbe48b3d76b0550`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5255dbb6cb56a3cd381c421d7f1cb66e3b935c6d09a78fd46f12ee69fb71acf`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efade5de673bdb9a7fa46fbb7eeef6451bb5f699b8b10a440ccec23abaa6523`  
		Last Modified: Mon, 28 Sep 2026 19:06:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:10aa6038a2a0fb292f6393bdd9e440b35bb21b0ff704e09d73613dec6415d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eee7da665ee8b62973b0f7268c52cebfe8ebcd9f6b26dacebed25969fb2b29`

```dockerfile
```

-	Layers:
	-	`sha256:dc0a7dfa1b9739f0f2734a19fe1025208a01fe5aab704acbfa38276354b644a1`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 43.9 MB (43913957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6f894fc02c89a45d8828bbbe867f50305810131982fe7013af378237bf6ef1`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a2b6043e560370180a63b6e66ae6cc204f447a58314d65d23a6c4ec2e54565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.4 MB (673384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3acad16c0342067c1a32c6ba6a9519108937b63930c2f38d72b3dd07021345c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:53 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:53 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:53 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:55:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42186fec15c084ceef02b4d9ddc208a31838b22574863f227085a8c5498e38`  
		Last Modified: Mon, 28 Sep 2026 18:58:39 GMT  
		Size: 236.2 MB (236178684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd53a482f1d980b203018a47eb49cd9b4de2d32a47cf25a0190f3fe5895626`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 16.6 MB (16576206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee66bf3f1a0ee8c343caef54f84b7bba6c0bc4987b341cadac25c2943c578f11`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 868.9 KB (868894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8e9228d42a49405a2998ca95cd2833e7927cb13d1b719f6dad0d15f0e0467`  
		Last Modified: Mon, 28 Sep 2026 18:58:42 GMT  
		Size: 390.8 MB (390816495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3efcc8facb7499680130043932522cf65d9aa576536786c67d13cc453bd5900`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc8d042b37e03bed021258878e2623f71a5634b7869ef6cfb8e0651bc77145`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d878762d6bd34fbd285f73a688284516dcd88c46675a3c870b531f74e05202`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d74ba628b7e4e8d753293d83538865507d235eb65696df26be8799e8208b04`  
		Last Modified: Mon, 28 Sep 2026 18:58:34 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:91bacfc84adb0b76c8369366664226a573923a654911a4e5b9ad0613f06f9652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43948578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43a085d363f65ec49f98ee79e5f1c246333143663c4e019394d69561231208c`

```dockerfile
```

-	Layers:
	-	`sha256:6a3392238e70a366d24d924c881bede8b198f5f0eeba5135a425243fcdc6ef8f`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 43.9 MB (43921229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed38f306d46a533882c67972223be4c8ffa2472d319c93b7bd32f5be54cd1b4e`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 27.3 KB (27349 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:699c703b1f1490f4115f14f733157c2a0d2c2a6edfaedd82b416a7307b27112b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 MB (693470484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bee23e46d1f8d6fca4e840a93b205bcfda78443995ac0f86bf9fa7f99a87b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:11:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:11:55 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:11:56 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:11:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:11:56 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
USER odoo
# Mon, 28 Sep 2026 19:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fdae333ddb2ba70f98cde185d6156f7be171425c4c2b0c05c3d7ff0b6ba0fa`  
		Last Modified: Mon, 28 Sep 2026 19:16:35 GMT  
		Size: 391.5 MB (391502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dca079dd1ad2c115c66b4645611c9122a93401087763f24c24d7450209e11`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d537c2483176795a82c0ea979575370ed8dc8aa12955176e58df4440912af3`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb71b3731ffb3477c77bb67aa067c12af40d851a739518fcb9378bb4cc4023a1`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234cdfd4ab13a2f30e7622775be373d1eccfca147777cc25d7ab907a1d22126`  
		Last Modified: Mon, 28 Sep 2026 19:16:27 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:417c04b74386af4c45d663c8d19f8a2c578f73dfd9087b7b7156f1407ffe2f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43949574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa88779743faf36751c011eb358b24982a0fed0bc14da4a88515fb55cd9a5dc`

```dockerfile
```

-	Layers:
	-	`sha256:cd3ee16aee4b551fbbb7fe55c27bbaafb8dd6d8af1cab4323d0c412e4fcc3a15`  
		Last Modified: Mon, 28 Sep 2026 19:16:28 GMT  
		Size: 43.9 MB (43922321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39be6e77fdd57557566968b000482e5988f1cae8b0f930619d812461331ba064`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 27.3 KB (27253 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260926`

```console
$ docker pull odoo@sha256:eea33387602b203a834d60eee027fcc0d9fcdfd47e310a2d1740ea82322445d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260926` - linux; amd64

```console
$ docker pull odoo@sha256:a9eada112e803de11a194504d5ae9de6ef0afd677d8364f80ad5df16180e5a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676952190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d504569fbae059a5733bab8a203b989a90580cbc7bdec6d1b72456530c42fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 19:03:11 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 19:03:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 19:03:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 19:03:11 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 19:03:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 19:03:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:04:33 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:04:33 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:05:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:05:28 GMT
USER odoo
# Mon, 28 Sep 2026 19:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e52320e6bbcdb3b726baa3213ee22984d03419bda875abd7143d0899963c5f7`  
		Last Modified: Mon, 28 Sep 2026 19:06:56 GMT  
		Size: 238.7 MB (238710998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f55e436c0a915933330ef40735940a368e4f633045e13b89a28067b5afa19`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 16.6 MB (16632467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0efd6f88f093eced4ae663f8bc9a1989b091d038b7ef75b8f5d7754172d51ea`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 868.9 KB (868944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7721a157cb0a9f9891c4ad130cf4f23db2e4356ff4f25b5e4f38cae5e427`  
		Last Modified: Mon, 28 Sep 2026 19:06:58 GMT  
		Size: 391.0 MB (390972868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def6101e5a65adcf6f3626a3afaa5c47a33c89b93374d40147932f2f5e6379b0`  
		Last Modified: Mon, 28 Sep 2026 19:06:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3e841f5ad2fa5bd0382ed2fcf852fa2ee50c082fb96bd1dbe48b3d76b0550`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5255dbb6cb56a3cd381c421d7f1cb66e3b935c6d09a78fd46f12ee69fb71acf`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efade5de673bdb9a7fa46fbb7eeef6451bb5f699b8b10a440ccec23abaa6523`  
		Last Modified: Mon, 28 Sep 2026 19:06:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:10aa6038a2a0fb292f6393bdd9e440b35bb21b0ff704e09d73613dec6415d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eee7da665ee8b62973b0f7268c52cebfe8ebcd9f6b26dacebed25969fb2b29`

```dockerfile
```

-	Layers:
	-	`sha256:dc0a7dfa1b9739f0f2734a19fe1025208a01fe5aab704acbfa38276354b644a1`  
		Last Modified: Mon, 28 Sep 2026 19:06:49 GMT  
		Size: 43.9 MB (43913957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6f894fc02c89a45d8828bbbe867f50305810131982fe7013af378237bf6ef1`  
		Last Modified: Mon, 28 Sep 2026 19:06:47 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260926` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a2b6043e560370180a63b6e66ae6cc204f447a58314d65d23a6c4ec2e54565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.4 MB (673384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3acad16c0342067c1a32c6ba6a9519108937b63930c2f38d72b3dd07021345c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:53 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:53 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:53 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:55:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:08 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:08 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:06 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42186fec15c084ceef02b4d9ddc208a31838b22574863f227085a8c5498e38`  
		Last Modified: Mon, 28 Sep 2026 18:58:39 GMT  
		Size: 236.2 MB (236178684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd53a482f1d980b203018a47eb49cd9b4de2d32a47cf25a0190f3fe5895626`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 16.6 MB (16576206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee66bf3f1a0ee8c343caef54f84b7bba6c0bc4987b341cadac25c2943c578f11`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 868.9 KB (868894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8e9228d42a49405a2998ca95cd2833e7927cb13d1b719f6dad0d15f0e0467`  
		Last Modified: Mon, 28 Sep 2026 18:58:42 GMT  
		Size: 390.8 MB (390816495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3efcc8facb7499680130043932522cf65d9aa576536786c67d13cc453bd5900`  
		Last Modified: Mon, 28 Sep 2026 18:58:32 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc8d042b37e03bed021258878e2623f71a5634b7869ef6cfb8e0651bc77145`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d878762d6bd34fbd285f73a688284516dcd88c46675a3c870b531f74e05202`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d74ba628b7e4e8d753293d83538865507d235eb65696df26be8799e8208b04`  
		Last Modified: Mon, 28 Sep 2026 18:58:34 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:91bacfc84adb0b76c8369366664226a573923a654911a4e5b9ad0613f06f9652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43948578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43a085d363f65ec49f98ee79e5f1c246333143663c4e019394d69561231208c`

```dockerfile
```

-	Layers:
	-	`sha256:6a3392238e70a366d24d924c881bede8b198f5f0eeba5135a425243fcdc6ef8f`  
		Last Modified: Mon, 28 Sep 2026 18:58:33 GMT  
		Size: 43.9 MB (43921229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed38f306d46a533882c67972223be4c8ffa2472d319c93b7bd32f5be54cd1b4e`  
		Last Modified: Mon, 28 Sep 2026 18:58:31 GMT  
		Size: 27.3 KB (27349 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260926` - linux; ppc64le

```console
$ docker pull odoo@sha256:699c703b1f1490f4115f14f733157c2a0d2c2a6edfaedd82b416a7307b27112b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 MB (693470484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bee23e46d1f8d6fca4e840a93b205bcfda78443995ac0f86bf9fa7f99a87b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
# Mon, 28 Sep 2026 19:11:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:11:55 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=b6a268db3fca5ce831a35070dd3c4bfc6a575b85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:11:56 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:11:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:11:56 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:11:56 GMT
USER odoo
# Mon, 28 Sep 2026 19:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fdae333ddb2ba70f98cde185d6156f7be171425c4c2b0c05c3d7ff0b6ba0fa`  
		Last Modified: Mon, 28 Sep 2026 19:16:35 GMT  
		Size: 391.5 MB (391502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dca079dd1ad2c115c66b4645611c9122a93401087763f24c24d7450209e11`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d537c2483176795a82c0ea979575370ed8dc8aa12955176e58df4440912af3`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb71b3731ffb3477c77bb67aa067c12af40d851a739518fcb9378bb4cc4023a1`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234cdfd4ab13a2f30e7622775be373d1eccfca147777cc25d7ab907a1d22126`  
		Last Modified: Mon, 28 Sep 2026 19:16:27 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:417c04b74386af4c45d663c8d19f8a2c578f73dfd9087b7b7156f1407ffe2f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43949574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa88779743faf36751c011eb358b24982a0fed0bc14da4a88515fb55cd9a5dc`

```dockerfile
```

-	Layers:
	-	`sha256:cd3ee16aee4b551fbbb7fe55c27bbaafb8dd6d8af1cab4323d0c412e4fcc3a15`  
		Last Modified: Mon, 28 Sep 2026 19:16:28 GMT  
		Size: 43.9 MB (43922321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39be6e77fdd57557566968b000482e5988f1cae8b0f930619d812461331ba064`  
		Last Modified: Mon, 28 Sep 2026 19:16:25 GMT  
		Size: 27.3 KB (27253 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:77bac5cd1e065210828f34883a7f76740b7373d06dd3a5a55d3eeb31ee2f85cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:899c45e79346587ec706f7a40a1e81180b0740026f7a8329371ea7e82bb4052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700417401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415bfd55bbf3a1463dc685195d69cf39a763d0be62c5ce9dfa5978c605948a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:01:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:01:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:02:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:02:00 GMT
USER odoo
# Mon, 28 Sep 2026 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:02:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1832d2f8944f4e6ef313759529d9ed0ecce5b451f5cc1ec2f929fa2eb195b98b`  
		Last Modified: Mon, 28 Sep 2026 19:03:45 GMT  
		Size: 414.4 MB (414437396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d74b14abea1c652f98d6741ea76d0273104c2f4e177f7a28784ee527603faf`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9f9369a705550b14a2f52619fc8f2853aa1183875a5f2aa6e8b258b70ea3f`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89c87bef2ad3a24ea3aaae6408d66032bf10ea60fe49150644f719a787ae073`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27600782684225eef620f2acb0996090072d19c6a4488f242daa441f06a87bb2`  
		Last Modified: Mon, 28 Sep 2026 19:03:38 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:07284f2b80c74d31fb4d49befc6088bcff03fe7a58c1c37d0e725a63fea7bd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52486085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c682ec0053d553774130c180366ec0838d912a050923b8ed4082555c37c6266`

```dockerfile
```

-	Layers:
	-	`sha256:a2344a0d6e0b2322ce399a0910c38c3ca3b77f1313d202fdbab5cfe07680856c`  
		Last Modified: Mon, 28 Sep 2026 19:03:39 GMT  
		Size: 52.5 MB (52458888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f1e0b310dbca52da24f0b0a9204a04d12c3f55e62a87bc8a1d731ecd13df2c`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e617e76183681ca27cb90599780ba1061f87df7311632fa68cfb9456dc884d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.9 MB (696865025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4dcc1d04dcbb55205a974fcbb752516752b0114f40459f7f997e904e4db997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:48 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:48 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:59 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 18:57:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c01e4e8f822734e88bf0b6a80a0f9a71d9dc02782203e00f6186cf820f754b`  
		Last Modified: Mon, 28 Sep 2026 18:59:24 GMT  
		Size: 236.2 MB (236179632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27242d6a2ce1cf047037a886812b7f3770bddbaa184cbccb48fa9e891d0faa38`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 16.6 MB (16576256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62ed1b779e3c1cbfae4a272f731bddbe65075d940e6f26e4387cad1240ac0`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 868.9 KB (868930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd91c887629e0ae40124c23e143d16b75f66ab06b8712e784861d9106b529f14`  
		Last Modified: Mon, 28 Sep 2026 18:59:27 GMT  
		Size: 414.3 MB (414295877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e08569eff0b0af271b5bf583fc7686291bd42d2fbdbcb0a2b10a1f0cdbaff1`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ac0adcecdbb8e1c4cb40bde3ceaf6a8807f6481a4f4d80d94f137f9ff6da6`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87711369f0c2aa4b881a63f21eea4cf49b054ad01edef4b63f480f1c3025d2`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8b74bad3d6f5643e307459f16881cab66907a155034e5fdf43af08a330d793`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:9e837e9263d8f4d9538d7e69a50c7b70f0fd1162a28a9964f44d213139f6ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52493508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f9b3df5d0e4dd5db7e34a8d6eb8c0fd698f8e3fa6d3c48e59cd57114ea103d`

```dockerfile
```

-	Layers:
	-	`sha256:005fcce766c807fe08b7f5fcb50b90e1dad0f90aa94e4a1567d4ee9f6218d473`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 52.5 MB (52466160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e40d28721b13d6f6019d20e02b23b7d663465e6218271d0260c22b9a0221f6`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 27.3 KB (27348 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:50be9d97a84546537ad63a96d693bacdcfbb6840284ce26116205fc25f763be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.0 MB (716957961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef274eac3d495fc45f6ded77efae73f7b42e56043cb5ef87a1f5246f0aa3936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:04:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4239e38dc7a54262dc6eb903b8decc32be4ed2ab0bc1990f5376dd26541b52e`  
		Last Modified: Mon, 28 Sep 2026 19:09:48 GMT  
		Size: 415.0 MB (414989621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2320d60577a6b8de223a276067f01e431dc8e8162015d11cee15c7a24cc2da2`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a913b081d386d4148a4a87a941f3ae38374e7d134d4a2cd7265ae86472a73`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b004dc1790754369bc00ad948793e0eeda838ee12c4e2e434a275f443c7d60a0`  
		Last Modified: Mon, 28 Sep 2026 19:09:36 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8537f0a4a294b1b9412a3f865ac6c788d91c53f38c6393fbb998ca70f3240f5`  
		Last Modified: Mon, 28 Sep 2026 19:09:38 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f1ce86f988c06db7fc33d622f440de18b22b1605dbf577f8e8128a3121af8dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52494504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e373ff6f56a2fd33401156c8154ff6f1c15c1b9aa1bb048ca7a291dc276da189`

```dockerfile
```

-	Layers:
	-	`sha256:ec98a7849bc2234ee830eda18a218c378cb668d16abad5782d01b5ecad2e6a19`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 52.5 MB (52467252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94345822266e6815f8e3a595d23aadbf5d3c36166a3c75f4b945dd144d3fa1b1`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 27.3 KB (27252 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:77bac5cd1e065210828f34883a7f76740b7373d06dd3a5a55d3eeb31ee2f85cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:899c45e79346587ec706f7a40a1e81180b0740026f7a8329371ea7e82bb4052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700417401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415bfd55bbf3a1463dc685195d69cf39a763d0be62c5ce9dfa5978c605948a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:01:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:01:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:02:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:02:00 GMT
USER odoo
# Mon, 28 Sep 2026 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:02:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1832d2f8944f4e6ef313759529d9ed0ecce5b451f5cc1ec2f929fa2eb195b98b`  
		Last Modified: Mon, 28 Sep 2026 19:03:45 GMT  
		Size: 414.4 MB (414437396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d74b14abea1c652f98d6741ea76d0273104c2f4e177f7a28784ee527603faf`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9f9369a705550b14a2f52619fc8f2853aa1183875a5f2aa6e8b258b70ea3f`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89c87bef2ad3a24ea3aaae6408d66032bf10ea60fe49150644f719a787ae073`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27600782684225eef620f2acb0996090072d19c6a4488f242daa441f06a87bb2`  
		Last Modified: Mon, 28 Sep 2026 19:03:38 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:07284f2b80c74d31fb4d49befc6088bcff03fe7a58c1c37d0e725a63fea7bd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52486085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c682ec0053d553774130c180366ec0838d912a050923b8ed4082555c37c6266`

```dockerfile
```

-	Layers:
	-	`sha256:a2344a0d6e0b2322ce399a0910c38c3ca3b77f1313d202fdbab5cfe07680856c`  
		Last Modified: Mon, 28 Sep 2026 19:03:39 GMT  
		Size: 52.5 MB (52458888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f1e0b310dbca52da24f0b0a9204a04d12c3f55e62a87bc8a1d731ecd13df2c`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e617e76183681ca27cb90599780ba1061f87df7311632fa68cfb9456dc884d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.9 MB (696865025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4dcc1d04dcbb55205a974fcbb752516752b0114f40459f7f997e904e4db997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:48 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:48 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:59 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 18:57:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c01e4e8f822734e88bf0b6a80a0f9a71d9dc02782203e00f6186cf820f754b`  
		Last Modified: Mon, 28 Sep 2026 18:59:24 GMT  
		Size: 236.2 MB (236179632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27242d6a2ce1cf047037a886812b7f3770bddbaa184cbccb48fa9e891d0faa38`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 16.6 MB (16576256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62ed1b779e3c1cbfae4a272f731bddbe65075d940e6f26e4387cad1240ac0`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 868.9 KB (868930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd91c887629e0ae40124c23e143d16b75f66ab06b8712e784861d9106b529f14`  
		Last Modified: Mon, 28 Sep 2026 18:59:27 GMT  
		Size: 414.3 MB (414295877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e08569eff0b0af271b5bf583fc7686291bd42d2fbdbcb0a2b10a1f0cdbaff1`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ac0adcecdbb8e1c4cb40bde3ceaf6a8807f6481a4f4d80d94f137f9ff6da6`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87711369f0c2aa4b881a63f21eea4cf49b054ad01edef4b63f480f1c3025d2`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8b74bad3d6f5643e307459f16881cab66907a155034e5fdf43af08a330d793`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9e837e9263d8f4d9538d7e69a50c7b70f0fd1162a28a9964f44d213139f6ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52493508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f9b3df5d0e4dd5db7e34a8d6eb8c0fd698f8e3fa6d3c48e59cd57114ea103d`

```dockerfile
```

-	Layers:
	-	`sha256:005fcce766c807fe08b7f5fcb50b90e1dad0f90aa94e4a1567d4ee9f6218d473`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 52.5 MB (52466160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e40d28721b13d6f6019d20e02b23b7d663465e6218271d0260c22b9a0221f6`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 27.3 KB (27348 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:50be9d97a84546537ad63a96d693bacdcfbb6840284ce26116205fc25f763be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.0 MB (716957961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef274eac3d495fc45f6ded77efae73f7b42e56043cb5ef87a1f5246f0aa3936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:04:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4239e38dc7a54262dc6eb903b8decc32be4ed2ab0bc1990f5376dd26541b52e`  
		Last Modified: Mon, 28 Sep 2026 19:09:48 GMT  
		Size: 415.0 MB (414989621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2320d60577a6b8de223a276067f01e431dc8e8162015d11cee15c7a24cc2da2`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a913b081d386d4148a4a87a941f3ae38374e7d134d4a2cd7265ae86472a73`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b004dc1790754369bc00ad948793e0eeda838ee12c4e2e434a275f443c7d60a0`  
		Last Modified: Mon, 28 Sep 2026 19:09:36 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8537f0a4a294b1b9412a3f865ac6c788d91c53f38c6393fbb998ca70f3240f5`  
		Last Modified: Mon, 28 Sep 2026 19:09:38 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f1ce86f988c06db7fc33d622f440de18b22b1605dbf577f8e8128a3121af8dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52494504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e373ff6f56a2fd33401156c8154ff6f1c15c1b9aa1bb048ca7a291dc276da189`

```dockerfile
```

-	Layers:
	-	`sha256:ec98a7849bc2234ee830eda18a218c378cb668d16abad5782d01b5ecad2e6a19`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 52.5 MB (52467252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94345822266e6815f8e3a595d23aadbf5d3c36166a3c75f4b945dd144d3fa1b1`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 27.3 KB (27252 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260926`

```console
$ docker pull odoo@sha256:77bac5cd1e065210828f34883a7f76740b7373d06dd3a5a55d3eeb31ee2f85cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260926` - linux; amd64

```console
$ docker pull odoo@sha256:899c45e79346587ec706f7a40a1e81180b0740026f7a8329371ea7e82bb4052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700417401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415bfd55bbf3a1463dc685195d69cf39a763d0be62c5ce9dfa5978c605948a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:01:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:01:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:01:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:02:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:02:00 GMT
USER odoo
# Mon, 28 Sep 2026 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:02:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1832d2f8944f4e6ef313759529d9ed0ecce5b451f5cc1ec2f929fa2eb195b98b`  
		Last Modified: Mon, 28 Sep 2026 19:03:45 GMT  
		Size: 414.4 MB (414437396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d74b14abea1c652f98d6741ea76d0273104c2f4e177f7a28784ee527603faf`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9f9369a705550b14a2f52619fc8f2853aa1183875a5f2aa6e8b258b70ea3f`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89c87bef2ad3a24ea3aaae6408d66032bf10ea60fe49150644f719a787ae073`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27600782684225eef620f2acb0996090072d19c6a4488f242daa441f06a87bb2`  
		Last Modified: Mon, 28 Sep 2026 19:03:38 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:07284f2b80c74d31fb4d49befc6088bcff03fe7a58c1c37d0e725a63fea7bd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52486085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c682ec0053d553774130c180366ec0838d912a050923b8ed4082555c37c6266`

```dockerfile
```

-	Layers:
	-	`sha256:a2344a0d6e0b2322ce399a0910c38c3ca3b77f1313d202fdbab5cfe07680856c`  
		Last Modified: Mon, 28 Sep 2026 19:03:39 GMT  
		Size: 52.5 MB (52458888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f1e0b310dbca52da24f0b0a9204a04d12c3f55e62a87bc8a1d731ecd13df2c`  
		Last Modified: Mon, 28 Sep 2026 19:03:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260926` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e617e76183681ca27cb90599780ba1061f87df7311632fa68cfb9456dc884d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.9 MB (696865025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4dcc1d04dcbb55205a974fcbb752516752b0114f40459f7f997e904e4db997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:48 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:48 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:59 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:56:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:56:11 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 18:57:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:25 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c01e4e8f822734e88bf0b6a80a0f9a71d9dc02782203e00f6186cf820f754b`  
		Last Modified: Mon, 28 Sep 2026 18:59:24 GMT  
		Size: 236.2 MB (236179632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27242d6a2ce1cf047037a886812b7f3770bddbaa184cbccb48fa9e891d0faa38`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 16.6 MB (16576256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62ed1b779e3c1cbfae4a272f731bddbe65075d940e6f26e4387cad1240ac0`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 868.9 KB (868930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd91c887629e0ae40124c23e143d16b75f66ab06b8712e784861d9106b529f14`  
		Last Modified: Mon, 28 Sep 2026 18:59:27 GMT  
		Size: 414.3 MB (414295877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e08569eff0b0af271b5bf583fc7686291bd42d2fbdbcb0a2b10a1f0cdbaff1`  
		Last Modified: Mon, 28 Sep 2026 18:59:16 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ac0adcecdbb8e1c4cb40bde3ceaf6a8807f6481a4f4d80d94f137f9ff6da6`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87711369f0c2aa4b881a63f21eea4cf49b054ad01edef4b63f480f1c3025d2`  
		Last Modified: Mon, 28 Sep 2026 18:59:17 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8b74bad3d6f5643e307459f16881cab66907a155034e5fdf43af08a330d793`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:9e837e9263d8f4d9538d7e69a50c7b70f0fd1162a28a9964f44d213139f6ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52493508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f9b3df5d0e4dd5db7e34a8d6eb8c0fd698f8e3fa6d3c48e59cd57114ea103d`

```dockerfile
```

-	Layers:
	-	`sha256:005fcce766c807fe08b7f5fcb50b90e1dad0f90aa94e4a1567d4ee9f6218d473`  
		Last Modified: Mon, 28 Sep 2026 18:59:18 GMT  
		Size: 52.5 MB (52466160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e40d28721b13d6f6019d20e02b23b7d663465e6218271d0260c22b9a0221f6`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 27.3 KB (27348 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260926` - linux; ppc64le

```console
$ docker pull odoo@sha256:50be9d97a84546537ad63a96d693bacdcfbb6840284ce26116205fc25f763be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.0 MB (716957961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef274eac3d495fc45f6ded77efae73f7b42e56043cb5ef87a1f5246f0aa3936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=19.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
# Mon, 28 Sep 2026 19:04:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=cb9d876779edc8d5f0394ddd3936a387e349077c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4239e38dc7a54262dc6eb903b8decc32be4ed2ab0bc1990f5376dd26541b52e`  
		Last Modified: Mon, 28 Sep 2026 19:09:48 GMT  
		Size: 415.0 MB (414989621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2320d60577a6b8de223a276067f01e431dc8e8162015d11cee15c7a24cc2da2`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a913b081d386d4148a4a87a941f3ae38374e7d134d4a2cd7265ae86472a73`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b004dc1790754369bc00ad948793e0eeda838ee12c4e2e434a275f443c7d60a0`  
		Last Modified: Mon, 28 Sep 2026 19:09:36 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8537f0a4a294b1b9412a3f865ac6c788d91c53f38c6393fbb998ca70f3240f5`  
		Last Modified: Mon, 28 Sep 2026 19:09:38 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:f1ce86f988c06db7fc33d622f440de18b22b1605dbf577f8e8128a3121af8dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52494504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e373ff6f56a2fd33401156c8154ff6f1c15c1b9aa1bb048ca7a291dc276da189`

```dockerfile
```

-	Layers:
	-	`sha256:ec98a7849bc2234ee830eda18a218c378cb668d16abad5782d01b5ecad2e6a19`  
		Last Modified: Mon, 28 Sep 2026 19:09:37 GMT  
		Size: 52.5 MB (52467252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94345822266e6815f8e3a595d23aadbf5d3c36166a3c75f4b945dd144d3fa1b1`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 27.3 KB (27252 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:20`

```console
$ docker pull odoo@sha256:dc76c42d292af9c513de826620e5a5dbe8152383ce8767eb6ed1390a806eb32f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:20` - linux; amd64

```console
$ docker pull odoo@sha256:74a8a7b1520341fdf6b197791c3b34e984f4d69cc1cdb025ea0c22d9d7c8eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.8 MB (797788224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd4db2906bb95b2a538b79fcd408e2956611cfaf219b42b16d484755e0e4bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:58:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:58:45 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:58:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:58:45 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
USER odoo
# Mon, 28 Sep 2026 18:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:58:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1150a8ef4c37303490fdb702f1f7df9c8be50dde56c466a23e68637d96c8f0`  
		Last Modified: Mon, 28 Sep 2026 19:00:48 GMT  
		Size: 511.8 MB (511808215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee51fb402ac9411c10736e6800bc51d1cf79ca0e0fe65e4e9d15fea885d1293`  
		Last Modified: Mon, 28 Sep 2026 19:00:36 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee75f7b01f9a3d3431c2a51ceb92c50e7c5c9c2563521a85090ccd76af6b00`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7fc3458d3bf7099097ac31f7610e3ba0c0e58c6bc59b60a292545e9f29025d`  
		Last Modified: Mon, 28 Sep 2026 19:00:38 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08a9a0b9479d6a7bea41a041faa9efe342f03e3a05f70715b852b2703acf6b`  
		Last Modified: Mon, 28 Sep 2026 19:00:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20` - unknown; unknown

```console
$ docker pull odoo@sha256:07c19f9cc0e22c84b1114e1fcb734569ec2e735bcfffad1cb8c307848048d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55020918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c65808c40c3f93b293bdee6620363d15a341dc0aeb102c6f931c3702ac70`

```dockerfile
```

-	Layers:
	-	`sha256:3ed60b3e57bcf2e9741e6a536b3d341d3b9b3018ec170992d059959aea3b48a7`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 55.0 MB (54993427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a71113a4602aa17bb14da2378cdb74f2285598b244cd35980441c3f97117c54`  
		Last Modified: Mon, 28 Sep 2026 19:00:33 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:69fb42ff26749fe4970616c234e45d76f6100c965b26e36678deb83431f95a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.2 MB (794212214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e507387dad5481f5ce1bfcbe046df73b29030c80f8e98d432f6c6ec5cfcee4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:44 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:44 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:44 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:14 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df0b9cd83d3280cfbdf5afb034365f561ba426911bd4edf98921cdf0dfd724d`  
		Last Modified: Mon, 28 Sep 2026 18:59:20 GMT  
		Size: 236.2 MB (236178835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23f235a24e3c9b16557ad35f5033cf08c48987fe734037fc282077d099c0c7`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 16.6 MB (16576295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41e94aa3162b4fcbf335febe5154f081e38d699fc487edaf189b9a287809f3`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 868.9 KB (868936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec2b586f2e9064667fef06c5b73365d39d2e292ffc30eb4f683230c165e6ca1`  
		Last Modified: Mon, 28 Sep 2026 18:59:25 GMT  
		Size: 511.6 MB (511643818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2864556ae071ac34feda1546b69e61a271fe451b8638ae2ed25ed024e9144bfc`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d28d15a5211ac0d2e6ff5042ae8515288c57dd10f47665d2b35f620b137122`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf9e637921bdd744276e881cc6c85b057884853554586f58a1eeffb0237876`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ba2b9a8519815c06ac5f8a4cb69d2a69be7a39313cb2434230673387591118`  
		Last Modified: Mon, 28 Sep 2026 18:59:15 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20` - unknown; unknown

```console
$ docker pull odoo@sha256:f990301203ef3be0e06011e548326251ada41d26e6347ae69905645cedc376bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55028366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa262d8e88e5a131a71ee4355d4df2d6ff38f148819f56d1186a4c76e039a5d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0a338a97c9176d684c6ae9b4393a0387c4d9d5a310c2c4d0f00e4673aaad50`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 55.0 MB (55000711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d819f243d723b6e8fcf31b1ebd3f81c7aec98f5fa4262635b97c6730a1e8132`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20` - linux; ppc64le

```console
$ docker pull odoo@sha256:ccca49d14b08518519e5b688e2aad4616afb00cd8eb680218f809c44c08bc793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.3 MB (814312281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd06ccc64f43832a4b83636f2ef5ade12f8160ec6eefc6711e630d04eec8c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 19:04:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:23 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538858bdaeb37c4fa8bb5215881ff361aa4270a0b648feb3dfbfc0ee407de75`  
		Last Modified: Mon, 28 Sep 2026 19:10:05 GMT  
		Size: 512.3 MB (512343945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4200c33b205355a49429f1fa1e0fc32acce66af58f46c9359169f016ad54579`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0214bd494b09595bf03579be8a8840dcb4b9b54fbb9b5b880457ee3f00c99`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385578020ea4dd6a58a07ffc853ebaa0d4a5198e0a718f4b572384c21ab3191`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52d7bfcc1e01bfc4b47f244e5855ea0de863d87916b0e1758e2bca695bd2c3`  
		Last Modified: Mon, 28 Sep 2026 19:09:55 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20` - unknown; unknown

```console
$ docker pull odoo@sha256:51ec8d38f6204e7f6334a40b30224238564306e7d1ed42fa9cbfbed112744b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f48ff56f3a8b8ef986ac6b5e5fd6113ccb1f295477bd6427c11792380a3c70`

```dockerfile
```

-	Layers:
	-	`sha256:b1eedb2b44faddd6e24ebd95005cea9dde1c3d2e3382be044f86db8795828039`  
		Last Modified: Mon, 28 Sep 2026 19:09:56 GMT  
		Size: 55.0 MB (55001797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a340389db09bb7869b9e803fb70bb6856e1d9507cb7c655d8d4373eea0aaf1bd`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 27.6 KB (27553 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:20.0`

```console
$ docker pull odoo@sha256:dc76c42d292af9c513de826620e5a5dbe8152383ce8767eb6ed1390a806eb32f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:20.0` - linux; amd64

```console
$ docker pull odoo@sha256:74a8a7b1520341fdf6b197791c3b34e984f4d69cc1cdb025ea0c22d9d7c8eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.8 MB (797788224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd4db2906bb95b2a538b79fcd408e2956611cfaf219b42b16d484755e0e4bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:58:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:58:45 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:58:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:58:45 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
USER odoo
# Mon, 28 Sep 2026 18:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:58:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1150a8ef4c37303490fdb702f1f7df9c8be50dde56c466a23e68637d96c8f0`  
		Last Modified: Mon, 28 Sep 2026 19:00:48 GMT  
		Size: 511.8 MB (511808215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee51fb402ac9411c10736e6800bc51d1cf79ca0e0fe65e4e9d15fea885d1293`  
		Last Modified: Mon, 28 Sep 2026 19:00:36 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee75f7b01f9a3d3431c2a51ceb92c50e7c5c9c2563521a85090ccd76af6b00`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7fc3458d3bf7099097ac31f7610e3ba0c0e58c6bc59b60a292545e9f29025d`  
		Last Modified: Mon, 28 Sep 2026 19:00:38 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08a9a0b9479d6a7bea41a041faa9efe342f03e3a05f70715b852b2703acf6b`  
		Last Modified: Mon, 28 Sep 2026 19:00:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0` - unknown; unknown

```console
$ docker pull odoo@sha256:07c19f9cc0e22c84b1114e1fcb734569ec2e735bcfffad1cb8c307848048d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55020918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c65808c40c3f93b293bdee6620363d15a341dc0aeb102c6f931c3702ac70`

```dockerfile
```

-	Layers:
	-	`sha256:3ed60b3e57bcf2e9741e6a536b3d341d3b9b3018ec170992d059959aea3b48a7`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 55.0 MB (54993427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a71113a4602aa17bb14da2378cdb74f2285598b244cd35980441c3f97117c54`  
		Last Modified: Mon, 28 Sep 2026 19:00:33 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:69fb42ff26749fe4970616c234e45d76f6100c965b26e36678deb83431f95a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.2 MB (794212214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e507387dad5481f5ce1bfcbe046df73b29030c80f8e98d432f6c6ec5cfcee4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:44 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:44 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:44 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:14 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df0b9cd83d3280cfbdf5afb034365f561ba426911bd4edf98921cdf0dfd724d`  
		Last Modified: Mon, 28 Sep 2026 18:59:20 GMT  
		Size: 236.2 MB (236178835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23f235a24e3c9b16557ad35f5033cf08c48987fe734037fc282077d099c0c7`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 16.6 MB (16576295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41e94aa3162b4fcbf335febe5154f081e38d699fc487edaf189b9a287809f3`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 868.9 KB (868936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec2b586f2e9064667fef06c5b73365d39d2e292ffc30eb4f683230c165e6ca1`  
		Last Modified: Mon, 28 Sep 2026 18:59:25 GMT  
		Size: 511.6 MB (511643818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2864556ae071ac34feda1546b69e61a271fe451b8638ae2ed25ed024e9144bfc`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d28d15a5211ac0d2e6ff5042ae8515288c57dd10f47665d2b35f620b137122`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf9e637921bdd744276e881cc6c85b057884853554586f58a1eeffb0237876`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ba2b9a8519815c06ac5f8a4cb69d2a69be7a39313cb2434230673387591118`  
		Last Modified: Mon, 28 Sep 2026 18:59:15 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f990301203ef3be0e06011e548326251ada41d26e6347ae69905645cedc376bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55028366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa262d8e88e5a131a71ee4355d4df2d6ff38f148819f56d1186a4c76e039a5d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0a338a97c9176d684c6ae9b4393a0387c4d9d5a310c2c4d0f00e4673aaad50`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 55.0 MB (55000711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d819f243d723b6e8fcf31b1ebd3f81c7aec98f5fa4262635b97c6730a1e8132`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ccca49d14b08518519e5b688e2aad4616afb00cd8eb680218f809c44c08bc793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.3 MB (814312281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd06ccc64f43832a4b83636f2ef5ade12f8160ec6eefc6711e630d04eec8c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 19:04:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:23 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538858bdaeb37c4fa8bb5215881ff361aa4270a0b648feb3dfbfc0ee407de75`  
		Last Modified: Mon, 28 Sep 2026 19:10:05 GMT  
		Size: 512.3 MB (512343945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4200c33b205355a49429f1fa1e0fc32acce66af58f46c9359169f016ad54579`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0214bd494b09595bf03579be8a8840dcb4b9b54fbb9b5b880457ee3f00c99`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385578020ea4dd6a58a07ffc853ebaa0d4a5198e0a718f4b572384c21ab3191`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52d7bfcc1e01bfc4b47f244e5855ea0de863d87916b0e1758e2bca695bd2c3`  
		Last Modified: Mon, 28 Sep 2026 19:09:55 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0` - unknown; unknown

```console
$ docker pull odoo@sha256:51ec8d38f6204e7f6334a40b30224238564306e7d1ed42fa9cbfbed112744b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f48ff56f3a8b8ef986ac6b5e5fd6113ccb1f295477bd6427c11792380a3c70`

```dockerfile
```

-	Layers:
	-	`sha256:b1eedb2b44faddd6e24ebd95005cea9dde1c3d2e3382be044f86db8795828039`  
		Last Modified: Mon, 28 Sep 2026 19:09:56 GMT  
		Size: 55.0 MB (55001797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a340389db09bb7869b9e803fb70bb6856e1d9507cb7c655d8d4373eea0aaf1bd`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 27.6 KB (27553 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:20.0-20260926`

```console
$ docker pull odoo@sha256:dc76c42d292af9c513de826620e5a5dbe8152383ce8767eb6ed1390a806eb32f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:20.0-20260926` - linux; amd64

```console
$ docker pull odoo@sha256:74a8a7b1520341fdf6b197791c3b34e984f4d69cc1cdb025ea0c22d9d7c8eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.8 MB (797788224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd4db2906bb95b2a538b79fcd408e2956611cfaf219b42b16d484755e0e4bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:58:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:58:45 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:58:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:58:45 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
USER odoo
# Mon, 28 Sep 2026 18:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:58:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1150a8ef4c37303490fdb702f1f7df9c8be50dde56c466a23e68637d96c8f0`  
		Last Modified: Mon, 28 Sep 2026 19:00:48 GMT  
		Size: 511.8 MB (511808215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee51fb402ac9411c10736e6800bc51d1cf79ca0e0fe65e4e9d15fea885d1293`  
		Last Modified: Mon, 28 Sep 2026 19:00:36 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee75f7b01f9a3d3431c2a51ceb92c50e7c5c9c2563521a85090ccd76af6b00`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7fc3458d3bf7099097ac31f7610e3ba0c0e58c6bc59b60a292545e9f29025d`  
		Last Modified: Mon, 28 Sep 2026 19:00:38 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08a9a0b9479d6a7bea41a041faa9efe342f03e3a05f70715b852b2703acf6b`  
		Last Modified: Mon, 28 Sep 2026 19:00:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:07c19f9cc0e22c84b1114e1fcb734569ec2e735bcfffad1cb8c307848048d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55020918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c65808c40c3f93b293bdee6620363d15a341dc0aeb102c6f931c3702ac70`

```dockerfile
```

-	Layers:
	-	`sha256:3ed60b3e57bcf2e9741e6a536b3d341d3b9b3018ec170992d059959aea3b48a7`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 55.0 MB (54993427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a71113a4602aa17bb14da2378cdb74f2285598b244cd35980441c3f97117c54`  
		Last Modified: Mon, 28 Sep 2026 19:00:33 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20.0-20260926` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:69fb42ff26749fe4970616c234e45d76f6100c965b26e36678deb83431f95a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.2 MB (794212214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e507387dad5481f5ce1bfcbe046df73b29030c80f8e98d432f6c6ec5cfcee4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:44 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:44 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:44 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:14 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df0b9cd83d3280cfbdf5afb034365f561ba426911bd4edf98921cdf0dfd724d`  
		Last Modified: Mon, 28 Sep 2026 18:59:20 GMT  
		Size: 236.2 MB (236178835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23f235a24e3c9b16557ad35f5033cf08c48987fe734037fc282077d099c0c7`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 16.6 MB (16576295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41e94aa3162b4fcbf335febe5154f081e38d699fc487edaf189b9a287809f3`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 868.9 KB (868936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec2b586f2e9064667fef06c5b73365d39d2e292ffc30eb4f683230c165e6ca1`  
		Last Modified: Mon, 28 Sep 2026 18:59:25 GMT  
		Size: 511.6 MB (511643818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2864556ae071ac34feda1546b69e61a271fe451b8638ae2ed25ed024e9144bfc`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d28d15a5211ac0d2e6ff5042ae8515288c57dd10f47665d2b35f620b137122`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf9e637921bdd744276e881cc6c85b057884853554586f58a1eeffb0237876`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ba2b9a8519815c06ac5f8a4cb69d2a69be7a39313cb2434230673387591118`  
		Last Modified: Mon, 28 Sep 2026 18:59:15 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:f990301203ef3be0e06011e548326251ada41d26e6347ae69905645cedc376bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55028366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa262d8e88e5a131a71ee4355d4df2d6ff38f148819f56d1186a4c76e039a5d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0a338a97c9176d684c6ae9b4393a0387c4d9d5a310c2c4d0f00e4673aaad50`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 55.0 MB (55000711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d819f243d723b6e8fcf31b1ebd3f81c7aec98f5fa4262635b97c6730a1e8132`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:20.0-20260926` - linux; ppc64le

```console
$ docker pull odoo@sha256:ccca49d14b08518519e5b688e2aad4616afb00cd8eb680218f809c44c08bc793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.3 MB (814312281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd06ccc64f43832a4b83636f2ef5ade12f8160ec6eefc6711e630d04eec8c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 19:04:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:23 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538858bdaeb37c4fa8bb5215881ff361aa4270a0b648feb3dfbfc0ee407de75`  
		Last Modified: Mon, 28 Sep 2026 19:10:05 GMT  
		Size: 512.3 MB (512343945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4200c33b205355a49429f1fa1e0fc32acce66af58f46c9359169f016ad54579`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0214bd494b09595bf03579be8a8840dcb4b9b54fbb9b5b880457ee3f00c99`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385578020ea4dd6a58a07ffc853ebaa0d4a5198e0a718f4b572384c21ab3191`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52d7bfcc1e01bfc4b47f244e5855ea0de863d87916b0e1758e2bca695bd2c3`  
		Last Modified: Mon, 28 Sep 2026 19:09:55 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:20.0-20260926` - unknown; unknown

```console
$ docker pull odoo@sha256:51ec8d38f6204e7f6334a40b30224238564306e7d1ed42fa9cbfbed112744b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f48ff56f3a8b8ef986ac6b5e5fd6113ccb1f295477bd6427c11792380a3c70`

```dockerfile
```

-	Layers:
	-	`sha256:b1eedb2b44faddd6e24ebd95005cea9dde1c3d2e3382be044f86db8795828039`  
		Last Modified: Mon, 28 Sep 2026 19:09:56 GMT  
		Size: 55.0 MB (55001797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a340389db09bb7869b9e803fb70bb6856e1d9507cb7c655d8d4373eea0aaf1bd`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 27.6 KB (27553 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:dc76c42d292af9c513de826620e5a5dbe8152383ce8767eb6ed1390a806eb32f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:74a8a7b1520341fdf6b197791c3b34e984f4d69cc1cdb025ea0c22d9d7c8eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.8 MB (797788224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd4db2906bb95b2a538b79fcd408e2956611cfaf219b42b16d484755e0e4bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:56:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 28 Sep 2026 18:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:57:36 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:57:36 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:58:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:58:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:58:45 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:58:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:58:45 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:58:45 GMT
USER odoo
# Mon, 28 Sep 2026 18:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:58:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde88b460eb7fe870c5edf7d27013a2fc0563622c30b6223f52cbe3e73f7c2`  
		Last Modified: Mon, 28 Sep 2026 19:00:43 GMT  
		Size: 238.7 MB (238711780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84777ec0c9bf24ba999ef92a3e68b661e6e28fe30ead0b0c1c00e2dbf56b43cd`  
		Last Modified: Mon, 28 Sep 2026 19:00:35 GMT  
		Size: 16.6 MB (16632408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636cf059bc7cc85204d88acba784f0183232d6bb5ea1ee1a055b9ead0be17310`  
		Last Modified: Mon, 28 Sep 2026 19:00:34 GMT  
		Size: 869.0 KB (868954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1150a8ef4c37303490fdb702f1f7df9c8be50dde56c466a23e68637d96c8f0`  
		Last Modified: Mon, 28 Sep 2026 19:00:48 GMT  
		Size: 511.8 MB (511808215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee51fb402ac9411c10736e6800bc51d1cf79ca0e0fe65e4e9d15fea885d1293`  
		Last Modified: Mon, 28 Sep 2026 19:00:36 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee75f7b01f9a3d3431c2a51ceb92c50e7c5c9c2563521a85090ccd76af6b00`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7fc3458d3bf7099097ac31f7610e3ba0c0e58c6bc59b60a292545e9f29025d`  
		Last Modified: Mon, 28 Sep 2026 19:00:38 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08a9a0b9479d6a7bea41a041faa9efe342f03e3a05f70715b852b2703acf6b`  
		Last Modified: Mon, 28 Sep 2026 19:00:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:07c19f9cc0e22c84b1114e1fcb734569ec2e735bcfffad1cb8c307848048d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55020918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c65808c40c3f93b293bdee6620363d15a341dc0aeb102c6f931c3702ac70`

```dockerfile
```

-	Layers:
	-	`sha256:3ed60b3e57bcf2e9741e6a536b3d341d3b9b3018ec170992d059959aea3b48a7`  
		Last Modified: Mon, 28 Sep 2026 19:00:37 GMT  
		Size: 55.0 MB (54993427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a71113a4602aa17bb14da2378cdb74f2285598b244cd35980441c3f97117c54`  
		Last Modified: Mon, 28 Sep 2026 19:00:33 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:69fb42ff26749fe4970616c234e45d76f6100c965b26e36678deb83431f95a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.2 MB (794212214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e507387dad5481f5ce1bfcbe046df73b29030c80f8e98d432f6c6ec5cfcee4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

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
# Mon, 28 Sep 2026 18:54:44 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:54:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:54:44 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:54:44 GMT
ARG TARGETARCH=arm64
# Mon, 28 Sep 2026 18:54:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:54:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 18:55:58 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 18:55:58 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 18:57:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 18:57:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 18:57:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 18:57:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 18:57:14 GMT
USER odoo
# Mon, 28 Sep 2026 18:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 18:57:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df0b9cd83d3280cfbdf5afb034365f561ba426911bd4edf98921cdf0dfd724d`  
		Last Modified: Mon, 28 Sep 2026 18:59:20 GMT  
		Size: 236.2 MB (236178835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23f235a24e3c9b16557ad35f5033cf08c48987fe734037fc282077d099c0c7`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 16.6 MB (16576295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41e94aa3162b4fcbf335febe5154f081e38d699fc487edaf189b9a287809f3`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 868.9 KB (868936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec2b586f2e9064667fef06c5b73365d39d2e292ffc30eb4f683230c165e6ca1`  
		Last Modified: Mon, 28 Sep 2026 18:59:25 GMT  
		Size: 511.6 MB (511643818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2864556ae071ac34feda1546b69e61a271fe451b8638ae2ed25ed024e9144bfc`  
		Last Modified: Mon, 28 Sep 2026 18:59:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d28d15a5211ac0d2e6ff5042ae8515288c57dd10f47665d2b35f620b137122`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf9e637921bdd744276e881cc6c85b057884853554586f58a1eeffb0237876`  
		Last Modified: Mon, 28 Sep 2026 18:59:13 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ba2b9a8519815c06ac5f8a4cb69d2a69be7a39313cb2434230673387591118`  
		Last Modified: Mon, 28 Sep 2026 18:59:15 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f990301203ef3be0e06011e548326251ada41d26e6347ae69905645cedc376bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55028366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa262d8e88e5a131a71ee4355d4df2d6ff38f148819f56d1186a4c76e039a5d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0a338a97c9176d684c6ae9b4393a0387c4d9d5a310c2c4d0f00e4673aaad50`  
		Last Modified: Mon, 28 Sep 2026 18:59:14 GMT  
		Size: 55.0 MB (55000711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d819f243d723b6e8fcf31b1ebd3f81c7aec98f5fa4262635b97c6730a1e8132`  
		Last Modified: Mon, 28 Sep 2026 18:59:10 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ccca49d14b08518519e5b688e2aad4616afb00cd8eb680218f809c44c08bc793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.3 MB (814312281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd06ccc64f43832a4b83636f2ef5ade12f8160ec6eefc6711e630d04eec8c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Sep 2026 11:54:01 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:54:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:54:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:54:04 GMT
ADD file:23a54200dc45d2e165b80cd813d76a8863b2e15710bb20b738f813328f74d05b in / 
# Fri, 11 Sep 2026 11:54:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 18:56:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 28 Sep 2026 18:56:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Sep 2026 18:56:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Sep 2026 18:56:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Sep 2026 18:56:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Sep 2026 18:56:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends nodejs npm     && npm install -g rtlcss     && apt-get purge --autoremove -y npm     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 19:01:02 GMT
ENV ODOO_VERSION=20.0
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_RELEASE=20260926
# Mon, 28 Sep 2026 19:01:02 GMT
ARG ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
# Mon, 28 Sep 2026 19:04:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Sep 2026 19:04:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Sep 2026 19:04:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260926 ODOO_SHA=7cb4a582ebe275a4f9c22eae24ce2bcb7fa27040
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Sep 2026 19:04:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Sep 2026 19:04:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Sep 2026 19:04:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Sep 2026 19:04:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Sep 2026 19:04:23 GMT
USER odoo
# Mon, 28 Sep 2026 19:04:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Sep 2026 19:04:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056e5335eeda1a995ed8e76b1a85d28b76a6c5a14082a11caf0eb7e8a3360e5`  
		Last Modified: Mon, 28 Sep 2026 19:09:44 GMT  
		Size: 249.4 MB (249411724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9b20d478d7bc13e8b5c5584b5a55ee99191a50a62d92801d4496c3078a2eb`  
		Last Modified: Mon, 28 Sep 2026 19:09:35 GMT  
		Size: 17.3 MB (17306945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74facc9a28a86e8d9f454c26a78b0ad456c1dcffcab77f8f363e061cc0ded848`  
		Last Modified: Mon, 28 Sep 2026 19:09:34 GMT  
		Size: 870.0 KB (869959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538858bdaeb37c4fa8bb5215881ff361aa4270a0b648feb3dfbfc0ee407de75`  
		Last Modified: Mon, 28 Sep 2026 19:10:05 GMT  
		Size: 512.3 MB (512343945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4200c33b205355a49429f1fa1e0fc32acce66af58f46c9359169f016ad54579`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0214bd494b09595bf03579be8a8840dcb4b9b54fbb9b5b880457ee3f00c99`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385578020ea4dd6a58a07ffc853ebaa0d4a5198e0a718f4b572384c21ab3191`  
		Last Modified: Mon, 28 Sep 2026 19:09:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52d7bfcc1e01bfc4b47f244e5855ea0de863d87916b0e1758e2bca695bd2c3`  
		Last Modified: Mon, 28 Sep 2026 19:09:55 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:51ec8d38f6204e7f6334a40b30224238564306e7d1ed42fa9cbfbed112744b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f48ff56f3a8b8ef986ac6b5e5fd6113ccb1f295477bd6427c11792380a3c70`

```dockerfile
```

-	Layers:
	-	`sha256:b1eedb2b44faddd6e24ebd95005cea9dde1c3d2e3382be044f86db8795828039`  
		Last Modified: Mon, 28 Sep 2026 19:09:56 GMT  
		Size: 55.0 MB (55001797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a340389db09bb7869b9e803fb70bb6856e1d9507cb7c655d8d4373eea0aaf1bd`  
		Last Modified: Mon, 28 Sep 2026 19:09:53 GMT  
		Size: 27.6 KB (27553 bytes)  
		MIME: application/vnd.in-toto+json
