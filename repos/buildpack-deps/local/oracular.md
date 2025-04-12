# `buildpack-deps:oracular`

## Docker Metadata

- Image ID: `sha256:b6368b3dc3d42516b229c8ed9f84959b5a68afa17d62b6754948de24b3433d74`
- Created: `2024-08-13T17:58:12Z`
- Virtual Size: ~ 829.91 Mb  
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

### `dpkg` source package: `aom=3.9.1-1`

Binary Packages:

- `libaom3:amd64=3.9.1-1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.9.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.9.1-1.dsc' aom_3.9.1-1.dsc 2280 SHA512:508f3bf16061267800bc17c8115dd256fcfeb96f7bc3e146761bf0cedc2b8855d307a7a383e0b160817968681e148c7fca2cf90defdc49f20c57d9a1c54f3d10
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.9.1.orig.tar.gz' aom_3.9.1.orig.tar.gz 5534785 SHA512:6d36a142abf8255bbe9d516d0a6fd62984285c276248aca87b9ee2779f6678f7be63a4bb83f715f3762990d58a56ad2a12cb02c21e9c05885eaa83c19fe4a3b1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.9.1-1.debian.tar.xz' aom_3.9.1-1.debian.tar.xz 20284 SHA512:9ab2ef19dd77ae66f40d9ce228d866822bd994eea59f8392946f311f2c788ac5afc89799a738c65a2a3cd62c869eb7db03efff44a4ed97ca598e1e2d461f2673
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

### `dpkg` source package: `autoconf=2.72-3`

Binary Packages:

- `autoconf=2.72-3`

Licenses: (parsed from: `/usr/share/doc/autoconf/copyright`)

- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Texinfo exception`
- `MIT-X-Consortium`
- `no-modification`
- `other`
- `permissive`
- `permissive-long-disclaimer`
- `permissive-short-disclaimer`
- `permissive-without-disclaimer`
- `permissive-without-notices-or-disclaimer`

Source:

```console
$ apt-get source -qq --print-uris autoconf=2.72-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.dsc' autoconf_2.72-3.dsc 2059 SHA512:5b268cd8d677e4776f7ab478b5b0e2ee4a0956f50683fd8ffda04c547859f7e04a18e02d443092ec70f6f6a7ce98a598a7fe0aa8af9c508b01070d47582668a6
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72.orig.tar.xz' autoconf_2.72.orig.tar.xz 1389680 SHA512:c4e9fbd858666d3e5c3b4fe7f89aa3e8e3a0a00dc7e166f8147d937d911b77ba3ac6a016f9d223ccdd830bc8960b3e60397c0607cc6a1fd2c50c7492839ddd17
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.debian.tar.xz' autoconf_2.72-3.debian.tar.xz 22980 SHA512:90b764a0c296a68195a48a0a47f248d77bdf1f68af40c16617f863ed2b2d9f936b136974593cdf0dc68bd32a486a6f2c1a2eb1a108bbc38e109f92d4745f9cba
```

### `dpkg` source package: `automake-1.16=1:1.16.5-1.3ubuntu1`

Binary Packages:

- `automake=1:1.16.5-1.3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris automake-1.16=1:1.16.5-1.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3ubuntu1.dsc' automake-1.16_1.16.5-1.3ubuntu1.dsc 2657 SHA512:8000fe08014aaa9da51cefe063499a6f8932515916e81cd9b4a3201313609804ce69a353a0bbb5d6e0b574107259e0e8e61a7af21f1932f4b2cfcea359ed619f
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz' automake-1.16_1.16.5.orig.tar.xz 1601740 SHA512:3084ae543aa3fb5a05104ffb2e66cfa9a53080f2343c44809707fd648516869511500dba50dae67ff10f92a1bf3b5a92b2a0fa01cda30adb69b9da03994d9d88
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz.asc' automake-1.16_1.16.5.orig.tar.xz.asc 833 SHA512:032a7c39abb4cabbefa4eb9c15263baec0902e48c0c81364307361a41fd55be282b9640707c789f5ae572e8e60240e34d1b575a671b5710f5d2a5716fafc2d51
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3ubuntu1.debian.tar.xz' automake-1.16_1.16.5-1.3ubuntu1.debian.tar.xz 14624 SHA512:95bf57bcfe7f509c2c1c5e3c6fbe9a407af96dca49ccde0e990580720b301974c882a3a4ae7a9e9bb26c0129918f0847fb480749a315a52204b705a0a277f2c2
```

### `dpkg` source package: `autotools-dev=20220109.1`

Binary Packages:

- `autotools-dev=20220109.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20220109.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.dsc' autotools-dev_20220109.1.dsc 1661 SHA512:aca60be8ed006832005e58bf176f8c7e8abe85986dbcc6d15d8b5c092c89322a132601784ef1f977d7e071c8b033debcef7c3cb5712765be00c2d298d9812d71
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.tar.xz' autotools-dev_20220109.1.tar.xz 87340 SHA512:5427cc6897685355018db547ec39fd6bcc0ecbd73ba25869fb841f3503c1753af9a323d963a2b3150ef40ff07486f39377acdec878b2c054c1fa51de9afe01bb
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

### `dpkg` source package: `binutils=2.43.1-4ubuntu1.2`

Binary Packages:

- `binutils=2.43.1-4ubuntu1.2`
- `binutils-common:amd64=2.43.1-4ubuntu1.2`
- `binutils-x86-64-linux-gnu=2.43.1-4ubuntu1.2`
- `libbinutils:amd64=2.43.1-4ubuntu1.2`
- `libctf-nobfd0:amd64=2.43.1-4ubuntu1.2`
- `libctf0:amd64=2.43.1-4ubuntu1.2`
- `libgprofng0:amd64=2.43.1-4ubuntu1.2`
- `libsframe1:amd64=2.43.1-4ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.43.1-4ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.43.1-4ubuntu1.2.dsc' binutils_2.43.1-4ubuntu1.2.dsc 9772 SHA512:0b064843eddbd0baa8e74d2745b1815deb5158390f7e48e3eb0cfbecd0f9917160450aeb8782cce87b33315d4b47c5ca9e61f8263117b0ac244f4a3a917269af
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.43.1.orig.tar.xz' binutils_2.43.1.orig.tar.xz 28174300 SHA512:20977ad17729141a2c26d358628f44a0944b84dcfefdec2ba029c2d02f40dfc41cc91c0631044560d2bd6f9a51e1f15846b4b311befbe14f1239f14ff7d57824
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.43.1-4ubuntu1.2.debian.tar.xz' binutils_2.43.1-4ubuntu1.2.debian.tar.xz 160304 SHA512:5bb9cb3d4033e5bb2be46349ffa2fa241d0bd63ccfff0278b8b242c6d69303c23db88597f6b48c150cfefa8ae8a0139f84d8d18fbb3194cdbb660beb19c2977b
```

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build2`
- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

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

- `bzip2=1.0.8-6`
- `libbz2-1.0:amd64=1.0.8-6`
- `libbz2-dev:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

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

### `dpkg` source package: `cairo=1.18.2-2`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.2-2`
- `libcairo-script-interpreter2:amd64=1.18.2-2`
- `libcairo2:amd64=1.18.2-2`
- `libcairo2-dev:amd64=1.18.2-2`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2-2.dsc' cairo_1.18.2-2.dsc 2763 SHA512:2ce8341b1caf77b3685e4816acc88b7ff2cf364b7be17db292a4f965e819e4ce7b99438bad1aaf2feb7ae4f898276c2ea77b9f20bf5a113903bb4f9fe5a76550
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2.orig.tar.xz' cairo_1.18.2.orig.tar.xz 32574256 SHA512:9b533ef65da120bdf6ec6e66b76c9a9a489b91951925357c2db9f399ce27fe03d10e500c4c03b72ad43d73bb5beb4d51e36c24443977a52ecfe1d24b07c99bef
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2-2.debian.tar.xz' cairo_1.18.2-2.debian.tar.xz 30396 SHA512:fadcbdd42490ff01217c7125b7635532cc658bc467df540b40b2a4e383ba150d0b2659f9ef9f30742a5cab2928bdcad09e4168e290d768cb9c1d745ad42e21ac
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
- `libcurl4-openssl-dev:amd64=8.9.1-2ubuntu2.2`
- `libcurl4t64:amd64=8.9.1-2ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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

### `dpkg` source package: `db-defaults=1:5.3.21ubuntu2`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.dsc' db-defaults_5.3.21ubuntu2.dsc 1663 SHA512:018dc4aedcf739f611a55d1ad1ee6ad62f0ed60d33ebfeb493ac9709e743f5cb2bd318ee246a3f52f0274424048c94c25f685889a82c16b24357c023f63917df
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.tar.xz' db-defaults_5.3.21ubuntu2.tar.xz 2644 SHA512:7a41ab8046316afe6da9623ba36bf6803b6de49059f29acdb5d931009e3f317381713c3d2f68c4aeefa5bbed2e625196359b4735421d8e9caffd07f0f06184b4
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-7ubuntu1`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-7ubuntu1`
- `libdb5.3t64:amd64=5.3.28+dfsg2-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdb5.3-dev/copyright`, `/usr/share/doc/libdb5.3t64/copyright`)

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

### `dpkg` source package: `djvulibre=3.5.28-2build4`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2build4`
- `libdjvulibre-text=3.5.28-2build4`
- `libdjvulibre21:amd64=3.5.28-2build4`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build4.dsc' djvulibre_3.5.28-2build4.dsc 2499 SHA512:55baf25f2ed6440d0a2bc111b493125a2762ab6ec60a26aae6ee33241ee00a0f3b73b998392e4593a7e8501765bb40b7b6c1d6c25edd14c1ad2eeda439867e63
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA512:4fdbecd2b7b583ee4211c9cda6638a3a831c883e2552b3c8ad09f69e8734831addc14f590faab8c58d7f9f017b527abccc384f6066e674e341cf43c96db49cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build4.debian.tar.xz' djvulibre_3.5.28-2build4.debian.tar.xz 17704 SHA512:ded773fa8599b2a3d0a1683d1bb59b276b82a76ed1d6ddc92ea04f5a5186d0c41058c8c99595a37b9a7f111755b52ef455b31cecb2bbca439bc5e2533fa4941b
```

### `dpkg` source package: `dpkg=1.22.11ubuntu1`

Binary Packages:

- `dpkg=1.22.11ubuntu1`
- `dpkg-dev=1.22.11ubuntu1`
- `libdpkg-perl=1.22.11ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

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

- `comerr-dev:amd64=2.1-1.47.1-1ubuntu1`
- `e2fsprogs=1.47.1-1ubuntu1`
- `libcom-err2:amd64=1.47.1-1ubuntu1`
- `libext2fs2t64:amd64=1.47.1-1ubuntu1`
- `libss2:amd64=1.47.1-1ubuntu1`
- `logsave=1.47.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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

### `dpkg` source package: `elfutils=0.191-2ubuntu0.1`

Binary Packages:

- `libelf1t64:amd64=0.191-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libelf1t64/copyright`)

- `BSD-2-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
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
$ apt-get source -qq --print-uris elfutils=0.191-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.191-2ubuntu0.1.dsc' elfutils_0.191-2ubuntu0.1.dsc 3402 SHA512:a8dc3939701876831db7019ff11d845506204fcb10e2c1c3f24b1e0c6c17f3b64f03a7ed3a78652fc70973f71ef153f50e07f4fcd1cffc8936bb5b9f0c3567e7
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.191.orig.tar.bz2' elfutils_0.191.orig.tar.bz2 9310088 SHA512:e22d85f25317a79b36d370347e50284c9120c86f9830f08791b7b6a7b4ad89b9bf4c7c71129133b8d193a0edffb2a2c17987b7e48428b9670aff5ce918777e04
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.191-2ubuntu0.1.debian.tar.xz' elfutils_0.191-2ubuntu0.1.debian.tar.xz 47400 SHA512:4489850b44e5cf6016f0529a50dd61d65e9818d49a1356c973541f6bbbcc312b19885b8a258d78c9fdd1b59a09f08860c2a87be89408f6c40d783098f9fdbb13
```

### `dpkg` source package: `expat=2.6.2-2ubuntu0.2`

Binary Packages:

- `libexpat1:amd64=2.6.2-2ubuntu0.2`
- `libexpat1-dev:amd64=2.6.2-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.2-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2-2ubuntu0.2.dsc' expat_2.6.2-2ubuntu0.2.dsc 1474 SHA512:f10fead65ceba608648188d5eea4387f47160abc5aed066f5eb06baeb06ae40ac01423de0e4764ad8f3f7f673a5c0c64a36923e3779914940ac8bd88d842bba8
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2.orig.tar.gz' expat_2.6.2.orig.tar.gz 8416128 SHA512:49b6be12bd6284106920abc61d86d441cba126615fc4019744fc56dc5e7c5efc72b02c09e5c7b491882a633c1c45dc4a03e92a96372ab62bcd70755f6878c6b6
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.2-2ubuntu0.2.debian.tar.xz' expat_2.6.2-2ubuntu0.2.debian.tar.xz 28688 SHA512:37ca98eec42a7be35a009b2690f7093584437a8cecd212504a0e2736c6e07bbaba8ad49611f7a126550edc87d700a40eae1fb95b4cb7f59b100afe0b9a7a0848
```

### `dpkg` source package: `fftw3=3.3.10-1ubuntu4`

Binary Packages:

- `libfftw3-double3:amd64=3.3.10-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu4.dsc' fftw3_3.3.10-1ubuntu4.dsc 2853 SHA512:a530b03a4ece9547cbad79ca2dca0b7994c592d4d74194ca06ead3e0da136a204074389e2841ec111e09f3b1a52c7d3e37d5a8014eaeb233ac0d0fba4e732d3e
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu4.debian.tar.xz' fftw3_3.3.10-1ubuntu4.debian.tar.xz 14916 SHA512:340f1e7fe78fb1674b0cae90f0ed4d4627a10ef7937d9559ab61a3895b6239cb4ef1fa07a704b10ba240ec51341d4b2d2c537672829e49c18b4669634feb2a6a
```

### `dpkg` source package: `file=1:5.45-3build1`

Binary Packages:

- `file=1:5.45-3build1`
- `libmagic-mgc=1:5.45-3build1`
- `libmagic1t64:amd64=1:5.45-3build1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.dsc' file_5.45-3build1.dsc 2408 SHA512:366c97f8faa11661879e0907bda25730f24dd6369455d60723790152a6d3e67b858ce99de82b095cae396d0621efff6dcd25ae11ce8e5e4af75006623ad85f19
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA512:12611a59ff766c22a55db4b4a9f80f95a0a2e916a1d8593612c6ead32c247102a8fdc23693c6bf81bda9b604d951a62c0051e91580b1b79e190a3504c0efc20a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA512:4bda3c9b23e534e31d8726eae110e108c538c88ca4884666989da9bedc5dcfd9cfcb3754e68885ca5310db67bff151f9bf4f21913f7b5046f158a9ca38bc00a4
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.debian.tar.xz' file_5.45-3build1.debian.tar.xz 35964 SHA512:292021c05c73e2ea593af147e6df690a73df6ebf5b10408760be48c161ed341d974145aed93161d09fcea6a7ce0348edfea8a4c0ece9fdf54e1c33e5d3673b86
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

### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig-dev:amd64=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-1.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.dsc' fontconfig_2.15.0-1.1ubuntu2.dsc 2817 SHA512:cd0eff27460c679b9d7db384bba94d4468f9cbf9d7bec41db6b12965f3d4ed48af35e73d3739d8ad8f5575bbc769379582e5e92e676dbe229260340f479c6d40
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA512:754cd5fffa198fc07a39cf7df683e9adfa7f54ab41fdff8c0eacc078fd35d3e01069ba343f2b045e0b40df88d9f1fc1ee0f7565799f9cb194a59cf95b64c4417
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz' fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz 30556 SHA512:a09fe533b6a684bc6e2bfc25eda89cad9f1020c3ba5738ff9799d770a3b6c09d6a12edfeeacffe38a73d8a3f28313e7108fa6f6acff70ba1eb346007f4bc73cb
```

### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-8
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA512:c5632f8cf1fa690efc292e7ae8239265ac3a04e13423601d9a151b200ea36ae5242a0867428e3c7148c0cd5fa6b4ff3c368b53451f3234e20634f2fc6fe5c1fa
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA512:e61fc8c675ef76edb49dd9a8caee62087280929bb8144b52aca2f8def30025c56246589ad8a6a806b9574e6876eedd16d57c70a6ce9c86817a2dfe39d8a2bb2b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA512:7a19189a106a1243c64d43b050f87cba6f6c32d070f246aceb5ccc687401366825a31a653e45fa700e1593f7ed32340581988cfc1a489b5f8b705e80c2a891ee
```

### `dpkg` source package: `freetype=2.13.3+dfsg-1`

Binary Packages:

- `libfreetype-dev:amd64=2.13.3+dfsg-1`
- `libfreetype6:amd64=2.13.3+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libfreetype-dev/copyright`, `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `Expat`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT-Modern-Variant`
- `MIT-SMC`
- `OpenGroup-MIT`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.13.3+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.dsc' freetype_2.13.3+dfsg-1.dsc 3680 SHA512:da953f9b177530c782fc32e09d5b53155c36f20664f35bf408a9ebe3d1f006d7df9d452ab358a7f707f1ff65223062b57cf1c8c55115dac9a493c593e76e63fd
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz 342404 SHA512:e662a20ad2ff80534e8ea0df2f299e8f61350f13d279f80f8257b18352e863dd2c266791b85d3410b0c83966cb12e3ff49cf398b83a651dc73772df9fcf5936c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:c676452fb04b49824ce0a7287b46dc0234cee301bf80d31da01f5a1e7009ddbc0479866bfca62086fe23105436b0c02b9fb729b8fa24e7ca703c0fc357fe3675
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz 2173852 SHA512:54ef9e3a4f0c298893268ed409f59aa1620a60c656ee3f8bdddbb91ffb2e70eea2f016a85c0a02eef699de362abee4aabae4482f0fa1cbf42967b5873fc84f2d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:bd1699aa0bf9f93a02b87a9c59ee6b69e4b24626fbcfbf9e0a0739f2634923bd397ee51379f57aae88465823ceb6bfe5cf6708a2bfa32d76f4a64ad6a9c08e3b
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig.tar.xz' freetype_2.13.3+dfsg.orig.tar.xz 2201416 SHA512:634c2644bb70b93a605fae4d3e731cb13d149af4d01029ecf2d166b2e07cba07489303440a836057adc54f9bdabcceb7fde102dc5e5bf69f35c99ebae66f7293
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.debian.tar.xz' freetype_2.13.3+dfsg-1.debian.tar.xz 43904 SHA512:b701ab41be470caf67fdf2efcd37f7504145d45872ce52d409a8e2a73b49031bc7159d0b1be02b4cc2b2abd82ca93e43d86b26bc3d3e7a08749f52ae5e3c9367
```

### `dpkg` source package: `fribidi=1.0.15-1`

Binary Packages:

- `libfribidi-dev:amd64=1.0.15-1`
- `libfribidi0:amd64=1.0.15-1`

Licenses: (parsed from: `/usr/share/doc/libfribidi-dev/copyright`, `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.15-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.15-1.dsc' fribidi_1.0.15-1.dsc 2004 SHA512:1d88586837309bc1c69f06070b256deeaad313cc97dcc2ac5186557b6bd0bf929c1117232626ca87e3d1b2dfc2f6cf4fc2de88ff52b186f5f478b24f0d5c97c0
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.15.orig.tar.xz' fribidi_1.0.15.orig.tar.xz 1166860 SHA512:98295f1a7203f401d63cc1da7cce3be6975729055fea54640d25cf05a6e6bc27d2e1a3f8edd1ddf4c7fc5ff6f7f1e2daf2bf86683d4aed5988ade8bfa5da414f
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.15-1.debian.tar.xz' fribidi_1.0.15-1.debian.tar.xz 8888 SHA512:0fe5fae694764396f45068b224c67636e86abbd5d860ff541b2dc736fb77dcbda4fe152a45bb41ee8bbc51fd41ec622a1c4b3ce8b58e7e05fe5097e5dae7007f
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2`

Binary Packages:

- `cpp-14=14.2.0-4ubuntu2`
- `cpp-14-x86-64-linux-gnu=14.2.0-4ubuntu2`
- `g++-14=14.2.0-4ubuntu2`
- `g++-14-x86-64-linux-gnu=14.2.0-4ubuntu2`
- `gcc-14=14.2.0-4ubuntu2`
- `gcc-14-base:amd64=14.2.0-4ubuntu2`
- `gcc-14-x86-64-linux-gnu=14.2.0-4ubuntu2`
- `libasan8:amd64=14.2.0-4ubuntu2`
- `libatomic1:amd64=14.2.0-4ubuntu2`
- `libcc1-0:amd64=14.2.0-4ubuntu2`
- `libgcc-14-dev:amd64=14.2.0-4ubuntu2`
- `libgcc-s1:amd64=14.2.0-4ubuntu2`
- `libgomp1:amd64=14.2.0-4ubuntu2`
- `libhwasan0:amd64=14.2.0-4ubuntu2`
- `libitm1:amd64=14.2.0-4ubuntu2`
- `liblsan0:amd64=14.2.0-4ubuntu2`
- `libquadmath0:amd64=14.2.0-4ubuntu2`
- `libstdc++-14-dev:amd64=14.2.0-4ubuntu2`
- `libstdc++6:amd64=14.2.0-4ubuntu2`
- `libtsan2:amd64=14.2.0-4ubuntu2`
- `libubsan1:amd64=14.2.0-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

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

### `dpkg` source package: `gcc-defaults=1.219ubuntu1`

Binary Packages:

- `cpp=4:14.1.0-2ubuntu1`
- `cpp-x86-64-linux-gnu=4:14.1.0-2ubuntu1`
- `g++=4:14.1.0-2ubuntu1`
- `g++-x86-64-linux-gnu=4:14.1.0-2ubuntu1`
- `gcc=4:14.1.0-2ubuntu1`
- `gcc-x86-64-linux-gnu=4:14.1.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.219ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.219ubuntu1.dsc' gcc-defaults_1.219ubuntu1.dsc 37367 SHA512:56003b91cb4286dc0c52b7a800724b2bc377452c9b9e938fd87b5ce67210b6c28dea0070a29e0021d593bd50a9d1fd7e2af74f40f8839a98088dc22223458cd2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.219ubuntu1.tar.xz' gcc-defaults_1.219ubuntu1.tar.xz 56628 SHA512:877add7ac19ff3d6bceafb5fc5d9f982280dda0eb05d81ab0f16f1b14deeaa9375cc061b8ce2696272a92a43d403f2032888697b8f37c8b3bfdf5b1083b840bd
```

### `dpkg` source package: `gdbm=1.24-2`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.24-2`
- `libgdbm-dev:amd64=1.24-2`
- `libgdbm6t64:amd64=1.24-2`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

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

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-1`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-1`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-gdkpixbuf-2.0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-dev/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-bin/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`)

- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.12+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-1.dsc' gdk-pixbuf_2.42.12+dfsg-1.dsc 3214 SHA512:54ffeb8691a4452390d4260815c7d9e5c5d68aed8ea36183c010d8550c4fbb8739d5163f9e0dca778193646c21f4310f2d21176c0e42c28a8d8476a77b831693
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.12+dfsg.orig.tar.xz 6443656 SHA512:b27ce26fa876416dcb81d1e20679074fcb292f2574c7404cf0748e551888c59d62376499a0511411880fa30fe233757d578fd1d4025bde98e33ab6584c4850d5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-1.debian.tar.xz' gdk-pixbuf_2.42.12+dfsg-1.debian.tar.xz 21576 SHA512:bfacc4deb25e8224859846da62ae5c2975e0e156949e5cc8f657af09cac9bc15b297f156c357bdc5e4815a1bf411c953524fef4f2df1e2742e53520f343043eb
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

### `dpkg` source package: `glib2.0=2.82.1-0ubuntu1`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.82.1-0ubuntu1`
- `gir1.2-glib-2.0-dev:amd64=2.82.1-0ubuntu1`
- `libgirepository-2.0-0:amd64=2.82.1-0ubuntu1`
- `libglib2.0-0t64:amd64=2.82.1-0ubuntu1`
- `libglib2.0-bin=2.82.1-0ubuntu1`
- `libglib2.0-data=2.82.1-0ubuntu1`
- `libglib2.0-dev:amd64=2.82.1-0ubuntu1`
- `libglib2.0-dev-bin=2.82.1-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/gir1.2-glib-2.0-dev/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `Iconv-PD`
- `Janik-permissive`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Mingw-PD`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`
- `cmph`
- `old-glib-tests`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.82.1-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.82.1-0ubuntu1.dsc' glib2.0_2.82.1-0ubuntu1.dsc 4656 SHA512:a705d8640dfe764ef6f9137654655b34f37e3c153cac6aa39f80e044b462a7186a2af66856e826373b996c65a7b7ebe4bc124dabdbc9defed48656c05cab62dd
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.82.1.orig-unicode-data.tar.xz' glib2.0_2.82.1.orig-unicode-data.tar.xz 262908 SHA512:4242b9c35af660c6f38b7e1aaed1e39926dfd8473657c4fce9a29539a4d8a0cd6fdd8cf2afc85d8e984ca15f20c32f4f39ba8eb3091901f8f59ef3f2dfe4411d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.82.1.orig.tar.xz' glib2.0_2.82.1.orig.tar.xz 5554132 SHA512:a176d00d2e2be0fb65b7084b2689fddb29cdfa8391ae4e5272b3205fbd4bc05f010b6dc81dff59581eb57cee28920b5f5147e2812725496c5abb5c7bf0937b12
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.82.1-0ubuntu1.debian.tar.xz' glib2.0_2.82.1-0ubuntu1.debian.tar.xz 132448 SHA512:78d8c9de83a444e2093bc92f8760c903e6df21090cc6800706364175778096a89bd14deb02ca67dce380293705ae1443ef9e1fe4cdba32ca77a70d10d7764e20
```

### `dpkg` source package: `glibc=2.40-1ubuntu3.1`

Binary Packages:

- `libc-bin=2.40-1ubuntu3.1`
- `libc-dev-bin=2.40-1ubuntu3.1`
- `libc6:amd64=2.40-1ubuntu3.1`
- `libc6-dev:amd64=2.40-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

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

- `libgmp-dev:amd64=2:6.3.0+dfsg-2ubuntu7`
- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu7`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-2ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libgmp-dev/copyright`, `/usr/share/doc/libgmp10/copyright`, `/usr/share/doc/libgmpxx4ldbl/copyright`)

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

- `libgnutls-dane0t64:amd64=3.8.6-2ubuntu1.1`
- `libgnutls-openssl27t64:amd64=3.8.6-2ubuntu1.1`
- `libgnutls28-dev:amd64=3.8.6-2ubuntu1.1`
- `libgnutls30t64:amd64=3.8.6-2ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libgnutls-dane0t64/copyright`, `/usr/share/doc/libgnutls-openssl27t64/copyright`, `/usr/share/doc/libgnutls28-dev/copyright`, `/usr/share/doc/libgnutls30t64/copyright`)

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

### `dpkg` source package: `gobject-introspection=1.80.1-4`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.80.1-4`
- `gir1.2-freedesktop-dev:amd64=1.80.1-4`

