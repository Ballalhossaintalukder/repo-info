# `buildpack-deps:oracular-scm`

## Docker Metadata

- Image ID: `sha256:ce3b2a7e0f7d79e4dfa160fb57d78622917c15040fe4b2e611b01b04ab8a3eae`
- Created: `2024-08-13T17:58:12Z`
- Virtual Size: ~ 260.51 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=24.10`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA512:8376928f8a96880edce6e6f1073623ed03bf3da4489807d531c0ecd4c5ff09d19754007e3533922389134aa55a4b64d6f71caa7186133d5a5f559eecf7e33427
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA512:58f4f202baa58a6912f85682b967dca282981c1b8d57ffcda1cd67784b5e3f1865ccd1c452d06a50978649d3cb5198d2d5d23004e103b5bd89352a7c1904444f
```

### `dpkg` source package: `adduser=3.137ubuntu2`

Binary Packages:

- `adduser=3.137ubuntu2`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.dsc' adduser_3.137ubuntu2.dsc 1688 SHA512:d0d9ec7cd37888ef35f697feb135951f5d929b889207911bda34519a9484f763324ed9f998ecbd97198b41613a5c7e4735f553ad23007af21aa6cccfd3586f6a
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.tar.xz' adduser_3.137ubuntu2.tar.xz 280520 SHA512:56ef280c99f93fffdd0e877a8592e51351f200df4dcafb5c3d81a459682838896563751f825718fb5bdf3b733781b93aee6b7343526d59cc467522f31f2b9859
```

### `dpkg` source package: `apr-util=1.6.3-3ubuntu1`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu1.dsc' apr-util_1.6.3-3ubuntu1.dsc 2897 SHA512:332d3b2c61b885c8c1bdc878b50366e296fe5dd148e5152530b18db549d582196b927e20521af3b3bb70f457740210f380900fe5821a75d354e6778d4ceb8c13
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2.asc' apr-util_1.6.3.orig.tar.bz2.asc 833 SHA512:6c483e823fb032b161b6bcf77f9a43945aee9afbe40050ebf042865434bc533d21168af20d4cdff597b60b782d8ac9322409a5c2a64bf921b22f5add2451d79d
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu1.debian.tar.xz' apr-util_1.6.3-3ubuntu1.debian.tar.xz 342592 SHA512:f9b1af3bf058bb3f4a75b7fb905dda1ee7609f19999cbe180bc73b2df381a420b871e0ae435bd7e672a49d39a4ad3a0221721ad6fb68e6c59acde5b738f3684c
```

### `dpkg` source package: `apr=1.7.2-3.2ubuntu1`

Binary Packages:

- `libapr1t64:amd64=1.7.2-3.2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.2-3.2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.2ubuntu1.dsc' apr_1.7.2-3.2ubuntu1.dsc 2097 SHA512:4f61c0acf136af3a3a0f901d8fc354555b8a6f3a6d024e43375fbf37958cacbc70734244bc2deb9e78a9fcb1e613ee9243356c78faa72aafddec8f204bbffe16
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2' apr_1.7.2.orig.tar.bz2 890218 SHA512:0a3a27ccc97bbe4865c1bc0b803012e3da6d5b1f17d4fb0da6f5f58eec01f6d2ae1f25e52896ea5f9c5ac04c5fddcfd1ac606b301c322cf40d5c4d4ce0a1b76e
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2.asc' apr_1.7.2.orig.tar.bz2.asc 833 SHA512:77da1e516b30032419b36da8453f56c6149ad18631772613adb095b6eccb7606dc51589d33d422572d3fcefe8f6129bfbb06d0ab7fde5848d873856f4ed93940
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.2ubuntu1.debian.tar.xz' apr_1.7.2-3.2ubuntu1.debian.tar.xz 55316 SHA512:5446d2c28bdff2cfd2e7447b599d9d69e2dd104998186b5f86396e6788f53bbf4d247763ac254d965b7545a6c31e937245c91f1691ea83648998e9425ec1320b
```

### `dpkg` source package: `apt=2.9.8`

Binary Packages:

- `apt=2.9.8`
- `libapt-pkg6.0t64:amd64=2.9.8`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.9.8
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.9.8.dsc' apt_2.9.8.dsc 2973 SHA512:461a8f74df4c02bd478950a3d4696e38a100ff34619986389e4e85ac4994d99bc70f6f4b949d3e972b26a332996525b8fdb50c9314d4421f022b7b4d61128170
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.9.8.tar.xz' apt_2.9.8.tar.xz 2388012 SHA512:b45229b244d3d7e98e13f25e6eb8d8f3b0a06e163dc736e1b0f5d975bad21e7f7b39d2e88a5a09c212e3d6d7bd265120100e0b2de7348440ded06f6efc3bc4cc
```

### `dpkg` source package: `attr=1:2.5.2-1build2`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1build2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build2.dsc' attr_2.5.2-1build2.dsc 2580 SHA512:a093106c93d64dc87e9e3b43a1645e7b12a8bb3d0dad217738ae837fd2631f68f05f534bb3b97d64cb3f5a45fed3bfc0e4c5a21ec0392c5895702a286ef13aa5
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build2.debian.tar.xz' attr_2.5.2-1build2.debian.tar.xz 26028 SHA512:0e2015dfd901bcd79202f032761973a3314eeddca984bffb1b0babe48f1c1e5cd754ecdd1f56654cece20e5df79c6d308446bf8223e611164181c74861e7937d
```

### `dpkg` source package: `audit=1:4.0.1-1ubuntu2`

Binary Packages:

- `libaudit-common=1:4.0.1-1ubuntu2`
- `libaudit1:amd64=1:4.0.1-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.1-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.1-1ubuntu2.dsc' audit_4.0.1-1ubuntu2.dsc 2757 SHA512:7b2fa3fe3a6d2db564471a75a5dd4e2c1edca4a4c7169eb009fc03659f44e1db0a00a34df963301f67b85e6492d7390c2991ae1e0a0398f69bd754643ed65bfe
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.1.orig.tar.gz' audit_4.0.1.orig.tar.gz 1194961 SHA512:7fbc426d0ddea340a36ceab52ac090e8e3dfb3450ebf50b478324a097f19ab4bb2cf78a2532644acb17e6114b59b8fda718affda9da62fb84181e3abf76039df
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.1-1ubuntu2.debian.tar.xz' audit_4.0.1-1ubuntu2.debian.tar.xz 20008 SHA512:794952d3a27c3029ccb168c35f0aea85fc6973b7793fd0ed698091635cb8a009e93c8561c8b3bdb86995a0cca36993cb9f490db4d42a4dc03e57589379e12bd9
```

### `dpkg` source package: `base-files=13.3ubuntu6`

Binary Packages:

- `base-files=13.3ubuntu6`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.3ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.3ubuntu6.dsc' base-files_13.3ubuntu6.dsc 1621 SHA512:d0bc3c7db2c00c2b19da8653acf4b96979dc500356134628cca641a49529d03d08aae088ec5e73464394853aa85843a36803ec5b149e9b637ad5a737a469e4c3
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.3ubuntu6.tar.xz' base-files_13.3ubuntu6.tar.xz 93652 SHA512:8519f1cc09c370de707b4fe81eb45124288b9106a60d1afd4c5800a615f9dc26e9be208c3dbaf07853491b2e3540f3b7f5ffe95219940c2ba373e44ab5b62bcf
```

### `dpkg` source package: `base-passwd=3.6.4`

Binary Packages:

- `base-passwd=3.6.4`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.4
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.4.dsc' base-passwd_3.6.4.dsc 1762 SHA512:1b2cd7f6964ae4bbbd8758a2d3af5a0953db6f5ef7ef11df7d9392133d7502c631bb406b6717211e45a3307118d84a2aa698d3a8543262350311076cc52919c8
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.4.tar.xz' base-passwd_3.6.4.tar.xz 58420 SHA512:de03afddf8efe777d7682c718f8584edef9f2daf8abd010ecefe27ca687f2d0b648894b0c21fd03a2ec96b339884cd790f2bd2cd0377b1fb4bc63b3d9367ef38
```

### `dpkg` source package: `bash=5.2.32-1ubuntu1.1`

Binary Packages:

- `bash=5.2.32-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `BSD-4-clause-UC`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `Latex2e`
- `MIT-like`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.32-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.32-1ubuntu1.1.dsc' bash_5.2.32-1ubuntu1.1.dsc 2408 SHA512:ec9ac448a9830e0ef7ee72402ce4fb2396d944e51540158270c64a386a824a69dac56a9f5062e8848dbddd7269b7cdda5a0052a1f0e424a00bb7a5a7b813edf2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.32.orig.tar.xz' bash_5.2.32.orig.tar.xz 5598292 SHA512:99035c3769f834209ac5087530e6a5ea87ee69420041147a538ec7896b9ded6ec77a1084032c150ab823769f8dc5392918c11eb22e5acc74a15ab99bb4827fcf
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.32-1ubuntu1.1.debian.tar.xz' bash_5.2.32-1ubuntu1.1.debian.tar.xz 95300 SHA512:08e2bb22514391e791eb0f9abfe4d0756289a669ad2430f3ddac596a65932d0d8edfc62b0b8a8b03b861233a622cbc4e004944f29047e01b5854d516a037972e
```

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.dsc' brotli_1.1.0-2build2.dsc 2401 SHA512:74b6f53c8917622cf69f3a5ec7d2032a5ffaf3673700efa7c0f1a095280024a48bee2518c17329d0d23a0c54d1868d0fa247e663aeca9b4587883b5f88eea1b6
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.debian.tar.xz' brotli_1.1.0-2build2.debian.tar.xz 5644 SHA512:d7f430be5228cfb92ccc2908b915ab817d6165291671721112c1b5511949e92a2bfd1017f7ad44afd00fa0a133c3724c02e9d22f81e2a726d9958bbdae9f44f0
```

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA512:ff346848f80a2d85266e27db27289e126ed016b0ee65f777594e92be388c9f76010419efcbe93dc1d5dde7fe356ee02e797e3579687252b0ae8f4152a245dcb2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA512:29a0df15aab88f4df3e4b3e13a04a428bae850b251d4b70541896b93fe28bce3397f9a7c5e3b251c81a8abd3e0a7911d31f546c1fe30a28c764ded587462831c
```

### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA512:3cd6d9322800a3469be7dcea1136daa0f9311ae148b258bbf6689d5992f4dda82351fba34d52bc07c505bf407f3f4feb4e284ecfc2fec18bb1c23b1652b98986
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA512:e9d7b5283c2be9425d18eb4a9b54b1fa54db0b9d1bdb28f9c6db7f8b2e03fd93442ac973f9b024b7a148d71ac2789edbc1207c2048ce4be589eb1a5376640670
```

### `dpkg` source package: `cdebconf=0.272ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.272ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.272ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.272ubuntu1.dsc' cdebconf_0.272ubuntu1.dsc 2873 SHA512:8d255383a565c2c1c7668147200d260d7af268003adff1291a86f8ac0f1a43693c08d16c6a118106bc9aef8d3e634431541e10b17d7dcb027fde43339da4960e
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.272ubuntu1.tar.xz' cdebconf_0.272ubuntu1.tar.xz 285752 SHA512:87c3147cb549a2b93047946a709149e9ad00830b9beff11fb5b628a4fa6d5bf71110bedc2e51b087f31f33f041d4de641c2c3720f14209758b2cd06616d543be
```

### `dpkg` source package: `coreutils=9.4-3.1ubuntu1`

Binary Packages:

- `coreutils=9.4-3.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris coreutils=9.4-3.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3.1ubuntu1.dsc' coreutils_9.4-3.1ubuntu1.dsc 2030 SHA512:72c7e1f1a4fb1fac35f5d65c25f8abd40e911858dcc113d22442cd34648f8e9dc30b2bd46aa119b4f4f6cd369994892773cca60f71cf437e7271cf1078d97dbd
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA512:7c55ee23b685a0462bbbd118b04d25278c902604a0dcf3bf4f8bf81faa0500dee5a7813cba6f586d676c98e520cafd420f16479619305e94ea6798d8437561f5
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3.1ubuntu1.debian.tar.xz' coreutils_9.4-3.1ubuntu1.debian.tar.xz 40568 SHA512:939dae986661ba1d70f98b7645fb8b3dab013880f7f958908de1582baa11e43710a8fbbe75c2a7b2e4a6a8d71e95bb149c4312fb7b21b177e07dd5d46c3c7f36
```

### `dpkg` source package: `curl=8.9.1-2ubuntu2.2`

Binary Packages:

- `curl=8.9.1-2ubuntu2.2`
- `libcurl3t64-gnutls:amd64=8.9.1-2ubuntu2.2`
- `libcurl4t64:amd64=8.9.1-2ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `OLDAP-2.8`
- `X11`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris curl=8.9.1-2ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.9.1-2ubuntu2.2.dsc' curl_8.9.1-2ubuntu2.2.dsc 3043 SHA512:2f0f2544ecf8906a3e70cbc01ccc966fa0cb30081b67ab4f80f1011102c65830bbd8d0d61939ea94519694f4d06490959e512ba28ae2cc3d98b03f855f6c19be
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.9.1.orig.tar.gz' curl_8.9.1.orig.tar.gz 4200000 SHA512:27c91a58f23f02dd150556edaa73e1be08a93134d3d05049e546b39f05e0f4383e41bf6a56a643eae03eda0f39a527059510b2e34167ae9e7c75b393964a9f8b
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.9.1-2ubuntu2.2.debian.tar.xz' curl_8.9.1-2ubuntu2.2.debian.tar.xz 61448 SHA512:0af3c3a69a04643dad542710e226b82fbd3b5d4c9cea6897120c7cb45919a8e67ca5fc61f3789e6f48e9d8295f5aed913cd9f654c3e38aa7b50fd1e6a6aa41a5
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-8`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-8`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-8`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-Clause-Attribution`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `RSA-MD`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-8
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-8.dsc' cyrus-sasl2_2.1.28+dfsg1-8.dsc 3223 SHA512:d6124e5103fd9805ec71367388a3bce620d6b79aecd4a4bc736c6ec3b9cd7ccbe187885e4f73dc6ea4185eaef3240b6b2a76e576c00a236b4ec64023f4d82cbe
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-8.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-8.debian.tar.xz 98980 SHA512:f0ea152db46ca638c3606dc525a914edb110f1c56b1fcc6a8a7073317d720059dc7669a58240ba2e771eecf7763de3a69990d5febd0ede925e789d5dbd2553c5
```

### `dpkg` source package: `dash=0.5.12-9ubuntu1`

Binary Packages:

- `dash=0.5.12-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-9ubuntu1.dsc' dash_0.5.12-9ubuntu1.dsc 1882 SHA512:bda472536c900945074763859bff26bb62d810ebe7d8809a7694c69ef006c88dc61cb43ba3a2d0f24b46b8748237ec8a84bfbf7c5a6cbbe692a77bbb044a270f
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-9ubuntu1.debian.tar.xz' dash_0.5.12-9ubuntu1.debian.tar.xz 40704 SHA512:59e306a5099a212252125907d1081c0e364e9a3989d65bfc4fc2e62d67079750345d2ccd96879b2a0b34bda70ba1b974311a1e6b965361848c2d8ccb88762bb4
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-7ubuntu1`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdb5.3t64/copyright`)

