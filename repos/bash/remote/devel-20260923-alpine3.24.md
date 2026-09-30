## `bash:devel-20260923-alpine3.24`

```console
$ docker pull bash@sha256:c113fcb5cac17519d4d1720430af5c04053c6c277dc1aa9b23e5705bf48125e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20260923-alpine3.24` - linux; amd64

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

### `bash:devel-20260923-alpine3.24` - unknown; unknown

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

### `bash:devel-20260923-alpine3.24` - linux; 386

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

### `bash:devel-20260923-alpine3.24` - unknown; unknown

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
