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
