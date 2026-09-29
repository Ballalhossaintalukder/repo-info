## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:a88641c76917a36ec13813df21ab9edb0af07c840711b22bc7f69a412ba11a86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1d2e53e632cbc07bdc0e9552ff403bb979fb43bf0e6eef746c36e8f48ca738ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123048246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dc845e78b4176bbcaac69d7874660c436bbe169aec000dea41b9a90295a3f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:59:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:59:58 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:10:18 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:10:18 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 20:10:18 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6e8bab6e74dd45e342ebe1c65e3f77adc2b305a64dcd2f7775ecfe9eb4cf2a18`  
		Last Modified: Sat, 26 Sep 2026 04:08:50 GMT  
		Size: 63.0 MB (62965372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc10ebfd418ee27345144979ad1f5d7d35ab3a20eff15a45a01235f4d7af6d0c`  
		Last Modified: Mon, 28 Sep 2026 20:10:33 GMT  
		Size: 60.1 MB (60082874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:81aa4916c63ebed525a4f07ca176f983cc292f76521e8c07739676facb8fc421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5366685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c641314833567bfbce8c9b3e52e5aa4947a5aa107d102842bad016e25027c328`

```dockerfile
```

-	Layers:
	-	`sha256:4ccbc4a23d8deeb5487e7cc588bce7dfd6a504b0ad719bcf2391c84d0cc52cce`  
		Last Modified: Mon, 28 Sep 2026 20:10:31 GMT  
		Size: 5.4 MB (5355776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb693a4abb869f3c58bbcf3640630c74de3cc66146db6c3be93f1fe275148ee`  
		Last Modified: Mon, 28 Sep 2026 20:10:31 GMT  
		Size: 10.9 KB (10909 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e1b4f42828e827a1760a26e081921ff98368b04a57780976b86305ae6035cdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124705950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6599d80d236d7f43dac7d097239d44365b19a956e4f53b18b54cdee8b623e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 20:00:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 20:00:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Sep 2026 20:10:11 GMT
ARG version=1.8.0_504.b01-1
# Mon, 28 Sep 2026 20:10:11 GMT
# ARGS: version=1.8.0_504.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 28 Sep 2026 20:10:11 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 20:10:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f73a3cbd21c88784f7ccaecb25687e74f9e18107394c9ac4f97f661ecb05173c`  
		Last Modified: Mon, 28 Sep 2026 07:53:59 GMT  
		Size: 64.8 MB (64806159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0c786ac1270a81a1f013058504cfa926e8978bacb23d964d201782efe54cf3`  
		Last Modified: Mon, 28 Sep 2026 20:10:26 GMT  
		Size: 59.9 MB (59899791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1b68f2ac34a35cf0b8d90e3535bbcc63ca85213d02a72cf24e91deb5ce66044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5366386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56cd4b49ff2c1c3b104b7e1844683219d36c5fab88fbf99f5f49b2836ad74f7`

```dockerfile
```

-	Layers:
	-	`sha256:9427533c492cc93a7dccd50d8eb5514b9d12c21666f87f9232ad8f59264add33`  
		Last Modified: Mon, 28 Sep 2026 20:10:25 GMT  
		Size: 5.4 MB (5355338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e653847d882fcfc2f6d5a4ee311b99cff8e5f82940d16d8b0da8d3b2e210d1`  
		Last Modified: Mon, 28 Sep 2026 20:10:24 GMT  
		Size: 11.0 KB (11048 bytes)  
		MIME: application/vnd.in-toto+json
