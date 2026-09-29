## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:b417f835dcc78c9ce25972bdd52e46fd0e687072c6b10e04cc87274e4e69cd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.33438; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.33438; amd64

```console
$ docker pull julia@sha256:19533cd65ce7a09fa1c1d3359fa79f8dd9ea2a397e9ab3d718b527941f2d63e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766881546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb156701154c8684a82a72cff8e6bb0ee154f53ecef00ae3847f0ffe6fddde0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sat, 05 Sep 2026 17:41:23 GMT
RUN Install update 10.0.26100.33438
# Mon, 28 Sep 2026 23:42:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Sep 2026 23:42:48 GMT
ENV JULIA_VERSION=1.13.1
# Mon, 28 Sep 2026 23:42:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.1-win64.exe
# Mon, 28 Sep 2026 23:42:49 GMT
ENV JULIA_SHA256=a9748efca5e4c4a4188261fd569f9275426cb655781692be308d604da1c1e1b7
# Mon, 28 Sep 2026 23:45:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Sep 2026 23:45:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ad760a8a0dac5abb352847ef76295f82b76df46372259a4df2102ad3adf78b`  
		Last Modified: Tue, 08 Sep 2026 17:45:23 GMT  
		Size: 934.6 MB (934570301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6b024ac08375648c1d3dd9d1a3c8a18f7b37a721d60c44715afdfa6d482b9f`  
		Last Modified: Mon, 28 Sep 2026 23:45:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eedd547e6565009d09136b32123dcfbb47e9c821c9723509f1b78c79274df4d`  
		Last Modified: Mon, 28 Sep 2026 23:45:10 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f7494af7342a64846fb01f7d034da738025632fca7997226f8f6f662e446ff`  
		Last Modified: Mon, 28 Sep 2026 23:45:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8ca8a7b4053d8487ca8e6500f15c3a3d55dbcbff0904f278191790aebb53d3`  
		Last Modified: Mon, 28 Sep 2026 23:45:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538907158ce0a26fc27b0632ccfb5a0f53902c110053d89da29fd5c8009d2b4`  
		Last Modified: Mon, 28 Sep 2026 23:45:47 GMT  
		Size: 309.2 MB (309245397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d74d26b958700b42ea4084988788b2fd993551ec2dee1e2f879f0068e36028`  
		Last Modified: Mon, 28 Sep 2026 23:45:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
