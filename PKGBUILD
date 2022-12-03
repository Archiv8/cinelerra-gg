#!/bin/bash

# Based on original PKGBUILD by Fabio "Lolix" Loli <fabio.loli@disroot.org> -> https://github.com/FabioLolix, pingplug < aur at pingplug dot me >, and goodguy <lists.cinelerra-gg.org>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# @ToDo Add files: User documentation
# @ToDo Add files: Tooling
# @ToDo Package manual and hints
# @ToDo libdpx: https://www.vpixx.com/manuals/python/html/libdpx.html
# @ToDo encore: Think that dependency should be  https://encore.dev/ not opencore-amr
# @ToDo Create vulkan-sdk package: https://vulkan.lunarg.com/doc/sdk/latest/linux/getting_started.html
# @Todo Create ilmbase package: https://github.com/aforsythe/IlmBase
# @FixMe The config reports opernexr as missing.  It is present in depends array
# and configure finds the header files
#configure:25095: checking for openexr available
#configure:25139: g++ -o conftest -I/usr/include/OpenEXR -I/usr/local/include/
# OpenEXR -I/usr/include/OpenEXR -pthread -I/usr/include/Imath  -I/usr/include/
# openjpeg-2.5 -I/usr/include/OpenEXR -Wl,-O1,--sort-common,--as-needed,-z,#
# relro,-z,now -flto=auto conftest.cpp  -lImath -lIlmThread -lIex -lpthread >&5
# configure:25139: $? = 0
# configure:25167: result: yes
# HAVE_OPENEXR='no'
# @FixMe The config reports lilv as missing.   It is present in depends array
# HAVE_lilv='no'
# @FixMe The config reports openjpeg as missing.   It is present in depends array as openjpeg2 should it be an older version
# HAVE_openjpeg='no'
# @FixMe The config reports serd as missing.   It is present in depends array
# HAVE_serd='no'
# @FixMe The config reports sord as missing.   It is present in depends array
# HAVE_sord='no'
# @FixMe The config reports sratom as missing.   It is present in depends array
# HAVE_sratom='no'
# @FixMe The config reports audiofile as missing but it is found by configure.
# It is present in depends array
# configure:23896: checking for audiofile.h
# configure:23896: gcc -c -march=x86-64 -mtune=generic -O2 -pipe -fno-plt
# -fexceptions         -Wp,-D_FORTIFY_SOURCE=2 -Wformat
# -Werror=format-security         -fstack-clash-protection -fcf-protection
# -flto=auto -I/usr/include/openjpeg-2.5 -I/usr/include/OpenEXR conftest.c >&5
# configure:23896: $? = 0
# configure:23896: result: yes
# configure:23907: checking audiofile headers
# configure:23909: result: yes
# HAVE_audiofile='no'
# @FixMe isofs.h is part of the linux kernel, which package contains the header file
# conftest.c:23:10: fatal error: linux/isofs.h: No such file or directory
#     23 | #include "linux/isofs.h"
# @Query Including audiofile, --enable-audiofile, causes build to fail:
#          - What features does it enable.
#          - Is there any current workaround
# Error message:
#      make[1]: *** [Makefile:585: all-recursive] Error 1
#      make[1]: Leaving directory "/build/cinelerra-gg/src/cinelerra-5.1"
#      make: *** [Makefile:532: all] Error 2

# @Query What do the following configuration options actually do
#    --enable-shared \
#    --disable-static \
# @FixMe Namcap warnings and errors
# Maintainer: Ross Clark <https://github.com/orgs/Archiv8/cinelerra-gg/discussions>
# Contributor: Ross Clark <https://github.com/orgs/Archiv8/cinelerra-gg/discussions>

_nameBase="cinelerra"
_nameSuffix="gg"
_nameShort="cin"
_ver="5.1"
_verSuffix="20221031"

