#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.63])
AC_INIT(hello, 0.1, welbon.wang@gmail.com)
AC_CONFIG_MACRO_DIR([m4])

AC_CONFIG_SRCDIR([src/hello/hello.c], [src/hellolib/hellolib.c], [lib/hello-lib.c])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE
LT_INIT

AC_ARG_ENABLE([hellolib],
  [  --disable-hellolib      do not build hellolib],
  [case "${enableval}" in
    yes) have_hellolib=true ;;
    no)  have_hellolib=false ;;
    *) AC_MSG_ERROR([bad value ${enableval} for --enable-hellolib]) ;;
   esac],
  [have_hellolib=true])
AM_CONDITIONAL([HAVE_HELLOLIB], [test x$have_hellolib = xtrue])

# Checks for programs.
AC_PROG_CC
AC_PROG_LIBTOOL

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([Makefile
                 inc/Makefile
                 lib/Makefile
                 src/Makefile
                 src/hello/Makefile
                 src/hellolib/Makefile])
AC_OUTPUT
