<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.46-37`](#percona8046-37)
-	[`percona:8.0.46-37-centos`](#percona8046-37-centos)
-	[`percona:9`](#percona9)
-	[`percona:9.7`](#percona97)
-	[`percona:9.7.2-2`](#percona972-2)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.46-37`](#perconaps-8046-37)
-	[`percona:ps-9`](#perconaps-9)
-	[`percona:ps-9.7`](#perconaps-97)
-	[`percona:ps-9.7.2-2`](#perconaps-972-2)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.29`](#perconapsmdb-6029)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.43`](#perconapsmdb-7043)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.32`](#perconapsmdb-8032)

## `percona:8`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.46-37`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.46-37` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.46-37` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.46-37-centos`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.46-37-centos` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.46-37-centos` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:9`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:9` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:9` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:9.7`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:9.7` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:9.7` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:9.7.2-2`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:9.7.2-2` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:9.7.2-2` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.46-37`

```console
$ docker pull percona@sha256:94458c42d5a67e6142571d529c8aed8ebfdac0589c8fe6da597ef81143a0d874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.46-37` - linux; amd64

```console
$ docker pull percona@sha256:02e28b7d8d49b50191da3ce0a297557991106b3c070c1db7283ae26a494c41fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411526600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7db6d5fd7db55013b29003e8e79031ad9245caac6245beb676e086fd23906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:00 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_VERSION=8.0.46-37.1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_PERCONA_VERSION=8.0.46-37.1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:52:00 GMT
ENV PS_TELEMETRY_VERSION=8.0.46-37-1
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:00 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:52:00 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:00 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:44 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:45 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:45 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b914a26782df33579d56e28c0a5113aaa55bf0c008ddc330aa11852dc2263481`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e8e20d37e24e7c1f3c661e991999a4800a496958b685c71216254d2de1736`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 9.4 MB (9361056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d152b51b0a4f3dbac5629cefe7b04195ff532d7307d84fa7eb292b9add2a1`  
		Last Modified: Tue, 29 Sep 2026 17:53:34 GMT  
		Size: 361.4 MB (361417829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6967720c7ba77c26a300df599c412ac4a019d1ed14eeccc0cf2f97360c31d1`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9addc42c2962466ca112e1cd01982d4a5a32d80004b7cdcef2eeec3792ae5f`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70573281bf470459f86eeff3a10962ba8b5766e33effb0f822dda3f4d509d269`  
		Last Modified: Tue, 29 Sep 2026 17:53:28 GMT  
		Size: 3.3 KB (3283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.46-37` - unknown; unknown

```console
$ docker pull percona@sha256:3fd83fd2a3e9e20e50c31a6ef6a95737b83b6f086ddd551774f0e152c40bdd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea1f29e1427b8338682db7d2783b135dbeed68746c954ccfe822837cd05f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4caa2a4e080ff7ca52572cdfdc50f57cec559bdb1c0c9122440a96660fe818`  
		Last Modified: Tue, 29 Sep 2026 17:53:27 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-9`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-9` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-9` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-9.7`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-9.7` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-9.7` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-9.7.2-2`

```console
$ docker pull percona@sha256:07ef38ff0e6a42b601ed3bca49ce4391f2f78a60867f5f5918b0948c60d06897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-9.7.2-2` - linux; amd64

```console
$ docker pull percona@sha256:f8f2711047ebff69fa4b792dd2136e0f94c962ee3fb5d64553a7d69c525da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452397734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168270b4c1a83609002eec1ef2e3a11474a7277ab249b4485179304ab3fe46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:51:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:51:23 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_VERSION=9.7.2-2.1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_PERCONA_VERSION=9.7.2-2.1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV FULL_MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_REPO=testing
# Tue, 29 Sep 2026 17:51:23 GMT
ENV PS_TELEMETRY_VERSION=9.7.2-2-1
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:51:23 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 29 Sep 2026 17:51:23 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:51:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:51:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-97-lts ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 29 Sep 2026 17:52:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         curl-minimal         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 29 Sep 2026 17:52:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:04 GMT
USER mysql
# Tue, 29 Sep 2026 17:52:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 29 Sep 2026 17:52:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608403b666ef9df028885735a5dca2f89c83232d9268cc1cbc414eb55b75e5bb`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f0ed69bbeebc7e1a846d1a44a0fe9ebb088e2957835870a16f816b42e5471b`  
		Last Modified: Tue, 29 Sep 2026 17:52:48 GMT  
		Size: 9.4 MB (9361046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08ecd0dc274754f02c9d9618c598fc5d88278da3266e7152db5ec1a5a6aee9`  
		Last Modified: Tue, 29 Sep 2026 17:52:55 GMT  
		Size: 402.3 MB (402288973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60566acdf7f6a52e9b568f7032e5bedabf6f1364ab9477ec68cc3ac7ffd70ab9`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c7a19044e4e8d3e1c95a5e1c334c9adc269466edfdbb1df31f06be92c78c6`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d65325605e66e112abe737eee0c3d7a4c61dff404edaa37b7c9abe1684055`  
		Last Modified: Tue, 29 Sep 2026 17:52:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-9.7.2-2` - unknown; unknown

```console
$ docker pull percona@sha256:fd26cc5ba15dada2f823603b992e29b5f08a855fc92ab8a71dc26232175f1a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd17679e104662b1c1299fe78baf0308a6d065dee1513ee3b728107809d6a32`

```dockerfile
```

-	Layers:
	-	`sha256:f1e15339f708bd7a4b85a5edffd9c0d2218ad6b8164ae9a65a899d73bb9583a2`  
		Last Modified: Tue, 29 Sep 2026 17:52:47 GMT  
		Size: 30.0 KB (29970 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:60e5e9653bfb284e1599e2784743438fcaac0d8340c6d50ba0a27379f9fa72a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:8ff0c40c3c28ad757527b9a62dbc49f520633fd2b8427ad95ad01fdb618b4414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279483316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530419ac27a6b45f4e1e42dcbf2b95ebde31c86e971f63519364557e3120d75f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 17:52:18 GMT
ENV PSMDB_VERSION=6.0.29-23
# Tue, 29 Sep 2026 17:52:18 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:18 GMT
ENV FULL_PERCONA_VERSION=6.0.29-23.el9
# Tue, 29 Sep 2026 17:52:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 17:52:18 GMT
ENV PSMDB_REPO=release
# Tue, 29 Sep 2026 17:52:18 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:18 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:18 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         libcap         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 17:52:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 17:52:42 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 17:52:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:43 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:43 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 17:52:43 GMT
USER 1001
# Tue, 29 Sep 2026 17:52:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f023522be7cd2e4dce63334169698eea43179b72c09b811ecbda6267205a4435`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 9.0 MB (8982628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c15946515005d5c685703af9ab368127906670218e499a94aa3fc396d1096`  
		Last Modified: Tue, 29 Sep 2026 17:53:15 GMT  
		Size: 228.8 MB (228809768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a8007ffdcdde7b906d5e22c9fa3e5484a1a5d6918e31879e56e5c868fce604`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d262623236be718d0b2c83f700d057dc477a04cbcbdbb550779c3b9d99cb2a`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1732b16002e0e755b9dfca50249876fd18181d7fd797a9a325adb5fcf32f45a`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3634742605bfb301a32c764e0821f0d8f244d6e145c212bc41c9d967c2e36c`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23062edf25a7e9a18e232ca77b5a7d883416517581fb48011c41f5e5e752ccd8`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22425dd43fb5f42ac148a090209744fe6d0eeba6a357ac42946c0068a5586c25`  
		Last Modified: Tue, 29 Sep 2026 17:53:13 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cc9fb902a675bf3a0871cedde7b25e71c2ce367524c926556f99c20e4c7922`  
		Last Modified: Tue, 29 Sep 2026 17:53:13 GMT  
		Size: 5.0 KB (4969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:2fa5d06c26d2b413e8458124fb39c33f400ef7162284adca1055e6498cd55066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb769bc0016936302468f00b78bf7bf3a19ca41757d75f30e91f065d71e1bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1c840dc442e4fb73b0bef321a2bbdf0f7f3d576115de03d95590c0cb5a287d16`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 32.9 KB (32939 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.29`

```console
$ docker pull percona@sha256:60e5e9653bfb284e1599e2784743438fcaac0d8340c6d50ba0a27379f9fa72a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.29` - linux; amd64

```console
$ docker pull percona@sha256:8ff0c40c3c28ad757527b9a62dbc49f520633fd2b8427ad95ad01fdb618b4414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279483316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530419ac27a6b45f4e1e42dcbf2b95ebde31c86e971f63519364557e3120d75f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 17:52:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 17:52:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 17:52:18 GMT
ENV PSMDB_VERSION=6.0.29-23
# Tue, 29 Sep 2026 17:52:18 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 17:52:18 GMT
ENV FULL_PERCONA_VERSION=6.0.29-23.el9
# Tue, 29 Sep 2026 17:52:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 17:52:18 GMT
ENV PSMDB_REPO=release
# Tue, 29 Sep 2026 17:52:18 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 17:52:18 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 17:52:18 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         libcap         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 17:52:41 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 17:52:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 17:52:42 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 17:52:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 17:52:43 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 17:52:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 17:52:43 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 17:52:43 GMT
USER 1001
# Tue, 29 Sep 2026 17:52:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f023522be7cd2e4dce63334169698eea43179b72c09b811ecbda6267205a4435`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 9.0 MB (8982628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c15946515005d5c685703af9ab368127906670218e499a94aa3fc396d1096`  
		Last Modified: Tue, 29 Sep 2026 17:53:15 GMT  
		Size: 228.8 MB (228809768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a8007ffdcdde7b906d5e22c9fa3e5484a1a5d6918e31879e56e5c868fce604`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d262623236be718d0b2c83f700d057dc477a04cbcbdbb550779c3b9d99cb2a`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1732b16002e0e755b9dfca50249876fd18181d7fd797a9a325adb5fcf32f45a`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3634742605bfb301a32c764e0821f0d8f244d6e145c212bc41c9d967c2e36c`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23062edf25a7e9a18e232ca77b5a7d883416517581fb48011c41f5e5e752ccd8`  
		Last Modified: Tue, 29 Sep 2026 17:53:12 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22425dd43fb5f42ac148a090209744fe6d0eeba6a357ac42946c0068a5586c25`  
		Last Modified: Tue, 29 Sep 2026 17:53:13 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cc9fb902a675bf3a0871cedde7b25e71c2ce367524c926556f99c20e4c7922`  
		Last Modified: Tue, 29 Sep 2026 17:53:13 GMT  
		Size: 5.0 KB (4969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.29` - unknown; unknown

```console
$ docker pull percona@sha256:2fa5d06c26d2b413e8458124fb39c33f400ef7162284adca1055e6498cd55066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb769bc0016936302468f00b78bf7bf3a19ca41757d75f30e91f065d71e1bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1c840dc442e4fb73b0bef321a2bbdf0f7f3d576115de03d95590c0cb5a287d16`  
		Last Modified: Tue, 29 Sep 2026 17:53:11 GMT  
		Size: 32.9 KB (32939 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:e0fa7959f094d6456dfc10a338c44bf75967e21a38e5e96919c052873a055571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:bc30efed4a7d0184ec5b76ab8ad7e13990a59bdc11ec7b0f4eecc2d7003ddb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304405516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69edf8fc92d30f4b6bb746aec9919f4a9b8c4a47a325e2ac4a15e924cece0790`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 18:05:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 18:05:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 18:05:52 GMT
ENV PSMDB_VERSION=7.0.43-23
# Tue, 29 Sep 2026 18:05:52 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 18:05:52 GMT
ENV FULL_PERCONA_VERSION=7.0.43-23.el9
# Tue, 29 Sep 2026 18:05:52 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 18:05:52 GMT
ENV PSMDB_REPO=release
# Tue, 29 Sep 2026 18:05:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 18:05:52 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 18:05:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 18:06:14 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 18:06:14 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 18:06:14 GMT
USER 1001
# Tue, 29 Sep 2026 18:06:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301afa58db84a92fdf7b6d0601c5d827eb6aed2019bd5a35e88b643c7c9a3cae`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 9.0 MB (8978486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0199e55e8810ce24111b161dbca0287b17b7743478001638efa53377362f9677`  
		Last Modified: Tue, 29 Sep 2026 18:06:45 GMT  
		Size: 253.7 MB (253736107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f0e146142ae8a0134cacaa27734b93377bd86406d3137342a2d100e8a56238`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b04e519fe0f239cc8a97e8ea16a6a609fce0471ddc1c1909cbce6e5e24be4b7`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24bea254bd4ee67aa2390d7ecc6d3c02ef03fb11da96338770c6631de15b70`  
		Last Modified: Tue, 29 Sep 2026 18:06:41 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde25d1ba8789a1659ddb816ae982b1d7be99a1e743cdcf41446eb4f295ccb7d`  
		Last Modified: Tue, 29 Sep 2026 18:06:41 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf457099b07362361f57e687e00768e79e47e83d91159c6d5fdec0d39d703195`  
		Last Modified: Tue, 29 Sep 2026 18:06:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c413ac7a8e23e3ec0da1c49090b641be4e7fee9422ce86ff2a1cd3af0d1a9fb`  
		Last Modified: Tue, 29 Sep 2026 18:06:42 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59060a7509b166d6506ce992332be84ae2f02633cf293292fb2be44fa37a7568`  
		Last Modified: Tue, 29 Sep 2026 18:06:43 GMT  
		Size: 5.0 KB (4970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:471fb1e426b6ee81b3cf773fad11549af0c31ee500baae62c24a0d03a4d85a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce763ced53b0c54a929d67d9f4bb50436dd0638e732ca161e8ab7df4a3d132`

```dockerfile
```

-	Layers:
	-	`sha256:7643afeb256b9545872eafa12c1be9f33042d1188c7ee7106dd7c2008c09748c`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 32.4 KB (32369 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.43`

```console
$ docker pull percona@sha256:e0fa7959f094d6456dfc10a338c44bf75967e21a38e5e96919c052873a055571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.43` - linux; amd64

```console
$ docker pull percona@sha256:bc30efed4a7d0184ec5b76ab8ad7e13990a59bdc11ec7b0f4eecc2d7003ddb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304405516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69edf8fc92d30f4b6bb746aec9919f4a9b8c4a47a325e2ac4a15e924cece0790`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 18:05:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 18:05:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 18:05:52 GMT
ENV PSMDB_VERSION=7.0.43-23
# Tue, 29 Sep 2026 18:05:52 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 18:05:52 GMT
ENV FULL_PERCONA_VERSION=7.0.43-23.el9
# Tue, 29 Sep 2026 18:05:52 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 18:05:52 GMT
ENV PSMDB_REPO=release
# Tue, 29 Sep 2026 18:05:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 18:05:52 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 18:05:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 18:06:12 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 18:06:14 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 18:06:14 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 18:06:14 GMT
USER 1001
# Tue, 29 Sep 2026 18:06:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301afa58db84a92fdf7b6d0601c5d827eb6aed2019bd5a35e88b643c7c9a3cae`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 9.0 MB (8978486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0199e55e8810ce24111b161dbca0287b17b7743478001638efa53377362f9677`  
		Last Modified: Tue, 29 Sep 2026 18:06:45 GMT  
		Size: 253.7 MB (253736107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f0e146142ae8a0134cacaa27734b93377bd86406d3137342a2d100e8a56238`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b04e519fe0f239cc8a97e8ea16a6a609fce0471ddc1c1909cbce6e5e24be4b7`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24bea254bd4ee67aa2390d7ecc6d3c02ef03fb11da96338770c6631de15b70`  
		Last Modified: Tue, 29 Sep 2026 18:06:41 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde25d1ba8789a1659ddb816ae982b1d7be99a1e743cdcf41446eb4f295ccb7d`  
		Last Modified: Tue, 29 Sep 2026 18:06:41 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf457099b07362361f57e687e00768e79e47e83d91159c6d5fdec0d39d703195`  
		Last Modified: Tue, 29 Sep 2026 18:06:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c413ac7a8e23e3ec0da1c49090b641be4e7fee9422ce86ff2a1cd3af0d1a9fb`  
		Last Modified: Tue, 29 Sep 2026 18:06:42 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59060a7509b166d6506ce992332be84ae2f02633cf293292fb2be44fa37a7568`  
		Last Modified: Tue, 29 Sep 2026 18:06:43 GMT  
		Size: 5.0 KB (4970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.43` - unknown; unknown

```console
$ docker pull percona@sha256:471fb1e426b6ee81b3cf773fad11549af0c31ee500baae62c24a0d03a4d85a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce763ced53b0c54a929d67d9f4bb50436dd0638e732ca161e8ab7df4a3d132`

```dockerfile
```

-	Layers:
	-	`sha256:7643afeb256b9545872eafa12c1be9f33042d1188c7ee7106dd7c2008c09748c`  
		Last Modified: Tue, 29 Sep 2026 18:06:40 GMT  
		Size: 32.4 KB (32369 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:42693981b4683499250d2dcdf0e5dfb8b98870640b25ea46d3945a8d1bb240f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:0a839a142798623496a70a4326b4b43f7b1a48480d5165caab03c02d62f9f120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324802193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e7ffd50724cae885e08c8e11c9b6d13c579f859bb61bc007ae4a5e49176d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 18:05:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 18:05:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 18:05:57 GMT
ENV PSMDB_VERSION=8.0.32-14
# Tue, 29 Sep 2026 18:05:57 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 18:05:57 GMT
ENV FULL_PERCONA_VERSION=8.0.32-14.el9
# Tue, 29 Sep 2026 18:05:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 18:05:57 GMT
ENV PSMDB_REPO=testing
# Tue, 29 Sep 2026 18:05:57 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 29 Sep 2026 18:05:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 18:05:57 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 18:05:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 18:06:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 18:06:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 18:06:19 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 18:06:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 18:06:20 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 18:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 18:06:20 GMT
USER 1001
# Tue, 29 Sep 2026 18:06:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a606c5b273ec07c4bf63682435d50f4fc5706af9298e3b9dbfecf16865ab196`  
		Last Modified: Tue, 29 Sep 2026 18:06:51 GMT  
		Size: 9.0 MB (8978505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddc296d8e079fc40acc45fc738f888eb02a87c1a6af2ffefae63752f3b6cd39`  
		Last Modified: Tue, 29 Sep 2026 18:06:59 GMT  
		Size: 274.1 MB (274132766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625faddbfdb30746181df907ac234d156cf25b7a2e33d4ecea577cf7f0e26747`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86daa1153f8b8612c4b6d3e7d38d8dd16ca2976480b426e51e343cab9a63f224`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be46994a59055669830f8a521137d52bd98cdc3be2ed8550b6c8601f4541b8`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6317381135f1e02e61dd939cb4077d0debbcc9ab79b8907e2f9e7c5aa31a75`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01836495fb18631ff610f5c3e77d5420153ed5027e359f05b5b440d4b194bf`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56798cb3c6b041ca06f6ea40847ee3d123200d03a4df10fe2b90de9d7320718b`  
		Last Modified: Tue, 29 Sep 2026 18:06:53 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3a8b7b018d14b0ed9209d6dbf259bb2cde60879d946e8779b5e8c9897517`  
		Last Modified: Tue, 29 Sep 2026 18:06:53 GMT  
		Size: 5.0 KB (4966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:c0fd9c725d2fde27c3f8b4adce42bd912b21fe9bab7beec3cddbaac3d25c385b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fb5b85a32657101ca9054c263f72bff04eaab17ab1a2c18651e517ec3fc8e7`

```dockerfile
```

-	Layers:
	-	`sha256:943cf19c25a153e178afb6d3870a90a923d313a2761b4ee2f5c794ceece02e92`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 32.7 KB (32673 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.32`

```console
$ docker pull percona@sha256:42693981b4683499250d2dcdf0e5dfb8b98870640b25ea46d3945a8d1bb240f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.32` - linux; amd64

```console
$ docker pull percona@sha256:0a839a142798623496a70a4326b4b43f7b1a48480d5165caab03c02d62f9f120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324802193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e7ffd50724cae885e08c8e11c9b6d13c579f859bb61bc007ae4a5e49176d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Sep 2026 00:38:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Sep 2026 00:38:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Sep 2026 00:38:29 GMT
ENV container oci
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:b4a6c7715927d81d10419af4e2efeb1035ad1a49df98a19d91ad52d293b06af7 in /      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 28 Sep 2026 00:38:29 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /usr/share/buildinfo/      
# Mon, 28 Sep 2026 00:38:29 GMT
COPY dir:7de23c68b8fd94c0d7aa9510a73926c4cb9eba4d61c780efa23e67a24fab1560 in /root/buildinfo/      
# Mon, 28 Sep 2026 00:38:30 GMT
LABEL "org.opencontainers.image.created"="2026-09-28T00:37:55Z" "org.opencontainers.image.revision"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "build-date"="2026-09-28T00:37:55Z" "architecture"="x86_64" "vcs-ref"="5fed6512327cf4e03d25e424d9f6d5eed9016958" "vcs-type"="git" "release"="1790555810"org.opencontainers.image.created=2026-09-28T00:37:55Z,org.opencontainers.image.revision=5fed6512327cf4e03d25e424d9f6d5eed9016958
# Tue, 29 Sep 2026 18:05:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 29 Sep 2026 18:05:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 29 Sep 2026 18:05:57 GMT
ENV PSMDB_VERSION=8.0.32-14
# Tue, 29 Sep 2026 18:05:57 GMT
ENV OS_VER=el9
# Tue, 29 Sep 2026 18:05:57 GMT
ENV FULL_PERCONA_VERSION=8.0.32-14.el9
# Tue, 29 Sep 2026 18:05:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 29 Sep 2026 18:05:57 GMT
ENV PSMDB_REPO=testing
# Tue, 29 Sep 2026 18:05:57 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 29 Sep 2026 18:05:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 29 Sep 2026 18:05:57 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 29 Sep 2026 18:05:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 29 Sep 2026 18:06:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         krb5-libs         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 29 Sep 2026 18:06:18 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Sep 2026 18:06:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 29 Sep 2026 18:06:19 GMT
VOLUME [/data/db]
# Tue, 29 Sep 2026 18:06:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 29 Sep 2026 18:06:20 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 29 Sep 2026 18:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Sep 2026 18:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Sep 2026 18:06:20 GMT
USER 1001
# Tue, 29 Sep 2026 18:06:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:33f1022e4c482a50c061fe8571a030ebac06d5b2828de5731b7820abc02b6e63`  
		Last Modified: Mon, 28 Sep 2026 01:28:44 GMT  
		Size: 40.7 MB (40737982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a606c5b273ec07c4bf63682435d50f4fc5706af9298e3b9dbfecf16865ab196`  
		Last Modified: Tue, 29 Sep 2026 18:06:51 GMT  
		Size: 9.0 MB (8978505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddc296d8e079fc40acc45fc738f888eb02a87c1a6af2ffefae63752f3b6cd39`  
		Last Modified: Tue, 29 Sep 2026 18:06:59 GMT  
		Size: 274.1 MB (274132766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625faddbfdb30746181df907ac234d156cf25b7a2e33d4ecea577cf7f0e26747`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86daa1153f8b8612c4b6d3e7d38d8dd16ca2976480b426e51e343cab9a63f224`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be46994a59055669830f8a521137d52bd98cdc3be2ed8550b6c8601f4541b8`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6317381135f1e02e61dd939cb4077d0debbcc9ab79b8907e2f9e7c5aa31a75`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01836495fb18631ff610f5c3e77d5420153ed5027e359f05b5b440d4b194bf`  
		Last Modified: Tue, 29 Sep 2026 18:06:52 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56798cb3c6b041ca06f6ea40847ee3d123200d03a4df10fe2b90de9d7320718b`  
		Last Modified: Tue, 29 Sep 2026 18:06:53 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3a8b7b018d14b0ed9209d6dbf259bb2cde60879d946e8779b5e8c9897517`  
		Last Modified: Tue, 29 Sep 2026 18:06:53 GMT  
		Size: 5.0 KB (4966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.32` - unknown; unknown

```console
$ docker pull percona@sha256:c0fd9c725d2fde27c3f8b4adce42bd912b21fe9bab7beec3cddbaac3d25c385b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fb5b85a32657101ca9054c263f72bff04eaab17ab1a2c18651e517ec3fc8e7`

```dockerfile
```

-	Layers:
	-	`sha256:943cf19c25a153e178afb6d3870a90a923d313a2761b4ee2f5c794ceece02e92`  
		Last Modified: Tue, 29 Sep 2026 18:06:50 GMT  
		Size: 32.7 KB (32673 bytes)  
		MIME: application/vnd.in-toto+json
