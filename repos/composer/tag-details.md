<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.8`](#composer288)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:6a441ba4ca93fecf9cdbb2966f70de4ea49bcdea1c9e88f47b6243cc44114406
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

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:ee7c7ebe6f13baa0ee96f64b514cce269c8a87cf03e0d80f8146abef81ab8d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54ab00e2479300e6fc9e5e54d825546b2f46d2ff05d658fbf2ee97efe592dd7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a02a632a8bd74a82264d92f77b1839d5276f53be2d72709fa2f3c22fe515e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 31.9 MB (31899991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117862230ee6cc0b7f43cdd0cae54b685ce0fc82bb2cc2a4a42c179b4c8e08c9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a3f29d3a3ab27b0283f718aebb0c09df7f2cbeac3cc607d39f0d5f4c7d023`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 734.7 KB (734735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:197ec87687bcd7ed960432a64c94036046d505016d5c3abfb662e5c52b954b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34bd22973e924faa0287156dd257aa0695d293d15d26503f5938be2e90a8519`

```dockerfile
```

-	Layers:
	-	`sha256:ad36e09e383ccc0b30debea84d9f833b66e463805addc69d442188dbe17a5870`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cad81707420445a0a31dcc496ff57c8054f12631e84f4504c5959f43d0a6ff8`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:b20eff724a0d497fb89d8517fe370fcbf1e78644dbc6aba243717a1183a5e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72492794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173feaba60ebf3ebc57aed2e4ddf19f357c6bbe7d9436e3e6a4463518c0d451d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdc42cf98e41db42adfbdb4958442855376712bb68a2cce50c4d6487e9589a1`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 735.4 KB (735372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4772ab84286365aef67446738386b13022299bfef402e2aa7ec5e6135cbc6`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec395881e83be02804dd7febd697ddb4b5541e385c0ecb084537093fdf3d99b`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:8f2c69407cf4fb429cfc4644e2adf7e100a5c9206a532208f1c6d1b7d41ad482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e0a17cf2696c9482c9a07941d212763d43553780719f472be67b6409a15df`

```dockerfile
```

-	Layers:
	-	`sha256:200b1e9990ad774e34a6b59ce2c06befc42fa92d3defb7b9d1a72af8c55b8a04`  
		Last Modified: Fri, 11 Apr 2025 18:10:21 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:1f535141ab1cb924ca84b844c84d3db7f99dd3b3fa6d6364cc4c046dc6e83012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69507114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832731341892c5f5ba684776b4eaad27c79e2491515856552ebcc8c4bf030112`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583da59d168f8b546b6cef11503cd8b7ad8562b49c616a0921ced4885d1e580`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 725.9 KB (725937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b08d8c440d90b3f00119b1e10440d1fbb8e7dbb33b92b0734dce08ad0eaf713`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61b8ee5bc050c7c8e68deb651b6cb41bc5f9ee46bb6bc824ad9d1464c6c04b9`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:039c128608e96558a871943c8f8fefad9e1542ba4659f67b140dd87437764704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882e46d7302d949960b3eaa1d49242db6cf573717d7694873bb3170cafdc8c0b`

```dockerfile
```

-	Layers:
	-	`sha256:5d21fde9f66e0e184cbf9a4efe23d5e6542b84be7d8d016266d39123e3ecfbfd`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc477ea8d6cb3e54ce160fdec0e69e86c94ebdd83f83a268589ea29d20046b1`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ef694efcdc83a4e5f7b8ec535327603e529e10ab592285585e34c9f08214ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75004712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffd8f8f3ad68b8978ab3f70ea8cdba155911b122812a5d3bdd78c093cdcb5c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3787342f6df2409b7f6dd8203832b8364f63725e41f5bbbaf9c22fbbfcab2ec5`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 734.9 KB (734851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78de78ac478186b2938ef9d18facd7703cb95dd2d6478f4c667aa3a48f6140f`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8d837b9b028503edf1c6817e58a4d3a0887455e615d73e236f41701df4460`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:5d6006ee3b56c7c60315c3eb3358e35ec3841ab972a06bf4cf1eaf987f71b158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4ef486774bc13d7594231f3b75ced66b742c8b1cd6dd77f66b12e57cbfb546`

```dockerfile
```

-	Layers:
	-	`sha256:fa58ea4dfab8b4b5a22b01529a8b2bc2dd08a16269e65815842dfa6ca34944ea`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ef1737b089e5031e89c2721fdb03d686929d252566d37da86d2880c3a7fccb`  
		Last Modified: Fri, 11 Apr 2025 19:25:12 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:2f562317571689d6abc1ced66e551007f23611fb969c6bd12526bf89f7502c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75116870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18a694727db6d59332132f5bd90db95172d70ba4bb0c3c081cc8e916443d46c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f85f4f2dfb4f0b3f9f5e7e36797c932f37003b63281f7a990537b442cc3b28`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 32.4 MB (32389603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d5640f20f831923510486a60383943933d6cd49285dfc8502bc03104d4fcfd`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b8c015f7d8ec37abaed6a25c282a9ce8f2b6e531fad6a084320aa98e5de58`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 746.7 KB (746651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:562c8d5e2c36f4751c7be6114fc3033b2c9856c75d710f4745e5b6f3d31abc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372654a007440a85e3afc241da8ca25a3a148c9377dbd5a3d604f1caefd70a41`

```dockerfile
```

-	Layers:
	-	`sha256:72eae1878e2a32c2dd3ad0e32c0982d062b1a44eb98c699629e415341c7fd55b`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03bba696066309fd9dc636af06aa0919748b3e2a5eb3b3e32339adf729704e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:71abdc2e26341e6d96b00a30fe57885d5c07c20ff25b57add0f0ef3cd721d4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77090045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485ed5b2afae7332d14bde45f386534b888f038558b22e66ea2b255f4ae8586c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26b1635a551030eb7f9dea805018529953631a4a2df7967c2bde38bef579e2`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 742.0 KB (741959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb2073d9e74dba37a02981096fbfc822794486111dad2a2202396d711a24d1`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12b6aa1c71a9fc2986879c4435880b94a8636e7e7822cde36aa83bc78aa89f`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:434b59051be13164883613dcd7fb2d70e12bf78bb4a4a4aa26dd1b00d71b4470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26abfa1b388a1cc555c4cf37bdc3add9bf2287676c8e716e4972e258106c44c5`

```dockerfile
```

-	Layers:
	-	`sha256:ea20134689d68d5b1bcb130768ec1c54a34a1415cd3b9c73402948b00e369870`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de99079ea128e8f31b53ce21f08c6414d6a024908180c4cb36a89658020d04f`  
		Last Modified: Fri, 11 Apr 2025 19:30:15 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:7a7c96523d067f1caf63f4e9e373763f47ac97da49546be1eff2c3b94aa59926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893a5cb82df3a701542e0e0ea97d6bad82e3bd8a31d57582ccb3058188c97e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026e9bbbd258e4be8747fc0ea92d68c37e1ba1145914e6d909f0ed0cf65986a9`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 733.0 KB (733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70614eec20fb8ff95ccd64fb1a560d8f06f8202d3d503d58122b1047398c1368`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c04e45c44986c60883898e2af5fd2db42f7c5418ccb176f4b120b14d39e17c`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3249d4f3f384dc86a5cb55946c0b52c8a80e3d017fc858e74a7ca8d4fe0beb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8747a6fd66b8072ea5bd2d7963de864e6d1163ce2534339f714a8ac82e413a2`

```dockerfile
```

-	Layers:
	-	`sha256:c108fae20e551b734ef879c777eb0632cd46812d685257130382ea6af5a1be0a`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c211df790a00531d8557a3a24f5e6c1a97e90440c9af530bb3eeb922b6dae`  
		Last Modified: Sat, 15 Mar 2025 06:54:29 GMT  
		Size: 30.5 KB (30458 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:cdcf2a426182c996441bdc1d09690e69bbf522a34f37c1f697dcdcf8af63a010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d66170d15889a16fba1886a57a65e4e98629a6775639d436158eae24d096f08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c638ab839328dcccd322fa34e84b1cd667df3860a6668e045151b94b7dd4ec3`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 738.1 KB (738126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4187ae083686809d4ce2d7311a07fddc76f98ca0183f9b2f5eef35073c673a9`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e5cc1f4f2a5f44d1223fdbbc0036a2af5c38eb3c388201358b75288c9fdbb`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:4037d0164aa20815340cc0107004be01b3ad8056714541875a08587bd4dae09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d24a9a36f30a8baa12dd5f11f2c819b10bd64decedf801ffafa2dbde19c592a`

```dockerfile
```

-	Layers:
	-	`sha256:d546369c9f0f9077efe0177b03c01e152f1ca1555a91a3f54ec49fde0567fbc6`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3cb77ddb435b83956a8eec2e52df8442c3724c31f242520b10f8c97973d54`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:6a441ba4ca93fecf9cdbb2966f70de4ea49bcdea1c9e88f47b6243cc44114406
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

### `composer:1.10` - linux; amd64

```console
$ docker pull composer@sha256:ee7c7ebe6f13baa0ee96f64b514cce269c8a87cf03e0d80f8146abef81ab8d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54ab00e2479300e6fc9e5e54d825546b2f46d2ff05d658fbf2ee97efe592dd7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a02a632a8bd74a82264d92f77b1839d5276f53be2d72709fa2f3c22fe515e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 31.9 MB (31899991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117862230ee6cc0b7f43cdd0cae54b685ce0fc82bb2cc2a4a42c179b4c8e08c9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a3f29d3a3ab27b0283f718aebb0c09df7f2cbeac3cc607d39f0d5f4c7d023`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 734.7 KB (734735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:197ec87687bcd7ed960432a64c94036046d505016d5c3abfb662e5c52b954b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34bd22973e924faa0287156dd257aa0695d293d15d26503f5938be2e90a8519`

```dockerfile
```

-	Layers:
	-	`sha256:ad36e09e383ccc0b30debea84d9f833b66e463805addc69d442188dbe17a5870`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cad81707420445a0a31dcc496ff57c8054f12631e84f4504c5959f43d0a6ff8`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:b20eff724a0d497fb89d8517fe370fcbf1e78644dbc6aba243717a1183a5e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72492794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173feaba60ebf3ebc57aed2e4ddf19f357c6bbe7d9436e3e6a4463518c0d451d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdc42cf98e41db42adfbdb4958442855376712bb68a2cce50c4d6487e9589a1`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 735.4 KB (735372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4772ab84286365aef67446738386b13022299bfef402e2aa7ec5e6135cbc6`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec395881e83be02804dd7febd697ddb4b5541e385c0ecb084537093fdf3d99b`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:8f2c69407cf4fb429cfc4644e2adf7e100a5c9206a532208f1c6d1b7d41ad482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e0a17cf2696c9482c9a07941d212763d43553780719f472be67b6409a15df`

```dockerfile
```

-	Layers:
	-	`sha256:200b1e9990ad774e34a6b59ce2c06befc42fa92d3defb7b9d1a72af8c55b8a04`  
		Last Modified: Fri, 11 Apr 2025 18:10:21 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:1f535141ab1cb924ca84b844c84d3db7f99dd3b3fa6d6364cc4c046dc6e83012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69507114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832731341892c5f5ba684776b4eaad27c79e2491515856552ebcc8c4bf030112`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583da59d168f8b546b6cef11503cd8b7ad8562b49c616a0921ced4885d1e580`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 725.9 KB (725937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b08d8c440d90b3f00119b1e10440d1fbb8e7dbb33b92b0734dce08ad0eaf713`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61b8ee5bc050c7c8e68deb651b6cb41bc5f9ee46bb6bc824ad9d1464c6c04b9`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:039c128608e96558a871943c8f8fefad9e1542ba4659f67b140dd87437764704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882e46d7302d949960b3eaa1d49242db6cf573717d7694873bb3170cafdc8c0b`

```dockerfile
```

-	Layers:
	-	`sha256:5d21fde9f66e0e184cbf9a4efe23d5e6542b84be7d8d016266d39123e3ecfbfd`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc477ea8d6cb3e54ce160fdec0e69e86c94ebdd83f83a268589ea29d20046b1`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ef694efcdc83a4e5f7b8ec535327603e529e10ab592285585e34c9f08214ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75004712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffd8f8f3ad68b8978ab3f70ea8cdba155911b122812a5d3bdd78c093cdcb5c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3787342f6df2409b7f6dd8203832b8364f63725e41f5bbbaf9c22fbbfcab2ec5`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 734.9 KB (734851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78de78ac478186b2938ef9d18facd7703cb95dd2d6478f4c667aa3a48f6140f`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8d837b9b028503edf1c6817e58a4d3a0887455e615d73e236f41701df4460`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:5d6006ee3b56c7c60315c3eb3358e35ec3841ab972a06bf4cf1eaf987f71b158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4ef486774bc13d7594231f3b75ced66b742c8b1cd6dd77f66b12e57cbfb546`

```dockerfile
```

-	Layers:
	-	`sha256:fa58ea4dfab8b4b5a22b01529a8b2bc2dd08a16269e65815842dfa6ca34944ea`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ef1737b089e5031e89c2721fdb03d686929d252566d37da86d2880c3a7fccb`  
		Last Modified: Fri, 11 Apr 2025 19:25:12 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:2f562317571689d6abc1ced66e551007f23611fb969c6bd12526bf89f7502c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75116870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18a694727db6d59332132f5bd90db95172d70ba4bb0c3c081cc8e916443d46c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f85f4f2dfb4f0b3f9f5e7e36797c932f37003b63281f7a990537b442cc3b28`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 32.4 MB (32389603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d5640f20f831923510486a60383943933d6cd49285dfc8502bc03104d4fcfd`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b8c015f7d8ec37abaed6a25c282a9ce8f2b6e531fad6a084320aa98e5de58`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 746.7 KB (746651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:562c8d5e2c36f4751c7be6114fc3033b2c9856c75d710f4745e5b6f3d31abc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372654a007440a85e3afc241da8ca25a3a148c9377dbd5a3d604f1caefd70a41`

```dockerfile
```

-	Layers:
	-	`sha256:72eae1878e2a32c2dd3ad0e32c0982d062b1a44eb98c699629e415341c7fd55b`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03bba696066309fd9dc636af06aa0919748b3e2a5eb3b3e32339adf729704e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:71abdc2e26341e6d96b00a30fe57885d5c07c20ff25b57add0f0ef3cd721d4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77090045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485ed5b2afae7332d14bde45f386534b888f038558b22e66ea2b255f4ae8586c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26b1635a551030eb7f9dea805018529953631a4a2df7967c2bde38bef579e2`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 742.0 KB (741959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb2073d9e74dba37a02981096fbfc822794486111dad2a2202396d711a24d1`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12b6aa1c71a9fc2986879c4435880b94a8636e7e7822cde36aa83bc78aa89f`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:434b59051be13164883613dcd7fb2d70e12bf78bb4a4a4aa26dd1b00d71b4470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26abfa1b388a1cc555c4cf37bdc3add9bf2287676c8e716e4972e258106c44c5`

```dockerfile
```

-	Layers:
	-	`sha256:ea20134689d68d5b1bcb130768ec1c54a34a1415cd3b9c73402948b00e369870`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de99079ea128e8f31b53ce21f08c6414d6a024908180c4cb36a89658020d04f`  
		Last Modified: Fri, 11 Apr 2025 19:30:15 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:7a7c96523d067f1caf63f4e9e373763f47ac97da49546be1eff2c3b94aa59926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893a5cb82df3a701542e0e0ea97d6bad82e3bd8a31d57582ccb3058188c97e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026e9bbbd258e4be8747fc0ea92d68c37e1ba1145914e6d909f0ed0cf65986a9`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 733.0 KB (733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70614eec20fb8ff95ccd64fb1a560d8f06f8202d3d503d58122b1047398c1368`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c04e45c44986c60883898e2af5fd2db42f7c5418ccb176f4b120b14d39e17c`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3249d4f3f384dc86a5cb55946c0b52c8a80e3d017fc858e74a7ca8d4fe0beb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8747a6fd66b8072ea5bd2d7963de864e6d1163ce2534339f714a8ac82e413a2`

```dockerfile
```

-	Layers:
	-	`sha256:c108fae20e551b734ef879c777eb0632cd46812d685257130382ea6af5a1be0a`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c211df790a00531d8557a3a24f5e6c1a97e90440c9af530bb3eeb922b6dae`  
		Last Modified: Sat, 15 Mar 2025 06:54:29 GMT  
		Size: 30.5 KB (30458 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:cdcf2a426182c996441bdc1d09690e69bbf522a34f37c1f697dcdcf8af63a010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d66170d15889a16fba1886a57a65e4e98629a6775639d436158eae24d096f08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c638ab839328dcccd322fa34e84b1cd667df3860a6668e045151b94b7dd4ec3`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 738.1 KB (738126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4187ae083686809d4ce2d7311a07fddc76f98ca0183f9b2f5eef35073c673a9`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e5cc1f4f2a5f44d1223fdbbc0036a2af5c38eb3c388201358b75288c9fdbb`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:4037d0164aa20815340cc0107004be01b3ad8056714541875a08587bd4dae09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d24a9a36f30a8baa12dd5f11f2c819b10bd64decedf801ffafa2dbde19c592a`

```dockerfile
```

-	Layers:
	-	`sha256:d546369c9f0f9077efe0177b03c01e152f1ca1555a91a3f54ec49fde0567fbc6`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3cb77ddb435b83956a8eec2e52df8442c3724c31f242520b10f8c97973d54`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:6a441ba4ca93fecf9cdbb2966f70de4ea49bcdea1c9e88f47b6243cc44114406
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

### `composer:1.10.27` - linux; amd64

```console
$ docker pull composer@sha256:ee7c7ebe6f13baa0ee96f64b514cce269c8a87cf03e0d80f8146abef81ab8d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74234886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54ab00e2479300e6fc9e5e54d825546b2f46d2ff05d658fbf2ee97efe592dd7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a02a632a8bd74a82264d92f77b1839d5276f53be2d72709fa2f3c22fe515e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 31.9 MB (31899991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117862230ee6cc0b7f43cdd0cae54b685ce0fc82bb2cc2a4a42c179b4c8e08c9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a3f29d3a3ab27b0283f718aebb0c09df7f2cbeac3cc607d39f0d5f4c7d023`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 734.7 KB (734735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:197ec87687bcd7ed960432a64c94036046d505016d5c3abfb662e5c52b954b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34bd22973e924faa0287156dd257aa0695d293d15d26503f5938be2e90a8519`

```dockerfile
```

-	Layers:
	-	`sha256:ad36e09e383ccc0b30debea84d9f833b66e463805addc69d442188dbe17a5870`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cad81707420445a0a31dcc496ff57c8054f12631e84f4504c5959f43d0a6ff8`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:b20eff724a0d497fb89d8517fe370fcbf1e78644dbc6aba243717a1183a5e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72492794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173feaba60ebf3ebc57aed2e4ddf19f357c6bbe7d9436e3e6a4463518c0d451d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdc42cf98e41db42adfbdb4958442855376712bb68a2cce50c4d6487e9589a1`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 735.4 KB (735372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4772ab84286365aef67446738386b13022299bfef402e2aa7ec5e6135cbc6`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec395881e83be02804dd7febd697ddb4b5541e385c0ecb084537093fdf3d99b`  
		Last Modified: Fri, 11 Apr 2025 18:10:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:8f2c69407cf4fb429cfc4644e2adf7e100a5c9206a532208f1c6d1b7d41ad482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e0a17cf2696c9482c9a07941d212763d43553780719f472be67b6409a15df`

```dockerfile
```

-	Layers:
	-	`sha256:200b1e9990ad774e34a6b59ce2c06befc42fa92d3defb7b9d1a72af8c55b8a04`  
		Last Modified: Fri, 11 Apr 2025 18:10:21 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:1f535141ab1cb924ca84b844c84d3db7f99dd3b3fa6d6364cc4c046dc6e83012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69507114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832731341892c5f5ba684776b4eaad27c79e2491515856552ebcc8c4bf030112`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583da59d168f8b546b6cef11503cd8b7ad8562b49c616a0921ced4885d1e580`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 725.9 KB (725937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b08d8c440d90b3f00119b1e10440d1fbb8e7dbb33b92b0734dce08ad0eaf713`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61b8ee5bc050c7c8e68deb651b6cb41bc5f9ee46bb6bc824ad9d1464c6c04b9`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:039c128608e96558a871943c8f8fefad9e1542ba4659f67b140dd87437764704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882e46d7302d949960b3eaa1d49242db6cf573717d7694873bb3170cafdc8c0b`

```dockerfile
```

-	Layers:
	-	`sha256:5d21fde9f66e0e184cbf9a4efe23d5e6542b84be7d8d016266d39123e3ecfbfd`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc477ea8d6cb3e54ce160fdec0e69e86c94ebdd83f83a268589ea29d20046b1`  
		Last Modified: Fri, 11 Apr 2025 19:40:32 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ef694efcdc83a4e5f7b8ec535327603e529e10ab592285585e34c9f08214ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75004712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffd8f8f3ad68b8978ab3f70ea8cdba155911b122812a5d3bdd78c093cdcb5c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3787342f6df2409b7f6dd8203832b8364f63725e41f5bbbaf9c22fbbfcab2ec5`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 734.9 KB (734851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78de78ac478186b2938ef9d18facd7703cb95dd2d6478f4c667aa3a48f6140f`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8d837b9b028503edf1c6817e58a4d3a0887455e615d73e236f41701df4460`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:5d6006ee3b56c7c60315c3eb3358e35ec3841ab972a06bf4cf1eaf987f71b158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4ef486774bc13d7594231f3b75ced66b742c8b1cd6dd77f66b12e57cbfb546`

```dockerfile
```

-	Layers:
	-	`sha256:fa58ea4dfab8b4b5a22b01529a8b2bc2dd08a16269e65815842dfa6ca34944ea`  
		Last Modified: Fri, 11 Apr 2025 19:25:13 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ef1737b089e5031e89c2721fdb03d686929d252566d37da86d2880c3a7fccb`  
		Last Modified: Fri, 11 Apr 2025 19:25:12 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:2f562317571689d6abc1ced66e551007f23611fb969c6bd12526bf89f7502c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75116870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18a694727db6d59332132f5bd90db95172d70ba4bb0c3c081cc8e916443d46c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f85f4f2dfb4f0b3f9f5e7e36797c932f37003b63281f7a990537b442cc3b28`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 32.4 MB (32389603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d5640f20f831923510486a60383943933d6cd49285dfc8502bc03104d4fcfd`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b8c015f7d8ec37abaed6a25c282a9ce8f2b6e531fad6a084320aa98e5de58`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 746.7 KB (746651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982964bf5dc25d697fc88d4275480861cd92899928abe423bdb0d782f121c5e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f23b8beb3fffe1cee2a316818845ac59e3634d2b74de308663a65c02d05245`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:562c8d5e2c36f4751c7be6114fc3033b2c9856c75d710f4745e5b6f3d31abc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372654a007440a85e3afc241da8ca25a3a148c9377dbd5a3d604f1caefd70a41`

```dockerfile
```

-	Layers:
	-	`sha256:72eae1878e2a32c2dd3ad0e32c0982d062b1a44eb98c699629e415341c7fd55b`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03bba696066309fd9dc636af06aa0919748b3e2a5eb3b3e32339adf729704e3`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:71abdc2e26341e6d96b00a30fe57885d5c07c20ff25b57add0f0ef3cd721d4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77090045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485ed5b2afae7332d14bde45f386534b888f038558b22e66ea2b255f4ae8586c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26b1635a551030eb7f9dea805018529953631a4a2df7967c2bde38bef579e2`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 742.0 KB (741959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb2073d9e74dba37a02981096fbfc822794486111dad2a2202396d711a24d1`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12b6aa1c71a9fc2986879c4435880b94a8636e7e7822cde36aa83bc78aa89f`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:434b59051be13164883613dcd7fb2d70e12bf78bb4a4a4aa26dd1b00d71b4470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26abfa1b388a1cc555c4cf37bdc3add9bf2287676c8e716e4972e258106c44c5`

```dockerfile
```

-	Layers:
	-	`sha256:ea20134689d68d5b1bcb130768ec1c54a34a1415cd3b9c73402948b00e369870`  
		Last Modified: Fri, 11 Apr 2025 19:30:16 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de99079ea128e8f31b53ce21f08c6414d6a024908180c4cb36a89658020d04f`  
		Last Modified: Fri, 11 Apr 2025 19:30:15 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:7a7c96523d067f1caf63f4e9e373763f47ac97da49546be1eff2c3b94aa59926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893a5cb82df3a701542e0e0ea97d6bad82e3bd8a31d57582ccb3058188c97e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026e9bbbd258e4be8747fc0ea92d68c37e1ba1145914e6d909f0ed0cf65986a9`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 733.0 KB (733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70614eec20fb8ff95ccd64fb1a560d8f06f8202d3d503d58122b1047398c1368`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c04e45c44986c60883898e2af5fd2db42f7c5418ccb176f4b120b14d39e17c`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:3249d4f3f384dc86a5cb55946c0b52c8a80e3d017fc858e74a7ca8d4fe0beb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8747a6fd66b8072ea5bd2d7963de864e6d1163ce2534339f714a8ac82e413a2`

```dockerfile
```

-	Layers:
	-	`sha256:c108fae20e551b734ef879c777eb0632cd46812d685257130382ea6af5a1be0a`  
		Last Modified: Sat, 15 Mar 2025 06:54:30 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c211df790a00531d8557a3a24f5e6c1a97e90440c9af530bb3eeb922b6dae`  
		Last Modified: Sat, 15 Mar 2025 06:54:29 GMT  
		Size: 30.5 KB (30458 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:cdcf2a426182c996441bdc1d09690e69bbf522a34f37c1f697dcdcf8af63a010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d66170d15889a16fba1886a57a65e4e98629a6775639d436158eae24d096f08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c638ab839328dcccd322fa34e84b1cd667df3860a6668e045151b94b7dd4ec3`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 738.1 KB (738126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4187ae083686809d4ce2d7311a07fddc76f98ca0183f9b2f5eef35073c673a9`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e5cc1f4f2a5f44d1223fdbbc0036a2af5c38eb3c388201358b75288c9fdbb`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:4037d0164aa20815340cc0107004be01b3ad8056714541875a08587bd4dae09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d24a9a36f30a8baa12dd5f11f2c819b10bd64decedf801ffafa2dbde19c592a`

```dockerfile
```

-	Layers:
	-	`sha256:d546369c9f0f9077efe0177b03c01e152f1ca1555a91a3f54ec49fde0567fbc6`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3cb77ddb435b83956a8eec2e52df8442c3724c31f242520b10f8c97973d54`  
		Last Modified: Fri, 11 Apr 2025 19:36:39 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:8fe8c8dcdcf9e4c5b390b60df4641cfcf115a82de2559846876fb427cd88f299
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

### `composer:2` - linux; amd64

```console
$ docker pull composer@sha256:d1f9a3724292137c09b7d2bf01b3b509d13fc61200f82e4d2b0fe2f88201ce83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74473432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a3bdf885ffdf6e3aef5d9dcf7a1bfdeadbacf2103cc12e6e0a3f404981e70c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509ab55c895beab91f6c90ae48de7d99603c66e3474f83bcc8a0ca0aedd37653`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 31.9 MB (31899867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01b194f1013b5b27b55fec92accbd224bc153115f60e65560776b367abe3da`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6de9c7a5772659e5d271fdac666c511a74f7f04a00bc38d775ba802c37137`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 973.4 KB (973397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf01bfedd4c1102169f56d2e45b053513e3640897ee956e36d9e0de21aa36df`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6e377c351d400fe1111c9c37e4c1d0f38427cda8ce59edf59ee0928ecc805`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:43d30ecf6c63136c7f4f9be50ebc49bf04ed640d168d6e9d46bd6311ea5ec872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a84b51c23284c23b023741b1d8ca93e6a8bdaacf8224072adcb7239230cd02`

```dockerfile
```

-	Layers:
	-	`sha256:ae87b4fcd3272bd830c70fbe50796918ab3bbabed5483fce8874ca479f5ed8e9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942904207b2a570e4eae3579b45678543d33798e5aa7dd3dec897f97c0d373e6`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:3ef5239220206922e5cc902a9b4e2a095820d6e5dadc3c5fe50ff6df07445b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db3d3a9609440a80e75f22fdd56c3e05a3f3323928f5221c48407278f5cd6fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a34643ac8080eb792162edf87a5d1bb6cb6200f000c6868daeadcec4ae36e`  
		Last Modified: Fri, 11 Apr 2025 18:10:58 GMT  
		Size: 973.4 KB (973376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4808aa0666e52f6471e3e966115fcd0150ddc6073a566ea060bcf43b36bbe067`  
		Last Modified: Mon, 07 Apr 2025 18:27:11 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda93248846bb795a6d366c8208532c3a525382c106ffeeec37585617f5b9f54`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:53abf5c90a9169919625e7e003337069669420ccfacb5b42bc1d2e15e0e645f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee516c854df84a65e97bdb5b9d9f8cdb67ddffce9eaa37fd01024c138ef6e05b`

```dockerfile
```

-	Layers:
	-	`sha256:5ee92ec4b1905550d532309fd56675c37817099218756d3a162ad86c2f6283ab`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:e77bc0a09419c01277bdbf065076077c92ba37c0edf629c9eadaa1615a721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69745181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75de10a053848f75afd367777db1fa36efdb47c0778e71402a77f357c9de97f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f65fd6f940c82a8c166fd24d4665f3f465b1fcbb2d103793d4656d54a1656c`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 964.0 KB (963995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9e0beff00bdf5b015f0aac204f7fe9a3066594cb59853bfbd5d271841bc56`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42c4d925094cf2a05a5ac36614a58ed0d0514c16751e5f606500b110fa43a8`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:8ce0a91cfcc894dfedb059c98d79926f62a80a459055c4227ac88ce3fadddf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7af4b9e1488223e20c7d676747db5a14248ab6c411151c1f0914c562542b9b7`

```dockerfile
```

-	Layers:
	-	`sha256:793de8e374497628c83e336e44b5671e0673982dabc76c86736d6c042caea121`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed152e48fcfd5e9bf12e9a756c4295a00364ab54210b7b5a6f4e91deeaf34e33`  
		Last Modified: Fri, 11 Apr 2025 19:41:11 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:a1d0ad849ed7139e6ee97e3a3eea4a710aa99551f254ed921e7670beab3f26f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee294a7818c30ea88f137022e8f7c42414537abe52fa0113b832c4243584a7fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83923b12588e2301b9e71a33005542c223e69335e610b0c7840e99efde924a8d`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 973.1 KB (973086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e05513a2e1f1324ee4397564bc67061ded98cba32df095ad2693ad798400041`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1547115648d094b42553472fbfdf9d84634b8ca48c7162ba31f5cbb74f83a0c6`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:bf6af03c683437e5c2448571d9df94a2888c391c5ae80cb4b5d80b74d80a5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b3e99b21bdafa208be140b4322827861ac66269ca7f502afd710672969ea28`

```dockerfile
```

-	Layers:
	-	`sha256:6644067f62b0b66dfa3a4e243910f7b0b8a69f8ba5cb7acd09823fd5997bf856`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0982021520e1a07030f1d22d009576b85ef2c9f5c3a7a9c02a49e182039bd22`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:91f259044f73c867c36c93537ea4ea299fd09c2e3fa78f5efd56a6d4c4bf4cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85288e1b13a1e952e306181f98aa841f963de0bb332bcfd1d1bc9cadcf6ca61a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054678de643e99369f09488a354017f53e9c018ffe32ff0f5a6c1a4a9863b106`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 32.4 MB (32389723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7984ef9d999bd2106c5eb4d399ea83f5d96377dbd5ff6eb722b13e11df6e62f7`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72235dc5244dc5af4e91b28c1c2cd55ce554eaef3a887fea5fcded4ce6ed38e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 987.3 KB (987302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f7a075730c760d5f8495f8a05b8db853fd3442784a9c2450c60f5bd83adcb`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4432930f16e27e5e489bd26af6eb90356679ad20f1785b6c7f9c2fc0fa1dc9e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:0cf998ee72f60117e5a2dfb60702a0bf3c8c424d07d6eec02c4757dd443b4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24260866c20c6db6c71913312bc0e7188e1728e56c4b3935a335d98e68596016`

```dockerfile
```

-	Layers:
	-	`sha256:68b6b4c0caf05a903ea4ce0314cc16d4d7333764b90904663f197d5fe04fc6e2`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a140744a8c72b499555d00d841e0d9664f4d73893e856e2a35fb640b606626d5`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:957afe8b3436a8e7f90792d3b3d6200805e998cc035c9705ab80240b39bcaeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77328254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd31b923dc64f9a52efc50fe34a509efaefc8749054cc9a187576987d9a3446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cae0199aee1f1d7675b425dd7a002b08f1c55aafbdd76c11a431bf5c6136a4`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 980.2 KB (980158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544ba637c1fbb847f3723ad515b9176fde84af1896c855c6f2a6e656a59db09`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2e04faaaa383cf0bdbf7145970c2f0efd8f0f70f917f5dcf07192cc75b0a9`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:1bfc304907c0eea715831e11bbca34587fa8558eb74854c09ecf14d571220e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255600b7aa0375c5a431914b16c1772a557741bc4180b1b14b019719ad2750d0`

```dockerfile
```

-	Layers:
	-	`sha256:dcbb644eb3e4cfe25a0778e44fa77f9c1bffd2f591a3cf96700bb04f041b89bd`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5358ecdab7bc58df4dbac1e6307865d0cf8fab94e35e63543a1729f2012eac06`  
		Last Modified: Fri, 11 Apr 2025 19:31:16 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:56990de21c9bca773b1b124b716cd66204b92be8a6437af837318e323ab73c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80230002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebfec9d1692cc828e75071fda5f0ff25f520aa87fe4580f0b2902ead0ac171a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e116d64bc7b99710ce15d59ac54326e69c760685b12a7901ee7bc480140314a8`  
		Last Modified: Mon, 07 Apr 2025 18:25:42 GMT  
		Size: 8.4 MB (8386079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226458f98d993141ed17504e38c4cd773aab2bbf8a6ffda3a2c121c75791e446`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665cae102abe189a75ef2af3451f2fbf276f2a8584b1d641c8ad383c7a867672`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a3eb24f29f53c1c2e8d25ce014ccee4a0185cc696f2c574c6d2da9fda1155897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0a6da777fbd04b4beafef8ae764ec48289a4d5e0857b3f8730a233f6a16f13`

```dockerfile
```

-	Layers:
	-	`sha256:7a7bc4fbad88fb98041126d295cf745f34e96d3526338b01abfaf49301c296f2`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 2.2 MB (2156780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e38e95f8d379d49ee6090dcccad27ba9c8b1e5405d708f047322285c7d4c3`  
		Last Modified: Mon, 07 Apr 2025 18:25:40 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:fad546c332bde77af83dee676657439d8a100f1af5e414e599427edae62c9419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576949660ee7a6f1c6d2917d8e98e673a3ee3bb67adb845c9c1dc6fffa16b4a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed50f3550c2abfcb1b9a5f45aed896719a13f4053fe85cc3914bbc582e3f5a3`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 976.5 KB (976453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b739b9129e764f75e6a59832dc964d90e2d4d36771324699de217df0ae9085d`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88c66732baa17dd7f6ec04f5671542bf12b7331761899f10921eb9ae285633`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:3e7e6d959f7598a83d628b8afa1816bec605c0a8aa3c6f5d17e0406f0d30ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8dd4b600398f57bb5894ff6fd71fe40243b0bbad2763b49ff365ce287669f5`

```dockerfile
```

-	Layers:
	-	`sha256:f85d928cff47a1cd9984fd2b5a09bb4030408d3c5a59beb89b3aa2da5e8e9790`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b4626e93f8bf63442942bb98c7b3ff0ff37481357fb211b3d564060d35c9d1`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:62ca5003b85975aff5a6fe29ab270f673f81800ee91cae01c57148e00d380005
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

### `composer:2.2` - linux; amd64

```console
$ docker pull composer@sha256:7f67814674175f073df23caf8b7c91b260a7137c533f8a803fe45958284014b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74319616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10540c1074154a7400fce6f045362a5b19fec4398ccad016970d22c8bc5d091a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f8587ed26b792c75e594eb6180abb023ce5ff41ca80ff1cb3f6957e6a561f`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 31.9 MB (31899808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9cc380879231e07691de5c5ea78ecb3c48fd1ba123f04b4199cd2ea57b702`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a381058bca45d65fc0b1d75d11afa62ffdd536a2e63f8ec53410a69e16582aa0`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 819.6 KB (819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055d851bf73a1cd79c9ee9827b9e30921b1ce6466ba2b9193cd2d55aff1f0c3d`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ef2f6b66a5614678ecb3f18212748e80795630c1052939b6eac00cfc24514`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:62846d4bfe113a3b8b99e0260b3c3dbea813ddeb6bb99a2caf4b873b5b6a4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb34fd963f132dc50b1d586d5d494bdab2563c3ecc45f4834830e0b15a7dd28`

```dockerfile
```

-	Layers:
	-	`sha256:21bb24eb1ec7e5634a14ae7cdc168c30941606b72d3e80575d3d4d680e6c15a3`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5525de3ecf05a3efcb441861b686dee89926597153e57240ce4825e160b8486`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:47d7b835171ffec0328fae7575bf8e29e75e1e866c91e0f0ffff3cb1be57ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baa72da663ecaf1ea7c583853eb9616914ccd62d14d2acde37ba57eeff56aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a7d66f5ee386637257f8a1f6bc089003e02af223a909850cf500f20b155d7`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 819.5 KB (819541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f213e26acf49ec38a850c7ff0fa23de5c8b2c17c069ac9c0902a85cf115fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb95489680753962b2de29f34d05756c60a995b837bdc5fa5e8eeefced2f56ba`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:1730724df72cd25002656a390bcde94a26888515007fea8e72cccce1c6fb0a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7410206d538eab0d239f168654d58738b3d56cb24113adcc5ec1c2da236211dc`

```dockerfile
```

-	Layers:
	-	`sha256:f95650052db6b6287a27c90ce79eb4e7846e05b6e251e80ea5f413df675831fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:89a74aee6ceff68f2e1c2321b2443464d9c6afc17b8df7c82dd314de38807cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69591459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e11c7867e7d5a0dd39f044532c925b0890cb6410e92006ac47323136fd75ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb034438936abf85793b650310894bd8bd13173aced1f7dc169fa7208e7d5bca`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 810.3 KB (810272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a0dd7b17e4584ef1b1efbf5688c229968887acdb82c8476165b39b3f5349a`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b2be749cc7fcd49eb802a71f3ac1ce66663d5dae7f71d1827f2e47d0867239`  
		Last Modified: Fri, 11 Apr 2025 19:39:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:6c93216690e2fe8247674c98e003134a7f2de7e4e7f5ba47de80d846fb5d8ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd50d65130115814f6185d2f625b813b300f82bd57128e854ae58c5c4904387`

```dockerfile
```

-	Layers:
	-	`sha256:b4d043fe6ac34149ce122ed212525bd843efbf9bd625dd9334732c703fd30d57`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca7bef7486b9cfa27052114b89b687b5e9fa6a03c0bbc106e11fcdca37e0e1`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:929cc7e998e81cd47db219e70fa257a480d636d729b103c88578aef1cd295f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cb88f4a6cac3721d08f194e49a16858bf48b009820ab3fbbce91e7db2cca1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15da7c67ee32af45a316a6f9c6c342a14223318ed0779a94c9ebf17037db04d`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 819.4 KB (819403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7789571e59cb91e330a208c04890b7ef977465021dc8e8b02602b7ab9865894`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839500dfa0ded5c129442f710c5c912a855dec8a5cb5afb7166bea3dce953ba`  
		Last Modified: Fri, 11 Apr 2025 19:24:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:9b2421f3eaff1e2cca976780d42de308c5a2047c4806c0aa1514d61da21fe221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb618408c20a5435dc2a4ae26f853bc341ca33fef495304a3d0056723a9da96a`

```dockerfile
```

-	Layers:
	-	`sha256:f04bf5edf85476ff574df13b64a1762bad84354aa9b30e36dffd41ccc91937ce`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41588df87c63458711fbaa30de2d87e937480d9edaec4f19a4b20df088c5de04`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:58e4c174b8103594f05977bd977804a3aeca612b897c189e5847f59d6a5f3549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75203837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca688659452b937358a5ec774995b2eb6cc73f93e40392279343dfe5ccc4b57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c342ad8eafb03b419ae29af4ef4059a105866abb7e43cfce9d46d6d82d7fd9`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 32.4 MB (32389724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4231e215abbfb69c86d27fc2b76e5e5340b88cd2c74399a390963ea725c605`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277eb15a82b83b148be52a1417ebd973a92ab090420deca4c42f497a41fc199`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 833.5 KB (833489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d34a5a44764514c6b3956401ca46c07fd4b8cd26f2822a1d5d79fcac0d8e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8aff9ab03e08f71c7cfa37dad17ed83c780074e269ffd3f8c529d72cf491f3`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:b959d0d1f4a8ed775e0e3eeb0a4f6a0a17a772e9f907a2eda3b44103ed910cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a4a4101e719bb7cc47398700d3d88f51a8a41348ce202664a24425858493fc`

```dockerfile
```

-	Layers:
	-	`sha256:ef336f0ece1bbfbc8013732815bea5dd2e9ace0b2038fe59bf6f3c46e2f4ba54`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7a130be4886e0992cc17ca28a845d97d4258e94933d18aa8cd64a25a17a868`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:37b0426cd93c53f5e0f1cdeb2c28f9d7b9ffa497152842bf20bd9bb1b0a2f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4bda40a0ea7330158522f1fb6d5f347ae30883be01214d636d4cba4754606f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0a36e58ec488f6c94472ac5305a4566f54edccef62ef776a2dd8e0ef07c71`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 826.4 KB (826358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e24a611fac22b50fab384e99e8176ac31d266631b646995db4c17f9ece57ae2`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c632ae1888a4dffabccc778283a3dcf18fb4e17671071f18c7483802e29eb`  
		Last Modified: Fri, 11 Apr 2025 19:29:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:b9b0a003d8cfda6b050ee6a1c11d241b2bcc8e56e1abd2081a3be51e02169f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f75030e17fa5d3af649ec522a70d16242e7e32daee2b70ea19b8040dce56d10`

```dockerfile
```

-	Layers:
	-	`sha256:99b344d2d1451234c62a01ec5f9ac9221e726c94a070c911eb994ffc9e03870c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65de8017361f5bd95197acdb9ee6c668e3c384cc8a330bf23618c20c2404e2c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:c8c9f924d43dad4966bbc045e1a0d101f1a342ec92528993a19850e9f770ce87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72661815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a13c6921667150b2cde5b0e0097252865b1cb890d09a71abba352d8e1e022c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92697fa690eb16f5f3a1f04e47a10869bcc5231665bd7f511c6b0bdc036dc8`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 817.9 KB (817892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cc89a24d8029aaa0bd6231af150db86c3620ed03d9956781752d3634b28fe`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40032bda6a57ee895b60e701cd79a2adb0e690a3c6087d54f7fdb06eda8f2488`  
		Last Modified: Sat, 15 Mar 2025 06:47:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:9b8f9221004aac4c24577c9c4c26355d63101933bcf811ffb69566e132a6ffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a749a5be401f08b78c2e9c0d9f21a9ec72ab341b7c251ad429d86dc3705b0a5`

```dockerfile
```

-	Layers:
	-	`sha256:b1e92b9f2c7997db127513c0e251912eff161f5a6b1d48c37992162fe3de25cd`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aba897460592ac0c7e2499751934a29ad36040f4ae78ae56da6e43caa705ae7`  
		Last Modified: Sat, 15 Mar 2025 06:49:13 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:22d3f1ac483a883cdac3170ec0c48534399b4614fd7b14eef991983310d52e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75441805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550c839a96536c03825b2ea784a0c6865d61f91e0a5446810a49a24476e805f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2abe1c95b14367537e000ce27b700e744674dbbf54603c7c19849713925f4f`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 822.7 KB (822682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9497720774556f9e9199ca165c9137abd44cc9521e30c99f31e99201ca6abf`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ce55bf35d81cdcc3a3502f45dcd9637bec07c398dc6b5c0483da389e68e57`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:ee3b78e48acf450beaa636f62e09931106cd4ef6acee53ee3f5a725fae3468ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd14dff933ed1c7de2454f0d532ef20288caf72647212c72add8cd14d46f08b`

```dockerfile
```

-	Layers:
	-	`sha256:acb87901ec354a0af4a7a84773ae6b0e6dbdbb11efb6892eb02f3727c7338e58`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86956f22dc6528092933cbb7a30e36a293df41719fc70b86779be850ba58e6fa`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:62ca5003b85975aff5a6fe29ab270f673f81800ee91cae01c57148e00d380005
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

### `composer:2.2.25` - linux; amd64

```console
$ docker pull composer@sha256:7f67814674175f073df23caf8b7c91b260a7137c533f8a803fe45958284014b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74319616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10540c1074154a7400fce6f045362a5b19fec4398ccad016970d22c8bc5d091a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f8587ed26b792c75e594eb6180abb023ce5ff41ca80ff1cb3f6957e6a561f`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 31.9 MB (31899808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9cc380879231e07691de5c5ea78ecb3c48fd1ba123f04b4199cd2ea57b702`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a381058bca45d65fc0b1d75d11afa62ffdd536a2e63f8ec53410a69e16582aa0`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 819.6 KB (819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055d851bf73a1cd79c9ee9827b9e30921b1ce6466ba2b9193cd2d55aff1f0c3d`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ef2f6b66a5614678ecb3f18212748e80795630c1052939b6eac00cfc24514`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:62846d4bfe113a3b8b99e0260b3c3dbea813ddeb6bb99a2caf4b873b5b6a4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb34fd963f132dc50b1d586d5d494bdab2563c3ecc45f4834830e0b15a7dd28`

```dockerfile
```

-	Layers:
	-	`sha256:21bb24eb1ec7e5634a14ae7cdc168c30941606b72d3e80575d3d4d680e6c15a3`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5525de3ecf05a3efcb441861b686dee89926597153e57240ce4825e160b8486`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:47d7b835171ffec0328fae7575bf8e29e75e1e866c91e0f0ffff3cb1be57ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baa72da663ecaf1ea7c583853eb9616914ccd62d14d2acde37ba57eeff56aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a7d66f5ee386637257f8a1f6bc089003e02af223a909850cf500f20b155d7`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 819.5 KB (819541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f213e26acf49ec38a850c7ff0fa23de5c8b2c17c069ac9c0902a85cf115fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb95489680753962b2de29f34d05756c60a995b837bdc5fa5e8eeefced2f56ba`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:1730724df72cd25002656a390bcde94a26888515007fea8e72cccce1c6fb0a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7410206d538eab0d239f168654d58738b3d56cb24113adcc5ec1c2da236211dc`

```dockerfile
```

-	Layers:
	-	`sha256:f95650052db6b6287a27c90ce79eb4e7846e05b6e251e80ea5f413df675831fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:89a74aee6ceff68f2e1c2321b2443464d9c6afc17b8df7c82dd314de38807cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69591459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e11c7867e7d5a0dd39f044532c925b0890cb6410e92006ac47323136fd75ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb034438936abf85793b650310894bd8bd13173aced1f7dc169fa7208e7d5bca`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 810.3 KB (810272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a0dd7b17e4584ef1b1efbf5688c229968887acdb82c8476165b39b3f5349a`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b2be749cc7fcd49eb802a71f3ac1ce66663d5dae7f71d1827f2e47d0867239`  
		Last Modified: Fri, 11 Apr 2025 19:39:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:6c93216690e2fe8247674c98e003134a7f2de7e4e7f5ba47de80d846fb5d8ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd50d65130115814f6185d2f625b813b300f82bd57128e854ae58c5c4904387`

```dockerfile
```

-	Layers:
	-	`sha256:b4d043fe6ac34149ce122ed212525bd843efbf9bd625dd9334732c703fd30d57`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca7bef7486b9cfa27052114b89b687b5e9fa6a03c0bbc106e11fcdca37e0e1`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:929cc7e998e81cd47db219e70fa257a480d636d729b103c88578aef1cd295f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cb88f4a6cac3721d08f194e49a16858bf48b009820ab3fbbce91e7db2cca1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15da7c67ee32af45a316a6f9c6c342a14223318ed0779a94c9ebf17037db04d`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 819.4 KB (819403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7789571e59cb91e330a208c04890b7ef977465021dc8e8b02602b7ab9865894`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839500dfa0ded5c129442f710c5c912a855dec8a5cb5afb7166bea3dce953ba`  
		Last Modified: Fri, 11 Apr 2025 19:24:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:9b2421f3eaff1e2cca976780d42de308c5a2047c4806c0aa1514d61da21fe221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb618408c20a5435dc2a4ae26f853bc341ca33fef495304a3d0056723a9da96a`

```dockerfile
```

-	Layers:
	-	`sha256:f04bf5edf85476ff574df13b64a1762bad84354aa9b30e36dffd41ccc91937ce`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41588df87c63458711fbaa30de2d87e937480d9edaec4f19a4b20df088c5de04`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:58e4c174b8103594f05977bd977804a3aeca612b897c189e5847f59d6a5f3549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75203837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca688659452b937358a5ec774995b2eb6cc73f93e40392279343dfe5ccc4b57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c342ad8eafb03b419ae29af4ef4059a105866abb7e43cfce9d46d6d82d7fd9`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 32.4 MB (32389724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4231e215abbfb69c86d27fc2b76e5e5340b88cd2c74399a390963ea725c605`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277eb15a82b83b148be52a1417ebd973a92ab090420deca4c42f497a41fc199`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 833.5 KB (833489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d34a5a44764514c6b3956401ca46c07fd4b8cd26f2822a1d5d79fcac0d8e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8aff9ab03e08f71c7cfa37dad17ed83c780074e269ffd3f8c529d72cf491f3`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:b959d0d1f4a8ed775e0e3eeb0a4f6a0a17a772e9f907a2eda3b44103ed910cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a4a4101e719bb7cc47398700d3d88f51a8a41348ce202664a24425858493fc`

```dockerfile
```

-	Layers:
	-	`sha256:ef336f0ece1bbfbc8013732815bea5dd2e9ace0b2038fe59bf6f3c46e2f4ba54`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7a130be4886e0992cc17ca28a845d97d4258e94933d18aa8cd64a25a17a868`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:37b0426cd93c53f5e0f1cdeb2c28f9d7b9ffa497152842bf20bd9bb1b0a2f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4bda40a0ea7330158522f1fb6d5f347ae30883be01214d636d4cba4754606f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0a36e58ec488f6c94472ac5305a4566f54edccef62ef776a2dd8e0ef07c71`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 826.4 KB (826358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e24a611fac22b50fab384e99e8176ac31d266631b646995db4c17f9ece57ae2`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c632ae1888a4dffabccc778283a3dcf18fb4e17671071f18c7483802e29eb`  
		Last Modified: Fri, 11 Apr 2025 19:29:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:b9b0a003d8cfda6b050ee6a1c11d241b2bcc8e56e1abd2081a3be51e02169f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f75030e17fa5d3af649ec522a70d16242e7e32daee2b70ea19b8040dce56d10`

```dockerfile
```

-	Layers:
	-	`sha256:99b344d2d1451234c62a01ec5f9ac9221e726c94a070c911eb994ffc9e03870c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65de8017361f5bd95197acdb9ee6c668e3c384cc8a330bf23618c20c2404e2c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:c8c9f924d43dad4966bbc045e1a0d101f1a342ec92528993a19850e9f770ce87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72661815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a13c6921667150b2cde5b0e0097252865b1cb890d09a71abba352d8e1e022c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92697fa690eb16f5f3a1f04e47a10869bcc5231665bd7f511c6b0bdc036dc8`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 817.9 KB (817892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cc89a24d8029aaa0bd6231af150db86c3620ed03d9956781752d3634b28fe`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40032bda6a57ee895b60e701cd79a2adb0e690a3c6087d54f7fdb06eda8f2488`  
		Last Modified: Sat, 15 Mar 2025 06:47:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:9b8f9221004aac4c24577c9c4c26355d63101933bcf811ffb69566e132a6ffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a749a5be401f08b78c2e9c0d9f21a9ec72ab341b7c251ad429d86dc3705b0a5`

```dockerfile
```

-	Layers:
	-	`sha256:b1e92b9f2c7997db127513c0e251912eff161f5a6b1d48c37992162fe3de25cd`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aba897460592ac0c7e2499751934a29ad36040f4ae78ae56da6e43caa705ae7`  
		Last Modified: Sat, 15 Mar 2025 06:49:13 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:22d3f1ac483a883cdac3170ec0c48534399b4614fd7b14eef991983310d52e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75441805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550c839a96536c03825b2ea784a0c6865d61f91e0a5446810a49a24476e805f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2abe1c95b14367537e000ce27b700e744674dbbf54603c7c19849713925f4f`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 822.7 KB (822682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9497720774556f9e9199ca165c9137abd44cc9521e30c99f31e99201ca6abf`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ce55bf35d81cdcc3a3502f45dcd9637bec07c398dc6b5c0483da389e68e57`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:ee3b78e48acf450beaa636f62e09931106cd4ef6acee53ee3f5a725fae3468ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd14dff933ed1c7de2454f0d532ef20288caf72647212c72add8cd14d46f08b`

```dockerfile
```

-	Layers:
	-	`sha256:acb87901ec354a0af4a7a84773ae6b0e6dbdbb11efb6892eb02f3727c7338e58`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86956f22dc6528092933cbb7a30e36a293df41719fc70b86779be850ba58e6fa`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:8fe8c8dcdcf9e4c5b390b60df4641cfcf115a82de2559846876fb427cd88f299
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

### `composer:2.8` - linux; amd64

```console
$ docker pull composer@sha256:d1f9a3724292137c09b7d2bf01b3b509d13fc61200f82e4d2b0fe2f88201ce83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74473432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a3bdf885ffdf6e3aef5d9dcf7a1bfdeadbacf2103cc12e6e0a3f404981e70c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509ab55c895beab91f6c90ae48de7d99603c66e3474f83bcc8a0ca0aedd37653`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 31.9 MB (31899867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01b194f1013b5b27b55fec92accbd224bc153115f60e65560776b367abe3da`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6de9c7a5772659e5d271fdac666c511a74f7f04a00bc38d775ba802c37137`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 973.4 KB (973397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf01bfedd4c1102169f56d2e45b053513e3640897ee956e36d9e0de21aa36df`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6e377c351d400fe1111c9c37e4c1d0f38427cda8ce59edf59ee0928ecc805`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:43d30ecf6c63136c7f4f9be50ebc49bf04ed640d168d6e9d46bd6311ea5ec872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a84b51c23284c23b023741b1d8ca93e6a8bdaacf8224072adcb7239230cd02`

```dockerfile
```

-	Layers:
	-	`sha256:ae87b4fcd3272bd830c70fbe50796918ab3bbabed5483fce8874ca479f5ed8e9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942904207b2a570e4eae3579b45678543d33798e5aa7dd3dec897f97c0d373e6`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:3ef5239220206922e5cc902a9b4e2a095820d6e5dadc3c5fe50ff6df07445b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db3d3a9609440a80e75f22fdd56c3e05a3f3323928f5221c48407278f5cd6fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a34643ac8080eb792162edf87a5d1bb6cb6200f000c6868daeadcec4ae36e`  
		Last Modified: Fri, 11 Apr 2025 18:10:58 GMT  
		Size: 973.4 KB (973376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4808aa0666e52f6471e3e966115fcd0150ddc6073a566ea060bcf43b36bbe067`  
		Last Modified: Mon, 07 Apr 2025 18:27:11 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda93248846bb795a6d366c8208532c3a525382c106ffeeec37585617f5b9f54`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:53abf5c90a9169919625e7e003337069669420ccfacb5b42bc1d2e15e0e645f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee516c854df84a65e97bdb5b9d9f8cdb67ddffce9eaa37fd01024c138ef6e05b`

```dockerfile
```

-	Layers:
	-	`sha256:5ee92ec4b1905550d532309fd56675c37817099218756d3a162ad86c2f6283ab`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:e77bc0a09419c01277bdbf065076077c92ba37c0edf629c9eadaa1615a721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69745181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75de10a053848f75afd367777db1fa36efdb47c0778e71402a77f357c9de97f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f65fd6f940c82a8c166fd24d4665f3f465b1fcbb2d103793d4656d54a1656c`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 964.0 KB (963995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9e0beff00bdf5b015f0aac204f7fe9a3066594cb59853bfbd5d271841bc56`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42c4d925094cf2a05a5ac36614a58ed0d0514c16751e5f606500b110fa43a8`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:8ce0a91cfcc894dfedb059c98d79926f62a80a459055c4227ac88ce3fadddf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7af4b9e1488223e20c7d676747db5a14248ab6c411151c1f0914c562542b9b7`

```dockerfile
```

-	Layers:
	-	`sha256:793de8e374497628c83e336e44b5671e0673982dabc76c86736d6c042caea121`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed152e48fcfd5e9bf12e9a756c4295a00364ab54210b7b5a6f4e91deeaf34e33`  
		Last Modified: Fri, 11 Apr 2025 19:41:11 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:a1d0ad849ed7139e6ee97e3a3eea4a710aa99551f254ed921e7670beab3f26f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee294a7818c30ea88f137022e8f7c42414537abe52fa0113b832c4243584a7fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83923b12588e2301b9e71a33005542c223e69335e610b0c7840e99efde924a8d`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 973.1 KB (973086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e05513a2e1f1324ee4397564bc67061ded98cba32df095ad2693ad798400041`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1547115648d094b42553472fbfdf9d84634b8ca48c7162ba31f5cbb74f83a0c6`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:bf6af03c683437e5c2448571d9df94a2888c391c5ae80cb4b5d80b74d80a5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b3e99b21bdafa208be140b4322827861ac66269ca7f502afd710672969ea28`

```dockerfile
```

-	Layers:
	-	`sha256:6644067f62b0b66dfa3a4e243910f7b0b8a69f8ba5cb7acd09823fd5997bf856`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0982021520e1a07030f1d22d009576b85ef2c9f5c3a7a9c02a49e182039bd22`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:91f259044f73c867c36c93537ea4ea299fd09c2e3fa78f5efd56a6d4c4bf4cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85288e1b13a1e952e306181f98aa841f963de0bb332bcfd1d1bc9cadcf6ca61a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054678de643e99369f09488a354017f53e9c018ffe32ff0f5a6c1a4a9863b106`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 32.4 MB (32389723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7984ef9d999bd2106c5eb4d399ea83f5d96377dbd5ff6eb722b13e11df6e62f7`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72235dc5244dc5af4e91b28c1c2cd55ce554eaef3a887fea5fcded4ce6ed38e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 987.3 KB (987302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f7a075730c760d5f8495f8a05b8db853fd3442784a9c2450c60f5bd83adcb`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4432930f16e27e5e489bd26af6eb90356679ad20f1785b6c7f9c2fc0fa1dc9e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:0cf998ee72f60117e5a2dfb60702a0bf3c8c424d07d6eec02c4757dd443b4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24260866c20c6db6c71913312bc0e7188e1728e56c4b3935a335d98e68596016`

```dockerfile
```

-	Layers:
	-	`sha256:68b6b4c0caf05a903ea4ce0314cc16d4d7333764b90904663f197d5fe04fc6e2`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a140744a8c72b499555d00d841e0d9664f4d73893e856e2a35fb640b606626d5`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:957afe8b3436a8e7f90792d3b3d6200805e998cc035c9705ab80240b39bcaeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77328254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd31b923dc64f9a52efc50fe34a509efaefc8749054cc9a187576987d9a3446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cae0199aee1f1d7675b425dd7a002b08f1c55aafbdd76c11a431bf5c6136a4`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 980.2 KB (980158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544ba637c1fbb847f3723ad515b9176fde84af1896c855c6f2a6e656a59db09`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2e04faaaa383cf0bdbf7145970c2f0efd8f0f70f917f5dcf07192cc75b0a9`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:1bfc304907c0eea715831e11bbca34587fa8558eb74854c09ecf14d571220e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255600b7aa0375c5a431914b16c1772a557741bc4180b1b14b019719ad2750d0`

```dockerfile
```

-	Layers:
	-	`sha256:dcbb644eb3e4cfe25a0778e44fa77f9c1bffd2f591a3cf96700bb04f041b89bd`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5358ecdab7bc58df4dbac1e6307865d0cf8fab94e35e63543a1729f2012eac06`  
		Last Modified: Fri, 11 Apr 2025 19:31:16 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:56990de21c9bca773b1b124b716cd66204b92be8a6437af837318e323ab73c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80230002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebfec9d1692cc828e75071fda5f0ff25f520aa87fe4580f0b2902ead0ac171a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e116d64bc7b99710ce15d59ac54326e69c760685b12a7901ee7bc480140314a8`  
		Last Modified: Mon, 07 Apr 2025 18:25:42 GMT  
		Size: 8.4 MB (8386079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226458f98d993141ed17504e38c4cd773aab2bbf8a6ffda3a2c121c75791e446`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665cae102abe189a75ef2af3451f2fbf276f2a8584b1d641c8ad383c7a867672`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a3eb24f29f53c1c2e8d25ce014ccee4a0185cc696f2c574c6d2da9fda1155897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0a6da777fbd04b4beafef8ae764ec48289a4d5e0857b3f8730a233f6a16f13`

```dockerfile
```

-	Layers:
	-	`sha256:7a7bc4fbad88fb98041126d295cf745f34e96d3526338b01abfaf49301c296f2`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 2.2 MB (2156780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e38e95f8d379d49ee6090dcccad27ba9c8b1e5405d708f047322285c7d4c3`  
		Last Modified: Mon, 07 Apr 2025 18:25:40 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:fad546c332bde77af83dee676657439d8a100f1af5e414e599427edae62c9419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576949660ee7a6f1c6d2917d8e98e673a3ee3bb67adb845c9c1dc6fffa16b4a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed50f3550c2abfcb1b9a5f45aed896719a13f4053fe85cc3914bbc582e3f5a3`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 976.5 KB (976453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b739b9129e764f75e6a59832dc964d90e2d4d36771324699de217df0ae9085d`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88c66732baa17dd7f6ec04f5671542bf12b7331761899f10921eb9ae285633`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:3e7e6d959f7598a83d628b8afa1816bec605c0a8aa3c6f5d17e0406f0d30ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8dd4b600398f57bb5894ff6fd71fe40243b0bbad2763b49ff365ce287669f5`

```dockerfile
```

-	Layers:
	-	`sha256:f85d928cff47a1cd9984fd2b5a09bb4030408d3c5a59beb89b3aa2da5e8e9790`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b4626e93f8bf63442942bb98c7b3ff0ff37481357fb211b3d564060d35c9d1`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.8`

```console
$ docker pull composer@sha256:8fe8c8dcdcf9e4c5b390b60df4641cfcf115a82de2559846876fb427cd88f299
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

### `composer:2.8.8` - linux; amd64

```console
$ docker pull composer@sha256:d1f9a3724292137c09b7d2bf01b3b509d13fc61200f82e4d2b0fe2f88201ce83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74473432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a3bdf885ffdf6e3aef5d9dcf7a1bfdeadbacf2103cc12e6e0a3f404981e70c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509ab55c895beab91f6c90ae48de7d99603c66e3474f83bcc8a0ca0aedd37653`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 31.9 MB (31899867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01b194f1013b5b27b55fec92accbd224bc153115f60e65560776b367abe3da`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6de9c7a5772659e5d271fdac666c511a74f7f04a00bc38d775ba802c37137`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 973.4 KB (973397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf01bfedd4c1102169f56d2e45b053513e3640897ee956e36d9e0de21aa36df`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6e377c351d400fe1111c9c37e4c1d0f38427cda8ce59edf59ee0928ecc805`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:43d30ecf6c63136c7f4f9be50ebc49bf04ed640d168d6e9d46bd6311ea5ec872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a84b51c23284c23b023741b1d8ca93e6a8bdaacf8224072adcb7239230cd02`

```dockerfile
```

-	Layers:
	-	`sha256:ae87b4fcd3272bd830c70fbe50796918ab3bbabed5483fce8874ca479f5ed8e9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942904207b2a570e4eae3579b45678543d33798e5aa7dd3dec897f97c0d373e6`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:3ef5239220206922e5cc902a9b4e2a095820d6e5dadc3c5fe50ff6df07445b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db3d3a9609440a80e75f22fdd56c3e05a3f3323928f5221c48407278f5cd6fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a34643ac8080eb792162edf87a5d1bb6cb6200f000c6868daeadcec4ae36e`  
		Last Modified: Fri, 11 Apr 2025 18:10:58 GMT  
		Size: 973.4 KB (973376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4808aa0666e52f6471e3e966115fcd0150ddc6073a566ea060bcf43b36bbe067`  
		Last Modified: Mon, 07 Apr 2025 18:27:11 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda93248846bb795a6d366c8208532c3a525382c106ffeeec37585617f5b9f54`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:53abf5c90a9169919625e7e003337069669420ccfacb5b42bc1d2e15e0e645f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee516c854df84a65e97bdb5b9d9f8cdb67ddffce9eaa37fd01024c138ef6e05b`

```dockerfile
```

-	Layers:
	-	`sha256:5ee92ec4b1905550d532309fd56675c37817099218756d3a162ad86c2f6283ab`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:e77bc0a09419c01277bdbf065076077c92ba37c0edf629c9eadaa1615a721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69745181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75de10a053848f75afd367777db1fa36efdb47c0778e71402a77f357c9de97f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f65fd6f940c82a8c166fd24d4665f3f465b1fcbb2d103793d4656d54a1656c`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 964.0 KB (963995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9e0beff00bdf5b015f0aac204f7fe9a3066594cb59853bfbd5d271841bc56`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42c4d925094cf2a05a5ac36614a58ed0d0514c16751e5f606500b110fa43a8`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:8ce0a91cfcc894dfedb059c98d79926f62a80a459055c4227ac88ce3fadddf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7af4b9e1488223e20c7d676747db5a14248ab6c411151c1f0914c562542b9b7`

```dockerfile
```

-	Layers:
	-	`sha256:793de8e374497628c83e336e44b5671e0673982dabc76c86736d6c042caea121`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed152e48fcfd5e9bf12e9a756c4295a00364ab54210b7b5a6f4e91deeaf34e33`  
		Last Modified: Fri, 11 Apr 2025 19:41:11 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:a1d0ad849ed7139e6ee97e3a3eea4a710aa99551f254ed921e7670beab3f26f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee294a7818c30ea88f137022e8f7c42414537abe52fa0113b832c4243584a7fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83923b12588e2301b9e71a33005542c223e69335e610b0c7840e99efde924a8d`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 973.1 KB (973086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e05513a2e1f1324ee4397564bc67061ded98cba32df095ad2693ad798400041`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1547115648d094b42553472fbfdf9d84634b8ca48c7162ba31f5cbb74f83a0c6`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:bf6af03c683437e5c2448571d9df94a2888c391c5ae80cb4b5d80b74d80a5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b3e99b21bdafa208be140b4322827861ac66269ca7f502afd710672969ea28`

```dockerfile
```

-	Layers:
	-	`sha256:6644067f62b0b66dfa3a4e243910f7b0b8a69f8ba5cb7acd09823fd5997bf856`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0982021520e1a07030f1d22d009576b85ef2c9f5c3a7a9c02a49e182039bd22`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; 386

```console
$ docker pull composer@sha256:91f259044f73c867c36c93537ea4ea299fd09c2e3fa78f5efd56a6d4c4bf4cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85288e1b13a1e952e306181f98aa841f963de0bb332bcfd1d1bc9cadcf6ca61a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054678de643e99369f09488a354017f53e9c018ffe32ff0f5a6c1a4a9863b106`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 32.4 MB (32389723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7984ef9d999bd2106c5eb4d399ea83f5d96377dbd5ff6eb722b13e11df6e62f7`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72235dc5244dc5af4e91b28c1c2cd55ce554eaef3a887fea5fcded4ce6ed38e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 987.3 KB (987302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f7a075730c760d5f8495f8a05b8db853fd3442784a9c2450c60f5bd83adcb`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4432930f16e27e5e489bd26af6eb90356679ad20f1785b6c7f9c2fc0fa1dc9e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:0cf998ee72f60117e5a2dfb60702a0bf3c8c424d07d6eec02c4757dd443b4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24260866c20c6db6c71913312bc0e7188e1728e56c4b3935a335d98e68596016`

```dockerfile
```

-	Layers:
	-	`sha256:68b6b4c0caf05a903ea4ce0314cc16d4d7333764b90904663f197d5fe04fc6e2`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a140744a8c72b499555d00d841e0d9664f4d73893e856e2a35fb640b606626d5`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; ppc64le

```console
$ docker pull composer@sha256:957afe8b3436a8e7f90792d3b3d6200805e998cc035c9705ab80240b39bcaeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77328254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd31b923dc64f9a52efc50fe34a509efaefc8749054cc9a187576987d9a3446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cae0199aee1f1d7675b425dd7a002b08f1c55aafbdd76c11a431bf5c6136a4`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 980.2 KB (980158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544ba637c1fbb847f3723ad515b9176fde84af1896c855c6f2a6e656a59db09`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2e04faaaa383cf0bdbf7145970c2f0efd8f0f70f917f5dcf07192cc75b0a9`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:1bfc304907c0eea715831e11bbca34587fa8558eb74854c09ecf14d571220e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255600b7aa0375c5a431914b16c1772a557741bc4180b1b14b019719ad2750d0`

```dockerfile
```

-	Layers:
	-	`sha256:dcbb644eb3e4cfe25a0778e44fa77f9c1bffd2f591a3cf96700bb04f041b89bd`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5358ecdab7bc58df4dbac1e6307865d0cf8fab94e35e63543a1729f2012eac06`  
		Last Modified: Fri, 11 Apr 2025 19:31:16 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; riscv64

```console
$ docker pull composer@sha256:56990de21c9bca773b1b124b716cd66204b92be8a6437af837318e323ab73c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80230002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebfec9d1692cc828e75071fda5f0ff25f520aa87fe4580f0b2902ead0ac171a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e116d64bc7b99710ce15d59ac54326e69c760685b12a7901ee7bc480140314a8`  
		Last Modified: Mon, 07 Apr 2025 18:25:42 GMT  
		Size: 8.4 MB (8386079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226458f98d993141ed17504e38c4cd773aab2bbf8a6ffda3a2c121c75791e446`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665cae102abe189a75ef2af3451f2fbf276f2a8584b1d641c8ad383c7a867672`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:a3eb24f29f53c1c2e8d25ce014ccee4a0185cc696f2c574c6d2da9fda1155897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0a6da777fbd04b4beafef8ae764ec48289a4d5e0857b3f8730a233f6a16f13`

```dockerfile
```

-	Layers:
	-	`sha256:7a7bc4fbad88fb98041126d295cf745f34e96d3526338b01abfaf49301c296f2`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 2.2 MB (2156780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e38e95f8d379d49ee6090dcccad27ba9c8b1e5405d708f047322285c7d4c3`  
		Last Modified: Mon, 07 Apr 2025 18:25:40 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; s390x

```console
$ docker pull composer@sha256:fad546c332bde77af83dee676657439d8a100f1af5e414e599427edae62c9419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576949660ee7a6f1c6d2917d8e98e673a3ee3bb67adb845c9c1dc6fffa16b4a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed50f3550c2abfcb1b9a5f45aed896719a13f4053fe85cc3914bbc582e3f5a3`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 976.5 KB (976453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b739b9129e764f75e6a59832dc964d90e2d4d36771324699de217df0ae9085d`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88c66732baa17dd7f6ec04f5671542bf12b7331761899f10921eb9ae285633`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:3e7e6d959f7598a83d628b8afa1816bec605c0a8aa3c6f5d17e0406f0d30ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8dd4b600398f57bb5894ff6fd71fe40243b0bbad2763b49ff365ce287669f5`

```dockerfile
```

-	Layers:
	-	`sha256:f85d928cff47a1cd9984fd2b5a09bb4030408d3c5a59beb89b3aa2da5e8e9790`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b4626e93f8bf63442942bb98c7b3ff0ff37481357fb211b3d564060d35c9d1`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:8fe8c8dcdcf9e4c5b390b60df4641cfcf115a82de2559846876fb427cd88f299
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

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:d1f9a3724292137c09b7d2bf01b3b509d13fc61200f82e4d2b0fe2f88201ce83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74473432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a3bdf885ffdf6e3aef5d9dcf7a1bfdeadbacf2103cc12e6e0a3f404981e70c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509ab55c895beab91f6c90ae48de7d99603c66e3474f83bcc8a0ca0aedd37653`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 31.9 MB (31899867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01b194f1013b5b27b55fec92accbd224bc153115f60e65560776b367abe3da`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6de9c7a5772659e5d271fdac666c511a74f7f04a00bc38d775ba802c37137`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 973.4 KB (973397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf01bfedd4c1102169f56d2e45b053513e3640897ee956e36d9e0de21aa36df`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6e377c351d400fe1111c9c37e4c1d0f38427cda8ce59edf59ee0928ecc805`  
		Last Modified: Fri, 11 Apr 2025 17:09:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:43d30ecf6c63136c7f4f9be50ebc49bf04ed640d168d6e9d46bd6311ea5ec872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a84b51c23284c23b023741b1d8ca93e6a8bdaacf8224072adcb7239230cd02`

```dockerfile
```

-	Layers:
	-	`sha256:ae87b4fcd3272bd830c70fbe50796918ab3bbabed5483fce8874ca479f5ed8e9`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942904207b2a570e4eae3579b45678543d33798e5aa7dd3dec897f97c0d373e6`  
		Last Modified: Fri, 11 Apr 2025 17:09:33 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:3ef5239220206922e5cc902a9b4e2a095820d6e5dadc3c5fe50ff6df07445b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db3d3a9609440a80e75f22fdd56c3e05a3f3323928f5221c48407278f5cd6fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a34643ac8080eb792162edf87a5d1bb6cb6200f000c6868daeadcec4ae36e`  
		Last Modified: Fri, 11 Apr 2025 18:10:58 GMT  
		Size: 973.4 KB (973376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4808aa0666e52f6471e3e966115fcd0150ddc6073a566ea060bcf43b36bbe067`  
		Last Modified: Mon, 07 Apr 2025 18:27:11 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda93248846bb795a6d366c8208532c3a525382c106ffeeec37585617f5b9f54`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:53abf5c90a9169919625e7e003337069669420ccfacb5b42bc1d2e15e0e645f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee516c854df84a65e97bdb5b9d9f8cdb67ddffce9eaa37fd01024c138ef6e05b`

```dockerfile
```

-	Layers:
	-	`sha256:5ee92ec4b1905550d532309fd56675c37817099218756d3a162ad86c2f6283ab`  
		Last Modified: Fri, 11 Apr 2025 18:10:57 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:e77bc0a09419c01277bdbf065076077c92ba37c0edf629c9eadaa1615a721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69745181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75de10a053848f75afd367777db1fa36efdb47c0778e71402a77f357c9de97f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f65fd6f940c82a8c166fd24d4665f3f465b1fcbb2d103793d4656d54a1656c`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 964.0 KB (963995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9e0beff00bdf5b015f0aac204f7fe9a3066594cb59853bfbd5d271841bc56`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42c4d925094cf2a05a5ac36614a58ed0d0514c16751e5f606500b110fa43a8`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:8ce0a91cfcc894dfedb059c98d79926f62a80a459055c4227ac88ce3fadddf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7af4b9e1488223e20c7d676747db5a14248ab6c411151c1f0914c562542b9b7`

```dockerfile
```

-	Layers:
	-	`sha256:793de8e374497628c83e336e44b5671e0673982dabc76c86736d6c042caea121`  
		Last Modified: Fri, 11 Apr 2025 19:41:12 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed152e48fcfd5e9bf12e9a756c4295a00364ab54210b7b5a6f4e91deeaf34e33`  
		Last Modified: Fri, 11 Apr 2025 19:41:11 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:a1d0ad849ed7139e6ee97e3a3eea4a710aa99551f254ed921e7670beab3f26f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee294a7818c30ea88f137022e8f7c42414537abe52fa0113b832c4243584a7fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83923b12588e2301b9e71a33005542c223e69335e610b0c7840e99efde924a8d`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 973.1 KB (973086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e05513a2e1f1324ee4397564bc67061ded98cba32df095ad2693ad798400041`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1547115648d094b42553472fbfdf9d84634b8ca48c7162ba31f5cbb74f83a0c6`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:bf6af03c683437e5c2448571d9df94a2888c391c5ae80cb4b5d80b74d80a5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b3e99b21bdafa208be140b4322827861ac66269ca7f502afd710672969ea28`

```dockerfile
```

-	Layers:
	-	`sha256:6644067f62b0b66dfa3a4e243910f7b0b8a69f8ba5cb7acd09823fd5997bf856`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0982021520e1a07030f1d22d009576b85ef2c9f5c3a7a9c02a49e182039bd22`  
		Last Modified: Fri, 11 Apr 2025 19:25:48 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:91f259044f73c867c36c93537ea4ea299fd09c2e3fa78f5efd56a6d4c4bf4cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75357651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85288e1b13a1e952e306181f98aa841f963de0bb332bcfd1d1bc9cadcf6ca61a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054678de643e99369f09488a354017f53e9c018ffe32ff0f5a6c1a4a9863b106`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 32.4 MB (32389723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7984ef9d999bd2106c5eb4d399ea83f5d96377dbd5ff6eb722b13e11df6e62f7`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72235dc5244dc5af4e91b28c1c2cd55ce554eaef3a887fea5fcded4ce6ed38e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 987.3 KB (987302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f7a075730c760d5f8495f8a05b8db853fd3442784a9c2450c60f5bd83adcb`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4432930f16e27e5e489bd26af6eb90356679ad20f1785b6c7f9c2fc0fa1dc9e`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0cf998ee72f60117e5a2dfb60702a0bf3c8c424d07d6eec02c4757dd443b4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24260866c20c6db6c71913312bc0e7188e1728e56c4b3935a335d98e68596016`

```dockerfile
```

-	Layers:
	-	`sha256:68b6b4c0caf05a903ea4ce0314cc16d4d7333764b90904663f197d5fe04fc6e2`  
		Last Modified: Fri, 11 Apr 2025 17:09:44 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a140744a8c72b499555d00d841e0d9664f4d73893e856e2a35fb640b606626d5`  
		Last Modified: Fri, 11 Apr 2025 17:09:43 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:957afe8b3436a8e7f90792d3b3d6200805e998cc035c9705ab80240b39bcaeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77328254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd31b923dc64f9a52efc50fe34a509efaefc8749054cc9a187576987d9a3446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cae0199aee1f1d7675b425dd7a002b08f1c55aafbdd76c11a431bf5c6136a4`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 980.2 KB (980158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544ba637c1fbb847f3723ad515b9176fde84af1896c855c6f2a6e656a59db09`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2e04faaaa383cf0bdbf7145970c2f0efd8f0f70f917f5dcf07192cc75b0a9`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:1bfc304907c0eea715831e11bbca34587fa8558eb74854c09ecf14d571220e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255600b7aa0375c5a431914b16c1772a557741bc4180b1b14b019719ad2750d0`

```dockerfile
```

-	Layers:
	-	`sha256:dcbb644eb3e4cfe25a0778e44fa77f9c1bffd2f591a3cf96700bb04f041b89bd`  
		Last Modified: Fri, 11 Apr 2025 19:31:17 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5358ecdab7bc58df4dbac1e6307865d0cf8fab94e35e63543a1729f2012eac06`  
		Last Modified: Fri, 11 Apr 2025 19:31:16 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:56990de21c9bca773b1b124b716cd66204b92be8a6437af837318e323ab73c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80230002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebfec9d1692cc828e75071fda5f0ff25f520aa87fe4580f0b2902ead0ac171a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e116d64bc7b99710ce15d59ac54326e69c760685b12a7901ee7bc480140314a8`  
		Last Modified: Mon, 07 Apr 2025 18:25:42 GMT  
		Size: 8.4 MB (8386079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226458f98d993141ed17504e38c4cd773aab2bbf8a6ffda3a2c121c75791e446`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665cae102abe189a75ef2af3451f2fbf276f2a8584b1d641c8ad383c7a867672`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a3eb24f29f53c1c2e8d25ce014ccee4a0185cc696f2c574c6d2da9fda1155897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0a6da777fbd04b4beafef8ae764ec48289a4d5e0857b3f8730a233f6a16f13`

```dockerfile
```

-	Layers:
	-	`sha256:7a7bc4fbad88fb98041126d295cf745f34e96d3526338b01abfaf49301c296f2`  
		Last Modified: Mon, 07 Apr 2025 18:25:41 GMT  
		Size: 2.2 MB (2156780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e38e95f8d379d49ee6090dcccad27ba9c8b1e5405d708f047322285c7d4c3`  
		Last Modified: Mon, 07 Apr 2025 18:25:40 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:fad546c332bde77af83dee676657439d8a100f1af5e414e599427edae62c9419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576949660ee7a6f1c6d2917d8e98e673a3ee3bb67adb845c9c1dc6fffa16b4a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.6
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed50f3550c2abfcb1b9a5f45aed896719a13f4053fe85cc3914bbc582e3f5a3`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 976.5 KB (976453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b739b9129e764f75e6a59832dc964d90e2d4d36771324699de217df0ae9085d`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88c66732baa17dd7f6ec04f5671542bf12b7331761899f10921eb9ae285633`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:3e7e6d959f7598a83d628b8afa1816bec605c0a8aa3c6f5d17e0406f0d30ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8dd4b600398f57bb5894ff6fd71fe40243b0bbad2763b49ff365ce287669f5`

```dockerfile
```

-	Layers:
	-	`sha256:f85d928cff47a1cd9984fd2b5a09bb4030408d3c5a59beb89b3aa2da5e8e9790`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b4626e93f8bf63442942bb98c7b3ff0ff37481357fb211b3d564060d35c9d1`  
		Last Modified: Fri, 11 Apr 2025 19:37:22 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:62ca5003b85975aff5a6fe29ab270f673f81800ee91cae01c57148e00d380005
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

### `composer:lts` - linux; amd64

```console
$ docker pull composer@sha256:7f67814674175f073df23caf8b7c91b260a7137c533f8a803fe45958284014b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74319616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10540c1074154a7400fce6f045362a5b19fec4398ccad016970d22c8bc5d091a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f8587ed26b792c75e594eb6180abb023ce5ff41ca80ff1cb3f6957e6a561f`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 31.9 MB (31899808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9cc380879231e07691de5c5ea78ecb3c48fd1ba123f04b4199cd2ea57b702`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a381058bca45d65fc0b1d75d11afa62ffdd536a2e63f8ec53410a69e16582aa0`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 819.6 KB (819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055d851bf73a1cd79c9ee9827b9e30921b1ce6466ba2b9193cd2d55aff1f0c3d`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ef2f6b66a5614678ecb3f18212748e80795630c1052939b6eac00cfc24514`  
		Last Modified: Fri, 11 Apr 2025 17:09:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:62846d4bfe113a3b8b99e0260b3c3dbea813ddeb6bb99a2caf4b873b5b6a4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb34fd963f132dc50b1d586d5d494bdab2563c3ecc45f4834830e0b15a7dd28`

```dockerfile
```

-	Layers:
	-	`sha256:21bb24eb1ec7e5634a14ae7cdc168c30941606b72d3e80575d3d4d680e6c15a3`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5525de3ecf05a3efcb441861b686dee89926597153e57240ce4825e160b8486`  
		Last Modified: Fri, 11 Apr 2025 17:09:31 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:47d7b835171ffec0328fae7575bf8e29e75e1e866c91e0f0ffff3cb1be57ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baa72da663ecaf1ea7c583853eb9616914ccd62d14d2acde37ba57eeff56aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ae3abe63a69ee610ec0a0ace1065229e2b76b365f06529f8e323f78eeeb68`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 31.6 MB (31595633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba44b041e04eb8c8bb0cc9e0d44c7a5bead2c3934f3c38d7c35d6a8fdc09d7c`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a7d66f5ee386637257f8a1f6bc089003e02af223a909850cf500f20b155d7`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 819.5 KB (819541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f213e26acf49ec38a850c7ff0fa23de5c8b2c17c069ac9c0902a85cf115fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb95489680753962b2de29f34d05756c60a995b837bdc5fa5e8eeefced2f56ba`  
		Last Modified: Fri, 11 Apr 2025 18:09:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:1730724df72cd25002656a390bcde94a26888515007fea8e72cccce1c6fb0a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7410206d538eab0d239f168654d58738b3d56cb24113adcc5ec1c2da236211dc`

```dockerfile
```

-	Layers:
	-	`sha256:f95650052db6b6287a27c90ce79eb4e7846e05b6e251e80ea5f413df675831fd`  
		Last Modified: Fri, 11 Apr 2025 18:09:21 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:89a74aee6ceff68f2e1c2321b2443464d9c6afc17b8df7c82dd314de38807cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69591459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e11c7867e7d5a0dd39f044532c925b0890cb6410e92006ac47323136fd75ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143b8d4578b0acec81687795021a9e65a931de1f734b1045ee3cb865f6012271`  
		Last Modified: Fri, 11 Apr 2025 19:39:53 GMT  
		Size: 30.2 MB (30152972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ed7c1f7aaa68ed002405a7699113c140ce6898368d1bd3b1c8dba19e67b00`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb034438936abf85793b650310894bd8bd13173aced1f7dc169fa7208e7d5bca`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 810.3 KB (810272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a0dd7b17e4584ef1b1efbf5688c229968887acdb82c8476165b39b3f5349a`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b2be749cc7fcd49eb802a71f3ac1ce66663d5dae7f71d1827f2e47d0867239`  
		Last Modified: Fri, 11 Apr 2025 19:39:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:6c93216690e2fe8247674c98e003134a7f2de7e4e7f5ba47de80d846fb5d8ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd50d65130115814f6185d2f625b813b300f82bd57128e854ae58c5c4904387`

```dockerfile
```

-	Layers:
	-	`sha256:b4d043fe6ac34149ce122ed212525bd843efbf9bd625dd9334732c703fd30d57`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca7bef7486b9cfa27052114b89b687b5e9fa6a03c0bbc106e11fcdca37e0e1`  
		Last Modified: Fri, 11 Apr 2025 19:39:51 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:929cc7e998e81cd47db219e70fa257a480d636d729b103c88578aef1cd295f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cb88f4a6cac3721d08f194e49a16858bf48b009820ab3fbbce91e7db2cca1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33408a3589f34ba3f1a46fa8a92089eb4b122ba02caf140888a4ca31f066c9`  
		Last Modified: Fri, 11 Apr 2025 19:24:37 GMT  
		Size: 32.0 MB (32007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab17d4b15824b6e50284d472791d1addb077a1841ba6ba719b819eafeb0470`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15da7c67ee32af45a316a6f9c6c342a14223318ed0779a94c9ebf17037db04d`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 819.4 KB (819403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7789571e59cb91e330a208c04890b7ef977465021dc8e8b02602b7ab9865894`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839500dfa0ded5c129442f710c5c912a855dec8a5cb5afb7166bea3dce953ba`  
		Last Modified: Fri, 11 Apr 2025 19:24:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:9b2421f3eaff1e2cca976780d42de308c5a2047c4806c0aa1514d61da21fe221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb618408c20a5435dc2a4ae26f853bc341ca33fef495304a3d0056723a9da96a`

```dockerfile
```

-	Layers:
	-	`sha256:f04bf5edf85476ff574df13b64a1762bad84354aa9b30e36dffd41ccc91937ce`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41588df87c63458711fbaa30de2d87e937480d9edaec4f19a4b20df088c5de04`  
		Last Modified: Fri, 11 Apr 2025 19:24:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:58e4c174b8103594f05977bd977804a3aeca612b897c189e5847f59d6a5f3549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75203837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca688659452b937358a5ec774995b2eb6cc73f93e40392279343dfe5ccc4b57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c342ad8eafb03b419ae29af4ef4059a105866abb7e43cfce9d46d6d82d7fd9`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 32.4 MB (32389724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4231e215abbfb69c86d27fc2b76e5e5340b88cd2c74399a390963ea725c605`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277eb15a82b83b148be52a1417ebd973a92ab090420deca4c42f497a41fc199`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 833.5 KB (833489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d34a5a44764514c6b3956401ca46c07fd4b8cd26f2822a1d5d79fcac0d8e8`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8aff9ab03e08f71c7cfa37dad17ed83c780074e269ffd3f8c529d72cf491f3`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:b959d0d1f4a8ed775e0e3eeb0a4f6a0a17a772e9f907a2eda3b44103ed910cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a4a4101e719bb7cc47398700d3d88f51a8a41348ce202664a24425858493fc`

```dockerfile
```

-	Layers:
	-	`sha256:ef336f0ece1bbfbc8013732815bea5dd2e9ace0b2038fe59bf6f3c46e2f4ba54`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7a130be4886e0992cc17ca28a845d97d4258e94933d18aa8cd64a25a17a868`  
		Last Modified: Fri, 11 Apr 2025 17:09:40 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:37b0426cd93c53f5e0f1cdeb2c28f9d7b9ffa497152842bf20bd9bb1b0a2f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4bda40a0ea7330158522f1fb6d5f347ae30883be01214d636d4cba4754606f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc508b46f993f0919871a2cf3415708be172f8a723a52373b383a560d7c6a8`  
		Last Modified: Fri, 11 Apr 2025 19:29:22 GMT  
		Size: 32.9 MB (32937759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31339043fa2737f0837501ace59f5f9f11c70b196149777b88975b0ca436925`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0a36e58ec488f6c94472ac5305a4566f54edccef62ef776a2dd8e0ef07c71`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 826.4 KB (826358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e24a611fac22b50fab384e99e8176ac31d266631b646995db4c17f9ece57ae2`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c632ae1888a4dffabccc778283a3dcf18fb4e17671071f18c7483802e29eb`  
		Last Modified: Fri, 11 Apr 2025 19:29:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:b9b0a003d8cfda6b050ee6a1c11d241b2bcc8e56e1abd2081a3be51e02169f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f75030e17fa5d3af649ec522a70d16242e7e32daee2b70ea19b8040dce56d10`

```dockerfile
```

-	Layers:
	-	`sha256:99b344d2d1451234c62a01ec5f9ac9221e726c94a070c911eb994ffc9e03870c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65de8017361f5bd95197acdb9ee6c668e3c384cc8a330bf23618c20c2404e2c`  
		Last Modified: Fri, 11 Apr 2025 19:29:20 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:c8c9f924d43dad4966bbc045e1a0d101f1a342ec92528993a19850e9f770ce87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72661815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a13c6921667150b2cde5b0e0097252865b1cb890d09a71abba352d8e1e022c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.5
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:3855ba0ffadf30fe55a4369cfff203307898b7e858e0370a1c62a52ad5b8d04c`  
		Last Modified: Fri, 14 Mar 2025 01:10:05 GMT  
		Size: 20.4 MB (20368845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c990a79b734233bb986321cf5e861f55ca89577543a2d837e4658a26c4c434c`  
		Last Modified: Fri, 14 Mar 2025 01:10:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fc2b4d44c560608e2a8a931d225af4552d7c688731926d18e480028c5ea22`  
		Last Modified: Fri, 14 Mar 2025 01:10:02 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bdd2214b2dc468af2ba58383a96f2a108c5b400f367acb20275ba2d0229d5`  
		Last Modified: Sat, 15 Mar 2025 06:49:18 GMT  
		Size: 31.0 MB (31010005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aea3f9459191f5e6da3af7cbf9bd28d2275f86ad057711b5bad1e7b9bd56e`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92697fa690eb16f5f3a1f04e47a10869bcc5231665bd7f511c6b0bdc036dc8`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 817.9 KB (817892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cc89a24d8029aaa0bd6231af150db86c3620ed03d9956781752d3634b28fe`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40032bda6a57ee895b60e701cd79a2adb0e690a3c6087d54f7fdb06eda8f2488`  
		Last Modified: Sat, 15 Mar 2025 06:47:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:9b8f9221004aac4c24577c9c4c26355d63101933bcf811ffb69566e132a6ffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a749a5be401f08b78c2e9c0d9f21a9ec72ab341b7c251ad429d86dc3705b0a5`

```dockerfile
```

-	Layers:
	-	`sha256:b1e92b9f2c7997db127513c0e251912eff161f5a6b1d48c37992162fe3de25cd`  
		Last Modified: Sat, 15 Mar 2025 06:49:14 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aba897460592ac0c7e2499751934a29ad36040f4ae78ae56da6e43caa705ae7`  
		Last Modified: Sat, 15 Mar 2025 06:49:13 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:22d3f1ac483a883cdac3170ec0c48534399b4614fd7b14eef991983310d52e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75441805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550c839a96536c03825b2ea784a0c6865d61f91e0a5446810a49a24476e805f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.6
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
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
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b1af28aa6df6d954098666e1a7806a38dad8ccda5597ec97c4a33bb368511`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 31.7 MB (31680890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27badc48e7144558f50e29eefad78978f5b9b283ae420832976616a818e25d`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2abe1c95b14367537e000ce27b700e744674dbbf54603c7c19849713925f4f`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 822.7 KB (822682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9497720774556f9e9199ca165c9137abd44cc9521e30c99f31e99201ca6abf`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ce55bf35d81cdcc3a3502f45dcd9637bec07c398dc6b5c0483da389e68e57`  
		Last Modified: Fri, 11 Apr 2025 19:35:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:ee3b78e48acf450beaa636f62e09931106cd4ef6acee53ee3f5a725fae3468ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd14dff933ed1c7de2454f0d532ef20288caf72647212c72add8cd14d46f08b`

```dockerfile
```

-	Layers:
	-	`sha256:acb87901ec354a0af4a7a84773ae6b0e6dbdbb11efb6892eb02f3727c7338e58`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86956f22dc6528092933cbb7a30e36a293df41719fc70b86779be850ba58e6fa`  
		Last Modified: Fri, 11 Apr 2025 19:35:48 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json
