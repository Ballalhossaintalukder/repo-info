## `drupal:php8.4-fpm-alpine`

```console
$ docker pull drupal@sha256:56ec406b71bf29e6149cc29bc1837af859d5228610039991c2b9accdfc8dabe5
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

### `drupal:php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:17e5dd25753e80a6e56208b86fd2fc06a9d50ae84f4129e2910d8b8896816db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59204309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9313295d57a6a1f6b8b3c5a4969ead70329d16910b43655b635c40c509e38e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:49d176296fff7d4d4069e1411b797d1cc1cdfa94de4dcde2739b9a689e8fe43b`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 2.0 MB (2048603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab01087e183b00e600cbdb1daa5b0b1367a9866a3709a92fb1b14ee31f374ab6`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5724edee1d9dde4c140abc09252771722f623aea781d631a49fe81a01f353ebe`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 750.6 KB (750613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c091a348aa62424ace99dbd419c2934a89bae03a37dedb1923ec2f7b9bca52a`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2db88c4d6767cb6016c949efd79e11a6366be7b830c85b2453bcb9220d0f0a`  
		Last Modified: Fri, 11 Apr 2025 18:11:04 GMT  
		Size: 20.1 MB (20060792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:4364e6bfbe6c8835235df9745e78eea5452a22ab66d02a52e5bc71665bdc178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (395978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5808853abc4db8c78323f15450edb7c7ebdeb65523f0b22fbc3a5b65531162`

```dockerfile
```

