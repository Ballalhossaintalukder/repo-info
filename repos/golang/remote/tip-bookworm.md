## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:bd2f44155042d6c898b72dc00a10f71c1dbb325a8d9248fb7e159419eb627ba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a2d9cc72f795c18dcf4f3cc14cefa72d4e87605bdb443411a34c3eef9adde18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334761939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2265f1491a75a8a15553777865202a69c8a6429197e32b31cbaf47b017a4a3f2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1789689600'
# Sat, 19 Sep 2026 00:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Sep 2026 01:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:55:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 29 Sep 2026 17:55:26 GMT
ENV GOPATH=/go
# Tue, 29 Sep 2026 17:55:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:55:26 GMT
COPY /target/ / # buildkit
# Tue, 29 Sep 2026 17:55:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 29 Sep 2026 17:55:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:eaac70c68abdf6ffacf6de10d31ed9de4813505d1a794eb7393cb27fceb624a6`  
		Last Modified: Sat, 19 Sep 2026 00:03:03 GMT  
		Size: 48.5 MB (48503440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2de2423ebd9d3290883175c0e46dccd6de955b08e6e9a5bd20909e3face240`  
		Last Modified: Sat, 19 Sep 2026 00:44:47 GMT  
		Size: 24.1 MB (24056077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81578410df169380efec491bfdc60a7e586d4b48ef4c0aeb9b6ff085812d9a7d`  
		Last Modified: Sat, 19 Sep 2026 01:46:20 GMT  
		Size: 64.4 MB (64424271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f48ca911d30c01dfd3a536851c89a4028048332f45569f66df7eb9be6ae825`  
		Last Modified: Tue, 29 Sep 2026 17:55:56 GMT  
		Size: 92.6 MB (92576152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0999eb6622672afabcfc473ab64fbbae45e06ec398e000d9469d723fe2f8fc34`  
		Last Modified: Tue, 29 Sep 2026 17:55:32 GMT  
		Size: 105.2 MB (105201841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2310cc23f680e781d4bd35ccae57454e1ed12c9642b757fa6d2aefd0a2c1b584`  
		Last Modified: Tue, 29 Sep 2026 17:55:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bf5c4436306af34b90f2d689a590fefbec122e55539ccb7cb40dbbd4848b5392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10531192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e609fe5cdbc304d872e0f6084aeff1c6c740dd21112fb2ef3fce04ec2f4591df`

```dockerfile
```

-	Layers:
	-	`sha256:40e7d6e8c22a4f8e0b26c73598dfb22aaa471cf6a98625ce503c73414b7633ed`  
		Last Modified: Tue, 29 Sep 2026 17:55:54 GMT  
		Size: 10.5 MB (10503090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f63642333bd0f9e438e998446778665422cc1ebeeabdcd405ba0f8f8349c9f7`  
		Last Modified: Tue, 29 Sep 2026 17:55:54 GMT  
		Size: 28.1 KB (28102 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:604211f2d156288f104c20bdda347b9cb4401e514627f7b63f235a9b9382f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293273500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f78799de0d53343af92b63884c3d974bd369a31f18483d5a25bb666c8156bc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1789689600'
# Sat, 19 Sep 2026 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Sep 2026 02:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:52:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:54:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 29 Sep 2026 17:54:22 GMT
ENV GOPATH=/go
# Tue, 29 Sep 2026 17:54:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:22 GMT
COPY /target/ / # buildkit
# Tue, 29 Sep 2026 17:54:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 29 Sep 2026 17:54:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a6c5079853e28bf683246929969c9815b5fe2309ca7008420ffa4f3b69991189`  
		Last Modified: Sat, 19 Sep 2026 00:02:43 GMT  
		Size: 44.2 MB (44202209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8a5fc11ebbfafa0cb2b3f94f30ae822f4f3c68b9cc1fc076c7fac3bd1a4e8f`  
		Last Modified: Sat, 19 Sep 2026 01:28:07 GMT  
		Size: 22.0 MB (21959053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b05f2afa4aeb0abd1b387e407cc8939c894ecaf8fbd3b034a72e34dae98c9a2`  
		Last Modified: Sat, 19 Sep 2026 02:26:25 GMT  
		Size: 59.7 MB (59661780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee0b18d13bd9402fe2cb1a6ce7f09b216079916cc3d2057ca09b4c636c47730`  
		Last Modified: Tue, 29 Sep 2026 17:54:51 GMT  
		Size: 66.4 MB (66426576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5834c2eea1c38cb14eb938262093caf670b377df50d3011c148b6338e7be6374`  
		Last Modified: Tue, 29 Sep 2026 17:54:51 GMT  
		Size: 101.0 MB (101023725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7de6a4cef4b510794a31bff56ac9086a1c05517ed0a0d08441007219451a904`  
		Last Modified: Tue, 29 Sep 2026 17:54:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3dd0c630266ed642a33cab1bb41aab906e418d5e96989bd66f05744ff2cac0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3135f26dafe989f1700961ac95e96bbd0b295efa05e4300866c89acb84d4ee58`

```dockerfile
```

-	Layers:
	-	`sha256:36e4ebad03f9340da23a679f1ac8fd5b33bf3023723d6cd6e6e5deb773f29901`  
		Last Modified: Tue, 29 Sep 2026 17:54:49 GMT  
		Size: 10.3 MB (10309784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9556033d5268c02d74c55d629f15857fca8acdc8d7947ce8cd75bcc6a4b06f80`  
		Last Modified: Tue, 29 Sep 2026 17:54:48 GMT  
		Size: 28.2 KB (28214 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c422ab91ee2d9959d486456c8fb160857b855f8f0c6f6659a07ecf6d84660e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322687414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c07925cd32720b3d865770f1f13bccc79986d8085a28b4384138b903af2aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1789689600'
# Sat, 19 Sep 2026 00:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Sep 2026 01:31:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:54:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 29 Sep 2026 17:54:40 GMT
ENV GOPATH=/go
# Tue, 29 Sep 2026 17:54:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:40 GMT
COPY /target/ / # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 29 Sep 2026 17:54:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:450fe15cad1eddfa7c19e4191f4de2d5c46b0c201ddee1db8d6f41d2fec7a742`  
		Last Modified: Sat, 19 Sep 2026 00:02:48 GMT  
		Size: 48.4 MB (48389910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528fa46febdafdfec8e02c978fc9de14e76dd532505c33472d8f915ac27a2f8`  
		Last Modified: Sat, 19 Sep 2026 00:47:27 GMT  
		Size: 23.6 MB (23627721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a0fa474a1ca8d79c015c72bce6d935298ea38f98b4e04dec9e350442e03d7`  
		Last Modified: Sat, 19 Sep 2026 01:31:38 GMT  
		Size: 64.5 MB (64500108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a81e5c49689a730440f0c74b465e36d76c6a4f00de49fab3be65fcd8ca1f75`  
		Last Modified: Tue, 29 Sep 2026 17:55:09 GMT  
		Size: 86.6 MB (86642109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407976649a33cee308503d4aa90a9d7d2d8c1f82dfaafc0b1053bffbd192236d`  
		Last Modified: Tue, 29 Sep 2026 17:54:56 GMT  
		Size: 99.5 MB (99527409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f155cbfb2db9360698cbb6776d4e958bd78a5288a91a00c8dae0b17665ebee`  
		Last Modified: Tue, 29 Sep 2026 17:55:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:404cb69ef259c77ba7940bb454e4ad9b56f849e2399cf0a3039af4f1e5be9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10559148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52094b57c28381f0ef8ddd1647d710de3c6f475609f071e8e4b4620b94a4abe8`

```dockerfile
```

-	Layers:
	-	`sha256:b3e44448b01b09704740b690399b6f41c155feab57041fbb3a3ec2bf39012bf9`  
		Last Modified: Tue, 29 Sep 2026 17:55:07 GMT  
		Size: 10.5 MB (10530914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d474630a5eee9af599121918bbc69e14c22a7670fb637af7f3eefc2a3d9add36`  
		Last Modified: Tue, 29 Sep 2026 17:55:07 GMT  
		Size: 28.2 KB (28234 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:06533c22e3b8657c85826ee605066075fa3a91d8a25e0ae94c471cf16a0e57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.6 MB (333635090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bc96beda525facf08d414a18f99cacd2865d30f8a9d88c9a86abf62728fbc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1789689600'
# Sat, 19 Sep 2026 00:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Sep 2026 01:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 17:54:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 29 Sep 2026 17:54:22 GMT
ENV GOPATH=/go
# Tue, 29 Sep 2026 17:54:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 17:54:22 GMT
COPY /target/ / # buildkit
# Tue, 29 Sep 2026 17:54:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 29 Sep 2026 17:54:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5251485f272d2f5b30f340b3424d4885551b55c64d74f383ca196bc8338f8f3e`  
		Last Modified: Sat, 19 Sep 2026 00:03:27 GMT  
		Size: 49.5 MB (49491404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8e3c04f871b1b16e9e51e8bd832c4d6c6367991bf2fb4fa68e1ada0e92f4d`  
		Last Modified: Sat, 19 Sep 2026 00:49:43 GMT  
		Size: 24.9 MB (24889211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707b21c933ac81a1325c7daf018024e4ba50850e560f2913144ce64343b9d3b`  
		Last Modified: Sat, 19 Sep 2026 01:35:29 GMT  
		Size: 66.3 MB (66257299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a5083a2775abc4c1a622dd29f2b35ca31fcc1bcbe696fc5f7033fdb679d685`  
		Last Modified: Tue, 29 Sep 2026 17:54:52 GMT  
		Size: 90.0 MB (89991435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d967aeb0675415130bbadac4f1c1ac365c9f4ede4e374f1f087f7b4cecd6f6cc`  
		Last Modified: Tue, 29 Sep 2026 17:53:53 GMT  
		Size: 103.0 MB (103005584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7de6a4cef4b510794a31bff56ac9086a1c05517ed0a0d08441007219451a904`  
		Last Modified: Tue, 29 Sep 2026 17:54:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bc3db979a15c60414b512f315292f28df99ea423e818b63c4bcf8cee699a8eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67065c26baeb1098623ec0242db357d52172b23f5f689bf5fffce8d92277363`

```dockerfile
```

-	Layers:
	-	`sha256:2a2fbe1198013fb49ad919ccc1fa388a84e10ab157113bcdaafdfe07530559d7`  
		Last Modified: Tue, 29 Sep 2026 17:54:50 GMT  
		Size: 10.5 MB (10482669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91897a5751a7ef9ac0763f017b8a5af0d3124fbc330a8843fd77e227b271a67c`  
		Last Modified: Tue, 29 Sep 2026 17:54:49 GMT  
		Size: 28.1 KB (28069 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b1a479ca11c8d6b9f85fe16ec2629a755636a1521b9b7bb4ebf902e10269b4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340192533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e8fd8a9eb00f1b293e6bc058ff00f76198fa6083edf2cd8d4f6b04ee389e0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1789689600'
# Sat, 19 Sep 2026 03:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Sep 2026 09:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 18:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Sep 2026 18:10:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 29 Sep 2026 18:10:06 GMT
ENV GOPATH=/go
# Tue, 29 Sep 2026 18:10:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:10:06 GMT
COPY /target/ / # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 29 Sep 2026 18:10:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:303f9548080ec7733e94ce124ddb2d901dc024b0db2d3e171bdfe62a1d04513b`  
		Last Modified: Sat, 19 Sep 2026 00:02:50 GMT  
		Size: 52.3 MB (52349305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e9f3363ace736c21292a425cd627663814b1275272b7cf79f502454af1cac`  
		Last Modified: Sat, 19 Sep 2026 03:16:20 GMT  
		Size: 25.7 MB (25703264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb8363b45637c8da3b7da1113159dbb24fb241a976701cf530477d2ae974472`  
		Last Modified: Sat, 19 Sep 2026 09:06:01 GMT  
		Size: 69.8 MB (69849171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2297a3bf9de8e522a5fddf94dc3aa1a0c0fead87ee774876352205e76ad574c`  
		Last Modified: Tue, 29 Sep 2026 18:12:16 GMT  
		Size: 90.6 MB (90578198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9dfcea9dbd54abdf4735c588b655a34ab5b353623c6254a20d02eaf7a19455`  
		Last Modified: Tue, 29 Sep 2026 18:12:17 GMT  
		Size: 101.7 MB (101712437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d51ed61ccbf89f7dbc24b464660647520dc719a0ecb3f3a97514e438aed8693`  
		Last Modified: Tue, 29 Sep 2026 18:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5d13c8fbde3ffade2952e66bd828d01dfd316922a3033e9140270fd4006e38ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671ce23eb1330a3c56a4685a0eda3166c215b9632143dd9d7a5e7ae8342ad0c`

```dockerfile
```

-	Layers:
	-	`sha256:a996498be6a36e5cea62b956017a4c27e22a00ee1ec6a3bb24c0e51d923564d8`  
		Last Modified: Tue, 29 Sep 2026 18:12:13 GMT  
		Size: 10.5 MB (10475575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bd64b98da38177be9746e446b8bd96f6d2961662031b4be7fad9ddf43c22e`  
		Last Modified: Tue, 29 Sep 2026 18:12:12 GMT  
		Size: 28.1 KB (28147 bytes)  
		MIME: application/vnd.in-toto+json