Licenses: (parsed from: `/usr/share/doc/gir1.2-freedesktop/copyright`, `/usr/share/doc/gir1.2-freedesktop-dev/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `BSD-2-clause`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFULLR`
- `GPL with Autoconf exception`
- `GPL-2`
- `GPL-2+`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`

Source:

```console
$ apt-get source -qq --print-uris gobject-introspection=1.80.1-4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-4.dsc' gobject-introspection_1.80.1-4.dsc 4044 SHA512:a4c5311b3d6069b69be8963c6f5ea36310a01ba905d5107d354d12a3ec6a6c91849eb96487c813a72574b293c2478d6f378395f408650e8c5d5030cde0f44849
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig-glib.tar.xz' gobject-introspection_1.80.1.orig-glib.tar.xz 5475296 SHA512:6968ac28451a72f2d8d50ce31a887be2c26ae2bc5ddba1a4aadaafb955c1bb11576017084006d78a6e6f09e88696534b94eb50c61b0b0509695a547de34c7620
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig.tar.xz' gobject-introspection_1.80.1.orig.tar.xz 1040228 SHA512:f45c2c1b105086488d974c6134db9910746df8edb187772f2ecd249656a1047c8ac88ba51f5bf7393c3d99c3ace143ecd09be256c2f4d0ceee110c9ad51a839a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-4.debian.tar.xz' gobject-introspection_1.80.1-4.debian.tar.xz 59428 SHA512:fb4df14e1350ffe0ead124c2a85e1b3d5b2eb7b5c5ebbf1511d172f93dce33f1b28042a4e5af27446c0a4acc1fd8063b7c81083b3b9e46174d2f7efd838c686f
```

### `dpkg` source package: `graphite2=1.3.14-2ubuntu1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2ubuntu1`
- `libgraphite2-dev:amd64=1.3.14-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`, `/usr/share/doc/libgraphite2-dev/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `custom-sil-open-font-license`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris graphite2=1.3.14-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.dsc' graphite2_1.3.14-2ubuntu1.dsc 2650 SHA512:76b4ecf1d5c2fdbd4e50b434d39b83f7661a79047d14733b22f3b58ba621164b341a14cc6d0b018bd5101ecd8e9bcdcaa25ea6c05fab45eba64c96c41cde0902
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.debian.tar.xz' graphite2_1.3.14-2ubuntu1.debian.tar.xz 14384 SHA512:6d25f7498c175c26533ae14088723110b9a35f5242e2b35e3a2cfe71bd92d2f855c013c11abce5c9cd058407c78940377c2fe97c1c6b3beaee41006ec24382a4
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

### `dpkg` source package: `harfbuzz=9.0.0-1ubuntu0.1`

Binary Packages:

- `gir1.2-harfbuzz-0.0:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz-cairo0:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz-dev:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz-gobject0:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz-icu0:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz-subset0:amd64=9.0.0-1ubuntu0.1`
- `libharfbuzz0b:amd64=9.0.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-harfbuzz-0.0/copyright`, `/usr/share/doc/libharfbuzz-cairo0/copyright`, `/usr/share/doc/libharfbuzz-dev/copyright`, `/usr/share/doc/libharfbuzz-gobject0/copyright`, `/usr/share/doc/libharfbuzz-icu0/copyright`, `/usr/share/doc/libharfbuzz-subset0/copyright`, `/usr/share/doc/libharfbuzz0b/copyright`)

- `Apache-2.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with AutoConf exception`
- `GPL-2+ with Font exception`
- `GPL-2+ with LibTool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with AutoConf exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `Monotype`
- `OFL-1.1`
- `UFL-1.0`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=9.0.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_9.0.0-1ubuntu0.1.dsc' harfbuzz_9.0.0-1ubuntu0.1.dsc 2995 SHA512:7527180f2cbdeaf4bf46a9a6ffb1405a399c840135949c099d8afe5d0c0fb4b16f657ee71bd1789d221d1a32271977cf7c96f8a9d9d81993a145a40986640c48
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_9.0.0.orig.tar.xz' harfbuzz_9.0.0.orig.tar.xz 17895360 SHA512:2700b560727d9c4440ad9c74a170b857f20f9e553e5d98b0c4bcf086a25ba644149d7c89009a41d964af7a924efcc486da4dcbfa5cc4d47f9f10e9b6b8c689af
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_9.0.0-1ubuntu0.1.debian.tar.xz' harfbuzz_9.0.0-1ubuntu0.1.debian.tar.xz 20700 SHA512:7ccaee7748a6c6a2afd7b9add9b7e37688ced642aa63f01a8f7b6dcfeeeec48ac83ab8ebad191a69e17f626c8ed155b885d6a56d015a72376a506a2735b40f92
```

### `dpkg` source package: `hicolor-icon-theme=0.18-1`

Binary Packages:

- `hicolor-icon-theme=0.18-1`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-1.dsc' hicolor-icon-theme_0.18-1.dsc 2325 SHA512:a9fb3dffa21b693b201c8f5e412d58cefa08d641b958a7aac77e665b82e9b2adbe8130d31845bac1429dd6e10e59d2c55265d2b8a662174c47d5592492acf9f3
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA512:07db44fb6bec797445740832fa2b3ba56f5f335834161a26a4e5f767a8c45c0885ef1189e887b56752bd20c4b1aac101c5d4a395df4177cd3817ee5105db0d37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA512:e00447c8918250978622a9465ac16181206deed977743d71faa068341f3aab4a1e98e70aed9f03e62806f2b3d8e1df20ff3b09332d0feda70d4532496154f0c2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-1.debian.tar.xz' hicolor-icon-theme_0.18-1.debian.tar.xz 9100 SHA512:7754fdbe398ca689a264808b6390aa62038afd0c413937861689f6625230e2afeaf5a8da3bc91db288993cd15e507a425d4840f3d17e76bbc714af95792f0f7d
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

### `dpkg` source package: `icu=74.2-1ubuntu4`

Binary Packages:

- `icu-devtools=74.2-1ubuntu4`
- `libicu-dev:amd64=74.2-1ubuntu4`
- `libicu74:amd64=74.2-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu74/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=74.2-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu4.dsc' icu_74.2-1ubuntu4.dsc 2343 SHA512:b40cf5c80daadb094c0fe63027d03591c3164d458cd1fe3396d1d2ea30faa69861941f1e9b62995cc0c9b619717de1f9bdb0abcc862aa6cd17dc6ab85936cc28
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz' icu_74.2.orig.tar.gz 26618071 SHA512:0cbe29122370ba03a8fb5b0f1494f598748044ad2aa4d66ba65fe98ebeb88da2d73d324ad6bfc44e004846e0ab5c9a34d1fdf3d6bdb3095c0d47e929b943e6db
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz.asc' icu_74.2.orig.tar.gz.asc 659 SHA512:e961664f91a66afe898041fb42950f925854cfe7f5a287f691b90ad79c215a14300cdd1aad94a310aa2b1cdda3d850ab978d1fe2eadba5fd46f375f4bcefcd11
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu4.debian.tar.xz' icu_74.2-1ubuntu4.debian.tar.xz 64428 SHA512:2b239bac899d1cd419ae7aa3052f087ea5e36a7492eb9fbddc21d4cda789c61a8ec62c60cb710f4493c0cab550fe244240cae008f7d286a1e6a3bbe153f5512f
```

### `dpkg` source package: `imagemagick=8:6.9.13.12+dfsg1-1`

Binary Packages:

- `imagemagick=8:6.9.13.12+dfsg1-1`
- `imagemagick-6-common=8:6.9.13.12+dfsg1-1`
- `imagemagick-6.q16=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6-arch-config:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6-headers=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-7-extra:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-7t64:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-dev:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-dev=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6-headers=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6.q16-7t64:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6.q16-dev:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickwand-dev=8:6.9.13.12+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6-arch-config/copyright`, `/usr/share/doc/libmagickcore-6-headers/copyright`, `/usr/share/doc/libmagickcore-6.q16-7-extra/copyright`, `/usr/share/doc/libmagickcore-6.q16-7t64/copyright`, `/usr/share/doc/libmagickcore-6.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-6-headers/copyright`, `/usr/share/doc/libmagickwand-6.q16-7t64/copyright`, `/usr/share/doc/libmagickwand-6.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

- `Artistic`
- `BSD-with-FSF-change-public-domain`
- `GNU-All-Permissive-License`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL2+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception-GNU`
- `ImageMagick`
- `ImageMagickLicensePartEZXML`
- `ImageMagickLicensePartFIG`
- `ImageMagickLicensePartGsview`
- `ImageMagickLicensePartOpenSSH`
- `ImageMagickPartGraphicsMagick`
- `ImageMagickPartlibjpeg`
- `ImageMagickPartlibsquish`
- `Imagemagick`
- `LGPL-3`
- `LGPL-3+`
- `Magick++`
- `Makefile-in`
- `Perllikelicence`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.13.12+dfsg1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1-1.dsc' imagemagick_6.9.13.12+dfsg1-1.dsc 5106 SHA512:e0c1417e9717dab052f8ece30ec1867f7ad71ae35ee1c49d0108ebe8456c0ddfc326bc643115cb065196b2b4103f0b0395085d0740ea568a49c4353ab90cb9a8
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1.orig.tar.xz' imagemagick_6.9.13.12+dfsg1.orig.tar.xz 9829420 SHA512:a4e100d743b39a135051e52a596643717f169723f60a7b90fb55eeb4cdb245eefc9ee702599359dd970e4a474029fdad32952092dc3fca1ccce3755795dd0e51
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1-1.debian.tar.xz' imagemagick_6.9.13.12+dfsg1-1.debian.tar.xz 260856 SHA512:8a73566490410f521217a0bc39d56d1c49f7db43f0b82718f0b1f9fc4c665014eefe2a86ab51eecbd02454db81b636927007bef29411bd07e0748b163ff61319
```

### `dpkg` source package: `imath=3.1.11-2ubuntu1`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.11-2ubuntu1`
- `libimath-dev:amd64=3.1.11-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.11-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.11-2ubuntu1.dsc' imath_3.1.11-2ubuntu1.dsc 2725 SHA512:9225aa4002da1ed0f5dd07c6db4cfa4da5ca0e42d5f27c0e0b3e322a86dd283da5001b829e29256bb6034014c4c24cd787ee163d19c9bd049e93e1dde32ec510
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.11.orig.tar.gz' imath_3.1.11.orig.tar.gz 596585 SHA512:0bc86bea3a2aca89d02b501b4fba3c13ca861e914cec558e820fe9e4c43ab14cac34e31ff278b8c35b5fe76f7bea32f2c8105c0d33eb92224eb23d42d7a402e9
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.11.orig.tar.gz.asc' imath_3.1.11.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.11-2ubuntu1.debian.tar.xz' imath_3.1.11-2ubuntu1.debian.tar.xz 9952 SHA512:877f52022c79707c92f4ce08195d6b5c3c1452bc1dc0185bd1980a711024ffa7c51d9cde9e2a6abbed08a42836dfdba513d79b597f836e95a9ead1ac6e78ed88
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

### `dpkg` source package: `isl=0.27-1`

Binary Packages:

- `libisl23:amd64=0.27-1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.27-1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA512:1dd37f08556f5adea516dfe737edac400b4aaf394b6e6dcbdc0bc194d96983f9e03523c1ecacb275e28dc415feacf3198376348cb543672ad742c1d6bb51ecc6
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA512:6d6f50c3f6f26e0d3f67586dee6427d87999c426c94069a6f3012ec3c9a41adeebd50f43b5d2705db6abc12e38eb01c19f55dba113c0799da5f667eef46b2be0
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA512:71f034e81f666ebafa4ec331430fd679643e5d157b094f196c1a1841a0a22f79f46052523c8469ec95b71005e53a82599fe37c08e27b60d5d7f60e94eb50c916
```

### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.dsc' jansson_2.14-2build2.dsc 2120 SHA512:46ec9f5477e738ee6ed2c10b7406dd0edcfe0148a394af3ca3ee214b14c9de95e691fefa34c3aa9770c1e23ec77d26b1f5149cc8faa4201f15680ba9f3a6d754
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.debian.tar.xz' jansson_2.14-2build2.debian.tar.xz 5580 SHA512:1eec1f274a77512033b857a64bb26f8bc2fa98212c33c17dcfedbbd7f82711d32a803ad4ea4d8d158ef9949be2a69f3d5d4126fc4ac3b63c9200c361bba0f939
```

