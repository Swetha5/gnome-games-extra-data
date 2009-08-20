# -*- Autoconf -*-

AC_PREREQ([2.53])

AC_INIT([GNOME Games Extra Data],
        [2.26.0],
        [http://bugzilla.gnome.org/enter_bug.cgi?product=gnome-games&component=general],
        [gnome-games-extra-data])

AC_CONFIG_SRCDIR([mahjongg/maya.png])

AM_INIT_AUTOMAKE([1.9 no-dist-gzip dist-bzip2])

m4_ifdef([AM_SILENT_RULES],[AM_SILENT_RULES([no])])

if test -z "$enable_maintainer_mode"; then
  enable_maintainer_mode=yes
fi
AM_MAINTAINER_MODE([enable])

AC_CONFIG_FILES([
Makefile
cards/Makefile
glines/Makefile
gnobots2/Makefile
gnometris/Makefile
iagno/Makefile
mahjongg/Makefile
same-gnome/Makefile
same-gnome/2.10/Makefile
])
AC_OUTPUT
