<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:26`](#mysql26)
-	[`mysql:26-oracle`](#mysql26-oracle)
-	[`mysql:26-oraclelinux9`](#mysql26-oraclelinux9)
-	[`mysql:26.7`](#mysql267)
-	[`mysql:26.7-oracle`](#mysql267-oracle)
-	[`mysql:26.7-oraclelinux9`](#mysql267-oraclelinux9)
-	[`mysql:26.7.0`](#mysql2670)
-	[`mysql:26.7.0-oracle`](#mysql2670-oracle)
-	[`mysql:26.7.0-oraclelinux9`](#mysql2670-oraclelinux9)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.11`](#mysql8411)
-	[`mysql:8.4.11-oracle`](#mysql8411-oracle)
-	[`mysql:8.4.11-oraclelinux9`](#mysql8411-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.7`](#mysql97)
-	[`mysql:9.7-oracle`](#mysql97-oracle)
-	[`mysql:9.7-oraclelinux9`](#mysql97-oraclelinux9)
-	[`mysql:9.7.2`](#mysql972)
-	[`mysql:9.7.2-oracle`](#mysql972-oracle)
-	[`mysql:9.7.2-oraclelinux9`](#mysql972-oraclelinux9)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux9`](#mysqlinnovation-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:26`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26-oracle`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26-oraclelinux9`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7-oracle`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7-oraclelinux9`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7.0`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7.0` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7.0-oracle`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:26.7.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:26.7.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:26.7.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:26.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.11`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.11` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.11` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.11-oracle`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.11-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.11-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.11-oraclelinux9`

```console
$ docker pull mysql@sha256:6ea90827b1100f8f2ae306a539f86d2c264a26ed435a2a9f75551dd5c3aeb242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.11-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:80f4933e3835f9dc4d35a28ec500d7986cb4414e6c6821c5461239cb7beb8995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238984566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d132912e9d3c985237567595ec2aeae04936044eb1f9336e8e4da2326238b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:38:31 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:38:31 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:39:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:39:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49eff447cf4f73f6c00aa97c8c3e0daa3625d7ab9b58fee2ef881f3c0415590`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c4a59849a8b41f240db9009cda9555bfed34b2c2db35663c6bc24ce3f265f`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cf390878331a896b1ab0d7d1eed1e10f1e255780f9fd341dfecb379d1e0b4`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 6.2 MB (6198178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056f6ecb394359dfe87b0e746d4485e161f4f1c5bf140e498aa3a9097b2dff9`  
		Last Modified: Tue, 29 Sep 2026 18:40:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff557ec8ac737f139cdd330e275c3bfca9fdc671bb87583511831c91eaffe2f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8d0b814939dd4d78df05161b0e8a5b892c74d18ca6e2ced927ddac62f8baf3`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 51.6 MB (51629304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a129719b3ee49a44231e17b8892482a66070b0995808fe4793b7426799224f8`  
		Last Modified: Tue, 29 Sep 2026 18:40:18 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea066d40f8befa2086f23b9f7039c2868513a58bbf0d5be3d6abff9665ef5af6`  
		Last Modified: Tue, 29 Sep 2026 18:40:21 GMT  
		Size: 132.4 MB (132422522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be21a6c94a690459920512a340ac5fd40e4ee85c24e9b20e781d402456e824b`  
		Last Modified: Tue, 29 Sep 2026 18:40:19 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e806cb172700d49bc35ef862c11531c3f8a558543c36d36654ed466dd6589772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073d9310b2ac9aed83fd13db4b9a5413333ac4725df758b234aa856d87c31dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4347f9bd42d8830b100034268850b870d25ff8c1275d25f1b4cba4107cd0e0f7`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 15.7 MB (15711922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead2e45f6d29eb6c510dbdd03e2f51099a71aee3df3ff1c7935daeea73a270cd`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 33.3 KB (33313 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.11-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ca3f0494c0f1fc86eb45f5e4786a1bb9f64d2f85b562cc74a9595046f6519a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233697875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd43bad43e0de5959b98c4404e987046de21cd85b9e725849208db6539d3c2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 29 Sep 2026 18:10:25 GMT
ENV MYSQL_VERSION=8.4.11-1.el9
# Tue, 29 Sep 2026 18:10:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:11:05 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 29 Sep 2026 18:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aeb931cc3039e56560911f4a323fcc25ecb529b093fd4a0abdab3317785a00`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e0586d6a0ba960b00641d9514ef038956c92985b7f75916e2abcccea93374`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa8c3382dd8b109cb8ea91c2509ce7fe8e7ecb8e24a4f4feed746d6d714892`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e7d54e98ebeb74462b69bd562986e6a2d2d69c1376d88a5ccef9a85632cb7`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddcbf9098d2a4da10b4e38e4005483d63c3a2607dc0c465edd0f8499bb6cf3`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43d3bd420c9d0e5cbb03673c529f96bcda8ca7431c43d216df6a6b303f895b`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 49.9 MB (49853260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1b48c6cb3bbdedee58eda4df2640fd013544e8e4de7fb74088bbece803772`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6670c3ce31c07a24de10d876c13db97c3693f5d4562680d7e22e7606d06f9b`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 130.8 MB (130789544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e7994a8f23acf957878e4b31b4aef38e4654998ebfc5994ae8d194bc420c9`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.11-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:41f5cae6e15ccd51271780348a0a4e358bed42115665510f0bb7dc92888d0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d91a945666bbe12d8c4c7761b5bc76c428cd467dad34ded31a48245003ca6`

```dockerfile
```

-	Layers:
	-	`sha256:1e6475e65a4b94e6158d0b9bad8260d3f443280b276716d7b7add017d61e5847`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 15.7 MB (15710322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a02c958f8a03b7d5bc13e7537850621123f2a68cee81709a86271b44bd788`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

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

### `mysql:9` - unknown; unknown

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

### `mysql:9` - linux; arm64 variant v8

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

### `mysql:9` - unknown; unknown

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

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

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

### `mysql:9-oracle` - unknown; unknown

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

### `mysql:9-oracle` - linux; arm64 variant v8

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

### `mysql:9-oracle` - unknown; unknown

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

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

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

### `mysql:9-oraclelinux9` - unknown; unknown

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

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

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

### `mysql:9-oraclelinux9` - unknown; unknown

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

## `mysql:9.7`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7` - linux; amd64

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

### `mysql:9.7` - unknown; unknown

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

### `mysql:9.7` - linux; arm64 variant v8

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

### `mysql:9.7` - unknown; unknown

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

## `mysql:9.7-oracle`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oracle` - linux; amd64

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

### `mysql:9.7-oracle` - unknown; unknown

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

### `mysql:9.7-oracle` - linux; arm64 variant v8

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

### `mysql:9.7-oracle` - unknown; unknown

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

## `mysql:9.7-oraclelinux9`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oraclelinux9` - linux; amd64

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

### `mysql:9.7-oraclelinux9` - unknown; unknown

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

### `mysql:9.7-oraclelinux9` - linux; arm64 variant v8

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

### `mysql:9.7-oraclelinux9` - unknown; unknown

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

## `mysql:9.7.2`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.2` - linux; amd64

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

### `mysql:9.7.2` - unknown; unknown

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

### `mysql:9.7.2` - linux; arm64 variant v8

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

### `mysql:9.7.2` - unknown; unknown

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

## `mysql:9.7.2-oracle`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.2-oracle` - linux; amd64

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

### `mysql:9.7.2-oracle` - unknown; unknown

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

### `mysql:9.7.2-oracle` - linux; arm64 variant v8

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

### `mysql:9.7.2-oracle` - unknown; unknown

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

## `mysql:9.7.2-oraclelinux9`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.2-oraclelinux9` - linux; amd64

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

### `mysql:9.7.2-oraclelinux9` - unknown; unknown

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

### `mysql:9.7.2-oraclelinux9` - linux; arm64 variant v8

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

### `mysql:9.7.2-oraclelinux9` - unknown; unknown

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

## `mysql:innovation`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

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

### `mysql:lts` - unknown; unknown

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

### `mysql:lts` - linux; arm64 variant v8

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

### `mysql:lts` - unknown; unknown

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

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:e2bde46db6563855d7177adb5f0b57b9dc663f5a20927a90f4259d3312068497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

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

### `mysql:lts-oracle` - unknown; unknown

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

### `mysql:lts-oracle` - linux; arm64 variant v8

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

### `mysql:lts-oracle` - unknown; unknown

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

## `mysql:oracle`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:9d48c42f8341068f199116dfccb919b607c99765b5c61e549a548a43033471a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c6f1eff7bfe5726467a6ce9d267f620d4d579a7dbf78927c6434c60013ea1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cdf7ebf7281aafd4243ffcf36e3085dd9bb877679de4268b513c855c9fd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:37:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:38:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:38:15 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:38:15 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:38:51 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:39:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:39:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:39:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f04f054c4bac6f4bc96f5395f8abcc4383c1e5b3c35c72c12991b723a793f`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441bc0931d15874215898cac7d215ea86d37239ff6c3a2cd567769de29eb4d0`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ddc05b7f8ccbacf15e322b2e2c20e85bc9c51b2ad9560d38ab32c6d2d3e3c`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 6.2 MB (6198172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7464ce26b4d5d21112ae07241e2ac3db7aae2174dff46cd8b50850e9e1c62`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c451c026abd4a84acd29f8de3a8551ad2d035f5839543bd7518c0642574a9`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a9fb3841eddc933b02d25edfa451c656fbb99f56f755921b0bded9409d803`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 57.5 MB (57450739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95bd78f862044f644fedcdbe9bf7b50d7c491fea0a47a46fd4607da04163e6e`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37786bee9684677a195105e8c4dcdfd0a331aeeba5eeedfd885af3c49eb1597`  
		Last Modified: Tue, 29 Sep 2026 18:40:17 GMT  
		Size: 160.0 MB (159966210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdafce1e6fbfe8da913da066062f7d2233b15d1a69b909330a3dea88fcec5bd`  
		Last Modified: Tue, 29 Sep 2026 18:40:15 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5712b5c0e97ae1824c719289a2847c436776bab292fea076be530c6f01e7bb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99dfe7369666ff94e55dbc2836e4f7e571530139e4a1def4adf4ecbcd735170`

```dockerfile
```

-	Layers:
	-	`sha256:5a27b49a98e1e516cb47a426c9450370066305c4d1588ff1d883598112265ebf`  
		Last Modified: Tue, 29 Sep 2026 18:40:13 GMT  
		Size: 17.4 MB (17417411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c462e963975fd30d09f9271284f77e8bafe0106923da4dad58867c85c7bb9cbf`  
		Last Modified: Tue, 29 Sep 2026 18:40:12 GMT  
		Size: 35.3 KB (35298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec2c4a24f87843670231e047eadfdf8774020b798111f47fff1a4f4d07ed1af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268718973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca882e200191305a9d7dc4224bdc673a537601ed85d0a8b32b835f1372e01546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:09:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 29 Sep 2026 18:09:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:09:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:10:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 29 Sep 2026 18:10:17 GMT
ENV MYSQL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:10:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 29 Sep 2026 18:10:58 GMT
ENV MYSQL_SHELL_VERSION=26.7.0-1.el9
# Tue, 29 Sep 2026 18:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 18:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d9894db96213ee2b65ea22f9dd84836a36982cefb349350e687cd24e4218b`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4df3a8cfcf9c23035212bbc1bba958c239f02bd7ef891ae7f3bafb2902b46d`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68dfbe89267b292aa24caf0ed1019be6250e8a75dca03e5003ead6f49212b`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 5.8 MB (5822766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69696509d6e39fcd079caf742138e4529d860ae9c5c2af349685d5f8ab5acc71`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d634759c265f80fcb767c336c918a5b0fb05d7b10da809a0c6ed34c68f493602`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53517c6d10623a0dd2b20a588bd7bd4fccf27f9f45ab5c46370d1a21ce597025`  
		Last Modified: Tue, 29 Sep 2026 18:12:28 GMT  
		Size: 57.4 MB (57428283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12149f5e6f211b99ee7aa4ca44d548bb4d34a4f2b1ed6414e184669a3e6b4d`  
		Last Modified: Tue, 29 Sep 2026 18:12:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47764fc2beb63f8ac19589aeff62badfd6fc8125dfa1231efeb92f0becb3803`  
		Last Modified: Tue, 29 Sep 2026 18:12:30 GMT  
		Size: 158.2 MB (158235612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b18b73cf3460e276ce40119d8adbd840a8ccfa67275e6d3eb309a4545505b7`  
		Last Modified: Tue, 29 Sep 2026 18:12:27 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:359a9aa7165afc8a977010d665bbfe830ee6c500e3fa319bb82f87a3b1fdce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c206cedf5945f9436de19fa3a506dbb11f705e14231946828d759ead1a61702`

```dockerfile
```

-	Layers:
	-	`sha256:71b159782c13370d136d41707058e05ab63e4f814ae2ec2362c7924da95a45bd`  
		Last Modified: Tue, 29 Sep 2026 18:12:25 GMT  
		Size: 17.4 MB (17415884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6bfd1d58a35a8429c2aa3467b9a373152a4019f8f0614404eaef5f19ab2396`  
		Last Modified: Tue, 29 Sep 2026 18:12:24 GMT  
		Size: 35.6 KB (35638 bytes)  
		MIME: application/vnd.in-toto+json