### `dpkg` source package: `jbigkit=2.1-6.1ubuntu2`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1ubuntu2`
- `libjbig0:amd64=2.1-6.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.dsc' jbigkit_2.1-6.1ubuntu2.dsc 2199 SHA512:6c5e2f89ed58fd018e27fa73352952192a347c19f8c0a454a2c9e3f9ab90d06bc578f522b32d074100f5de44a8d9d62b3d096fbb7f5f01e2bd803b37a8104de3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.debian.tar.xz' jbigkit_2.1-6.1ubuntu2.debian.tar.xz 11172 SHA512:1ecf331f4e530f5f3105c57c2d7b366591f113220745f143b9335f3e383bf04dd963d61aecc4c8eb16ef4ecc74a2f5e2743779d95dcd8626dc6eaea8b2824c18
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

- `krb5-multidev:amd64=1.21.3-3ubuntu0.2`
- `libgssapi-krb5-2:amd64=1.21.3-3ubuntu0.2`
- `libgssrpc4t64:amd64=1.21.3-3ubuntu0.2`
- `libk5crypto3:amd64=1.21.3-3ubuntu0.2`
- `libkadm5clnt-mit12:amd64=1.21.3-3ubuntu0.2`
- `libkadm5srv-mit12:amd64=1.21.3-3ubuntu0.2`
- `libkdb5-10t64:amd64=1.21.3-3ubuntu0.2`
- `libkrb5-3:amd64=1.21.3-3ubuntu0.2`
- `libkrb5-dev:amd64=1.21.3-3ubuntu0.2`
- `libkrb5support0:amd64=1.21.3-3ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-3ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-3ubuntu0.2.dsc' krb5_1.21.3-3ubuntu0.2.dsc 4101 SHA512:7161efd7e01d2ee072312e5f6638e9d27d84578696e97352f5fa23abca9162f4c9897699e7a9eccd1499e7ea3392473a53b3f1a97df94e2edde76efb103e3f31
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA512:8992a5f5247315b9846aa73be4ee1ea223c0231a52d5c6c28718b1f3e3b45d62e2dad4aa5543a83163d1369bb79886b6c1c22766f22d8aa2f6b2575c54d0075c
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-3ubuntu0.2.debian.tar.xz' krb5_1.21.3-3ubuntu0.2.debian.tar.xz 110884 SHA512:ccf948bb0cd6a3dfe2ee15d5a1a55097c5707a1e445fcf1a73ba2558b976da8be85aa903f66948f46aef5fcae8ec477e0e4eb36405b89824bb633a0b188977d9
```

### `dpkg` source package: `lcms2=2.14-2build1`

Binary Packages:

- `liblcms2-2:amd64=2.14-2build1`
- `liblcms2-dev:amd64=2.14-2build1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.14-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2build1.dsc' lcms2_2.14-2build1.dsc 2076 SHA512:a07321bc0c14d05183402f5aafac34d2a151a70b3095bfa4380a7fd69bbe443bade7f0079dadfdbb61b6b839caa73b367453697c4fb856fdc668fb5e464e92e0
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14.orig.tar.gz' lcms2_2.14.orig.tar.gz 7406694 SHA512:92fba0a457ea81590eba0b8d98b7b621da6a83e3857948585e0b524235954954f9ac1670cf6a19b457c0fce22a87899ea4c5810db1ff2acf7c6b6e0dc4b61a1b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2build1.debian.tar.xz' lcms2_2.14-2build1.debian.tar.xz 11848 SHA512:a594544bd5350b53112fd18838886859a83178348f0e69cf97f29fc2c9ca89101616527b06f41f31ce1578ab7a90eddaee3653ce139daec6d7abfc3e0bae6e54
```

### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu2`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-4ubuntu2`
- `liblerc4:amd64=4.0.0+ds-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu2.dsc' lerc_4.0.0+ds-4ubuntu2.dsc 2733 SHA512:b9fcf936ebc688ac277f11bc4a1233460d4745269c69d26a71867fc92c06ad7540a81c9275c235b66a9623e7360b03db6a9e1ea7aa668aaa084cae22b174edfc
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu2.debian.tar.xz' lerc_4.0.0+ds-4ubuntu2.debian.tar.xz 7344 SHA512:61f8c1a0b20e3c3016a7787307325e0a56549ff13f88af815bbdfa5e24285e0a090c05ae51b9c9b068b917a64e808cd329c7204e81273169489ba0727e59d1c7
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

### `dpkg` source package: `libdatrie=0.2.13-3build1`

Binary Packages:

- `libdatrie-dev:amd64=0.2.13-3build1`
- `libdatrie1:amd64=0.2.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libdatrie-dev/copyright`, `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.dsc' libdatrie_0.2.13-3build1.dsc 2368 SHA512:37dc9a866dc340d8291bcb07cdb8a20f39ba8ee0dca0c8c37cbbfb9403afe0a8229b18f1d019a54d19855977ac499df9067e7ecdf0a297cedc4d239e67353272
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.debian.tar.xz' libdatrie_0.2.13-3build1.debian.tar.xz 9776 SHA512:a44919cfcb079af400a09c4f9468cf16edc3fc05fe46bf57b7a22abd80130da91b5ce3b6d8c8cacfa8c0f48b751220b0b74bc624be433db01b3ab1aac9bc6524
```

### `dpkg` source package: `libde265=1.0.15-1build4`

Binary Packages:

- `libde265-0:amd64=1.0.15-1build4`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

Source:

```console
$ apt-get source -qq --print-uris libde265=1.0.15-1build4
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15-1build4.dsc' libde265_1.0.15-1build4.dsc 2320 SHA512:13df375faac90d80a8b39214728fc5c14c5d4676e7a271c28cc1f778d7d3b7263b6459d7e755c4c114e1c9b141b0cc803d4088c4270a6f859ab1600854b64870
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15.orig.tar.gz' libde265_1.0.15.orig.tar.gz 846016 SHA512:375d8e781108247e0e8b4d7a036d20cc5d0670bdbf6ddb40a6d3dbf912fa776d2f001fb762301cb97e4d43be29eb415b0cdbfc6e07aa18b3f2346f7409c64fce
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.15-1build4.debian.tar.xz' libde265_1.0.15-1build4.debian.tar.xz 136788 SHA512:b63199c4e94fd4e494c3289f395478e7092f835e775dfa24b9f40c25206002e6d9d92361d8bc87c22315488555d02bc7edccbf0542b49a60568c03b8cdb79bee
```

### `dpkg` source package: `libdeflate=1.21-1`

Binary Packages:

- `libdeflate-dev:amd64=1.21-1`
- `libdeflate0:amd64=1.21-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.21-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.21-1.dsc' libdeflate_1.21-1.dsc 2214 SHA512:d1f98353f60564549effdc413687c2e94a2464c0dda4b5a6851ed10313a5bb35fbe4bdf9924bc2fccf32460cf2483014d3788464b13d6fe0ad11b7a277475726
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.21.orig.tar.gz' libdeflate_1.21.orig.tar.gz 195361 SHA512:7cd9bc91992ef824a0fdf175b0da081b8381decc325013477a3fbfcfe6cf240f66cedbeec830a51343fedb8c27c76fba8782c1aed3fc538e3afd6c9f8cdc90fb
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.21-1.debian.tar.xz' libdeflate_1.21-1.debian.tar.xz 5504 SHA512:4c00fe472db31b1a073f8dc7bdf8c6c05ea478a78807a38f250994eff856f45fcc9bdc2f2b3527b2a4d4b43dd320ed8dea6abc63415bb333574c2d9f4c664276
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

### `dpkg` source package: `libevent=2.1.12-stable-10`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-dev=2.1.12-stable-10`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-10`

Licenses: (parsed from: `/usr/share/doc/libevent-2.1-7t64/copyright`, `/usr/share/doc/libevent-core-2.1-7t64/copyright`, `/usr/share/doc/libevent-dev/copyright`, `/usr/share/doc/libevent-extra-2.1-7t64/copyright`, `/usr/share/doc/libevent-openssl-2.1-7t64/copyright`, `/usr/share/doc/libevent-pthreads-2.1-7t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSL`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `FSFULLR-No-Warranty`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris libevent=2.1.12-stable-10
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10.dsc' libevent_2.1.12-stable-10.dsc 2412 SHA512:969e1fd08a03875ec0148230fa9a755831b02d3723623e077320d509e1cf22eb6d7e5decbba26a76314d8060d55aac28c8f8a0ba556a00a51d9e50fec0570163
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10.debian.tar.xz' libevent_2.1.12-stable-10.debian.tar.xz 17908 SHA512:164b8ff27a7e9313e96fae90449888d878b8aa81ed0a1415813dd58be8db3eccf2358ec882986fa178d9c352b93c6a6e59200eaf954d7b1d8a92138fa5b8b895
```

### `dpkg` source package: `libexif=0.6.24-1build2`

Binary Packages:

- `libexif-dev:amd64=0.6.24-1build2`
- `libexif12:amd64=0.6.24-1build2`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.24-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build2.dsc' libexif_0.6.24-1build2.dsc 2211 SHA512:d0172894995cb89f271addf6b735d6e3a79e55f4d1dd8c71b4475f277ffe2f16516b843c72a9351e493470365a9274264ed242aed537c1effdbecf9ed3ac5310
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24.orig.tar.gz' libexif_0.6.24.orig.tar.gz 1140079 SHA512:0b15a157c1030490bf1c4239487dffda90daad467ac6281db2a1b34a8419fca32b4b5265452e75cbcd2c9dc9a829643231cd3749e88251ed1b596756d1c5a9f4
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build2.debian.tar.xz' libexif_0.6.24-1build2.debian.tar.xz 11872 SHA512:24a2e46cd80073ed6b943d13f42078dbf9eac53c156c53d7c1f17e4a3a2b63b4e431d3d869bb38e675c39fe22bbc9ccc5e846d7d718397665c7d995b1c4916cc
```

### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi-dev:amd64=3.4.6-1build1`
- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi8/copyright`)

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

### `dpkg` source package: `libheif=1.18.1-2`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.18.1-2`
- `libheif-plugin-libde265:amd64=1.18.1-2`
- `libheif1:amd64=1.18.1-2`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `BSL-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.18.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.18.1-2.dsc' libheif_1.18.1-2.dsc 3520 SHA512:97ba7d45e4be748c893748479b498313f48c7cd83225642f46bcc61a23f87dcdb2f24e67c6ee7c9b2e62d9894341caef8189927f19547361ee8d9ee7815bc51c
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.18.1.orig.tar.gz' libheif_1.18.1.orig.tar.gz 1524386 SHA512:0b37b834882af8368fc550e75245f4cf487c71a041833ba5e7887155e289e9c2058b41724524091347f297cfdec45b537796a97f4c43531aecf9f0a099753f41
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.18.1-2.debian.tar.xz' libheif_1.18.1-2.debian.tar.xz 11852 SHA512:00723f9de1ceb48de6310acb71e81f654e1f1d691f785d5b4e16a081469afa1ce80aa07924f9d508dfb6dc52530134007e4828a66e8135bf39de88271cd89712
```

### `dpkg` source package: `libice=2:1.0.10-1build3`

Binary Packages:

- `libice-dev:amd64=2:1.0.10-1build3`
- `libice6:amd64=2:1.0.10-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build3.dsc' libice_1.0.10-1build3.dsc 2181 SHA512:7f380aeae73731a89a717a8374072b7beb2bfcccc89086b2e1f5d3f9e790783e318c337c4282f7fb73b6512d04667c1a66818617b6089548032bcd226aee58aa
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA512:2d4757f7325eb01180b5d7433cc350eb9606bd3afe82dabc8aa164feda75ef03a0624d74786e655c536c24a80d0ccb2f1e3ecbb04d3459b23f85455006ca8a91
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build3.diff.gz' libice_1.0.10-1build3.diff.gz 11722 SHA512:a643009809766e385b9eaf7fddbf4ff4acdc5dc98b5a8a8bb940c4ead4e635d13123494e5cbecad487cb7b7d1cf4ae826f957ef1e552362f2efe483057cb9916
```

### `dpkg` source package: `libidn2=2.3.7-2build2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build2`
- `libidn2-dev:amd64=2.3.7-2build2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

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

### `dpkg` source package: `libjpeg-turbo=2.1.5-2ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-2ubuntu2`
- `libjpeg-turbo8-dev:amd64=2.1.5-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu2.dsc' libjpeg-turbo_2.1.5-2ubuntu2.dsc 2535 SHA512:aaf83542c31e42beb369561f0eee167e6bbb117d535f145a82c029926ba8cbc66a4e2593a608375d63e5aa0fd5d3d0bfa0d4d638168918afd9a62959e3a38079
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu2.debian.tar.xz' libjpeg-turbo_2.1.5-2ubuntu2.debian.tar.xz 108492 SHA512:52a61609f8aa4397be2ff97f40fe8429543d82a1a0bd3bcdee43e79640a0342b537ce7a2d31268172760d9de75683a534609db9ce66874fb20eac3dcb9419038
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg-dev:amd64=8c-2ubuntu11`
- `libjpeg8:amd64=8c-2ubuntu11`
- `libjpeg8-dev:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg8/copyright`, `/usr/share/doc/libjpeg8-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu11
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.dsc' libjpeg8-empty_8c-2ubuntu11.dsc 1579 SHA512:345994a54ea05e741e0e6d35f0a7fc39f45c3fc34a995e972ae6b2843baf0b2fcc0bf4726aa7bb86249e39f46a7e23a273d2430d0fcb9bb88f03c6e9d3c912aa
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.tar.gz' libjpeg8-empty_8c-2ubuntu11.tar.gz 1959 SHA512:eb9cec5b6f3fa5e65950b72c14709d33e638b52a2bd2ac2f2297e0edb9e9e224e6da9bbe355e082026b92d980614e8fe40196e4a3ed7cdd560a65f03b138782b
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

### `dpkg` source package: `liblqr=0.4.2-2.1build2`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1build2`
- `liblqr-1-0-dev:amd64=0.4.2-2.1build2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1build2
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.dsc' liblqr_0.4.2-2.1build2.dsc 2096 SHA512:30b38f252c27f4d20ef46e5c923eb0da2ba7e32fdb4277181980c6e0f82de4d5624cfd51339a3a16883357b1f6db4f6b8cf827be09f14c882752ec866ed5ca08
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.debian.tar.xz' liblqr_0.4.2-2.1build2.debian.tar.xz 5448 SHA512:ff140c20c1683b3fc3c4a91682d72214a39ce60b4a3ecaf9bbfdf6229b79a48e2d38e26009f2243dafc953bad3c54ef8520de2dad51b762ba0d019691a678ce2
```

