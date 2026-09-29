## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:bd07857c8870598c53b14c7e06220dca3ac2ecc55d23cab655ec4c847daa1095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5622; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.5622; amd64

```console
$ docker pull julia@sha256:d80b2fd1d3f8d0bd40a75273cc2444796167da8b315d5d74ad7f8f0922194e55
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528711919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d049d0624180ccb46605e8b882e0814a8518de02ac2c3deb84c1411ca66b40`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sat, 05 Sep 2026 23:48:54 GMT
RUN Install update 10.0.20348.5622
# Mon, 28 Sep 2026 23:42:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Sep 2026 23:42:50 GMT
ENV JULIA_VERSION=1.13.1
# Mon, 28 Sep 2026 23:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.1-win64.exe
# Mon, 28 Sep 2026 23:42:53 GMT
ENV JULIA_SHA256=a9748efca5e4c4a4188261fd569f9275426cb655781692be308d604da1c1e1b7
# Mon, 28 Sep 2026 23:48:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Sep 2026 23:48:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415798186eb335ced6c3ef7f07db644b7c42771bc47e33781ec5cea24c3285b6`  
		Last Modified: Tue, 08 Sep 2026 17:15:52 GMT  
		Size: 730.5 MB (730469634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92da9030d6488f94c1464eb176bb167430fb388622462eac1f949824e0acc18e`  
		Last Modified: Mon, 28 Sep 2026 23:48:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff33d826f815dec6608e75581bc01ec232731fb89cb350ded1dd8bd78454911`  
		Last Modified: Mon, 28 Sep 2026 23:48:37 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f378efe657f23f5ca4ae347c6b2bf7458de16545e1ad8e559df5143c8b54f2ab`  
		Last Modified: Mon, 28 Sep 2026 23:48:36 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d9687ed7d58f696d166555a841fa614e9547d662d39bf95ee4adb669bfc06`  
		Last Modified: Mon, 28 Sep 2026 23:48:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7dc4c6ea2d5855227f2a4f5885ef3a733b6cb6b437857e7129c06c6001b4c`  
		Last Modified: Mon, 28 Sep 2026 23:49:16 GMT  
		Size: 309.2 MB (309216633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f9703cfdaae26f297da651b0bd60ed19718316a562b5bb325e333cfb6c798`  
		Last Modified: Mon, 28 Sep 2026 23:48:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
