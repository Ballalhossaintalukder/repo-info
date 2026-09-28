## `archlinux:base-devel-20260927.0.600689`

```console
$ docker pull archlinux@sha256:51dd3d24f7fba779e7c471caeee7804c50e8c134ad948e19685a1c83a42facc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260927.0.600689` - linux; amd64

```console
$ docker pull archlinux@sha256:8edb44f40a0cb5d3e44ef474f02780098ce0084e591c8641bdc01f02f185cc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 MB (308019709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34af4119590d5a3a0f0b5c477b50093954b32886c858c01fcb3c1c543274fea5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.version=20260927.0.600689
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 28 Sep 2026 19:21:42 GMT
LABEL org.opencontainers.image.created=2026-09-27T00:10:06+00:00
# Mon, 28 Sep 2026 19:21:42 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Sep 2026 19:21:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260927.0.600689' /etc/os-release # buildkit
# Mon, 28 Sep 2026 19:21:49 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 19:21:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:27af5b1cb8f85fbabef288d4d274bc1cb91aa34e96e8f31766ab6c4cbb53844e`  
		Last Modified: Mon, 28 Sep 2026 19:22:41 GMT  
		Size: 308.0 MB (308008204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b2c7e4c0de65cb8100863e2533227dca4ccf6e1c07ce2540ab9ab8e190ab`  
		Last Modified: Mon, 28 Sep 2026 19:22:35 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260927.0.600689` - unknown; unknown

```console
$ docker pull archlinux@sha256:616ca35582fbe6951e54027cbf3278bcb346ec9dab6e648138156cf24079b88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759f5bae127a669e775911e7def4ba6890a1ad8b317f363a811326272b06ab7f`

```dockerfile
```

-	Layers:
	-	`sha256:089babf3a676a2ff62c3d689713fdb69a3de91731cbeac93b6b64453c14b4cf2`  
		Last Modified: Mon, 28 Sep 2026 19:22:35 GMT  
		Size: 14.4 MB (14447629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3668a92c97a10d16ec26a879d79a54d034eb79bb8fc0ccead3a2bd350af2d93e`  
		Last Modified: Mon, 28 Sep 2026 19:22:35 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
