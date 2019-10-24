# _Purely_ static NGiИX
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?longCache=true&style=flat-square)](//semantic-release.gitbook.io/semantic-release)
[![ISC License](https://img.shields.io/badge/license-ISC-brightgreen.svg?longCache=true&style=flat-square)](//www.isc.org/downloads/software-support-policy/isc-license/)
[![Build Status](https://travis-ci.org/concatime/nginx-zero.svg?branch=master)](//travis-ci.org/concatime/nginx-zero)
[![builds.sr.ht status](https://builds.sr.ht/~concatime/nginx-zero.svg)](//builds.sr.ht/~concatime/nginx-zero)

Package       | Version | Latest available
:------------:|---------|-
NGiИX         | 1.17.5  | [![](https://repology.org/badge/latest-versions/nginx.svg)](//nginx.org/en/CHANGES)
MUSL          | 1.1.23  | [![](https://repology.org/badge/latest-versions/musl.svg)](//git.musl-libc.org/cgit/musl/tree/WHATSNEW)
PCRE          | 8.43    | [![](https://repology.org/badge/latest-versions/pcre.svg)](//pcre.org/original/changelog.txt)
ZLIB          | 1.2.11  | [![](https://repology.org/badge/latest-versions/zlib.svg)](//zlib.net/ChangeLog.txt)
LIBRESSL      | 2.9.0\* | [![](https://repology.org/badge/latest-versions/libressl.svg)](//raw.githubusercontent.com/libressl-portable/portable/master/ChangeLog)
JEMALLOC      | 5.2.1   | [![](https://repology.org/badge/latest-versions/jemalloc.svg)](//raw.githubusercontent.com/jemalloc/jemalloc/master/ChangeLog)
LIBATOMIC\_OPS| 7.6.10  | [![](https://repology.org/badge/latest-versions/libatomic-ops.svg)](//raw.githubusercontent.com/ivmai/libatomic_ops/blob/master/ChangeLog)

\* OCSP stapling [broken](//github.com/libressl-portable/portable/issues/532) on `2.9.1`, `2.9.2` & `3.0.0`.

### Modules
Package                        | Version | Latest available
:-----------------------------:|---------|-
NJS                            | 0.3.6   | [![](https://img.shields.io/github/tag/nginx/njs.svg)](//nginx.org/en/docs/njs/changes.html)
Brotli                         | master  | [![](https://img.shields.io/github/tag/google/ngx_brotli.svg)](//github.com/google/ngx_brotli/releases)
Length Hiding Filter (my fork) | master  | [![](https://img.shields.io/github/tag/concatime/nginx-length-hiding-filter-module.svg)](//github.com/concatime/nginx-length-hiding-filter-module/releases)

Jemalloc provides Bzip tarballs. I convert them with `bzcat IN.tar.bz2 | gzip --best > OUT.tar.gz`.
By default, jemalloc is now disabled since it causes boilerplate.

The script (`nginx-zero`) requires:
 - POSIX sh
 - gcc or clang `>=3.5` (otherwise, `ld: cannot find -l-user-{start,end}`)
 - tar (+gzip)
 - git
 - make
 - cmake
 - patch

To clone:
``git clone --recurse-submodules https://github.com/concatime/nginx-zero.git``

To speed-up the clone process, add `-j` with the number of threads.

To install, download the release file called `nginx.tar.gz`, and then
`sudo tar xf nginx.tar.gz -C/opt`