- `Artistic`
- `BSD-3-clause`
- `BSD-3-clause-fjord`
- `GPL`
- `GPL-3`
- `MIT-old`
- `Ms-PL`
- `Sleepycat`
- `TCL-like`
- `X11`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7ubuntu1.dsc' db5.3_5.3.28+dfsg2-7ubuntu1.dsc 2481 SHA512:9ba9efbb4b592e7e48345c2be1fb1187a548d3e0acc3aada561aba42493bfbb6a3a7a9fbf173f7047725f64d61f0ec704f1e30d22c4f88e6f531d10151f961e0
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7ubuntu1.debian.tar.xz' db5.3_5.3.28+dfsg2-7ubuntu1.debian.tar.xz 35772 SHA512:6d7c4f84f212041bbb211d1426d203915ae4e0b4935fd095d9a237bc00f0f430aff5ae7e6aba77a5d37946170e6be59e772a9cb25678799a67bbe14dfc8ed7f1
```

### `dpkg` source package: `debconf=1.5.86ubuntu1`

Binary Packages:

- `debconf=1.5.86ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.86ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.dsc' debconf_1.5.86ubuntu1.dsc 2030 SHA512:d06dc6bfa5e60ddb38839b25437641dcbd06acabc59dfa46955db87bf47370b381906916bde881de51a8dc4beaf1be9c3288bb25292718e608077c755a491988
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.tar.xz' debconf_1.5.86ubuntu1.tar.xz 574112 SHA512:e63b3d4241e8b347fcd71f7ae838e6b0c40123bea65298a9492ae6dabb24e54d31176c11a8b1870edb5a96ea346080d2f9ca8821cef74e73f20c03265aafd95d
```

### `dpkg` source package: `debianutils=5.20`

Binary Packages:

- `debianutils=5.20`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.20
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.20.dsc' debianutils_5.20.dsc 1631 SHA512:34c1a006fb3eca4b86e7fbf9284ca1aaaece6e6681f6f4d90308bc66b4968df341143a09f06d69b80279fc3d0217d16d9fc44382214ef88fbda141e083ef65ac
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.20.tar.xz' debianutils_5.20.tar.xz 80776 SHA512:a16a2312f2c16ff5fd8809c8b06cbe97518b56b5ffeb6185275f331855defb540cf3b982602d3c6e572a3d1dbeb92ae21ce9794373aa1b70498e8a0a55a3a4e8
```

### `dpkg` source package: `diffutils=1:3.10-1build1`

Binary Packages:

- `diffutils=1:3.10-1build1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with autoconf exception`
- `GPL-3+ with texinfo exception`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3.0+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.10-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.dsc' diffutils_3.10-1build1.dsc 2192 SHA512:60bfa2bb6c9316393e21d03863c0f7a837280bccd4bf20818ca6bc749328172f4dd433603c231d5ce17b6ed68d4070c7e5037546a94f71d8bc50b81578b9645f
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.debian.tar.xz' diffutils_3.10-1build1.debian.tar.xz 14068 SHA512:36cb15f987cfd57dbe5bfe347a990887ffe52f8ba3756c4f806e78ba702d2b1acc2f316292bf1096a1a7db158358b4cd6261cabe70a77fd292945e07d5808cb5
```

### `dpkg` source package: `dpkg=1.22.11ubuntu1`

Binary Packages:

- `dpkg=1.22.11ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.11ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.11ubuntu1.dsc' dpkg_1.22.11ubuntu1.dsc 3152 SHA512:e781099099c7dfdad9b31864514eca3cd2f39fe6408ca8aa873faff964d4325c5685853faf55d22704be020259fd4f1dce8d5ab78777dab7e7aaba7efdf5448a
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.11ubuntu1.tar.xz' dpkg_1.22.11ubuntu1.tar.xz 5553236 SHA512:2b7408a142e267d400af39e902f3a74adbda391e991ddeb812050244a0a958ac3065d38054bb6d52419daa28c13934dce926913a5cac9d4fd28dadc4e79d922c
```

### `dpkg` source package: `e2fsprogs=1.47.1-1ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.1-1ubuntu1`
- `libcom-err2:amd64=1.47.1-1ubuntu1`
- `libext2fs2t64:amd64=1.47.1-1ubuntu1`
- `libss2:amd64=1.47.1-1ubuntu1`
- `logsave=1.47.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1ubuntu1.dsc' e2fsprogs_1.47.1-1ubuntu1.dsc 3193 SHA512:2c2d22af2bd4832646950d5817f0414ad18c095ff443ac1d1b46144a1366271d188f6cf4542d724f7ec9bea978989ed02385935d35753e1fa03278a0ee8097eb
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz' e2fsprogs_1.47.1.orig.tar.gz 9952468 SHA512:da4f3ad764774e0e7709b0d3185da325fb0b51026496c668c9000881324439dc675f146bdd042c10aa06a557d791102b54c40763be07952fc2acc7c5b8008550
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz.asc' e2fsprogs_1.47.1.orig.tar.gz.asc 488 SHA512:8c8565b37330133319ab817d1ea16fadddbe162fab1dfa3706603a58bb6e4947b090fc938636dc1ec04337a334743ce91d5ba31bdca81f0001fa785e195aec27
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1ubuntu1.debian.tar.xz' e2fsprogs_1.47.1-1ubuntu1.debian.tar.xz 91684 SHA512:e68352288ac29bef8283e23e9859939408972b1730e86932be35b6e40cc1921c68f3716203dbfed51b34ac504bd215bb9f3a31fee7a45d842ff40636db5db33e
```

### `dpkg` source package: `expat=2.6.2-2ubuntu0.2`

Binary Packages:

- `libexpat1:amd64=2.6.2-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.2-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2-2ubuntu0.2.dsc' expat_2.6.2-2ubuntu0.2.dsc 1474 SHA512:f10fead65ceba608648188d5eea4387f47160abc5aed066f5eb06baeb06ae40ac01423de0e4764ad8f3f7f673a5c0c64a36923e3779914940ac8bd88d842bba8
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2.orig.tar.gz' expat_2.6.2.orig.tar.gz 8416128 SHA512:49b6be12bd6284106920abc61d86d441cba126615fc4019744fc56dc5e7c5efc72b02c09e5c7b491882a633c1c45dc4a03e92a96372ab62bcd70755f6878c6b6
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2-2ubuntu0.2.debian.tar.xz' expat_2.6.2-2ubuntu0.2.debian.tar.xz 28688 SHA512:37ca98eec42a7be35a009b2690f7093584437a8cecd212504a0e2736c6e07bbaba8ad49611f7a126550edc87d700a40eae1fb95b4cb7f59b100afe0b9a7a0848
```

### `dpkg` source package: `findutils=4.10.0-3`

Binary Packages:

- `findutils=4.10.0-3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.10.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA512:7a651b7be4777d486eee6fc81ba656734e7952a1adae79c3c5d6a5f02441fa04841026dbbd3d9f2d627f4c627d7e0c54c6756e2ffaf3ba47222be3671c81d73b
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA512:b8b683d21cd26c6da4f41c56e83cadbda4780f8610a2bbd4b4e34bb1f339c3209721974b03e076d5eef0331fd876d947b398197aad37c29bbcc2e0405c641b34
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA512:a835153a0671309021be187bf78afee58d9682acb40545aaa9dd187f0ebdea0cfa5583bd03f363243633ea056ddb0a7a6603987ab5e34a608426cb4265ac6d8f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA512:578c4fa152b39e0e0b9d5ab1ea146889ae53cb623d01f84a93d0ba936c9355b2bc5eb20bd761e5638226a040d131edaba60cc573bb3ef4f04889cd5067d167f5
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2`
- `libgcc-s1:amd64=14.2.0-4ubuntu2`
- `libstdc++6:amd64=14.2.0-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2.dsc' gcc-14_14.2.0-4ubuntu2.dsc 46712 SHA512:e3ce301f697617fa271690ad68e11bad99effea78a418b44d0e861cd24acf5587d2a1ef4ac599d6b5a4d1c47c47b2ab67b58fdeedc233d05d391f19e8978d89f
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2.debian.tar.xz' gcc-14_14.2.0-4ubuntu2.debian.tar.xz 1950228 SHA512:dfd6ea9a7bb3459815086092639a99f0ff55f0d0880f82ba36835a91db44ba7d118dbafe8626a602312a7e7ac3a9a54b1b34aced21d9d6a1d4f424d4d0b15dcd
```

### `dpkg` source package: `gdbm=1.24-2`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.24-2`
- `libgdbm6t64:amd64=1.24-2`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.24-2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.dsc' gdbm_1.24-2.dsc 2466 SHA512:b25a2656224dc0e7703375a50cb58cb3cb8b63f89a3a2c2e749b96fb40ae989f06a169bb0655dddecbe3e39fe856e8f22022c0b253d9dca303475f4361541dc2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz' gdbm_1.24.orig.tar.gz 1195931 SHA512:401ff8c707079f21da1ac1d6f4714a87f224b6f41943078487dc891be49f51fd1ac7a32fd599aae0fad185f2c6ba7432616d328fd6aaab068eb54db9562ff7fa
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz.asc' gdbm_1.24.orig.tar.gz.asc 195 SHA512:c39d91aa6dee98851eac16b27a192300dab9545cff5e441d66a55a0939f1c6bc9e5ead0e96a48ef941f69d586b34d78e786d262d65e3b13ffe2c4f372d823fd6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.debian.tar.xz' gdbm_1.24-2.debian.tar.xz 16880 SHA512:bb98e8032f57a1dc33d34004e6b748a859aa465bd9fd6a592abe6d3ca09eedfebf05fbf0245d5c4eb01560ee0998f16016cd85ebc3367c25713795a9bab97a0f
```

### `dpkg` source package: `git=1:2.45.2-1ubuntu1.1`

Binary Packages:

- `git=1:2.45.2-1ubuntu1.1`
- `git-man=1:2.45.2-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-3-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.45.2-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.45.2-1ubuntu1.1.dsc' git_2.45.2-1ubuntu1.1.dsc 2927 SHA512:8beb00ad1b65de18f74af78b8e547ef68857e87ba905e73fefb0f342dea769931859c81e74a240322c7aecdc2536534197181d3b2b8791d2b9e7a378804d9040
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.45.2.orig.tar.xz' git_2.45.2.orig.tar.xz 7487680 SHA512:dce30d0d563f3f76ef49c8dc88105e0cf0941c8cd70303418d9d737f840ffba36bcc575c380c75080edf64af74487e1a680db146ec5f527a32104e887d4ceb73
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.45.2-1ubuntu1.1.debian.tar.xz' git_2.45.2-1ubuntu1.1.debian.tar.xz 785768 SHA512:9e83f26644f086ec61f8144105098e791b7cdd43c147d2bcf072344485f9e9d70016e69b4190b4c5d50e20013f788f76de8734e5fa1a073d684d3f41f3e068c5
```

### `dpkg` source package: `glibc=2.40-1ubuntu3.1`

Binary Packages:

- `libc-bin=2.40-1ubuntu3.1`
- `libc6:amd64=2.40-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.40-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.40-1ubuntu3.1.dsc' glibc_2.40-1ubuntu3.1.dsc 8090 SHA512:fe1e921111a5678bac2b0d1879c6dce8438a2d2f01644f3dcaaa45e52106805e006b9f459c680c9ee27b2691347f9a05b23e0603641a12d77449383660968ed5
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.40.orig.tar.xz' glibc_2.40.orig.tar.xz 18752204 SHA512:33caf91dbfddde6480b7cdf7a68b36aff8c522bfee56160af26af297f1b768668edb08bc4e1a7ff61c64721e3c1d49c347a5dd01c5edd3b914ee6479c8b27885
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.40.orig.tar.xz.asc' glibc_2.40.orig.tar.xz.asc 833 SHA512:c38a5d11b6d9272966e8e6492fe8c92ab75cd3755189f8f768c038376a4f3c83fb07b3d671fd31cd327f65092554ca412f85f94c896abae78b6d255e93026163
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.40-1ubuntu3.1.debian.tar.xz' glibc_2.40-1ubuntu3.1.debian.tar.xz 440996 SHA512:ea0162489b0c95c4337fa0dd245da348ed470f5d847c09b0f1ef2a7cf20aca617d22ec610a76ffe68c0198070345eb4f30651f7742fe116b221fcaa17cfc0c2e
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu7`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu7.dsc' gmp_6.3.0+dfsg-2ubuntu7.dsc 2337 SHA512:fbb79b31b3a3ee6955474176f16b8843d8608d8f0f76c7938f2f04bfe2c9af7424495b5a1d9e409103a7f357fd09ccba83ffd3cb58771ed0e544e64f95b10ee7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu7.debian.tar.xz' gmp_6.3.0+dfsg-2ubuntu7.debian.tar.xz 38872 SHA512:8716e62bee58fed0a6221147cf4c29b856305bcebb1b95b273853d4d7ba6f6e77aba170fad385f5f3bde8f5bd8ebd01698e2b55afa0679290c0f318cb23b9c04
```

