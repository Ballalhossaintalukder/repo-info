## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:a78fa55a4f270427fe69214ce558c40a826412c410be0ad58420206b38b1dd8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:lts-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:f2393c6a0fb81fc855494414a96fe34e32e1e6dd7f48cb160e57f7b7583f226e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166624346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b6d2d0c42a955681563eaa5b9257840680c9192e94fb17a61e4d9e67b021c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:57:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 00:57:55 GMT
ENV container oci
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:c94af32992a1c8563dae2c41b7cbae240915b79b6cafaf819ca86a1c2db6bfb3 in /      
# Mon, 28 Sep 2026 00:57:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:57:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:2ced94c8bcf5dc4ee352fe2c68f9c259358bc1a6ec5d2ce9613e5d90666c4655 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:57:55 GMT
COPY dir:2ced94c8bcf5dc4ee352fe2c68f9c259358bc1a6ec5d2ce9613e5d90666c4655 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:57:55 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:57:32Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T00:57:32Z" "architecture"="x86_64" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T00:57:32Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:55:53 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 29 Sep 2026 17:55:55 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:55:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 17:55:59 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 17:55:59 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 29 Sep 2026 17:55:59 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 29 Sep 2026 17:55:59 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 29 Sep 2026 17:55:59 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 29 Sep 2026 17:55:59 GMT
ARG MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:55:59 GMT
ENV MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:56:21 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 29 Sep 2026 17:56:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 17:56:21 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Sep 2026 17:56:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 29 Sep 2026 17:56:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:56:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:56:21 GMT
USER mysql
# Tue, 29 Sep 2026 17:56:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 29 Sep 2026 17:56:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a34145e205c19dadb74ed940321031a946571a492b3cf835b60f57003df2bdee`  
		Last Modified: Mon, 28 Sep 2026 02:11:46 GMT  
		Size: 34.9 MB (34929005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb096096ae72fcd4b135ca0bb6957b77bc31dab0b7e7ceb00ed11e27d2c80bd6`  
		Last Modified: Tue, 29 Sep 2026 17:56:42 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a40ef95981cdf6ff89ef96722c4e3e39d18be0c851ccaad784590d8cad864a`  
		Last Modified: Tue, 29 Sep 2026 17:56:42 GMT  
		Size: 2.3 MB (2274333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d8f4b645755622d17b1fda9a534ef22d6651128a12910a2cc8fdf6c52ab4c`  
		Last Modified: Tue, 29 Sep 2026 17:56:43 GMT  
		Size: 10.1 MB (10136096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf887bf79088f3d32dac6631758d31abaa1899a0686ec133d23fe9bb4d5756e6`  
		Last Modified: Tue, 29 Sep 2026 17:56:42 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b4dd4ba7aa4f1ac407b959b6530d300d57f1433d21454b687dcde55b707c49`  
		Last Modified: Tue, 29 Sep 2026 17:56:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5226b96f999f7bc14b76bb18f0458904a549fb15ea599ea3b155e9399b213c`  
		Last Modified: Tue, 29 Sep 2026 17:56:46 GMT  
		Size: 119.3 MB (119266882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7076d5be8def21bde6fc0712ed7e00ccbc20561fe2274ee2c2e236f00fc5cb8a`  
		Last Modified: Tue, 29 Sep 2026 17:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec4f0f4a770b303a944afa7f4b67c89a69829382e3999d22edeaac59ea2a101`  
		Last Modified: Tue, 29 Sep 2026 17:56:44 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c330775f06b90edd87f6bdac08751cce5c79ea5701cc5e63288561a32c1b4f09`  
		Last Modified: Tue, 29 Sep 2026 17:56:44 GMT  
		Size: 8.5 KB (8491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:89d5d5743bedc4850a90afd4ce7ab408446dc35272f27e4033e212af58d860e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc84956b7ee8f47233c6a86057bf1ab9e5b7ab912b81d9a76b8d35df0e233de5`

```dockerfile
```

-	Layers:
	-	`sha256:e5b7616e787a91b82485e781e8762d8fe24c4c6db6dfa1ca578db0c5f4e26fbb`  
		Last Modified: Tue, 29 Sep 2026 17:56:43 GMT  
		Size: 4.9 MB (4928098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a50c7763abbd32559a2f6a63a4cf96f9ef51376688098e09fe220843d3d6c86`  
		Last Modified: Tue, 29 Sep 2026 17:56:42 GMT  
		Size: 34.6 KB (34568 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7679d771534104bc7ccfbe55c7fe3ab75492cc78ab8d10d9a93d5d1c4aab307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161259858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff95b5abf6de6d7e5e7d65835784736617455b84ea58ed18e2fa07d89690c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:00:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:00:40 GMT
ENV container oci
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:ab0c5d24ca1747829dc1e0e979790e14bee66df400e8e4d271a15d552af407bf in /      
# Mon, 28 Sep 2026 01:00:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:00:41 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:7aacb9dad5ed908942374b1668501c386999af28176419b212897b761c97da4e in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:00:41 GMT
COPY dir:7aacb9dad5ed908942374b1668501c386999af28176419b212897b761c97da4e in /root/buildinfo/      
# Mon, 28 Sep 2026 01:00:41 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:00:17Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:00:17Z" "architecture"="aarch64" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:00:17Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:55:15 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 29 Sep 2026 17:55:17 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:55:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 17:55:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 17:55:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 29 Sep 2026 17:55:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 29 Sep 2026 17:55:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 29 Sep 2026 17:55:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 29 Sep 2026 17:55:21 GMT
ARG MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:55:21 GMT
ENV MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:55:44 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 29 Sep 2026 17:55:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 17:55:44 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Sep 2026 17:55:44 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 29 Sep 2026 17:55:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:55:44 GMT
USER mysql
# Tue, 29 Sep 2026 17:55:44 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 29 Sep 2026 17:55:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:842ae2bcf67a61456b432d1f1a94bcb7d69f0613459a34bb97404ab26399ad66`  
		Last Modified: Mon, 28 Sep 2026 02:12:22 GMT  
		Size: 33.1 MB (33124832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc033ee036e57c33d7fb66ada81ed0701ac69daaca0f6d5919bcca20828a4ac`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f789c1ad09dd42d92378195312baa1913f4230cbf70c783910c1af957431feb4`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 2.3 MB (2273501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd978c9283fe3f139e063657778c15c47d18f31bb00d2c5efbd1f8fdc5357b7`  
		Last Modified: Tue, 29 Sep 2026 17:56:06 GMT  
		Size: 9.9 MB (9931629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2565366676a778d82cd3e3abc064fd7cb1eaa42a1350ba20498161b1a1488d`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ee20a865477edd3e3a8c5ed3ad5ee28bb8b9783e73597bcb67b287cc9f983`  
		Last Modified: Tue, 29 Sep 2026 17:56:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99f6aeb6d20a0e0d4d79b08496c93046be820f6aaa2a1591a973399e7e717c0`  
		Last Modified: Tue, 29 Sep 2026 17:56:09 GMT  
		Size: 115.9 MB (115911861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7f594dc3440c0d0862aa92861453490220c8aa2c8085bb20e7ba76d8e5d8d`  
		Last Modified: Tue, 29 Sep 2026 17:56:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817efeef191386df3afea19f4403a9c3bf664747d1e969f064a076dce0a7384e`  
		Last Modified: Tue, 29 Sep 2026 17:56:07 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599287038fe248a11c9a53d22ef784832b7e1a4ef92fd8e936f75555bc018935`  
		Last Modified: Tue, 29 Sep 2026 17:56:08 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:32e63f527c8036a07402fc2ed10371553609ad94d619ecfb16ff4721fc19b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4948263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bb74eca0c88cfb4dd7621b0953da39a3029e82b6a0242de0654be45f113a42`

```dockerfile
```

-	Layers:
	-	`sha256:71f321454c6a3a48d0006e5838ef25ab7720600f4a328ad3317b8a308ddad613`  
		Last Modified: Tue, 29 Sep 2026 17:56:06 GMT  
		Size: 4.9 MB (4913497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5385e6dcb74e31d0018e1a96b890f2d3915c4a27241786b57aa5e06e52851c`  
		Last Modified: Tue, 29 Sep 2026 17:56:05 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8ba37a065556d2fe512f1fdd6ac8bb549970bca26c453741b3bb52f9d17e4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176804440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0cd5c4ba0a7be2e4be7f5f420e8897872a367c62c42190a3354d353debade9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:00:57 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:00:57 GMT
ENV container oci
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:15640a8bb09c7ee6c64cb6dd35f25cbd39908e3326f3c8d28382a9522b129d54 in /      
# Mon, 28 Sep 2026 01:00:58 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:00:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:9e1e6cef5a4091efaa305feea8bbd3feed428affc645bb8ad805c85f218842d6 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:00:58 GMT
COPY dir:9e1e6cef5a4091efaa305feea8bbd3feed428affc645bb8ad805c85f218842d6 in /root/buildinfo/      
# Mon, 28 Sep 2026 01:00:58 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:00:35Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:00:35Z" "architecture"="ppc64le" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:00:35Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 18:16:47 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 29 Sep 2026 18:16:51 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:16:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 18:16:57 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 18:16:58 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 29 Sep 2026 18:19:15 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 29 Sep 2026 18:19:15 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 29 Sep 2026 18:19:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 29 Sep 2026 18:19:15 GMT
ARG MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 18:19:15 GMT
ENV MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 18:20:03 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 29 Sep 2026 18:20:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 18:20:04 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Sep 2026 18:20:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 29 Sep 2026 18:20:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 18:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 18:20:05 GMT
USER mysql
# Tue, 29 Sep 2026 18:20:05 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 29 Sep 2026 18:20:05 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:869c2426a34dac9af44481336945ab2a560ef9817565e34bc71e3f7d2128897b`  
		Last Modified: Mon, 28 Sep 2026 06:28:56 GMT  
		Size: 39.1 MB (39116127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a290b428886319ddd6c90e881c29f005ab0d8b11e9edffd89aec0abc9dc8d`  
		Last Modified: Tue, 29 Sep 2026 18:18:51 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dab0a580b87f8ecc5eb5d52d5f25396a0ef71b75d851588079014fbb936baa`  
		Last Modified: Tue, 29 Sep 2026 18:18:51 GMT  
		Size: 2.3 MB (2299805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b05c0f150ee4d59af4ebb22876648f1afcf6ffa026073296b810186acb19ed`  
		Last Modified: Tue, 29 Sep 2026 18:18:51 GMT  
		Size: 10.6 MB (10605856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935bf87d490af75efb6163628b823ae95f8a33a47b8b8c885f89383a6fe3b2c1`  
		Last Modified: Tue, 29 Sep 2026 18:18:51 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ae0c23d2a659881e839c431ba16a0ab73f4081bd574203e20a72984783212c`  
		Last Modified: Tue, 29 Sep 2026 18:20:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc76fa027ee85ed9a962450dd268466603924799cff779d372b994a7d8a2cb`  
		Last Modified: Tue, 29 Sep 2026 18:21:00 GMT  
		Size: 124.8 MB (124764613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009e847c7bf2b8fb2cf87141fb407f91c4ff0104ff2b5cb363b322053b3558b1`  
		Last Modified: Tue, 29 Sep 2026 18:20:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c581c1ede9c3f1133292d2782b1b57aad67fbff14f8b621ed0168a7e0f3e96`  
		Last Modified: Tue, 29 Sep 2026 18:20:57 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f1388b693749e99c7dddbb28a525add93584470b447382cbe4d7bb161c5fc`  
		Last Modified: Tue, 29 Sep 2026 18:20:58 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:026732b4c77260258583945df6ec31bf95a37dfffd28a5a4733f59537596e1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56dd2470a4e25ae659fca8a5a81d0afe6d9b44389692914fb57ba4754d7c057`

```dockerfile
```

-	Layers:
	-	`sha256:770dd2e873db6b5a40b136feaa29aa9537dc683875ff4a2eb9debc7c52f27ecd`  
		Last Modified: Tue, 29 Sep 2026 18:20:57 GMT  
		Size: 4.9 MB (4902595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c774ca492f3b3f67bea4113c04ddfda79bdd4aec7a2c5aa7844a353394a7ad7`  
		Last Modified: Tue, 29 Sep 2026 18:20:57 GMT  
		Size: 34.6 KB (34638 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:b07ea094589fb93b9c4f84a2b1f8ba61215a1652fd8975f1e08b019fbdf5b169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171625200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43000df73d45ab1fa8476f73bb14ddcd3e54da711df61a7bf2583c99a76ca3af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 28 Sep 2026 01:27:23 GMT
ENV container oci
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:627ae3085e2bde6038f6671100fa887f782801ff3b2f6b6d06098a5bbfa348e3 in /      
# Mon, 28 Sep 2026 01:27:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 01:27:23 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:a5fd2ac24b6a4404a3524023e09e42dbddc24c5636dee74d1cd2462add8a5608 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 01:27:23 GMT
COPY dir:a5fd2ac24b6a4404a3524023e09e42dbddc24c5636dee74d1cd2462add8a5608 in /root/buildinfo/      
# Mon, 28 Sep 2026 01:27:23 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T01:26:09Z" "org.opencontainers.image.revision"="7f58b38be2088aa773281b773dc5491ca3cf688a" "build-date"="2026-09-28T01:26:09Z" "architecture"="s390x" "vcs-ref"="7f58b38be2088aa773281b773dc5491ca3cf688a" "vcs-type"="git" "release"="1790556942"org.opencontainers.image.created=2026-09-28T01:26:09Z,org.opencontainers.image.revision=7f58b38be2088aa773281b773dc5491ca3cf688a
# Tue, 29 Sep 2026 17:53:53 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 29 Sep 2026 17:53:55 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 17:53:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 29 Sep 2026 17:53:58 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Sep 2026 17:53:58 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 29 Sep 2026 17:56:22 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 29 Sep 2026 17:56:22 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 29 Sep 2026 17:56:22 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 29 Sep 2026 17:56:22 GMT
ARG MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:56:22 GMT
ENV MARIADB_VERSION=12.3.3
# Tue, 29 Sep 2026 17:56:40 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 29 Sep 2026 17:56:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Sep 2026 17:56:40 GMT
# ARGS: MARIADB_VERSION=12.3.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Sep 2026 17:56:40 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 29 Sep 2026 17:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Sep 2026 17:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:56:40 GMT
USER mysql
# Tue, 29 Sep 2026 17:56:40 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 29 Sep 2026 17:56:40 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3e51340b5abee43447a0b1bfecbe6d76485a0883aea31b7aec7aa8f604d00e2f`  
		Last Modified: Mon, 28 Sep 2026 06:28:51 GMT  
		Size: 34.8 MB (34837868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954744d8dda01d6504f0483310306571bb8537a802dce00a3fd0b1cea924806e`  
		Last Modified: Tue, 29 Sep 2026 17:55:12 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1775a721629263e2ada9709d945cac68e0f6b5a6b4390cc030f115925a5ab4ce`  
		Last Modified: Tue, 29 Sep 2026 17:55:12 GMT  
		Size: 2.3 MB (2279969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a4463610bdbb50e2040be113856eefe9ee2acccbee31cb2d49324636af921a`  
		Last Modified: Tue, 29 Sep 2026 17:55:12 GMT  
		Size: 10.3 MB (10270275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b023aacbe00b1306c86663853b542bd6fb56bda2afdc6e2b17dd6c3ba9753a1d`  
		Last Modified: Tue, 29 Sep 2026 17:55:12 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2b971957b6fa602b44bcf2bcc1941b37d43d0ee1ffa269338afe3a1e3bfd07`  
		Last Modified: Tue, 29 Sep 2026 17:57:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db834d0eb49c6743f5dc9582fa82c0232e1fb558325f9aa608412688757a79b6`  
		Last Modified: Tue, 29 Sep 2026 17:57:20 GMT  
		Size: 124.2 MB (124219057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecdb9643a11fb8483e1edebd678000478d4690cb73a0869b8efb1241b1ccef5`  
		Last Modified: Tue, 29 Sep 2026 17:57:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e13cbe3308e85d72e92777b44992fb5909a864e78842d2edf5e12955a9687f5`  
		Last Modified: Tue, 29 Sep 2026 17:57:17 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180b70d9482ebd9626f36a2c4a19ceb2e7801a46de860ad0ead56bc1758e8b4e`  
		Last Modified: Tue, 29 Sep 2026 17:57:18 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:d3eaddc7bd5208a8e22e17160d4f3acfb9b21986131d0f8d198a67db54e063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9af3020e15ca6a0e2c3dbee139bc94c66e596d6ca33986538f41ebee9a5ebb`

```dockerfile
```

-	Layers:
	-	`sha256:25a196ce77b3a651c2b70a06e5a2034f8f05e06a52f9117b68ef6deffd26acf2`  
		Last Modified: Tue, 29 Sep 2026 17:57:18 GMT  
		Size: 4.9 MB (4906504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9461b642ed1fdfd9ddb4199d17c8adf3e494d74a9e31482493325d2fec1def55`  
		Last Modified: Tue, 29 Sep 2026 17:57:17 GMT  
		Size: 33.8 KB (33769 bytes)  
		MIME: application/vnd.in-toto+json