### `dpkg` source package: `libmaxminddb=1.10.0-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.10.0-1`
- `libmaxminddb0:amd64=1.10.0-1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `CC-BY-SA-3.0`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.10.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.10.0-1.dsc' libmaxminddb_1.10.0-1.dsc 2329 SHA512:26776ba5df910db189ee5aba123e00a38078d03e1578238b31abc7165f33326f4d68b9ba0b4aab9a527dc7645202c8f5475257ebba8db5ef28e0ae6072362a40
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.10.0.orig.tar.gz' libmaxminddb_1.10.0.orig.tar.gz 366960 SHA512:41bb3f78f83f6583cf6da53b5eff62ed5b613652945fcf472bc9a5ccf736bb78df42301e1e7d2eda44e143aa887799d553213cae39912008ce8dd3360aa46cb5
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.10.0-1.debian.tar.xz' libmaxminddb_1.10.0-1.debian.tar.xz 12604 SHA512:ef0342d5dd66825e62c8ffce391f448c4f90359198fad583937e69d1fefa274b957e86fb482e794cd9d3f5ce21c59facf037be1f4f4727e99b4191d48aa19c2d
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

### `dpkg` source package: `libpng1.6=1.6.44-1`

Binary Packages:

- `libpng-dev:amd64=1.6.44-1`
- `libpng16-16t64:amd64=1.6.44-1`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libpng1.6=1.6.44-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.44-1.dsc' libpng1.6_1.6.44-1.dsc 2247 SHA512:a7c7ca125f5919ccd75a830ca08638274cd90cf02438251ef19990ff5770e6eecb3e29fd17bdf7fb00cfde9a1cd1227b631fcdc6201bfa66528c71b0a0e97441
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.44.orig.tar.gz' libpng1.6_1.6.44.orig.tar.gz 1558044 SHA512:c023bc7dcf3d0ea045a63204f2266b2c53b601b99d7c5f5a7b547bc9a48b205a277f699eefa47f136483f495175b226527097cd447d6b0fbceb029eb43638f63
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.44-1.debian.tar.xz' libpng1.6_1.6.44-1.debian.tar.xz 31504 SHA512:bcadcf8d14f645866dd77274bac22598603ee93a9f086c8ea0992c6759e9baa93f41b472644ea247f34cdf6980cbb69a4bb0ae5b715ec7a3e5d07992b5cc0af1
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl-dev:amd64=0.21.2-1.1build1`
- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl-dev/copyright`, `/usr/share/doc/libpsl5t64/copyright`)

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

### `dpkg` source package: `libraw=0.21.2-2.1build1`

Binary Packages:

- `libraw23t64:amd64=0.21.2-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.2-2.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2-2.1build1.dsc' libraw_0.21.2-2.1build1.dsc 2360 SHA512:c666f7557ae3d3f02b93f7e2f618e6f09bef54b9c9830459bbbfd849db16ec25082fc4ed9695ee47d11bcc0afbf115f02ec9b771f978328725cd9256e5c81928
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2.orig.tar.gz' libraw_0.21.2.orig.tar.gz 565383 SHA512:a8b0ec275cc0055d6eb2069008c3312ae007cd86e481111f68d5d60544afcd76b728f8418bf63a80d35d7d00283536da63e03f5eecb4cc28f4cc8d92070e8b39
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.2-2.1build1.debian.tar.xz' libraw_0.21.2-2.1build1.debian.tar.xz 24828 SHA512:ac6bca1ac907e284ce63303992ddc5e9c3c5cf040ecfb946751aea182ae61ca162fc5b757618d123d7ddde757c13e5c4ee0ea48aa395fdafcb5f0b84356a35f5
```

### `dpkg` source package: `librsvg=2.59.1+dfsg-1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.59.1+dfsg-1`
- `librsvg2-2:amd64=2.59.1+dfsg-1`
- `librsvg2-common:amd64=2.59.1+dfsg-1`
- `librsvg2-dev:amd64=2.59.1+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-rsvg-2.0/copyright`, `/usr/share/doc/librsvg2-2/copyright`, `/usr/share/doc/librsvg2-common/copyright`, `/usr/share/doc/librsvg2-dev/copyright`)

- `0BSD`
- `0BSD,`
- `Apache-2.0`
- `Apache-2.0,`
- `BSD-2-clause`
- `BSD-2-clause,`
- `BSD-3-clause`
- `BSD-3-clause,`
- `Boost-1.0`
- `Boost-1.0,`
- `CC-zero-waive-1.0-us`
- `Expat`
- `Expat,`
- `FSFAP`
- `LGPL-2`
- `LGPL-2+`
- `MPL-2.0`
- `MPL-2.0,`
- `OFL-1.1`
- `Sun-permissive`
- `Sun-permissive,`
- `Unlicense`
- `Unlicense,`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris librsvg=2.59.1+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.59.1%2bdfsg-1.dsc' librsvg_2.59.1+dfsg-1.dsc 3046 SHA512:a4ff13bb94074b7989d38bf0c7c0cd30a4b76d421f276ef9dc1b9e41d4c416dc669c137b7b928b01a348c99b368e347b13b11f82597219d79249951996a1a9d9
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.59.1%2bdfsg.orig.tar.xz' librsvg_2.59.1+dfsg.orig.tar.xz 6113468 SHA512:7bf4e21ee1279c5a8b7f9699d0f5a5a27b130f4ac1c17c144c362b9380d0bb623770229ec1f94a7a819e72d66c770bda336c356bad03e1e5b7eead4268c176f5
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.59.1%2bdfsg-1.debian.tar.xz' librsvg_2.59.1+dfsg-1.debian.tar.xz 17809436 SHA512:7bb0c19c31bf19ea4a2e5715a33e28e895927ca711c0710377070b2f4ea0595d7a067e7b920d365161c64c9d71b053fdbe504d4447782d9af89a2b9f4689ac2f
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
- `libselinux1-dev:amd64=3.5-2ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

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

- `libsepol-dev:amd64=3.7-1`
- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

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

### `dpkg` source package: `libsm=2:1.2.3-1build3`

Binary Packages:

- `libsm-dev:amd64=2:1.2.3-1build3`
- `libsm6:amd64=2:1.2.3-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build3.dsc' libsm_1.2.3-1build3.dsc 2170 SHA512:8a520e3ffb431799786f69aecf52ad9ebd54d0c2146aa9ba79cd7c7d301aff12da18fa10cb3c9abdab3a6ff7f36f08c3ebf3625312ec306453bf54a5e370f704
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA512:03b77d86b33cdb3df4f9d65131a0025182f3cb0c17b33a90d236e8563b3011d225b9d006186302d07850edafa5b899aec6a086b8d437d357cd69fedd5f22d94b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build3.diff.gz' libsm_1.2.3-1build3.diff.gz 9110 SHA512:9d091a10e743ee293094e270865b4499e77d0cee4815dfb21d42a53832d50ea82a599e6bf8945bfd1c51add353de20d77eb672dc666400c98b5c8a390b6dec2c
```

### `dpkg` source package: `libssh2=1.11.0-7`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.0-7`
- `libssh2-1t64:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

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
- `libtasn1-6-dev:amd64=4.19.0-3ubuntu0.24.10.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

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

### `dpkg` source package: `libthai=0.1.29-2build1`

Binary Packages:

- `libthai-data=0.1.29-2build1`
- `libthai-dev:amd64=0.1.29-2build1`
- `libthai0:amd64=0.1.29-2build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai-dev/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.dsc' libthai_0.1.29-2build1.dsc 2451 SHA512:63a4a7a95532beb3aed3d7311b7f341689b89b0ff87e112a02a03448408a14464c4ad3339e16a1fae76fefacb8e72286850494c907d8c49e0c7eb83651d7ab36
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA512:0ba1261581a1705a2a2546a3071acb3c63892dbf111f0dad415667165a6b9542a5e4549061c67b11ec53de7c9e70fceb3c04d794fd12a22d991a539dbacebda1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.debian.tar.xz' libthai_0.1.29-2build1.debian.tar.xz 12744 SHA512:40ede6bac42730219a2df5db772814ff4185e5464ea33ebde225b8a068bbbb277c5201ba6f0e6f8e57fdf2733925ead1b54a86463073cb79c402fde101774577
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

### `dpkg` source package: `libtool=2.4.7-7build1`

Binary Packages:

- `libltdl-dev:amd64=2.4.7-7build1`
- `libltdl7:amd64=2.4.7-7build1`
- `libtool=2.4.7-7build1`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.7-7build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7build1.dsc' libtool_2.4.7-7build1.dsc 2389 SHA512:7617c6e809ba2cd2be45b5da2142386214c7c3badd4655efe135032706e285655a407eba20615e59173b36cf437039fbc2819e865a973a93fc2664b43cf0fa8a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7.orig.tar.xz' libtool_2.4.7.orig.tar.xz 1026028 SHA512:424f4549aa713917859dc31e62153934c67b8b9d5718452f0e50bb8f6ef48ae6274cc4d4ddd905b15858d19c60daf8c194471e6ed0c8f76e7d55e7ef932a8d3a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7build1.debian.tar.xz' libtool_2.4.7-7build1.debian.tar.xz 41052 SHA512:a96fff303067f7e0bb71534f5ec2777c737127cb6540a196a5cdad7dc1731a83d006b13addf0d4c422a4b2a7526df65a5f19ae52aa2063518871c6b04d7ece29
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

### `dpkg` source package: `libwebp=1.4.0-0.1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.4.0-0.1`
- `libsharpyuv0:amd64=1.4.0-0.1`
- `libwebp-dev:amd64=1.4.0-0.1`
- `libwebp7:amd64=1.4.0-0.1`
- `libwebpdecoder3:amd64=1.4.0-0.1`
- `libwebpdemux2:amd64=1.4.0-0.1`
- `libwebpmux3:amd64=1.4.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.4.0-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.4.0-0.1.dsc' libwebp_1.4.0-0.1.dsc 2569 SHA512:2617f5b32b95ce1b79180ef77076227bf984142acecfc727efbdb62b6ce18f3da01d7598cf7d27e218df9e413da048f17f61bb048ffc112ca6350d0d48b4462c
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz' libwebp_1.4.0.orig.tar.gz 4281370 SHA512:1217363fbb5c860b17c2ba4612f240f121c74ced6e3e58e8aa61252a9022f59893c5874bfa433cc50a7e65bac1ae2bfa99fa2cede070183b7a467f148cebb0bd
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz.asc' libwebp_1.4.0.orig.tar.gz.asc 833 SHA512:3cd635a25ff706055a6ac041f222cc7624d08cb9af125a9df1c721ffdb6820e829b95e87f61c7498facc64425f8c1149928661463eabc02929c6e9f0ac93f042
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.4.0-0.1.debian.tar.xz' libwebp_1.4.0-0.1.debian.tar.xz 11048 SHA512:8751e902b6ee0545cd6cafbe084b6bd53f11182576f12e84a4269c543311ba49003c0475362b0ced3a35b2b00cd6fd337afbbd0b03aaee384861175a3bd7a0d6
```

### `dpkg` source package: `libwmf=0.2.13-1.1build3`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1build3`
- `libwmf-dev=0.2.13-1.1build3`
- `libwmflite-0.2-7:amd64=0.2.13-1.1build3`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.dsc' libwmf_0.2.13-1.1build3.dsc 2635 SHA512:c14c4480ca692ed9652cb54f75bac5ddbb79dc9a4fc2c3661ee6d52979e1f5d6fe454c5df1a418838383fb1eff3fcf4b151f770d156cbd3fed5a01d557f09bc7
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.debian.tar.xz' libwmf_0.2.13-1.1build3.debian.tar.xz 25912 SHA512:0a2a4aeef81c7644eeebaa5ed800c26107472244667814477b153b0597c7fc9c8f2684e6e3a2bc4f3607e84adbcfa09c88116795eb21146b5fa792f0e87372be
```

### `dpkg` source package: `libx11=2:1.8.7-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1build1`
- `libx11-data=2:1.8.7-1build1`
- `libx11-dev:amd64=2:1.8.7-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1build1.dsc' libx11_1.8.7-1build1.dsc 2612 SHA512:a18064c14d2b134395187fb20df777148669e91b3d48ff92bff35ab120daa3ca267d9d66ca5dc43315714a395a978021669d4ced1ac3d77feb11f1861f4fd20a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA512:67575740356aecc6a7a4898e92ff1007aa6a44ff506d80fe577c1bdc3d64a900edf545cf3e082e9f17c25f4afe28e724145d5e82ae428bdc44348d368d9451a6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA512:92c410ca14412092680bd511f9536fcf1eb1f32632c33fb833246f8c90bb6dcb8045b9e12cbffa0b6093bf91fe8897ba76d2abb4303a343b4b7deb3b586098b4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1build1.diff.gz' libx11_1.8.7-1build1.diff.gz 74380 SHA512:009bf70e5acec4708f2d734f69c224674497c6a8eb9cbb2bff511ffb141fa79d3041e1dbcea669278626358ac03b9a918f5b4d8a03ac9ab49fd9c2ef792dcb9c
```

### `dpkg` source package: `libxau=1:1.0.9-1build6`

Binary Packages:

- `libxau-dev:amd64=1:1.0.9-1build6`
- `libxau6:amd64=1:1.0.9-1build6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1build6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build6.dsc' libxau_1.0.9-1build6.dsc 2315 SHA512:7cb47244c991544aed1268a831fbbd157713cbefb6252c8fe863522b6f1e3f1bd4dab892fbecdb253246c2fe34cd48a838b1139bdbc59e2cbd54cf1581af57df
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA512:3b22f34a4e35d17421189df8ce3f858b0914aef0cea0b12689dd8576f14eb811e39d6e32384251573daa7e3daba400deea98e7c0e29b4105138cf82195d7f875
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA512:e59b2944591499d0c0291a8d80ad8ee2cb13ee00c32b0d26c6af12a2bb96c947d4d15924ef15b377b8d7640b75b50f9b8127ba53c582090b3f73b7bcf9e00b01
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build6.diff.gz' libxau_1.0.9-1build6.diff.gz 10712 SHA512:49c075d30bcadd86ea03acc160824d06f32c65c5cd71e6f08ba2aece7ef719980f595f54f106d0c4d8e3d35d00e922289516907e7ba56741065253879faeba03
```

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2`
- `libxcb-render0-dev:amd64=1.17.0-2`
- `libxcb-shm0:amd64=1.17.0-2`
- `libxcb-shm0-dev:amd64=1.17.0-2`
- `libxcb1:amd64=1.17.0-2`
- `libxcb1-dev:amd64=1.17.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA512:5a54b2c0274d7914ca5d11eac94a3547d30e4428ddcdd78c8c8efb3ec2b206f1b26b7b66c2925c758fe426efd4960a017cffefbd5c51ac0a3f9e966d150b973b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA512:58624a33d39371a7ff58368ed5a09c1c31bea3abd040173db1d41018de4208bc52d2fb8cfd7382ff34d01b98d01a3e314a71a808533880564cd51cd96624a7bb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA512:60ca4c10826b430b7c43bc2de504b1e6d09d152b7a41325437f5017ce39093d78c72b70189162c814b888701686fa12c2de8d3489a4ffe5b9703cd001bb817b8
```

### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4build1`
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

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu6`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.3-0ubuntu6`
- `libxdmcp6:amd64=1:1.1.3-0ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.3-0ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu6.dsc' libxdmcp_1.1.3-0ubuntu6.dsc 2252 SHA512:daa70b073691db6046dfb0900d5dac63daa213b96b8e019e132dafc12d0cd0c9167c9216d823191ddfbabf16e6290073229f3b6ba310c86234a13e05c3cbc28a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3.orig.tar.gz' libxdmcp_1.1.3.orig.tar.gz 429668 SHA512:edd05654ad9ea893e9e08269e25ea050d10eaf9f997a08494e24127d1ba0c896cd5338b4595b155c8cbf576e1d910b76e6ad7820fee62d74644f1f276551e2f2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu6.diff.gz' libxdmcp_1.1.3-0ubuntu6.diff.gz 18400 SHA512:5b6effc30e3f6dba946dd95c73d3242210d99612aec3dc8df4fe986a42758e7d9c6ddc7a713375edb0c78a1875e64872ca9329c8d5be83984c66e8457c355c23
```

### `dpkg` source package: `libxext=2:1.3.4-1build2`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1build2`
- `libxext6:amd64=2:1.3.4-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.dsc' libxext_1.3.4-1build2.dsc 2250 SHA512:6b9b001f4dd81843f12ca625bb90a8ea78dda531f80d6fc9c90c071b6cc925d94c53b2d20abc42d21df77904ff5ba059025ce426cf25838918040da71b1a6ea4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.diff.gz' libxext_1.3.4-1build2.diff.gz 12720 SHA512:6ec71960a93504538ef944620b0af7bb2ffdf21270ddaf1715dec4faf79d0d1ec1372a148e9acb64a014b2a761eadf01f0b83955dda7ff2fdf942b5998bd1b34
```

### `dpkg` source package: `libxml2=2.12.7+dfsg-3ubuntu0.2`

Binary Packages:

- `libxml2:amd64=2.12.7+dfsg-3ubuntu0.2`
- `libxml2-dev:amd64=2.12.7+dfsg-3ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.12.7+dfsg-3ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg-3ubuntu0.2.dsc' libxml2_2.12.7+dfsg-3ubuntu0.2.dsc 3095 SHA512:602944d2958c96064cb5d307f5ef1aa6c9e5d37ab1ab7ec9ad3a9ca99011deaef7f97e5fe147ba9042429db1b6fca2342aff4abe241285ca9ad93c1fcda46356
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg.orig.tar.xz' libxml2_2.12.7+dfsg.orig.tar.xz 1810596 SHA512:0973a4079490d1252825d2faf79c0a517c7aa126f6efb42ca93562624b22fcfb95ef13144450e2cf03cf44205a557dafe30760f3faf92b0b0ea43083e541157a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg-3ubuntu0.2.debian.tar.xz' libxml2_2.12.7+dfsg-3ubuntu0.2.debian.tar.xz 29736 SHA512:27c1fa39d082481873aae4bbe4625e062385603571db092ff91fa8b56ad63f29ab2aad0ee00aa02716454348011e24a9c6a5cdce53c286045b305faedb5295af
```

### `dpkg` source package: `libxrender=1:0.9.10-1.1build1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1build1`
- `libxrender1:amd64=1:0.9.10-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.dsc' libxrender_0.9.10-1.1build1.dsc 2204 SHA512:ac21ce52dc62e66c8e0e6c94c727a978b8b285755dd7c3de9b8bd34057bdef1ee23acdfbdd3efb2052734b763904c02e98cd71b4b0bb28a1673a6da3eb7cb8f6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA512:7768e62b500f468460f88f27bc1130170b204b478573d9e4406867e557b5638b7c1e21d88d51f9e774ce2344780a384e3c3be51421275d2ee880f9a978a3a232
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.diff.gz' libxrender_0.9.10-1.1build1.diff.gz 15274 SHA512:dca2b6bf90a6ce1ec30376a001f6f24f2d95e917c3a4890242022bf5eefa20c9c1e775c66c229cbb7ee47482650b9a0a750e7bf1890aec89d3bec6b692f4174a
```

### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu1.2`

Binary Packages:

- `libxslt1-dev:amd64=1.1.39-0exp1ubuntu1.2`
- `libxslt1.1:amd64=1.1.39-0exp1ubuntu1.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu1.2.dsc' libxslt_1.1.39-0exp1ubuntu1.2.dsc 2283 SHA512:753a62225fc9cc57c667a1f563796eeef1a681424015e3aab100ece79988bda70df54b1816b5923d3713279e5e3c7d9edd2d573e12723e7a5f58af74946f2b81
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu1.2.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu1.2.debian.tar.xz 23508 SHA512:3aaef7bfcaf78da862534e435d009f6b3310e3ca3936417e771464741a90df85e46f844fa3374e25444d2a6c85e37154520b37403a78d05efa7bb1ce84fc2812
```

### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2build1`
- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.dsc' libxt_1.2.1-1.2build1.dsc 2488 SHA512:ebe5d28a22400920f1ce994c3977affdb7da2033a8a6fe0d8b460b90d9eb37de4053843c9e6cc0addd0e712928870eae79d7bdbed0690577701f6d1bca400265
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.diff.gz' libxt_1.2.1-1.2build1.diff.gz 45676 SHA512:e16fcaaba4f0574d31b7418b2a364a09eb9cee3008c4022a09ebd606ee2eecdcbb49c8e1562f1479b1eda5bdea977b3777c384848c21c437793a6a76cc007467
```

### `dpkg` source package: `libyaml=0.2.5-1build1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1build1`
- `libyaml-dev:amd64=0.2.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1build1.dsc' libyaml_0.2.5-1build1.dsc 2203 SHA512:872e28e7564a127ef6da7a47c401d2cd7a339d789b2e8fa6c514baad5fa986e96698661649e77fbfcdc31e38c1bea058fb1e004d7b2340854802bc90bfcae3f6
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1build1.debian.tar.xz' libyaml_0.2.5-1build1.debian.tar.xz 5496 SHA512:d1b42bf0a1076d970298ca762a51f57c1ed76a2eac44d5385928709ce5876617f2629dab7841f8e1b6837264098cfc4c9c2aa214466f781b66077fa1979c809a
```

### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd-dev:amd64=1.5.6+dfsg-1`
- `libzstd1:amd64=1.5.6+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

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

### `dpkg` source package: `linux=6.11.0-21.21`

Binary Packages:

- `linux-libc-dev:amd64=6.11.0-21.21`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.11.0-21.21
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.11.0-21.21.dsc' linux_6.11.0-21.21.dsc 8412 SHA512:b99c10c29eaf75b89d8dc843c42aa6019e139b52a4abed169d44552d1832200e89fc26a1c56416d48d74771a914fcba2e335cf6b1cff0c66451250912cf8c5bb
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.11.0.orig.tar.gz' linux_6.11.0.orig.tar.gz 238316413 SHA512:3bde6385b17f326180c78de6afc98425b60a19dbdfcebf4cc4dd42cae8b99a696ab3537a78d81df25b484bb30bc260ac6132e86d61f28c4032672b308b36e546
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.11.0-21.21.diff.gz' linux_6.11.0-21.21.diff.gz 2998489 SHA512:2807a8c751ec4171f5d0521f4a0d1098102bb72d15d21ae399d2c9a5e685b6c5521dcce39345c90a2579045f178d74fd64e77f71054aa03240c92a167404d877
```

### `dpkg` source package: `lto-disabled-list=53`

Binary Packages:

- `lto-disabled-list=53`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=53
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_53.dsc' lto-disabled-list_53.dsc 1435 SHA512:ed4c6db868275b58a8493d9e2729682745d8fe21388f4674651dfdc7cfc702e983c7a8fcb44c52e6f356c420b9729b300b96f404c357d6759a4a3cbebfc35578
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_53.tar.xz' lto-disabled-list_53.tar.xz 13624 SHA512:94cdbd05ba24d832435983b8799d37ab48182e026191bae2adf2282daa6f9bdc94201abba635725bd8a68be606501fb69b02716274b582375d22a6cc542a4533
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

### `dpkg` source package: `lzo2=2.10-3`

Binary Packages:

- `liblzo2-2:amd64=2.10-3`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-3
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-3.dsc' lzo2_2.10-3.dsc 1923 SHA512:fde8fa4920e2128fb34f7543e72a10adc8bb7467d33db7ba0edc0707b225c436df69e8e5b9e6a470f7ad73b15f203d1162d172f85806059b6b510bb5f59b8ad8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA512:a3dae5e4a6b93b1f5bf7435e8ab114a9be57252e9efc5dd444947d7a2d031b0819f34bcaeb35f60b5629a01b1238d738735a64db8f672be9690d3c80094511a4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-3.debian.tar.xz' lzo2_2.10-3.debian.tar.xz 7228 SHA512:11a28d17b6167f2abcf5d9f3c8ce688ea7e74b81e775b0ac62233432747294ead7f6f856d8f2f13ba3694b86444a865b7e10883efe0423098be0d2a08e121f4f
```

### `dpkg` source package: `m4=1.4.19-4build1`

Binary Packages:

- `m4=1.4.19-4build1`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4build1.dsc' m4_1.4.19-4build1.dsc 2114 SHA512:af4b77797c56d650ba50831f6730de1b45c9ee9a22e6875db30145b46c972b94507fc075b1ecfeee75c47616b3aaba5a9247d4c4989e1fe33ad33641613ad87d
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA512:47f595845c89709727bda0b3fc78e3188ef78ec818965b395532e7041cabe9e49677ee4aca3d042930095a7f8df81de3da1026b23b6897be471f6cf13ddd512b
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA512:d6ac9c6a54c57e9b53fb3e34a60d49df2f46a6e494da0a0c9ae8246b984e68a853b5d8c42677c1a0485c3f36b0bce10a481d3775c0edc1dbdfb27b43545bc31e
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4build1.debian.tar.xz' m4_1.4.19-4build1.debian.tar.xz 17460 SHA512:cd8501c3323749074e702ced7c648506034f69e25442b648876aa46a186b9ff613e969a737437757ad8595b660aa298e677c8ebfd4dc8797a36510acc3d359f9
```

### `dpkg` source package: `make-dfsg=4.3-4.1build2`

Binary Packages:

- `make=4.3-4.1build2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build2.dsc' make-dfsg_4.3-4.1build2.dsc 2151 SHA512:78402aabf7f2d9cf40f9bc2ecb5d0063e005ce8ecd131145863dd4c57c2f78ecdc0d98f8c78861903472b211f37975c6004a05fc88c9bce1c6f405569aca89cb
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA512:bdc150f9d256145923380d6e7058ab9b2b4e43fcb1d75ab2984fa8f859eab6852a68e4ea5f626633e0bec76fbebf1477378e268e8ffdb5cb2a53b29cbc439bc1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build2.diff.gz' make-dfsg_4.3-4.1build2.diff.gz 50933 SHA512:84074f8c50818009fc0beeb1a61bb74d9fba8b277f2911cfb20ba1f5807e72f18d83b69a318b0799bd3568d0756e790c8a27d09d382b8379d79a22ad58db5f9e
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

### `dpkg` source package: `mpclib3=1.3.1-1build2`

Binary Packages:

- `libmpc3:amd64=1.3.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build2.dsc' mpclib3_1.3.1-1build2.dsc 1955 SHA512:0db012f9a6b64579eb2b40419184495e975f985b33b286410ba061ccca30581d1af1b9a6de0b6c258df8763103bfc58c9acfef89220df403c365d2626edecc46
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build2.debian.tar.xz' mpclib3_1.3.1-1build2.debian.tar.xz 4824 SHA512:60e8bb220559964234c5c844ae684d7a1a1dadd23bff6c977f40bfa6f83e137055339b483c11182588a166aee55feb3c260075a0eeedf3df5f0e951694da945f
```

### `dpkg` source package: `mpfr4=4.2.1-1build2`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build2.dsc' mpfr4_4.2.1-1build2.dsc 2037 SHA512:31ec6ede37f6dbd315d965ff3a51fa6e228e91c76cb337b77963f3ec15e6b8ee69e3034858977bf21a6b2696579fd56e81f9d16a07caec7052cf0738be5ba6dd
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA512:bc68c0d755d5446403644833ecbb07e37360beca45f474297b5d5c40926df1efc3e2067eecffdf253f946288bcca39ca89b0613f545d46a9e767d1d4cf358475
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build2.debian.tar.xz' mpfr4_4.2.1-1build2.debian.tar.xz 12748 SHA512:2e4e2edb471230785fee71b9cfeea9d1cb16736dfab7d3d62874ea251f763aa9f9500da24cdff0906070d90ddcec084ed9753784797c49727fadc6f8605934f2
```

### `dpkg` source package: `mysql-8.0=8.0.41-0ubuntu0.24.10.1`

Binary Packages:

