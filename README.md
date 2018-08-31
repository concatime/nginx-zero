# _Purely_ static NGiИX
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?longCache=true&style=flat-square)](//github.com/semantic-release/semantic-release)
[![ISC License](https://img.shields.io/badge/license-ISC-brightgreen.svg?longCache=true&style=flat-square)](//www.isc.org/downloads/software-support-policy/isc-license/)
[![Build Status](https://travis-ci.org/concatime/nginx-zero.svg?branch=master)](//travis-ci.org/concatime/nginx-zero)

Package | Version | Latest available
:------:|---------|-
NGiИX   | 1.15.3  | ![](https://repology.org/badge/latest-versions/nginx.svg)
NJS     | 0.2.3   | ![](https://repology.org/badge/latest-versions/nginx-mod-njs.svg)
MUSL    | 1.1.19  | ![](https://repology.org/badge/latest-versions/musl.svg)
JEMALLOC| 5.1.0   | ![](https://repology.org/badge/latest-versions/jemalloc.svg)
PCRE    | 8.42    | ![](https://repology.org/badge/latest-versions/pcre.svg)
ZLIB    | 1.2.11  | ![](https://repology.org/badge/latest-versions/zlib.svg)
LIBRESSL| 2.8.0   | ![](https://repology.org/badge/latest-versions/libressl.svg)

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
