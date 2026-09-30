## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:f3c4ed50b4b975dc0dae20d211af04d16bead2101472ec0f9c0c8e05efeebebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:4-management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f50f1cbbec73032d248d516b043a6dd334302b571d71b68486e7b32a86efb45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120965519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4153f3bd8189c8889680694cac71daac93c2f79dcbbc9635b2a9992095af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

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
# Tue, 29 Sep 2026 22:02:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 29 Sep 2026 22:02:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 29 Sep 2026 22:02:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 29 Sep 2026 22:02:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 29 Sep 2026 22:02:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:02:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:02:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
ENV RABBITMQ_VERSION=4.3.6
# Tue, 29 Sep 2026 22:02:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 29 Sep 2026 22:02:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 29 Sep 2026 22:02:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:03:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 29 Sep 2026 22:03:17 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 29 Sep 2026 22:03:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 29 Sep 2026 22:03:17 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:03:17 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 29 Sep 2026 22:03:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 22:03:17 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 29 Sep 2026 22:03:17 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 29 Sep 2026 22:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:03:17 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 29 Sep 2026 22:03:17 GMT
CMD ["rabbitmq-server"]
# Tue, 29 Sep 2026 22:07:07 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 29 Sep 2026 22:07:15 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 29 Sep 2026 22:07:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:edd1ed89f0d443580bd42e5a10cd8736aba5a3438b2a0645c2ebb50119bb0eba`  
		Last Modified: Fri, 11 Sep 2026 13:38:39 GMT  
		Size: 29.8 MB (29764116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a4163f0af562d8256285cd3f7656dd6585c34a0f2f01c9890d80a5fe9eae0c`  
		Last Modified: Tue, 29 Sep 2026 22:03:43 GMT  
		Size: 46.4 MB (46371674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1972d98e9498c7993f67bf81239e8511935fe87cadb9cb1ed3d5a6d2bb82314`  
		Last Modified: Tue, 29 Sep 2026 22:03:41 GMT  
		Size: 9.0 MB (9018247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78bead6007fbb69b055ee1f57325693b0576a2a4ac351b4f5ce0b2dbaee236e`  
		Last Modified: Tue, 29 Sep 2026 22:03:40 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87ea5df114dcbf721ccb74f973638f98b6bfbf688605f53209570c280176d8b`  
		Last Modified: Tue, 29 Sep 2026 22:03:42 GMT  
		Size: 31.2 MB (31219508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638cbece8ddac20f778d1992727c4940f1d33eeef78728274b2e4939ec460aa`  
		Last Modified: Tue, 29 Sep 2026 22:03:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052e7efbeeb3b281549333e2aa5709578d211d3a5b80df1ec03fcc0b1b8ccb37`  
		Last Modified: Tue, 29 Sep 2026 22:03:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8bab38f045b74667a8e8981ea69790959cfa54df928c58e380afffce0c1d53`  
		Last Modified: Tue, 29 Sep 2026 22:03:43 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8e1cda52583811d4fb97b43f0d6dde4d64671720dde991ac7085e66b5f6e6`  
		Last Modified: Tue, 29 Sep 2026 22:03:44 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2bf0bf33d477146d45224ac41a57764217f92e1e42a259d2847f7fd64f80f4`  
		Last Modified: Tue, 29 Sep 2026 22:07:23 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc75d08b633c599a9cf0f048e8ef9183e0388137095ff637cf2c9422853c47be`  
		Last Modified: Tue, 29 Sep 2026 22:07:23 GMT  
		Size: 4.6 MB (4580259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:34800de7c6f9dca2324dc30354aa25f965600acab9e77136485c7197a615f479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516c469a00dea94cde616ed438de41cfd08e02f8c66c62bc0b8b65c40ae66726`

```dockerfile
```

-	Layers:
	-	`sha256:f383815217717e75c6459ea83ccd0241ecfbafea57b601ac9a2eda4c8148abdc`  
		Last Modified: Tue, 29 Sep 2026 22:07:23 GMT  
		Size: 2.5 MB (2470593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf068907deac472f487ff2135cb33e7f19ef46d15735a953475ac725e4804f`  
		Last Modified: Tue, 29 Sep 2026 22:07:23 GMT  
		Size: 16.3 KB (16268 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:23cb993b1d4f05cbfd135f7c2826507097c83a404fdf0cc4db5ba44f83245f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98139327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae18a8cd1ae1b241c510e9881a354551dffd6a51443d5ab32821a7be1568de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 11 Sep 2026 11:45:45 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:45:45 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:45:48 GMT
ADD file:683b4c146da2addbd0ae70d2240b8e3a57dd2f7582c952d416231fdd6496720f in / 
# Fri, 11 Sep 2026 11:45:48 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 22:02:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 29 Sep 2026 22:02:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 29 Sep 2026 22:02:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 29 Sep 2026 22:02:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 29 Sep 2026 22:02:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:02:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:02:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 29 Sep 2026 22:02:12 GMT
ENV RABBITMQ_VERSION=4.3.6
# Tue, 29 Sep 2026 22:02:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 29 Sep 2026 22:02:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 29 Sep 2026 22:02:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:02:33 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 29 Sep 2026 22:02:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 29 Sep 2026 22:02:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 29 Sep 2026 22:02:34 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:02:34 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 29 Sep 2026 22:02:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 22:02:34 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 29 Sep 2026 22:02:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 29 Sep 2026 22:02:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:02:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 29 Sep 2026 22:02:34 GMT
CMD ["rabbitmq-server"]
# Tue, 29 Sep 2026 22:07:19 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 29 Sep 2026 22:07:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 29 Sep 2026 22:07:19 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f98fce276933dc8d40e338c8a5447d14e10d972c731f074e9fcd9f9bb629aa50`  
		Last Modified: Fri, 11 Sep 2026 13:38:53 GMT  
		Size: 26.9 MB (26894925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f774e19fac2248eb2b485837e3b84e553008db308a9cb296cce2d5bc5dfaaaf`  
		Last Modified: Tue, 29 Sep 2026 22:02:58 GMT  
		Size: 33.4 MB (33397173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ad75d19436dde39e16986e9a13d1b5a1ff5b836fb3c269a663d2f35eb0ce2`  
		Last Modified: Tue, 29 Sep 2026 22:02:57 GMT  
		Size: 7.3 MB (7329321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796f53e9f323240f21e72d331067fdbaa4c6d135707cc292152ee61e84623399`  
		Last Modified: Tue, 29 Sep 2026 22:02:57 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ce91329ae802be37f94624945b8020d58b79aef3eacf4354a0c695183c6d4d`  
		Last Modified: Tue, 29 Sep 2026 22:02:58 GMT  
		Size: 30.5 MB (30506103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522e02583e485655f52bbad93e524dcc06935326d0c6f0ae81fc35dd0fc7eca0`  
		Last Modified: Tue, 29 Sep 2026 22:02:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b080b4b89968f56c84018fce60d3b769a35e718b053a9d076b96f22796953f`  
		Last Modified: Tue, 29 Sep 2026 22:02:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f6979d328b532b1002be8c533fa1d4e71a0123262343fd2a6888cbaa22a8fc`  
		Last Modified: Tue, 29 Sep 2026 22:02:59 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2738c28c1b9c270a49acba3a62666fed0cde1df93c5e79e31aa5d0aaf510a6a0`  
		Last Modified: Tue, 29 Sep 2026 22:03:00 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d8158d5dc1dc56094b7fd230b2c330af02bf6a7553dbb29a102b60d094fde`  
		Last Modified: Tue, 29 Sep 2026 22:07:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fc4efee828abf39df2bd6f96f2621a682af708951a1bce3382719c3784642d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd172dddd1afe6f92e7056172212d0f3ede2e2fae2706ffab7253fe2920919`

```dockerfile
```

-	Layers:
	-	`sha256:cea7f9e5073ebe2a3a89b5c9339169d16280054f7e1024d8a46545c856e80bf4`  
		Last Modified: Tue, 29 Sep 2026 22:07:26 GMT  
		Size: 2.5 MB (2471391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ce238468862890bc7165f44c6d4601907dfedd2e38a548674abc345a096ed`  
		Last Modified: Tue, 29 Sep 2026 22:07:26 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:63b6765be1dc072aed0b979651714df1e52ad48dc4e207b59b8007e2d2d2720f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118526728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9900e7c9e523a8be726552813b8b6c6a096b380072922dd97da1b8cd46056748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

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
# Tue, 29 Sep 2026 22:02:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 29 Sep 2026 22:02:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 29 Sep 2026 22:02:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 29 Sep 2026 22:02:31 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 29 Sep 2026 22:02:31 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:02:31 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:02:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 29 Sep 2026 22:02:32 GMT
ENV RABBITMQ_VERSION=4.3.6
# Tue, 29 Sep 2026 22:02:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 29 Sep 2026 22:02:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 29 Sep 2026 22:02:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:02:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:02:55 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 29 Sep 2026 22:02:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 22:02:55 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 29 Sep 2026 22:02:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:02:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 29 Sep 2026 22:02:55 GMT
CMD ["rabbitmq-server"]
# Tue, 29 Sep 2026 22:07:58 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 29 Sep 2026 22:08:11 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 29 Sep 2026 22:08:11 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:8a38824eedc553ba80cf1eb7df278a003340f7409fd4b9002bce07db8840a9a2`  
		Last Modified: Fri, 11 Sep 2026 13:38:46 GMT  
		Size: 28.9 MB (28941580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a72daf8bf0340ba43d1f146d1eba5e4ba40e5b5f40c1e6d746d6f50559321e4`  
		Last Modified: Tue, 29 Sep 2026 22:03:21 GMT  
		Size: 44.5 MB (44462487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b040444c22444ca345049ff949a7e7ece5a518ea9ce7540c69cee358c9799d16`  
		Last Modified: Tue, 29 Sep 2026 22:03:20 GMT  
		Size: 9.7 MB (9742949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10ead5837d62d05206c84aa542fa354cb7da6db29096afaf4ea1d0f270c6cbb`  
		Last Modified: Tue, 29 Sep 2026 22:03:19 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdee68229df95cfc6710fae8607ae116c01fd016ef27f8f292ce082de5bf2dc`  
		Last Modified: Tue, 29 Sep 2026 22:03:21 GMT  
		Size: 31.0 MB (30987593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fc8bf85b9d1e02bcc98b2a70f31aeb9dfe6112c37f33623fbc267832d0bffd`  
		Last Modified: Tue, 29 Sep 2026 22:03:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf55647d4604543b6adcc77f204f5fe9da081828eb20829d74a2efda057787`  
		Last Modified: Tue, 29 Sep 2026 22:03:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb6efe37310ea00eee496472ca60184bd123408b63a27d32546f60b7359dc68`  
		Last Modified: Tue, 29 Sep 2026 22:03:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce075c3e147017176812c802b3c819c6d28cd13cd30f80f58723663873def91`  
		Last Modified: Tue, 29 Sep 2026 22:03:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27a22ccaa5b8e22770f31a496780c09bbeb150acd130673198d6ec28e875ba1`  
		Last Modified: Tue, 29 Sep 2026 22:08:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5109659bcb6244a5aaf9e316af48add4075ff152c7f158621295bcbd2a5d5912`  
		Last Modified: Tue, 29 Sep 2026 22:08:18 GMT  
		Size: 4.4 MB (4380473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b2fd6406c76386ec578604fb3817e8a4a86332f9524c81c6fd3b6c5c5c238665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3451644e5440ba25df20843ca4a0a64de4c1eee375b41cc921f5e08e5ba1261`

```dockerfile
```

-	Layers:
	-	`sha256:3db9806fe523fc384c5d9da0ba4fdb918cf1652278960ed4cb1228e976887426`  
		Last Modified: Tue, 29 Sep 2026 22:08:18 GMT  
		Size: 2.5 MB (2471653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed23151db91b075fd1661cb14fd42cfefa01437d969aa6dd630283ab35c09cea`  
		Last Modified: Tue, 29 Sep 2026 22:08:18 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:fc252e59b375d20e78e90ca4658f75bffc553eb745efc479b28b3f68ca75ae97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9763f6229f0c6891cb827644c3d37ae6ec63e7b7ca9b507e3cc58a9d73880771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

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
# Tue, 22 Sep 2026 20:04:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 22 Sep 2026 20:04:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 22 Sep 2026 20:04:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 22 Sep 2026 20:04:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 22 Sep 2026 20:04:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Sep 2026 20:04:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 22 Sep 2026 20:04:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 22 Sep 2026 20:04:29 GMT
ENV RABBITMQ_VERSION=4.3.6
# Tue, 22 Sep 2026 20:04:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 22 Sep 2026 20:04:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 22 Sep 2026 20:04:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Sep 2026 20:04:59 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 22 Sep 2026 20:05:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 22 Sep 2026 20:05:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 22 Sep 2026 20:05:02 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 22 Sep 2026 20:05:02 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 22 Sep 2026 20:05:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 22 Sep 2026 20:05:02 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 22 Sep 2026 20:05:02 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 22 Sep 2026 20:05:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Sep 2026 20:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Sep 2026 20:05:03 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 22 Sep 2026 20:05:03 GMT
CMD ["rabbitmq-server"]
# Tue, 22 Sep 2026 21:45:37 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 22 Sep 2026 21:45:38 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 22 Sep 2026 21:45:38 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a7067f7ee788cc3e90f83fa0ac84d48a200fde4469a2a5e638f059842a8f11d1`  
		Last Modified: Fri, 11 Sep 2026 13:39:01 GMT  
		Size: 34.4 MB (34376958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479c9135ef3ff7948fa33db75718e4d70c5746025a7a1d8d143ccf32bef0e7d8`  
		Last Modified: Tue, 22 Sep 2026 20:05:51 GMT  
		Size: 39.6 MB (39606239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a5778ab699775d6f81014bb4505fe6e2865330b0eeec3223cbcdcf2fb9877`  
		Last Modified: Tue, 22 Sep 2026 20:05:50 GMT  
		Size: 9.6 MB (9613912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008ce6e4c1d3622c509ef94fc659efc29f7ff4f11061dfb465df2bcd5c29e5b5`  
		Last Modified: Tue, 22 Sep 2026 20:05:50 GMT  
		Size: 9.7 KB (9685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44097c167eb72e6c53294343438a939feee7e639ccf55e9ca1d5c15bac8ab8a`  
		Last Modified: Tue, 22 Sep 2026 20:05:51 GMT  
		Size: 28.8 MB (28771737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7c0a9b66bebc18406ca6aea23e8e9f16ce8426514de3961e0fc1744ab3b9b8`  
		Last Modified: Tue, 22 Sep 2026 20:05:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dc7637da998619f8378ff8dcd9604d976f965d0aa37273f373e34347556c86`  
		Last Modified: Tue, 22 Sep 2026 20:05:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a946b412674b0f9976e62624e61388cca1243f10b6d3abe2fd0548107391a406`  
		Last Modified: Tue, 22 Sep 2026 20:05:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ceb294057fe28a44712d997737c64fa6f43d4989ed916d76a6812cd48a843`  
		Last Modified: Tue, 22 Sep 2026 20:05:53 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83358158fbfd88ad8044788e0bc3547bb6579b8a6f440a051789488870243c`  
		Last Modified: Tue, 22 Sep 2026 21:46:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:39a0bb8b03f7abfda43984fa906f34d13fd540f6f3871177779cfa6e02a76421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2491356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2f9472cd781fcf6f1253a8788ea8a63ace01628a16c930f46c44cc11d4d228`

```dockerfile
```

-	Layers:
	-	`sha256:ad96dfdee09e17df62a8e528966080a59ddd525ad645b9005af498176de80951`  
		Last Modified: Tue, 22 Sep 2026 21:46:01 GMT  
		Size: 2.5 MB (2475046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5bbaa4dd5cfedd3f0ab5913376037b689bd4bcf2dd29d1b954762746aef3c5`  
		Last Modified: Tue, 22 Sep 2026 21:46:00 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:deef910f937c602f486fae233454ac2e56ee7c98b651b23988a35438775146af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105793835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a214ec8bf6a868f0cab14357cc2b707518d5ad6442f4863a809d6273e7d023`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Sep 2026 07:43:12 GMT
ARG RELEASE
# Mon, 07 Sep 2026 07:43:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Sep 2026 07:43:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Sep 2026 07:44:03 GMT
ADD file:b9e2d6d291d1ed94a7f69f48c708e50bb181af64736f283e384c42c217fefce1 in / 
# Mon, 07 Sep 2026 07:44:07 GMT
CMD ["/bin/bash"]
# Wed, 09 Sep 2026 04:07:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Sep 2026 04:07:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Sep 2026 04:07:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Sep 2026 04:07:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Sep 2026 04:07:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2026 04:07:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Sep 2026 04:07:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 09 Sep 2026 04:07:56 GMT
ENV RABBITMQ_VERSION=4.3.5
# Wed, 09 Sep 2026 04:07:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Sep 2026 04:07:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Sep 2026 04:07:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2026 04:10:05 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Sep 2026 04:10:14 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Sep 2026 04:10:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Sep 2026 04:10:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Sep 2026 04:10:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Sep 2026 04:10:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Sep 2026 04:10:14 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 09 Sep 2026 04:10:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Sep 2026 04:10:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Sep 2026 04:10:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Sep 2026 04:10:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Sep 2026 04:10:15 GMT
CMD ["rabbitmq-server"]
# Wed, 09 Sep 2026 08:34:13 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 10 Sep 2026 05:45:08 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 10 Sep 2026 05:45:08 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:43253cac98e0bd3027a1f91776c6624571e5e05e6df478c1452294560ee5ff91`  
		Last Modified: Mon, 07 Sep 2026 07:57:26 GMT  
		Size: 31.0 MB (31049202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b58e4430419ed5705cf7cff214eaa19c5b4d03d7df32ba4df92e4483282f3`  
		Last Modified: Wed, 09 Sep 2026 04:16:35 GMT  
		Size: 35.2 MB (35228253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a9ec13efc66307917dd99fb99a924f327adf54e58af508fb8f6777f9b295a`  
		Last Modified: Wed, 09 Sep 2026 04:16:28 GMT  
		Size: 10.9 MB (10853353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdde48530b3542e0d76418e9ce967dad412b4291f598567ad4541c6d297a817`  
		Last Modified: Wed, 09 Sep 2026 04:16:22 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2247f2170afe9240c20219f188a6b373bfdffe60d2ab4741e472cd2fdd27b797`  
		Last Modified: Wed, 09 Sep 2026 04:16:34 GMT  
		Size: 28.7 MB (28651294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f3ec4d43a6790ca0bc0ae5556b25d2f00ac177a994f915b9c671d4956bd38f`  
		Last Modified: Wed, 09 Sep 2026 04:16:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1f2c1e3370af83eadefcc43a754fc1942ce7c6f4777a093f9bebf85edf488e`  
		Last Modified: Wed, 09 Sep 2026 04:16:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b38049e80d33c3a9685c3e3262068e3174d90ae89d8a883d264645b5192246a`  
		Last Modified: Wed, 09 Sep 2026 04:16:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e612d495479b5eaa69a59f27b7498f69d2f4ef89759a28ed146c62f090232b`  
		Last Modified: Wed, 09 Sep 2026 04:16:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72aea3ffd2b0c883c4fc81cd9c12045fc4a939c748c660a0ba75dab6d9062fd`  
		Last Modified: Wed, 09 Sep 2026 08:35:31 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a99e598054ae3959e3533630a55beadc95935b43c3309ebdb19c648e212bd79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15be56bfc18cff62ef5d8393bf738e8db86ccedd40393cc8bd7a27386c1bf0e7`

```dockerfile
```

-	Layers:
	-	`sha256:d8de81e2919bf49cab68648d3a1e93d6721c8c9782e7c8c782e40a8a84c39fbe`  
		Last Modified: Thu, 10 Sep 2026 05:46:26 GMT  
		Size: 2.5 MB (2462958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49202e54444ad5da544d8c00b382bde9e8e283e69eccb070a6d52f8c39830988`  
		Last Modified: Thu, 10 Sep 2026 05:46:26 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:63add33e214f7641dd8474d4e58f05d5615f74ebe86444ec82bbe989b7f71128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108182600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d921abf9af417c3a0fb533bb3131f94ecb7d20fdad420b94af0f2e70b18bda9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 11 Sep 2026 11:53:08 GMT
ARG RELEASE
# Fri, 11 Sep 2026 11:53:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Sep 2026 11:53:08 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Sep 2026 11:53:09 GMT
ADD file:62feb922e0e5d063c128e1d59ecbc5c2274c804b45055ac83d490a0a0c953700 in / 
# Fri, 11 Sep 2026 11:53:09 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 22:03:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 29 Sep 2026 22:03:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 29 Sep 2026 22:03:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 29 Sep 2026 22:03:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 29 Sep 2026 22:03:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:03:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:03:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 29 Sep 2026 22:03:26 GMT
ENV RABBITMQ_VERSION=4.3.6
# Tue, 29 Sep 2026 22:03:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 29 Sep 2026 22:03:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 29 Sep 2026 22:03:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 22:03:38 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 29 Sep 2026 22:03:39 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 29 Sep 2026 22:03:39 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 29 Sep 2026 22:03:39 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 29 Sep 2026 22:03:39 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 29 Sep 2026 22:03:39 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 29 Sep 2026 22:03:39 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 29 Sep 2026 22:03:39 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 29 Sep 2026 22:03:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 22:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 22:03:39 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 29 Sep 2026 22:03:39 GMT
CMD ["rabbitmq-server"]
# Tue, 29 Sep 2026 22:09:00 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 29 Sep 2026 22:09:00 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-x86_64-unknown-linux-gnu'; digest='31887e0dc96e7654a9dfa007182af1281ee2fd4045de011ca1af72b0b962df51' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.35.0/rabbitmqadmin-2.35.0-aarch64-unknown-linux-gnu'; digest='cd97862b5a19688779717bbd920bbf299a960ad6cafcd9121bf764c01e4c66eb' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 29 Sep 2026 22:09:00 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2d1aac92a29a4eacd140d431dc526f6da099043772d537d221717429ee877b2a`  
		Last Modified: Fri, 11 Sep 2026 13:39:18 GMT  
		Size: 29.9 MB (29945392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b069188abb6eacf3e98dd8ce0b154809127bef993f8c1034f1db78eb1e28e3`  
		Last Modified: Tue, 29 Sep 2026 22:04:13 GMT  
		Size: 38.7 MB (38688929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfe3999ccf676b582d7d17443601bda5ccdb9e111e511b76393023ccff23a8f`  
		Last Modified: Tue, 29 Sep 2026 22:04:12 GMT  
		Size: 8.6 MB (8647066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3836027ea231497bb25986372dee6f97c52facf556c8534b8ab7088d7b1d27b`  
		Last Modified: Tue, 29 Sep 2026 22:04:12 GMT  
		Size: 9.8 KB (9787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5653a8398040b1315140a441fa3e60a82c6b51639d43417f92580a3e7fea060b`  
		Last Modified: Tue, 29 Sep 2026 22:04:13 GMT  
		Size: 30.9 MB (30889372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56020845e4b1b36fcf77260e2a3489f435b510f4e594d71a4ed51036ccc25188`  
		Last Modified: Tue, 29 Sep 2026 22:04:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5740d44aa564a89cc4799a4e6445b0a4d528c9b555305061045a23ca8143cf`  
		Last Modified: Tue, 29 Sep 2026 22:04:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39854f295ba79b088cd8e502d1be20a83ea3165502cb21f7ac547f0bf3b7a72`  
		Last Modified: Tue, 29 Sep 2026 22:04:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1192e3efcdb38dd55b349efd9561e805eb42d676b18c0d9ebd6c43de6c27cf95`  
		Last Modified: Tue, 29 Sep 2026 22:04:14 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae82e6f0877a2a0cb81347c5f70a0571e7226356a0beb12704c644dfd9af503`  
		Last Modified: Tue, 29 Sep 2026 22:09:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b6b3b78bba256d5bfa5327d1fa0f79ce2312cb16b0415723e09da24794727ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335b61d0027cd1a53f21b1ad3fe90ffe4cfee07f48a5ff5c388a18d96a06637f`

```dockerfile
```

-	Layers:
	-	`sha256:20d1fd2165b265b153f5d122284a24fab74ffbd24bf05bd669610ae03aa8c926`  
		Last Modified: Tue, 29 Sep 2026 22:09:11 GMT  
		Size: 2.5 MB (2472702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5f28138080fbececea41582c521e3533537bac4d683104b6efc87dd0dc0952`  
		Last Modified: Tue, 29 Sep 2026 22:09:11 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