-	Layers:
	-	`sha256:14634f68d302778be07a4e8b47066cda101c124a546707bc7f287affd7b6273b`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 362.3 KB (362289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f68f8ffaae776457d3356ec4582c19a00b896825624e3e22d5c9989ba57b19b`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 33.7 KB (33689 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:1520101cea66d4ec1e5a7e0c1d0bdd4ef19e1dd5ddcd21538c30f3680c0fbbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57514736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e6a58a8f72d096ec4d66e53881d59ce624b77479b7cd031141fcc0bc54293`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:74a54e942014de50b77fa0dfaff0c94b4e3f74dd8930fead7ec169674b951213`  
		Last Modified: Fri, 11 Apr 2025 19:07:18 GMT  
		Size: 1.4 MB (1405616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b5311bcad89326162b03e6595d2806c54006aa98953fb027d0a9c268f7bc09`  
		Last Modified: Fri, 11 Apr 2025 19:07:17 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0add51b36c30acfe290fa1eb01821709452e7bb7836aef66524a352f07084`  
		Last Modified: Fri, 11 Apr 2025 19:07:18 GMT  
		Size: 750.6 KB (750612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee2b9346adc588fbd32d230a2409ba4443402aa30bc048fe1fb87f596e78d2`  
		Last Modified: Fri, 11 Apr 2025 19:07:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113bb9934172d0ed583964ea7aee532cc62c1a7042526e137b603da5c653a86f`  
		Last Modified: Fri, 11 Apr 2025 19:07:19 GMT  
		Size: 20.1 MB (20060846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:c518337c7c4a7bc71936a1389a5d3b7f77758cffd66c127f423b81e00155d09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 KB (33629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f550046a29f6c49dfe754d6bc68a3b6ae651739431028c22ccd40922fb53e7`

```dockerfile
```

-	Layers:
	-	`sha256:d486628cc0186f6da9b54418deac84a0477a6a72bccd59062ed9d9c2234b78eb`  
		Last Modified: Fri, 11 Apr 2025 19:07:17 GMT  
		Size: 33.6 KB (33629 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:61ae04b54b9e30253e0cb0d4637e058a4ef7c0d23ca7bf576cccf78abc5b0f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56145138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c9b7181b48e0f926dbddc807378f48c9b97203ebd998fef92cdb84e6904d4a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:6de82140018df9e3aab0237f1ce895952d54a3e791830ef9b8fc0e496a20987a`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 1.3 MB (1301609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fd36cd40d47735142d28bc71df9e96e67fdaf973ab5ed944b9931e797d8a36`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414103fa4719aadc1199432f94eea055b8ab1513d8dc0caaad6eacf2f290f241`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 750.6 KB (750616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3fee8d103360f7fbecd510b8ad4d3b51d9c1fe562bb95a61ac056050a63f92`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c40149fc40701639e1d5b562edcdf7d93030b234de7341140975193a4bae123`  
		Last Modified: Fri, 11 Apr 2025 20:26:43 GMT  
		Size: 20.1 MB (20060838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:e837fa72a14eb800283fdd1d7686ee10809b95b5b9466d1d9e6c0ce5437d1c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 KB (393389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb49e862da385393ab410bcfda7008c78850b8d829b41c5e37fd1157c87223e`

```dockerfile
```

-	Layers:
	-	`sha256:4bfd1b7e142eb2ecff8e76532a8856e7376032278bbe9d8621719d493504a81e`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 359.5 KB (359544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21e0efcd8e08856c597e160f050b09109328b52f8d605cf8e6d26adcad3b71c6`  
		Last Modified: Fri, 11 Apr 2025 20:26:41 GMT  
		Size: 33.8 KB (33845 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:af7ee95d8a0d433e30dfbb5088f11e33165dd0ae5d625585642b2d44610ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cfd03501d9b6367a1e4d8b927e6ff8e471f8b9613aae200074720b5e8a51b8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:41265121985b1f2712aeefa4a14294fa0accd9c6f8d049b8305b1e8a2ade08b5`  
		Last Modified: Fri, 11 Apr 2025 20:33:24 GMT  
		Size: 2.0 MB (1960395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4887c695b6b15403382975c700541ccba9330fbe504ea83866b6a21a1882b40`  
		Last Modified: Fri, 11 Apr 2025 20:33:24 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e540ae030a5981e6cbf4ef7f52fc89a5b9200c87d9b1450ceab29642607a479`  
		Last Modified: Fri, 11 Apr 2025 20:33:24 GMT  
		Size: 750.6 KB (750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f351e71fab6fbb020d8ec561644bca3516991b5732dc3d4d16866706d51b4bdb`  
		Last Modified: Fri, 11 Apr 2025 20:33:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6a2eb0685aaa4a2ce447669bd09da55638a42529c6c66a1c59baf77182ff8e`  
		Last Modified: Fri, 11 Apr 2025 20:33:26 GMT  
		Size: 20.1 MB (20060854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:95782f4098e1648e4f4c979be6fa9b8acade11f581426849d009195040808151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 KB (393477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f610650eedc2c812064ae9633c7fe0c47c94f6bf2b08371c3c71e0578c37bd`

```dockerfile
```

-	Layers:
	-	`sha256:7e2843dd59c17a861a545002cbd0a5c325aa09f2666bff8dff26c5446b33e7bf`  
		Last Modified: Fri, 11 Apr 2025 20:33:24 GMT  
		Size: 359.6 KB (359580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca95ef060bf20a0b9028ebdc77763a87d6236b9369703f57590a6935efd735d4`  
		Last Modified: Fri, 11 Apr 2025 20:33:23 GMT  
		Size: 33.9 KB (33897 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:7228f1244f3c616c1ed566380bc076b18def70443cce1aa901a8aff4e2e387f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59570258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0678caaaed1de37fec2b5866cc63083564f48c91c04754a664df7afe48fd3690`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:eb0dd71e8513770333940e71f234df0cc13be835782ea5d203ef35f663a22326`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 2.2 MB (2158599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0be262e59397e27ed138dae39b8acbea9c883a251926b37889d65faab4208e`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2973c387fc11a6a1336bfae7591b51264f285109d70857ab35fc620616c1ba97`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 750.6 KB (750612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897a77028a59ea9ddfb4b0f942c9283e7256f46bbddfc314930480d25baaa33`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52da9f960213d4ccbc4ed714da4cc6b81936817232742f6ee5cedd23850b571`  
		Last Modified: Fri, 11 Apr 2025 18:11:12 GMT  
		Size: 20.1 MB (20060871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:702185347017e18a751a0d9cee1b34d37b3bdcf7c1ce419c3c6d3da78043014a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 KB (395870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a5fe4f80664ab7bf4a4fe12592dd48349b9c5dad02f0119ce09b169c146530`

```dockerfile
```

-	Layers:
	-	`sha256:149a6eca46252f1d3584f070df1b982c701d6a3c6b95ae3f255d1e4d2b7fdd6e`  
		Last Modified: Fri, 11 Apr 2025 18:11:10 GMT  
		Size: 362.2 KB (362244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed668dbea1c7905ea85424a2db49fdb688323a806206c53712ab54c3bfb0a57`  
		Last Modified: Fri, 11 Apr 2025 18:11:10 GMT  
		Size: 33.6 KB (33626 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:b0eeaf0ec0b8f844cc24a577be75dcca6f8af10bfff9b3512bc6370cfe9db981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60241300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433ca9de1b8f402817949b40ddca3d62fdb8dbe7694b8d6516ad7a29ffc95fd2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:defd35ccab6fb10d2b715e59289d427a372941e99174d102209fee8577002d24`  
		Last Modified: Fri, 11 Apr 2025 20:52:14 GMT  
		Size: 1.7 MB (1706194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb2f5b37804cf60a386d4eb9809a85885e96b7ef8ab7cf2df332458a5173fe`  
		Last Modified: Fri, 11 Apr 2025 20:52:14 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f38ec6e4e87aaf6d1b45f25632f98cef4de70cebc4ea4035c0c8dd8aeef236e`  
		Last Modified: Fri, 11 Apr 2025 20:52:14 GMT  
		Size: 750.6 KB (750619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa956a16a0458f09d6f51c23209878bcfc44fff6335170b09d18b9dc76f648f3`  
		Last Modified: Fri, 11 Apr 2025 20:52:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a324db4325a42784ada96ba59ecf49acdb4335fefaf6b45e9ff4395fc378292`  
		Last Modified: Fri, 11 Apr 2025 20:52:16 GMT  
		Size: 20.1 MB (20060853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:bcf84a5a9231115727c024eb6d99f9d1d255d0905d858c16b20cc58970503d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 KB (391354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe800f447922bffc806724f35a86bd565ba650b30933c3274cffee716b92c2c3`

```dockerfile
```

-	Layers:
	-	`sha256:78e53663ba779a7f3762c531028b93a4fc7672e161b02c5c214ab90cd1087143`  
		Last Modified: Fri, 11 Apr 2025 20:52:13 GMT  
		Size: 357.6 KB (357583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea94149033c301e8e4477ed35778c142a0ca410d9530298260e3d1e842c35b1c`  
		Last Modified: Fri, 11 Apr 2025 20:52:13 GMT  
		Size: 33.8 KB (33771 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:a64c395bf98f5e2e70a14cc0dd8e0f436f85cd9782afa4cb3eb83e3efb0e0a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa70937edea3fdb0982d5da076ebd943154af05389be13ebd85e5db2e5d96c0`
-	Entrypoint: `["docker-php-entrypoint"]`
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
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:9c8df2873696c1d2578cde5f8b51e273dd30a3562f0c37a9a260ba6e0238831a`  
		Last Modified: Sat, 15 Mar 2025 07:35:30 GMT  
		Size: 1.5 MB (1492370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cd04d0cf1488665ea3659282e00764dc3a6ff5d10bd4b7b8cca893471b8a2`  
		Last Modified: Sat, 15 Mar 2025 07:35:30 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b1a81397bff161ecb208f2e8243a20ed58e2859469850b00888d9510fa937`  
		Last Modified: Mon, 07 Apr 2025 18:45:39 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d231731ff878f1de3fca6d838e461db16a06dfcbfe4b2042ec9179f50dab97`  
		Last Modified: Mon, 07 Apr 2025 18:45:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4788533b83b9045142c4f8e265474772b3958acc451e625aef56f668ccee3a7b`  
		Last Modified: Mon, 07 Apr 2025 18:45:42 GMT  
		Size: 20.1 MB (20061339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:cdedb5c159cad3227f82453ecb5cede722c5f1f0b13fa7406ea5b9d3c5447479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 KB (391351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb17bcb43cadab6bf9c5d6514ad505822f2bfdedadd877c5dd6073957feae26`

```dockerfile
```

-	Layers:
	-	`sha256:c221ec36ef95ddd9987585195653398403326cd1f882507249419b673a2001a6`  
		Last Modified: Mon, 07 Apr 2025 18:45:38 GMT  
		Size: 357.6 KB (357579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a149a7d7fdec0b1b360b6a1b9ab9ed2ef52d76126fafc3ce9f49ec195e583176`  
		Last Modified: Mon, 07 Apr 2025 18:45:37 GMT  
		Size: 33.8 KB (33772 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:30e526deb452540f5d145f2f3906b3d4b9af10011e186864ac85a4925eca0810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59827891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023299f23473714c0fdeb09968f8f1688ed47faaa9c165ec2e30ee85261a566`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:4b864abc84ce10a956aa9732d993b4e2c62eade3fe60d26a3fd68a3ab20766a3`  
		Last Modified: Fri, 11 Apr 2025 21:14:34 GMT  
		Size: 1.6 MB (1625543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71575c21e47d0273b9d60bf14dddb5126255bda60fae8dc9e2cfb0d8293d86aa`  
		Last Modified: Fri, 11 Apr 2025 21:14:34 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a3133f53c0e91a95cef84ea8c0309097a1cae682846b746e7fda998f7b0cc7`  
		Last Modified: Fri, 11 Apr 2025 21:14:34 GMT  
		Size: 750.6 KB (750619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e0f0e13a0396c1146880730a9ad4fb5a63e2f03bc4d61460838079ff1ec99`  
		Last Modified: Fri, 11 Apr 2025 21:14:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c27f99a387a7ef2fac4bdccdddd47c662d78413b0b2d6a2f298dac45c121e6`  
		Last Modified: Fri, 11 Apr 2025 21:14:35 GMT  
		Size: 20.1 MB (20060862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:0a9d325d84fa4f7110af872fac5d1afe299eae8684369c433181ba57a834945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 KB (391212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8d059b5c5a54eaad3f6ab697ffd5443de4719a403e9a9228c59b9346b9b44`

```dockerfile
```

-	Layers:
	-	`sha256:4ebe803a9336bceb232c56b34330667bc9c45e4d2b34180599c56053632512a9`  
		Last Modified: Fri, 11 Apr 2025 21:14:33 GMT  
		Size: 357.5 KB (357525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362c5be51777129e4d50fd55810ccd99dec3fbedf64c1a66701a8c3b29faa506`  
		Last Modified: Fri, 11 Apr 2025 21:14:33 GMT  
		Size: 33.7 KB (33687 bytes)  
		MIME: application/vnd.in-toto+json
