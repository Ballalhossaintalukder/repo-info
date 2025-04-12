# `buildpack-deps:trixie`

## Docker Metadata

- Image ID: `sha256:42a9a29f68461753943f832688217121cc3ed2477296d6b3c40ccbdfc49b1a7c`
- Created: `2024-01-31T23:01:46Z`
- Virtual Size: ~ 1.02 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `adduser=3.149`

Binary Packages:

- `adduser=3.149`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.149
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.149.dsc' adduser_3.149.dsc 1678 SHA256:9bcb11771940b5b3a3d4cfec2385f7ca7ef1362219f6bf64b7e5e356dde83cd2
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.149.tar.xz' adduser_3.149.tar.xz 330712 SHA256:061375486b8e6907eefd28e3b03efce50bbb2f93e1e084ed634c0a8688fb393f
```

Other potentially useful URLs:

- https://sources.debian.net/src/adduser/3.149/ (for browsing the source)
- https://sources.debian.net/src/adduser/3.149/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/adduser/3.149/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr-util=1.6.3-3`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3+b1`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3-3.dsc' apr-util_1.6.3-3.dsc 2789 SHA256:46f5901bea392299900c639e61e5ee1c3fabc2f78103985a9460405fa8b3a99d
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA256:a41076e3710746326c3945042994ad9a4fcac0ce0277dd8fea076fec3c9772b5
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2.asc' apr-util_1.6.3.orig.tar.bz2.asc 833 SHA256:5fd08491a2cb35fdbf9fa93d753cfd25e59fe58a75a3f3ed62582ebf2a5b3a51
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3-3.debian.tar.xz' apr-util_1.6.3-3.debian.tar.xz 341208 SHA256:25ac498e60b6c3b600ed76e25d34e0a9cb8cf3f2bae29a8b187e65d472a5ce2f
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr-util/1.6.3-3/ (for browsing the source)
- https://sources.debian.net/src/apr-util/1.6.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr-util/1.6.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr=1.7.5-1`

Binary Packages:

- `libapr1t64:amd64=1.7.5-1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.5-1
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.5-1.dsc' apr_1.7.5-1.dsc 2289 SHA256:e31e60f2e81d7ed9b0d65ba386e546769d29b31426aeae69bddbd43ee6d03786
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.5.orig.tar.bz2' apr_1.7.5.orig.tar.bz2 898264 SHA256:cd0f5d52b9ab1704c72160c5ee3ed5d3d4ca2df4a7f8ab564e3cb352b67232f2
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.5.orig.tar.bz2.asc' apr_1.7.5.orig.tar.bz2.asc 833 SHA256:28b73a98834d022d52c8faae919aa4b9aefe3ebd6d6e78bb74e68a53bdc26ec3
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.5-1.debian.tar.xz' apr_1.7.5-1.debian.tar.xz 64960 SHA256:d511152126b62b2904637dda119aa7544c4a726502bf4ee1a6a2da5eed4a3d8d
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr/1.7.5-1/ (for browsing the source)
- https://sources.debian.net/src/apr/1.7.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr/1.7.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.9.35`

Binary Packages:

- `apt=2.9.35`
- `libapt-pkg7.0:amd64=2.9.35`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.35/


### `dpkg` source package: `architecture-properties=0.2.6`

Binary Packages:

- `native-architecture=0.2.6`

