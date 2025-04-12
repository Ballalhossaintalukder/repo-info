## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:4ca52eb5ab227649ab777d71eeb668fc4eff5bca901206f6ca671666a8a4e169
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:11f4a629036b052e09583a78ede07c30ad98973a3f2ad30ea15f342228dc7059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c328ea9370d9eb6101f9d7401032a0ebb43a5731f4abf1db3e6d14503775af0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771c768c2909767d99f6730ef0a1159de998d4d8ef8cfaf93d7b0abd78052a3`  
		Last Modified: Fri, 11 Apr 2025 17:04:18 GMT  
		Size: 3.3 MB (3339333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a88cd8e1d75810f1946774626843d6fd4cac3c9340c6f0c0280153f2f9fe0b3`  
		Last Modified: Fri, 11 Apr 2025 17:04:18 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae7fe872f4d95b2585cb5b35514ec5a03e20a1ce3ede5efd64774590f584729`  
		Last Modified: Fri, 11 Apr 2025 17:04:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c15cb39f8e6d8b7aa9aeec20dd2fb636e819590aac05632fd83c4f3823c24d7`  
		Last Modified: Fri, 11 Apr 2025 17:04:19 GMT  
		Size: 13.6 MB (13634004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7198cddc3e778d959156f3692c7f26164f3db50fd6372ab8129e53492d7f3bb`  
		Last Modified: Fri, 11 Apr 2025 17:04:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fab6d658a371c92f7dbc65effb065a9abc8499fbc443c7c06bfb19d708e6bb`  
		Last Modified: Fri, 11 Apr 2025 17:04:19 GMT  
		Size: 15.7 MB (15694946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d211649154c1f7e2155070eff90c87145755be3a4aa96348dca5683b2159e50`  
		Last Modified: Fri, 11 Apr 2025 17:04:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729caed02bf20e878325b5e981d1156fbbcde7445c54d07986c897e7cb0bed7e`  
		Last Modified: Fri, 11 Apr 2025 17:04:20 GMT  
		Size: 20.0 KB (20040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727734df4a486cef75dcb450f863122a35c869bc1b7ca6b947f58bfcdcd2dde2`  
		Last Modified: Fri, 11 Apr 2025 17:04:20 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28735a9bb34ca567cbdc50a517046c51508079e8c298a82fa2f972fadb9fdd1`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 685.0 KB (685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe4b51764aa63babe18c141c3b55238bd806a5dfdc92f4bff890068c9f8d366`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190bf3cc0631b6f919580f979ce046ec5720182aac31f1e489621f676be206bb`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 481.8 KB (481761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6c1837254ea6f3d8be2d5e7f91f3433aad02a743d560204f3d4afcc9e5f3fa`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 5.7 MB (5705147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a65458f5f8b0d09773ed132331a7d2481b148d1f66406774cd239eaa781b26`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f2af70d34f263bd311d3ba73bc99c22e285cf7a05f4ce742a99d736aabf009`  
		Last Modified: Fri, 11 Apr 2025 17:09:48 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:0ab1bb8319666c03289a29591adb6f7d4ae3c08056921c44b005064060487f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982758a3ab985a7f7bbee3c6e7862732807379786a6b0de9cd7c5ef431026094`

```dockerfile
```

-	Layers:
	-	`sha256:03f8b7f122c5a3f1a9e7e6234e37890c6be5fb4e5e272da42185a680fba5238b`  
		Last Modified: Fri, 11 Apr 2025 17:09:47 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:057cea18c387061cadb5ec22e66959f0a956f120fd404113244ddccf1d7a567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1727b9c75fd33744b27a796db1a8ff02b406727ffe8d9a35872b4a2031cda148`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99721caeced5447f0e5afae5f5f8e76005987b2b190cd4dddc22a580dfd0514`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 13.6 MB (13634008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ababb234d29b8f731d40c161eed8e52acac75254dd16fa03f85bf2beb52b5f34`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d3beb71fdd4e89530d9538edebbdf662d30df4dab595076c2339b9738e1a5`  
		Last Modified: Fri, 11 Apr 2025 17:08:48 GMT  
		Size: 15.0 MB (14956262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caefdec80f466e95cd32cd918f83514793c13e1ffd0e1c5933b5f7e27db4292c`  
		Last Modified: Fri, 11 Apr 2025 17:08:47 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052d607be03a9a7fe4f05cff1ac46eb18a9a920a6d3ab7f28fd968ff2508558`  
		Last Modified: Fri, 11 Apr 2025 17:08:47 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181206aeca0c71157b3f78ac8c8d32bc01bbcf10ef562e45e3d19713aaa9113`  
		Last Modified: Fri, 11 Apr 2025 17:08:48 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acabb0e412b701276d9c5d491ea97f0d8f1e95684ff61ec26e347325f933`  
		Last Modified: Fri, 11 Apr 2025 18:20:16 GMT  
		Size: 191.3 KB (191283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37670f6689e700495aa4d5ad1b653bead2bd9ab92b1f43fae38ba3e78b6082`  
		Last Modified: Fri, 11 Apr 2025 18:20:16 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cd427b60fc1c1aa3d1bfe370ac8856ed4aa3dba1eed834e1ac850ead6ee9aa`  
		Last Modified: Fri, 11 Apr 2025 18:20:16 GMT  
		Size: 481.3 KB (481285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988bf1c8d84af7dfd51bf910e0934dd34d6211b034b5fbc6d93a7025b50e848`  
		Last Modified: Fri, 11 Apr 2025 18:20:16 GMT  
		Size: 5.7 MB (5705147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e461d98275cac073852294fa1bf96612cec9ea061767c15d22071b27c250cf`  
		Last Modified: Fri, 11 Apr 2025 18:20:17 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da07e2ec05925d3d78b0b9c28750cde27ceea77c5803a388009caee6f81890ad`  
		Last Modified: Fri, 11 Apr 2025 18:20:17 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:87149982cf24046517b4573df5fc78b172f50d6d9a344f7991ae446a5c0bff02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73192b3a592e7e1967a6425b5edeab3c0401b9115b9abf85e1811c44ebebc58`

```dockerfile
```

-	Layers:
	-	`sha256:23de502f9eaa53c29b6079bb9d582c542ecd5e82586d3bbf370b4001abb7f56a`  
		Last Modified: Fri, 11 Apr 2025 18:20:15 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d68dac6bf81082a42e3d914965726239f84d274b170141fb6fd1cae592139881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40361209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2118293570d0e735d93570e58cda1bc419815176de3a26ff171acd198199a8`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1dd0d977bcb89dc169bd09934ab44550fcd7fa84e4c1a764504338b64dc02`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 13.6 MB (13634016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d041d9fc32e068941229ecca755921cb7bf3dca41459078370b44bc0e1716b`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8ab4e3342c80a8df6f41a65d4899692859038e198f4e96264c5fb47025e7b`  
		Last Modified: Fri, 11 Apr 2025 17:51:13 GMT  
		Size: 14.1 MB (14145921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d93e43d251d9e4493d04cf625fd93ddf17e9341f9278477fa727dfdd95582`  
		Last Modified: Fri, 11 Apr 2025 17:51:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9995c3cfa304a217b8a6930c9d1bd454daa4f229856baff2543aba82144de6`  
		Last Modified: Fri, 11 Apr 2025 17:51:13 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50424e1bb13209597d152c7e118b5f039d2a81fe222a96fb1fb88aca826cd8d`  
		Last Modified: Fri, 11 Apr 2025 17:51:13 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfb64d730ec4d3e768ea9d9afa68b00dc5ed9e7646cb87b88587b1bfaab266b`  
		Last Modified: Fri, 11 Apr 2025 19:37:02 GMT  
		Size: 178.3 KB (178323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9253a30b96814171dbdc3ca05ee611b82fde498a846e1c6401b585ccc06333`  
		Last Modified: Fri, 11 Apr 2025 19:37:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cc37a120ca8ed2b5439369ca53a45e149299b97157edc55a55d250978c070d`  
		Last Modified: Fri, 11 Apr 2025 19:37:02 GMT  
		Size: 442.0 KB (441981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ed1f650705c7651f18231652520fa372cd4b6a1b7063883cdeeb95fc65bd97`  
		Last Modified: Fri, 11 Apr 2025 19:37:02 GMT  
		Size: 5.7 MB (5705147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b01d440c8345d89f07c250f849b86989b6dd41383db17d59bc2d698a5cc222`  
		Last Modified: Fri, 11 Apr 2025 19:37:03 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87129a223f9384942a8ba324f4157f5f8192c1b85d8064b4901dce8497fd884`  
		Last Modified: Fri, 11 Apr 2025 19:37:03 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:bb9dace99c9da3238c52288945590db4405768a66712e1b097440437a70a06f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d64b0613b658bf859ee6fad8638c02c1729f8f51d1b1e025180254b1ec54ae9`

```dockerfile
```

-	Layers:
	-	`sha256:4261eff1b7da3982bde7150015c0a4c5ae2a214b73c602ba03ec9abc20d0d1bc`  
		Last Modified: Fri, 11 Apr 2025 19:37:02 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:afb92f5cfff794501179622ebdd3347930485529430ecf1c35fd4b4793723988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43934407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a477e6b5ff33d99c0a6cc7c28e5d84df9da04006e7eb6957078909cb11682a85`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eeb5b6ce9478bd6c574eb74b77f0d1b395a57ce5b3c1301f9be9922f5b8709`  
		Last Modified: Fri, 14 Feb 2025 19:55:10 GMT  
		Size: 3.3 MB (3330757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26966b371bd90aa880696c07e5efe82fae85afb1dbbdc01200a938f225097a2f`  
		Last Modified: Fri, 14 Feb 2025 19:55:09 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8ec9c416f52d757beb3b934ea2fba8bda54f1a415fee89e3c4d7160ce5971`  
		Last Modified: Fri, 14 Feb 2025 19:55:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888604a1b9394bb976269325deda07c4d8169c4cee14278818bd445ca6ace6d8`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 13.6 MB (13634025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8095d66e8713db05b04fb8f754744cdc779ee671ef4eafa9088f937e0deaa2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19f86d61818f2d0717680f9ead4e8c3e98e2738c4d27ea0e87fbd18561077c`  
		Last Modified: Fri, 11 Apr 2025 17:30:44 GMT  
		Size: 16.1 MB (16096275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b183e11fc4c52a3e1febf9344fa85d2baba6f9e4b71683e19764a9a8679c3b3`  
		Last Modified: Fri, 11 Apr 2025 17:30:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa787c6df26ec2c27849d9489d02bfea8dada030f796ece6ef9e24fd4f95ba5`  
		Last Modified: Fri, 11 Apr 2025 17:30:43 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6dc6f7164fe9f81d7bf1416c5814bd1e56b74d54ad99226ab05fbc6995d7cd`  
		Last Modified: Fri, 11 Apr 2025 17:30:43 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ca4e0bc0f70edc493832eddf1c66e9da0c341c7c2ab2b35f0b40e35a63351f`  
		Last Modified: Fri, 11 Apr 2025 19:17:44 GMT  
		Size: 601.3 KB (601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bdb5d33f33fb23e14defcdf74c5f7743e06106ee573b978d61d959cadbf9dd`  
		Last Modified: Fri, 11 Apr 2025 19:17:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca812742cb7c11eff84c410662e0fbe79b4bf4a8a2ac08abc5c1d5eafc1930`  
		Last Modified: Fri, 11 Apr 2025 19:17:44 GMT  
		Size: 536.6 KB (536572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb0a65fb942fa43bde6a602aa0a6704a3f88a9531ab273ed024b54314f1e434`  
		Last Modified: Fri, 11 Apr 2025 19:17:45 GMT  
		Size: 5.7 MB (5705142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a0df6728a562fa0bd5c64448921ea7a9a9e5baba1a07fc98d92f151592a0ec`  
		Last Modified: Fri, 11 Apr 2025 19:17:45 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7dacdf94e31e29d32380be853329a72ae41e2a3c51f8c6cf4d43a88656ef74`  
		Last Modified: Fri, 11 Apr 2025 19:17:45 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:9ef83ae5f1dd3c248a616788f49858812cab83c7a750949e596fbadda37aa30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314e1e486aa9478f145f91945d2057ca77d3ba47bcfa65891e4da3597cb1c89`

```dockerfile
```

-	Layers:
	-	`sha256:5ea06ac19523f7530cf39dab1ad1cc06cdd7059a0ebd66451a083eb3e9c149c2`  
		Last Modified: Fri, 11 Apr 2025 19:17:44 GMT  
		Size: 30.6 KB (30642 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:036d5bc2ed3ac8b14a2bc6b8a339249b924660b408489e0dd683a6dba53dd840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43508790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8844a2510099ff8ee1d06f1a7b09f7138a9a781e3d65737e61918d5c0685557a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ecafa885edcdd25affab236cc1946e45b37b115640364fb9b81d8a5850d9f`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1663a42abc582daa94d0ffd21c09399b8878e0bdbcfc8d65268372c89eb0e44`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b77953c6fb644e1aa77079c94275735d3c2525f9c26f2fa33c864ac35b0b7`  
		Last Modified: Fri, 11 Apr 2025 17:03:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17514da0cad829aa8cb12268e7daf7fdb343090bbd7ae6a0b61e3024296299f`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28683388a2e729e604f1ab8c9257a99d38fb3d6166d650bae6398ea4612863d6`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b792702d94c85cc7656fac2425a28acb49b7eb12ee4bf2c1b820d7d23c1dec2`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 16.1 MB (16088884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89016ba0374916f94e6d20680b94ebcd5ba717c47d9249905696acd90d951ef0`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba902fdf9ed8c8cfa7b488b6f757564c89b9d90438652a9bc0323c8406455c`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 20.0 KB (20045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10c4e1a1efb8932ff90f05d5abb838c62f2d55a5e54c3476fbbc8b6816ef37e`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f06950339a96a1289da08e9760bcca0858279949feddf320684a2f3a34d379`  
		Last Modified: Fri, 11 Apr 2025 17:10:14 GMT  
		Size: 710.3 KB (710339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb81a6e5e8538e8f671ca4b603cee53b026179f069f5abfb92a54aed5eaebd7`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25162128dfc840bd9315ce46498b29d4f49e73d7876c716dfaa185089ee466fd`  
		Last Modified: Fri, 11 Apr 2025 17:10:14 GMT  
		Size: 489.5 KB (489463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407675e67c418cc32b1cecad0661ac270175a7b17c1e53b82d47f4b9ae05fdaf`  
		Last Modified: Fri, 11 Apr 2025 17:10:14 GMT  
		Size: 5.7 MB (5705130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d4a7012d0163120251da713a0d7cc5af3445e39a0b712808ebd2449e0052e1`  
		Last Modified: Fri, 11 Apr 2025 17:10:14 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e767c8541835980f538047c15c8353e9e252f09ff7f092e0ed7af9cdc9901c3e`  
		Last Modified: Fri, 11 Apr 2025 17:10:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:687d2fb739d469443f719c4dcda628d7d7019ed78c574e0f8101d3b8742e97fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e2d1cfb7d5da09d2d5140d7a2bd8397a202225427d0b5f422474b3d0293b6`

```dockerfile
```

-	Layers:
	-	`sha256:890b49f0d0bf5407bbd24e2e6fe01d7ee63a2b12db70a02bd74f75ffab09a167`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 30.5 KB (30455 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:8529aee0b6b7507cf9431bd986239e0a79c86875bfe292895fdcf457faa632a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1155307af09a394e6db1630333524a6c91a8e8fe13ec60e120866051ab4bf780`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d560ffba9f9be51f581e9871fc30dcf9172500f0ab642bf3db44cad9005ba`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 13.6 MB (13634021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f992d633689cfd581ee2285b1814cf7241f57ab8b1e6b81ec099f7db10cddd31`  
		Last Modified: Fri, 11 Apr 2025 17:18:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636026e3dc0f80883927b47a97e24c48f0dec43cd8e04698de9ca62ac2d81e8`  
		Last Modified: Fri, 11 Apr 2025 17:22:30 GMT  
		Size: 17.0 MB (17000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2cc07b6e8f7b1061ce7a57f7714813b2a6213cd0afe37bdf332f8b7ff94e90`  
		Last Modified: Fri, 11 Apr 2025 17:22:29 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537265a0e87dcaa88e266bd58d797e5b9806757322b46a27c37599841410dd35`  
		Last Modified: Fri, 11 Apr 2025 17:22:29 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd820d92cf6a9b923110fe290cbf7ada41f2f4aa812bafed55b73ce20668178`  
		Last Modified: Fri, 11 Apr 2025 17:22:29 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294e9b8c9b22bde1bb75ea06d6601b330f38241bfa9fafcad06792b714664786`  
		Last Modified: Fri, 11 Apr 2025 19:23:27 GMT  
		Size: 228.3 KB (228311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172decff34842876dab31708b97678937f5fe3dc69ab35a37f92448aedbf22c7`  
		Last Modified: Fri, 11 Apr 2025 19:23:27 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad17eb448a266337a2cfef48bbfe3a653403fdaa611035d4162641a66ff4ed7`  
		Last Modified: Fri, 11 Apr 2025 19:23:27 GMT  
		Size: 547.6 KB (547605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb4aabd455454537b54658eb4e66c79b80add8ca3db913c23a90e572423ed3`  
		Last Modified: Fri, 11 Apr 2025 19:23:28 GMT  
		Size: 5.7 MB (5705147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6dc32d57fda5b1cf26dd70f29a179a894586ba28523f446813bd679329ba85`  
		Last Modified: Fri, 11 Apr 2025 19:23:28 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6f445aa1c56d97543eab06273d1ae902fcbcaff3eb5deb80d739ebee15af55`  
		Last Modified: Fri, 11 Apr 2025 19:23:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:edd81c7c1f53ae1b3aca2d22a30d336c615512cf736f9ec6326763d5d4df5517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358302205bc8e84506c59413106c6457783513fdca864ba249a8437de294ad1f`

```dockerfile
```

-	Layers:
	-	`sha256:66faeafedbacaa2bb42d13c7ba2bf1f4ae24213360326b820ae8a149458dbd4c`  
		Last Modified: Fri, 11 Apr 2025 19:23:27 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; riscv64

```console
$ docker pull yourls@sha256:ec37e5e7f73c04fcedc6983a7796dbb762f3349758f69a2e80e0728b3c4527a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41977472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f03d99aa218a147f8980d38ce82770cfcbeac479603e3d33f7c058e7d067403`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acccb6e0bcdd10c08a400b4db8b6c7bd5dd3ca2c23301728673a7f5491ccc38f`  
		Last Modified: Fri, 14 Mar 2025 01:10:04 GMT  
		Size: 13.6 MB (13625990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9ccf98b87a4802fb32b2288d08446f4a0e1b4c024ac344aab0b8e5bbb5e808`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3957f77eb3ce9edc9897baf34a81f9d23527a1426a6aa5e5bf562ad1b1727719`  
		Last Modified: Fri, 14 Mar 2025 02:13:34 GMT  
		Size: 15.1 MB (15097140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b270c1efbd4131ccc39daf10edc5c1a2c89d9c55458ddfe2192bccef71a9fd88`  
		Last Modified: Fri, 14 Mar 2025 02:13:31 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e1eba187d35dec49969fc1bd73d30a90588d911df77e75fa9543cdb4627df1`  
		Last Modified: Fri, 14 Mar 2025 02:13:31 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465d71834bebdadf9368114624a1b922a66a2070d0e748b560e26871dfbd4d3`  
		Last Modified: Fri, 14 Mar 2025 02:13:32 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34408e20fc2e718610e0174fbb8ab1531f8b55a15572795113ce9fbea54eafbf`  
		Last Modified: Thu, 03 Apr 2025 17:49:31 GMT  
		Size: 203.8 KB (203847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b937e4a0f9646b247b1a33d06787fc306fcebf07df4094a9edafb1ae13ec11c3`  
		Last Modified: Thu, 03 Apr 2025 17:49:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db240e8c808932e6a31bc018d443320a562582007717f5eba2d60b9941dd00ca`  
		Last Modified: Thu, 03 Apr 2025 17:49:31 GMT  
		Size: 493.7 KB (493697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bdacebfa0b040695d1894adb30c5d00a580372af7b83f5401a7631e89e923b`  
		Last Modified: Thu, 03 Apr 2025 17:49:32 GMT  
		Size: 5.7 MB (5705141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5a8339e4c9c4c5fd1d18ff5e948019c68fc0b73ddd326b8795359ae8cfde53`  
		Last Modified: Thu, 03 Apr 2025 17:49:32 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e1d13a73627d54f6dc521b2b6e6d3800accfbd47e485828481ec2e67c5a0d`  
		Last Modified: Thu, 03 Apr 2025 17:49:32 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:09b2b86019dadcc9add629e6abe3da86e8cf06c3b15f0dc2cfd3b5b59bbb09f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcd0cbb1b309da278db1b85d7cd5f17838d6d50e9da6c501db4302bbcdb5f2b`

```dockerfile
```

-	Layers:
	-	`sha256:755dc3d3320235bbf5d8bb874b15cb9a68d081bcf51ee1ccb43d055c5a04c61e`  
		Last Modified: Thu, 03 Apr 2025 17:49:30 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:5512911c05dbb743a09dab734ab0f3ebcc67d599ecf78c1c8bac9a82796076f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43829732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a2053993c15f2c6f0a29a6c801b410f92a1f16732d7d7610745890bb1819e1`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253288de5d5858d726a01e6fb54a8ce6491ee7ad88813406dc682b718a6163b`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 13.6 MB (13634013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846313eea72572bda46ef3194365448f1a2fdab2a7deb8841505aab296e073b`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1f0559501c0940a5064155987a28eac3dfdba391cc038a2b4b2756bacdbd54`  
		Last Modified: Fri, 11 Apr 2025 20:18:20 GMT  
		Size: 16.7 MB (16689488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a3b2948b89f5b587d743a61c105bca619cd3ff941639ff3dbe7cdcba277233`  
		Last Modified: Fri, 11 Apr 2025 20:18:20 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090372dbce12897b3e838c8f4eb7d5b57ecd89e2c6cd016a20d881ef3c43955`  
		Last Modified: Fri, 11 Apr 2025 20:18:20 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bea048f24d36be606abb5e1f99e090dfd5639e867eae4ee190e05f4b0db6f5`  
		Last Modified: Fri, 11 Apr 2025 20:18:20 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d3e9070936af7ad5ae257a9727fdd1f048cefde5331690be5bbd9a15f6275`  
		Last Modified: Fri, 11 Apr 2025 21:12:00 GMT  
		Size: 219.5 KB (219464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a12f9cbdff117e207ea3d6f8714423632a1ff2c31c35169be625ce9a84f862`  
		Last Modified: Fri, 11 Apr 2025 21:12:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140de232705d6e8e216646f30ad4b56e4e581a5f702e7d4a40e0bdf0a021fb2`  
		Last Modified: Fri, 11 Apr 2025 21:12:00 GMT  
		Size: 510.6 KB (510570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf50ad04d07bfc579ed4ff3b87091ec3a51822e78695af4a6be0e3d58a147299`  
		Last Modified: Fri, 11 Apr 2025 21:12:00 GMT  
		Size: 5.7 MB (5705147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dad8fee314e2cf4853e825547df6ee7aa3dd21cb66e3d6c1d2a80695f3d83d`  
		Last Modified: Fri, 11 Apr 2025 21:12:01 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be975b9f992d52e2626b334ddf4e1ca49fb5a101fca6b7df1c8446de6c6987c`  
		Last Modified: Fri, 11 Apr 2025 21:12:01 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:86b813bf2223ae88f943f6f3e45c0c56445b0620e808661e0e5c542d32d8f0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26ce1737b85ad9d82819a6846d1da439fae610e9ec248367a3f6ca1e4570c1`

```dockerfile
```

-	Layers:
	-	`sha256:7f37af550a27482b81617f9429126a250a96ded79e9ab03bba0d7f1b8ba4ed98`  
		Last Modified: Fri, 11 Apr 2025 21:12:00 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json