- `libmysqlclient-dev=8.0.41-0ubuntu0.24.10.1`
- `libmysqlclient21:amd64=8.0.41-0ubuntu0.24.10.1`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient21/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-like`
- `Boost-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `public-domain`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mysql-8.0=8.0.41-0ubuntu0.24.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.41-0ubuntu0.24.10.1.dsc' mysql-8.0_8.0.41-0ubuntu0.24.10.1.dsc 3866 SHA512:c9a6285c17e0d8d75d3e0f1860672d4bb19651253ea681695cd4501ade4baacf8a35bf0516f441e1ee4e57df2755ddb3960bc01344515e543a7dfd0eddcccef0
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.41.orig.tar.gz' mysql-8.0_8.0.41.orig.tar.gz 488749630 SHA512:e5bb314082be6bf037808ea7a2130c8e2b44491a6c54bc3f611d823be5285021d05093afca71c3d33da6dece2bac3a8e24da5198080060407d8c4dbfeeea8a99
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.41.orig.tar.gz.asc' mysql-8.0_8.0.41.orig.tar.gz.asc 833 SHA512:2e9a6eea9dc6a001c7ebf505960d2c41aa1806d7400be234c9db74771950e7e54e8f2a13d93ba931496ebc4b27cd99fe2e2ccf7fbf1f7119faa94d66fb87307d
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.41-0ubuntu0.24.10.1.debian.tar.xz' mysql-8.0_8.0.41-0ubuntu0.24.10.1.debian.tar.xz 145832 SHA512:5d0eeb4d1e27ed0f5f2659a88046a92679d139139c34999bf5ebf1b8c15fdb285cb598bd06ef221af3b4c635370a73f0a2347945055cb2f3c068e99a452c24e4
```

### `dpkg` source package: `mysql-defaults=1.1.1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1`
- `mysql-common=5.8+1.1.1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.dsc' mysql-defaults_1.1.1.dsc 2202 SHA512:ad3993ddeed3e8bfb9a0a050205814e546a6f5166a6058085256255ed3cf5fa919f6d55faa421983ae70bd5de2288dd1a1bcc9ae578548408a9a562c84791a1a
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.tar.xz' mysql-defaults_1.1.1.tar.xz 7460 SHA512:45ef13a37506a51065662002b97a45fa2acc185e149312c173839d1c50d0a89dfe4fede4022403f5367139e2513fe5b8c706104be35b4bcdaffd2644d0725637
```

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libncurses-dev:amd64=6.5-2`
- `libncurses6:amd64=6.5-2`
- `libncursesw6:amd64=6.5-2`
- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

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
- `nettle-dev:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`, `/usr/share/doc/nettle-dev/copyright`)

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
- `libnghttp2-dev:amd64=1.62.1-2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

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

### `dpkg` source package: `openexr=3.1.5-5.1build3`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1build3`
- `libopenexr-dev=3.1.5-5.1build3`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.5-5.1build3
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.dsc' openexr_3.1.5-5.1build3.dsc 2629 SHA512:6754aafb095ee18dbd5f3df736e9e619af5189e3fb6d61245d64d18aaec9874e23b75daa51b8e55b61c93732163575f85496e1e61baf97de1470939dfe8eae8e
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz' openexr_3.1.5.orig.tar.gz 20327926 SHA512:01ef16eacd2dde83c67b81522bae87f47ba272a41ce7d4e35d865dbdcaa03093e7ac504b95d2c1b3a19535f2364a4f937b0e0570c74243bb1c6e021fce7b620c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz.asc' openexr_3.1.5.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.debian.tar.xz' openexr_3.1.5-5.1build3.debian.tar.xz 18952 SHA512:717a1362e1150abf4d555725539bd4b873591646f1c48859c200cb9a7b46946e00824d58ce68cb5dbee4ab3231e77f01cb75624a3eca99f633a4a99ba72e4e09
```

### `dpkg` source package: `openjpeg2=2.5.0-2ubuntu1.2`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2ubuntu1.2`
- `libopenjp2-7-dev:amd64=2.5.0-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.0-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu1.2.dsc' openjpeg2_2.5.0-2ubuntu1.2.dsc 2833 SHA512:a80c4914f1db33e47c0f1fa1105b19fa5ef781ef92daa42f09364bcb4f5853a88ef02eeda52467b1bc17e555557fefe790def0ca1106a49fbe9976a4e76e0459
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0.orig.tar.xz' openjpeg2_2.5.0.orig.tar.xz 1221108 SHA512:a266297d60ff93e14dbee890b01a76870bda69f082dbe8932fc444ccd260c27aaaac8b22e3c00ca71930b2555a1cad6cf6ed0d5d882d9d13f472cc494cab8234
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu1.2.debian.tar.xz' openjpeg2_2.5.0-2ubuntu1.2.debian.tar.xz 20000 SHA512:4d9181a730534d50e36a9c574a74739ee205bf4c7a8f71efd4b9adefa679ef340fae71cabc2898801bd374aaa4c35d3cf58be50c7718ff559b594b05635dacb2
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

- `libssl-dev:amd64=3.3.1-2ubuntu2.1`
- `libssl3t64:amd64=3.3.1-2ubuntu2.1`
- `openssl=3.3.1-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`)

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

- `libp11-kit-dev:amd64=0.25.5-2ubuntu1`
- `libp11-kit0:amd64=0.25.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit-dev/copyright`, `/usr/share/doc/libp11-kit0/copyright`)

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

### `dpkg` source package: `pango1.0=1.54.0+ds-2`

Binary Packages:

- `gir1.2-pango-1.0:amd64=1.54.0+ds-2`
- `libpango-1.0-0:amd64=1.54.0+ds-2`
- `libpango1.0-dev:amd64=1.54.0+ds-2`
- `libpangocairo-1.0-0:amd64=1.54.0+ds-2`
- `libpangoft2-1.0-0:amd64=1.54.0+ds-2`
- `libpangoxft-1.0-0:amd64=1.54.0+ds-2`
- `pango1.0-tools=1.54.0+ds-2`

Licenses: (parsed from: `/usr/share/doc/gir1.2-pango-1.0/copyright`, `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpango1.0-dev/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`, `/usr/share/doc/libpangoxft-1.0-0/copyright`, `/usr/share/doc/pango1.0-tools/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `Chromium-BSD-style`
- `Example`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OFL-1.1`
- `TCL`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.54.0+ds-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-2.dsc' pango1.0_1.54.0+ds-2.dsc 3671 SHA512:73ea4bc8a6130ba94ca5c793a2822a59754242d0d5affa5bb04a5cca6e94eeb01b2cf37105a62a1b047e9d720ecf17cbf32fec14b496f0a403c0da71f203645f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.54.0%2bds.orig.tar.xz' pango1.0_1.54.0+ds.orig.tar.xz 1745280 SHA512:05b294e946d6eea593f593a8be3b221b28ed08330bbc1dddb50439971697ac8976acef54622123c94cb7f1a2d73d900e9f3c7aa10c941c93049beab5d3b36762
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-2.debian.tar.xz' pango1.0_1.54.0+ds-2.debian.tar.xz 43800 SHA512:d696b3368c831d1230b221c01ff4c8222dba3054343e8df5144ba2724e785302a46ee9203c47130ff1c7cd1222f92baac3eaeb53e0d4c8ae1a28022aac7c1705
```

### `dpkg` source package: `patch=2.7.6-7build3`

Binary Packages:

- `patch=2.7.6-7build3`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7build3
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.dsc' patch_2.7.6-7build3.dsc 1838 SHA512:205ad1e6f47a5c039c878387f95ee3a91e2115ccd740f6d2e6ce0b7d9996bad38332739418e3cb70d215f93a083c3fc5174269893f5d3e200caf18ef0d8e1f05
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA512:fcca87bdb67a88685a8a25597f9e015f5e60197b9a269fa350ae35a7991ed8da553939b4bbc7f7d3cfd863c67142af403b04165633acbce4339056a905e87fbd
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.debian.tar.xz' patch_2.7.6-7build3.debian.tar.xz 15324 SHA512:46d2d3d5da88ddf723891df3288165405794cf414c6fdad65723a0f7333e918676a04eaa254d2dbc7b682e4e214d6089af461b490c51a5c8e7e02d4743b4249f
```

### `dpkg` source package: `pcre2=10.42-4ubuntu3`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4ubuntu3`
- `libpcre2-32-0:amd64=10.42-4ubuntu3`
- `libpcre2-8-0:amd64=10.42-4ubuntu3`
- `libpcre2-dev:amd64=10.42-4ubuntu3`
- `libpcre2-posix3:amd64=10.42-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

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

### `dpkg` source package: `pixman=0.42.2-1build1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1build1`
- `libpixman-1-dev:amd64=0.42.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1build1.dsc' pixman_0.42.2-1build1.dsc 2153 SHA512:433d3a48159ab6d981bc4a6c40abfb7cef8aa6ca7c893420042d071e1c236ad78471df956ac83d2e88df25e107b36b3ce808fa97bc701178804d452523ba0826
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA512:0a4e327aef89c25f8cb474fbd01de834fd2a1b13fdf7db11ab72072082e45881cd16060673b59d02054b1711ae69c6e2395f6ae9214225ee7153939efcd2fa5d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1build1.diff.gz' pixman_0.42.2-1build1.diff.gz 327276 SHA512:a07846ba47b3f3407e43aefee37efe6265445a8c1e81589a715f175e426ed2a75822cce7545ac94bb368c3eecaaa2ccd7b0c7944aba9b51f0e939403b2f57d1e
```

### `dpkg` source package: `pkgconf=1.8.1-3ubuntu1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-3ubuntu1`
- `pkgconf:amd64=1.8.1-3ubuntu1`
- `pkgconf-bin=1.8.1-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-3ubuntu1.dsc' pkgconf_1.8.1-3ubuntu1.dsc 2237 SHA512:4ee585ec931665c1638d805281dc2f2192848af037f10bf685c92daeb5087275c065430bdcb4c054df2f9765fec684f20fc8d2988b2cf6a8937a30ed796e6952
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-3ubuntu1.debian.tar.xz' pkgconf_1.8.1-3ubuntu1.debian.tar.xz 17752 SHA512:54172e152e4b1a9ba0e915a8bd49f447af0d7b2b0a3341fc64e76a2c82eb8a1283bdf65622cf22e05cfec676e21732fc5d956c41cace3c9b7a3b47b31296cd5c
```

### `dpkg` source package: `postgresql-16=16.8-0ubuntu0.24.10.1`

Binary Packages:

- `libpq-dev=16.8-0ubuntu0.24.10.1`
- `libpq5:amd64=16.8-0ubuntu0.24.10.1`

Licenses: (parsed from: `/usr/share/doc/libpq-dev/copyright`, `/usr/share/doc/libpq5/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Custom-Unicode`
- `Custom-pg_dump`
- `Custom-regex`
- `GPL-1`
- `PostgreSQL`
- `Tcl`
- `double-metaphone`
- `nagaysau-ishii`

Source:

```console
$ apt-get source -qq --print-uris postgresql-16=16.8-0ubuntu0.24.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.8-0ubuntu0.24.10.1.dsc' postgresql-16_16.8-0ubuntu0.24.10.1.dsc 4409 SHA512:6447436f94faeb3042b3d383782e3b518ad4aa9635e150be9ad4c0cfc44cb1e331b04518a38e9190c4fc8a445dc12c51edd725e501c4de52cb462a22d3e9a4e7
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.8.orig.tar.gz' postgresql-16_16.8.orig.tar.gz 32765514 SHA512:16758b3d4a0aa8fd693dfb09abc0c6fb5ffc768138d2dc0266f7d697fea12efd5b6bbfb2ef77ea3d804745e4b4085bbd26b4acf972c5e6207f8c6a29bf9c8c93
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.8-0ubuntu0.24.10.1.debian.tar.xz' postgresql-16_16.8-0ubuntu0.24.10.1.debian.tar.xz 34812 SHA512:4f56777f3b67cf58579254b739694ba3cbe8ad898d27328562ff4f730898451bfe25c80ab6421562c39da78412211be0aefdac01b409aa5d402be9854368971e
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

### `dpkg` source package: `python-packaging=24.1-1`

Binary Packages:

- `python3-packaging=24.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=24.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.1-1.dsc' python-packaging_24.1-1.dsc 1932 SHA512:7226d603362eec1c608f911ba792577aaa3250584f4ea859ee12a9b30cd7741d1e3e2bfba5aded8e629e783cf5c8dffc856bed13ad24b831bfa34e3a5446c8c8
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.1.orig.tar.gz' python-packaging_24.1.orig.tar.gz 148788 SHA512:fba8b94c1798c380c6af2c7fe211137fcc5669b1af3b0de52d6bcba05907f5bc74693df740677213d6c230e8d2db48ab9c4b8309752813c25cee87f1622fd4ab
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.1-1.debian.tar.xz' python-packaging_24.1-1.debian.tar.xz 2948 SHA512:0daa0fdefc99b15982f6ea9cf3e38e75385f7ea66c9355c1db748860c74c33187bd178b0b0ad12a84fe315ee6542b67c97500530fa6faa067f05208eaf33d0cf
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

- `libreadline-dev:amd64=8.2-5`
- `libreadline8t64:amd64=8.2-5`
- `readline-common=8.2-5`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

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

### `dpkg` source package: `rpcsvc-proto=1.4.2-0ubuntu7`

Binary Packages:

- `rpcsvc-proto=1.4.2-0ubuntu7`

Licenses: (parsed from: `/usr/share/doc/rpcsvc-proto/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.2-0ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.dsc' rpcsvc-proto_1.4.2-0ubuntu7.dsc 2113 SHA512:898f925a91776d16b8f6934b502f0a05983079af42a633245d2f5e25975daf3eece0be7a999dc640739b0c29315a657d33c1d5e5ed03e74ab5b911638571a96c
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2.orig.tar.xz' rpcsvc-proto_1.4.2.orig.tar.xz 171620 SHA512:631fbfc00af94c5d7def0759f27e97dc14d400b4468c906719ae18ecef74815730798c882d1aaa4f90359224e7b829019b786baddc3097905b54f940ca85a714
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz' rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz 4336 SHA512:faf9f6eb4e7da5e4fed0e358e836cc4137f783079127cbabe3bed82f8ad2d08250d827d62f0f49df23604d685b7c55d6c30b8ec69dff0f14e3267ae180cb9f96
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-2build7`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

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

### `dpkg` source package: `shared-mime-info=2.4-5`

Binary Packages:

- `shared-mime-info=2.4-5`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-5
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.dsc' shared-mime-info_2.4-5.dsc 2237 SHA512:57108936794b1dbeedec4865416a59ef045fd0c81e1f34f2af965968245cbe0e0e71616a26c4f6fd34f0fd25283fa0935d90e683af11111dac865627e584b714
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA512:712f414e80919bf2a0f5083ced44c54a350948a526850466a6e9f35365dcfd97fad8bcdbb29945de2715a8f9b70a108e931c8500209a4d6e3dddf97af02771cb
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.debian.tar.xz' shared-mime-info_2.4-5.debian.tar.xz 10812 SHA512:842d469aec8fc0972357b3c4bb6a3704693c42635df62ab2e1d664e0afe52031e7fc067cff6cbb09a35d7b5c108c07ba301b6974b9589969228199a3945c7428
```

