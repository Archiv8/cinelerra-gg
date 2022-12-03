`configure' configures cinelerra 5.1 to adapt to many kinds of systems.

Usage: ./configure [OPTION]... [VAR=VALUE]...

To assign environment variables (e.g., CC, CFLAGS...), specify them as
VAR=VALUE.  See below for descriptions of some of the useful variables.

Defaults for the options are specified in brackets.

Configuration:
  -h, --help              display this help and exit
      --help=short        display options specific to this package
      --help=recursive    display the short help of all the included packages
  -V, --version           display version information and exit
  -q, --quiet, --silent   do not print `checking ...' messages
      --cache-file=FILE   cache test results in FILE [disabled]
  -C, --config-cache      alias for `--cache-file=config.cache'
  -n, --no-create         do not create output files
      --srcdir=DIR        find the sources in DIR [configure dir or `..']

Installation directories:
  --prefix=PREFIX         install architecture-independent files in PREFIX
                          [/usr/local]
  --exec-prefix=EPREFIX   install architecture-dependent files in EPREFIX
                          [PREFIX]

By default, `make install' will install all the files in
`/usr/local/bin', `/usr/local/lib' etc.  You can specify
an installation prefix other than `/usr/local' using `--prefix',
for instance `--prefix=$HOME'.

For better control, use the options below.

Fine tuning of the installation directories:
  --bindir=DIR            user executables [EPREFIX/bin]
  --sbindir=DIR           system admin executables [EPREFIX/sbin]
  --libexecdir=DIR        program executables [EPREFIX/libexec]
  --sysconfdir=DIR        read-only single-machine data [PREFIX/etc]
  --sharedstatedir=DIR    modifiable architecture-independent data [PREFIX/com]
  --localstatedir=DIR     modifiable single-machine data [PREFIX/var]
  --runstatedir=DIR       modifiable per-process data [LOCALSTATEDIR/run]
  --libdir=DIR            object code libraries [EPREFIX/lib]
  --includedir=DIR        C header files [PREFIX/include]
  --oldincludedir=DIR     C header files for non-gcc [/usr/include]
  --datarootdir=DIR       read-only arch.-independent data root [PREFIX/share]
  --datadir=DIR           read-only architecture-independent data [DATAROOTDIR]
  --infodir=DIR           info documentation [DATAROOTDIR/info]
  --localedir=DIR         locale-dependent data [DATAROOTDIR/locale]
  --mandir=DIR            man documentation [DATAROOTDIR/man]
  --docdir=DIR            documentation root [DATAROOTDIR/doc/cinelerra]
  --htmldir=DIR           html documentation [DOCDIR]
  --dvidir=DIR            dvi documentation [DOCDIR]
  --pdfdir=DIR            pdf documentation [DOCDIR]
  --psdir=DIR             ps documentation [DOCDIR]

Program names:
  --program-prefix=PREFIX            prepend PREFIX to installed program names
  --program-suffix=SUFFIX            append SUFFIX to installed program names
  --program-transform-name=PROGRAM   run sed PROGRAM on installed program names

Optional Features:
  --disable-option-checking  ignore unrecognized --enable/--with options
  --disable-FEATURE       do not include FEATURE (same as --enable-FEATURE=no)
  --enable-FEATURE[=ARG]  include FEATURE [ARG=yes]
  --enable-silent-rules   less verbose build output (undo: "make V=1")
  --disable-silent-rules  verbose build output (undo: "make V=0")
  --enable-dependency-tracking
                          do not reject slow dependency extractors
  --disable-dependency-tracking
                          speeds up one-time build
  --enable-a52dec         build a52dec (yes)
  --enable-djbfft         build djbfft (yes)
  --enable-audiofile      build audiofile (no)
  --enable-encore         build encore (no)
  (Abandoned)--enable-esound         build esound (no)
  --enable-ffmpeg         build ffmpeg (yes)
  --enable-fftw           build fftw (auto)
  --enable-flac           build flac (auto)
  --enable-giflib         build giflib (yes)
  --enable-lame           build lame (auto)
  --enable-libavc1394     build libavc1394 (auto)
  --enable-libraw1394     build libraw1394 (auto)
  --enable-libiec61883    build libiec61883 (auto)
  --enable-libdv          build libdv (auto)
  ?? Version --enable-libjpeg        build libjpeg (auto)
  --enable-opus           build opus (auto)
  --enable-openjpeg       build openjpeg (auto)
          build libogg (auto)
  --enable-libsndfile     build libsndfile (auto)
  --enable-libtheora      build libtheora (auto)
  --enable-libuuid        build libuuid (yes)
  --enable-libvorbis      build libvorbis (auto)
  --enable-mjpegtools     build mjpegtools (yes)
  --enable-openexr        build openexr (auto)
  --enable-openExr        build openExr (auto)
  --enable-ilmBase        build ilmBase (auto)
  --enable-tiff           build tiff (auto)
  --enable-twolame        build twolame (auto)
  --enable-x264           build x264 (auto)
  --enable-x265           build x265 (auto)
  --enable-libvpx         build libvpx (auto)
  --enable-lv2            build lv2 (auto)
  --enable-sratom         build sratom (auto)
  --enable-serd           build serd (auto)
  --enable-sord           build sord (auto)
  --enable-lilv           build lilv (auto)
  --enable-suil           build suil (auto)
  --enable-libaom         build libaom (auto)
  --enable-dav1d          build dav1d (auto)
  --enable-libwebp        build libwebp (auto)
  --enable-ffnvcodec      build ffnvcodec (auto)
  --enable-libdpx         build libdpx (auto)
  --enable-libbthread     build libbthread (auto)
  --enable-static-build   build static ([auto])
  --enable-x264_hidepth   build x264 10bit ([no])
  --enable-x265_hidepth   build x265 10bit ([no])

Optional Packages:


Some influential environment variables:
  CC          C compiler command
  CFLAGS      C compiler flags
  LDFLAGS     linker flags, e.g. -L<lib dir> if you have libraries in a
              nonstandard directory <lib dir>
  LIBS        libraries to pass to the linker, e.g. -l<library>
  CPPFLAGS    (Objective) C/C++ preprocessor flags, e.g. -I<include dir> if
              you have headers in a nonstandard directory <include dir>
  CCAS        assembler compiler command (defaults to CC)
  CCASFLAGS   assembler compiler flags (defaults to CFLAGS)
  CXX         C++ compiler command
  CXXFLAGS    C++ compiler flags

Use these variables to override the choices made by `configure' or to help
it to find libraries and programs with nonstandard names/locations.

Report bugs to <mail@lists.cinelerra-gg.org>.

./configure --prefix=/usr --with-opencv --with-clang --with-video4linux2 --with-commercial