### `dpkg` source package: `gnupg2=2.4.4-2ubuntu18.2`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu18.2`
- `gnupg=2.4.4-2ubuntu18.2`
- `gnupg-utils=2.4.4-2ubuntu18.2`
- `gpg=2.4.4-2ubuntu18.2`
- `gpg-agent=2.4.4-2ubuntu18.2`
- `gpgconf=2.4.4-2ubuntu18.2`
- `gpgsm=2.4.4-2ubuntu18.2`
- `gpgv=2.4.4-2ubuntu18.2`
- `keyboxd=2.4.4-2ubuntu18.2`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-2+`
- `GPL-2.0`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.4.4-2ubuntu18.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu18.2.dsc' gnupg2_2.4.4-2ubuntu18.2.dsc 3947 SHA512:870669b3e40971c095f33dd87ce537406b171c4d90205f2936335927174b99e90a84bf5d4371a9df4d8b82c4bdc16097c1057ae9f35081a0888760525a69211e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu18.2.debian.tar.xz' gnupg2_2.4.4-2ubuntu18.2.debian.tar.xz 95968 SHA512:56fe06a128de1a4e98c1daf6cd4097dde6399387772d2bb68f78ef80d2cb510de65a71b98de7387fcd200e13910b7eff00ad3c3d1e3696dc586ed330489da9e5
```

### `dpkg` source package: `gnutls28=3.8.6-2ubuntu1.1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.6-2ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `GPLv3+`
- `LGPL`
- `LGPL-3`
- `LGPLv2.1+`
- `LGPLv3+_or_GPLv2+`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.6-2ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.6-2ubuntu1.1.dsc' gnutls28_3.8.6-2ubuntu1.1.dsc 3384 SHA512:93a483a6e0f6e60a36818466369b695e51921d4a99f87d8a7f0c07af262743b2c12e6294b3c132fe00374a94b24a5f5ec6d85ea00c25e21dc47c8a8f782059c5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz' gnutls28_3.8.6.orig.tar.xz 6517476 SHA512:58631c456dfb43f8cb6a1703ffa91c593a33357f37dc146e808d88692e19c7ac10aeabea40bee9952205be97e00648879e9f0fa80e670e8e695f8633ba726513
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz.asc' gnutls28_3.8.6.orig.tar.xz.asc 228 SHA512:37959932cebdcde588b81ec5ec1eb5c4f7355f5dc9cb68fc6e8804c4a357006f33de5b6eeca5bb5a8cc3350ef1ebdd428ca7d1decfd790097cbd636bd78bea2d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.6-2ubuntu1.1.debian.tar.xz' gnutls28_3.8.6-2ubuntu1.1.debian.tar.xz 87680 SHA512:4204183b578e7379005f5fb4adeb6295dc8cad08b32402cc75a7337102c87fa12456fbaa144b82705bf0fbda10a03553c533060319d7860b9731de5de4ee033e
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.dsc' grep_3.11-4build1.dsc 2379 SHA512:5106f25775f36ba92fd7d73634d8c271fcea7dc9defef2f84d6080eb6a47dd0b1194272807267413807aa35d945c9bb66f076162d3eba539cc35eca5d255d2f9
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.debian.tar.xz' grep_3.11-4build1.debian.tar.xz 20584 SHA512:212c903c240071dda1d8e966991908730af26746558078262aa32b6b0683487cb510d9b9a2c40cafb31024e78e2c74d17eb5681e329aa142b0921b88cacef7eb
```

### `dpkg` source package: `gzip=1.12-1.1ubuntu1`

Binary Packages:

- `gzip=1.12-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1.1ubuntu1.dsc' gzip_1.12-1.1ubuntu1.dsc 2042 SHA512:abff305a668518406b9e8735383619adcb1a3d6dcff7af970d44a6bcc246decb943af6f6a3212eee552ccdbe9fc5a5de4e98ac9590edf0b189f70974b51d1188
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA512:116326fe991828227de150336a0c016f4fe932dfbb728a16b4a84965256d9929574a4f5cfaf3cf6bb4154972ef0d110f26ab472c93e62ec9a5fd7a5d65abea24
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1.1ubuntu1.debian.tar.xz' gzip_1.12-1.1ubuntu1.debian.tar.xz 20444 SHA512:bbc816852faa8f0612a156af76dbc6ce58c043aa3581146dfadf2519b9e6a50f5766357520dd4bed49749300eb6c51a443cbf539edf12f56b62390ff84522350
```

### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.dsc' hostname_3.23+nmu2ubuntu2.dsc 1567 SHA512:a61538c601492aaba10aafc2b181f3db3f7f0ef768ce5fe4da1c4dece8655247627a77df89a7700938c665792cd134a46bfa8dd20ae59e7d0ccc199bd43b06a6
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.tar.xz' hostname_3.23+nmu2ubuntu2.tar.xz 13276 SHA512:ce7606f7bd3be9a2a2089955c1510244c8b5ef76d9e1978547870f2ff6e5fbb6cd12c040f38dc5473c46a2d77e7e7257da5787638cf5619adcced206c2c34419
```

### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.dsc' init-system-helpers_1.66ubuntu1.dsc 2353 SHA512:f6aafcef04d63b54d6ff273312ff2a9194345b8725bfbbaac69793a3d016cbda730f2de8de9862d8038c36ca0fba39b868d6d640701ccf8db417094816d0e9db
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.tar.xz' init-system-helpers_1.66ubuntu1.tar.xz 45100 SHA512:222f73347b0ce9eb137c8ce5dc36e9fedbc8dc5ed3f1fde7fbf52258a5437d0a10d3d610ca1d1b206646bb92a5355d1061705440b2d22d9109b5de6d1cb92e98
```

### `dpkg` source package: `keyutils=1.6.3-3build1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3build1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.dsc' keyutils_1.6.3-3build1.dsc 2211 SHA512:8a40b63e5c4ef4ae645ffdfc865ed91192a7dfc65c8271e59388e63d867b43ac0da90ca1f5e85682886e4561681b83f3bf8bc6a3d90f205dd0feea116f7a30b8
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.debian.tar.xz' keyutils_1.6.3-3build1.debian.tar.xz 13456 SHA512:ef729447f8f4adebdb986d115e227bd908b346e26115eb7a0385a084ad69f6772c914744d8c24928587247cd5fc329ed1305e9b006db276d0445b9614f20603f
```

### `dpkg` source package: `krb5=1.21.3-3ubuntu0.2`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-3ubuntu0.2`
- `libk5crypto3:amd64=1.21.3-3ubuntu0.2`
- `libkrb5-3:amd64=1.21.3-3ubuntu0.2`
- `libkrb5support0:amd64=1.21.3-3ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-3ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-3ubuntu0.2.dsc' krb5_1.21.3-3ubuntu0.2.dsc 4101 SHA512:7161efd7e01d2ee072312e5f6638e9d27d84578696e97352f5fa23abca9162f4c9897699e7a9eccd1499e7ea3392473a53b3f1a97df94e2edde76efb103e3f31
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA512:8992a5f5247315b9846aa73be4ee1ea223c0231a52d5c6c28718b1f3e3b45d62e2dad4aa5543a83163d1369bb79886b6c1c22766f22d8aa2f6b2575c54d0075c
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-3ubuntu0.2.debian.tar.xz' krb5_1.21.3-3ubuntu0.2.debian.tar.xz 110884 SHA512:ccf948bb0cd6a3dfe2ee15d5a1a55097c5707a1e445fcf1a73ba2558b976da8be85aa903f66948f46aef5fcae8ec477e0e4eb36405b89824bb633a0b188977d9
```

### `dpkg` source package: `libassuan=2.5.6-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.5.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.dsc' libassuan_2.5.6-1build1.dsc 2734 SHA512:5a430eef8b98b19d7750ab96717a36749fd586533290ae3ab0129d4d7236f34c524e5fcdb7cc1105cf1fa16c64f604956ef36af0eb952cbf1308b61819364f57
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA512:dcca942d222a2c226a7e34ba7988ee0c3c55bd6032166eb472caf2053db89aeeea7a40e93d8c2887c7ee73c5f838e8b0725e8cfb595accc1606646559362f7ee
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA512:aaa1222607320c260d7339a95cca6532947782520b07df3198a5a228129e0247b87f6f3b6fea17590147fbc7345ea36bfa8da45116d3d85c6fc2d4a3df0f629b
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.debian.tar.xz' libassuan_2.5.6-1build1.debian.tar.xz 14412 SHA512:a09775ff7ab780566ec1385cacb7dcd34b8b418f4472b5285b57d442ab21a4482fa720c43fdd81dda7e042300ff7ff97efa0bdb0ebdf7aa29d71b83ae3ee7b00
```

### `dpkg` source package: `libbsd=0.12.2-1`

Binary Packages:

- `libbsd0:amd64=0.12.2-1`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.12.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-1.dsc' libbsd_0.12.2-1.dsc 2347 SHA512:cd7e00ee592505a8b23a7e189ae22417ee000e7e02e12baf660672cd0597cb20c14a5f6a53b158daca50f7fe429c7116c4604078428de3a12a32029efb1303c1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-1.debian.tar.xz' libbsd_0.12.2-1.debian.tar.xz 18612 SHA512:3dfaaa774bc8154c5d0fdbcad1058ef0e33b3855c1fc27c29b9619ebd8a66aac2e28941e9e244af27597cc82fdb3f6664246405e07e2a8c77f78f519bf96a3eb
```

