# _Purely_ static NGiИX
[![ISC License](https://img.shields.io/badge/license-ISC-brightgreen.svg)](//www.isc.org/downloads/software-support-policy/isc-license/)
[![Build Status](https://travis-ci.org/concatime/nginx-zero.svg?branch=master)](//travis-ci.org/concatime/nginx-zero)

Package | Version | Latest available
:------:|---------|-
NGiИX   | 1.15.2  | ![](https://repology.org/badge/latest-versions/nginx.svg)
NJS     | 0.2.2   | ![](https://repology.org/badge/latest-versions/nginx-mod-njs.svg)
MUSL    | 1.1.19  | ![](https://repology.org/badge/latest-versions/musl.svg)
JEMALLOC| 5.1.0   | ![](https://repology.org/badge/latest-versions/jemalloc.svg)
PCRE    | 8.42    | ![](https://repology.org/badge/latest-versions/pcre.svg)
ZLIB    | 1.2.11  | ![](https://repology.org/badge/latest-versions/zlib.svg)
LIBRESSL| 2.7.4   | ![](https://repology.org/badge/latest-versions/libressl.svg)

By default, jemalloc is now disabled since it causes boilerplate.

The script (`nginx-zero`) requires:
 - gcc or clang>=3.5 (otherwise, `ld: cannot find -l-user-{start,end}`)
 - tar (+gzip)
 - git
 - make
 - cmake
 - ninja
 - patch

`git clone --recurse-submodules -j8 git://github.com/concatime/nginx-zero`

### Notes (for me)
In `deps/jemalloc/.gitignore`, I need to manually remove `configure`.
