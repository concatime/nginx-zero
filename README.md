# _Purely_ static NGiИX
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?longCache=true&style=flat-square)](//github.com/semantic-release/semantic-release)
[![ISC License](https://img.shields.io/badge/license-ISC-brightgreen.svg?longCache=true&style=flat-square)](//www.isc.org/downloads/software-support-policy/isc-license/)
[![Build Status](https://travis-ci.org/concatime/nginx-zero.svg?branch=master)](//travis-ci.org/concatime/nginx-zero)

Package | Version | Latest available
:------:|---------|-
NGiИX   | 1.15.6  | [![](https://repology.org/badge/latest-versions/nginx.svg)](//nginx.org/en/CHANGES)
NJS     | 0.2.5   | [![](https://repology.org/badge/latest-versions/nginx-mod-njs.svg)](//nginx.org/en/docs/njs/changes.html)
MUSL    | 1.1.20  | [![](https://repology.org/badge/latest-versions/musl.svg)](//git.musl-libc.org/cgit/musl/tree/WHATSNEW)
PCRE    | 8.42    | [![](https://repology.org/badge/latest-versions/pcre.svg)](//pcre.org/original/changelog.txt)
ZLIB    | 1.2.11  | [![](https://repology.org/badge/latest-versions/zlib.svg)](//zlib.net/ChangeLog.txt)
LIBRESSL| 2.8.2   | [![](https://repology.org/badge/latest-versions/libressl.svg)](//raw.githubusercontent.com/libressl-portable/portable/master/ChangeLog)
~JEMALLOC~| 5.1.0   | [![](https://repology.org/badge/latest-versions/jemalloc.svg)](//raw.githubusercontent.com/aerospike/jemalloc/master/ChangeLog)

By default, jemalloc is now disabled since it causes boilerplate.

The script (`nginx-zero`) requires:
 - gcc or clang>=3.5 (otherwise, `ld: cannot find -l-user-{start,end}`)
 - tar (+gzip)
 - git
 - make
 - cmake
 - patch

To clone:
`git clone --recurse-submodules -j8 git://github.com/concatime/nginx-zero`

To install, download the release file called `nginx.tar.gz`, and then
`sudo tar xf nginx.tar.gz -C/opt`

### Notes (for me)
In `deps/jemalloc/.gitignore`, I need to manually remove `configure`.
