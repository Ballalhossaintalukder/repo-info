## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:091c9c7c4b6a6b4d2329d54b7f40d323741785ca990469df9a1d706be0db43e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270913951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073491946f86c298c2b044c6faa71346849873f54c330a2a55e8befad1f83cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:29 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 29 Sep 2026 18:38:29 GMT
ENV MYSQL_VERSION=9.7.2-1.el9
# Tue, 29 Sep 2026 18:38:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:08 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 18:39:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf478cf509db6ad95b6b7148d5cfe735c6e909e3c14c0034c9c9d4062a95722`  
		Last Modified: Tue, 29 Sep 2026 18:40:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7083062f81513393b74998dc5c306f06717045eb36c962951f70c400e021fd1a`  
		Last Modified: Tue, 29 Sep 2026 18:40:32 GMT  
		Size: 783.6 KB (783561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b7f80eabb905d2feb6ae9d7b821c7518d2954d8968569d6f47fd1c28eeffe6`  
		Last Modified: Tue, 29 Sep 2026 18:40:32 GMT  
		Size: 6.2 MB (6198186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22dfff9583fa20446a01e68e54f090aa3125747d11faeb5e21b0e305224da15`  
		Last Modified: Tue, 29 Sep 2026 18:40:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c0190609f1e1bb5d7f176fb82d1079493e6d8c947ff03b21b310c5ca583840`  
		Last Modified: Tue, 29 Sep 2026 18:40:33 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0475d97c302c8ebf110f9170ac4fe15ae554d178809d3f757710fbc63bf95b`  
		Last Modified: Tue, 29 Sep 2026 18:40:35 GMT  
		Size: 57.0 MB (57046643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82925b7a5a989b37b675e761ca97660e4833ae783142bf794238a00f7562618`  
		Last Modified: Tue, 29 Sep 2026 18:40:33 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072928172793eb61845a57d8904ba0cc84ec9ddeeb12598982d7ff1cdf49f13`  
		Last Modified: Tue, 29 Sep 2026 18:40:37 GMT  
		Size: 158.9 MB (158934565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe6d1db8f226d7925c666685b2c8c45fe86063dd617cb77801a9555ca3288b2`  
		Last Modified: Tue, 29 Sep 2026 18:40:34 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9ca2d5c3dc341ac8a8e5b7ab498082d8e8e423422e9ea50742b1e7b02ce03ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16833394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79cac349c6c836ab6771692e86c194f97a41af4249b4867af3f927cdcfcf277`

```dockerfile
```

-	Layers:
	-	`sha256:867c393ef9de058d3a4931e7b831158098142cd0cd155dfe14f94c03ee043fa0`  
		Last Modified: Tue, 29 Sep 2026 18:40:32 GMT  
		Size: 16.8 MB (16799187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7ac0deb5ec7405106d6fe2ec83d65205bb50add864e22f2c4f357c42fec74d`  
		Last Modified: Tue, 29 Sep 2026 18:40:32 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1e0ac1b5ee3ede4c0d6ada2f4ca3a696923e1ea5c93201585336b2429deb3e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267376419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b252d79c338807539aa1aef682fdd08236a3eab5bc83531a570ea4558563623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:22 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 29 Sep 2026 18:10:22 GMT
ENV MYSQL_VERSION=9.7.2-1.el9
# Tue, 29 Sep 2026 18:10:22 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:02 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:02 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 18:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f703d9bd77dcccb2074ba618fe121f4ae27d466f7ceb608e4ed2b8199af8ad4`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8e363b3cda4119b4292819fb2e93a3fb90c6b11e89e9cc0cd149b1535ec23c`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219d9ec7e4ea261a9c51f7865e22c7c53d286c2f8552915b544349f15b23ae16`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 5.8 MB (5822795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e63c9f7bc7c28953914ed87a3d2745bb6bcd00d6cc048aedcc03c274e7da74`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5ca6c869cff0f7090b50c26c040b8aed0bee1c4b38044aa0a1f8bee6a3f941`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707f1b33883275492acb12088f0c0443266ea5ee8cabf4ab68bd4e1e04b2750`  
		Last Modified: Tue, 29 Sep 2026 18:12:32 GMT  
		Size: 57.1 MB (57113219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f0084b0dca242c3d6af4c67084ff32c6c4ae15ca863a6561ca68b14c9e133`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a23372beb3cde28144bcc091455c0efbb7796d59df8ff7885c3039b3690b67b`  
		Last Modified: Tue, 29 Sep 2026 18:12:34 GMT  
		Size: 157.2 MB (157208110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d450c3f8c0fe4ba68a5482628f4a6ce483aa48c51cf592c05cc3a94226f60de6`  
		Last Modified: Tue, 29 Sep 2026 18:12:32 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a5e838c4cd6079ce367b07022c88af50344194d4e87e3847a5ac68c42176df8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64622af0a3ad471954afe840f75d230e8cf7376e610cd4d78f366c02d46da16f`

```dockerfile
```

-	Layers:
	-	`sha256:f81b47fe9fdb56cc31a50fbc87667633b102af0d8d576bdc820d8d0effb768bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 16.8 MB (16797623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59eff3b70e8d8daefa78b331e5e4af1b1e29c27958e080af0198fdfdad6013f8`  
		Last Modified: Tue, 29 Sep 2026 18:12:29 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json
