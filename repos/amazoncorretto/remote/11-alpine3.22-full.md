## `amazoncorretto:11-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:cf7e6f7cfa8dfcb4e5f02fd68fba4d99f75fda8fa28015611af102b8b24cfbbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fdc85aac06fa62257549c51c9cd2ec8a3786baabe520a6da027b26ae3f61c6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147746227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47aa1d59d82d3efdeb6c1dac33bb072207a18868c0cd7499392227fe40dc604`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:44 GMT
ADD alpine-minirootfs-3.22.6-x86_64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:44 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:03:01 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:03:01 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:03:01 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:03:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:03:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:53f8f5e03afd86ade91b7aa57a749f5a3d1419c113be5d8c10e7ee61bb5ab887`  
		Last Modified: Thu, 17 Sep 2026 20:37:49 GMT  
		Size: 3.8 MB (3792075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e7b9bf853abfe8dcfec34f948186482f7415b3d43ec77f6421044200d5e88`  
		Last Modified: Mon, 28 Sep 2026 18:03:17 GMT  
		Size: 144.0 MB (143954152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:524f20124b0a827dc30dd053b922f2232bfb8c8f71fa505daae204bcc776e7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f7dd6f4e6cedbb14049affd8723ede234cb22223f8792f9d007237fe3dcff`

```dockerfile
```

-	Layers:
	-	`sha256:431909437459a1b81737b2628af35b2be69251c897f80bdb608d3022f77ecada`  
		Last Modified: Mon, 28 Sep 2026 18:03:13 GMT  
		Size: 588.9 KB (588939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b1e7b8f1138c748127596ca418693fc3b801f10051e34a12775db42daa95b24`  
		Last Modified: Mon, 28 Sep 2026 18:03:13 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5dafaa8e33705c3086f01a2a7bee0d83bb355828907e93b65570f80e0848087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146455153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906ea0975a9633d0bf0b64c9effbf2c743474d8f4618bc1f585147d038f32d1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Sep 2026 20:37:30 GMT
ADD alpine-minirootfs-3.22.6-aarch64.tar.gz / # buildkit
# Thu, 17 Sep 2026 20:37:30 GMT
CMD ["/bin/sh"]
# Mon, 28 Sep 2026 18:02:50 GMT
ARG version=11.0.32.12.1
# Mon, 28 Sep 2026 18:02:50 GMT
# ARGS: version=11.0.32.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 28 Sep 2026 18:02:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Sep 2026 18:02:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 28 Sep 2026 18:02:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:16fc4f52163f03cd2189c3d6a4b3f28a605cfb7919af64b3da4562cca69d2306`  
		Last Modified: Thu, 17 Sep 2026 20:37:36 GMT  
		Size: 4.1 MB (4123084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067cba9d368098abd7eb7a6e61274f8e2e23c25138d3875331c05017dfc6b52`  
		Last Modified: Mon, 28 Sep 2026 18:03:08 GMT  
		Size: 142.3 MB (142332069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92bc46d6ea1b43f21f2f33d1902652cead44b0cb3c33404d0fb4e49893fd5cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5940f4fc78cdd25dae425a7b56e118db9bc72b7be53634f981cac6ae4600c9`

```dockerfile
```

-	Layers:
	-	`sha256:685157fe01dfbcc802441260b4613cc0f53328118eb9b49da6847bfe8eaf27b6`  
		Last Modified: Mon, 28 Sep 2026 18:03:04 GMT  
		Size: 589.0 KB (588995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f7a1da4beb950b900a4bb42a6a1e783323f140c2e7e54dc56766b529d987e5`  
		Last Modified: Mon, 28 Sep 2026 18:03:04 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
