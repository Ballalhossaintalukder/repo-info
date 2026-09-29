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