pkgname="${_nameBase}-${_nameSuffix}"
pkgver="${_ver}.${_verSuffix}"
pkgrel=1
pkgdesc="Professional video editing and compositing environment"
arch=(
  "x86_64"
)
url="https://www.cinelerra-gg.org"
license=(
  "GPL2"
)
depends=(
  # Arch Linux Official repositories
  "alsa-lib"
  "aom"
  "atk"
  # @See notes above for audiofile
  "audiofile"
  "a52dec"
  "bzip2"
  "cairo"
  "clang"
  # @See above for cuda
  # "cuda"
  # "cuda-tools"
  "dav1d"
  "dvdauthor"
  "expat"
  "fftw"
  "flac"
  "fontconfig"
  "freetype2"
  "fribidi"
  "gcc-libs"
  "gdk-pixbuf2"
  "glib2"
  "glibc"
  "glu"
  "graphite"
  "gtk2"
  "harfbuzz"
  # @See above for ilmbase
  "imath"
  "inkscape"
  "jbig2dec"
  "jbigkit"
  "ladspa"
  "lame"
  "libavc1394"
  "libxcomposite"
  "libdatrie"
  "libdv"
  "libffi"
  "libglvnd"
  "libiec61883"
  "libjpeg-turbo"
  "libogg"
  "libpng"
  "libpulse"
  "libraw1394"
  "libsndfile"
  "libthai"
  "libtiff"
  "libtheora"
  "libutil-linux"
  "libusb"
  "libva"
  "libvdpau"
  "libvorbis"
  "libvpx"
  "libwebp"
  "libx11"
  "libxau"
  "libxcb"
  "libxcursor"
  "libxdamage"
  "libxdmcp"
  "libxext"
  "libxfixes"
  "libxft"
  "libxi"
  "libxinerama"
  "libxrandr"
  "libxrender"
  "libxv"
  # @See above for lilv
  "lilv"
  "mjpegtools"
  "numactl"
  # @See above for encore
  "opencore-amr"
  "opencv"
  # @See above for openexr
  "openexr"
  # @See above for openjpeg
  "openjpeg2"
  "opus"
  "pango"
  "pcre"
  "perl"
  "pixman"
  # @See above for serd
  "serd"
  # @See above for sord
  "sord"
  # @See above for sratom
  "sratom"
  "suil"
  "ttf-dejavu"
  "twolame"
  "udftools"
  "x264"
  "x265"
  "xorg-fonts-misc"
  "xorg-server"
  "xz"
  "zlib"
)
makedepends=(
  "autoconf"
  "automake"
  "cmake"
  "ctags"
  "git"
  "libtool"
  "libxml2"
  "nasm"
  "perl-xml-libxml"
  "perl-xml-parser"
  "python"
  "xorg-mkfontdir"
  "xorg-mkfontscale"
  "yasm"
)
conflicts=(
  "cin"
)
source=(
  "https://${pkgname}.org/download/pkgs/src/${_nameShort}_${pkgver}-src.tgz"
  "https://${pkgname}.org/download/images/HTML_Manual-${_verSuffix}.tgz"
)
sha512sums=(
  "50a637ebc616e4220c1ce275696ac742fe7cadb0d81a223e54ac93626de6b2fcb8837b31c1ad2931bec3f13acea0fc18c8438b0082f2b9a3a3bb6d89226aedd6"
  "c82088b123e61521af4cacc21cbd5c05fbd467e2754033bc08de3430daac93c75025d6a233f80d1a3225430b4379c9aef462c2f42b4f1aa188424808f3224c7f"
)

prepare() {

  cd "${srcdir}/${_nameBase}-${_ver}"

  ./autogen.sh
}

build() {

  cd "${srcdir}/${_nameBase}-${_ver}"

  # @See above for notes on config options

  ./configure \
    --prefix=/usr \
    --without-single-user \
    --disable-static-build \
    --with-exec-name="${pkgname}" \
    CPPFLAGS="-I/usr/include/openjpeg-2.5 -I/usr/include/OpenEXR"

  make -j1
}

package() {

  cd "${srcdir}/${_nameBase}-${_ver}"
  make -j1 DESTDIR="${pkgdir}" install
}