Licenses: (parsed from: `/usr/share/doc/native-architecture/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris architecture-properties=0.2.6
'http://deb.debian.org/debian/pool/main/a/architecture-properties/architecture-properties_0.2.6.dsc' architecture-properties_0.2.6.dsc 1803 SHA256:a20b7a40268b8e8cd904ad9c95568c91b7a3ff12612accbb90c8286fd44f11b3
'http://deb.debian.org/debian/pool/main/a/architecture-properties/architecture-properties_0.2.6.tar.xz' architecture-properties_0.2.6.tar.xz 5368 SHA256:cec5cbfc3516fb1d51174bc2d95bb69d2d2c726b25a5c05ab73593a3a5ee20a8
```

Other potentially useful URLs:

- https://sources.debian.net/src/architecture-properties/0.2.6/ (for browsing the source)
- https://sources.debian.net/src/architecture-properties/0.2.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/architecture-properties/0.2.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `attr=1:2.5.2-3`

Binary Packages:

- `libattr1:amd64=1:2.5.2-3`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-3
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA256:c2ae3e15db059029030ddf4fdac179d8f90d423f2310a6ef8c745ba28ac18b0a
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA256:153f98c87575277ea021e24dae36293b7738699174438a2060b47e8312b771e3
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-3/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:4.0.2-2`

Binary Packages:

- `libaudit-common=1:4.0.2-2`
- `libaudit1:amd64=1:4.0.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.dsc' audit_4.0.2-2.dsc 2408 SHA256:d0b9457933409cd3287bc0b8bfb10f41c08fb5b24bd5c5b8364125d5a6894974
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA256:d5d1b5d50ee4a2d0d17875bc6ae6bd6a7d5b34d9557ea847a39faec531faaa0a
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.debian.tar.xz' audit_4.0.2-2.debian.tar.xz 19228 SHA256:33030d53299c57cda73e9e45813b8488f9bc3ad8992aef0b740afabbf66a2ba2
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.0.2-2/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.0.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.0.2-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.72-3.dsc' autoconf_2.72-3.dsc 2059 SHA256:8abbcf3e76f5bf556193b90a12963395de367e8d2e172a12e64ff3dfed7717e1
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.72.orig.tar.xz' autoconf_2.72.orig.tar.xz 1389680 SHA256:ba885c1319578d6c94d46e9b0dceb4014caafe2490e437a0dbca3f270a223f5a
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.72-3.debian.tar.xz' autoconf_2.72-3.debian.tar.xz 22980 SHA256:567456dba70e2902be944eaa6175d92c553825569ca2146768d1f122bcfd50fb
```

Other potentially useful URLs:

- https://sources.debian.net/src/autoconf/2.72-3/ (for browsing the source)
- https://sources.debian.net/src/autoconf/2.72-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autoconf/2.72-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `automake-1.17=1:1.17-4`

Binary Packages:

- `automake=1:1.17-4`

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
$ apt-get source -qq --print-uris automake-1.17=1:1.17-4
'http://deb.debian.org/debian/pool/main/a/automake-1.17/automake-1.17_1.17-4.dsc' automake-1.17_1.17-4.dsc 2527 SHA256:fd680cdc08468a40800bd446e13618fadf2caa3d5d418ee63377f40853ccc45f
'http://deb.debian.org/debian/pool/main/a/automake-1.17/automake-1.17_1.17.orig.tar.xz' automake-1.17_1.17.orig.tar.xz 1652632 SHA256:8920c1fc411e13b90bf704ef9db6f29d540e76d232cb3b2c9f4dc4cc599bd990
'http://deb.debian.org/debian/pool/main/a/automake-1.17/automake-1.17_1.17.orig.tar.xz.asc' automake-1.17_1.17.orig.tar.xz.asc 833 SHA256:14085dcd85164920da538105f388c6d2e2d0211d5e633a3e075691af6b7352cb
'http://deb.debian.org/debian/pool/main/a/automake-1.17/automake-1.17_1.17-4.debian.tar.xz' automake-1.17_1.17-4.debian.tar.xz 13064 SHA256:9bd14c38347f6a92749fc3b878d9ef243a428cb19429909641a4a87796e492ff
```

Other potentially useful URLs:

- https://sources.debian.net/src/automake-1.17/1:1.17-4/ (for browsing the source)
- https://sources.debian.net/src/automake-1.17/1:1.17-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/automake-1.17/1:1.17-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `autotools-dev=20240727.1`

Binary Packages:

- `autotools-dev=20240727.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20240727.1
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20240727.1.dsc' autotools-dev_20240727.1.dsc 1661 SHA256:be24901a0f474bb9a6eb70490f65888c0c9462008d48a0ef854cfe1dd67d691d
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20240727.1.tar.xz' autotools-dev_20240727.1.tar.xz 99716 SHA256:799808eb70d3f8c851c0974e2a4acc3539a6e6f5c8dcf27d7c1ef9de5cc18bb0
```

Other potentially useful URLs:

- https://sources.debian.net/src/autotools-dev/20240727.1/ (for browsing the source)
- https://sources.debian.net/src/autotools-dev/20240727.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autotools-dev/20240727.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.7`

Binary Packages:

- `base-files=13.7`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.7
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.7.dsc' base-files_13.7.dsc 1102 SHA256:5dcd518081e204dc564923384e950837129dce46ac12afc8c5c79948769fd683
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.7.tar.xz' base-files_13.7.tar.xz 68412 SHA256:3c13412f5f828f24ec8b7a213eed72aa6d35ba9587b9a75a87fd04ffcff3b210
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/13.7/ (for browsing the source)
- https://sources.debian.net/src/base-files/13.7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/13.7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.7`

Binary Packages:

- `base-passwd=3.6.7`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.7
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.7.dsc' base-passwd_3.6.7.dsc 1891 SHA256:23dafe71f85d7595d9e20efba17729c1c975a33bd469cf09bfad9e96b1f542f3
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.7.tar.xz' base-passwd_3.6.7.tar.xz 60872 SHA256:cf869870fed7862b57bfa9e99cd5cd6f365e2349705a1b65af7fc182629bd1ab
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.7/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.37-1.1`

Binary Packages:

- `bash=5.2.37-1.1+b2`

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
$ apt-get source -qq --print-uris bash=5.2.37-1.1
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37-1.1.dsc' bash_5.2.37-1.1.dsc 2070 SHA256:bc818c517cae2e4d316127acbddf7e643e7e6f440e5ba75a0c97bef75447b113
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA256:370704c9c859f4060b7df19055e43bb9b5fa09d887699cf6ba87885c5485d36a
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37-1.1.debian.tar.xz' bash_5.2.37-1.1.debian.tar.xz 88324 SHA256:0afc2d7394d1f6418b074099b0f23c12a9a6995deced5606d9355d01ac02186c
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.2.37-1.1/ (for browsing the source)
- https://sources.debian.net/src/bash/5.2.37-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.2.37-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `binutils=2.44-3`

Binary Packages:

- `binutils=2.44-3`
- `binutils-common:amd64=2.44-3`
- `binutils-x86-64-linux-gnu=2.44-3`
- `libbinutils:amd64=2.44-3`
- `libctf-nobfd0:amd64=2.44-3`
- `libctf0:amd64=2.44-3`
- `libgprofng0:amd64=2.44-3`
- `libsframe1:amd64=2.44-3`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.44-3
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.44-3.dsc' binutils_2.44-3.dsc 11429 SHA256:5abd1ae1adb61fd8ecbadfdc16668738668e81c745884aefa0ce97791b2a74b8
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.44.orig.tar.xz' binutils_2.44.orig.tar.xz 27504768 SHA256:c41a0272424f41bb01bf828e7ffef1b2d59d1788064fd6b5f1d971717e9320b8
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.44-3.debian.tar.xz' binutils_2.44-3.debian.tar.xz 131700 SHA256:555c856d6fb5a797c2692c24c3083e7b1a76811a470eaab01d90c969c2f92784
```

Other potentially useful URLs:

- https://sources.debian.net/src/binutils/2.44-3/ (for browsing the source)
- https://sources.debian.net/src/binutils/2.44-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/binutils/2.44-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2+b7`
- `libbrotli1:amd64=1.1.0-2+b7`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

Other potentially useful URLs:

- https://sources.debian.net/src/brotli/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/brotli/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/brotli/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA256:cd3bfd77254a6b5ef1be144bdc90a0dd374bc8206afd98ba4abf828741b79820
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA256:648ed0dac9a041ba6951e0cca521628aa39947cefee78139f7b934a5dc502095
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.8-6/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.8-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.8-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ca-certificates=20241223`

Binary Packages:

- `ca-certificates=20241223`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20241223
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20241223.dsc' ca-certificates_20241223.dsc 1766 SHA256:8b17779dedec18ad64b97ec99dd3b8f10ec06698e73242dbe7b8d992bd803a55
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20241223.tar.xz' ca-certificates_20241223.tar.xz 278044 SHA256:dd8286d0a9dd35c756fea5f1df3fed1510fb891f376903891b003cd9b1ad7e03
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20241223/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20241223/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20241223/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cairo=1.18.4-1`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.4-1+b1`
- `libcairo-script-interpreter2:amd64=1.18.4-1+b1`
- `libcairo2:amd64=1.18.4-1+b1`
- `libcairo2-dev:amd64=1.18.4-1+b1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-1
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.4-1.dsc' cairo_1.18.4-1.dsc 2763 SHA256:717ca0717208ae5ef1ab354e47328867ee7038fe65fb75e0ce366139b34bf67f
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA256:445ed8208a6e4823de1226a74ca319d3600e83f6369f99b14265006599c32ccb
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.4-1.debian.tar.xz' cairo_1.18.4-1.debian.tar.xz 29920 SHA256:bf2d9ea10097fd06faf6b4ef2149677e7aa0eb8abf85aa5d46851ea11a713f68
```

Other potentially useful URLs:

- https://sources.debian.net/src/cairo/1.18.4-1/ (for browsing the source)
- https://sources.debian.net/src/cairo/1.18.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cairo/1.18.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.277`

Binary Packages:

- `libdebconfclient0:amd64=0.277`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.277
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.277.dsc' cdebconf_0.277.dsc 2707 SHA256:12afc241658ae9bcbb11d239d06e708fb6138b417b7ce9c31ac642f57fcc4613
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.277.tar.xz' cdebconf_0.277.tar.xz 285420 SHA256:93a72ed5c5cab66f1f7439908348aa3bd97c4fa4a47416694e5dc3add2866e7b
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.277/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.277/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.277/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `coreutils=9.5-1`

Binary Packages:

- `coreutils=9.5-1+b1`

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
$ apt-get source -qq --print-uris coreutils=9.5-1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5-1.dsc' coreutils_9.5-1.dsc 2104 SHA256:83558c321a5e7a39dcf538a5a425f03486fbd2e6d95941a17ed98d04ed5ea7af
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz' coreutils_9.5.orig.tar.xz 6007136 SHA256:cd328edeac92f6a665de9f323c93b712af1858bc2e0d88f3f7100469470a1b8a
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz.asc' coreutils_9.5.orig.tar.xz.asc 833 SHA256:b2843cd7c5972c7bc4d01fc34eb82e5a3ec84a199363288e3999304e3dddc805
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5-1.debian.tar.xz' coreutils_9.5-1.debian.tar.xz 21768 SHA256:fe704f7ba9b23cbc857e755bd3ec987228166b1342c1651f04bd16649b71d84d
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.5-1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `curl=8.13.0-1`

Binary Packages:

- `curl=8.13.0-1`
- `libcurl3t64-gnutls:amd64=8.13.0-1`
- `libcurl4-openssl-dev:amd64=8.13.0-1`
- `libcurl4t64:amd64=8.13.0-1`

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
$ apt-get source -qq --print-uris curl=8.13.0-1
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.13.0-1.dsc' curl_8.13.0-1.dsc 3231 SHA256:26a74899a9d222e693c24ff9d44fe9d9a48a4a74af25c158be5ef7e450e0fa33
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.13.0.orig.tar.gz' curl_8.13.0.orig.tar.gz 4188717 SHA256:c261a4db579b289a7501565497658bbd52d3138fdbaccf1490fa918129ab45bc
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.13.0.orig.tar.gz.asc' curl_8.13.0.orig.tar.gz.asc 488 SHA256:a13900f07f7c54cb5fa3bb288b12e13532475ed6ef482fbe9a59f6d440759aa5
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.13.0-1.debian.tar.xz' curl_8.13.0-1.debian.tar.xz 53496 SHA256:bf0acedff580831a7c3c7f604d48f80116e08b08c7f4e15043c80e56f94365e9
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/8.13.0-1/ (for browsing the source)
- https://sources.debian.net/src/curl/8.13.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/8.13.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.dsc' cyrus-sasl2_2.1.28+dfsg1-9.dsc 3306 SHA256:179cda376ee9f9a54098f902174299dd183ae78c703f72b86bd4c3297db4c153
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9.debian.tar.xz 99180 SHA256:8215afa01ee2907da0a650bfa6b9cf0fae12f2611a098eedd853b5e71adf6623
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-9/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.28+dfsg1-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.12-12`

Binary Packages:

- `dash=0.5.12-12`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.dsc' dash_0.5.12-12.dsc 1460 SHA256:589efc4d87a4ae4745c273bdb33198d7c4f28a71736a8ece81d3677cf9c6e5ce
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.debian.tar.xz' dash_0.5.12-12.debian.tar.xz 47300 SHA256:a278acb5d9a1f5d9a086d36a547287cbf3105b8f33c0e62d86d264decf5ba1ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-12/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dav1d=1.5.1-1`

Binary Packages:

- `libdav1d-dev:amd64=1.5.1-1`
- `libdav1d7:amd64=1.5.1-1`

Licenses: (parsed from: `/usr/share/doc/libdav1d-dev/copyright`, `/usr/share/doc/libdav1d7/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dav1d=1.5.1-1
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.5.1-1.dsc' dav1d_1.5.1-1.dsc 2290 SHA256:a418ee8fdc8003feee1ba19391eac250e3ef03106c995c8e25b8a42b56de18cf
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.5.1.orig.tar.xz' dav1d_1.5.1.orig.tar.xz 1020760 SHA256:401813f1f89fa8fd4295805aa5284d9aed9bc7fc1fdbe554af4292f64cbabe21
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.5.1.orig.tar.xz.asc' dav1d_1.5.1.orig.tar.xz.asc 195 SHA256:4cad1d03a19a717562c2c80c1df195b629e43898cd1af19296958847f6212554
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.5.1-1.debian.tar.xz' dav1d_1.5.1-1.debian.tar.xz 8468 SHA256:41f758fda3a2d9860691cae422365bae656060f42c9a5375f7ac4124005f4e7e
```

Other potentially useful URLs:

- https://sources.debian.net/src/dav1d/1.5.1-1/ (for browsing the source)
- https://sources.debian.net/src/dav1d/1.5.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dav1d/1.5.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db-defaults=5.3.4`

Binary Packages:

- `libdb-dev:amd64=5.3.4`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=5.3.4
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.4.dsc' db-defaults_5.3.4.dsc 1585 SHA256:0709e552cc31edcad465fc057bb04fcfd9f0467637125374bed81432fb922bef
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.4.tar.xz' db-defaults_5.3.4.tar.xz 2600 SHA256:1774d9974b0afba1d8fc02186ed05e38287a97f94623b440b5e7606831e9c442
```

Other potentially useful URLs:

- https://sources.debian.net/src/db-defaults/5.3.4/ (for browsing the source)
- https://sources.debian.net/src/db-defaults/5.3.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db-defaults/5.3.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db5.3=5.3.28+dfsg2-9`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-9`
- `libdb5.3t64:amd64=5.3.28+dfsg2-9`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA256:045f392c75dffc9d4f3bd44978b90ca8d45b935cf0ae4202bf79a760f2ce07b1
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA256:21fe6ee0491c83d0c34fe52e0e0e423946172eff68262584a0cc8ef880c36b74
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-9/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA256:1aa3ceaef24ef533cfffe7f9ca750c6325dbaea86a7abca77cb4439ceae930d8
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA256:18f3f43924ccc870be483d7c5f1a9be59e51ae1da403059d654666b5a175bf15
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.91/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.91/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.91/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2023.4`

Binary Packages:

- `debian-archive-keyring=2023.4`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2023.4
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.dsc' debian-archive-keyring_2023.4.dsc 1261 SHA256:c97d048486078fcc6866a477df83b19270ae872102f4ed64b5a5e9995ff79afa
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.tar.xz' debian-archive-keyring_2023.4.tar.xz 177568 SHA256:7f9b64d7c5e748b0cb99fd0674d872111c219e119f296912c59fc61ab49bb78a
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2023.4/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2023.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2023.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debianutils=5.21`

Binary Packages:

- `debianutils=5.21`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.21
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.21.dsc' debianutils_5.21.dsc 1631 SHA256:9e26a955c62d09a9401aeb53cb190eca078b2cc13ea33ec874e944e95c21935e
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.21.tar.xz' debianutils_5.21.tar.xz 81916 SHA256:0053dcfd89e5c7dbfb2632450c00af6b8a646eeaaf185bbc8f2915488f994fe5
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.21/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.21/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.21/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `diffutils=1:3.10-3`

Binary Packages:

- `diffutils=1:3.10-3`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-3
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-3.dsc' diffutils_3.10-3.dsc 1851 SHA256:f8d39747fc6bfe89d761e168f521f75239b72a9361776b02fd4a870f0c077377
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-3.debian.tar.xz' diffutils_3.10-3.debian.tar.xz 14284 SHA256:95fc3956547b30ef2a7bf35b682faa1b6500695d2b05babcfc37a6fcefefb185
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.10-3/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.10-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.10-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `djvulibre=3.5.28-2`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2+b2`
- `libdjvulibre-text=3.5.28-2`
- `libdjvulibre21:amd64=3.5.28-2+b2`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28-2.dsc' djvulibre_3.5.28-2.dsc 2388 SHA256:0b5f31e70a8f81afec47e67e9465dbece7756f0c7f88da643f0dda82bf78a1ba
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA256:1223b7bf7c8dfe2e290882f3bfb88ba2468b30495a1bf8dfd54dc7e810987887
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28-2.debian.tar.xz' djvulibre_3.5.28-2.debian.tar.xz 17420 SHA256:6f85dcd7cdb856cc3e4a31fc381e73a6cab717c90e058f474fb4d2ab29635d91
```

Other potentially useful URLs:

- https://sources.debian.net/src/djvulibre/3.5.28-2/ (for browsing the source)
- https://sources.debian.net/src/djvulibre/3.5.28-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/djvulibre/3.5.28-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.22.18`

Binary Packages:

- `dpkg=1.22.18`
- `dpkg-dev=1.22.18`
- `libdpkg-perl=1.22.18`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.18
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.18.dsc' dpkg_1.22.18.dsc 3406 SHA256:570965593ff88a6be0ccc4bef8eff566922c6758f86989d376cb03702374d1d4
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.18.tar.xz' dpkg_1.22.18.tar.xz 5753376 SHA256:7135eb7960e38b2c77810d5aab8cabf5f690fed7475b7b0f2654fd91efbba0f6
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.22.18/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.22.18/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.22.18/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.47.2-1`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.2-1+b1`
- `libcom-err2:amd64=1.47.2-1+b1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/libcom-err2/copyright`)

- `0BSD`
- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.dsc' e2fsprogs_1.47.2-1.dsc 3032 SHA256:e6392801ad349ed0217c45684b61db03b33fae940ceb4de23b71a24dab4e1bfc
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA256:6dcd67ff9d8b13274ba3f088e4318be4f5b71412cd863524423fc49d39a6371f
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA256:2063f62a198dd3df21f789c990c2cf9b4a5de24ed55f0b78d86e97e98daffc9d
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.debian.tar.xz' e2fsprogs_1.47.2-1.debian.tar.xz 92348 SHA256:b9d1c79da5b32975f5771a5c487edbd9301729e6e813018209f31e2897a46617
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.2-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `elfutils=0.192-4`

Binary Packages:

- `libelf1t64:amd64=0.192-4`

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
$ apt-get source -qq --print-uris elfutils=0.192-4
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.192-4.dsc' elfutils_0.192-4.dsc 3314 SHA256:37d101658c45a25afc15d2053a1378df2381dadbb368e262ede2cea79241779f
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.192.orig.tar.bz2' elfutils_0.192.orig.tar.bz2 11913897 SHA256:616099beae24aba11f9b63d86ca6cc8d566d968b802391334c91df54eab416b4
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.192-4.debian.tar.xz' elfutils_0.192-4.debian.tar.xz 44456 SHA256:a18efee3ae99ea25e10a0b8c4b731a28dee685361ae89ea8136e9065c86c8942
```

Other potentially useful URLs:

- https://sources.debian.net/src/elfutils/0.192-4/ (for browsing the source)
- https://sources.debian.net/src/elfutils/0.192-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/elfutils/0.192-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `expat=2.7.1-1`

Binary Packages:

- `libexpat1:amd64=2.7.1-1`
- `libexpat1-dev:amd64=2.7.1-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.1-1
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.7.1-1.dsc' expat_2.7.1-1.dsc 1964 SHA256:4ffb7f7a8adf961deaaec47654866eb965bafeda54bbf006fbad56d33c2d1290
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.7.1.orig.tar.gz' expat_2.7.1.orig.tar.gz 8433717 SHA256:85372797ff0673a8fc4a6be16466bb5a0ca28c0dcf3c6f7ac1686b4a3ba2aabb
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.7.1-1.debian.tar.xz' expat_2.7.1-1.debian.tar.xz 13204 SHA256:1c604a215810ed6598dcf49d87462a3b79c9d780aaf997ee1814b7afc1f25022
```

Other potentially useful URLs:

- https://sources.debian.net/src/expat/2.7.1-1/ (for browsing the source)
- https://sources.debian.net/src/expat/2.7.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/expat/2.7.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fftw3=3.3.10-2`

Binary Packages:

- `libfftw3-bin=3.3.10-2+b1`
- `libfftw3-dev:amd64=3.3.10-2+b1`
- `libfftw3-double3:amd64=3.3.10-2+b1`
- `libfftw3-long3:amd64=3.3.10-2+b1`
- `libfftw3-quad3:amd64=3.3.10-2+b1`
- `libfftw3-single3:amd64=3.3.10-2+b1`

Licenses: (parsed from: `/usr/share/doc/libfftw3-bin/copyright`, `/usr/share/doc/libfftw3-dev/copyright`, `/usr/share/doc/libfftw3-double3/copyright`, `/usr/share/doc/libfftw3-long3/copyright`, `/usr/share/doc/libfftw3-quad3/copyright`, `/usr/share/doc/libfftw3-single3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-2
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10-2.dsc' fftw3_3.3.10-2.dsc 2754 SHA256:58bdea9754119c591f95e373c1c85ff2b6861383b20bf3bb1e81af9c76a51d71
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4144100 SHA256:56c932549852cddcfafdab3820b0200c7742675be92179e59e6215b340e26467
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10-2.debian.tar.xz' fftw3_3.3.10-2.debian.tar.xz 14628 SHA256:369066d9b28af25ac779ad23cce78be8dad3896bcbeb80de30d3d36b7a94fd67
```

Other potentially useful URLs:

- https://sources.debian.net/src/fftw3/3.3.10-2/ (for browsing the source)
- https://sources.debian.net/src/fftw3/3.3.10-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fftw3/3.3.10-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `file=1:5.45-3`

Binary Packages:

- `file=1:5.45-3+b1`
- `libmagic-mgc=1:5.45-3+b1`
- `libmagic1t64:amd64=1:5.45-3+b1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-3
'http://deb.debian.org/debian/pool/main/f/file/file_5.45-3.dsc' file_5.45-3.dsc 2268 SHA256:5f406d2169753ca86828bfa41e5a9db3059f984004e6d07ba02edfd7de0f37ab
'http://deb.debian.org/debian/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA256:fc97f51029bb0e2c9f4e3bffefdaf678f0e039ee872b9de5c002a6d09c784d82
'http://deb.debian.org/debian/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA256:81aacbee95911bd9825e81748d42f41dadf846ba13165462dc428467ed9ee075
'http://deb.debian.org/debian/pool/main/f/file/file_5.45-3.debian.tar.xz' file_5.45-3.debian.tar.xz 35856 SHA256:6637b243f7811317d4e07219b14f4f40777c7ab3783a8d7834f53695e01e263e
```

Other potentially useful URLs:

- https://sources.debian.net/src/file/1:5.45-3/ (for browsing the source)
- https://sources.debian.net/src/file/1:5.45-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/file/1:5.45-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA256:fa6b67056d9e5b4d8edbfc8ab95ac15ac769b140284426973f6a1ef07a4594ec
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA256:7d19668508523a6fcfb7731f5646305a8b1a00a3105ee3f0a5f167adf93a8a46
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.10.0-3/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.10.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.10.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fontconfig=2.15.0-2.2`

Binary Packages:

- `fontconfig=2.15.0-2.2`
- `fontconfig-config=2.15.0-2.2`
- `libfontconfig-dev:amd64=2.15.0-2.2`
- `libfontconfig1:amd64=2.15.0-2.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-2.2
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.2.dsc' fontconfig_2.15.0-2.2.dsc 2699 SHA256:b6d4a31cf21bb8be4e5b76749abf1c3ea2df0f42d3a5714837f9a006cb124bed
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA256:63a0658d0e06e0fa886106452b58ef04f21f58202ea02a94c39de0d3335d7c0e
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.2.debian.tar.xz' fontconfig_2.15.0-2.2.debian.tar.xz 59124 SHA256:08f4f6339d992162e99fa64e312cf5516b6b85c9aa81b97da3967a7bfa9721b8
```

Other potentially useful URLs:

- https://sources.debian.net/src/fontconfig/2.15.0-2.2/ (for browsing the source)
- https://sources.debian.net/src/fontconfig/2.15.0-2.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fontconfig/2.15.0-2.2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA256:219f7f8fba98827caaa296520730171ec230d3090ed8b6d663edb66839b48847
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA256:4b21c5203f792343d5e90ab1cb0cf07e99887218abe3d83cd9a98cea9085e799
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA256:2401402245dec8a59fc5f0f8eff76d203a38440797f7f223e1d044e07c2d41fb
```

Other potentially useful URLs:

- https://sources.debian.net/src/fonts-dejavu/2.37-8/ (for browsing the source)
- https://sources.debian.net/src/fonts-dejavu/2.37-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fonts-dejavu/2.37-8/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.dsc' freetype_2.13.3+dfsg-1.dsc 3680 SHA256:122104ec96184391361f4ee9e5c70e83b05a5c0b90030f2b94befb0fad0664c3
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz 342404 SHA256:8775e5ffded1a885ba2ccb3ea0e82c73306a03b764080c3e4c79da15b5c9a28a
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:931bfa17e59c0ec7db391160f43977e0907f36ea3c39d7e6063731cd4612dd51
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz 2173852 SHA256:b7b66149bea769e226fd3d6d1eee6160e5b6beb4249b088071434fbe85fd1070
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:65c66aec6244d247540430b21d3e80b677f1361906347a5be7fad371d46655da
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig.tar.xz' freetype_2.13.3+dfsg.orig.tar.xz 2201416 SHA256:686ec73cbf6783b245dd068a09ce807b729ac0f8a46dd70f7867923c32fdf4de
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.debian.tar.xz' freetype_2.13.3+dfsg-1.debian.tar.xz 43904 SHA256:e2de836c8bb52c5a59173465bfddbf476a277f3f065ba322d111c5046ef8b8c8
```

Other potentially useful URLs:

- https://sources.debian.net/src/freetype/2.13.3+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/freetype/2.13.3+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/freetype/2.13.3+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fribidi=1.0.16-1`

Binary Packages:

- `libfribidi-dev:amd64=1.0.16-1`
- `libfribidi0:amd64=1.0.16-1`

Licenses: (parsed from: `/usr/share/doc/libfribidi-dev/copyright`, `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-1
'http://deb.debian.org/debian/pool/main/f/fribidi/fribidi_1.0.16-1.dsc' fribidi_1.0.16-1.dsc 2004 SHA256:10f003abcad934adde409c94f2780ec9638517dc1cc495b2a1df03a13c1d4315
'http://deb.debian.org/debian/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA256:1b1cde5b235d40479e91be2f0e88a309e3214c8ab470ec8a2744d82a5a9ea05c
'http://deb.debian.org/debian/pool/main/f/fribidi/fribidi_1.0.16-1.debian.tar.xz' fribidi_1.0.16-1.debian.tar.xz 8928 SHA256:8d1cd7177a436b25ca8153e3dd2b9fb6da411a2c3cb0105eaadf4e42b777da6f
```

Other potentially useful URLs:

- https://sources.debian.net/src/fribidi/1.0.16-1/ (for browsing the source)
- https://sources.debian.net/src/fribidi/1.0.16-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fribidi/1.0.16-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-14=14.2.0-19`

Binary Packages:

- `cpp-14=14.2.0-19`
- `cpp-14-x86-64-linux-gnu=14.2.0-19`
- `g++-14=14.2.0-19`
- `g++-14-x86-64-linux-gnu=14.2.0-19`
- `gcc-14=14.2.0-19`
- `gcc-14-base:amd64=14.2.0-19`
- `gcc-14-x86-64-linux-gnu=14.2.0-19`
- `libasan8:amd64=14.2.0-19`
- `libatomic1:amd64=14.2.0-19`
- `libcc1-0:amd64=14.2.0-19`
- `libgcc-14-dev:amd64=14.2.0-19`
- `libgcc-s1:amd64=14.2.0-19`
- `libgomp1:amd64=14.2.0-19`
- `libhwasan0:amd64=14.2.0-19`
- `libitm1:amd64=14.2.0-19`
- `liblsan0:amd64=14.2.0-19`
- `libquadmath0:amd64=14.2.0-19`
- `libstdc++-14-dev:amd64=14.2.0-19`
- `libstdc++6:amd64=14.2.0-19`
- `libtsan2:amd64=14.2.0-19`
- `libubsan1:amd64=14.2.0-19`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-19
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-19.dsc' gcc-14_14.2.0-19.dsc 47347 SHA256:7db1e202cce66617e9134a662c877a3a773de5b612fd52179815877e0ecfb847
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-19.debian.tar.xz' gcc-14_14.2.0-19.debian.tar.xz 2577016 SHA256:31cbab4bafa48aa1c540497bd8098cbcf98e673778f927651ed944709f687781
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14.2.0-19/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14.2.0-19/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14.2.0-19/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-defaults=1.220`

Binary Packages:

- `cpp=4:14.2.0-1`
- `cpp-x86-64-linux-gnu=4:14.2.0-1`
- `g++=4:14.2.0-1`
- `g++-x86-64-linux-gnu=4:14.2.0-1`
- `gcc=4:14.2.0-1`
- `gcc-x86-64-linux-gnu=4:14.2.0-1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.220
'http://deb.debian.org/debian/pool/main/g/gcc-defaults/gcc-defaults_1.220.dsc' gcc-defaults_1.220.dsc 36895 SHA256:abfa2d362033435385e733f97d0cace1fbc917fd4160c81cc89abac38d3cdc37
'http://deb.debian.org/debian/pool/main/g/gcc-defaults/gcc-defaults_1.220.tar.xz' gcc-defaults_1.220.tar.xz 54044 SHA256:d40fbdb57f351a58e050c3e1037201853e88e3f673242b62357dc20030ad4805
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-defaults/1.220/ (for browsing the source)
- https://sources.debian.net/src/gcc-defaults/1.220/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-defaults/1.220/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.24-2.dsc' gdbm_1.24-2.dsc 2466 SHA256:28acecf1cf00240942833c04079a02bb4c199a48faa1f4ca90f0ea9b79dc5841
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz' gdbm_1.24.orig.tar.gz 1195931 SHA256:695e9827fdf763513f133910bc7e6cfdb9187943a4fec943e57449723d2b8dbf
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz.asc' gdbm_1.24.orig.tar.gz.asc 195 SHA256:8fb2f87e817ed6bd1d7ef2ab976f6a0046814a5ff28a06c521b796e0d3fd1226
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.24-2.debian.tar.xz' gdbm_1.24-2.debian.tar.xz 16880 SHA256:736d23450674c1bf0b03a2f65b83870b0801bc3747df3099df970c1479b0ab63
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdbm/1.24-2/ (for browsing the source)
- https://sources.debian.net/src/gdbm/1.24-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdbm/1.24-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-2`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-2`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-2`

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
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.12+dfsg-2
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-2.dsc' gdk-pixbuf_2.42.12+dfsg-2.dsc 3091 SHA256:7d93dab8a4d7c0c0ea69c68e0bdda113fadf7458994e93fcd34226d626bf0706
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.12+dfsg.orig.tar.xz 6443656 SHA256:2fab7a828f1a017a235cd800cf0b47d83733037bade493337c46ed79e7ef3678
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-2.debian.tar.xz' gdk-pixbuf_2.42.12+dfsg-2.debian.tar.xz 21832 SHA256:f95cc3b01eac0b6c8bb045187d265445d54b342259ad6755330697f8de272ba2
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdk-pixbuf/2.42.12+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/gdk-pixbuf/2.42.12+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdk-pixbuf/2.42.12+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `git=1:2.47.2-0.1`

Binary Packages:

- `git=1:2.47.2-0.1`
- `git-man=1:2.47.2-0.1`

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
$ apt-get source -qq --print-uris git=1:2.47.2-0.1
'http://deb.debian.org/debian/pool/main/g/git/git_2.47.2-0.1.dsc' git_2.47.2-0.1.dsc 2832 SHA256:0ff8e1ffeb1471f012ee2b93bcf21ceb2776abd88b1e9a171771f94d13eecde6
'http://deb.debian.org/debian/pool/main/g/git/git_2.47.2.orig.tar.xz' git_2.47.2.orig.tar.xz 7655652 SHA256:b19268be6b6f1556b47a9dd834272e167d3a75740cdcd283cf3812edffe3930f
'http://deb.debian.org/debian/pool/main/g/git/git_2.47.2-0.1.debian.tar.xz' git_2.47.2-0.1.debian.tar.xz 792848 SHA256:a183a1a1edd7190b6c6836f62a98662d1d2228a8b16ddd8163c29101b4342482
```

Other potentially useful URLs:

- https://sources.debian.net/src/git/1:2.47.2-0.1/ (for browsing the source)
- https://sources.debian.net/src/git/1:2.47.2-0.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/git/1:2.47.2-0.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glib2.0=2.84.0-2`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.84.0-2`
- `gir1.2-glib-2.0-dev:amd64=2.84.0-2`
- `girepository-tools:amd64=2.84.0-2`
- `libgio-2.0-dev:amd64=2.84.0-2`
- `libgio-2.0-dev-bin=2.84.0-2`
- `libgirepository-2.0-0:amd64=2.84.0-2`
- `libglib2.0-0t64:amd64=2.84.0-2`
- `libglib2.0-bin=2.84.0-2`
- `libglib2.0-data=2.84.0-2`
- `libglib2.0-dev:amd64=2.84.0-2`
- `libglib2.0-dev-bin=2.84.0-2`

Licenses: (parsed from: `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/gir1.2-glib-2.0-dev/copyright`, `/usr/share/doc/girepository-tools/copyright`, `/usr/share/doc/libgio-2.0-dev/copyright`, `/usr/share/doc/libgio-2.0-dev-bin/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/glib2.0/2.84.0-2/


### `dpkg` source package: `glibc=2.41-6`

Binary Packages:

- `libc-bin=2.41-6`
- `libc-dev-bin=2.41-6`
- `libc6:amd64=2.41-6`
- `libc6-dev:amd64=2.41-6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
- `GPL-3+`
- `IBM`
- `ISC`
- `Inner-Net`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+-with-link-exception`
- `LGPL-3`
- `LGPL-3+`
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.41-6
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.41-6.dsc' glibc_2.41-6.dsc 7540 SHA256:1b744ccc0a51e15665b72d6f0281a8f242ca8d2f1a6035e1ad675ada336a8401
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.41.orig.tar.xz' glibc_2.41.orig.tar.xz 20323540 SHA256:f24aa441021121a79266f0d75242706cab8843a47901fefe74527491807f1998
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.41-6.debian.tar.xz' glibc_2.41-6.debian.tar.xz 407868 SHA256:68a9b65aed26de7fa1fed84374d1f338b885cc6df0e14ca609bbff737faf99e8
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.41-6/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.41-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.41-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.3.0+dfsg-3`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-3`
- `libgmp10:amd64=2:6.3.0+dfsg-3`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-3`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.dsc' gmp_6.3.0+dfsg-3.dsc 2251 SHA256:f7b64af28f52b7346bb8581e01d3c19daf769639345f234f8ae1e29c42171443
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.debian.tar.xz' gmp_6.3.0+dfsg-3.debian.tar.xz 19912 SHA256:1d890bbe25dd649d2ddba1926483176520e50f22115a00566f250b613b8c20ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.2.46-6`

Binary Packages:

- `dirmngr=2.2.46-6`
- `gnupg=2.2.46-6`
- `gnupg-l10n=2.2.46-6`
- `gpg=2.2.46-6`
- `gpg-agent=2.2.46-6`
- `gpgconf=2.2.46-6`
- `gpgsm=2.2.46-6`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
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
$ apt-get source -qq --print-uris gnupg2=2.2.46-6
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.46-6.dsc' gnupg2_2.2.46-6.dsc 3874 SHA256:3165b07d7fb87095a8efcc64c25e49d91a062f711a4b08d6153ed9798b34b2f0
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.46.orig.tar.bz2' gnupg2_2.2.46.orig.tar.bz2 7073667 SHA256:7249e12405e38f12996602faa4b791f136463637f58e834246037ebf8846796e
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.46.orig.tar.bz2.asc' gnupg2_2.2.46.orig.tar.bz2.asc 325 SHA256:0cd4d189897eed7c8f583e8347d9a58f7281be7e617159d87663b7f97e495ed4
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.46-6.debian.tar.xz' gnupg2_2.2.46-6.debian.tar.xz 159696 SHA256:46d7cc0e8537744df0b32837c9feea9aeccbda0da9920cb92220e0df1e7f84b6
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnupg2/2.2.46-6/ (for browsing the source)
- https://sources.debian.net/src/gnupg2/2.2.46-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnupg2/2.2.46-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnutls28=3.8.9-2`

Binary Packages:

- `libgnutls-dane0t64:amd64=3.8.9-2`
- `libgnutls-openssl27t64:amd64=3.8.9-2`
- `libgnutls28-dev:amd64=3.8.9-2`
- `libgnutls30t64:amd64=3.8.9-2`

Licenses: (parsed from: `/usr/share/doc/libgnutls-dane0t64/copyright`, `/usr/share/doc/libgnutls-openssl27t64/copyright`, `/usr/share/doc/libgnutls28-dev/copyright`, `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `FSFAP`
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
$ apt-get source -qq --print-uris gnutls28=3.8.9-2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.9-2.dsc' gnutls28_3.8.9-2.dsc 3236 SHA256:ee7571c280c896765fd3e5baa2f5b422a57b6227616120e95b7a79565d575cf0
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz' gnutls28_3.8.9.orig.tar.xz 6847364 SHA256:69e113d802d1670c4d5ac1b99040b1f2d5c7c05daec5003813c049b5184820ed
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz.asc' gnutls28_3.8.9.orig.tar.xz.asc 833 SHA256:7631d47762865d4ef494492cca794cf0fe6a8be892a4aa02f362ae29006d3054
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.9-2.debian.tar.xz' gnutls28_3.8.9-2.debian.tar.xz 78404 SHA256:69786eec12ca5559bdf3ccc47c18e93190149e83d92a3d2b79c9068ad101642e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.9-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gobject-introspection=1.84.0-1`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.84.0-1`
- `gir1.2-freedesktop-dev:amd64=1.84.0-1`

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
$ apt-get source -qq --print-uris gobject-introspection=1.84.0-1
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.84.0-1.dsc' gobject-introspection_1.84.0-1.dsc 4202 SHA256:cf33962fbdb12b9562889b181ea1054b33dbcb11514c1873feab9e8bfabdd686
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.84.0.orig-glib.tar.xz' gobject-introspection_1.84.0.orig-glib.tar.xz 5475296 SHA256:b3764dd6e29b664085921dd4dd6ba2430fc19760ab6857ecfa3ebd4e8c1d114c
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.84.0.orig.tar.xz' gobject-introspection_1.84.0.orig.tar.xz 1080316 SHA256:945b57da7ec262e5c266b89e091d14be800cc424277d82a02872b7d794a84779
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.84.0-1.debian.tar.xz' gobject-introspection_1.84.0-1.debian.tar.xz 58824 SHA256:f06e9414cf0a6781ef133a5ba6234769b7bc0126f9fffefba08da590f7711351
```

Other potentially useful URLs:

- https://sources.debian.net/src/gobject-introspection/1.84.0-1/ (for browsing the source)
- https://sources.debian.net/src/gobject-introspection/1.84.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gobject-introspection/1.84.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `graphite2=1.3.14-2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2+b1`
- `libgraphite2-dev:amd64=1.3.14-2+b1`

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
$ apt-get source -qq --print-uris graphite2=1.3.14-2
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14-2.dsc' graphite2_1.3.14-2.dsc 2568 SHA256:98ee6be2e35e2a4f7dbc71a21315399d59c4f79339cb832c6caccf8f62342d26
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA256:7a3b342c5681921ce2e0c2496509d30b5b078399d5a7bd2358f95166d57d91df
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14-2.debian.tar.xz' graphite2_1.3.14-2.debian.tar.xz 14168 SHA256:dc46cc532a54adfc7ed5798061795120325bf0722221b2a6299f49c403ee9cd4
```

Other potentially useful URLs:

- https://sources.debian.net/src/graphite2/1.3.14-2/ (for browsing the source)
- https://sources.debian.net/src/graphite2/1.3.14-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/graphite2/1.3.14-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA256:dd6f8eb933bc05446e483f7792c8bf0a1aba9d498e65c6ccafe64e9bf27ac054
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA256:1db2aedde89d0dea42b16d9528f894c8d15dae4e190b59aecc78f5a951276eab
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA256:89ec23ffd59b68822732dc8204fc89883c3af30a90ae390feb94346d9d09a589
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA256:f10394b7589c58ca7de4b580692b1b59431f898cb2068e86222c174e093fdf49
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.11-4/ (for browsing the source)
- https://sources.debian.net/src/grep/3.11-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.11-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gzip=1.13-1`

Binary Packages:

- `gzip=1.13-1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.dsc' gzip_1.13-1.dsc 1884 SHA256:4942638dbb63dc5690e0a95ed70ee9f11e93565c43941c2485da3e561ec72028
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA256:7454eb6935db17c6655576c2e1b0fabefd38b4d0936e0f87f48cd062ce91a057
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz.asc' gzip_1.13.orig.tar.xz.asc 833 SHA256:aa752d6460fff2e0064857f1c6057d2dc49a28a45ad28c6b29c525851d6771f1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.debian.tar.xz' gzip_1.13-1.debian.tar.xz 19028 SHA256:29319b3f91d8e03d940d4d7c0f2a5fe5ec4f2ba4a0e621c9ef2682f2d0240dd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.13-1/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.13-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.13-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `harfbuzz=10.2.0-1`

Binary Packages:

- `gir1.2-harfbuzz-0.0:amd64=10.2.0-1+b1`
- `libharfbuzz-cairo0:amd64=10.2.0-1+b1`
- `libharfbuzz-dev:amd64=10.2.0-1+b1`
- `libharfbuzz-gobject0:amd64=10.2.0-1+b1`
- `libharfbuzz-icu0:amd64=10.2.0-1+b1`
- `libharfbuzz-subset0:amd64=10.2.0-1+b1`
- `libharfbuzz0b:amd64=10.2.0-1+b1`

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
$ apt-get source -qq --print-uris harfbuzz=10.2.0-1
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.dsc' harfbuzz_10.2.0-1.dsc 2564 SHA256:be25f4a4d1ca2032fbb51530649579fa843fa39c3f1941d1c644955e741f282d
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0.orig.tar.xz' harfbuzz_10.2.0.orig.tar.xz 17957608 SHA256:620e3468faec2ea8685d32c46a58469b850ef63040b3565cde05959825b48227
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.debian.tar.xz' harfbuzz_10.2.0-1.debian.tar.xz 20108 SHA256:9bbdda73722f662b8a52c39a7d4d9ef6e024c0d4dd2cb41d825b066b6d170633
```

Other potentially useful URLs:

- https://sources.debian.net/src/harfbuzz/10.2.0-1/ (for browsing the source)
- https://sources.debian.net/src/harfbuzz/10.2.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/harfbuzz/10.2.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hicolor-icon-theme=0.18-2`

Binary Packages:

- `hicolor-icon-theme=0.18-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-2
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.dsc' hicolor-icon-theme_0.18-2.dsc 2325 SHA256:8d8c91162fa2557d55ffd34f3df7f8c4946c9db641c206c64c1488df407445a6
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA256:db0e50a80aa3bf64bb45cbca5cf9f75efd9348cf2ac690b907435238c3cf81d7
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA256:0fe29ecd5d445805e33b33d7ff35813eabab2100806c06dd002efd35b37fb855
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.debian.tar.xz' hicolor-icon-theme_0.18-2.debian.tar.xz 9148 SHA256:749d43f2b8f67f301ce08ca29b5c8492e8eed12bbe2974c7db40ca4a0b834508
```

Other potentially useful URLs:

- https://sources.debian.net/src/hicolor-icon-theme/0.18-2/ (for browsing the source)
- https://sources.debian.net/src/hicolor-icon-theme/0.18-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hicolor-icon-theme/0.18-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA256:80aadf116c3423044be69a4cef8ba2766f412bd4d46a500aacb61f303c19c4ef
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA256:5bb5d1be011158090157c9e7587ae5606c262a5020ecdc5caac6686b9910592e
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.25/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.25/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.25/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `icu=76.1-3`

Binary Packages:

- `icu-devtools=76.1-3`
- `libicu-dev:amd64=76.1-3`
- `libicu76:amd64=76.1-3`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu76/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=76.1-3
'http://deb.debian.org/debian/pool/main/i/icu/icu_76.1-3.dsc' icu_76.1-3.dsc 2236 SHA256:79dd7a3643acddc5218ceb597320edbe01a3fc9b0f9c7a2b456694afac4bbb15
'http://deb.debian.org/debian/pool/main/i/icu/icu_76.1.orig.tar.gz' icu_76.1.orig.tar.gz 27437767 SHA256:dfacb46bfe4747410472ce3e1144bf28a102feeaa4e3875bac9b4c6cf30f4f3e
'http://deb.debian.org/debian/pool/main/i/icu/icu_76.1.orig.tar.gz.asc' icu_76.1.orig.tar.gz.asc 228 SHA256:6ef6ef96376eb6550f2b450e08b84c29238f60a77b89273f1521e1b57db73472
'http://deb.debian.org/debian/pool/main/i/icu/icu_76.1-3.debian.tar.xz' icu_76.1-3.debian.tar.xz 63784 SHA256:c8f775809d791490284db9ba8c00d73ef8960bd044619a17763b1f72fb14cf44
```

Other potentially useful URLs:

- https://sources.debian.net/src/icu/76.1-3/ (for browsing the source)
- https://sources.debian.net/src/icu/76.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/icu/76.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `imagemagick=8:7.1.1.43+dfsg1-1`

Binary Packages:

- `imagemagick=8:7.1.1.43+dfsg1-1`
- `imagemagick-7-common=8:7.1.1.43+dfsg1-1`
- `imagemagick-7.q16=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7-arch-config:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7-headers=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-10:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-dev=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7-headers=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7.q16-10:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickwand-dev=8:7.1.1.43+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-7-common/copyright`, `/usr/share/doc/imagemagick-7.q16/copyright`, `/usr/share/doc/libmagickcore-7-arch-config/copyright`, `/usr/share/doc/libmagickcore-7-headers/copyright`, `/usr/share/doc/libmagickcore-7.q16-10/copyright`, `/usr/share/doc/libmagickcore-7.q16-10-extra/copyright`, `/usr/share/doc/libmagickcore-7.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-7-headers/copyright`, `/usr/share/doc/libmagickwand-7.q16-10/copyright`, `/usr/share/doc/libmagickwand-7.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

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
$ apt-get source -qq --print-uris imagemagick=8:7.1.1.43+dfsg1-1
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1.dsc' imagemagick_7.1.1.43+dfsg1-1.dsc 5129 SHA256:ea905fe178cb4f854ee59f2e7444de0b8369767a30d988766f2e6c62638802c0
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1.orig.tar.xz' imagemagick_7.1.1.43+dfsg1.orig.tar.xz 10501740 SHA256:bcb4f3c78a930a608fa4889f889edbcb384974246ad9407fce1858f2c0607bfe
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1.debian.tar.xz' imagemagick_7.1.1.43+dfsg1-1.debian.tar.xz 275384 SHA256:4315813d0e1f9f76e7e77387fed5fcd152f540473d3ba97f37d5855b115b119e
```

Other potentially useful URLs:

- https://sources.debian.net/src/imagemagick/8:7.1.1.43+dfsg1-1/ (for browsing the source)
- https://sources.debian.net/src/imagemagick/8:7.1.1.43+dfsg1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/imagemagick/8:7.1.1.43+dfsg1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `imath=3.1.12-1`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1+b3`
- `libimath-dev:amd64=3.1.12-1+b3`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.12-1.dsc' imath_3.1.12-1.dsc 2721 SHA256:4e2161a9517b5241c2c48e750ea0aed5586c73ebb17b30b56a7b02e96d6d61d7
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA256:8a1bc258f3149b5729c2f4f8ffd337c0e57f09096e4ba9784329f40c4a9035da
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA256:a2c4ac5151789903ca8ab3093a2798491463ccf2abfd003a20f96453e505dd5f
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.12-1.debian.tar.xz' imath_3.1.12-1.debian.tar.xz 9800 SHA256:d5f9d34eff5ff87d5c9cb1d626cb42383eb85cb4af08720e10b9922b74196913
```

Other potentially useful URLs:

- https://sources.debian.net/src/imath/3.1.12-1/ (for browsing the source)
- https://sources.debian.net/src/imath/3.1.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/imath/3.1.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `init-system-helpers=1.68`

Binary Packages:

- `init-system-helpers=1.68`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.68
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA256:58bf10802cf5d2496059368948a80d4a49f768d27b918fbe6dc28353c6cda72c
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA256:cdf1c7fe87362a4e3f7446a95b75c29ca6071fda3911adb269508203cd3c458d
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.68/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.68/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.68/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA256:35ceb67dbb1b4098431b184e342143c2bd94c4a41ebfb3a983e3be31440b0453
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA256:6d8babb59e7b672e8cb7870e874f3f7b813b6e00e6af3f8b04f7579965643d5c
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA256:1ac2e33075903489d4284ff4e86645405e68a282a80432ee4ee0c43397f59224
```

Other potentially useful URLs:

- https://sources.debian.net/src/isl/0.27-1/ (for browsing the source)
- https://sources.debian.net/src/isl/0.27-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/isl/0.27-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b3`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA256:6296ddd9c0a022bd1b70074aefb171cfcdf5694a04ffd32b35fd66097621af87
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA256:c739578bf6b764aa0752db9a2fdadcfe921c78f1228c7ec0bb47fa804c55d17b
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA256:e89fe4fd8221f6934ddb50f2e7f8404311928d0e23e49a5599f3d3d14ee8cb88
```

Other potentially useful URLs:

- https://sources.debian.net/src/jansson/2.14-2/ (for browsing the source)
- https://sources.debian.net/src/jansson/2.14-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jansson/2.14-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jbigkit=2.1-6.1`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1+b2`
- `libjbig0:amd64=2.1-6.1+b2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.dsc' jbigkit_2.1-6.1.dsc 2089 SHA256:8dea586c47cb4b2436f77fd33ef4a702b9da936d74de8332a72a8ddbe8124e09
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.debian.tar.xz' jbigkit_2.1-6.1.debian.tar.xz 9244 SHA256:c9ba99e84d18b1affdc97b26b625721ed06b41a92996d9b426b62c0dbe3868cd
```

Other potentially useful URLs:

- https://sources.debian.net/src/jbigkit/2.1-6.1/ (for browsing the source)
- https://sources.debian.net/src/jbigkit/2.1-6.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jbigkit/2.1-6.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `keyutils=1.6.3-4`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-4`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-4
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-4.dsc' keyutils_1.6.3-4.dsc 2193 SHA256:1943ee7376e7abedfebce2285c04a5c1d3062f63fce14ab2bcfbf65c52073b89
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-4.debian.tar.xz' keyutils_1.6.3-4.debian.tar.xz 13872 SHA256:d64f58058ba3f3776e068fdd4cddf9a7a81b19006563a1e8d10894d949923806
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.6.3-4/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.6.3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.6.3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.21.3-5`

Binary Packages:

- `krb5-multidev:amd64=1.21.3-5`
- `libgssapi-krb5-2:amd64=1.21.3-5`
- `libgssrpc4t64:amd64=1.21.3-5`
- `libk5crypto3:amd64=1.21.3-5`
- `libkadm5clnt-mit12:amd64=1.21.3-5`
- `libkadm5srv-mit12:amd64=1.21.3-5`
- `libkdb5-10t64:amd64=1.21.3-5`
- `libkrb5-3:amd64=1.21.3-5`
- `libkrb5-dev:amd64=1.21.3-5`
- `libkrb5support0:amd64=1.21.3-5`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-5.dsc' krb5_1.21.3-5.dsc 3983 SHA256:88e736b6439d0fe30317ae7c38c3093b7139f1b7709997debe28d756f92de353
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-5.debian.tar.xz' krb5_1.21.3-5.debian.tar.xz 104424 SHA256:521fdfaf5cda93a64cc70afd357dc31ea6f4128ff5a489b036b58887eceddd46
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.21.3-5/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.21.3-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.21.3-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lcms2=2.16-2`

Binary Packages:

- `liblcms2-2:amd64=2.16-2`
- `liblcms2-dev:amd64=2.16-2`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.16-2
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.16-2.dsc' lcms2_2.16-2.dsc 1972 SHA256:3e5796b630090628b5a5662f002d4a9909592963626514241dd201e45e7b1d1c
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.16.orig.tar.gz' lcms2_2.16.orig.tar.gz 7632822 SHA256:d873d34ad8b9b4cea010631f1a6228d2087475e4dc5e763eb81acc23d9d45a51
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.16-2.debian.tar.xz' lcms2_2.16-2.debian.tar.xz 11908 SHA256:5475f5d85514c3004a33a2c103a01a7f6a8ed4fcb41d53518d098fb927b4f916
```

Other potentially useful URLs:

- https://sources.debian.net/src/lcms2/2.16-2/ (for browsing the source)
- https://sources.debian.net/src/lcms2/2.16-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lcms2/2.16-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lerc=4.0.0+ds-5`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-5`
- `liblerc4:amd64=4.0.0+ds-5`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.dsc' lerc_4.0.0+ds-5.dsc 2673 SHA256:84de8dac3dd5f5edc005c5c02be58c1f549f9365ad4147c138c85e07d624cc12
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.debian.tar.xz' lerc_4.0.0+ds-5.debian.tar.xz 8576 SHA256:28ab2b1c19c845cd493e804bb9c43b47f72d5852281ebf832ed68a7576afbf6d
```

Other potentially useful URLs:

- https://sources.debian.net/src/lerc/4.0.0+ds-5/ (for browsing the source)
- https://sources.debian.net/src/lerc/4.0.0+ds-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lerc/4.0.0+ds-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=3.0.2-2`

Binary Packages:

- `libassuan9:amd64=3.0.2-2`

Licenses: (parsed from: `/usr/share/doc/libassuan9/copyright`)

- `FSFULLR`
- `FSFULLRWD`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-2.with.nonstandard.Autoconf-data.exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `GPL-3+ with Autoconf-data exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libassuan=3.0.2-2
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2-2.dsc' libassuan_3.0.2-2.dsc 2682 SHA256:4c6b68814cef421d1768628b401a62176c579dc8e1e3026348d7ec159943f0c7
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA256:d2931cdad266e633510f9970e1a2f346055e351bb19f9b78912475b8074c36f6
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA256:3799b287fd7d48f750597bd9104621d2cbafd508de83303b1a5f5eef08f06072
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2-2.debian.tar.xz' libassuan_3.0.2-2.debian.tar.xz 17536 SHA256:05566fa4ac35ad6af7214ce01beeaffcc2ce1c13d20daac4cf86949c5fad25fc
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/3.0.2-2/ (for browsing the source)
- https://sources.debian.net/src/libassuan/3.0.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/3.0.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libbsd=0.12.2-2`

Binary Packages:

- `libbsd0:amd64=0.12.2-2`

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
$ apt-get source -qq --print-uris libbsd=0.12.2-2
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA256:01eb1d0c896096f9038213f5f00376ecfd1c0d1def21b7042f28ae070e4837e3
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA256:36c878a32c1f190ca2cb474de5c6139990a6c029906493d3566770b1ebd569bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.12.2-2/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.12.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.12.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.8.5-4`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.dsc' libcap-ng_0.8.5-4.dsc 1710 SHA256:a5745b7d68a11068ae5beddcc7fbc94cd87dd81cb2d7495e7d48610603be3526
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.debian.tar.xz' libcap-ng_0.8.5-4.debian.tar.xz 7816 SHA256:f5d4e7f38bdbca87de77317ce95f973883081370ef257019b484e29e3368a20d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.8.5-4/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.8.5-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.8.5-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap2=1:2.75-4`

Binary Packages:

- `libcap2:amd64=1:2.75-4`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-4
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75-4.dsc' libcap2_2.75-4.dsc 2466 SHA256:122d050adc9896829461e0fdb13a08a34c7ae682c80efc73c2c1916a4743842e
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA256:de4e7e064c9ba451d5234dd46e897d7c71c96a9ebf9a0c445bc04f4742d83632
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA256:c71b593e7c3160fd7f406641074d93462bbc4906c9243937a0e232f42d5c54d2
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.75-4.debian.tar.xz' libcap2_2.75-4.debian.tar.xz 21304 SHA256:131bbe80c3caadb417627cb5024ea5c36ed773e04f4bc64e8a5d2f72c6dc40b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap2/1:2.75-4/ (for browsing the source)
- https://sources.debian.net/src/libcap2/1:2.75-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap2/1:2.75-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcbor=0.10.2-2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-2.dsc' libcbor_0.10.2-2.dsc 2156 SHA256:45d6e3f92a54584c5a19ea861095d04415d1eb380658a0e6ee61f690f378cba3
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA256:e75f712215d7b7e5c89ef322a09b701f7159f028b8b48978865725f00f79875b
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-2.debian.tar.xz' libcbor_0.10.2-2.debian.tar.xz 6148 SHA256:85c84ec8bafc8369fddb183ddb4c173cb23b1fc5f57bdd94e2763c4bdbccc6ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcbor/0.10.2-2/ (for browsing the source)
- https://sources.debian.net/src/libcbor/0.10.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcbor/0.10.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libdatrie=0.2.13-3`

Binary Packages:

- `libdatrie-dev:amd64=0.2.13-3+b1`
- `libdatrie1:amd64=0.2.13-3+b1`

Licenses: (parsed from: `/usr/share/doc/libdatrie-dev/copyright`, `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.dsc' libdatrie_0.2.13-3.dsc 2236 SHA256:6ddcaf319da01cc044f9b335b6b01b608a0380ccdaecb06bda71710b6f4395bb
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA256:12231bb2be2581a7f0fb9904092d24b0ed2a271a16835071ed97bed65267f4be
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.debian.tar.xz' libdatrie_0.2.13-3.debian.tar.xz 9668 SHA256:e656d536beb5db9e52ef92dd1fccd5480ebd21e4eddbfe013c51a1e2ec45cf38
```

Other potentially useful URLs:

- https://sources.debian.net/src/libdatrie/0.2.13-3/ (for browsing the source)
- https://sources.debian.net/src/libdatrie/0.2.13-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libdatrie/0.2.13-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libde265=1.0.15-1`

Binary Packages:

- `libde265-0:amd64=1.0.15-1+b3`

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
$ apt-get source -qq --print-uris libde265=1.0.15-1
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15-1.dsc' libde265_1.0.15-1.dsc 1872 SHA256:41fe11a559a57a8cdf19978c55f58f0d83de78c61e1367f8b73d05bdcce416eb
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15.orig.tar.gz' libde265_1.0.15.orig.tar.gz 846016 SHA256:00251986c29d34d3af7117ed05874950c875dd9292d016be29d3b3762666511d
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15-1.debian.tar.xz' libde265_1.0.15-1.debian.tar.xz 136584 SHA256:70cb236e55972d2d1bc062bacd68320ad402e0d378c79c99224a512208c90e5b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libde265/1.0.15-1/ (for browsing the source)
- https://sources.debian.net/src/libde265/1.0.15-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libde265/1.0.15-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libdeflate=1.23-1`

Binary Packages:

- `libdeflate-dev:amd64=1.23-1+b1`
- `libdeflate0:amd64=1.23-1+b1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-1
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.23-1.dsc' libdeflate_1.23-1.dsc 2214 SHA256:392c29c266379d6f9c9b80ea4d1997305fb5cf64d192474b2191be07cc1edcf4
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA256:1ab18349b9fb0ce8a0ca4116bded725be7dcbfa709e19f6f983d99df1fb8b25f
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.23-1.debian.tar.xz' libdeflate_1.23-1.debian.tar.xz 5536 SHA256:1cf0ab0f0100c2d6b544982854fd4bb71c732be9bd1685af2098baf15d2171b1
```

Other potentially useful URLs:

- https://sources.debian.net/src/libdeflate/1.23-1/ (for browsing the source)
- https://sources.debian.net/src/libdeflate/1.23-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libdeflate/1.23-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libedit=3.1-20250104-1`

Binary Packages:

- `libedit2:amd64=3.1-20250104-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20250104-1
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20250104-1.dsc' libedit_3.1-20250104-1.dsc 2264 SHA256:1faea2073588dc3310133fb2dca5b9b6d3e759ae8653c2afefa1c802085cf544
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20250104.orig.tar.gz' libedit_3.1-20250104.orig.tar.gz 546745 SHA256:23792701694550a53720630cd1cd6167101b5773adddcb4104f7345b73a568ac
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20250104-1.debian.tar.xz' libedit_3.1-20250104-1.debian.tar.xz 16708 SHA256:2720852d7c1bb1634b682ed24d700e0313167e5a5529a5b7cc95a5d0e24273fe
```

Other potentially useful URLs:

- https://sources.debian.net/src/libedit/3.1-20250104-1/ (for browsing the source)
- https://sources.debian.net/src/libedit/3.1-20250104-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libedit/3.1-20250104-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liberror-perl=0.17030-1`

Binary Packages:

- `liberror-perl=0.17030-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17030-1
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.dsc' liberror-perl_0.17030-1.dsc 2337 SHA256:44590c5e4057ee2b2090b7ca661cdbead886528a2b5b5fa7ae708f8b9c1814bf
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030.orig.tar.gz' liberror-perl_0.17030.orig.tar.gz 33488 SHA256:34d382276c0fb0d6b38355b94c96a30b12d834d5662eb53f088ee25e3e712924
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.debian.tar.xz' liberror-perl_0.17030-1.debian.tar.xz 4660 SHA256:6824b886f5068d9345279e2425b423fd47623c3ffe74732074b67c5863040ac7
```

Other potentially useful URLs:

- https://sources.debian.net/src/liberror-perl/0.17030-1/ (for browsing the source)
- https://sources.debian.net/src/liberror-perl/0.17030-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liberror-perl/0.17030-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libevent=2.1.12-stable-10`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-10+b1`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-10+b1`
- `libevent-dev=2.1.12-stable-10+b1`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-10+b1`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-10+b1`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-10+b1`

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
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable-10.dsc' libevent_2.1.12-stable-10.dsc 2412 SHA256:43ebc80590ab06ab0bdc6a07d4e5d85b4c5ce4ef61bf82103edcc4603873abe0
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA256:92e6de1be9ec176428fd2367677e61ceffc2ee1cb119035037a27d346b0403bb
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable-10.debian.tar.xz' libevent_2.1.12-stable-10.debian.tar.xz 17908 SHA256:82743ad3391b9868516826b37e60a199aae9830f94d1ba5042f62dcbbe375349
```

Other potentially useful URLs:

- https://sources.debian.net/src/libevent/2.1.12-stable-10/ (for browsing the source)
- https://sources.debian.net/src/libevent/2.1.12-stable-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libevent/2.1.12-stable-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libexif=0.6.25-1`

Binary Packages:

- `libexif-dev:amd64=0.6.25-1`
- `libexif12:amd64=0.6.25-1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-3-Clause`
- `CC0-1.0`
- `GPL-2`
- `GPL-2.0`
- `LGPL-2.1`
- `LGPL-2.1-or-later`
- `LicenseRef-Wrobel`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.25-1
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.25-1.dsc' libexif_0.6.25-1.dsc 2091 SHA256:7ab0af52a1679e23e45cae31b3f8c83323ac5d5b7c731516abbbd182b7babff7
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.25.orig.tar.gz' libexif_0.6.25.orig.tar.gz 1253324 SHA256:ee0795432c20d2fdb2a8a579dd6fc0e19d402e36f14f42c03ab60d2345950f09
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.25-1.debian.tar.xz' libexif_0.6.25-1.debian.tar.xz 12104 SHA256:d0e5ebb493300088ea83b3e9110dcb4d2bf86d6870dd02c01668b6fdc00eeca1
```

Other potentially useful URLs:

- https://sources.debian.net/src/libexif/0.6.25-1/ (for browsing the source)
- https://sources.debian.net/src/libexif/0.6.25-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libexif/0.6.25-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.4.7-1`

Binary Packages:

- `libffi-dev:amd64=3.4.7-1`
- `libffi8:amd64=3.4.7-1`

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
$ apt-get source -qq --print-uris libffi=3.4.7-1
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.7-1.dsc' libffi_3.4.7-1.dsc 1948 SHA256:905661067ccb62604691b4fdfffaaa29e0af6fe9994a61cb1e7ad6befc2eb5ae
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.7.orig.tar.gz' libffi_3.4.7.orig.tar.gz 593636 SHA256:f07c08c9c14977eafb9b5f9277713d91358ec18fc8aaa5607d6790cde90cba12
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.7-1.debian.tar.xz' libffi_3.4.7-1.debian.tar.xz 10776 SHA256:af65d5c7024e664f71ba2b3a0ff4b72dc885d8d1b75a7d2d596f3d8e36eb3229
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.4.7-1/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.4.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.4.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libfido2=1.15.0-1`

Binary Packages:

- `libfido2-1:amd64=1.15.0-1+b1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.15.0-1
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0-1.dsc' libfido2_1.15.0-1.dsc 2585 SHA256:eb792b5b55bfd5421ce9abb30797317767b9b3e5884a071ab31e16a39ba21aba
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz' libfido2_1.15.0.orig.tar.gz 670019 SHA256:abaab1318d21d262ece416fb8a7132fa9374bda89f6fa52b86a98a2f5712b61e
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz.asc' libfido2_1.15.0.orig.tar.gz.asc 228 SHA256:7b757a545a07c989c75528d884d863a52ba61a4cc94661338dbbb2b7e62560ee
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0-1.debian.tar.xz' libfido2_1.15.0-1.debian.tar.xz 52960 SHA256:4c20c21cffd478556f2fd2ab1ab529fd75bc1fc499f0851a45af91f78c3b4626
```

Other potentially useful URLs:

- https://sources.debian.net/src/libfido2/1.15.0-1/ (for browsing the source)
- https://sources.debian.net/src/libfido2/1.15.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libfido2/1.15.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgcrypt20=1.11.0-7`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-7
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7.dsc' libgcrypt20_1.11.0-7.dsc 2945 SHA256:275f26ee0b57fe374b8642213f8d5896bdd22f0d687727f8869701d72308b719
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA256:09120c9867ce7f2081d6aaa1775386b98c2f2f246135761aae47d81f58685b9c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA256:9fedf4f7bb80d5178d4e26ec2f03ba5fc44eddfc72c2e9966d7d619aeee3df2c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7.debian.tar.xz' libgcrypt20_1.11.0-7.debian.tar.xz 40452 SHA256:c6811619ea9ae05a214256264c21816b3d1cf1d5ae1113f658071efae3ba9355
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.11.0-7/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.11.0-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.11.0-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.51-4`

Binary Packages:

- `libgpg-error0:amd64=1.51-4`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.51-4
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.51-4.dsc' libgpg-error_1.51-4.dsc 2956 SHA256:fecb803e22016cbf46b7c0a0d5c23f8a45a2f70fa10d3b3b67b10be917987410
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2' libgpg-error_1.51.orig.tar.bz2 1085510 SHA256:be0f1b2db6b93eed55369cdf79f19f72750c8c7c39fc20b577e724545427e6b2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2.asc' libgpg-error_1.51.orig.tar.bz2.asc 228 SHA256:5e8c9179635b3105f4c07d09168fda9ce039607e926628aec6a06134908be918
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.51-4.debian.tar.xz' libgpg-error_1.51-4.debian.tar.xz 22332 SHA256:9d1edd110f540c9f7163035f352836dd968ca38977f31adb073b99b9a05f8c4d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.51-4/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.51-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.51-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libheif=1.19.7-1`

Binary Packages:

- `libheif-plugin-dav1d:amd64=1.19.7-1`
- `libheif-plugin-libde265:amd64=1.19.7-1`
- `libheif1:amd64=1.19.7-1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-dav1d/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

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
$ apt-get source -qq --print-uris libheif=1.19.7-1
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.19.7-1.dsc' libheif_1.19.7-1.dsc 3631 SHA256:ee16f79a0301e070a1658d402df33b01a922522c236e79599431376f070a6ac1
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.19.7.orig.tar.gz' libheif_1.19.7.orig.tar.gz 1717186 SHA256:161c042d2102665fcee3ded851c78a0eb5f2d4bfe39fba48ba6e588fd6e964f3
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.19.7-1.debian.tar.xz' libheif_1.19.7-1.debian.tar.xz 12240 SHA256:538d639af752d5d863e09e79d0aa1f5b366e1ae5066eec22f0c3904002f9cfdd
```

Other potentially useful URLs:

- https://sources.debian.net/src/libheif/1.19.7-1/ (for browsing the source)
- https://sources.debian.net/src/libheif/1.19.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libheif/1.19.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libice=2:1.1.1-1`

Binary Packages:

- `libice-dev:amd64=2:1.1.1-1`
- `libice6:amd64=2:1.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.1.1-1.dsc' libice_1.1.1-1.dsc 2021 SHA256:88722aa66d7f1807d1b0d3ae5bc62f8f06424dc5e970b1c73a0ea2fdf171f0b8
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA256:04fbd34a11ba08b9df2e3cdb2055c2e3c1c51b3257f683d7fcf42dabcf8e1210
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.1.1-1.diff.gz' libice_1.1.1-1.diff.gz 7355 SHA256:8ce8ffaf775b0868e0633053fcd0755850938ddda9d977232e536a206c063d18
```

Other potentially useful URLs:

- https://sources.debian.net/src/libice/2:1.1.1-1/ (for browsing the source)
- https://sources.debian.net/src/libice/2:1.1.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libice/2:1.1.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libidn2=2.3.8-2`

Binary Packages:

- `libidn2-0:amd64=2.3.8-2`
- `libidn2-dev:amd64=2.3.8-2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-2
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8-2.dsc' libidn2_2.3.8-2.dsc 2961 SHA256:af3327227dbbf12fff281f71b7feb90371d2dbe597f3129e38b93c3faadcea61
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA256:bbad1678d35d28e2c62e6a2577083829461402d9e47b908791c55314a5cb5e04
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA256:8995cab7db361d9d6989eab26d9b521c74236960a5d78250121c8d369b013bd8
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8-2.debian.tar.xz' libidn2_2.3.8-2.debian.tar.xz 17532 SHA256:ab95c2bab110557505ba437bc162f67a5a85fa9d8a2e55501245dc7f0fe2e412
```

Other potentially useful URLs:

- https://sources.debian.net/src/libidn2/2.3.8-2/ (for browsing the source)
- https://sources.debian.net/src/libidn2/2.3.8-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libidn2/2.3.8-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-3.1`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-3.1`
- `libjpeg62-turbo:amd64=1:2.1.5-3.1`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-3.1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-3.1
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.1.dsc' libjpeg-turbo_2.1.5-3.1.dsc 2478 SHA256:3b1089198a0f5dd0f6af7a6bbb381c0c710eb1cedf4ae887115a4c8209f081f3
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.1.debian.tar.xz' libjpeg-turbo_2.1.5-3.1.debian.tar.xz 107924 SHA256:ec48689b143c03fbc0a06e116f3916ca319afd8b9f2ef2b1226e245464878856
```

Other potentially useful URLs:

- https://sources.debian.net/src/libjpeg-turbo/1:2.1.5-3.1/ (for browsing the source)
- https://sources.debian.net/src/libjpeg-turbo/1:2.1.5-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libjpeg-turbo/1:2.1.5-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libksba=1.6.7-2`

Binary Packages:

- `libksba8:amd64=1.6.7-2+b1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA256:47f8b314c6b74fdcfb42390327dc0441c6ba6bfdb4511ca12e2b4478fc452e1c
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA256:cf72510b8ebb4eb6693eef765749d83677a03c79291a311040a5bfd79baab763
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA256:cd704f8100151752b12776fa87dac42a3f99334ed155bcbcbaeda8e786581316
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA256:28f0ef1f9dd2a7f1cef23e49393d750d50aade01476462d8d5225a23e4ad9929
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.6.7-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.6.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.6.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liblqr=0.4.2-2.1`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1+b2`
- `liblqr-1-0-dev:amd64=0.4.2-2.1+b2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.1.dsc' liblqr_0.4.2-2.1.dsc 2095 SHA256:c54c34cd2f7470a29366eeacde2ca4859a97d684a406fb81a918b970c01d617c
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA256:d4c22373432cca749e4326cd41fce365e6ff857c0bfd7a5302b8eb34b69f0336
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.1.debian.tar.xz' liblqr_0.4.2-2.1.debian.tar.xz 5300 SHA256:284a002f1ecac63ac17b1aafbb230da9ce7bd9efe2d5b94e8cad49b607eb2564
```

Other potentially useful URLs:

- https://sources.debian.net/src/liblqr/0.4.2-2.1/ (for browsing the source)
- https://sources.debian.net/src/liblqr/0.4.2-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liblqr/0.4.2-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmaxminddb=1.12.2-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.12.2-1`
- `libmaxminddb0:amd64=1.12.2-1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `LGPL-3`
- `LGPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.12.2-1
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1.dsc' libmaxminddb_1.12.2-1.dsc 2235 SHA256:eff18dd8d9b1f191c206faa166acae9224453dc9a18e03f65b24f65b0d456f69
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2.orig.tar.gz' libmaxminddb_1.12.2.orig.tar.gz 369848 SHA256:c0b20260a54cf4cebd3b879ac8e487cf2eac218fe6a5f64f1e2c3032b564fdd8
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1.debian.tar.xz' libmaxminddb_1.12.2-1.debian.tar.xz 6912 SHA256:39e24b93cdebcb869fc0b45020ff86b0a318ac463fcbcb33f0ea3f12d7bb091a
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmaxminddb/1.12.2-1/ (for browsing the source)
- https://sources.debian.net/src/libmaxminddb/1.12.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmaxminddb/1.12.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2+b1`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmd/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/libmd/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmd/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpng1.6=1.6.47-1.1`

Binary Packages:

- `libpng-dev:amd64=1.6.47-1.1`
- `libpng16-16t64:amd64=1.6.47-1.1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.47-1.1
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47-1.1.dsc' libpng1.6_1.6.47-1.1.dsc 2287 SHA256:82ff8051d34181df9ad5d951801d000563613afc357246b73f8db2ad69a7d00f
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47.orig.tar.gz' libpng1.6_1.6.47.orig.tar.gz 1571845 SHA256:631a4c58ea6c10c81f160c4b21fa8495b715d251698ebc2552077e8450f30454
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47-1.1.debian.tar.xz' libpng1.6_1.6.47-1.1.debian.tar.xz 33204 SHA256:288540aedc46a760f7eb0dc5b58d92d7b647a15fcec3e7ec557ada3aa3dd2579
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpng1.6/1.6.47-1.1/ (for browsing the source)
- https://sources.debian.net/src/libpng1.6/1.6.47-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpng1.6/1.6.47-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpsl=0.21.2-1.1`

Binary Packages:

- `libpsl-dev:amd64=0.21.2-1.1+b1`
- `libpsl5t64:amd64=0.21.2-1.1+b1`

Licenses: (parsed from: `/usr/share/doc/libpsl-dev/copyright`, `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.dsc' libpsl_0.21.2-1.1.dsc 2285 SHA256:b9b5496ca2bffb827cb0b2d997469908a2b7a7475c20a11c02f9dcd1ed2a0cc9
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.debian.tar.xz' libpsl_0.21.2-1.1.debian.tar.xz 12120 SHA256:0eccab147b6dfbfb7f5ad40fb5bd9f888d72a0fe44e7d1801811c34a9acad1a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpsl/0.21.2-1.1/ (for browsing the source)
- https://sources.debian.net/src/libpsl/0.21.2-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpsl/0.21.2-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libraw=0.21.3-1`

Binary Packages:

- `libraw23t64:amd64=0.21.3-1+b1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.3-1
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.3-1.dsc' libraw_0.21.3-1.dsc 2364 SHA256:20ce2be6b6de0c44764e0cc680099b2f59bc25609d183fb5e410fded65de6417
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.3.orig.tar.gz' libraw_0.21.3.orig.tar.gz 566017 SHA256:dc3d8b54e333d9d5441336049db255d14b27f19bd326a306cf5aea866806780a
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.3-1.debian.tar.xz' libraw_0.21.3-1.debian.tar.xz 24172 SHA256:a5cc438c93f27aedeabd8c7d6cf2d38d5b29facce4b0f8ed8454f7c8c9e4538f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libraw/0.21.3-1/ (for browsing the source)
- https://sources.debian.net/src/libraw/0.21.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libraw/0.21.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `librsvg=2.60.0+dfsg-1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.60.0+dfsg-1`
- `librsvg2-2:amd64=2.60.0+dfsg-1`
- `librsvg2-common:amd64=2.60.0+dfsg-1`
- `librsvg2-dev:amd64=2.60.0+dfsg-1`

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
$ apt-get source -qq --print-uris librsvg=2.60.0+dfsg-1
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg-1.dsc' librsvg_2.60.0+dfsg-1.dsc 3057 SHA256:c6584073d5e7b69819e45f14bb0e1b943517ceae7cdecc0068b2f1db22ba913d
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg.orig.tar.xz' librsvg_2.60.0+dfsg.orig.tar.xz 6735208 SHA256:1b9f126ad3115e4126c682f3011023a05dcf19a69e5e878fbffb420ade671b81
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg-1.debian.tar.xz' librsvg_2.60.0+dfsg-1.debian.tar.xz 10832756 SHA256:58db12d59958016e3b114de74ebe137255da9a900593f0a9d5b3392709a7cbe7
```

Other potentially useful URLs:

- https://sources.debian.net/src/librsvg/2.60.0+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/librsvg/2.60.0+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/librsvg/2.60.0+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.6.0-2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.dsc' libseccomp_2.6.0-2.dsc 2622 SHA256:d05f94536558d34fa339326c6f958a3357b51efac8234470b5d97b69472db765
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA256:83b6085232d1588c379dc9b9cae47bb37407cf262e6e74993c61ba72d2a784dc
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA256:52e338fa958128293cbd25d2be189e34da41c4f4abbb1b641cf58f373c001f94
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.debian.tar.xz' libseccomp_2.6.0-2.debian.tar.xz 20800 SHA256:ed705ec85719403e77d004c99c0b06b795f090c66fcae265c4bcf37ffea9cc27
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.6.0-2/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.6.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.6.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.8.1-1`

Binary Packages:

- `libselinux1:amd64=3.8.1-1`
- `libselinux1-dev:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.8.1-1
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.8.1-1.dsc' libselinux_3.8.1-1.dsc 3013 SHA256:e430b782a396e266f86c32fa779efadebfd40e6a0d10ddbd786fc47905f723b9
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz' libselinux_3.8.1.orig.tar.gz 204411 SHA256:ec2d2789f931152d21c1db1eb4bc202ce4eccede34d9be9e360e3b45243cee2c
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz.asc' libselinux_3.8.1.orig.tar.gz.asc 833 SHA256:7f983714a780d89f7677e7ba140ce29974022b8ba225f60246b6c33de1477dd6
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.8.1-1.debian.tar.xz' libselinux_3.8.1-1.debian.tar.xz 37812 SHA256:1af25952374f083cf3d6d0edd5beb938f2e53c30eb404afa1e32fcd1cb127db7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.8.1-1/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.8.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.8.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=3.8.1-1`

Binary Packages:

- `libsemanage-common=3.8.1-1`
- `libsemanage2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.8.1-1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.8.1-1.dsc' libsemanage_3.8.1-1.dsc 2992 SHA256:b22bfc4ab2cd47fac46cc9e45d418bb30eb540c3e5c1052d6c669f53e180e4e5
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz' libsemanage_3.8.1.orig.tar.gz 184618 SHA256:7b39127b219cc70bfd935a4af6b0f2ba83d4b35c916f253c7e942c23ab490f07
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz.asc' libsemanage_3.8.1.orig.tar.gz.asc 833 SHA256:5b4856cb5823fba1b247ff1b5355692706da68a4df61a936d1b33b1f9e9b2f3d
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.8.1-1.debian.tar.xz' libsemanage_3.8.1-1.debian.tar.xz 37572 SHA256:6d1e5bd4d06bbd25ced1b75fba394c3e2157bd604cf1cd33fb581793d70bd7b8
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.8.1-1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.8.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.8.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.8.1-1`

Binary Packages:

- `libsepol-dev:amd64=3.8.1-1`
- `libsepol2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.8.1-1
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.8.1-1.dsc' libsepol_3.8.1-1.dsc 2347 SHA256:0351ffc8c3f66918c9e4ecae9244ae2af27857d8795e424e384ddda794718c34
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz' libsepol_3.8.1.orig.tar.gz 513830 SHA256:0e78705305f955abd4c0654d37a5477ee26349ab74db9e2b03a7868897ae1ddf
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz.asc' libsepol_3.8.1.orig.tar.gz.asc 833 SHA256:183f6cf96054986704d4224f89518e9139370385c43a533078f45ca688dca8b6
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.8.1-1.debian.tar.xz' libsepol_3.8.1-1.debian.tar.xz 21432 SHA256:7aac515a941f8dd19581b16c664b3098962e6a8ed7fa0afdafd306a85c667619
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.8.1-1/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.8.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.8.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsm=2:1.2.6-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.6-1`
- `libsm6:amd64=2:1.2.6-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.6-1.dsc' libsm_1.2.6-1.dsc 2302 SHA256:d0ab34a54b145ea728242638b878d05f84bcb71feabf075c5e9510cc608aab93
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA256:166b4b50d606cdd83f1ddc61b5b9162600034f848b3e32ccbb0e63536b7d6cdd
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA256:b5e59abae8a79ae9901e73178dacf5af9d7c3b91704fd86de85d305fd7a17a7f
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.6-1.diff.gz' libsm_1.2.6-1.diff.gz 13291 SHA256:7cc1d915c18fa6c34cc57c44ca844b62e99fba79b70c0941466d3747e15f2195
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsm/2:1.2.6-1/ (for browsing the source)
- https://sources.debian.net/src/libsm/2:1.2.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsm/2:1.2.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libssh2=1.11.1-1`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1`
- `libssh2-1t64:amd64=1.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.dsc' libssh2_1.11.1-1.dsc 2319 SHA256:f97f7ac25300908b255a29c63055e78684e68c12c308edb016747da1de592377
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA256:d9ec76cbe34db98eec3539fe2c899d26b0c837cb3eb466a56b0f109cabf658f7
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA256:f5618c9356a1d5a8059d6cf64015d86547f06b2b8b1f542fbbaf381a736c8075
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.debian.tar.xz' libssh2_1.11.1-1.debian.tar.xz 17136 SHA256:f3b9e55f706c89e9408478a1eecb0067b8e18902e0cab168f44194fcc53641cf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libssh2/1.11.1-1/ (for browsing the source)
- https://sources.debian.net/src/libssh2/1.11.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libssh2/1.11.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`
- `libtasn1-6-dev:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.20.0-2
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.dsc' libtasn1-6_4.20.0-2.dsc 2665 SHA256:54800d16bf3c7eaf675356f2e9d30226991710d78717219bb6425dcc453a55a2
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz' libtasn1-6_4.20.0.orig.tar.gz 1783873 SHA256:92e0e3bd4c02d4aeee76036b2ddd83f0c732ba4cda5cb71d583272b23587a76c
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz.asc' libtasn1-6_4.20.0.orig.tar.gz.asc 1223 SHA256:0faa628b6a3e4bb84ca5f00f127c6dfa1fc96a7ad88030dd7aa048753cf4b201
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.debian.tar.xz' libtasn1-6_4.20.0-2.debian.tar.xz 18640 SHA256:d9d911708f4863437b88eeff7f779d39f6b77613dc2851c64db2bd8160a07c30
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.20.0-2/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.20.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.20.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtext-charwidth-perl=0.04-11`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11+b4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.dsc' libtext-charwidth-perl_0.04-11.dsc 2162 SHA256:8a4f6e7a44880f8b4dd8f3dc0c97a39c6fef979f99899de4962c9ccfe84a2577
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA256:2990c13c3f4a5479d7dbc5a94b86c23798cf0dc7df54ffe54e065f072558b6ed
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.debian.tar.xz' libtext-charwidth-perl_0.04-11.debian.tar.xz 3016 SHA256:2590d0b6ee7b9cea5396debb96190077210874b4847e844f9eb0d8a4d87ba19c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtext-charwidth-perl/0.04-11/ (for browsing the source)
- https://sources.debian.net/src/libtext-charwidth-perl/0.04-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtext-charwidth-perl/0.04-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtext-wrapi18n-perl=0.06-10`

Binary Packages:

- `libtext-wrapi18n-perl=0.06-10`

Licenses: (parsed from: `/usr/share/doc/libtext-wrapi18n-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-wrapi18n-perl=0.06-10
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA256:726c08c23af488c28b70600a5c1632468f1535cb50dcd5255cc153a4f8558ed9
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA256:432c2a801efe9f12d631124c1163439eac4c99449ba13d80133c45ecacc627f5
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA256:751073476ee62cc3430ff0afcab74a4e02b432199d7612e1fd63105fc89ec378
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtext-wrapi18n-perl/0.06-10/ (for browsing the source)
- https://sources.debian.net/src/libtext-wrapi18n-perl/0.06-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtext-wrapi18n-perl/0.06-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libthai=0.1.29-2`

Binary Packages:

- `libthai-data=0.1.29-2`
- `libthai-dev:amd64=0.1.29-2+b1`
- `libthai0:amd64=0.1.29-2+b1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai-dev/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29-2.dsc' libthai_0.1.29-2.dsc 2319 SHA256:564814dc31a466566cb50c077c5f6c5926a451594f52a0fc6b6367100445dddb
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA256:fc80cc7dcb50e11302b417cebd24f2d30a8b987292e77e003267b9100d0f4bcd
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29-2.debian.tar.xz' libthai_0.1.29-2.debian.tar.xz 12644 SHA256:18a66bc2e766f475c206492612eabe3a206642bb69866236eb4a0a4126bf4f41
```

Other potentially useful URLs:

- https://sources.debian.net/src/libthai/0.1.29-2/ (for browsing the source)
- https://sources.debian.net/src/libthai/0.1.29-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libthai/0.1.29-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtool=2.5.4-4`

Binary Packages:

- `libltdl-dev:amd64=2.5.4-4`
- `libltdl7:amd64=2.5.4-4`
- `libtool=2.5.4-4`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.5.4-4
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.5.4-4.dsc' libtool_2.5.4-4.dsc 2232 SHA256:37d98d7c45d1c12c0b7bd55fb6a90fa05aff8aa9ab2bbd9617ce7a6233b1965e
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.5.4.orig.tar.xz' libtool_2.5.4.orig.tar.xz 1069572 SHA256:d9189031edeaa6aa74695b2aeb80a8c26df50b29d8b72c991667e01adecea42c
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.5.4-4.debian.tar.xz' libtool_2.5.4-4.debian.tar.xz 37504 SHA256:93e8e286db1322a4f17e3120654ec2664a721e6684c017cb37d471daeb380f8e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtool/2.5.4-4/ (for browsing the source)
- https://sources.debian.net/src/libtool/2.5.4-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtool/2.5.4-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libunistring=1.3-2`

Binary Packages:

- `libunistring5:amd64=1.3-2`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `BSD-3-clause`
- `FreeSoftware`
- `GFDL-1.2+`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode-DFS-2016`
- `X11`
- `bsd-3-clause`
- `gfdl-1.2+`
- `gfdl-1.3+`
- `isc`
- `public-domain`
- `unicode-dfs-2016`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.3-2
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA256:0c09938cace7fbbf36c73af8bc2243fd2f70d3fe336539e8d4c10d0e61742571
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA256:f245786c831d25150f3dfb4317cda1acc5e3f79a5da4ad073ddca58886569527
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA256:62201b5b7ce9c0b033c50cefa5d7769dff4b7cee8205572e0cf917653cae9e33
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA256:feaf9761d365430178ea46feefeb602b435c21acf5924918e2257238e0378fc9
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/1.3-2/ (for browsing the source)
- https://sources.debian.net/src/libunistring/1.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/1.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwebp=1.5.0-0.1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.5.0-0.1`
- `libsharpyuv0:amd64=1.5.0-0.1`
- `libwebp-dev:amd64=1.5.0-0.1`
- `libwebp7:amd64=1.5.0-0.1`
- `libwebpdecoder3:amd64=1.5.0-0.1`
- `libwebpdemux2:amd64=1.5.0-0.1`
- `libwebpmux3:amd64=1.5.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.dsc' libwebp_1.5.0-0.1.dsc 2865 SHA256:2e7be6f202ebfaac738278bebc10b151768aef60857e63734018ced4d59b9c9a
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA256:7d6fab70cf844bf6769077bd5d7a74893f8ffd4dfb42861745750c63c2a5c92c
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA256:1383ff0b093f57d65f5a902e1bc51c550795ce4713b38712c60bb9151e15dcd6
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.debian.tar.xz' libwebp_1.5.0-0.1.debian.tar.xz 11284 SHA256:0dc0e727dc5f5e04ddd41b482f964626e92658099981b57ddd156b530ae01826
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwebp/1.5.0-0.1/ (for browsing the source)
- https://sources.debian.net/src/libwebp/1.5.0-0.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwebp/1.5.0-0.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwmf=0.2.13-1.1`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1+b3`
- `libwmf-dev=0.2.13-1.1+b3`
- `libwmflite-0.2-7:amd64=0.2.13-1.1+b3`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13-1.1.dsc' libwmf_0.2.13-1.1.dsc 2345 SHA256:05907248aae50ef26e44f518b628008b86cb8666513e568473fb62dfdee504af
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA256:18ba69febd2f515d98a2352de284a8051896062ac9728d2ead07bc39ea75a068
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13-1.1.debian.tar.xz' libwmf_0.2.13-1.1.debian.tar.xz 25784 SHA256:0032481fbf98810ca446ab8931392acd13bfee29d1df4000fb783b7126f8e0f4
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwmf/0.2.13-1.1/ (for browsing the source)
- https://sources.debian.net/src/libwmf/0.2.13-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwmf/0.2.13-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libx11=2:1.8.12-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1`
- `libx11-data=2:1.8.12-1`
- `libx11-dev:amd64=2:1.8.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.12-1.dsc' libx11_1.8.12-1.dsc 2490 SHA256:745fb04a4b0f8942183f6ac84ebd9e2dae1416c37f90abeaacabb57dc11286f5
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA256:220fbcf54b6e4d8dc40076ff4ab87954358019982490b33c7802190b62d89ce1
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA256:c3d177c8efcef9d3a1963956de0edc56ef2dd63d13dc39d3d7473dc9011fca65
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.12-1.diff.gz' libx11_1.8.12-1.diff.gz 74466 SHA256:2231b0ec8ce2eb380256b67eb30c05d90b0e92d75dd583c24e0bf640b3078977
```

Other potentially useful URLs:

- https://sources.debian.net/src/libx11/2:1.8.12-1/ (for browsing the source)
- https://sources.debian.net/src/libx11/2:1.8.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libx11/2:1.8.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxau=1:1.0.11-1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.11-1`
- `libxau6:amd64=1:1.0.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.11-1.dsc' libxau_1.0.11-1.dsc 2213 SHA256:6058ab58b243ae2b175eee067b868f37b74cd4e8cc40b90607ce6d9ee99c50f9
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA256:3a321aaceb803577a4776a5efe78836eb095a9e44bbc7a465d29463e1a14f189
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA256:72320a0c036cc2d36bebdd7d279c402620e2f3553f639581dfb23736803ce258
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.11-1.diff.gz' libxau_1.0.11-1.diff.gz 22671 SHA256:0af3f94102f73c585c48a6b17f54c92e154f6b560a061871d437bd720edd5314
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxau/1:1.0.11-1/ (for browsing the source)
- https://sources.debian.net/src/libxau/1:1.0.11-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxau/1:1.0.11-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2+b1`
- `libxcb-render0-dev:amd64=1.17.0-2+b1`
- `libxcb-shm0:amd64=1.17.0-2+b1`
- `libxcb-shm0-dev:amd64=1.17.0-2+b1`
- `libxcb1:amd64=1.17.0-2+b1`
- `libxcb1-dev:amd64=1.17.0-2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA256:b2728d156f79d2e757e7378cfcefca52bd570739d2efffa87e1aaeaf4f21de3a
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA256:2c69287424c9e2128cb47ffe92171e10417041ec2963bceafb65cb3fcf8f0b85
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA256:c5b33b67a61d0d1c1b624bf88a8150f4be1ba9b46e855e38f03a8f73858af558
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcb/1.17.0-2/ (for browsing the source)
- https://sources.debian.net/src/libxcb/1.17.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcb/1.17.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.38-1`
- `libcrypt1:amd64=1:4.4.38-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.38-1
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.dsc' libxcrypt_4.4.38-1.dsc 1573 SHA256:feba1874a84616791c1c17f9a290c9e97562b2904b3b0200edc82a2db54f3f07
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA256:6a275a356622c64ba9f693892215dbb399c003a7a4afeed9c4c74070eaab20f4
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.debian.tar.xz' libxcrypt_4.4.38-1.debian.tar.xz 8512 SHA256:6b87bcb5325e417ab3f4c01c364233444b4c9008a69ec1d6fababb3f6e693a5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.4.38-1/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.4.38-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.4.38-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxdmcp=1:1.1.5-1`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.5-1`
- `libxdmcp6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-1
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.dsc' libxdmcp_1.1.5-1.dsc 2331 SHA256:d4a124405528eba3cf8794cc4fb8c4339ad74e79dd916fc0565b3a30c9fc1fe3
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA256:31a7abc4f129dcf6f27ae912c3eedcb94d25ad2e8f317f69df6eda0bc4e4f2f3
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA256:0c7666da02d66ab785584cd16a6f9324f0d949555734e70b3b1385e525c7860b
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.diff.gz' libxdmcp_1.1.5-1.diff.gz 9764 SHA256:7ec2e7da28c38723aa115ce2bd18389f7d73e716b0f50bec9e6e0d1b24f19954
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxdmcp/1:1.1.5-1/ (for browsing the source)
- https://sources.debian.net/src/libxdmcp/1:1.1.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxdmcp/1:1.1.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1+b3`
- `libxext6:amd64=2:1.3.4-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4-1.dsc' libxext_1.3.4-1.dsc 2118 SHA256:25024f57d955739c6b858822bf93ec3c71400b56fc0d666826f440e3661fd7c0
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4-1.diff.gz' libxext_1.3.4-1.diff.gz 12509 SHA256:b975870d6a7b791ffbe2d57efdf6e20c250c5e76d12e45b04c8655f593bb8337
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxext/2:1.3.4-1/ (for browsing the source)
- https://sources.debian.net/src/libxext/2:1.3.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxext/2:1.3.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxml2=2.12.7+dfsg+really2.9.14-0.4`

Binary Packages:

- `libxml2:amd64=2.12.7+dfsg+really2.9.14-0.4`
- `libxml2-dev:amd64=2.12.7+dfsg+really2.9.14-0.4`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.12.7+dfsg+really2.9.14-0.4
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg%2breally2.9.14-0.4.dsc' libxml2_2.12.7+dfsg+really2.9.14-0.4.dsc 3060 SHA256:ed52ed86b0dbc448c79490829aa8f6b73abf37794e3be27d746a8aa1c90a94e0
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg%2breally2.9.14.orig.tar.xz' libxml2_2.12.7+dfsg+really2.9.14.orig.tar.xz 2351200 SHA256:4fe913dec8b1ab89d13b489b419a8203176ea39e931eaa0d25b17eafb9c279e9
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg%2breally2.9.14-0.4.debian.tar.xz' libxml2_2.12.7+dfsg+really2.9.14-0.4.debian.tar.xz 38312 SHA256:02dd4c440b5b8bd9376030b5e224a0da707d60e649eec28787b35ebdeebb4f0d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxml2/2.12.7+dfsg+really2.9.14-0.4/ (for browsing the source)
- https://sources.debian.net/src/libxml2/2.12.7+dfsg+really2.9.14-0.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxml2/2.12.7+dfsg+really2.9.14-0.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxrender=1:0.9.12-1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.12-1`
- `libxrender1:amd64=1:0.9.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.dsc' libxrender_0.9.12-1.dsc 2258 SHA256:2980c127d296455f4e9bcaf5ba114284fa0735ce3ef5b613dbe99d854bc87ca3
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA256:0fff64125819c02d1102b6236f3d7d861a07b5216d8eea336c3811d31494ecf7
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA256:0bbd310ac3974ef398cf4d8a4b362b0b4d60ceb43e6eba393c3cc740b03816fc
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.diff.gz' libxrender_0.9.12-1.diff.gz 21464 SHA256:c0d3e91a3aa474772c242dcbb997504dff4c28e177d9b7fbb70c50ce7bf56fc5
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxrender/1:0.9.12-1/ (for browsing the source)
- https://sources.debian.net/src/libxrender/1:0.9.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxrender/1:0.9.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxslt=1.1.35-1.2`

Binary Packages:

- `libxslt1-dev:amd64=1.1.35-1.2`
- `libxslt1.1:amd64=1.1.35-1.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.35-1.2
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35-1.2.dsc' libxslt_1.1.35-1.2.dsc 2319 SHA256:f65d6360b13fa59fd2f283296ae83e86640d5270cf59cbbe7de17761520577a9
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35.orig.tar.xz' libxslt_1.1.35.orig.tar.xz 1827548 SHA256:8247f33e9a872c6ac859aa45018bc4c4d00b97e2feac9eebc10c93ce1f34dd79
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35-1.2.debian.tar.xz' libxslt_1.1.35-1.2.debian.tar.xz 23644 SHA256:6f56561d6f8d129ca6c72ada897f59684a8ea1a8acaa6835c8152e44b8151000
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxslt/1.1.35-1.2/ (for browsing the source)
- https://sources.debian.net/src/libxslt/1.1.35-1.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxslt/1.1.35-1.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxt=1:1.2.1-1.2`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2+b2`
- `libxt6t64:amd64=1:1.2.1-1.2+b2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.dsc' libxt_1.2.1-1.2.dsc 2373 SHA256:780be4cf9b0b90757758691dc8196d85322b30a599c36fb8fe368b7060c7b774
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA256:6da1bfa9dd0ed87430a5ce95b129485086394df308998ebe34d98e378e3dfb33
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA256:da406cc94c25ca6773bb37c2055e2eb5665491f7ca6dfc9ea04f0f30ea3fd098
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.diff.gz' libxt_1.2.1-1.2.diff.gz 45635 SHA256:d4c510871909584398d88552b69cc5e92e124098ce544be93ef1743d0d112d4c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxt/1:1.2.1-1.2/ (for browsing the source)
- https://sources.debian.net/src/libxt/1:1.2.1-1.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxt/1:1.2.1-1.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libyaml=0.2.5-2`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-2`
- `libyaml-dev:amd64=0.2.5-2`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-2
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5-2.dsc' libyaml_0.2.5-2.dsc 2040 SHA256:c1c3dab54fe7b355753f46a8c783b74a0a6e1099fb3878f4963a175691351477
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA256:fa240dbf262be053f3898006d502d514936c818e422afdcf33921c63bed9bf2e
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5-2.debian.tar.xz' libyaml_0.2.5-2.debian.tar.xz 5656 SHA256:3bdf4ab4a530c66358e44129e0f96183a13fcfef4355a41df296b1c5e0cf63d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/libyaml/0.2.5-2/ (for browsing the source)
- https://sources.debian.net/src/libyaml/0.2.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libyaml/0.2.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.7+dfsg-1`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-1`
- `libzstd1:amd64=1.5.7+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-1
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1.dsc' libzstd_1.5.7+dfsg-1.dsc 2371 SHA256:8f6ab97fa772d921334e50fa5756a0951e23c718dc913e43a228f28c1a23adf9
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA256:0c092ef267edce57ba7f3f2645c861f72eaf5e76273c6c3632869423464b90a5
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1.debian.tar.xz' libzstd_1.5.7+dfsg-1.debian.tar.xz 23036 SHA256:5e88424d919941291f79e1bfada6cb1a6f748671d9de7d4b7d931f361f183a15
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.7+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.7+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.7+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `linux=6.12.21-1`

Binary Packages:

- `linux-libc-dev=6.12.21-1`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+-or-X11`
- `LGPL-2.1`
- `Unicode-data`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=6.12.21-1
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.12.21-1.dsc' linux_6.12.21-1.dsc 206735 SHA256:77cef4ffe00d0cfb1ca3a81fc6daeb5a0882821e01520be687329d408f654a62
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.12.21.orig.tar.xz' linux_6.12.21.orig.tar.xz 150978192 SHA256:9b6763b159f136deb7aa8b739075e416fdaac73a559df1e4f7c0bd346f5cb30f
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.12.21-1.debian.tar.xz' linux_6.12.21-1.debian.tar.xz 1607564 SHA256:9b7d07830c0fae71c71696d696dcf19ee159c02e282032df36113ab2ee339086
```

Other potentially useful URLs:

- https://sources.debian.net/src/linux/6.12.21-1/ (for browsing the source)
- https://sources.debian.net/src/linux/6.12.21-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/linux/6.12.21-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.10.0-4`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-4
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-4.dsc' lz4_1.10.0-4.dsc 1941 SHA256:394c635aa75a21cd5896680e48821c05336645072ae866b2717d53f36b9ba851
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-4.debian.tar.xz' lz4_1.10.0-4.debian.tar.xz 8080 SHA256:8d276c3254182c2c9cf319b9a6504cf257c56b441f37d3db8ad97d33d46a0911
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.10.0-4/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.10.0-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.10.0-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lzo2=2.10-3`

Binary Packages:

- `liblzo2-2:amd64=2.10-3+b1`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-3
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10-3.dsc' lzo2_2.10-3.dsc 1923 SHA256:d3efa3ce5107bafda50ca2769e4ad896a34f7ed0b70600c1d986d6937898786c
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA256:c0f892943208266f9b6543b3ae308fab6284c5c90e627931446fb49b4221a072
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10-3.debian.tar.xz' lzo2_2.10-3.debian.tar.xz 7228 SHA256:cf18b57e9a0a5c5f816facd5905e5c8dce0f99d2598b8416dab46b0064ba2cd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/lzo2/2.10-3/ (for browsing the source)
- https://sources.debian.net/src/lzo2/2.10-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lzo2/2.10-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `m4=1.4.19-7`

Binary Packages:

- `m4=1.4.19-7`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-7
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19-7.dsc' m4_1.4.19-7.dsc 1755 SHA256:c23e935c0aec078d12d34e29982307c903ced3baa03ea236486d72aabd124ba7
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA256:63aede5c6d33b6d9b13511cd0be2cac046f2e70fd0a07aa9573a04a82783af96
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA256:9700ba4dca539b06e033b4e3ab37fa5b983becb6c14569a8b8aa02dee6ab666c
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19-7.debian.tar.xz' m4_1.4.19-7.debian.tar.xz 18024 SHA256:3c4a5fc77db322c370523d2a68e7f9f6e3c00916bd57e5536399de295b83441b
```

Other potentially useful URLs:

- https://sources.debian.net/src/m4/1.4.19-7/ (for browsing the source)
- https://sources.debian.net/src/m4/1.4.19-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/m4/1.4.19-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `make-dfsg=4.4.1-1`

Binary Packages:

- `make=4.4.1-1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/make-dfsg/4.4.1-1/


### `dpkg` source package: `mariadb=1:11.8.1-2`

Binary Packages:

- `libmariadb-dev=1:11.8.1-2`
- `libmariadb-dev-compat=1:11.8.1-2`
- `libmariadb3:amd64=1:11.8.1-2`
- `mariadb-common=1:11.8.1-2`

Licenses: (parsed from: `/usr/share/doc/libmariadb-dev/copyright`, `/usr/share/doc/libmariadb-dev-compat/copyright`, `/usr/share/doc/libmariadb3/copyright`, `/usr/share/doc/mariadb-common/copyright`)

- `Artistic`
- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-bison-exception`
- `GPL-3+-with-bison-exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `SWsoft`
- `public-domain`
- `unlimited-free-doc`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mariadb=1:11.8.1-2
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.8.1-2.dsc' mariadb_11.8.1-2.dsc 5621 SHA256:78a24139e56cf69236a6cb596eb847f4a3ec44392ae85bc2c8f4239c0c3a927f
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.8.1.orig.tar.gz' mariadb_11.8.1.orig.tar.gz 112837824 SHA256:c58e9e96e8e69dba09aa179b9bea63fc2775f3194efb72dfc2c277abfb9936e5
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.8.1.orig.tar.gz.asc' mariadb_11.8.1.orig.tar.gz.asc 833 SHA256:c6a7daa2a40f47997b18515b7e2855a8f1fca603ac91a8a08c97aa47dad10b53
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.8.1-2.debian.tar.xz' mariadb_11.8.1-2.debian.tar.xz 288292 SHA256:0e1ec62635ef9c9ba8f93c8f8e02bab7ef3473ebef94e53ff12a4869cdf3d122
```

Other potentially useful URLs:

- https://sources.debian.net/src/mariadb/1:11.8.1-2/ (for browsing the source)
- https://sources.debian.net/src/mariadb/1:11.8.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mariadb/1:11.8.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.4.20250131-1`

Binary Packages:

- `mawk=1.3.4.20250131-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20250131-1
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131-1.dsc' mawk_1.3.4.20250131-1.dsc 2969 SHA256:147dd01670e2ebf61f3c78470e0025b87d14e69c7ba9cfafd54da32a355dea84
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA256:51bcb82d577b141d896d9d9c3077d7aaa209490132e9f2b9573ba8511b3835be
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA256:bc83f127727edb42a91d516770c8d0d3cdb5f6e541aa3cb5213b79dae494db95
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20250131-1.debian.tar.xz' mawk_1.3.4.20250131-1.debian.tar.xz 16008 SHA256:23dea8244bf4f116ec3cd202ab5d4693207d82d986cd0a3d79442b916be4e2b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20250131-1/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20250131-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20250131-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `media-types=13.0.0`

Binary Packages:

- `media-types=13.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=13.0.0
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_13.0.0.dsc' media-types_13.0.0.dsc 1647 SHA256:a664c287e8d358da16bae998374c546cf0eaf3e0416f7059a56818eefe018546
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_13.0.0.tar.xz' media-types_13.0.0.tar.xz 62960 SHA256:bcd40584a3e092fd33e45f324e10652a400fea3b0e206d286d1c2d6414d763e7
```

Other potentially useful URLs:

- https://sources.debian.net/src/media-types/13.0.0/ (for browsing the source)
- https://sources.debian.net/src/media-types/13.0.0/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/media-types/13.0.0/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mercurial=6.9.5-1`

Binary Packages:

- `mercurial=6.9.5-1`
- `mercurial-common=6.9.5-1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.9.5-1
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.9.5-1.dsc' mercurial_6.9.5-1.dsc 2826 SHA256:d3a54b3db58b6f87625332f2c8dca6c19c01417083852ebf87ca635b5ef11c60
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.9.5.orig.tar.gz' mercurial_6.9.5.orig.tar.gz 8922574 SHA256:d3f22aeef9e9dcd6e562132950226c2c955d35271bd00a01481efca2b1cc65fd
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.9.5.orig.tar.gz.asc' mercurial_6.9.5.orig.tar.gz.asc 659 SHA256:6dced9fffab5df4ba2c7d27150a8b45659ef87816ff0bd4b881d9d983eac493c
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.9.5-1.debian.tar.xz' mercurial_6.9.5-1.debian.tar.xz 55596 SHA256:7868f7a171f6ebb1ec1a70bd5a96e547525e665277ff498852e352517dc01363
```

Other potentially useful URLs:

- https://sources.debian.net/src/mercurial/6.9.5-1/ (for browsing the source)
- https://sources.debian.net/src/mercurial/6.9.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mercurial/6.9.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpclib3=1.3.1-1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1+b3`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.dsc' mpclib3_1.3.1-1.dsc 1877 SHA256:b2252a499fd0f8e92ce2cf7d8e68477ffc9dd06127803a91f0a1115822efec75
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.debian.tar.xz' mpclib3_1.3.1-1.debian.tar.xz 4656 SHA256:25adb496258adacad69c022d712f96fbc465bcef9fd4751829dc351d9ce6a45d
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpclib3/1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/mpclib3/1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpclib3/1.3.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpfr4=4.2.2-1`

Binary Packages:

- `libmpfr6:amd64=4.2.2-1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.2-1
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.2-1.dsc' mpfr4_4.2.2-1.dsc 1960 SHA256:08ee7b45f8a9980570508770a9d48f70d4c1962fd7c98af4a78cbc3747002ecd
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA256:b67ba0383ef7e8a8563734e2e889ef5ec3c3b898a01d00fa0a6869ad81c6ce01
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.2-1.debian.tar.xz' mpfr4_4.2.2-1.debian.tar.xz 12564 SHA256:3e203524cdc516a99ec8a676dd9d21435b5f020e624149d39f4c530393d5a563
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpfr4/4.2.2-1/ (for browsing the source)
- https://sources.debian.net/src/mpfr4/4.2.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpfr4/4.2.2-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.dsc' mysql-defaults_1.1.1.dsc 2202 SHA256:4fd91907a56a2251e2e0dc0faa37c52299a2ae8d68e457cd250ac29d160090f1
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.tar.xz' mysql-defaults_1.1.1.tar.xz 7460 SHA256:054d8da3bfd3419081a7ccb795ad614c235e8aa06674c5588cb88973467c1cdc
```

Other potentially useful URLs:

- https://sources.debian.net/src/mysql-defaults/1.1.1/ (for browsing the source)
- https://sources.debian.net/src/mysql-defaults/1.1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mysql-defaults/1.1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.5+20250216-2`

Binary Packages:

- `libncurses-dev:amd64=6.5+20250216-2`
- `libncurses6:amd64=6.5+20250216-2`
- `libncursesw6:amd64=6.5+20250216-2`
- `libtinfo6:amd64=6.5+20250216-2`
- `ncurses-base=6.5+20250216-2`
- `ncurses-bin=6.5+20250216-2`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-2
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.dsc' ncurses_6.5+20250216-2.dsc 3890 SHA256:00539cc2bc6bb84be1b8a8a5decf606682e14b6f39b76b9aa090e65d2c2d4580
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA256:b37baafa436e7133bb12a185cb8f60e1599b1947e9f0181c76f3190acf28b6eb
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA256:64f4d17923322176c44079f18f170e2164a59d551d7e4e9c1a6e4eebedc5dd6f
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.debian.tar.xz' ncurses_6.5+20250216-2.debian.tar.xz 50420 SHA256:546930a8992ae3325d8c38378f290265d969cf6333cfae9648ac6d69e1e8a8a6
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.5+20250216-2/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.5+20250216-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.5+20250216-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `netbase=6.5`

Binary Packages:

- `netbase=6.5`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.5.dsc' netbase_6.5.dsc 899 SHA256:e8691899f57c06fcc383b0f2214b662137df539227d9d7811dc8223f32ebe4c7
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.5.tar.xz' netbase_6.5.tar.xz 32544 SHA256:9116047aebbaa1698934052d01c6e09b4c3aed643e93df63d2ddcbec243c26d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/6.5/ (for browsing the source)
- https://sources.debian.net/src/netbase/6.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/6.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.10.1-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.1-1`
- `libnettle8t64:amd64=3.10.1-1`
- `nettle-dev:amd64=3.10.1-1`

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
$ apt-get source -qq --print-uris nettle=3.10.1-1
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.1-1.dsc' nettle_3.10.1-1.dsc 2053 SHA256:7b440850ce04b341363f3f5e23dfb9f96ebf7d52e0ef7ba2d07120c90ca61b3c
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.1.orig.tar.gz' nettle_3.10.1.orig.tar.gz 2643267 SHA256:b0fcdd7fc0cdea6e80dcf1dd85ba794af0d5b4a57e26397eee3bc193272d9132
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.1-1.debian.tar.xz' nettle_3.10.1-1.debian.tar.xz 25036 SHA256:2d40d02ddac5985d8833532a17a0ef96cb685ee0547ee9617ec13793b22e34c6
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.10.1-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.10.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.10.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp2=1.64.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1`
- `libnghttp2-dev:amd64=1.64.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.dsc' nghttp2_1.64.0-1.dsc 2531 SHA256:2707e30147f7f5c5562245f1760876476798cf0cac10a9784f8e66a4d14d42a3
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA256:b452dc69a1fcbc9375389b8b154175d8b7b125cdd713fc426774c2b79a1ebd77
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.debian.tar.xz' nghttp2_1.64.0-1.debian.tar.xz 38888 SHA256:3085083399b3f02bfc00e9b4f9c286ddd33c9624b622713a55ebbd8c398625eb
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp2/1.64.0-1/ (for browsing the source)
- https://sources.debian.net/src/nghttp2/1.64.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp2/1.64.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp3=1.8.0-1`

Binary Packages:

- `libnghttp3-9:amd64=1.8.0-1`
- `libnghttp3-dev:amd64=1.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp3-9/copyright`, `/usr/share/doc/libnghttp3-dev/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris nghttp3=1.8.0-1
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.8.0-1.dsc' nghttp3_1.8.0-1.dsc 1603 SHA256:ffc623e78be62361a82f0a2e7b9a19ff0bcdfc371b8bcc1842039499a12adba2
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.8.0.orig.tar.xz' nghttp3_1.8.0.orig.tar.xz 398640 SHA256:a9dd28970977e6802a3eaf2cfaeae6d0fae60c8d2c0f2c4ce600036a7998ee9a
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.8.0.orig.tar.xz.asc' nghttp3_1.8.0.orig.tar.xz.asc 833 SHA256:c2549dd50a5ad392610d108244357c1cc750fd5bf4a5ef91de1d94d11c49b0cf
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.8.0-1.debian.tar.xz' nghttp3_1.8.0-1.debian.tar.xz 8228 SHA256:fc0cfa954de5b8fef85bd13e1edcbfccb463ce211905e925921b608390c840c9
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp3/1.8.0-1/ (for browsing the source)
- https://sources.debian.net/src/nghttp3/1.8.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp3/1.8.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ngtcp2=1.11.0-1`

Binary Packages:

- `libngtcp2-16:amd64=1.11.0-1`
- `libngtcp2-crypto-gnutls8:amd64=1.11.0-1`

Licenses: (parsed from: `/usr/share/doc/libngtcp2-16/copyright`, `/usr/share/doc/libngtcp2-crypto-gnutls8/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ngtcp2=1.11.0-1
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.11.0-1.dsc' ngtcp2_1.11.0-1.dsc 1969 SHA256:ebb120f6d08f61f8a5d0878fd37f7d00ffcc09977ee75469a6f1992c34d934f8
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.11.0.orig.tar.xz' ngtcp2_1.11.0.orig.tar.xz 652904 SHA256:382c15bf66b630f26021631b25b7eb1feac42c67c1d6826189d61091dfaa4d09
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.11.0.orig.tar.xz.asc' ngtcp2_1.11.0.orig.tar.xz.asc 833 SHA256:56193493ac1e2a05dbf48d7b4480a2590d7fbdb2439475fd7c5087bc31cb988d
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.11.0-1.debian.tar.xz' ngtcp2_1.11.0-1.debian.tar.xz 9764 SHA256:e054092ac4f0f3138950f8d99aeb1961d3fa6f71dcd0bc983a3dae35170ac10c
```

Other potentially useful URLs:

- https://sources.debian.net/src/ngtcp2/1.11.0-1/ (for browsing the source)
- https://sources.debian.net/src/ngtcp2/1.11.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ngtcp2/1.11.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `npth=1.8-2`

Binary Packages:

- `libnpth0t64:amd64=1.8-2`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-2
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8-2.dsc' npth_1.8-2.dsc 2188 SHA256:97a6cf299da7e9eaed481cda941d3e8a6ef3cc987491c322172401a33244d356
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA256:8bd24b4f23a3065d6e5b26e98aba9ce783ea4fd781069c1b35d149694e90ca3e
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA256:1a2bd2f85ad832d5166e616cbf336b072c6bdc20335146c5adccd3e2795a24bc
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8-2.debian.tar.xz' npth_1.8-2.debian.tar.xz 8908 SHA256:53f3df114ec3dcba66f0fa7ea8f24fe2caf8fadb5ba51e2935eeb36d38083c13
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.8-2/ (for browsing the source)
- https://sources.debian.net/src/npth/1.8-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.8-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openexr=3.1.13-2`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.13-2`
- `libopenexr-dev=3.1.13-2`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.13-2
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.13-2.dsc' openexr_3.1.13-2.dsc 2144 SHA256:a44f8572a8018ce8b51a35fd2e8a90492b2358b434b8e2beba66f4dd6dd944f8
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.13.orig.tar.gz' openexr_3.1.13.orig.tar.gz 20542408 SHA256:26d265d8cf8df4dad115b066ba209118ca8832cda076ec704ce1a57f827c75c6
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.13-2.debian.tar.xz' openexr_3.1.13-2.debian.tar.xz 19268 SHA256:5e0e5768b1577dd604bb410666d3420566ac1f8858e69a234633259c3efb52a3
```

Other potentially useful URLs:

- https://sources.debian.net/src/openexr/3.1.13-2/ (for browsing the source)
- https://sources.debian.net/src/openexr/3.1.13-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openexr/3.1.13-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openjpeg2=2.5.3-2`

Binary Packages:

- `libopenjp2-7:amd64=2.5.3-2`
- `libopenjp2-7-dev:amd64=2.5.3-2`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.3-2
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.dsc' openjpeg2_2.5.3-2.dsc 2414 SHA256:f9f15d8400a1ab69381e408ad7ec23c38121efd3a3f50fad5baf514d7df25f9f
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.3.orig.tar.xz' openjpeg2_2.5.3.orig.tar.xz 1393716 SHA256:3100f0316e922630112cf6d72c0c20776896e64ad7eab72c2f713c460287eb92
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.debian.tar.xz' openjpeg2_2.5.3-2.debian.tar.xz 14992 SHA256:a1300a5efb9e91f49449b571a3cca04d221f7df5024674cb50c77ca82ec5c65e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openjpeg2/2.5.3-2/ (for browsing the source)
- https://sources.debian.net/src/openjpeg2/2.5.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openjpeg2/2.5.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openldap=2.6.9+dfsg-2`

Binary Packages:

- `libldap-dev:amd64=2.6.9+dfsg-2`
- `libldap2:amd64=2.6.9+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libldap-dev/copyright`, `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.9+dfsg-2
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2.dsc' openldap_2.6.9+dfsg-2.dsc 3278 SHA256:10633be67f8b00746b184bad568c79c1974c26a076136657ca65e70de5d4f73d
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg.orig.tar.xz' openldap_2.6.9+dfsg.orig.tar.xz 3753260 SHA256:dfce3ca171b4036b371455314dd35176b700ee988d3b556f156f37088516ef93
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2.debian.tar.xz' openldap_2.6.9+dfsg-2.debian.tar.xz 170064 SHA256:c1a8d955f17f6d04497636ab17a1b94b149ffaa14e9617276df22d2de449f2d0
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.6.9+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.6.9+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.6.9+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssh=1:9.9p2-2`

Binary Packages:

- `openssh-client=1:9.9p2-2`

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
$ apt-get source -qq --print-uris openssh=1:9.9p2-2
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_9.9p2-2.dsc' openssh_9.9p2-2.dsc 3466 SHA256:07c25a5189faa05dbacede72c48d017616f94223799a21618a781341e41cf1fb
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_9.9p2.orig.tar.gz' openssh_9.9p2.orig.tar.gz 1944499 SHA256:91aadb603e08cc285eddf965e1199d02585fa94d994d6cae5b41e1721e215673
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_9.9p2.orig.tar.gz.asc' openssh_9.9p2.orig.tar.gz.asc 833 SHA256:17daea197718ef7907db917983547dbece321ac8beb1f2c215b45a93c485f5c2
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_9.9p2-2.debian.tar.xz' openssh_9.9p2-2.debian.tar.xz 196324 SHA256:b39f0d09d9b1fbddcc4f8326a3f913de0b71d5f10973c06d7750ce1970aa5d8e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssh/1:9.9p2-2/ (for browsing the source)
- https://sources.debian.net/src/openssh/1:9.9p2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssh/1:9.9p2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.4.1-1`

Binary Packages:

- `libssl-dev:amd64=3.4.1-1`
- `libssl3t64:amd64=3.4.1-1`
- `openssl=3.4.1-1`
- `openssl-provider-legacy=3.4.1-1`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.4.1-1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.4.1-1.dsc' openssl_3.4.1-1.dsc 2808 SHA256:850f658197e44d13882b13929b04008c18e2f643ca2781eda180b5f288cb5699
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz' openssl_3.4.1.orig.tar.gz 18346056 SHA256:002a2d6b30b58bf4bea46c43bdd96365aaf8daa6c428782aa4feee06da197df3
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz.asc' openssl_3.4.1.orig.tar.gz.asc 833 SHA256:488c2d4051d5d27b1c0f9d21fd717630e0a2e1b82216875b2fb0fceeb0e8ea5a
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.4.1-1.debian.tar.xz' openssl_3.4.1-1.debian.tar.xz 50548 SHA256:ffd963c2e742809bedb03a9416e64426c585ec987fd6e3b5c3a1eed4d9fc882d
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.4.1-1/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.4.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.4.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.25.5-3`

Binary Packages:

- `libp11-kit-dev:amd64=0.25.5-3`
- `libp11-kit0:amd64=0.25.5-3`

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
$ apt-get source -qq --print-uris p11-kit=0.25.5-3
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-3.dsc' p11-kit_0.25.5-3.dsc 2538 SHA256:65e21a68dd942741bba82f5bf20901f616b64de91a976d92a54a0cb314896544
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA256:04d0a86450cdb1be018f26af6699857171a188ac6d5b8c90786a60854e1198e5
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz.asc' p11-kit_0.25.5.orig.tar.xz.asc 228 SHA256:066c92b9d2accb2fda6a2f71e676fb6526fcc153051b1f04ee7d7c8c96a09989
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-3.debian.tar.xz' p11-kit_0.25.5-3.debian.tar.xz 24184 SHA256:3800ea81e4615898813f533834ad37ec270f6f7d4c9413c84e712075a197849c
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.25.5-3/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.25.5-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.25.5-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.7.0-3`

Binary Packages:

- `libpam-modules:amd64=1.7.0-3`
- `libpam-modules-bin=1.7.0-3`
- `libpam-runtime=1.7.0-3`
- `libpam0g:amd64=1.7.0-3`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-3
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-3.dsc' pam_1.7.0-3.dsc 2210 SHA256:55350f07d07d565e1323282b2ceda48559c335c27ec7199d99c4e803006349d0
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-3.debian.tar.xz' pam_1.7.0-3.debian.tar.xz 132064 SHA256:ff446441cd74a3440b2bd32098d8865e959e497fde167b92ba776d1f354a0946
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.7.0-3/ (for browsing the source)
- https://sources.debian.net/src/pam/1.7.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.7.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pango1.0=1.56.3-1`

Binary Packages:

- `gir1.2-pango-1.0:amd64=1.56.3-1`
- `libpango-1.0-0:amd64=1.56.3-1`
- `libpango1.0-dev:amd64=1.56.3-1`
- `libpangocairo-1.0-0:amd64=1.56.3-1`
- `libpangoft2-1.0-0:amd64=1.56.3-1`
- `libpangoxft-1.0-0:amd64=1.56.3-1`
- `pango1.0-tools=1.56.3-1`

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
$ apt-get source -qq --print-uris pango1.0=1.56.3-1
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.56.3-1.dsc' pango1.0_1.56.3-1.dsc 3690 SHA256:173af22e6447fd24322d8ffbed4bbafd090b88ea463c416701b9aa37cae75266
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.56.3.orig.tar.xz' pango1.0_1.56.3.orig.tar.xz 1883584 SHA256:2606252bc25cd8d24e1b7f7e92c3a272b37acd6734347b73b47a482834ba2491
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.56.3-1.debian.tar.xz' pango1.0_1.56.3-1.debian.tar.xz 43788 SHA256:00576a0cd3fd4ded5edcd5b5e1c710ee8034b00b49907b2d9c3e38906151f816
```

Other potentially useful URLs:

- https://sources.debian.net/src/pango1.0/1.56.3-1/ (for browsing the source)
- https://sources.debian.net/src/pango1.0/1.56.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pango1.0/1.56.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `patch=2.7.6-7`

Binary Packages:

- `patch=2.7.6-7`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6-7.dsc' patch_2.7.6-7.dsc 1706 SHA256:d954fd576d935ac54b7d44d4976eb52d0da84a57f7bad90c6e5bd5e33595030a
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA256:ac610bda97abe0d9f6b7c963255a11dcb196c25e337c61f94e4778d632f1d8fd
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6-7.debian.tar.xz' patch_2.7.6-7.debian.tar.xz 15084 SHA256:7725f30b042d8cf63516e480036e93ca2ff0ce5ad3754db4a4e69d33e96a2624
```

Other potentially useful URLs:

- https://sources.debian.net/src/patch/2.7.6-7/ (for browsing the source)
- https://sources.debian.net/src/patch/2.7.6-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/patch/2.7.6-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre2=10.45-1`

Binary Packages:

- `libpcre2-16-0:amd64=10.45-1`
- `libpcre2-32-0:amd64=10.45-1`
- `libpcre2-8-0:amd64=10.45-1`
- `libpcre2-dev:amd64=10.45-1`
- `libpcre2-posix3:amd64=10.45-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.45-1
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.45-1.dsc' pcre2_10.45-1.dsc 2337 SHA256:9b9d6aa2c970a416cb6808ac894d18fe37dd6df0497e2d75c13bb86429fa7b35
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.45.orig.tar.gz' pcre2_10.45.orig.tar.gz 2715958 SHA256:0e138387df7835d7403b8351e2226c1377da804e0737db0e071b48f07c9d12ee
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.45-1.diff.gz' pcre2_10.45-1.diff.gz 8659 SHA256:02ef5e4fbdf274f344c7be0efb3d1bdff538bd621e6988cc0a3d2c43da40b351
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.45-1/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.45-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.45-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.40.1-2`

Binary Packages:

- `libperl5.40:amd64=5.40.1-2`
- `perl=5.40.1-2`
- `perl-base=5.40.1-2`
- `perl-modules-5.40=5.40.1-2`

Licenses: (parsed from: `/usr/share/doc/libperl5.40/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.40/copyright`)

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
$ apt-get source -qq --print-uris perl=5.40.1-2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-2.dsc' perl_5.40.1-2.dsc 2372 SHA256:a6a3011bb0422d31b6ae42b755ba3c2667e9de2a3d84559fcb70f8db354fe115
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-2.debian.tar.xz' perl_5.40.1-2.debian.tar.xz 167424 SHA256:fb98273ae62b5750534640cbfeb018c668538dd69d72c1bedec9f5a8a4999044
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.40.1-2/ (for browsing the source)
- https://sources.debian.net/src/perl/5.40.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.40.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pinentry=1.3.1-2`

Binary Packages:

- `pinentry-curses=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.1-2
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.1-2.dsc' pinentry_1.3.1-2.dsc 3206 SHA256:368802b3766c8bc619f1902b72dd2dddf3b745a92fed18a051560a211e4856a1
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2' pinentry_1.3.1.orig.tar.bz2 611233 SHA256:bc72ee27c7239007ab1896c3c2fae53b076e2c9bd2483dc2769a16902bce8c04
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2.asc' pinentry_1.3.1.orig.tar.bz2.asc 390 SHA256:bc51c827206fb48de8003bd09dec6be7e28193f772459a505b7d7483669b4b9b
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.1-2.debian.tar.xz' pinentry_1.3.1-2.debian.tar.xz 21032 SHA256:7b6174d6469bb15555cbcee453ad7a61e4c2532b2d7ed1ad47b36fe61e6ff1a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/pinentry/1.3.1-2/ (for browsing the source)
- https://sources.debian.net/src/pinentry/1.3.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pinentry/1.3.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pixman=0.44.0-3`

Binary Packages:

- `libpixman-1-0:amd64=0.44.0-3`
- `libpixman-1-dev:amd64=0.44.0-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.44.0-3
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.44.0-3.dsc' pixman_0.44.0-3.dsc 2019 SHA256:b05388a6cb71550a2ed425e9689b09b1dc458fa06d842f87328ede5e0eb7345f
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.44.0.orig.tar.gz' pixman_0.44.0.orig.tar.gz 812995 SHA256:89a4c1e1e45e0b23dffe708202cb2eaffde0fe3727d7692b2e1739fec78a7dac
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.44.0-3.diff.gz' pixman_0.44.0-3.diff.gz 9417 SHA256:820f71488852530f2a662bb6bdcc8bd8e065a15800d8b459d7ec69e6ffc98a85
```

Other potentially useful URLs:

- https://sources.debian.net/src/pixman/0.44.0-3/ (for browsing the source)
- https://sources.debian.net/src/pixman/0.44.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pixman/0.44.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pkgconf=1.8.1-4`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-4`
- `pkgconf:amd64=1.8.1-4`
- `pkgconf-bin=1.8.1-4`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-4
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.dsc' pkgconf_1.8.1-4.dsc 2130 SHA256:782a764448d1ecf39f80c7a1747c28fcbde1800b615eee6a46639a17e58b62f9
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.debian.tar.xz' pkgconf_1.8.1-4.debian.tar.xz 17736 SHA256:e56c56a5f40eb0d57bebcb79983a755e16cf1e1595a6fec7f02b20bd58baa734
```

Other potentially useful URLs:

- https://sources.debian.net/src/pkgconf/1.8.1-4/ (for browsing the source)
- https://sources.debian.net/src/pkgconf/1.8.1-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pkgconf/1.8.1-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `postgresql-17=17.4-1`

Binary Packages:

- `libpq-dev=17.4-1+b1`
- `libpq5:amd64=17.4-1+b1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/postgresql-17/17.4-1/


### `dpkg` source package: `procps=2:4.0.4-7`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-7`
- `procps=2:4.0.4-7`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-7
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-7.dsc' procps_4.0.4-7.dsc 2124 SHA256:460a4816eb0457adb04d059bd6950a7a94b0847859560ff5d02d703df5c00bc2
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-7.debian.tar.xz' procps_4.0.4-7.debian.tar.xz 29964 SHA256:460a5fb98ad62b5a0256c180b3246099f5c3cb73c97b235aeafaa30fef561015
```

Other potentially useful URLs:

- https://sources.debian.net/src/procps/2:4.0.4-7/ (for browsing the source)
- https://sources.debian.net/src/procps/2:4.0.4-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/procps/2:4.0.4-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python-packaging=24.2-1`

Binary Packages:

- `python3-packaging=24.2-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=24.2-1
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.2-1.dsc' python-packaging_24.2-1.dsc 1911 SHA256:4d6ece32ca44d4c83ea688fe38ea459928b7ce0d4662ab72816157b81f8360dc
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.2.orig.tar.gz' python-packaging_24.2.orig.tar.gz 163950 SHA256:c228a6dc5e932d346bc5739379109d49e8853dd8223571c7c5b55260edc0b97f
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.2-1.debian.tar.xz' python-packaging_24.2-1.debian.tar.xz 2964 SHA256:9e435cf0be0dfec57b5736968df5c499b2ccd846be3b807b2ec021a07536524f
```

Other potentially useful URLs:

- https://sources.debian.net/src/python-packaging/24.2-1/ (for browsing the source)
- https://sources.debian.net/src/python-packaging/24.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python-packaging/24.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3-defaults=3.13.2-2`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.2-2`
- `python3=3.13.2-2`
- `python3-minimal=3.13.2-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.2-2
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.13.2-2.dsc' python3-defaults_3.13.2-2.dsc 2948 SHA256:5c9680f0f0ebc39ba8037b0d10bef81b46272ee1d3db8ec49ec4aea029ad2447
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.13.2-2.tar.gz' python3-defaults_3.13.2-2.tar.gz 388662 SHA256:153c628880eff39da3124dd8561fbf3fe9d1b84527cab50e2f193f12fcb289a3
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3-defaults/3.13.2-2/ (for browsing the source)
- https://sources.debian.net/src/python3-defaults/3.13.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3-defaults/3.13.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3.13=3.13.2-3`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.2-3`
- `libpython3.13-stdlib:amd64=3.13.2-3`
- `python3.13=3.13.2-3`
- `python3.13-minimal=3.13.2-3`

Licenses: (parsed from: `/usr/share/doc/libpython3.13-minimal/copyright`, `/usr/share/doc/libpython3.13-stdlib/copyright`, `/usr/share/doc/python3.13/copyright`, `/usr/share/doc/python3.13-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.13=3.13.2-3
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.2-3.dsc' python3.13_3.13.2-3.dsc 4300 SHA256:1fa371106d16222a85182e652f4d80f66702ba550ba7859c3197c5e33b28d731
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.2.orig.tar.xz' python3.13_3.13.2.orig.tar.xz 22621108 SHA256:d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.2.orig.tar.xz.asc' python3.13_3.13.2.orig.tar.xz.asc 963 SHA256:5b9ea87ee586301f8bc0ad83b7755257f10994e9f9ba918b47d1b0fac2b29327
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.2-3.debian.tar.xz' python3.13_3.13.2-3.debian.tar.xz 585440 SHA256:1304333c34d328f21c60a0a239f303a01d73fbc93c599b2684b70e966029ff92
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3.13/3.13.2-3/ (for browsing the source)
- https://sources.debian.net/src/python3.13/3.13.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3.13/3.13.2-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `readline=8.2-6`

Binary Packages:

- `libreadline-dev:amd64=8.2-6`
- `libreadline8t64:amd64=8.2-6`
- `readline-common=8.2-6`

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
$ apt-get source -qq --print-uris readline=8.2-6
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2-6.dsc' readline_8.2-6.dsc 2810 SHA256:6f94c7144d6b6b1ff88aaebd81480e87f8773b7638031782aac12ef93ffd2e71
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA256:3feb7171f16a84ee82ca18a36d7b9be109a52c04f492a053331d7d1095007c35
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2-6.debian.tar.xz' readline_8.2-6.debian.tar.xz 38396 SHA256:d1cf806644dbce298cf929f1cc9b3af5a50cd7db97b6f69db280c1eb2f544376
```

Other potentially useful URLs:

- https://sources.debian.net/src/readline/8.2-6/ (for browsing the source)
- https://sources.debian.net/src/readline/8.2-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/readline/8.2-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rpcsvc-proto=1.4.3-1`

Binary Packages:

- `rpcsvc-proto=1.4.3-1`

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
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.3-1
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA256:7d8e122bd18b02fe0de6d467a0ecdafff74035b3e1ed0da1c0c792d9c015682f
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA256:69315e94430f4e79c74d43422f4a36e6259e97e67e2677b2c7d7060436bd99b1
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA256:02034b9dadcf3af5424f72eb65c3842c8d7117b6b78e7a3c798316ceb60843d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/rpcsvc-proto/1.4.3-1/ (for browsing the source)
- https://sources.debian.net/src/rpcsvc-proto/1.4.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rpcsvc-proto/1.4.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-2+b5`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b5`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2.dsc 2299 SHA256:a296819cd2ab5880b67ad963ef0867cb10e462f4403e52565aa863eb05bb1370
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2.debian.tar.xz 8096 SHA256:26d47de07d16285e4ca55b0828cbbf1ba35e671f9b3500a87e301fe755d26882
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sq=1.3.1-1`

Binary Packages:

- `sq=1.3.1-1`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-1
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-1.dsc' rust-sequoia-sq_1.3.1-1.dsc 4064 SHA256:63b6a23e312314658d7e7d03c510c789f92492c871ebf3af833e118de8ac83f3
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA256:5c04b662da1c207e79beaeff6e5ab2d713ab10c1263f64c367f8489aac815705
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-1.debian.tar.xz' rust-sequoia-sq_1.3.1-1.debian.tar.xz 5488 SHA256:affd8d112cebecaf017aaaad9887ceaf280188f7429bfcdf7e7e0c09882cd477
```

Other potentially useful URLs:

- https://sources.debian.net/src/rust-sequoia-sq/1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/rust-sequoia-sq/1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rust-sequoia-sq/1.3.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sqv=1.2.1-6`

Binary Packages:

- `sqv=1.2.1-6+b1`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/rust-sequoia-sqv/1.2.1-6/


### `dpkg` source package: `sed=4.9-2`

Binary Packages:

- `sed=4.9-2`

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
$ apt-get source -qq --print-uris sed=4.9-2
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.9-2/ (for browsing the source)
- https://sources.debian.net/src/sed/4.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.9-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA256:f84ac7cccca8e0f3f9e5c0d5173c7d1f22afdc0a98210120d1d35a92b4baf9df
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA256:620602b900bad2b9856556a7895ea146110f602cd526a1cc03068a0bc9542803
```

Other potentially useful URLs:

- https://sources.debian.net/src/sensible-utils/0.0.24/ (for browsing the source)
- https://sources.debian.net/src/sensible-utils/0.0.24/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sensible-utils/0.0.24/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `serf=1.3.10-3`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3+b1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/serf/1.3.10-3/


### `dpkg` source package: `shadow=1:4.17.3-3`

Binary Packages:

- `login.defs=1:4.17.3-3`
- `passwd=1:4.17.3-3`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.17.3-3/


### `dpkg` source package: `shared-mime-info=2.4-5`

Binary Packages:

- `shared-mime-info=2.4-5+b2`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-5
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.dsc' shared-mime-info_2.4-5.dsc 2237 SHA256:daadcf9aadf96cb45875856d8046f692d1e563bda5687150d993f9deba274a39
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA256:32dc32ae39ff1c1bf8434dd3b36770b48538a1772bc0298509d034f057005992
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.debian.tar.xz' shared-mime-info_2.4-5.debian.tar.xz 10812 SHA256:10eceaa29c5927dcc9cc9ba419f7bbdee68542cc5cfb3be15dde3e36735a3206
```

Other potentially useful URLs:

- https://sources.debian.net/src/shared-mime-info/2.4-5/ (for browsing the source)
- https://sources.debian.net/src/shared-mime-info/2.4-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shared-mime-info/2.4-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.46.1-2`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-2`
- `libsqlite3-dev:amd64=3.46.1-2`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-2
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1-2.dsc' sqlite3_3.46.1-2.dsc 2632 SHA256:4da786a1b198d282e6df350629715eb9e08dac9000098a5ceb39247ff00b4106
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA256:648df41a8e532882b1905df45919aae4bafaf74c455f66bc86f1f52f45c8b8f0
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA256:d0cdd2ece271b29e7ce18095745d892517ee26d0f270065b3a25c2e9eb11639c
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1-2.debian.tar.xz' sqlite3_3.46.1-2.debian.tar.xz 30732 SHA256:7a199eec1342441a637fe36ce01e0e2badffbf67f0eb9f311edce1247e2373ce
```

Other potentially useful URLs:

- https://sources.debian.net/src/sqlite3/3.46.1-2/ (for browsing the source)
- https://sources.debian.net/src/sqlite3/3.46.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sqlite3/3.46.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `subversion=1.14.5-2`

Binary Packages:

- `libsvn1:amd64=1.14.5-2+b3`
- `subversion=1.14.5-2+b3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/subversion/1.14.5-2/


### `dpkg` source package: `sysprof=48.0-2`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=48.0-2`

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
$ apt-get source -qq --print-uris sysprof=48.0-2
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_48.0-2.dsc' sysprof_48.0-2.dsc 3085 SHA256:8e67bfd77ba5d6405dd373625553fedb2d2147aa29268c5639e459727a787e8e
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_48.0.orig.tar.xz' sysprof_48.0.orig.tar.xz 1224264 SHA256:1b0f0380f2f30708ba87829321a06fee1db36dfa87797bbf07f0a7acf4498d18
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_48.0-2.debian.tar.xz' sysprof_48.0-2.debian.tar.xz 17728 SHA256:212e0fb593e6d23ae74ebeca99d73bb9cc5c4bc23607dd384b7e5552a9cd6da6
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysprof/48.0-2/ (for browsing the source)
- https://sources.debian.net/src/sysprof/48.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysprof/48.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=257.4-3`

Binary Packages:

- `libsystemd0:amd64=257.4-3`
- `libudev1:amd64=257.4-3`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/systemd/257.4-3/


### `dpkg` source package: `sysvinit=3.14-4`

Binary Packages:

- `sysvinit-utils=3.14-4`

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
$ apt-get source -qq --print-uris sysvinit=3.14-4
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14-4.dsc' sysvinit_3.14-4.dsc 2375 SHA256:1cfe65682218077e6f76011f0c5caacc9f2ab214d55893307d4a54c93312ac92
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA256:4e90a148707cf64113fc97343c053f9c0c9589551936b053999dcc69731f295f
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14-4.debian.tar.xz' sysvinit_3.14-4.debian.tar.xz 122156 SHA256:2ba0aa763232112696bce50ee5acc707a515fcbd5b2c194193bfa7a0a525bff6
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.14-4/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.14-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.14-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tar=1.35+dfsg-3.1`

Binary Packages:

- `tar=1.35+dfsg-3.1`

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
$ apt-get source -qq --print-uris tar=1.35+dfsg-3.1
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA256:5bb58d4966d94c99a9f1b182676089ecc05058d62fdb927f5c07539d9cda4077
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA256:0d0278034b82ed84dce04a461879b6e1871e4cb416a0ff04d3d35ff05fc30a53
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-3.1/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tiff=4.7.0-2`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-2`
- `libtiff6:amd64=4.7.0-2`
- `libtiffxx6:amd64=4.7.0-2`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tiff/4.7.0-2/


### `dpkg` source package: `tzdata=2025b-1`

Binary Packages:

- `tzdata=2025b-1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-1
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b-1.dsc' tzdata_2025b-1.dsc 2434 SHA256:184bbd6afb219c5d267fab313e2f2bc7325fa2a4f6a5259ad171f0f718add531
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA256:11810413345fc7805017e27ea9fa4885fd74cd61b2911711ad038f5d28d71474
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA256:829c06258175c0143754a89e26d7445c243a86cef8e9cf7d020b128f6d82496b
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b-1.debian.tar.xz' tzdata_2025b-1.debian.tar.xz 126756 SHA256:fa7f90e6efc37c27db5e4464f1f9a656b26ceac42e8c14d7cadb3a74698df5e0
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2025b-1/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2025b-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2025b-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ucf=3.0051`

Binary Packages:

- `ucf=3.0051`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0051
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0051.dsc' ucf_3.0051.dsc 1512 SHA256:2b7419efb55fb4aa273df04d1de88a1db90220afd68168e451f04185d099482c
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0051.tar.xz' ucf_3.0051.tar.xz 70872 SHA256:760439e290955065d95c6daabb0ed097f4b7cecf31a760a6f40c7ba3efeaae74
```

Other potentially useful URLs:

- https://sources.debian.net/src/ucf/3.0051/ (for browsing the source)
- https://sources.debian.net/src/ucf/3.0051/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ucf/3.0051/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `unbound=1.22.0-1`

Binary Packages:

- `libunbound8:amd64=1.22.0-1+b1`

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
$ apt-get source -qq --print-uris unbound=1.22.0-1
'http://deb.debian.org/debian/pool/main/u/unbound/unbound_1.22.0-1.dsc' unbound_1.22.0-1.dsc 3169 SHA256:0f0af250e37756b71e644e9ca850efcd5b4b75edac8ae191bdb3b325abca613d
'http://deb.debian.org/debian/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz' unbound_1.22.0.orig.tar.gz 6682466 SHA256:c5dd1bdef5d5685b2cedb749158dd152c52d44f65529a34ac15cd88d4b1b3d43
'http://deb.debian.org/debian/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz.asc' unbound_1.22.0.orig.tar.gz.asc 833 SHA256:1b5d91ad040b1f1c0351b8f6fe288b4123fc63b887152463512be69bc687f915
'http://deb.debian.org/debian/pool/main/u/unbound/unbound_1.22.0-1.debian.tar.xz' unbound_1.22.0-1.debian.tar.xz 28800 SHA256:d92e3d3231905c2612cd0c88a5f4634ef0372b7d963169c59e946a267efac75b
```

Other potentially useful URLs:

- https://sources.debian.net/src/unbound/1.22.0-1/ (for browsing the source)
- https://sources.debian.net/src/unbound/1.22.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/unbound/1.22.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `unzip=6.0-29`

Binary Packages:

- `unzip=6.0-29`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-29
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0-29.dsc' unzip_6.0-29.dsc 1464 SHA256:ecc73beeb9a18f354124b87f6713facb726ffd4b732ce7a6e144d073a1e777ae
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0-29.debian.tar.xz' unzip_6.0-29.debian.tar.xz 25876 SHA256:14043e5ea351c02b3bc8676e1e6d20d79b9a690b6d7520e8138ac629cc048417
```

Other potentially useful URLs:

- https://sources.debian.net/src/unzip/6.0-29/ (for browsing the source)
- https://sources.debian.net/src/unzip/6.0-29/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/unzip/6.0-29/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `utf8proc=2.9.0-1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1+b2`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0-1.dsc' utf8proc_2.9.0-1.dsc 2187 SHA256:bb9fd54cb4584ee7c677901312608249f503aa910ca60db043d3273b86dd228a
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA256:18c1626e9fc5a2e192311e36b3010bfc698078f692888940f1fa150547abb0c1
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0-1.debian.tar.xz' utf8proc_2.9.0-1.debian.tar.xz 5836 SHA256:b285489bb5d293ce24d2eea42450f3ef15ff13a23fc422de6a0cf5760872f789
```

Other potentially useful URLs:

- https://sources.debian.net/src/utf8proc/2.9.0-1/ (for browsing the source)
- https://sources.debian.net/src/utf8proc/2.9.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/utf8proc/2.9.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.41-3`

Binary Packages:

- `bsdutils=1:2.41-3`
- `libblkid-dev:amd64=2.41-3`
- `libblkid1:amd64=2.41-3`
- `liblastlog2-2:amd64=2.41-3`
- `libmount-dev:amd64=2.41-3`
- `libmount1:amd64=2.41-3`
- `libsmartcols1:amd64=2.41-3`
- `libuuid1:amd64=2.41-3`
- `login=1:4.16.0-2+really2.41-3`
- `mount=2.41-3`
- `util-linux=2.41-3`
- `uuid-dev:amd64=2.41-3`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/liblastlog2-2/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.41-3
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41-3.dsc' util-linux_2.41-3.dsc 4942 SHA256:7f94e770c585ea1d9ff6add283789701bd81e12fe2ded0d206008108434f11b2
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41.orig.tar.xz' util-linux_2.41.orig.tar.xz 9535724 SHA256:81ee93b3cfdfeb7d7c4090cedeba1d7bbce9141fd0b501b686b3fe475ddca4c6
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.41-3.debian.tar.xz' util-linux_2.41-3.debian.tar.xz 104492 SHA256:2236f0cca01aac1b9d01bc5106a9ca9626e65cfb33ace0bdbccdc787bf1fbb8c
```

Other potentially useful URLs:

- https://sources.debian.net/src/util-linux/2.41-3/ (for browsing the source)
- https://sources.debian.net/src/util-linux/2.41-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/util-linux/2.41-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `wget=1.25.0-2`

Binary Packages:

- `wget=1.25.0-2`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0-2.dsc' wget_1.25.0-2.dsc 2251 SHA256:32caf133042db927360a8c35357e4b2877eb83ff0ca144ceb64508947d894f55
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA256:766e48423e79359ea31e41db9e5c289675947a7fcf2efdcedb726ac9d0da3784
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz.asc' wget_1.25.0.orig.tar.gz.asc 854 SHA256:47f0989685931c3df6166061069659bc13a75b221a62041625007fa2dad7411b
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0-2.debian.tar.xz' wget_1.25.0-2.debian.tar.xz 27884 SHA256:45d4411e892d12af710ddff536d2daf430031387e336153f5f996cf536487b90
```

Other potentially useful URLs:

- https://sources.debian.net/src/wget/1.25.0-2/ (for browsing the source)
- https://sources.debian.net/src/wget/1.25.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/wget/1.25.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xft=2.3.6-1`

Binary Packages:

- `libxft-dev:amd64=2.3.6-1+b4`
- `libxft2:amd64=2.3.6-1+b4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1
'http://deb.debian.org/debian/pool/main/x/xft/xft_2.3.6-1.dsc' xft_2.3.6-1.dsc 2006 SHA256:252220495bd12fac30d8f1b1994916beaed9c5149138dcc62e230fee17339530
'http://deb.debian.org/debian/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA256:b7e59f69e0bbabe9438088775f7e5a7c16a572e58b11f9722519385d38192df5
'http://deb.debian.org/debian/pool/main/x/xft/xft_2.3.6-1.diff.gz' xft_2.3.6-1.diff.gz 17995 SHA256:9d4c64fc52626134a3f753df88fceaba0cb460bd9b56544f0e42178deca77019
```

Other potentially useful URLs:

- https://sources.debian.net/src/xft/2.3.6-1/ (for browsing the source)
- https://sources.debian.net/src/xft/2.3.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xft/2.3.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.dsc' xorg-sgml-doctools_1.11-1.1.dsc 1987 SHA256:6aac68e597386c10b02646d2026a833d301749a938701f4ca8efd4d19ad34295
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA256:986326d7b4dd2ad298f61d8d41fe3929ac6191c6000d6d7e47a8ffc0c34e7426
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.diff.gz' xorg-sgml-doctools_1.11-1.1.diff.gz 3296 SHA256:0c11e15d4f9aaacd38452a6a37d064f1a07058dcead7ab1e2aca223ec0a94d11
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1.1/ (for browsing the source)
- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg-sgml-doctools/1:1.11-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorg=1:7.7+24`

Binary Packages:

- `x11-common=1:7.7+24`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+24
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7%2b24.dsc' xorg_7.7+24.dsc 1970 SHA256:3bff9d33df4e1e27c64e777f2fbf68b5f0de93f3985783e953ecaa2d00a636f9
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7%2b24.tar.xz' xorg_7.7+24.tar.xz 234100 SHA256:d3a417626799a1a989c34f76a930597e3feee46710b55a334e01a5233cf1daf2
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg/1:7.7+24/ (for browsing the source)
- https://sources.debian.net/src/xorg/1:7.7+24/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg/1:7.7+24/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorgproto=2024.1-1`

Binary Packages:

- `x11proto-dev=2024.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2024.1-1
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1-1.dsc' xorgproto_2024.1-1.dsc 3336 SHA256:56c08773592f3cf529bc087449de421aac0645b5c43fad41387b856b5e29fab7
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz' xorgproto_2024.1.orig.tar.gz 1115486 SHA256:4f6b9b4faf91e5df8265b71843a91fc73dc895be6210c84117a996545df296ce
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz.asc' xorgproto_2024.1.orig.tar.gz.asc 195 SHA256:41d650fd19f3df1ae8ad24c2570638d5cdadff819613f8cff96d17310d35347c
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1-1.diff.gz' xorgproto_2024.1-1.diff.gz 25061 SHA256:f250a5bc693079f84dc0caad3cc282433940d3665ff9a77b8dc4dc0961f83d1b
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorgproto/2024.1-1/ (for browsing the source)
- https://sources.debian.net/src/xorgproto/2024.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorgproto/2024.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA256:dd74ab9199e8f45215b566a9317cac7953bf063ce6893c185eccaf0fb4d84d8f
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA256:48ed850ce772fef1b44ca23639b0a57e38884045ed2cbb18ab137ef33ec713f9
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA256:0dac18165654d79e0796b80fab4c1104998d29e6d0b098af0426a1d72399521e
```

Other potentially useful URLs:

- https://sources.debian.net/src/xtrans/1.4.0-1/ (for browsing the source)
- https://sources.debian.net/src/xtrans/1.4.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xtrans/1.4.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xxhash=0.8.3-2`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA256:9d1f7aaace7871fbdb8775d756c6eaca84e6ad5d8e9c6ac465b7e0adc06ff90c
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA256:aae608dfe8213dfd05d909a57718ef82f30722c392344583d3f39050c7f29a80
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA256:13824bfb2b2367225dfe3090d0ae050614f1c470a47db7232a2e9d4b2b14ad31
```

Other potentially useful URLs:

- https://sources.debian.net/src/xxhash/0.8.3-2/ (for browsing the source)
- https://sources.debian.net/src/xxhash/0.8.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xxhash/0.8.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.6.4-1`

Binary Packages:

- `liblzma-dev:amd64=5.6.4-1`
- `liblzma5:amd64=5.6.4-1`
- `xz-utils=5.6.4-1`

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
$ apt-get source -qq --print-uris xz-utils=5.6.4-1
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.4-1.dsc' xz-utils_5.6.4-1.dsc 2705 SHA256:d0eadcd46b89742b5673a51f98f5624b8d7cf464e556727879083a16dd7abd1e
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.4.orig.tar.xz' xz-utils_5.6.4.orig.tar.xz 1340516 SHA256:829ccfe79d769748f7557e7a4429a64d06858e27e1e362e25d01ab7b931d9c95
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.4.orig.tar.xz.asc' xz-utils_5.6.4.orig.tar.xz.asc 833 SHA256:a41ebfd79595cadc2ff59f27ff11bea80428028f43cce1463df5a379759fe066
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.4-1.debian.tar.xz' xz-utils_5.6.4-1.debian.tar.xz 30080 SHA256:ae164f6790927bd11f93e005a7275444e0e63614e9c9ed709e23c7f07545cffe
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.6.4-1/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.6.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.6.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1+b1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg+really1.3.1-1/ (for access to the source package after it no longer exists in the archive)
