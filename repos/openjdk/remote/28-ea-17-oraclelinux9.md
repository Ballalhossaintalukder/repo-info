## `openjdk:28-ea-17-oraclelinux9`

```console
$ docker pull openjdk@sha256:8d02c7fed8d6aa51204eba022db948095ea4698ab4226d8468b0185dbfe136e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-17-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:d55e358bfa13f580dd223a3cfb3959c047ab71c69a613ecb40620a398a97a412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329032776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab7c820ea00d5f6c8ccdc9ddcea5e15e20ba57c60794aa7c8c6fe8a2b8bbafa`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Sep 2026 18:06:05 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:06:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:38:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:39:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 29 Sep 2026 18:39:02 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:39:02 GMT
ENV LANG=C.UTF-8
# Tue, 29 Sep 2026 18:39:02 GMT
ENV JAVA_VERSION=28-ea+17
# Tue, 29 Sep 2026 18:39:02 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/17/GPL/openjdk-28-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='59f29554ce7e6bdfba2c28181f5f7689cad7722d650d8cb7f20d611cfce41808'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/17/GPL/openjdk-28-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='0894b7bbf4c95f0b8a76d4ee6e78390d4cc3767fad41ffbcdaa4010f03a4f1cc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 29 Sep 2026 18:39:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0da02031b8109b1e4f838db1d6ebbebafcce8f05b799018f73cb97e201d2c663`  
		Last Modified: Tue, 29 Sep 2026 18:06:16 GMT  
		Size: 47.9 MB (47941627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef22f4929c75e7f7045ff52e4e7c2799d2a2a12a4e1263c9724dc1836c4c896`  
		Last Modified: Tue, 29 Sep 2026 18:39:27 GMT  
		Size: 38.3 MB (38279009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068e1ab486d92a51ff5d825e95f6bd73e163e46feb666930690e98c63e7f4ef`  
		Last Modified: Tue, 29 Sep 2026 18:39:31 GMT  
		Size: 242.8 MB (242812140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-17-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:8823faf096e31132a9c72dbe4daf7e5433af146a370d2683fa29859bcb0157f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a3888fec27fad2945fd3ffbb77e7e60bff3e815bd2fd5c2271eb828a37c4fa`

```dockerfile
```

-	Layers:
	-	`sha256:58044b6dccb357233a02fa8b8008694568ae781c85a3111215939e286d5a3a1c`  
		Last Modified: Tue, 29 Sep 2026 18:39:26 GMT  
		Size: 3.7 MB (3656652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61718187fecb73b6d60d8eab4522fb249e763c6f90ad7231338a4e6218ee135a`  
		Last Modified: Tue, 29 Sep 2026 18:39:26 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-17-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:938b2c981cc138442048c12d13d546dff332fcd32482062797a65cfe56390a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326028249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de04c4f767969cf2c00c7f1eff62cbad527f762e75c579a68b15e34c4d09914`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Sep 2026 18:04:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Sep 2026 18:04:02 GMT
CMD ["/bin/bash"]
# Tue, 29 Sep 2026 18:10:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 29 Sep 2026 18:10:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 29 Sep 2026 18:10:44 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Sep 2026 18:10:44 GMT
ENV LANG=C.UTF-8
# Tue, 29 Sep 2026 18:10:44 GMT
ENV JAVA_VERSION=28-ea+17
# Tue, 29 Sep 2026 18:10:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/17/GPL/openjdk-28-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='59f29554ce7e6bdfba2c28181f5f7689cad7722d650d8cb7f20d611cfce41808'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/17/GPL/openjdk-28-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='0894b7bbf4c95f0b8a76d4ee6e78390d4cc3767fad41ffbcdaa4010f03a4f1cc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 29 Sep 2026 18:10:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a7411e35d6d4eea8eeb20d02d7532cb2bf74ebb746bccf80d7ec7d4d5f99efff`  
		Last Modified: Tue, 29 Sep 2026 18:04:15 GMT  
		Size: 46.5 MB (46485404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77685572848e555318037347fc4070104089347987311dbab0972aa1bbd9eec5`  
		Last Modified: Tue, 29 Sep 2026 18:11:12 GMT  
		Size: 38.7 MB (38672291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfddefd7085c9029b586a501df2a540219ed74ce46dd34b0ed4b561e27fcfa2f`  
		Last Modified: Tue, 29 Sep 2026 18:11:16 GMT  
		Size: 240.9 MB (240870554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-17-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:078d8df222cf57a3cb569fc3c02bbd7d5fc423589cbfb09f87016ead6dc00deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832545dbea580fb93ea7c5d7378b508b0c69f2943a052625af8786fc0ab691be`

```dockerfile
```

-	Layers:
	-	`sha256:7647c9a7b8c8c4a90e32ce4b1b33098371ab2144295a79a9890270920bc6f191`  
		Last Modified: Tue, 29 Sep 2026 18:11:10 GMT  
		Size: 3.7 MB (3654262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319c8ed3711c151e672b2992a90379466d1611f5ff010fe54bb3901404446012`  
		Last Modified: Tue, 29 Sep 2026 18:11:10 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