### `dpkg` source package: `libcap-ng=0.8.5-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.dsc' libcap-ng_0.8.5-1.dsc 1638 SHA512:1f0d54585a1625a1aeb7f0efc7fc473731cbe4c145ed09b8b697d0709f9a067a070b178e8ed195c39fd86a2985b12badc72207a5985cfe86ea90fbae566e0445
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.debian.tar.xz' libcap-ng_0.8.5-1.debian.tar.xz 7400 SHA512:03ed0abdf93156de2ba4a5456eb0de8bb256b59bef51a627b805a7252506e4e643f6e9da116ee1a2a4510101f786c0ffae98669032a474c44f0b8b4bd1e3cdf9
```

### `dpkg` source package: `libcap2=1:2.66-5ubuntu3.1`

Binary Packages:

- `libcap2:amd64=1:2.66-5ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-5ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu3.1.dsc' libcap2_2.66-5ubuntu3.1.dsc 2319 SHA512:4f96df69825fb15dd35e710d1c207b884344a02e8a105168d051d2b7863e39cd1d2f8297c04561f4e92c0eacad249be513b21313f4af5ef91597b799aacdad8e
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA512:ac005b622f6e065f30ce282a5c87240e7b9da75366ee537aa4835bc501b44bc242c10a4ba4dc070e2415fc7f635d1c3c4e45fbeeaf962cf7973dda82bf6377f0
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu3.1.debian.tar.xz' libcap2_2.66-5ubuntu3.1.debian.tar.xz 23068 SHA512:131396bcc66de6364a5f86ec1c182ae7fac700bc5196fb5da7acca7a42a1cf2ca40bb2b7f69d032e6dc6490323a8efe37e1241b0c0035cb207f4551ad6762680
```

### `dpkg` source package: `libcbor=0.10.2-1.2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-1.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-1.2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.2ubuntu2.dsc' libcbor_0.10.2-1.2ubuntu2.dsc 2283 SHA512:69f6e793bc9fc1a23f298a3738fc2d810b8aa243c2426347be18d9bebe7a6b0c7b82177545ec0bb4cc3deb5932228e72576c03026da0d5fe95f34b034ebb0bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.2ubuntu2.debian.tar.xz' libcbor_0.10.2-1.2ubuntu2.debian.tar.xz 6560 SHA512:d42dc2b89e3af8c1b65c3d227f1c98a2025f620645052fba062c9bf415830970ed4b3ed47878d5de316661201dafbd69c6c30bb3b40e242dc0b6738df8e6323b
```

### `dpkg` source package: `libedit=3.1-20240517-1`

Binary Packages:

- `libedit2:amd64=3.1-20240517-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20240517-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20240517-1.dsc' libedit_3.1-20240517-1.dsc 2264 SHA512:62667a607c0e9cda35c9b7b3d4942c105da2bd72af85621a0c7c58b66464882c1743ca7a00066a49a946a5cd88f0572a1329fc358a359a1559e489ea14b287d4
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20240517.orig.tar.gz' libedit_3.1-20240517.orig.tar.gz 534690 SHA512:bc17371eeb8842b93cd5ed7ce3a04aa1cadf26aa697d92e3440f9f729a4d0631eef60ea2c96844ff773e1b3b80ae518fd3ae684126373dfc69b65d67a0f25e90
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20240517-1.debian.tar.xz' libedit_3.1-20240517-1.debian.tar.xz 16700 SHA512:2e0fbb0cc282c5e98977d7fcc2f10f00d31a1f1b2c927658a073cce1a9e20390d45ad180a81424000da50fd9fda60da1960f835645f724bec6c271d659a2d93c
```

### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17029-2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.dsc' liberror-perl_0.17029-2.dsc 2085 SHA512:9b469f24ebdd65c5aacfa41b7099cb1fec5214d98e6e0d793d55a56bc0f0edae8f2ad3c0e09f44558249ff5456f05704c213d7e84661e0e4d774e644d3fd405a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029.orig.tar.gz' liberror-perl_0.17029.orig.tar.gz 33304 SHA512:266ba1feff897c1d162e69a83e595cb40da9a6e1d8b10cc5531626eff392c6da94be03ba722c74827fc2ea0d9d1c1e62e824d9021e098b700db65dd0b3acbd0a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.debian.tar.xz' liberror-perl_0.17029-2.debian.tar.xz 4608 SHA512:beb596444319797a60470e98c14e8e736fd5be9c307ba5482fe96bf77c1382603b1f2a58d68406ecbf2bc5469cab4654645f5469cf059336fef24605b235cb61
```

### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.4.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.dsc' libffi_3.4.6-1build1.dsc 2055 SHA512:21cc7b6880fac7c143e88a81c47e5144d38bea3fd66f71182d1408f56bfc6801d39481638e04c02bb29dfc2429e3d968b65591cf95d20cfeca6769684d3c86ac
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA512:cbacde8911aa6a9fae5c0a8d5959221a25bf8a3310c44a7f4ef755e6676f5226b9f2d1c6cfb36c117ebed10d379aa24b4b7516c3e0dca3bf73f9439057463eb8
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.debian.tar.xz' libffi_3.4.6-1build1.debian.tar.xz 10736 SHA512:432e6e7ddb9aecca508f982293112b2bf86f5da2d6d646437b10b2857dadaf2c8aecb1646d2e592c259df26a5240f69cc1411155cbad8c3d942748d6856e587c
```

### `dpkg` source package: `libfido2=1.15.0-1`

Binary Packages:

- `libfido2-1:amd64=1.15.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.15.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0-1.dsc' libfido2_1.15.0-1.dsc 2585 SHA512:d2f279927ea33d6f7b5d130d5058fc6fdb3f905ee51618e4f421d46a6fb7e638986987e7974483b67fe2bd32bb12607fe0adf7130d628ba5ec6f93c576e1c682
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz' libfido2_1.15.0.orig.tar.gz 670019 SHA512:cca142e3b3b7e216289934785fcad6be3bcd344001445f04fcecf01d4f568523b949c7204eec2f32faf12605a98c7496b9f64bb34d6a312342fa997689e61635
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz.asc' libfido2_1.15.0.orig.tar.gz.asc 228 SHA512:577f592b236e5182d92b7790600bd038b0b0019a7db0efada77e7af3ec04264fdb51cdb00ff5a32e68ca478951c59646b786c57a124932d43410e37a672d0fd5
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0-1.debian.tar.xz' libfido2_1.15.0-1.debian.tar.xz 52960 SHA512:574a8032af24a5c17669a4493ef75dcc787fb6a10cc233a875cda80269089d75f9001421a1625a17ba375305fcd597fe1ec76f82c39efea4697d7f1d6b3b89c3
```

### `dpkg` source package: `libgcrypt20=1.11.0-6ubuntu1`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.dsc' libgcrypt20_1.11.0-6ubuntu1.dsc 2984 SHA512:4f63db3009d6a91aa989f0b8c45d1a6f722f89f99829b464222d1fdddc0c1df383cf6403fedfa9739637f219b9756f11a4c4c245fe42908968af8b7701fc844b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA512:8e093e69e3c45d30838625ca008e995556f0d5b272de1c003d44ef94633bcc0d0ef5d95e8725eb531bfafb4490ac273488633e0c801200d4666194f86c3e270e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA512:eebd4c599bd8f375445566c3c73df5a223f256cb650cf18d8fed033a1f13a1fb8b9b10a17d686be21ad2bced60fc8e27d71b07e5f556a854a893e44c5dd81ae7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz' libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz 39784 SHA512:d7cb33ed130ba6de0339aa1030a13a5e272a2d43f26f9922107d1699f0c339c968aa538c014b817e8a2815141be2e2147deb7f0d3402be99ed256c14f621b105
```

### `dpkg` source package: `libgpg-error=1.50-4`

Binary Packages:

- `libgpg-error0:amd64=1.50-4`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.50-4
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.50-4.dsc' libgpg-error_1.50-4.dsc 2935 SHA512:be18a7403134fc9fa082da5e2fd6c1ce4dcab39469b7b057d60349a3b6696e6472db87e7f1093df0c1b26289783822439c8e11cb9f69a50b65c3a75a8798e0ce
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.50.orig.tar.bz2' libgpg-error_1.50.orig.tar.bz2 1082003 SHA512:96e466d892a50843af6d7c08c0da602518bc6a28836bfc35f0a28cde74d368f57c5c70c65f0f41edb4fc1ca5ebd00f2ece531d8b3eb1bd6db566adbb29bc61ff
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.50.orig.tar.bz2.asc' libgpg-error_1.50.orig.tar.bz2.asc 228 SHA512:639678e99a7252753271dba90c5ad0fd28ab7a9f23e9328e9fcabb87eeb6db4072df504553494e68da5fada1e9ccc6c725acc7eb620d59cd007cc8f69d448bcb
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.50-4.debian.tar.xz' libgpg-error_1.50-4.debian.tar.xz 19640 SHA512:206decfde32ec1d2fe59d767805f17471977d14e6ab5152900d4a2e03792021f3c7efcc903b20b6af743007779a61514e9baf11ab4ff74b6ac7eb72f11b44659
```

### `dpkg` source package: `libidn2=2.3.7-2build2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.7-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.dsc' libidn2_2.3.7-2build2.dsc 2643 SHA512:0c8575d0c7ab0ebe6bc8dfd3cbe966090f074793d7a91a11fcd7e5bcb0939c4d5cbfd25917396baf523e2a2d334b60e38774e04a7649a3a140ab9599f151cfa8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA512:eab5702bc0baed45492f8dde43a4d2ea3560ad80645e5f9e0cfa8d3b57bccd7fd782d04638e000ba07924a5d9f85e760095b55189188c4017b94705bef9b4a66
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA512:00e5f8c3b6b1aef9ee341db99b339217080a57dbe65fba56798d60ad4be971a9535d8ae27e1f243b18b9fc9e900ada6c452b040a6c8094d5e05d8a76d1d79c03
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.debian.tar.xz' libidn2_2.3.7-2build2.debian.tar.xz 16452 SHA512:55a812a877b2a8039d4105bb8509f389613ad8cb469eb560a3c08085578c448eff1ee1277f69df0505072b1d77ebc6104ad29cd0b6e84be5c56f74e5d0f8ba50
```

### `dpkg` source package: `libksba=1.6.7-2`

Binary Packages:

- `libksba8:amd64=1.6.7-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA512:239da32159ba455f0f76d8a89899e177a04e4621220d24c62b3faa341508d9ee9ac56fccee881b3c2bcba6965806f1c2083c49c47beb0c805ab8e8650975406b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA512:60cb9df9f502ca479818f45b78c4bc2b78f6f359be2b8da489ea98f8896a43ab2c20cf97526b79a3220fb32f1701e62a6481fe61e91e567186ecf4f33d8e64d3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA512:66208b8e4fe76a753943f13a0e65b765eb496013f7f9aeb0b66a454dfb8c67794d1b70841a4014ef0c7ac4642d7b56c38b35cb34be9d8ee8ea6820cc13db53aa
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA512:92fd1450d10419f232cc0e0604f232aae57cff4b05b471b456ed21d40d36c1bfaba7f108cfc57a856d409cbd5421a47cb1d4ca848b127a73161e7f1c0e4e332e
```

### `dpkg` source package: `libmd=1.1.0-2build2`

Binary Packages:

- `libmd0:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libmd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-3-clause`
- `BSD-3-clause-Aaron-D-Gifford`
- `Beerware`
- `ISC`
- `public-domain-md4`
- `public-domain-md5`
- `public-domain-sha1`

Source:

```console
$ apt-get source -qq --print-uris libmd=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.dsc' libmd_1.1.0-2build2.dsc 2383 SHA512:d5d7a38fe932fa60a25630e0ba3ab5ef231b47ac5190e3b04e5c6130f8121a440594955031f9bc52338a29af0b119c696171b3447c46ac71967d7878fd572cd0
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.debian.tar.xz' libmd_1.1.0-2build2.debian.tar.xz 8428 SHA512:3e4caf3b94503176a782241f319a5ed19fb3e9e8dd4056e59beb6fd7208c45ce77396fdd2e8a9c18ca19a65f93b49834853b13f2fbba59195e5499736113d776
```

### `dpkg` source package: `libnsl=1.3.0-3build3`

Binary Packages:

- `libnsl2:amd64=1.3.0-3build3`

Licenses: (parsed from: `/usr/share/doc/libnsl2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-2+-libtool-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris libnsl=1.3.0-3build3
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3build3.dsc' libnsl_1.3.0-3build3.dsc 2095 SHA512:7a8e16ca6e0547d64006f6c4965e46a5ee74a6042a224476b781646759d19a1101a2662e23e0a17b33cec6b30cc5830a476f0aefd6c2b6045f29bc0f9a45fdb6
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA512:a5a6c3ccb2d1e724c8c1f65e55dcd09383eb1ae019c55f4c09441eadf23ffbc2196cfad259805b0ac40ddf3a10af0da453e4d739d67d46829c64d0995dab4e55
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3build3.debian.tar.xz' libnsl_1.3.0-3build3.debian.tar.xz 4932 SHA512:8d808e1e300fb049b0f5bdde17ae8ff2430bb2f176c0621197515ebc4ba41927d0beb85d85e2d053401989c995759433ed8fd67695a6eb3dfd942e98a9a663f0
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.dsc' libpsl_0.21.2-1.1build1.dsc 2425 SHA512:f6036e1386802ab44ad0d65b81f4e81dd2ac084da738752f058d58f8d96074b2ab7b00e8275cdd73bedb18d5ae6ba1fc4b19fb95d4b61e58df5695225629ef7c
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.debian.tar.xz' libpsl_0.21.2-1.1build1.debian.tar.xz 12244 SHA512:316b41dc3611a45c0b7ab0ec7fc617d2c710f8e11d943daefa524fc92155b63e777504a11dbe1b8427e1ad6d15f98095c90cd115df71fb8f90449a461dc9cd3d
```

### `dpkg` source package: `libseccomp=2.5.5-1ubuntu4`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu4.dsc' libseccomp_2.5.5-1ubuntu4.dsc 2831 SHA512:db4f622fc8a8d99d4238c70d59bead099e9253d71ddc2d92fecb05a04e7396682b9804a74cd34fceb90e5a43715874cffcca576a89ddaf1742f1c96c7f578829
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA512:f630e7a7e53a21b7ccb4d3e7b37616b89aeceba916677c8e3032830411d77a14c2d74dcf594cd193b1acc11f52595072e28316dc44300e54083d5d7b314a38da
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA512:a32a7146598f9183179ad15603181d1066e806d01f7c5f215d5405ad8618c06a265d05fff3b4a6cc49c50a577d93d6b920e85f6a581786b3db7389f52a4638e2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu4.debian.tar.xz' libseccomp_2.5.5-1ubuntu4.debian.tar.xz 24476 SHA512:104137ae400eedcea24d0dfcab8d161fb06e76e38c8a4e2e0f0bfeed185b665679beb98c4c282493fd97ebd84d9f083fe4c8b2f677f462aa51ecc374b4b1c7ae
```

