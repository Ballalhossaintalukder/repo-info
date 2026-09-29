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
