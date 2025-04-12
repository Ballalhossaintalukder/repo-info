## `drupal:php8.4-apache-bullseye`

```console
$ docker pull drupal@sha256:96c1faf371784008b929803adbe02ba17468cd3b94b9c71d74c4cead1f5a218c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:php8.4-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:1fc4f9f7185e6c15a91fdbd78d78d112e0af4ae1a416c4db155323ec2aaeca63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191686706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38d3519204b83898a6daf445b8ffc9531e5086ab4633af8676902d202e4ec7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b00bfe3b38b6df472bad086baec8091a3d690dd8f53d20a9e83eb3cc6a9a82`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7838bb3046277cc9493b13ccca25357b8063aedb9c3d9b6958688e469376dd20`  
		Last Modified: Fri, 11 Apr 2025 17:02:28 GMT  
		Size: 91.7 MB (91653833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79987005c8824198c75a0b9876befc066f346f42221764e8d00c4b6f26c16ea`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c594422c6945c12b3e74f30a9bc0f51fff26da57f7ef6771a4addae4686ed`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 19.1 MB (19064215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b86c6ba776a767da47cddf9e7de266eb384fdb9bb0a303dbe4790817493a7a7`  
		Last Modified: Fri, 11 Apr 2025 17:02:27 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6393ca4723edaa574aa9c6fbb2162e868828e1eaa01ece363f6d0c723f3a6c2c`  
		Last Modified: Fri, 11 Apr 2025 17:02:27 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f8a4dbf0d5e0db95a076afdd81182858dd615a5357358dde426e932733bcca`  
		Last Modified: Fri, 11 Apr 2025 17:02:28 GMT  
		Size: 13.7 MB (13737595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407afc1c51b5162e239a7ad578fc9209c2f5c2e3668ed4a859d878a2c9e39cf0`  
		Last Modified: Fri, 11 Apr 2025 17:02:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4ee4d91ccc74316913d174864d7dd816a3c527776161d095eb93191db238bb`  
		Last Modified: Fri, 11 Apr 2025 17:02:28 GMT  
		Size: 14.1 MB (14091446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6580d68ec2c92685fc9c337e2afb1c94ae7314a15d0b492164704197787c0`  
		Last Modified: Fri, 11 Apr 2025 17:02:28 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab56ef12b3ca3a42e4eab353a3fa14e7a2e5e94f3bf5b2202cc5581d9ff74ac1`  
		Last Modified: Fri, 11 Apr 2025 17:02:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0fbba489a346233e47360113504ee65ce2fb89e47037847e30b22955b1100`  
		Last Modified: Fri, 11 Apr 2025 17:02:29 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9be375f4ccc4d933d28fc132ade4b0d808bed5bd1fbf0c526772d188496c00c`  
		Last Modified: Fri, 11 Apr 2025 18:11:19 GMT  
		Size: 2.1 MB (2061772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06440ca8a819f569d641d8030cd9f1034e2d5dd34d872e551b7df600ab98ee51`  
		Last Modified: Fri, 11 Apr 2025 18:11:18 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8647ed7caa840f82c805ce2f4d7799406595a12372863fd6e7c83132b39f74fc`  
		Last Modified: Fri, 11 Apr 2025 18:11:19 GMT  
		Size: 750.6 KB (750619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90924a22efb5de83b71d91597e9eb35a1304720f40f910bf5317be6c30bf4d4c`  
		Last Modified: Fri, 11 Apr 2025 18:11:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14248465bd3f414b6a5e73a9765980c4540aeee43a87c464f43b3874a7823c`  
		Last Modified: Fri, 11 Apr 2025 18:11:20 GMT  
		Size: 20.1 MB (20063914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ee161d3b8716de34fbec3a5dd80899ba9659ae724c98618eacd387223f52e562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795241be2a1c2626af6281728d4517c94d36e282d7d994ebfb22084aabf9c957`

```dockerfile
```

-	Layers:
	-	`sha256:c9c79c85a6f377e7e59992d55f3b8be52fb68eb9704c3f38c5768d25cd833dbb`  
		Last Modified: Fri, 11 Apr 2025 18:11:19 GMT  
		Size: 7.0 MB (7037089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faa929c7c34cd1178fbe24b5b05e766fa2b9a2e28d9ddfd254ea5b6bf758184`  
		Last Modified: Fri, 11 Apr 2025 18:11:18 GMT  
		Size: 36.7 KB (36682 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b6106909c89eb640dfd8c7f577ce30c30746df75c90fd57bf28457fb1b168f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160816631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776e91be69dae040e637523ea2a366948bf0aa4b991e58dcc01dfafa65b4cd6e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92905eaafdfcd979db495c58a48e731910176c26b376274ee7cb223a8c038a9b`  
		Last Modified: Tue, 08 Apr 2025 02:22:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b830cfc597b4f010f0ffe2c61b85171bd1913ba887acd5db1195c0f4451fc74`  
		Last Modified: Tue, 08 Apr 2025 02:22:08 GMT  
		Size: 69.3 MB (69324658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced68bec9de0dd3b531c6d6097fd77987a5e1401ad87f2c13daa930ebea5d07f`  
		Last Modified: Tue, 08 Apr 2025 02:22:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15cd11cd94a45d3f42639fe5069e8576f9c3f352afd3e318aa2eeee206f9e06`  
		Last Modified: Tue, 08 Apr 2025 02:25:52 GMT  
		Size: 17.8 MB (17817086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050fc544b8fdd7310c891ad6ba3e06deb200761ccbe5641d3103f549f3c0801`  
		Last Modified: Tue, 08 Apr 2025 02:25:51 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f480ab0c7e7dba154ce3b39509ee85942760d1affd46dc47a28e625198f925`  
		Last Modified: Tue, 08 Apr 2025 02:25:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d292115a671d0e61e335837ad9a397d0b2411bbba69c6c1a560e489fe154ac3`  
		Last Modified: Fri, 11 Apr 2025 17:31:01 GMT  
		Size: 13.7 MB (13735932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d18a90df41904e5a04a42e8d7407fac04dc54abc341fa4da3f41e4785f50a`  
		Last Modified: Fri, 11 Apr 2025 17:31:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdf60b9c53ca0da6bf0164f62142b1128feb221d784984bd7ad9b367d563f36`  
		Last Modified: Fri, 11 Apr 2025 17:31:01 GMT  
		Size: 12.3 MB (12260289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7561ecb0b71b49792096439e53e68f8bb775e33b416aa389ce1756ad93d95e0`  
		Last Modified: Fri, 11 Apr 2025 17:31:00 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4865bb0d78323d7085bd69d5d639460c4e2a95e8e324390534eb80b5cedf0de8`  
		Last Modified: Fri, 11 Apr 2025 17:31:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824b1754635509b6a1f1555fe9613280d29d691cb6e7aed46b6d983edfb8ee53`  
		Last Modified: Fri, 11 Apr 2025 17:31:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb1bc150e660aaf5c441e6a1522276e1ad08ab52345797e13a0ef02fcd290c8`  
		Last Modified: Fri, 11 Apr 2025 20:24:14 GMT  
		Size: 1.3 MB (1319127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861cb402d7172b27bdcf0ff6b4489e28c97c04d58bfe4dda63e6b01af5d292ff`  
		Last Modified: Fri, 11 Apr 2025 20:24:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d76bd2113c76efe76b200d79dc31956a0f27fb105ff3bdf24f3453940bf5602`  
		Last Modified: Fri, 11 Apr 2025 20:24:15 GMT  
		Size: 750.6 KB (750622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dfa8105c98e51c8e84163f6eeaa439b388790d7f72b75640c666ea2c4dcc97`  
		Last Modified: Fri, 11 Apr 2025 20:24:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7739474aec6cd09a0a776791fac04c004ccdf363426b0fc361e7ce2cb6c85415`  
		Last Modified: Fri, 11 Apr 2025 20:24:16 GMT  
		Size: 20.1 MB (20063870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f210d58adde1cd60231bff65a0a70c1d9d581c36976c274d5a7aac6a4dd555c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6882792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58cd63cac0cda1e4cdf4f89fb5dc1ffd0cb5463dadb962fa0799ce11e4cea57`

```dockerfile
```

-	Layers:
	-	`sha256:a25719faeb71269a36cba88e1746d6dd78144c69f0ebb8d120b968f0c57b618d`  
		Last Modified: Fri, 11 Apr 2025 20:24:14 GMT  
		Size: 6.8 MB (6845985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f82aaaaea5351474051803cb1ed23e31e07ec3c2837b4d55ea01e7479b7d28`  
		Last Modified: Fri, 11 Apr 2025 20:24:14 GMT  
		Size: 36.8 KB (36807 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:391c5b855e55181bcb2f252db5689f84e960fbcc17c635c985d97dde560bcf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184971304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5171129f0b0ffbca4d25e9fdfdb0914adb1e468f7b95986b55318ecb14b920`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d395ead3808d660fade41a9d9e7a84bbfab9a7365f9a865f3b9f811603f5611`  
		Last Modified: Fri, 11 Apr 2025 17:13:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c411a9f034b3f145c0d92dbc82007b803a51634c501d9cc3fe6756e5c91c8d8`  
		Last Modified: Fri, 11 Apr 2025 17:13:44 GMT  
		Size: 86.9 MB (86940123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14073c5ce0dd3f253e624762299b5c965137eed6b963c8019ceea5e7897ca178`  
		Last Modified: Fri, 11 Apr 2025 17:13:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb47b5fd0e87a957c25659f046ca622c1d63a998fb8119c0398c241dba5fba3`  
		Last Modified: Fri, 11 Apr 2025 17:16:57 GMT  
		Size: 19.0 MB (18981598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aefab3cb2d706e4485250a5a4de364aee0d182a97cc435661d0d07c5e077bd`  
		Last Modified: Fri, 11 Apr 2025 17:16:56 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba4e0e7ca67b84c5346f1bfe58f621275f676e9b2022e5bf2b9abc9975193e9`  
		Last Modified: Fri, 11 Apr 2025 17:16:56 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e879da707dcf1d69c34ba64f2038af9fe13747b984ec632365a4bd14535f6c7`  
		Last Modified: Fri, 11 Apr 2025 17:16:57 GMT  
		Size: 13.7 MB (13736828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841a49e1d11acc418a8822080c8c3b66db3dd9010c412370ae4615aa9ef5d86b`  
		Last Modified: Fri, 11 Apr 2025 17:16:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e30b2e2b21b0f83cf0618ee96258b3a304abba61c552ca4fbf52075124467db`  
		Last Modified: Fri, 11 Apr 2025 17:16:58 GMT  
		Size: 13.8 MB (13782054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f92744fecf3a9e0d56a839c489819176b5b5e526446bf7eda1c275058fe769`  
		Last Modified: Fri, 11 Apr 2025 17:16:58 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff8f64bebe79ba18e9c60cb79dfaf4f2bb4ccad1a47ba984635bc2dee3ed46`  
		Last Modified: Fri, 11 Apr 2025 17:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db65e4f9b84e15d0ad46ba60b88025dd200f53b36d72dd3458f47a1c6ec45abd`  
		Last Modified: Fri, 11 Apr 2025 17:16:59 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815200b64852fee997aba51d944a44b5bc43340b509274ee2f402a72aa7db5d`  
		Last Modified: Fri, 11 Apr 2025 20:30:41 GMT  
		Size: 2.0 MB (1960802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850642861e7a95e687c9925321d849cd2778907166c3d3a9e27c30168e402ca2`  
		Last Modified: Fri, 11 Apr 2025 20:30:40 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8638db4fa8daa7062b13ff031c1012ef42ecdacedf3a37b81bd90eaf8caaa4`  
		Last Modified: Fri, 11 Apr 2025 20:30:41 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76259c9f51c88214e8905156c58c5e4f39b4ae49ac0d0ada2817620a40d9bfce`  
		Last Modified: Fri, 11 Apr 2025 20:30:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68fc24582ba125a2b77745fab2d1ed54106a28291c2deb4b046f37b05d0231`  
		Last Modified: Fri, 11 Apr 2025 20:30:42 GMT  
		Size: 20.1 MB (20063871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:9e94f0693c378d7f562ae035bcc709c9a874173a1b9f3f06dd280dae263dcea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216aed18556d8142b8812954edab54b537dd22fdc1e88d7e09c8f7dabbcb48f8`

```dockerfile
```

-	Layers:
	-	`sha256:64336e14a71b215143557380454c59edc4013afba254fd8a1750eabdab302c35`  
		Last Modified: Fri, 11 Apr 2025 20:30:40 GMT  
		Size: 7.0 MB (7039885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd29df6a87d6f731878bdff457b5826122c970eddbce156f434543be30fa652`  
		Last Modified: Fri, 11 Apr 2025 20:30:40 GMT  
		Size: 36.8 KB (36843 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:368988ded73bc6d6c0f50cfcfb8bb85cce60f26c9a564de29cf223518b3f4d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194571125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf552449b116f4380f656f0c7013e601958319417448476001704154eccc99e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47811393257555765f07cc0843dcbb2bc0a652c3f54def7f3cdec0ecafd0f76b`  
		Last Modified: Fri, 11 Apr 2025 17:02:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8b5411fefff577d31f7b3d69694e667dd0d93da08db368d3112cb9e4648f84`  
		Last Modified: Fri, 11 Apr 2025 17:02:54 GMT  
		Size: 92.7 MB (92724607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa88fa5ec2efed365e7d1a722ec2437ffdcb9436ff26cb8bc9dad52cbf9243c7`  
		Last Modified: Fri, 11 Apr 2025 17:02:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6a492adf661cb9dbea546bcf73cd65eae03dd8cd54e56e1fbc08d6fcac41d`  
		Last Modified: Fri, 11 Apr 2025 17:02:52 GMT  
		Size: 19.6 MB (19552762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d01b0f2e9bd0056dbe6195fecd637efc5c759e167432eff4df8e7ca91d2241`  
		Last Modified: Fri, 11 Apr 2025 17:02:52 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9040e101b0f73e8b9add2bd687862d647051dae9ea795c43ebabee58d5f140d1`  
		Last Modified: Fri, 11 Apr 2025 17:02:52 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d9bc5bd0b7a3e6442f29607e094227071ac2a6c17e3e131ad9c5d6e2dcfe5b`  
		Last Modified: Fri, 11 Apr 2025 17:02:54 GMT  
		Size: 13.7 MB (13736798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be6d04b3ec39dbc26a3acaac53468be4f346bc64c80621b251f4b7a5e3ccbc`  
		Last Modified: Fri, 11 Apr 2025 17:02:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ededde0022a2b2f4bff43ebc020a3f7f7b5599122897b6e3875c636b1c70f`  
		Last Modified: Fri, 11 Apr 2025 17:02:54 GMT  
		Size: 14.4 MB (14387761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a0df67c5b43b13613dbede3aa4b3ed2f8103cc222707d3c5ebabecfb748407`  
		Last Modified: Fri, 11 Apr 2025 17:02:54 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a50bf03b70fa752662a4ced486e562eb9aecfd59b5545037fb19e2c784f3064`  
		Last Modified: Fri, 11 Apr 2025 17:02:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c403817e85f75c6b21d9ca78aec691b38939391047b1f5597d22628246557`  
		Last Modified: Fri, 11 Apr 2025 17:02:55 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e514b5f6b281571d70168b1f8e375272e3bdaca5cc3b964b4b0c1c3e3cbb9a3f`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 2.2 MB (2164154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c98c4b37cca75ae2448ab9fe655f25a2b98643509209b760dae3c9f7d16a9b`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a428f473f711fa4829f0f00f8efc173af558d4d8a2f2f503c98db3232f517`  
		Last Modified: Fri, 11 Apr 2025 18:11:12 GMT  
		Size: 750.6 KB (750621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c091a348aa62424ace99dbd419c2934a89bae03a37dedb1923ec2f7b9bca52a`  
		Last Modified: Fri, 11 Apr 2025 18:11:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a986216d9ce707fbb45a00e064f5960bd2100c079548aa701da90f30ce0993`  
		Last Modified: Fri, 11 Apr 2025 18:11:13 GMT  
		Size: 20.1 MB (20063937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5f66530391d8488171074428b4931f4d707f2f4b1f8590ba8595f9e147eb1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7064330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d0c7627d9acefcc4a84b6cbf6aeccb51bb3efe5c2284402526ee20014d730`

```dockerfile
```

-	Layers:
	-	`sha256:fb3461f3323b2661289651c38f89055316b3d5be0b67d2a67b3606d9783bcf45`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 7.0 MB (7027691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0c4d5d138f60e64be9ac98e113d337c7da1f1627d365939ea46c7a786ff20f`  
		Last Modified: Fri, 11 Apr 2025 18:11:11 GMT  
		Size: 36.6 KB (36639 bytes)  
		MIME: application/vnd.in-toto+json