### `dpkg` source package: `libselinux=3.5-2ubuntu5`

Binary Packages:

- `libselinux1:amd64=3.5-2ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu5.dsc' libselinux_3.5-2ubuntu5.dsc 3119 SHA512:385cbfcea190e95cd31240c5de38c043af455029b6a40e793095aad42e35307f24b9f7ec1332e8b6e6f4487167eececa11dd3e895521d7ec36ea71d07792928d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA512:4e13261a5821018a5f3cdce676f180bb62e5bc225981ca8a498ece0d1c88d9ba8eaa0ce4099dd0849309a8a7c5a9a0953df841a9922f2c284e5a109e5d937ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA512:ba486d29c92801a02f75213ef5bcc4a0c4a87afe9dfa797aa9bb495ded40f21e37b22d6ea114c0e480d669b090d1116e8b9cac9fa9ea29678d3647bc58d8bb29
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu5.debian.tar.xz' libselinux_3.5-2ubuntu5.debian.tar.xz 38104 SHA512:8adf223e2279377cd73a2d60f7465361ddbbca6b2470622027824c446e72dd534e13ac260c76f05bcf9994f71a12145308ca7ed546347ea7f4a4bdc73d7c5b57
```

### `dpkg` source package: `libsemanage=3.5-1build6`

Binary Packages:

- `libsemanage-common=3.5-1build6`
- `libsemanage2:amd64=3.5-1build6`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1build6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build6.dsc' libsemanage_3.5-1build6.dsc 3097 SHA512:c485c37e7c45924a76a555317e97d4b0a4ed5ff7f218849f8f9577e3d57614a5e57b56961dc931b7d8ea324b917356d00fae1eb6184d8eb9bcb49a126d820fb6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA512:959fbd0d6bc6849da6caa13dc41c3f8818cbbd29f04b5d2ac7246c4b395b4f370f113a04cc9cfcb52be2afebfa636013ac4ad4011384c58c7ce066a45cae2751
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA512:c0a5ddb69c32ddefa26b3d1ec676bcc373e959dd8b4a7fcf6e1f74a3ca8e9af22af851ca66d3c43a704215ff79d27244e33d23038ef2f52ccc321aeb5f0c2790
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build6.debian.tar.xz' libsemanage_3.5-1build6.debian.tar.xz 30224 SHA512:f9d6ca1dec7e1dbee745af28184de2215f23eb560e10f479ca836ca17a7624ec55c976bcd7e724f397bf50d9a03739b4fa1fd8094f40fc34982e1e8ae590fcc7
```

### `dpkg` source package: `libsepol=3.7-1`

Binary Packages:

- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA512:f6739a13677ec7575fa3a84c3877780c23fbdc65a1a4d1d4a5d9657438fc6b66ddb59390271837d04266c02e087a862ea6ab49cb302596fc95abd7c931a0a467
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA512:85d12d0ba5a7a3225f08d041a18fd59641608db5e0a78a1e9649754e45be54a807cd422d4889b88da6e806b4af546336c7a0913448f08ac33dc6ffb983890ef8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA512:9809b3b82c0f816c7fb9b2ec2eb5be8ced95d2d774aebb0834c6848621d0b337ef2950d98602b75e1619db08fb90e4e59e5a0025dfa1a782222addc9535318d5
```

### `dpkg` source package: `libssh2=1.11.0-7`

Binary Packages:

- `libssh2-1t64:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.0-7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.0-7.dsc' libssh2_1.11.0-7.dsc 2328 SHA512:6b4ecfac1f4a9d468cb2c1c7f62b4bc98e8507758eae58580b60ce0872f1915bbd8805f007a43aa03faacb2b1c04aa04a34215d2709da582bf02666b4d79d598
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz' libssh2_1.11.0.orig.tar.gz 1053562 SHA512:ef85e152dc252bd9b1c05276972b9c22313f5d492743dde090235742746d67f634f2a419eff9162132e2274c8582113b75279b074e0c7b34b2526b92fd1a1e8e
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz.asc' libssh2_1.11.0.orig.tar.gz.asc 488 SHA512:6187582a94be24d9ca68963b6d139982e8527378aee7ef8a4cbc0f5c2bae8aee4552e32ec85eb290ec4e940f1d6ebf6737f92468215e0b43b245762753bb2647
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.0-7.debian.tar.xz' libssh2_1.11.0-7.debian.tar.xz 17000 SHA512:657bd2d991e83ab631a9f8197b3d95c354ba5bf4982e250af296732f53bd491b653cfa511cfbe8b35d98ea87d8d369df95755631b62eceb25f135588934ac53f
```

### `dpkg` source package: `libtasn1-6=4.19.0-3ubuntu0.24.10.1`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3ubuntu0.24.10.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3ubuntu0.24.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.10.1.dsc' libtasn1-6_4.19.0-3ubuntu0.24.10.1.dsc 2846 SHA512:c874c14bb2d2829eb755c5355dab8fe0af0aaf6a4a99cb7f902f8a3c20ae4eca773e0b5ff347927d14e926324c2a518bed44aaaea405b8e82e76415f84b545f1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.10.1.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.10.1.debian.tar.xz 24764 SHA512:ac2b0c10d014e85d54e77b13b892515c93109a0d55100bd1ce522bc3a242654396cd52560468334654359850b13b44b067915250a36335e10f29b4dafe47ece9
```

### `dpkg` source package: `libtirpc=1.3.4+ds-1.3`

Binary Packages:

- `libtirpc-common=1.3.4+ds-1.3`
- `libtirpc3t64:amd64=1.3.4+ds-1.3`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc3t64/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PERMISSIVE`
- `__AUTO_PERMISSIVE__`

Source:

```console
$ apt-get source -qq --print-uris libtirpc=1.3.4+ds-1.3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.3.dsc' libtirpc_1.3.4+ds-1.3.dsc 1914 SHA512:457a9a20e8f8815c85fe6d7617c49985ccbb1d6d85cceb907ef06dd34307d33c85b81a9290f9c8397efc36bd1bd1adbc5aa79e061b72f24ef070b33f17d60181
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds.orig.tar.gz' libtirpc_1.3.4+ds.orig.tar.gz 700735 SHA512:125e26247f1ffbf5ce310657515eb84be03b69867e5efbacac6768f406470f9124b66124639daccd9af0c8220a8099cb5dbbe0a370315c61069aa73a5b53815d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.3.debian.tar.xz' libtirpc_1.3.4+ds-1.3.debian.tar.xz 11892 SHA512:56c2fc331c9813c6fee4329d0be86c05255fd51133d2f99c6e18edd1a1dc2ea0bd69501c95bb2b7857c5820476e666f83de33f41f67a7256cd18379fa4480ca5
```

### `dpkg` source package: `libunistring=1.2-1`

Binary Packages:

- `libunistring5:amd64=1.2-1`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-NIV-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.2-1.dsc' libunistring_1.2-1.dsc 2181 SHA512:d2c8b05cb062fa3fe4a8ba1899e266b39daf13f5176bcbcee4df0033216cbc1cf22b678c5bb38b9b552221a656909108614de0dc7788d1b0c438e87e22f5d0f4
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz' libunistring_1.2.orig.tar.xz 2502196 SHA512:5fbb5a0a864db73a6d18cdea7b31237da907fff0ef288f3a8db6ebdba8ef61ad8855e5fc780c2bbf632218d8fa59dd119734e5937ca64dc77f53f30f13b80b17
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz.asc' libunistring_1.2.orig.tar.xz.asc 833 SHA512:fe8eb188ad0628dd288257364bae5f95d803522e0d52133565306cbaf4b2a559e710c43be8419f7cc86ea2b4914fa980418fec4d21503074e14dcea726f675ec
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.2-1.debian.tar.xz' libunistring_1.2-1.debian.tar.xz 13656 SHA512:bd64c568367e9d38ea58cabd4d6e1853ae22af902b888ef18ef5e7ee1dd5e5ea9e978ff28090971945ebc51078e2aad784389f70b1bf2cde9195402b3c30d17c
```

### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.dsc' libxcrypt_4.4.36-4build1.dsc 2300 SHA512:5e9c4a5c26299ac291eb755a9a386ddaac65d6af2e6b9cc37c2803101e1d8b257a83eb36c12f2955873ee99a0a95f61ad2a204e5e5a2c88d33f043a426121c32
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA512:82839d70fc068a4d4d5e14488ea7599e2430091ace53640d639628330eff52a058ac589b6b5a39bc6c83166e68cbf9b9e2024e0371df1f949336f633f2a1726e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.debian.tar.xz' libxcrypt_4.4.36-4build1.debian.tar.xz 8356 SHA512:d181e5637d40e322cf03d80dff03acb9982c0a07a73229d660d8b2fcd02f31783347c0b0208d2ebb077bdf44e87330b04a8cd10a4bc272dbb0feca7f1adfe013
```

### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.dsc' libzstd_1.5.6+dfsg-1.dsc 2369 SHA512:4a35ee6bab82d90c5327828dbc0feeb4246f42a442b05881ab5f9da55e947bf028106699c9ae9ab975659de76bcf9f8f2625bbe7a09686b142657e70c87af59e
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA512:487f37a3cf2a14c57606f0593d43bde00265f59093edf61f10c3c3190676bd7d9fe81d67dc3ef3c925b9e3d6a9ad5ea9e49590a28253965e93b0e72c43acd9c7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.debian.tar.xz' libzstd_1.5.6+dfsg-1.debian.tar.xz 22624 SHA512:5131c85871307dd2323a178903be8f28c537611efa6e63fcc2e10e58f0b4de6a756ab8bd25fec5058a126d175c07454fc3f7791563ca08ca01edd5fab4521b98
```

### `dpkg` source package: `lz4=1.9.4-3`

Binary Packages:

- `liblz4-1:amd64=1.9.4-3`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-3
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-3.dsc' lz4_1.9.4-3.dsc 1934 SHA512:dc2d873a88a2db48bb6f4d4cafd7a3baa51c3b38b458fc53d49f70d7ddfa697add9e74fbf53ba5f7918b90075db63651de14a0389ffc8d5c2fe79f1e1708f8f1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA512:043a9acb2417624019d73db140d83b80f1d7c43a6fd5be839193d68df8fd0b3f610d7ed4d628c2a9184f7cde9a0fd1ba9d075d8251298e3eb4b3a77f52736684
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-3.debian.tar.xz' lz4_1.9.4-3.debian.tar.xz 7076 SHA512:b993e40bf6e14d51df8e01bc01408516e977080368ce37fbec0dd0351a856a4c930ef393dced38e59055b6557beed335d0a8ee5b6eb4306cc2a3a671e4b74e63
```

### `dpkg` source package: `mawk=1.3.4.20240622-2`

Binary Packages:

- `mawk=1.3.4.20240622-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240622-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240622-2.dsc' mawk_1.3.4.20240622-2.dsc 2969 SHA512:3be37afa4f8631bf20894ca94ef87d6756f3ab853b540c9ef5a22dd82ccac4bcb266b90d543f7f8001b15383b6b91e0735958f2ce8993346fd0525d201d01209
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz' mawk_1.3.4.20240622.orig.tar.gz 414190 SHA512:29fed436502531e226af5e04bc54c2f4f9430c80d863f27e520401577c1f03a10d8a0d9def94c71ca43de40a7b1f450340802de37a7276bfe91d029779b1460e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz.asc' mawk_1.3.4.20240622.orig.tar.gz.asc 729 SHA512:a97297424dea27207b49b51fd1461c9a158dd9a4e5289e91194beebe67a35b3b9fbb414cf8367eae296688038264f1e7b6d69a00903f9c88d0b90d32fc154ae3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240622-2.debian.tar.xz' mawk_1.3.4.20240622-2.debian.tar.xz 16136 SHA512:bc4cf923d96fb14dcba444eeb34177710e4411e76fab471ea6a97d0b8a33ded6edae21201eeb6b2a0068fafd76519ab26962fd47524643c3ed656c97a0f5ed54
```

### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=10.1.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.dsc' media-types_10.1.0.dsc 1624 SHA512:78ee4c91efa0eea0314213b1df7cc659f3b47556a648e07c4044f1ae7ae08ccd6c4d479e6425297ac79c38a2a607a157ed781c66751235cecee1eb1ed8edf6b5
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.tar.xz' media-types_10.1.0.tar.xz 59052 SHA512:db92986166c6eedd44d839617c75a1f60704af6d87f92a5c9bb5f207a8e4e27f67b86e340745f6f41e793908d48eb609575678495194a21d368db2fc102b35c9
```

### `dpkg` source package: `mercurial=6.8-3ubuntu1`

Binary Packages:

- `mercurial=6.8-3ubuntu1`
- `mercurial-common=6.8-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.8-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.8-3ubuntu1.dsc' mercurial_6.8-3ubuntu1.dsc 2901 SHA512:9c4185692e40024d9ffa0b49d4c8b8186e693e35e74ac018844d23e666ac56308fa31169346c4fa83d302ec3ef694a9c4e45bc92b201c41190bbf23110939310
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.8.orig.tar.gz' mercurial_6.8.orig.tar.gz 8322075 SHA512:e0eab77c4599f24e33210404b16d591952fbcb7c5e3b64805abc18167c67eaad3d9baa2226e885add5e36569a5148d6a11c5690d68167690570e6e5b243e50f0
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.8.orig.tar.gz.asc' mercurial_6.8.orig.tar.gz.asc 659 SHA512:6ae767aea90e6b22998d4c970445a5e66981abe757276098140610f16912e94e25fcfda7dc657df26e2597b8ffe8f0538b4aa503642db07e4613ff785fba2240
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.8-3ubuntu1.debian.tar.xz' mercurial_6.8-3ubuntu1.debian.tar.xz 55428 SHA512:4eb99cc2e769ef3377a1f4aab09b9f52fb69d1501f0df7dbd531a24ccb19c6499b8599bd74b58be3423f1858489abe2d12a82edb19293e9fbebe6c7c15ac7a22
```

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libncursesw6:amd64=6.5-2`
- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5-2.dsc' ncurses_6.5-2.dsc 3799 SHA512:1855b54f0462cdcb69ed3ef63c9a67fcd536d144574c6b011af026f456c93db8a19a1c96ef09090a3cce3575a019aea7b9017f57e5c608e1d24f4aa0fa31ebc1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz' ncurses_6.5.orig.tar.gz 3688489 SHA512:fc5a13409d2a530a1325776dcce3a99127ddc2c03999cfeb0065d0eee2d68456274fb1c7b3cc99c1937bc657d0e7fca97016e147f93c7821b5a4a6837db821e8
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz.asc' ncurses_6.5.orig.tar.gz.asc 729 SHA512:96a9cb7b3e8a0c4d058129d4aadbc4388b4f022eee6605cca8d270f31c54d1f06429a7c1af09e7de13f2bfeee71fc33d9581b0773830914c8a431be7e7f0e6ba
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5-2.debian.tar.xz' ncurses_6.5-2.debian.tar.xz 49852 SHA512:fd1aca2f0c40d7a2109a7df5825c693616b5d2194533d50ad8391a9fb3fad38328d4d5b651e49f96c9a23ed30ae67e86cfba63c574d69e4d587e1a0cc9bbc994
```

### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.4
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.dsc' netbase_6.4.dsc 898 SHA512:243ea79c8566581ff6137d0525195c0c9ceea2234cf74eb28aef5f6791ba35003e91bc063ce508c7be3038c05cf081db1d8f717d193f78554b7aa4a215d7c9ef
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.tar.xz' netbase_6.4.tar.xz 32712 SHA512:cbc588e5fbef5e3e2c8a2dc49214237e8340bf3fae66973237d1714f67c039d4b8d6886581d92b45a004fa23ff016ad8c82cb15b6f752d1ffa23e3284fe0b80a
```

### `dpkg` source package: `nettle=3.10-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10-1`
- `libnettle8t64:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10-1.dsc' nettle_3.10-1.dsc 2276 SHA512:17edd6e817f764d653549363fe3d424c3ee34005c24b1b6c24e11f1e9dc001bb8b309c860d7d5a5fb069da3d9088b2885218924c055ee6ee808dc271bded8800
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.orig.tar.gz' nettle_3.10.orig.tar.gz 2640485 SHA512:18d5b904ce60514aa81b57bff2945e5f7f4366d4775e6a5ffc227b85be2def72b3d2159b983b75ac95a56d3167a2ef1a25b5dfc2fb6193f16a012935c36a7b34
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.orig.tar.gz.asc' nettle_3.10.orig.tar.gz.asc 573 SHA512:d966dd35dc603f058fc245d017a36428839bcee230457ea8a5d559195c67d00761568c5044ba478fcf565a9379e2767098c87705fd45a81fdb2a36d45b6a4b00
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10-1.debian.tar.xz' nettle_3.10-1.debian.tar.xz 24936 SHA512:984528bc6ddf2296fcc7b4a8a262e0a76ca27b3a168c224b95eff0cd501127401d1433cdb9b9ca59f3f14114fcb33011b7b673ee563a69508ae0e3ccd32dda15
```

### `dpkg` source package: `nghttp2=1.62.1-2`

Binary Packages:

- `libnghttp2-14:amd64=1.62.1-2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.62.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.62.1-2.dsc' nghttp2_1.62.1-2.dsc 2531 SHA512:8e27495883b6ad8834af706db8c95bf71ff0ae06fd5c2c2e3e7fe39e19806c376e93ed4ac01ac9d176f1ca2ad2184ce167aa59b6dd3c521324aba8d99e826006
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.62.1.orig.tar.gz' nghttp2_1.62.1.orig.tar.gz 1066103 SHA512:debb43ad331c1a1e8a1591e9aab21a0e5f7a03372a845ee67f32307863aed5acf9d87feb4ca037158452c7482b59ce3e2a113992d5d696c8bfd7131bb02b38b1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.62.1-2.debian.tar.xz' nghttp2_1.62.1-2.debian.tar.xz 38852 SHA512:76435b74cf25a12eb633d094b52a26add1409f24c4eb7a3fe605b8986d5903c1cf38a0af221a8b889c7b2b53d334c19a5eb11c11b085fd05b586d798cbc4be5e
```

### `dpkg` source package: `npth=1.6-3.1build1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.dsc' npth_1.6-3.1build1.dsc 2107 SHA512:83fc5c562da895742de6b46585a0707052e053804e3187525d290e0cc05938feb7681bb9a7dd053ed930a3774c7abc95a4d1a9e437930ca72c438e29cb7183d8
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA512:2ed1012e14a9d10665420b9a23628be7e206fd9348111ec751349b93557ee69f1176bcf7e6b195b35b1c44a5e0e81ee33b713f03d79a33d1ecd9037035afeda2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.debian.tar.xz' npth_1.6-3.1build1.debian.tar.xz 11036 SHA512:caf36d8727c335bbcf996421e65cf044d6468d95d70e9b671b57196341e49e67f687d6c80cab78d6c0388a90f795e4ed0ff28aaa0d4e7dd6f4701abdfc77a09a
```

### `dpkg` source package: `openldap=2.6.8+dfsg-1~exp4ubuntu1.1`

Binary Packages:

- `libldap-common=2.6.8+dfsg-1~exp4ubuntu1.1`
- `libldap2:amd64=2.6.8+dfsg-1~exp4ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap2/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-California`
- `BSD-3-clause-variant`
- `BSD-4-clause-California`
- `Beerware`
- `Expat`
- `Expat-ISC`
- `Expat-UNM`
- `F5`
- `FSF-unlimited`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with Libtool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Libtool exception`
- `JCG`
- `MIT-XC`
- `NeoSoft-permissive`
- `OpenLDAP-2.8`
- `UMich`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openldap=2.6.8+dfsg-1~exp4ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.8%2bdfsg-1%7eexp4ubuntu1.1.dsc' openldap_2.6.8+dfsg-1~exp4ubuntu1.1.dsc 3422 SHA512:e9c04402478df1c0b9405a99150a2c3ed6f41d61ef410d61e843e0e30e25fd110b9170690e2c3dc129403272c732a46ab9ed8083196aa87ceaf731b5d4e1b7b9
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.8%2bdfsg.orig.tar.xz' openldap_2.6.8+dfsg.orig.tar.xz 3739164 SHA512:30d24f29081e86472acf8a18d345b4c19f016b26760baebc8ec2858b852e4988bbacce7b8ba9b32a5e0ac6bdb268bfa25371e791a35cebb6f731306f6fe0757d
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.8%2bdfsg-1%7eexp4ubuntu1.1.debian.tar.xz' openldap_2.6.8+dfsg-1~exp4ubuntu1.1.debian.tar.xz 186476 SHA512:56cfdae6937c4e996eb2c2db8febbfb9167acb22f6a1d373e952ddda744472cfd9d87cf12e26212c5d8f9e7a392821d20ee169473296d79cb172a44602a2e7ca
```

### `dpkg` source package: `openssh=1:9.7p1-7ubuntu4.2`

Binary Packages:

- `openssh-client=1:9.7p1-7ubuntu4.2`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:9.7p1-7ubuntu4.2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.7p1-7ubuntu4.2.dsc' openssh_9.7p1-7ubuntu4.2.dsc 3091 SHA512:e18ea44d8b2962fca95c77738ac220323beeff73b2365e8295ec9db659add9c88c37108ae3e40b2b2cc82af1ebdce60872c8be2afb6f73a0da9828e24074cc80
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.7p1.orig.tar.gz' openssh_9.7p1.orig.tar.gz 1848766 SHA512:0cafc17d22851605a4a5495a1d82c2b3fbbe6643760aad226dbf2a25b5f49d4375c3172833706ea3cb6c05d5d02a40feb9a7e790eae5c4570dd344a43e94ca55
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.7p1-7ubuntu4.2.debian.tar.xz' openssh_9.7p1-7ubuntu4.2.debian.tar.xz 209752 SHA512:5f60168938ed69d16e4b10a0a69a3390097b8902b5cc459064c14685d1965e86d6c15fc82cc8e4d05a8ba1a22b6b13d1fcdc1bfdb8e4cd9524de0dd8896e5aa3
```

### `dpkg` source package: `openssl=3.3.1-2ubuntu2.1`

Binary Packages:

- `libssl3t64:amd64=3.3.1-2ubuntu2.1`
- `openssl=3.3.1-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.3.1-2ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.3.1-2ubuntu2.1.dsc' openssl_3.3.1-2ubuntu2.1.dsc 2771 SHA512:739af349acd5909f3a9a410b452d6b1009f50ce3e86febcf13a76f6856aeabe0a47fad1d6c7880581d1b6914d5965526e7c5df3d3d56596f8c6d8be04fec0823
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.3.1.orig.tar.gz' openssl_3.3.1.orig.tar.gz 18055752 SHA512:d3682a5ae0721748c6b9ec2f1b74d2b1ba61ee6e4c0d42387b5037a56ef34312833b6abb522d19400b45d807dd65cc834156f5e891cb07fbaf69fcf67e1c595d
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.3.1.orig.tar.gz.asc' openssl_3.3.1.orig.tar.gz.asc 833 SHA512:ae2db74829b71a68e1fc86229396d76f60a9a98e6bba9adc62bdcf2581b60fb0e29ecde2b53a5686c452e754801568e05d3c4f47e8faf02219ac1aae78283338
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.3.1-2ubuntu2.1.debian.tar.xz' openssl_3.3.1-2ubuntu2.1.debian.tar.xz 93832 SHA512:a923afd0241ab7029a50f26d3d329140b0e804a518e3f54c2dcaedd64af4e1185e629085d36be7a0b89138471cf4b12ffd360e9d0d5f55d4cbb6428fec803714
```

### `dpkg` source package: `p11-kit=0.25.5-2ubuntu1`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `X11`
- `customFSFUL`
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.5-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-2ubuntu1.dsc' p11-kit_0.25.5-2ubuntu1.dsc 2398 SHA512:1ffb277dafb37f741f54bcb9d68460c3c77bbaa3aecad201fc3df963df839516fdadc48cab1815394c2ce1a4a72e8b77239cbe29547b4b112cd3fc584c8536e0
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA512:177ec6ff5eb891901078306dce2bf3f5c1a0e5c2a8c493bdf5a08ae1ff1240fdf6952961e973c373f80ac3d1d5a9927e07f4da49e4ff92269d992e744889fc94
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-2ubuntu1.debian.tar.xz' p11-kit_0.25.5-2ubuntu1.debian.tar.xz 24376 SHA512:959d33b22fbd8c60131f3e292645e49a1cf422357c5f89b5202ed5d499a7393c22ee5b3561048abe5f3635c9265b749e9e0ecf99270bad6032b4b628aec240e4
```

### `dpkg` source package: `pam=1.5.3-7ubuntu2`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7ubuntu2`
- `libpam-modules-bin=1.5.3-7ubuntu2`
- `libpam-runtime=1.5.3-7ubuntu2`
- `libpam0g:amd64=1.5.3-7ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.5.3-7ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu2.dsc' pam_1.5.3-7ubuntu2.dsc 2411 SHA512:5af4fd2fc5327aa7db1acc4701434e037802061440b5e750468e655fc5a4571f1cd9b843248113f419ee85b95120963e97cae0e1a5308b141243d56bb7a3fd40
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu2.debian.tar.xz' pam_1.5.3-7ubuntu2.debian.tar.xz 186520 SHA512:ef589ef5dbdcd661bff0ef82ec599571de7eaf64e105b2ef6f5c908f3dcbcc13a60c486f97337365c805db156a5bdad5d427a40d2d3528ce5453418bdd5f2370
```