### `dpkg` source package: `sqlite3=3.46.1-1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-1`
- `libsqlite3-dev:amd64=3.46.1-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

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

### `dpkg` source package: `sysprof=47.2-1~ubuntu24.10.1`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=47.2-1~ubuntu24.10.1`

Licenses: (parsed from: `/usr/share/doc/libsysprof-capture-4-dev/copyright`)

- `BSD-2-Clause-Patent`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-3`
- `LGPL-3.0+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sysprof=47.2-1~ubuntu24.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_47.2-1%7eubuntu24.10.1.dsc' sysprof_47.2-1~ubuntu24.10.1.dsc 3138 SHA512:b65a7c468c3555d2e5ef9b6b3ab75df3faaab2dc3389d7d41be10576918f1a6f8034898de8a6961f6bb6da9ac791ba0b90f7debcaa4131ef5ca66d30b2671d84
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_47.2.orig.tar.xz' sysprof_47.2.orig.tar.xz 1192172 SHA512:3673b8035ba115f581c3d4d881a6ac99f15d96d461f5d0824d727cfb504ae41363c5b5e0fc117acd202b203c251bb514e53307799c1dbea1d2b0d320ed2fd104
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_47.2-1%7eubuntu24.10.1.debian.tar.xz' sysprof_47.2-1~ubuntu24.10.1.debian.tar.xz 16712 SHA512:130baf965c2cd42d56633e579b02f20c2d96e1464e6477c6af85c7d71269c28939c500e4b5febff97596e423da1a3b88d5938ff3baa3a764724c9a5e2185c706
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

### `dpkg` source package: `tiff=4.5.1+git230720-4ubuntu4`

Binary Packages:

- `libtiff-dev:amd64=4.5.1+git230720-4ubuntu4`
- `libtiff6:amd64=4.5.1+git230720-4ubuntu4`
- `libtiffxx6:amd64=4.5.1+git230720-4ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu4.dsc' tiff_4.5.1+git230720-4ubuntu4.dsc 2435 SHA512:04aa0fc51de733bf4f6dc468eb8b247352f0968f0c62bd55933b95eb5200b311736d1e765115f329406f76ffb0eba90b4aedb3c67ed912c21ff053d1eebfcadd
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA512:6bf9653f5c65d17c2944b20d14a5d5ab3b89d461bc6eb935a54aa8df99ce7221aeb2172f06b44affd06d81aeaab5698b90b07fde883167d0abf51debaaa6f71b
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu4.debian.tar.xz' tiff_4.5.1+git230720-4ubuntu4.debian.tar.xz 29972 SHA512:6e7398bd9108946b8ad5d95b1a6af62408a2f8577c41102e78bb2a483a3e114964745f7b1190a26d8609a2f8f9265dc57170015a68a203785a74af7692090843
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

### `dpkg` source package: `unbound=1.20.0-1ubuntu2.3`

Binary Packages:

- `libunbound8:amd64=1.20.0-1ubuntu2.3`

Licenses: (parsed from: `/usr/share/doc/libunbound8/copyright`)

- `BSD-2-VUT`
- `BSD-3-ADG`
- `BSD-3-CZ.NIC`
- `BSD-3-Farsight`
- `BSD-3-NLnetLabs`
- `BSD-3-NLnetLabs-Mekking`
- `BSD-3-Regents-DEC`
- `BSD-3-Todd-Miller`
- `BSD-3-VUT`
- `BSD-3-Viagénie`
- `BSD-3-WIDE`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris unbound=1.20.0-1ubuntu2.3
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.20.0-1ubuntu2.3.dsc' unbound_1.20.0-1ubuntu2.3.dsc 3045 SHA512:52e9109f2f927593759f655efb82e07dcc74a315e4db0ba3bf2ad7227ddb7a526f7b09cf323ceb61862a3a482fda37d1031202b6254680f6018f16a534eb171b
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.20.0.orig.tar.gz' unbound_1.20.0.orig.tar.gz 6550938 SHA512:2f6bc76c03b71ca1c2cd2331dc72d62f51493d15e17c59af46b400e542fcabff22e6b9d33f750a3e5f918a0116f45afa760651b2d5aa2feadac151cbbd71b0bd
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.20.0-1ubuntu2.3.debian.tar.xz' unbound_1.20.0-1ubuntu2.3.debian.tar.xz 33784 SHA512:f64af61ce33709b0881883ee25394da1ccef4e5ca4bfbb9806c8554be53c89b75b3bf672e77a300dcc7cd701007205b0d6a54b4a1b2ef8019e079f27f1d1f4ff
```

### `dpkg` source package: `unzip=6.0-28ubuntu6`

Binary Packages:

- `unzip=6.0-28ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu6.dsc' unzip_6.0-28ubuntu6.dsc 1883 SHA512:ea06f2ade23550e63c60fc72ea78226c53bf75e4fe309f94949e80177130a1a3752c341645c9df2febdd7d75508a3ef12ff6094606b317d061f569c219101dd6
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu6.debian.tar.xz' unzip_6.0-28ubuntu6.debian.tar.xz 47148 SHA512:c45fdf158c89a3a8199d41d33e7c960e6689242ad00d48b8cb82815ab5e12384e8e3c5b1b3d6e3d83b37add7dda881cdf9a412b3201b03397322c95fe3d11fd5
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
- `libblkid-dev:amd64=2.40.2-1ubuntu1.1`
- `libblkid1:amd64=2.40.2-1ubuntu1.1`
- `libmount-dev:amd64=2.40.2-1ubuntu1.1`
- `libmount1:amd64=2.40.2-1ubuntu1.1`
- `libsmartcols1:amd64=2.40.2-1ubuntu1.1`
- `libuuid1:amd64=2.40.2-1ubuntu1.1`
- `mount=2.40.2-1ubuntu1.1`
- `util-linux=2.40.2-1ubuntu1.1`
- `uuid-dev:amd64=2.40.2-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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

### `dpkg` source package: `xft=2.3.6-1build1`

Binary Packages:

- `libxft-dev:amd64=2.3.6-1build1`
- `libxft2:amd64=2.3.6-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6-1build1.dsc' xft_2.3.6-1build1.dsc 2138 SHA512:448b5bf2f9d7b9245c70b0f81c82e4bf96f8f7bba4888bce5b7ad4dcaa0a568786b979bf59e2b6cbcf3d71adaba1a310fd4e4fd61ecc737c72fec8880a545cfc
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA512:291bec2cc297a6e39baff5c2dec37017f37f97b438468a6d6b66f496a9987936da6ee2e3ace77e4527d8c5fd09e1dd731b2f042fa74880f667b8a03a913512d2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6-1build1.diff.gz' xft_2.3.6-1build1.diff.gz 18138 SHA512:c8566508d00ba5a57436311ccb862e8dbb9701a0f01ed787dec62ed24ca29c9c76835537b2997165e842e07aa22285b9e3183000347e777108e6d4f58d7992e0
```

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.dsc' xorg-sgml-doctools_1.11-1.1.dsc 1987 SHA512:1682e1a4d4be1bfb1242adfa22b2764a9425b035cbfae9fd58925d4904eb301fe48bf92fc5935e973d7653db001ab221a8eac8cc5e2840d5a2e0cb4f1bb4895c
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA512:a2386e41a8e2f7deaded61e00eaeab922647c0d0f4e36268c4337dc71d2412b0ec433140d080a0fd118b6112ed0a4f960280f932fe8d4a90ea9dc8bedf1eb75e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.diff.gz' xorg-sgml-doctools_1.11-1.1.diff.gz 3296 SHA512:0ea09f6de75cf649fb82705a0470e5ba04edbe59ccfa26132e60120e04036b86e9ff47785fdcee2499fa005cbbdfc9e04ebdca619d0253ea558e2fe5501b9ec4
```

### `dpkg` source package: `xorg=1:7.7+23ubuntu3`

Binary Packages:

- `x11-common=1:7.7+23ubuntu3`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.dsc' xorg_7.7+23ubuntu3.dsc 2095 SHA512:dd0091767574109a7e1308a0222f8e5115529baa9def0d822f9812c1761eb43b03caa440ba80874a9c1470a52911e94e6e03f52dc94cf2339006e6bd9ea372a0
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.tar.gz' xorg_7.7+23ubuntu3.tar.gz 301634 SHA512:16e7194bcbbc38f185130de2115817c2a34238a1541bbfff08239b0a84e3a5637d907dc1465556061645c6ff0845c47047231a0b384758162ace93d20db6e4d0
```

### `dpkg` source package: `xorgproto=2024.1-1`

Binary Packages:

- `x11proto-core-dev=2024.1-1`
- `x11proto-dev=2024.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-core-dev/copyright`, `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2024.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.dsc' xorgproto_2024.1-1.dsc 3336 SHA512:2e7799b28e6267936afdc2b1926c40326d5bc3040801f57e41fee6ab32ed2d49df8a36c42900604e3f4f19c0d4ae0fbee611cadff3c7da365f0beeea9c331fc1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz' xorgproto_2024.1.orig.tar.gz 1115486 SHA512:c2d67a98c5ba9b2f4d0b844c96dab342c497710753a8878b75dbf12ecd64b105c9ee3c5fd11eb91e45960420cf8dd7d02547072a32d5c53e58e009394fe33666
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz.asc' xorgproto_2024.1.orig.tar.gz.asc 195 SHA512:9dc7d40a50178f65b47bcd9a360b85f8d40f30e9151bf242d2eef9a12a3d8e5a1488af7e0c0c4c1dbc3e6cb447acd0735fe749290c46d021b4d7e10de3912a33
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.diff.gz' xorgproto_2024.1-1.diff.gz 25061 SHA512:0ba012c2ecad1f6b23d6286c76cfc7f130635e8d30cdb6b2a9a7cb7a0731bb17a5f974d4dcab8efbd104977d95d438295f850c0242d7f46b64a1562891766a08
```

### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA512:ac171ce0f00e1741e97a4ddad630ccff69070c0ef60047071b3f940fad08cb468d5ded7b2d4f0f500aeda73f2b703d55a7a4bbe0d5fff88cc3381486a111f580
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA512:21287ccf18fe2ebd458765496b026d175bf47c6e8e5c21d5b9ea17203967efc0cf6928fa2f3385d289a680c7002c3640e4731937029e99933c2a64bb9fab5326
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA512:d6deaa9579fb61e6ffd296ffe6b083eb9de572001c0a5bc82229ecc3d50bf2ee2f6504b3daa533bd34f3d647d6bd2235728084ec0b59869f6446652b998797f7
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

### `dpkg` source package: `xz-utils=5.6.2-2ubuntu0.2`

Binary Packages:

- `liblzma-dev:amd64=5.6.2-2ubuntu0.2`
- `liblzma5:amd64=5.6.2-2ubuntu0.2`
- `xz-utils=5.6.2-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

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
$ apt-get source -qq --print-uris xz-utils=5.6.2-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2-2ubuntu0.2.dsc' xz-utils_5.6.2-2ubuntu0.2.dsc 2819 SHA512:2d66f15d76d64ec524f6cc71989e55aecf0af5ff2467c8de2e7e35105b12da6eb6273064e3300478a73f9afaa557ca4d8ed215701f763f096d9e394dd1a8e0a1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz' xz-utils_5.6.2.orig.tar.xz 1307448 SHA512:af3fd021a9c8eaacfb1ae2af3f7e2a0b0554068461de5be3e2c631174cf5fe15425b739832e826c0fb158484b8cea53701be8c568d7ce1f6113b4630205f5c26
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz.asc' xz-utils_5.6.2.orig.tar.xz.asc 833 SHA512:813119ca9b057936971dbad80c1e4ac0664f8149ec4318b2fbf546140bba051e566d3b457cb69f61b584219b023bce808b4347bc209cd3e025028ff8d431ccf8
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.2-2ubuntu0.2.debian.tar.xz' xz-utils_5.6.2-2ubuntu0.2.debian.tar.xz 28076 SHA512:3ace0b1e5ac235dce41914e973f38cc348ea5fa0a44d75c41614937d3d27bf3860c12467c4d62cd8b103fc1143f9949d7f6b467017c489b0c137074fc3668ed5
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu1.dsc 2993 SHA512:b87b9b973aa22f9cea28d9653bba4383a27203ffb391ff0df537225bbca131eb47b08bc12178bf4d05348e379159be275bddf2d611c97a6bcebd80a0f1ca6e8f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu1.debian.tar.xz 59676 SHA512:c4d82f270d4334711e26d5d328683d0214d3171a2cfaff0b5b613d4df28adabf01e69ec9f6093991ef8f124f289826f30f2fc64223956462d26c9d67866482fe
```
