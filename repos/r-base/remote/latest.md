## `r-base:latest`

```console
$ docker pull r-base@sha256:b10a3f345a4eaa8c56ccf942720646275f70c2b1d061bde197816043db04b065
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:d99b3b8362b7d0e3c74ec68e8f1a64d4cdc24cbe5e3c450eeb14d5f428ae09eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358891167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae7f36cd2bab83d0b953b5f1b4378f4e544fa93dae003cf1ab27baf40bfc896`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1743984000'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:84ba2382b477852b9eb0f58e8c78193809a3ff42688c937f8f26ef1b5cb0b397`  
		Last Modified: Tue, 08 Apr 2025 00:23:12 GMT  
		Size: 47.5 MB (47545406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894194a8647d8e2cd52b72f9482abd0697d60bc60b684888cb6cfdb7804e2a7`  
		Last Modified: Fri, 11 Apr 2025 19:06:50 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f062bf69f38646fcf8007cafebda771b4ce7b78a72fbeccb811b6971e734cf27`  
		Last Modified: Fri, 11 Apr 2025 19:06:50 GMT  
		Size: 30.4 MB (30384258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5535e8ff3cf3704ef6dcc63b803a14df03ae5717d24544ff6804c607ce236d9b`  
		Last Modified: Fri, 11 Apr 2025 19:06:50 GMT  
		Size: 868.5 KB (868491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384fe89fbb505899d329001078810bd22cc03c2fb445b6248467d897547c6a89`  
		Last Modified: Fri, 11 Apr 2025 19:06:50 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dd6a292c811481af561c257f38f16555689395214829e67160e1712a5a5fc1`  
		Last Modified: Fri, 11 Apr 2025 19:06:55 GMT  
		Size: 280.1 MB (280089352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c5558ee537842e688c2a1efaa507ed74f675cf1bc9001fbc84015df567aa46e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12623211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21754b5dd51b431876cd338abbb2001556950509a552c338cf8fb2f9450cf7d2`

```dockerfile
```

-	Layers:
	-	`sha256:ca2c59fffb9fd704526d3b768d9242be9d363b97a67fd881f51bff6e9b21b397`  
		Last Modified: Fri, 11 Apr 2025 19:06:49 GMT  
		Size: 12.6 MB (12605071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78907243685c700f17fb3f82da60198e7e9b980895a897687db8142995ae2f31`  
		Last Modified: Fri, 11 Apr 2025 19:06:49 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:fda864029f21a3a6b38e5a52980bb5eadb71e9f4850ad4f78035a079c55ee92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339433055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cc0ca89bd64d30794846c191ef2a9fd3ab5aa3beaba97e596d5a4d9331435c`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1743984000'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9c4cb0c74a61b785b62934a6d6fd4ab95b7ed41be5718849de5c3a44f7208065`  
		Last Modified: Tue, 08 Apr 2025 00:25:28 GMT  
		Size: 47.9 MB (47922424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786264ec77371817d104197a847342249384865cb9e08c24fc2ecbb1e03771e9`  
		Last Modified: Tue, 08 Apr 2025 05:31:41 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62eb34d910240e603d3f077b06a044ab457f6971d133943041011f6aaf9a4248`  
		Last Modified: Tue, 08 Apr 2025 05:31:43 GMT  
		Size: 26.7 MB (26724306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019a00dc67c1255301c9f5316836c1e0d66db5f76f43233a155fe8a2bcba2236`  
		Last Modified: Tue, 08 Apr 2025 05:31:42 GMT  
		Size: 868.5 KB (868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e057150c8a5f8b23bc459070cf3b0d5974a25e163a1be37dc6e05c979669d898`  
		Last Modified: Tue, 08 Apr 2025 05:31:41 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ba9c30b039eff65896cae2313bfe8ac357d0c16d5615288f2546c3a3c404d3`  
		Last Modified: Tue, 08 Apr 2025 05:31:48 GMT  
		Size: 263.9 MB (263914176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f254df13cd59b57ed6004ddbd440145c60d7a851bddc94a5171763b9004c3205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12704519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9a4a59ceda25bd0acbe92eb5ff61212a0a2927fedd6f7972b9d7fc2a18d844`

```dockerfile
```

-	Layers:
	-	`sha256:f216a7ac7b5576152bd8098c743d11b700f0f572c9682797f53a1866751dd27b`  
		Last Modified: Tue, 08 Apr 2025 05:31:42 GMT  
		Size: 12.7 MB (12686238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b5ef868527ac165bb18c3e1a254f7985f52001273979d9844309a58284b196`  
		Last Modified: Tue, 08 Apr 2025 05:31:41 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:70ccbe103ea683abe93632729c75229bd03e1e29094b4372f11b767e7b1a60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352873477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe0dbadf6249e8a8b6a9ce0ff9fad58cf53cb1f58b88e1dfe6dd0411e6ebd9c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1743984000'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:94af65771ef5ac9ffd033a7f6e815eb76cbf2f6d30662a8ee31535fe2e877af3`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 51.2 MB (51205081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1bc3bc37bf3186d5e902f7a518d0bf35717f452e4cd0ba1b3142330bac9f4`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7145d40106fb401dea44aeb46892c95726cdf61c8a68e766e3801bf579cd06a`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 30.9 MB (30885971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da407ab06e695749a9529c07eceb917e5c0a2002cb5f481497b2c8897f21f46c`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a784d24729b5ffce1d8c1a9d0f0ce9ef1878ece4d5ecb2d3f1c572af5d9f7`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7dc33b44df48d88a97a6dd47e6d2966150fa8d9417343d2d459e7e8e6ee2e`  
		Last Modified: Fri, 11 Apr 2025 20:45:21 GMT  
		Size: 269.9 MB (269910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:e234faadc4714f8490d1542d567c7728af874ef754f7c4ab239a2acf696bf5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12625387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf7297d9bee6944697630ffa359de3341609442dbfe64f9fe4e967a5707f128`

```dockerfile
```

-	Layers:
	-	`sha256:0d251be70af51f8526a025b0f4025c0767032a4063ba2e996f92f8e8dd66753b`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 12.6 MB (12607206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14deaf896df33b97145024f7e527340fa5f28a806407f8cef5519bec18e712f0`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:bdeac5f48fa5c573cb54e969fbe8a1d50ade286ed781dc88cadd106c26b4d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325671966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc78a7f6f74584e16f5f3556b436a9482b4dde1f6610e4836ed8c3d8c0f2e7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1743984000'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:48a40651234402db43f1c969ef6cb47f45fce4911e1b97bd34c6c3560c0dbe3a`  
		Last Modified: Tue, 08 Apr 2025 00:26:20 GMT  
		Size: 47.6 MB (47577869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c167db55143fbe259f7b3ed883cbcdf0a48ff9bce493db0881cd8dcf6888b4e`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57addaefeb1ce4cd33eda9ba4d1089b742977d847b483ad271dc32408c68d57e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 30.0 MB (30012650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4af72354faf3ededa2b4bc1c1298685b920e62e586f339b4ee6c85786d162e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f588160484ca2e1396694a042b8799e2dd102da694535dabbfe040bfebe656`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324197b1aaf814935d08c12aff8c6e9d1e7f8bd6df1c4595d5a4af40646e321`  
		Last Modified: Fri, 11 Apr 2025 19:12:57 GMT  
		Size: 247.2 MB (247153240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ad5298a7239b73e031e3c45e2ba90ec07eaf10384aa1159b7399fc7fa46c7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12432378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656cc6e464442422307246daa629bb9a060f8660e08eacda82dbec2ca3eef028`

```dockerfile
```

-	Layers:
	-	`sha256:122fd534226a13ae34a6b62c12cdcacdb9201335e2c331eab0df98657e9529f1`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 12.4 MB (12414238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d8f9fcbe5db59720a0243a51118f9b42bac86d0b6c26c32bf377dfa7e8fe66`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json