### `dpkg` source package: `pcre2=10.42-4ubuntu3`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu3.dsc' pcre2_10.42-4ubuntu3.dsc 2269 SHA512:feb393c82703f4b8250cd931d5c6535af7df06d8f575f0367458c3c9522e37debdea3c3238133506e4a0fb56c6acb4768d21b4ec6be156572ceda5d4042c9385
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA512:a3db6c5c620775838819be616652e73ce00f5ef5c1f49f559ff3efb51a119d02f01254c5901c1f7d0c47c0ddfcf4313e38d6ca32c35381b8f87f36896d10e6f7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu3.diff.gz' pcre2_10.42-4ubuntu3.diff.gz 8510 SHA512:12dce72417a2ef0edc027774f3e1ca614fec8261f0398d6f987fd1ffc4b245bcdf092ecd4c6bec1138ba1c9ab39f57bb159bdfd1fbbb83838dc2061808f73ba1
```

### `dpkg` source package: `perl=5.38.2-5`

Binary Packages:

- `libperl5.38t64:amd64=5.38.2-5`
- `perl=5.38.2-5`
- `perl-base=5.38.2-5`
- `perl-modules-5.38=5.38.2-5`

Licenses: (parsed from: `/usr/share/doc/libperl5.38t64/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.38/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `Artistic-dist`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `FSFAP`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.38.2-5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-5.dsc' perl_5.38.2-5.dsc 2938 SHA512:0c89e2550a13148816dfb0e9caedc9327532c63bfff24e62c093ebe80e0ddde73eb24a74d73f802d37d4e157eecdea22e12fc31b0be9ef60d1a2600d0a09c78f
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA512:c4ea40ce9eda247c2ced678a75bdbd8bc292baee5ec3490cb00b1947277e1e0e9e5160d108676380efff13d4f1304f0c8d4eaa2c7e66e543ecd57e513075cb8c
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA512:0ca51e447c7a18639627c281a1c7ae6662c773745ea3c86bede46336d5514ecc97ded2c61166e1ac15635581489dc596368907aa3a775b34db225b76d7402d10
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-5.debian.tar.xz' perl_5.38.2-5.debian.tar.xz 168016 SHA512:cb9c6f5c9271d382d8a31aa6055f4ee4d1f94697bd14e2a2f59a9a7345d071cc06fe5f218185c79aa384c9152782f6beec1ddd014c54e5d0935a6d77ca1844d1
```

### `dpkg` source package: `pinentry=1.2.1-3ubuntu5`

Binary Packages:

- `pinentry-curses=1.2.1-3ubuntu5`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.dsc' pinentry_1.2.1-3ubuntu5.dsc 3322 SHA512:86814cb072f65755573416f567476616d001aefa000362e84b751c85ed42b02297391fc67d7dfabcfd70d7e953e0b9d95b63d98222f8ea79aec527da37fc0c15
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA512:a665315628f4dcf07e16a22db3f3be15d7e7e93b3deec0546c7275b71b0e3bd65535a08af5e12d6339fd6595132df86529401d9d12bd17c428a3466e8dfafab6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA512:60b63b7fe2d6793840be55635f9a704cd42eda69ccaea2453d47b5f7a5198d313b8f23555972584f7f087fd5d0fc2a379bfc5f7512f325b018cc5c3e2e54a47e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.debian.tar.xz' pinentry_1.2.1-3ubuntu5.debian.tar.xz 19244 SHA512:7d4a8fe8920f1d6ef656ab485e2625bc646c5726ba18f91eedb3f4c95241680f2169b80791355e34a707bbebdb0de9986e264f2d8f36848e48a8300fc8497481
```

### `dpkg` source package: `procps=2:4.0.4-4ubuntu5`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-4ubuntu5`
- `procps=2:4.0.4-4ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-4ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu5.dsc' procps_4.0.4-4ubuntu5.dsc 2243 SHA512:aabf9b2b44668b0483484795b459643992c534339531c0e58d714c77ec10bfa3ebc3207ce80510dfc5922720c079f3d153d4393a4f46f1a2cf0ead23c5b15365
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu5.debian.tar.xz' procps_4.0.4-4ubuntu5.debian.tar.xz 38800 SHA512:3326242b1ebfd6060abe1f1411d32219839c8b73a3c23ffa55419aa3319f8e657288fc0cdbd1248b362c042e8668c8eaa2003dec2343b32c30bbff9506b8f759
```

### `dpkg` source package: `python3-defaults=3.12.6-0ubuntu1`

Binary Packages:

- `libpython3-stdlib:amd64=3.12.6-0ubuntu1`
- `python3=3.12.6-0ubuntu1`
- `python3-minimal=3.12.6-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.6-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.6-0ubuntu1.dsc' python3-defaults_3.12.6-0ubuntu1.dsc 3071 SHA512:6a2014832da997fae930303faa5bd0cd452c7a92d6437ee35547aaf79877eaa8f740f6ee0cbe2c3ddd7537a2fafa52350ae9d13bd1b8892615b0ee4d976ddde7
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.6-0ubuntu1.tar.gz' python3-defaults_3.12.6-0ubuntu1.tar.gz 147144 SHA512:0e56d09aa0442cc114ffe715bdee8ec643f38fd8f82f1158ee2bb245c0a43ccded07f7fc7ac38f80ceec3639f50df7d4bfd57d4d1ed36727bdb83ef3bcceb980
```

### `dpkg` source package: `python3.12=3.12.7-1ubuntu2`

Binary Packages:

- `libpython3.12-minimal:amd64=3.12.7-1ubuntu2`
- `libpython3.12-stdlib:amd64=3.12.7-1ubuntu2`
- `python3.12=3.12.7-1ubuntu2`
- `python3.12-minimal=3.12.7-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

- `* Permission to use this software in any way is granted without`
- `By obtaining, using, and/or copying this software and/or its`
- `GPL-2`
- `Permission  is  hereby granted,  free  of charge,  to  any person`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Permission to use, copy, modify,`
- `Redistribution`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `binary forms, with`
- `distribute this software`
- `distribute this software and`
- `distribute this software for any`
- `implied`
- `its`
- `use in source`
- `without`

Source:

```console
$ apt-get source -qq --print-uris python3.12=3.12.7-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.7-1ubuntu2.dsc' python3.12_3.12.7-1ubuntu2.dsc 4340 SHA512:1a4b4fb9559c3810bada2fbdf1ddd9cabeff8c309acce7b9cd6ac0d1cb68086b6b6c8d619f38b4140187d59dc5aac111601903db8bc5d7f90e0f402bbcf05e35
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.7.orig.tar.xz' python3.12_3.12.7.orig.tar.xz 20444032 SHA512:4a363d3f852ad8f4fd1484aa4cec35494a3811be48ef67fadb2bdf2e2489ed07dc78fad6ab475257db503ddd64d39f9800f23a1c94b6bbd15b7f632cff0c90ae
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.7.orig.tar.xz.asc' python3.12_3.12.7.orig.tar.xz.asc 963 SHA512:4d0a7a0da2c81888e93d8ff89ca2ed4bb85a7b0bd00f0d54a14e2c201affac2677ef3984d2b5aea253e624f6465548d9032eefdd9033c1eb3864d82cfd8d3df0
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.7-1ubuntu2.debian.tar.xz' python3.12_3.12.7-1ubuntu2.debian.tar.xz 223532 SHA512:e0c0ec2439d69451a3310e71e990ce4e238b6ea9f29d4bb7d910bbd46ce3b354e6115b6848ec298e8d83933b3da21280c55a128aafdaea87b927dd92067e6374
```

### `dpkg` source package: `readline=8.2-5`

Binary Packages:

- `libreadline8t64:amd64=8.2-5`
- `readline-common=8.2-5`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-5
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-5.dsc' readline_8.2-5.dsc 2810 SHA512:f24d114bb268146833ece44757a170379eb115fbd4846fd22ad08dabc66144ac33360ff1dcf9df45d0e764987a451475556b7bb29f8d913ecfac5eb38e9afb1f
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-5.debian.tar.xz' readline_8.2-5.debian.tar.xz 38368 SHA512:a87dd453e15d5df1b76d705c85be128b272a1d7f8164301b96fae5912101b01dd80dbe6fec940a328456cc2bc061d7d6b674f19b863bf905ca588ca06e7faa56
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.dsc 2439 SHA512:5e2fb3986c0f0e2150c6054e0428adbf1719bb0c33f92ae4acb74a11e625d731ede0262f0d8887c769a95a61f3cd4d23d44bf2f375f0153eba6c0f25b68719c5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.debian.tar.xz 8464 SHA512:812edf4f933ad0f723404192bfbfceca86e58303169a30e3b1f47781b709b91a259621293533d31d7abd16bc522824e2db325426a4ce9a6b428b88d492ae4c6c
```

### `dpkg` source package: `rust-sequoia-sq=0.37.0-1`

Binary Packages:

- `sq=0.37.0-1`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=0.37.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0-1.dsc' rust-sequoia-sq_0.37.0-1.dsc 3827 SHA512:55ff659f34feaf97887d4e842b752e4d3dfd22615d870edd45b9943f381f1f4ac1116de2971851fecc98fbaa7244845d631b65746386a5b5e8729cf794c19062
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0.orig.tar.gz' rust-sequoia-sq_0.37.0.orig.tar.gz 515850 SHA512:c716284bfd1f8492d7f073c07adbbfd73495573a8503d7aa5e24a42873a50392086c69c25a1bd655e3d09df6c369bc2568d02dfda3dc83c189cb9187c440162c
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0-1.debian.tar.xz' rust-sequoia-sq_0.37.0-1.debian.tar.xz 52436 SHA512:cd3d843283d7e8b1dcebdd376ebb895053e62c72a37fad6de0cb53244b5bcadaaa8769bed46e410429102340607e23e1e6d691623440b02338a90c2cc9e8784d
```

### `dpkg` source package: `sed=4.9-2build1`

Binary Packages:

- `sed=4.9-2build1`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `BSD-4-clause-UC`
- `BSL-1`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `X11`
- `pcre`

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.dsc' sed_4.9-2build1.dsc 1992 SHA512:c1fb23ca19645e3c77d7d466818b0ff15ec2fefa423d03c60746d3c441a767af9a551c0af022a5c17e69e58589b8004bc6e127dbb63d806c6269ba0ee2c1e8fd
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.debian.tar.xz' sed_4.9-2build1.debian.tar.xz 62896 SHA512:e9e57380873aa800f7892d99dbebb362a2ba9f27cc984180753d306592d6ca572d0baa3c4faf4b10dbc2aa33985e759f668f1efb4e0b09e4ae2ae689e32969ad
```

### `dpkg` source package: `sensible-utils=0.0.24`

Binary Packages:

- `sensible-utils=0.0.24`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.24
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA512:7f5abddecd7ca44b37c278dbd1ba9515667cfea27fb4819e8b2187da199871855c53ba5115979484ec5f5ac0767c5ef054788d0082e10b597d502c8a620d1ff5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA512:2db2b14bb4b8e616d0e22ac39c56e4e995ba565da59f624ea5ce8958d3eaf545d69136a518e30bd7183adde411607465d7d07fa8e88cc0d980b5d464f8a3b902
```

### `dpkg` source package: `serf=1.3.10-3ubuntu1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `shadow=1:4.15.3-3ubuntu2`

Binary Packages:

- `login=1:4.15.3-3ubuntu2`
- `passwd=1:4.15.3-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.15.3-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.15.3-3ubuntu2.dsc' shadow_4.15.3-3ubuntu2.dsc 2608 SHA512:ab6f70407c132f4d021784bbd4057f3e149bca1c283b37fdb6a48501a10b38fb2d9e1ef1eaf14e056482c643862bee22b340cdb0c76f5137d2bae22ef5412e39
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.15.3.orig.tar.xz' shadow_4.15.3.orig.tar.xz 2054548 SHA512:61427da1ba712e6105d8d6cd55335b5f9544ba9c85d3c2883bd26e7c929016231ef38440cf9f61600a77e6ae58a792be8e80a6149f89c71a69a5824557592c1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.15.3-3ubuntu2.debian.tar.xz' shadow_4.15.3-3ubuntu2.debian.tar.xz 186380 SHA512:995c6d5a34661b7b8961ed86db36f2a46c9cf5cb3d23e1914185299e6f0e711ff95b31052d946107131ddd07e5d87af8e9a78998a81e7960851c498f1e9b7b85
```

