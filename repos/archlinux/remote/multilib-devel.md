## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c8b647459b2836c213c3382091cd946bd67ae1e484cb6c412f105a8d91370bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bab132758d881b917ce978bb935420c672a8626a5b6846336e49f790ff420c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330502220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37400cd59eb580c486020c3c79d340996e42c96eec08dcf051415adfc83e8ae`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.version=20260927.0.600689
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 28 Sep 2026 19:21:24 GMT
LABEL org.opencontainers.image.created=2026-09-27T00:10:06+00:00
# Mon, 28 Sep 2026 19:21:24 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:21:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260927.0.600689' /etc/os-release # buildkit
# Mon, 28 Sep 2026 19:21:32 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 19:21:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2cade83a685b7d78a6373d08f7c8d885fd3188244c1a285953bd77be24d46db7`  
		Last Modified: Mon, 28 Sep 2026 19:22:29 GMT  
		Size: 330.5 MB (330489505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a405d9b1716c4a1446431483ce5ef7768afaa805b507ff7e5c6c8fcfec4eb7d`  
		Last Modified: Mon, 28 Sep 2026 19:22:22 GMT  
		Size: 12.7 KB (12715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:60b8f1a3d314a28977736b2c1a4b2fc4cda04f0ea4bb14b023af5d2fba4a9cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a85beec15f459f264b55f367a242acac678eacc9d9fc6a85d5596a416086082`

```dockerfile
```

-	Layers:
	-	`sha256:201495d2a74e967f26881c540bb3520ecab2305b021bca381fd53741e3128455`  
		Last Modified: Mon, 28 Sep 2026 19:22:22 GMT  
		Size: 14.7 MB (14718717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c63f00825fedd5588b0b2002e5b510b154d24617af791171531dc52c02da7b4`  
		Last Modified: Mon, 28 Sep 2026 19:22:22 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
