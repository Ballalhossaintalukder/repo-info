## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:2cf1e2db1d8685d477fc8fd40b039dec25e8b54d34b405df9071ab83fdc6048a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a1f001cbce5d8b3daa2e6f3771b402195689a34e3d348f99236d46736fbb0a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.0 MB (648049421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3dd70bea920cab684e34a7066761486d21d845434105f13bd26f1010bed13a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 00:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 01:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 02:17:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cef6b9e146b59354ff9c67b76eb738a3cbd721da62af9fea96e49a9203bfbc82`  
		Last Modified: Sat, 19 Sep 2026 00:03:30 GMT  
		Size: 50.1 MB (50075078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299213d11485d48d2dc0b0cfa241bfd389b24a5597b89d1d2390ca7f7e3195f6`  
		Last Modified: Sat, 19 Sep 2026 00:44:59 GMT  
		Size: 28.3 MB (28303412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b2db1ca298518bf33f4c99ca6a64de84b79047845d9bf8b50121f5096cdf37`  
		Last Modified: Sat, 19 Sep 2026 01:24:18 GMT  
		Size: 79.8 MB (79804897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2501ba674b6ff2a62fd85c134f95011a505798b6b3fe4177b1c8b6d1225dd33e`  
		Last Modified: Sat, 19 Sep 2026 02:18:25 GMT  
		Size: 489.9 MB (489866034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6050897e88230bb4735a3465ad86d7f4d0232ff79b5a1871c0ea3cdf59b85702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16909824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf61c4272a709d8c75dd329c8aac2822e26862e3f300a190b439948870633a2`

```dockerfile
```

-	Layers:
	-	`sha256:c23258f53530b3fed857097af540b8cccb10cbe9fffec03da64f7f9d320e70b7`  
		Last Modified: Sat, 19 Sep 2026 02:18:17 GMT  
		Size: 16.9 MB (16899680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85aebf56e0ad68bf6e2f53b885cf437c36be6a16ca28ed28a0b845e9278f2a2f`  
		Last Modified: Sat, 19 Sep 2026 02:18:17 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:79502c9483831e71cfd75afe46395ce8c3c681a0efa65b1b91137606387b3a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590687181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63560c2cbd8398a08da5d310dc86302f319797680edd366411b4adaef7e0185b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 01:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 02:26:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 03:16:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c0dd4e73154d77853deb35b3302ee7d1c0dad7b51f51b93765769185d7b5842e`  
		Last Modified: Sat, 19 Sep 2026 00:03:00 GMT  
		Size: 46.5 MB (46451843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4788c3ca83a7687582f132989ac6f323df18ccef0b22e71085a93673782ba479`  
		Last Modified: Sat, 19 Sep 2026 01:28:27 GMT  
		Size: 25.5 MB (25543288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9793cbdf073ab4cf4e058006fa7c3eb2e43894cd97025d7266cf342e80a7e657`  
		Last Modified: Sat, 19 Sep 2026 02:27:11 GMT  
		Size: 73.6 MB (73575242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2a643bc64d42f4865b47d9b5d5eff389d977946146f49ee1ce8cb5ec9e9a8f`  
		Last Modified: Sat, 19 Sep 2026 03:17:39 GMT  
		Size: 445.1 MB (445116808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e7806400126a08a1d9ec6cb0e25e25a213732652fb4b158e7a585063a779534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16695033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2af0fcf7ebc595ad179f61cec7558948ce41ae5c2cff42b5216858a8263449`

```dockerfile
```

-	Layers:
	-	`sha256:cd90b7ba08b5ea9814cbcecf2e2f50ac36e4ec1c2cd2cd2399b6d01911759844`  
		Last Modified: Sat, 19 Sep 2026 03:17:29 GMT  
		Size: 16.7 MB (16684824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2cb3c8ebebdd4e4ccadc359ab40fb2acbb0fedc6f614c17a0d9125eb7095a9`  
		Last Modified: Sat, 19 Sep 2026 03:17:28 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:36e8d33f17ff347d8e4ef860fd15b64b33ce972e4a61a857d2028c9119da9fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 MB (642797380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d80f3bbcdcd0a9d64df5b73abaa6c41c75dcdd092f6065f9d4c96701044c355`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 00:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 01:31:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 02:16:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bc8b68ec4249a062f0351d0b052f82733e554595d28d36e1fb5f71baf24fcc1b`  
		Last Modified: Sat, 19 Sep 2026 00:03:17 GMT  
		Size: 49.6 MB (49556485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd35190aa3eb3f538f8f5090a5d01dbbca12a0eeeb3ecaf7ad4f8469989642`  
		Last Modified: Sat, 19 Sep 2026 00:47:36 GMT  
		Size: 27.3 MB (27308052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2cc4193f31749c0a086ffe81b14cb44f8bb234cf63fb05ba116e5b9f0fde4`  
		Last Modified: Sat, 19 Sep 2026 01:31:49 GMT  
		Size: 78.5 MB (78523478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e470fdf4e70e9c0ba1ffd055c67badadccc67150ab4c154d7b247e7833914f34`  
		Last Modified: Sat, 19 Sep 2026 02:18:10 GMT  
		Size: 487.4 MB (487409365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:616193edce7b4a5dc3d279dadaf673acb1db8f564d395ad62fad5776fc32c2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17016864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb471aeecba51f1afbcdba197cd7e02b3da948e2492c5428a8448dac1ee1578`

```dockerfile
```

-	Layers:
	-	`sha256:dc515da39210ae423846931402d0e35055d450e19f0fd2d02d82e3af4c45c868`  
		Last Modified: Sat, 19 Sep 2026 02:18:01 GMT  
		Size: 17.0 MB (17006639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b8b1adfb6909e008d963f4e58520797931e71b9de79c663dec4f699d900935`  
		Last Modified: Sat, 19 Sep 2026 02:18:00 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7466e960000b7a6ce8210f79b019042f321f5a9e05dd81b48c97cf41f3bf3026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681163195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58b9517e7e8f285f302409dadaa2d6a93d47af279409eab2be0acba25e7ce2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 00:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 01:35:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 02:17:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0eb126bb9a612ea416a905152fba9260f6164878660baff5271d28b45a7d68ac`  
		Last Modified: Sat, 19 Sep 2026 00:03:45 GMT  
		Size: 51.2 MB (51213279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5302722500c1d4e0c8017b6e1222f78d208df1afdc63a149e631ea9bababc5`  
		Last Modified: Sat, 19 Sep 2026 00:49:52 GMT  
		Size: 29.5 MB (29515371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7af518ef419662d426b01b4e1349d0a7a421bf914d2533916cdee72bad1bac`  
		Last Modified: Sat, 19 Sep 2026 01:35:54 GMT  
		Size: 81.8 MB (81755726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d24a5c1ee13df38a187ae763a38a468bc0c7951125b5fb7cf6d1a14b455ac3`  
		Last Modified: Sat, 19 Sep 2026 02:18:23 GMT  
		Size: 518.7 MB (518678819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ef2b038db8ceb7f3a8997111dabbf51fc9d7f0b445d1181a2df5547e7db366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16878835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebb8a8940d73051a01aad8ec50db50cda98c426df9aa79dc15e9e848eb33f12`

```dockerfile
```

-	Layers:
	-	`sha256:ac2a578adf2704216347f8ff4462cb182c7a1a9e77a6ba42ec7beb48aa848131`  
		Last Modified: Sat, 19 Sep 2026 02:18:14 GMT  
		Size: 16.9 MB (16868712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297bba91a18860fbfe5b08e256b9cf14b2834bd209e4d8f14803047c3a8b2c64`  
		Last Modified: Sat, 19 Sep 2026 02:18:13 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd298df11df204b806802c07192572589a507c5203e488604020cf1f2f187d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 MB (634672159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa069724207b44d8563d1a805d35132fae91a2fee204eb83d45e2f4bf5ce60ae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 03:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 09:06:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 11:48:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cb7fd76ce3e2978f396620d2ce4db34c6e31abd26f0d973e1cace0466a535365`  
		Last Modified: Sat, 19 Sep 2026 00:03:15 GMT  
		Size: 54.8 MB (54839170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbde7b92d1c7ceb8b1b93f8ec99f707204170fe93143733548c9d2c686a85fb`  
		Last Modified: Sat, 19 Sep 2026 03:16:32 GMT  
		Size: 30.4 MB (30382524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2922b9a12c908cea888f8e335ceffe240cd69711d13ba2f018d00a4c3a9bc0d`  
		Last Modified: Sat, 19 Sep 2026 09:06:51 GMT  
		Size: 86.1 MB (86059194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31d2d8f817614c96af3241f4620cb7d748e94d079b42618fca8b0fa5b2dd59`  
		Last Modified: Sat, 19 Sep 2026 11:50:32 GMT  
		Size: 463.4 MB (463391271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:906fd54a1d90ead48ecb096e6aad88a218648b412bc07ae4e502f648762558a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16912245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c871ac35887aa1e51d861ee8ad3930edf0469516ab5010c1a61afd2be0dc3f0`

```dockerfile
```

-	Layers:
	-	`sha256:9a68982095af9305077f0a810ee7886f0a843b0f9ba8a1c36f6cf155fbbd11ac`  
		Last Modified: Sat, 19 Sep 2026 11:50:23 GMT  
		Size: 16.9 MB (16902068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649be0e3082d8ac4181c6f7ecea8c8c95fdd396fd61aaac05a8615b7d92bde66`  
		Last Modified: Sat, 19 Sep 2026 11:50:22 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:470033d342a8f4f3802b8431b6f6e57d796cd9d055920d53bb46110f805f3261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518795934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa72dbe895b92778ff3220f92778ae337d1c8038ca35c3f40a6e4436f67bb2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1789689600'
# Thu, 24 Sep 2026 23:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 29 Sep 2026 00:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 30 Sep 2026 02:32:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf3253bbe95a1084c47d384bd326e2e3ea3a863f4a42281ad8260ddc95d7b83e`  
		Last Modified: Sat, 19 Sep 2026 03:52:30 GMT  
		Size: 47.6 MB (47644100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac10860ca9f6ee9ff6d460a6f6932521f283b32c9b77cd3475d4d427e5658cf4`  
		Last Modified: Thu, 24 Sep 2026 23:36:57 GMT  
		Size: 27.5 MB (27464051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52708233344dc3c47f7e9e73c553d8f9936b5c6c221a474fe445dc7aa1c07e2b`  
		Last Modified: Tue, 29 Sep 2026 00:13:37 GMT  
		Size: 78.5 MB (78535451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64196d62b52fd78ee7db2ffc8e5985887e6c05c0a4edecc59e337132700b6e98`  
		Last Modified: Wed, 30 Sep 2026 02:49:48 GMT  
		Size: 365.2 MB (365152332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fd566457823aa0ce5bd284fd16e497e9c2fdf591e524d8ce665a941e7aa29d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df108a837559002394cb6817a37e0da9a6ee26c253c8126f81d0f064e370521a`

```dockerfile
```

-	Layers:
	-	`sha256:818a9bb62a562b3443e5bd717512de8f010854225fc46406bb83fbb8dc85bc10`  
		Last Modified: Wed, 30 Sep 2026 02:48:56 GMT  
		Size: 17.0 MB (16970325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d723666b252abbeaf162de01f8aecf6bcdecd10e3b5e742700b8f2fc85db939c`  
		Last Modified: Wed, 30 Sep 2026 02:48:51 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2f4e2ca4affae61b47bbb1671da8541126b64dd61227d9d00734d52d85e78e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.6 MB (587597146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf93343e618cdc8f45ad6d39caefbd035a4a9d4fb3de4d001eadb2b547b0d89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1789689600'
# Sat, 19 Sep 2026 00:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 01:38:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 19 Sep 2026 02:15:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:00ec1575105e35cd5f9de7595058425838bb280d5ebcf3a21e441c789789cbb0`  
		Last Modified: Sat, 19 Sep 2026 00:02:10 GMT  
		Size: 49.3 MB (49326582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba1811152ba63201f9e1cf242891f09afd424d2ef3908d7fd84818e3ae9f8f5`  
		Last Modified: Sat, 19 Sep 2026 00:58:16 GMT  
		Size: 27.7 MB (27662346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9ec302172397ae02f03cc112fbbbc6b2b32db208613b2e9d7520361db4bad0`  
		Last Modified: Sat, 19 Sep 2026 01:39:06 GMT  
		Size: 79.9 MB (79906678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51997c9abc8af82a881339f22a4d35e481c1b08685cf13b91212f7b7dd81ff1`  
		Last Modified: Sat, 19 Sep 2026 02:16:33 GMT  
		Size: 430.7 MB (430701540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbe1651d992941144159b8c6c1637f9a2bd8ef4c0f3d8746406e7fc12fe02a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16715099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45cdd103b235c954faca3d036f254022bdaf5579fbf824cabe15d41b41d1c98`

```dockerfile
```

-	Layers:
	-	`sha256:bdc334aebe74a01ac895f6b556e0f808d2c183d2af989b127a644c8555c1c446`  
		Last Modified: Sat, 19 Sep 2026 02:16:26 GMT  
		Size: 16.7 MB (16704954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a06a54be660f7604cdc3cf618c3625ff683f048ea978691051c77d611aaab4a0`  
		Last Modified: Sat, 19 Sep 2026 02:16:24 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
