# _Purely_ static NGiИX
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?longCache=true&style=flat-square)](//semantic-release.gitbook.io/semantic-release)
[![ISC License](https://img.shields.io/badge/license-ISC-brightgreen.svg?longCache=true&style=flat-square)](//www.isc.org/downloads/software-support-policy/isc-license/)
[![Build Status](https://travis-ci.org/concatime/nginx-zero.svg?branch=master)](//travis-ci.org/concatime/nginx-zero)

Package      | Version | Latest available
:-----------:|---------|-
NGiИX        | 1.15.9  | [![](https://repology.org/badge/latest-versions/nginx.svg)](//nginx.org/en/CHANGES)
MUSL         | 1.1.21  | [![](https://repology.org/badge/latest-versions/musl.svg)](//git.musl-libc.org/cgit/musl/tree/WHATSNEW)
PCRE         | 8.43    | [![](https://repology.org/badge/latest-versions/pcre.svg)](//pcre.org/original/changelog.txt)
ZLIB         | 1.2.11  | [![](https://repology.org/badge/latest-versions/zlib.svg)](//zlib.net/ChangeLog.txt)
LIBRESSL     | 2.9.0   | [![](https://repology.org/badge/latest-versions/libressl.svg)](//raw.githubusercontent.com/libressl-portable/portable/master/ChangeLog)
JEMALLOC     | 5.1.0   | [![](https://repology.org/badge/latest-versions/jemalloc.svg)](//raw.githubusercontent.com/aerospike/jemalloc/master/ChangeLog)
LIBATOMIC_OPS| 7.6.10  | [![](https://repology.org/badge/latest-versions/libatomic-ops.svg)](//raw.githubusercontent.com/ivmai/libatomic_ops/blob/master/ChangeLog)

### Modules
Package              | Version | Latest available
:-------------------:|---------|-
NJS                  | 0.2.8   | [![](https://img.shields.io/github/tag/nginx/njs.svg?maxAge=2592000)](//nginx.org/en/docs/njs/changes.html)
Brotli               | 0.1.3-rc| [![](https://img.shields.io/github/tag/eustas/ngx_brotli.svg?maxAge=2592000)](//github.com/eustas/ngx_brotli/releases)
Length Hiding Filter | 1.1.1   | [![](https://img.shields.io/github/tag/nulab/nginx-length-hiding-filter-module.svg?maxAge=2592000)](//github.com/nulab/nginx-length-hiding-filter-module/releases)


By default, jemalloc is now disabled since it causes boilerplate.

The script (`nginx-zero`) requires:
 - gcc or clang>=3.5 (otherwise, `ld: cannot find -l-user-{start,end}`)
 - tar (+gzip)
 - git
 - make
 - cmake
 - patch

To clone:
`git clone --recurse-submodules -j8 https://github.com/concatime/nginx-zero.git`

To install, download the release file called `nginx.tar.gz`, and then
`sudo tar xf nginx.tar.gz -C/opt`

### Notes (for me)
In `deps/jemalloc/.gitignore`, I need to manually remove `configure`.
