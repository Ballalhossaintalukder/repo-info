## `julia:1-trixie`

```console
$ docker pull julia@sha256:3020db6caac249f56124b9ca90b92c24af460b3f3a99c8a287097ba5d72e5da4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:3cfe070b79d4006209a64da305bef372b881f6ef713ddc5bae3fa4fdab7fb75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342385368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a909fd67c47640113acdb607232cd144552db8df03cf9c791cdfb8c0d0e4dd4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1789689600'
# Mon, 28 Sep 2026 23:39:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 23:40:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Sep 2026 23:40:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Sep 2026 23:40:17 GMT
ENV JULIA_GPG=64B779A570972FFF7BFC2B54EAD471E1A1F2C10A
# Mon, 28 Sep 2026 23:40:17 GMT
ENV JULIA_VERSION=1.13.1
# Mon, 28 Sep 2026 23:40:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.1-linux-x86_64.tar.gz'; 			sha256='0f2e18c8dea60a2c8711d089cd9612f7a8df394b89e5208096fe5867647e0908'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.1-linux-i686.tar.gz'; 			sha256='8bd3f8f20c0fd346b31ba5204f50d770c21abc0dba6f37b7ad7c02faa05033a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.1-linux-aarch64.tar.gz'; 			sha256='78341862e24734ea1c2fa8795183c52627c23a99aba5aa1d0ec840edecec5ce0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Sep 2026 23:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Sep 2026 23:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Sep 2026 23:40:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6b37362b3da78869050b894b799ad4df04f1f3b52774087db0d81151570244c8`  
		Last Modified: Sat, 19 Sep 2026 00:06:05 GMT  
		Size: 29.8 MB (29830418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543f97d6f4d104f87cf50a1a08f5c7dc995982f7d0a71a39306bd26e5c873f6`  
		Last Modified: Mon, 28 Sep 2026 23:41:00 GMT  
		Size: 6.2 MB (6249340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a1787301f220e82f88ac81b6321eb97818f8e6082c5227c1914595888b75a`  
		Last Modified: Mon, 28 Sep 2026 23:41:05 GMT  
		Size: 306.3 MB (306305237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9029e39d4be160a7656370f153cbc5582a2da82e7ac73ee3df38b4c8e352a0e`  
		Last Modified: Mon, 28 Sep 2026 23:40:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1419624df307dcce75afcb405b57aa56387cded5bedc9cf3694d81619d40f531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2265334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b6386289162a995eb791344138a852524107fb56dfa8c2cb9689fcfc3d13d2`

```dockerfile
```

-	Layers:
	-	`sha256:e52a4a2ca440dd6e8d41eabb1cf3298ce21dc691b0094753339b790ca4d53a1c`  
		Last Modified: Mon, 28 Sep 2026 23:40:59 GMT  
		Size: 2.2 MB (2247633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3977dd3836cba102027704599aab0a8556efb2c82bd241fb3b0d2c6edbca7435`  
		Last Modified: Mon, 28 Sep 2026 23:40:59 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fc35c2cc45fe796d145ff77d0085ae48b9728e6f1e698b695bceaa03e1700b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361702091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba82012fb043b98d22bbdd6b23f75897c78038a7733b65f9b9774bd4f563513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1789689600'
# Mon, 28 Sep 2026 23:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 23:40:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Sep 2026 23:40:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Sep 2026 23:40:06 GMT
ENV JULIA_GPG=64B779A570972FFF7BFC2B54EAD471E1A1F2C10A
# Mon, 28 Sep 2026 23:40:06 GMT
ENV JULIA_VERSION=1.13.1
# Mon, 28 Sep 2026 23:40:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.1-linux-x86_64.tar.gz'; 			sha256='0f2e18c8dea60a2c8711d089cd9612f7a8df394b89e5208096fe5867647e0908'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.1-linux-i686.tar.gz'; 			sha256='8bd3f8f20c0fd346b31ba5204f50d770c21abc0dba6f37b7ad7c02faa05033a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.1-linux-aarch64.tar.gz'; 			sha256='78341862e24734ea1c2fa8795183c52627c23a99aba5aa1d0ec840edecec5ce0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Sep 2026 23:40:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Sep 2026 23:40:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Sep 2026 23:40:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd36565c0fdebaf0f3af5c3b4ce610ca085ced32e9e9da850d95912f5f18f47b`  
		Last Modified: Sat, 19 Sep 2026 00:05:57 GMT  
		Size: 30.2 MB (30189691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0366dd6aa3937678d5593d07e08d63bfbff75430329bc821e7398047814c3ba9`  
		Last Modified: Mon, 28 Sep 2026 23:40:52 GMT  
		Size: 6.2 MB (6156312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765cd64b5d9f5c6baff9d0f361816e0e159ce149ba61379e0109bb9bb2951e8`  
		Last Modified: Mon, 28 Sep 2026 23:40:58 GMT  
		Size: 325.4 MB (325355717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ad0a31b9b6b4d419688eca44c451d678ebabf52206aba383d9c3bbe065b66`  
		Last Modified: Mon, 28 Sep 2026 23:40:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:08bc340756f73efcfec64cc6941447861f45d61f57f162e5f8e52bb11ab518ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2265825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ee11e2d0c74ff5c610f7fb83f083fafb43bde33f068ae7651d89273e67d4d`

```dockerfile
```

-	Layers:
	-	`sha256:ce2c43b1d79a851f5bd063f9ef92be1e49aaa58b755f8d186e043b744fe59c12`  
		Last Modified: Mon, 28 Sep 2026 23:40:52 GMT  
		Size: 2.2 MB (2247957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2f8ec7b811f1b24fb5e7f792bebea56321547547ef24000e13b6ad53515580`  
		Last Modified: Mon, 28 Sep 2026 23:40:52 GMT  
		Size: 17.9 KB (17868 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:aafb099c15d17941bc38fa8e627511247ecb24c49aa9d4790fd10382ac8a5b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280474343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691a5a29a9c02806d285ef2aef63bcbb27f81755642cdaddb80ec4611ecf958b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 18 Sep 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1789689600'
# Mon, 28 Sep 2026 23:39:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Sep 2026 23:39:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Sep 2026 23:39:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Sep 2026 23:39:56 GMT
ENV JULIA_GPG=64B779A570972FFF7BFC2B54EAD471E1A1F2C10A
# Mon, 28 Sep 2026 23:39:56 GMT
ENV JULIA_VERSION=1.13.1
# Mon, 28 Sep 2026 23:39:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.1-linux-x86_64.tar.gz'; 			sha256='0f2e18c8dea60a2c8711d089cd9612f7a8df394b89e5208096fe5867647e0908'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.1-linux-i686.tar.gz'; 			sha256='8bd3f8f20c0fd346b31ba5204f50d770c21abc0dba6f37b7ad7c02faa05033a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.1-linux-aarch64.tar.gz'; 			sha256='78341862e24734ea1c2fa8795183c52627c23a99aba5aa1d0ec840edecec5ce0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Sep 2026 23:39:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Sep 2026 23:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Sep 2026 23:39:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fa51aa063d1c9d8582b37a45055739eef6ee879e1364bcb6b75a064ad0d1906`  
		Last Modified: Sat, 19 Sep 2026 00:04:01 GMT  
		Size: 31.3 MB (31340398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5cee169f604a8ecbc199b1e46e61e0543aaea3cc1ad9a094fe89c4de660b6`  
		Last Modified: Mon, 28 Sep 2026 23:40:29 GMT  
		Size: 6.4 MB (6436338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fcb59d0969b36cecdd2c91bedd98895e139d4cb3595de3e7120f56383c830b`  
		Last Modified: Mon, 28 Sep 2026 23:40:33 GMT  
		Size: 242.7 MB (242697240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed31b011875b42105d61eb1617fc7a9ffec8100b23c9ada6df0f158c747a5842`  
		Last Modified: Mon, 28 Sep 2026 23:40:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:0832ea23c70c2052280ace84b048d1d4b44b59749503647e765fca3cf0edc8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa7e980f31ac8b682d4a4e52c3b167b5349f4f0908806e8d64931d202368bb`

```dockerfile
```

-	Layers:
	-	`sha256:89473f9227f260ea06f7fdfb330aca47992da02ac560e46b846908d7be3ce0b2`  
		Last Modified: Mon, 28 Sep 2026 23:40:28 GMT  
		Size: 2.2 MB (2244758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f23288df4e17c5e1763566ca320413c483fa9454e2777c87a091644ebcdc039`  
		Last Modified: Mon, 28 Sep 2026 23:40:28 GMT  
		Size: 17.6 KB (17647 bytes)  
		MIME: application/vnd.in-toto+json
