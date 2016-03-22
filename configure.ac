AC_PREREQ(2.63)
AC_INIT([FIXME], [m4_esyscmd([./version.sh])], [bugs@niftylogic.com])

#AC_CONFIG_SRCDIR([])
AC_CONFIG_AUX_DIR([build])
AC_CONFIG_MACRO_DIR([build])

AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])

AC_PROG_CC
AC_PROG_INSTALL

AX_TEST_COVERAGE

AC_CONFIG_HEADER([config.h])
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
