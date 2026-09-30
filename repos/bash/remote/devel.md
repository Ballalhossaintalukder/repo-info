## `bash:devel`

```console
$ docker pull bash@sha256:25364489302cdb1d0b66c5bb6acecf39f2f700bce88834e62a71ba330ccb06d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:9db68232257f562de3242c733c2128cb73ee2e7389b6549eddfdc292868fe76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7f85ea24f412e4142ed8e44050428aeb9466f00ca5e523f25ccc41ee39249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:20 GMT
ADD alpine-minirootfs-3.24.2-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:20 GMT
CMD ["/bin/sh"]
# Tue, 29 Sep 2026 22:05:28 GMT
ENV _BASH_COMMIT=1c20880e1683aaabc887a1358c98cdb9c169a630
# Tue, 29 Sep 2026 22:05:28 GMT
ENV _BASH_VERSION=devel-20260923
# Tue, 29 Sep 2026 22:05:28 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 29 Sep 2026 22:06:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Sep 2026 22:06:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:06:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:06:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e2de96513ba9eb53b431787ec8a65cdde380ac4772a3e4c4b714dcfde2a102b5`  
		Last Modified: Thu, 17 Sep 2026 20:37:26 GMT  
		Size: 3.8 MB (3849738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44c3cbb0c4d472d00f258e3267bfb68201df02da715e5971a8ea15628c33f95`  
		Last Modified: Tue, 29 Sep 2026 22:06:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2ff31f94eb7de11cda72d051d05c951ebd68d5fd2b6218210733015c07e404`  
		Last Modified: Tue, 29 Sep 2026 22:06:08 GMT  
		Size: 3.1 MB (3054306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bb0363be44267e861a5e96d5ce25f195abe498921f5f65efb78abbe47f20f4`  
		Last Modified: Tue, 29 Sep 2026 22:06:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a7781c7ee7c3a7325028c2a36b55caebaccbee16bd5a35095c2f9a0b659f72e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb2179a044a372955c86e18e906d4f3101606857c9ad1b33c365cb14a39ec99`

```dockerfile
```

-	Layers:
	-	`sha256:d65a95cf7eac5553f321ef0553c469398551d957f350bd1477b7d9ba7cbc46e4`  
		Last Modified: Tue, 29 Sep 2026 22:06:08 GMT  
		Size: 117.1 KB (117128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e0c6e626201f43b53f30def0c47afc599b828584091270b70f94253759446e`  
		Last Modified: Tue, 29 Sep 2026 22:06:08 GMT  
		Size: 18.2 KB (18212 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:7be12d2f18d0d8b56a522cd7c5e6bb993fb4cb959867d8534901db4a9b794d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17f4817210a54045d17f7db927686d203e7d849ba0eddf18c4fbb631528fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:46 GMT
ADD alpine-minirootfs-3.24.2-armhf.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:46 GMT
CMD ["/bin/sh"]
# Thu, 17 Sep 2026 21:15:23 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Thu, 17 Sep 2026 21:15:23 GMT
ENV _BASH_VERSION=devel-20260908
# Thu, 17 Sep 2026 21:15:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 17 Sep 2026 21:16:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 17 Sep 2026 21:16:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Sep 2026 21:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Sep 2026 21:16:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f218cc0a85b16ce88f0b295e09ea08f059389ba0e628af7344be20a2700e9091`  
		Last Modified: Thu, 17 Sep 2026 20:37:51 GMT  
		Size: 3.6 MB (3555113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa963f6f0d5787e6fb69328574afc44d3ecfc3f954fb195f2d99c7fd8f7de326`  
		Last Modified: Thu, 17 Sep 2026 21:16:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5cf8fc554f52f4f85cfb08b3e08da148bffbcbc8eda92736b62090aa94f95b`  
		Last Modified: Thu, 17 Sep 2026 21:16:12 GMT  
		Size: 3.0 MB (3011874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685d99d4479b9cec9d39b325abf24b9adfa52dc03223a7ddd80e7d422407c18e`  
		Last Modified: Thu, 17 Sep 2026 21:16:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0b3d4918cea135ffb190cc19e9d89b094a61f0e36894043a6496a66cf2df569d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c15ec64a018647e6e17534787c3c1de8d06f0b0b793c04e1c49f593bf9fa148`

```dockerfile
```

-	Layers:
	-	`sha256:50c272a695805870e60f1b4c8a2cb3ee4633b2bf521c7b1e54260a48263c6706`  
		Last Modified: Thu, 17 Sep 2026 21:16:11 GMT  
		Size: 18.1 KB (18113 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:2a53c3f9653384491eed477d943ec3b56f3034c7be6db8db2e27cec63098ecfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf952f3db5ddf79a36729aff84a94822873578b250e523aac1d1e60f44a7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:03 GMT
ADD alpine-minirootfs-3.24.2-armv7.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Sep 2026 21:12:37 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Thu, 17 Sep 2026 21:12:37 GMT
ENV _BASH_VERSION=devel-20260908
# Thu, 17 Sep 2026 21:12:37 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 17 Sep 2026 21:13:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 17 Sep 2026 21:13:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Sep 2026 21:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Sep 2026 21:13:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b694adf9dd1b9680f02f1458dca365ef3c3afa077ecb86f4c1ae12b519305e0`  
		Last Modified: Thu, 17 Sep 2026 20:37:09 GMT  
		Size: 3.3 MB (3265202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50180b6e76dc2a1f8207a58994432d111c4f369d51c5ad19c9ee1157c90a293`  
		Last Modified: Thu, 17 Sep 2026 21:13:26 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97860c177ceb34a2c4d0248e57817056c8b0abacfe6ce74cb6eca347cf6756cc`  
		Last Modified: Thu, 17 Sep 2026 21:13:26 GMT  
		Size: 3.0 MB (2959300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2310dfc8e03bc06a5e7f6520d62ec21211a03c5a7c58730e9ff102453b7661b`  
		Last Modified: Thu, 17 Sep 2026 21:13:26 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:17f3eeae4342f2a0b1227525833d90ff046262186d1cba422f18cfbdbbc4df5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99edb8a9a223fe6a9a3f9aee2231662856d0396686030c9bc0b31a4d5626b1a2`

```dockerfile
```

-	Layers:
	-	`sha256:7d411b469b3ec8f6bbfaf6c3d7a05cb52fd0b8afd1c3cd80fe42bc059a488b89`  
		Last Modified: Thu, 17 Sep 2026 21:13:26 GMT  
		Size: 116.5 KB (116514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042dadce2768b182cc0ac570a1461574c49826b070586b3acefdb49cbe67e366`  
		Last Modified: Thu, 17 Sep 2026 21:13:26 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:784280743ef28ecc738dc684856034fbf1c84b4142537a87e8a4ddbecaf7d594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7315542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce95d96363210ddda6c89cae0d5b16ca7a85724053049b72d0f940f55741fd6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:05 GMT
ADD alpine-minirootfs-3.24.2-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:05 GMT
CMD ["/bin/sh"]
# Thu, 17 Sep 2026 21:13:24 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Thu, 17 Sep 2026 21:13:24 GMT
ENV _BASH_VERSION=devel-20260908
# Thu, 17 Sep 2026 21:13:24 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 17 Sep 2026 21:14:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 17 Sep 2026 21:14:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Sep 2026 21:14:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Sep 2026 21:14:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a9986cd6f37dbddae7862a6d4be71683472e7c2ea708e87db14f8a6393c00f00`  
		Last Modified: Thu, 17 Sep 2026 20:37:10 GMT  
		Size: 4.2 MB (4187659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8231b54a2bc3b3ee5da46b1aa04ac540d04bdd0bc950e3f92dbb8d7ee39b8c5b`  
		Last Modified: Thu, 17 Sep 2026 21:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8e244d5073b2d400556066bcbccb1817e7e3425e81ffb061af2b33f64c52c6`  
		Last Modified: Thu, 17 Sep 2026 21:14:10 GMT  
		Size: 3.1 MB (3127097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8b0d3a50d1cb7e9e6c0d1a5523c2f781bf1502f28ce22db7949f676aed69da`  
		Last Modified: Thu, 17 Sep 2026 21:14:10 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:decaa9678a7ad09d725dcbcd4ea19c5875b4081417603b9928fd20b5ed47f4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6faa26e2a04cc1d6d14f2fe75d8c516f0d4c0ef090e4826206eb2a339c680b`

```dockerfile
```

-	Layers:
	-	`sha256:f19d654d5d35d422253d972d3e6150b02f4625f8c7b7d340257cc96d9952e26b`  
		Last Modified: Thu, 17 Sep 2026 21:14:10 GMT  
		Size: 116.5 KB (116534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aca3d219c123ee456bc83c2f9511211dd7fb0d2dcb58b2e0cce16fa34818224`  
		Last Modified: Thu, 17 Sep 2026 21:14:10 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:eccc62d875fabf254643173c6150e782b0295273d3b81de9522818e462a97cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6657535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f372b159cc45ec8b1aa0c0de23066560d0b3c96fc746e7bbab302365bc25c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:15 GMT
ADD alpine-minirootfs-3.24.2-x86.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:15 GMT
CMD ["/bin/sh"]
# Tue, 29 Sep 2026 22:05:11 GMT
ENV _BASH_COMMIT=1c20880e1683aaabc887a1358c98cdb9c169a630
# Tue, 29 Sep 2026 22:05:11 GMT
ENV _BASH_VERSION=devel-20260923
# Tue, 29 Sep 2026 22:05:11 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 29 Sep 2026 22:05:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Sep 2026 22:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:05:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7be2e280ebe651ae43469c64580d088eda7831741949c39082fb6d3333d52edd`  
		Last Modified: Thu, 17 Sep 2026 20:37:21 GMT  
		Size: 3.7 MB (3676781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f99d135243a594c63f882c098ca9ca306adb583cf085f0f5d0238896958968`  
		Last Modified: Tue, 29 Sep 2026 22:05:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c858f716e9f0469b1985819970127e8a042ebb8cc4aa68cdcea824d4bb31a17e`  
		Last Modified: Tue, 29 Sep 2026 22:05:54 GMT  
		Size: 3.0 MB (2979965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e3a28afa854bfd82b759fcd0757609ecd5e243e4f2e326d223676fc2f9803`  
		Last Modified: Tue, 29 Sep 2026 22:05:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d9e501050df99a8a4b293142f9c63a8c0346c33c5392114a79b42c8928ebc2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e052b1300dc633ad1e515cd1935183a5b37c1a2e16b70c723f6560ee1351125c`

```dockerfile
```

-	Layers:
	-	`sha256:03ce492fb19513f120f2fa3ac47d80a1c95db6e5f19be2bd3e5cf2df03dda6f9`  
		Last Modified: Tue, 29 Sep 2026 22:05:54 GMT  
		Size: 117.1 KB (117103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6277b2807494f3f51bea09b47aa8fa190d17f33c5b26b41f003b1d9f9ebc790f`  
		Last Modified: Tue, 29 Sep 2026 22:05:54 GMT  
		Size: 18.2 KB (18179 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:e4243e8122d997f91d7d3aa230bc815813cebfdadbb4b196771bfe09d9a03d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3965e60327f83f80ecf8b870f8df64613da03dee7745a9d0c714ebf3f329dbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 20:36:41 GMT
ADD alpine-minirootfs-3.24.2-ppc64le.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:36:41 GMT
CMD ["/bin/sh"]
# Thu, 17 Sep 2026 21:11:45 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Thu, 17 Sep 2026 21:11:45 GMT
ENV _BASH_VERSION=devel-20260908
# Thu, 17 Sep 2026 21:11:45 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 17 Sep 2026 21:12:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 17 Sep 2026 21:12:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Sep 2026 21:12:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Sep 2026 21:12:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ba454b17b5e915ee06cfc2c66078f1264549d4f6cdd08dc18cd56fdaaa487b25`  
		Last Modified: Thu, 17 Sep 2026 20:36:53 GMT  
		Size: 3.8 MB (3817477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa30614ad12fc6e50d3d0bdcb95ada31353334536daa086de9c3c4b886eaba1`  
		Last Modified: Thu, 17 Sep 2026 21:13:06 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8fe3a95fbad8219f7582afa914e9ded07ed2a41c6bf637d511f359ecfad52`  
		Last Modified: Thu, 17 Sep 2026 21:13:06 GMT  
		Size: 3.4 MB (3368296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6801cb4b9227a69a4aa1e023cd058e4bb9571f1b5cc73b7678e6e78c5a06bc63`  
		Last Modified: Thu, 17 Sep 2026 21:13:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6b1915602c91af0342c414589cccd787c0934195a9403f501cac013de2135f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e845688ec2a3a2575e42bb9354d174eafc40b09dbdecadc21f5805d23642d6b1`

```dockerfile
```

-	Layers:
	-	`sha256:cda6c14f88928f7f960de4fff99ffff4a60d141d80a20d22e9e23574d3fdef94`  
		Last Modified: Thu, 17 Sep 2026 21:13:06 GMT  
		Size: 116.5 KB (116511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad9674ceb8856ece169a0566b70ba6c31f6f151fc5d85db327d70777ac8a2d7`  
		Last Modified: Thu, 17 Sep 2026 21:13:06 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:c8c63214f1695b782b8b6c1ca0f7214567845abb17cf37fb513b636d8ec67415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6820333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0d3f5f606b0e8cb7fc33379caca3f5be036a1e20b76623849978f4660e3979`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 16:49:18 GMT
ADD alpine-minirootfs-3.24.2-riscv64.tar.gz / # buildkit
# Fri, 18 Sep 2026 16:49:18 GMT
CMD ["/bin/sh"]
# Sat, 19 Sep 2026 02:06:21 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Sat, 19 Sep 2026 02:06:21 GMT
ENV _BASH_VERSION=devel-20260908
# Sat, 19 Sep 2026 02:06:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Sat, 19 Sep 2026 02:15:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Sat, 19 Sep 2026 02:15:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 19 Sep 2026 02:15:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Sep 2026 02:15:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:64f7f08b6763becdda2e72bfacdfd36663e4847bc6fdb366336127620012bc02`  
		Last Modified: Fri, 18 Sep 2026 16:49:42 GMT  
		Size: 3.6 MB (3575371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f9703cc9344fbd3f99a9ef07e8e8e00c6b237a05a76e6332b04eff5f6c2e1`  
		Last Modified: Sat, 19 Sep 2026 02:16:05 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e2463deb4fbe4fd15b2ddf17a5c23c1b74d507a22d5e54faf5c83ba4840d8`  
		Last Modified: Sat, 19 Sep 2026 02:16:05 GMT  
		Size: 3.2 MB (3244167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb62aca0e4b354948c5840b43b611bd9f33d7ac099c81ddeeef4952d0a214d63`  
		Last Modified: Sat, 19 Sep 2026 02:16:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:20b172cb70a57244f35d58b47211b3273b952f047d5e8f8c375bfc5ac40c78f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f83f671e584c9f1a66ac19bb859911671c442eba825fc9d82eed0b3c9e820`

```dockerfile
```

-	Layers:
	-	`sha256:38687a61d7d541085c4c6739ef12af2450f8ced168d81ebf023798806350f2fd`  
		Last Modified: Sat, 19 Sep 2026 02:16:05 GMT  
		Size: 116.5 KB (116507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684365f175b2b53b95b3393c3ec1951a18d4b6aaabf1c4321a5c7c026464539a`  
		Last Modified: Sat, 19 Sep 2026 02:16:05 GMT  
		Size: 18.3 KB (18292 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:2fc96869fe2bd6f77434f77963f04a4c10abe59c4fbf2c878e6657046f68b526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6860056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0877e392752b81f8366f84ccafcb035a686fbb4cd297cd5a1f40578b0519127b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Sep 2026 21:38:20 GMT
ADD alpine-minirootfs-3.24.2-s390x.tar.gz / # buildkit
# Thu, 17 Sep 2026 21:38:20 GMT
CMD ["/bin/sh"]
# Thu, 17 Sep 2026 22:17:56 GMT
ENV _BASH_COMMIT=f26caaa17864b10e80056eed8fd8e2c0d5eb1b4b
# Thu, 17 Sep 2026 22:17:56 GMT
ENV _BASH_VERSION=devel-20260908
# Thu, 17 Sep 2026 22:17:56 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 17 Sep 2026 22:18:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 17 Sep 2026 22:18:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Sep 2026 22:18:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Sep 2026 22:18:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1bdda2e019dd384cc5410b8fd73c0c305664bf6db8ebc07b058877aee1a778ec`  
		Last Modified: Thu, 17 Sep 2026 21:38:29 GMT  
		Size: 3.7 MB (3715339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d371c1e5f87d9db3218df4f1975afda9cfbe49b9dc32a7dda618fb7fa20a61`  
		Last Modified: Thu, 17 Sep 2026 22:18:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a189547267f8c1f8c1d3baca9b02c1c34968f61298d8d31d1b1e631e53bc2ff5`  
		Last Modified: Thu, 17 Sep 2026 22:18:48 GMT  
		Size: 3.1 MB (3143924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc220325b33b0d318f2dfd3cc3c2d4f714c73de3cf700c7feaff6d2bbd33f02`  
		Last Modified: Thu, 17 Sep 2026 22:18:48 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8a85f155da13338674e1aa37e27ca7d117a7ab72fd676ae3ad8d21421ff76e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34053fff57eab6c34ff9cae0d2b6f4254e50770e7b93499ba8a4e4e5c3ec004`

```dockerfile
```

-	Layers:
	-	`sha256:ecddc6bbb85ee96ddaba0b78b5567df3669c13d63359c9de6eb8e9d0849f586f`  
		Last Modified: Thu, 17 Sep 2026 22:18:48 GMT  
		Size: 116.5 KB (116477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5e145c053c302305540e9c6c987b86d8afa1f4cd4fd20366b89a0c03d91d9a`  
		Last Modified: Thu, 17 Sep 2026 22:18:48 GMT  
		Size: 18.2 KB (18248 bytes)  
		MIME: application/vnd.in-toto+json