### `dpkg` source package: `sqlite3=3.46.1-1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-1.dsc' sqlite3_3.46.1-1.dsc 2486 SHA512:8d7bfca74317c4aa7ca51650285759275cd9eac5a167265214b81bf73a74c36597e098d6b9e5d60f4dcd201b3ff7cf5d9b1494e4afdb86b388a5ecd5e73fc2af
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA512:a5ec0f57d014b2f33d679cfbae0ca1935eb84871376b29216ffcc286a92a363a823ca0ec729a000d702054ee90b2fcc1887c1fb4bebfabcd14894f8ef91b7ad6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA512:47d3c900d95641c89d5d807881e20e97f3b7889cf44c76d48715066ba5c1860defcd17498440d79bcc49b15c2ea28e81ed4b5b159f9e947941e5c1ee27de06ba
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-1.debian.tar.xz' sqlite3_3.46.1-1.debian.tar.xz 30452 SHA512:d641dd2519ee88b0d9b6faaac7bb8d88d00a622327210d81255508e41d79326f29e0659cbe5e5382f00a574c9c92aa85b50fff2462fd6814369382f44cf9a853
```

### `dpkg` source package: `subversion=1.14.3-2build1`

Binary Packages:

- `libsvn1:amd64=1.14.3-2build1`
- `subversion=1.14.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `AFL-3`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BoostAcMacros`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `Svnwrap`
- `Unicode`
- `Utfwidth`

Source:

```console
$ apt-get source -qq --print-uris subversion=1.14.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-2build1.dsc' subversion_1.14.3-2build1.dsc 3823 SHA512:4909144e510aac0d24a32c51f0a7ac8e7b23bbcf3f8b1191231ac10e59c119748636d4eaf8b8385c6b2490cee8a31d35e9154819258b00355b7cb4d01a35b16e
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz' subversion_1.14.3.orig.tar.gz 11621442 SHA512:12188a1c07b8b72594d27b1058c13b2ab81d0306d6da2853400be5a73f12ac5d5ff5ae80b6bfd0320e58d8d797b813d71d6c688ba230d3a010ebaf8bdd910c13
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz.asc' subversion_1.14.3.orig.tar.gz.asc 1724 SHA512:d3922207f672cf17446ce05aa1c7361f4c15279fd1182f7c44cab18be63b086cbac4f22830377f8a4e6ca3cc130dfd5cccaa5536c190b5ac8d786af6ecb7ef30
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-2build1.debian.tar.xz' subversion_1.14.3-2build1.debian.tar.xz 338508 SHA512:c37449f216a0db18ce534e8acf7680a4eabfe15c37a4f22056b201acd2849cebcf76df91d1accef9ae25e45ec8754a7102159ea441e6326f556a691dab4ea7da
```

### `dpkg` source package: `systemd=256.5-2ubuntu3.1`

Binary Packages:

- `libsystemd0:amd64=256.5-2ubuntu3.1`
- `libudev1:amd64=256.5-2ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=256.5-2ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_256.5-2ubuntu3.1.dsc' systemd_256.5-2ubuntu3.1.dsc 8224 SHA512:5350aa2462c30972f816f7d29c2b36f39064f097e4defaec380bb210f792131a7eb41a1027b23d25894a3c8b6972c3b77f44cd2ef4db2044e5cbf71297868d90
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_256.5.orig.tar.gz' systemd_256.5.orig.tar.gz 15664466 SHA512:40558194e05a17b218adf3d6df48b738c866855d43d09c1e9381c2c568a44a8f1617b64476736fc7e34416ad9e8d25dc023cf9de090b4ef9079866919377009f
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_256.5-2ubuntu3.1.debian.tar.xz' systemd_256.5-2ubuntu3.1.debian.tar.xz 227504 SHA512:3fef2cf533a897cd7ba028865a218c0e0939a731eddbf52166b1ee10c879d52d9af1d6c67077f00eb12e590bde450d4e9f2741e704e0a952c1c0c7b41e4f1798
```

### `dpkg` source package: `sysvinit=3.08-6ubuntu3`

Binary Packages:

- `sysvinit-utils=3.08-6ubuntu3`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.08-6ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.dsc' sysvinit_3.08-6ubuntu3.dsc 2495 SHA512:8200c0fa7220e8922a8546f4f1a4beb3a7194b23abd8730c82ea0cfa57bc6fba01e0b7883a0a9b5b1f10c7b7be805689db80df2930c6d345754a3b85a4ddac02
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08.orig.tar.gz' sysvinit_3.08.orig.tar.gz 513674 SHA512:63ed7ebd50944adce1a35af7798d0e2d6248f36a606f63bb7a567424555ec33e83c33b897528c801b4b4ac61b24d2a3555c9a690031c50a94e7ead83f37f8e96
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.debian.tar.xz' sysvinit_3.08-6ubuntu3.debian.tar.xz 140128 SHA512:fa53bd172bf4ce998743f3011b44ebf188948ed436f202181fc6eb7d4535e4d1426aeeac76cda4a650b040d22f9487b890e9f826cd222ddc5e939901c5f7c67c
```

### `dpkg` source package: `tar=1.35+dfsg-3build1`

Binary Packages:

- `tar=1.35+dfsg-3build1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.dsc' tar_1.35+dfsg-3build1.dsc 2141 SHA512:bb080610adc480448cf511d591eaaeb301395e5bbe01b16b254ad33edb33233aba18af79a4cf505fec330c83dac9570d84122432ff11b781a12c5dc409a173f6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.debian.tar.xz' tar_1.35+dfsg-3build1.debian.tar.xz 20948 SHA512:82b1a9f70c99c17f5288a4a9fbe8b1bef0adcd9543f97f876ee81afc16e3ac02e46182557406ff434ae90c81950f22346c3229ee3e5f5f9578dcf09a20053e9f
```

### `dpkg` source package: `tzdata=2025b-0ubuntu0.24.10`

Binary Packages:

- `tzdata=2025b-0ubuntu0.24.10`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-0ubuntu0.24.10
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.10.dsc' tzdata_2025b-0ubuntu0.24.10.dsc 2704 SHA512:287de8c774bd704a7519f0e863782c6da5136aeb1203983a16fdf90157093b3ab3481e69ce1a0a8bcc895b71590609bffe0b5678df7ad93ccc0af845525442e8
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.10.debian.tar.xz' tzdata_2025b-0ubuntu0.24.10.debian.tar.xz 188140 SHA512:1b1aa9cb7f8c94294567597fa31c18334842bbe990d8877581e901c3636610e77071dca08d62aa2163671ce901fde55367a7c1c3cfa531a95cdc5b27a9933aad
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.dsc' ubuntu-keyring_2023.11.28.1.dsc 1872 SHA512:4d3c094e1e01367eb8303808ea5bfea696ee672d855a64272c9222400bec397ebbaa57783bbc8eb4365f0631c9951edeb1b12f04efb3e34275408ef57620f023
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.tar.xz' ubuntu-keyring_2023.11.28.1.tar.xz 20236 SHA512:b17824a91d6e25c5658eae8d9ae509a4158b406768d5d4a8e117a230226ab7cd4327cf7e5b9bbb7baae7c66f3807d27926de85a1ea5c11a82684a890aeb8fd18
```

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA512:608423c255fa2c1072bcaa9c71addd0f393f008ebd321ef4939ed4d714aa43bea4c90979fa5817c19e3d7355415cc70aa8c80ff79760b4286411cfbd58242d77
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA512:8949f197f6aec35ef7ff8c076ed9f863ef369c65de1a17947445c7182623393633e0094e882d50eadbb0435bf03b9a5cb5d11b6e3bd40e33d5d7b15425583b38
```

### `dpkg` source package: `utf8proc=2.9.0-1build1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.dsc' utf8proc_2.9.0-1build1.dsc 2294 SHA512:0a183389b81b1ad614d5a5bf1ace1a2fac8cd91ea7724da25b8443a006c71099cd5ea0d2dc909bfa4a580e816e9e34cc9c4f64a752fef5b0ece510e092690491
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA512:544ed59812279af4135e5622e2e77b3f067765df819cf8b78e679dfc481e9baa5a357a33c40426c5053c1d5107109e3c4c191ed83f3f7c4a6b1769d04b17715c
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.debian.tar.xz' utf8proc_2.9.0-1build1.debian.tar.xz 5956 SHA512:66f918055be1f55b39929c504521094860b66518c99f644a2d826a52076416a7e79d0ed6ec260617e47202e4907f69d7489549737d38ff920942c173e0867693
```

### `dpkg` source package: `util-linux=2.40.2-1ubuntu1.1`

Binary Packages:

- `bsdutils=1:2.40.2-1ubuntu1.1`
- `libblkid1:amd64=2.40.2-1ubuntu1.1`
- `libmount1:amd64=2.40.2-1ubuntu1.1`
- `libsmartcols1:amd64=2.40.2-1ubuntu1.1`
- `libuuid1:amd64=2.40.2-1ubuntu1.1`
- `mount=2.40.2-1ubuntu1.1`
- `util-linux=2.40.2-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.40.2-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2-1ubuntu1.1.dsc' util-linux_2.40.2-1ubuntu1.1.dsc 5010 SHA512:3a015218365a50bbd3808ab60279428c317938d7b317231d8a8fad0ce85f1b7526ddb410842d1c92735147f1b1a0c0f6a8a95d1df6a38c078b3374d33e5b6b56
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2.orig.tar.xz' util-linux_2.40.2.orig.tar.xz 8854820 SHA512:ffe20b915a518a150401d429b0338bc7022190e4ca0ef91a6d9eea345db8c1e11ad01784163b8fcf978506f3f5cad473f29d5d4ef93a4c66a5ae0ebd9fb0c8f2
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2-1ubuntu1.1.debian.tar.xz' util-linux_2.40.2-1ubuntu1.1.debian.tar.xz 114656 SHA512:47ef35bbccad6dda0ebd0dfe57c63812e58d9cd6beca3a39609be17298e7d7f76ee80444882a49de10d13443209c78e607ed329f7ccf8cf65021484a513c44f5
```

### `dpkg` source package: `wget=1.24.5-1ubuntu2`

Binary Packages:

- `wget=1.24.5-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.24.5-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5-1ubuntu2.dsc' wget_1.24.5-1ubuntu2.dsc 2240 SHA512:ced30c1d75e40466b812962a3f12b32bdff370c678efd2fb345ed5c26b4878ef107a163a81278b26a0cfd83c9f17f2665444ac0a5eead5121fb5b94bb0ca3573
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5.orig.tar.gz' wget_1.24.5.orig.tar.gz 5182521 SHA512:572aa54717e51a9eb9959e127c7afb696645088f32ff7df2cfe9d243957e34ee235e98988fa94649df023d2e3d62b6973e8c9f2eb92beba820dd96d5de2a950d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5.orig.tar.gz.asc' wget_1.24.5.orig.tar.gz.asc 854 SHA512:f819dc43a466682ace38e8537698e3c7c3919203f77373bdaea1b63ead40c4d3663590209dfeb6187d98edd00e30848a3abd5735795fb47878924f1d9b2ee10d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5-1ubuntu2.debian.tar.xz' wget_1.24.5-1ubuntu2.debian.tar.xz 65096 SHA512:52a0f1afdc7e05f9fd7f821f31812c19d94bd744e2a9c889a340d75b1fc6d0dfec010f6c050909a234bf6cd87c03aa1a169f901b70ef7e44390831f60dfa53a5
```

### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.dsc' xxhash_0.8.2-2build1.dsc 2076 SHA512:9a1bc162cefe90fd63c2f1225ba28eda45a3972e2bf45fc851bc3c7adcf70e5be65a294aedebc47aedc05516f0c0d9fca065d64196d237497c44840dbf5305e9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA512:3e3eef21432fe88bc4dd9940ccad0308fdea3537b06fa5ac0e74c1bde53413dff29c8b3fc617a8a42b9ce88fcf213311d338a31b1ce73b3729342c9e68f06c78
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.debian.tar.xz' xxhash_0.8.2-2build1.debian.tar.xz 5048 SHA512:c789fd0a22fd40db8983c0f69054141647ebaab94251598723ce1fdf894d0ed2d48c2d5a7f0df7d61e2d874485286e5742a546748d17cc22d5227ad61f6b4ef2
```

### `dpkg` source package: `xz-utils=5.6.2-2`

Binary Packages:

- `liblzma5:amd64=5.6.2-2`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

- `0BSD`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3.0-or-later-WITH-Autoconf-exception-macro`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `noderivs`
- `none`
- `permissive-nowarranty`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.6.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2-2.dsc' xz-utils_5.6.2-2.dsc 2704 SHA512:90bf9580c512dc42edc8a46c8ed034dd3a3e1dcbc845ff5723ffb9666807b16885483eb2d097831707c809a464b6a47a823af515e0f62d530312fea707c5af6d
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz' xz-utils_5.6.2.orig.tar.xz 1307448 SHA512:af3fd021a9c8eaacfb1ae2af3f7e2a0b0554068461de5be3e2c631174cf5fe15425b739832e826c0fb158484b8cea53701be8c568d7ce1f6113b4630205f5c26
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz.asc' xz-utils_5.6.2.orig.tar.xz.asc 833 SHA512:813119ca9b057936971dbad80c1e4ac0664f8149ec4318b2fbf546140bba051e566d3b457cb69f61b584219b023bce808b4347bc209cd3e025028ff8d431ccf8
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2-2.debian.tar.xz' xz-utils_5.6.2-2.debian.tar.xz 24560 SHA512:d821e762d19fececf112f54485aab4decc0276cabbd13aa260348a7eff895f22118164b6691adf77b741e3a41523b663190e14eaab3111f78e1dc801d9a04ad5
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu1.dsc 2993 SHA512:b87b9b973aa22f9cea28d9653bba4383a27203ffb391ff0df537225bbca131eb47b08bc12178bf4d05348e379159be275bddf2d611c97a6bcebd80a0f1ca6e8f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu1.debian.tar.xz 59676 SHA512:c4d82f270d4334711e26d5d328683d0214d3171a2cfaff0b5b613d4df28adabf01e69ec9f6093991ef8f124f289826f30f2fc64223956462d26c9d67866482fe
```
