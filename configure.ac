AC_INIT([termite], [0.0.1], [termite@termite.org])

AC_CONFIG_SRCDIR([source/termite.cc])
AC_CONFIG_HEADER([config.h])

##
# Setup automake to be silent and in foreign mode.
##
AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects dist-xz])
AM_SILENT_RULES([yes])

AC_USE_SYSTEM_EXTENSIONS
##
# Check for compiler
##
m4_include([m4/ax_cxx_compile_stdcxx_11.m4])
AC_PROG_CXX
AX_CXX_COMPILE_STDCXX_11 
AM_PROG_CC_C_O


dnl ---------------------------------------------------------------------
dnl Check dependencies
dnl ---------------------------------------------------------------------
PKG_PROG_PKG_CONFIG
PKG_CHECK_MODULES([gtk],     [gtk+-3.0 >= 3.0])
PKG_CHECK_MODULES([vte],     [vte-2.91])

dnl ---------------------------------------------------------------------
dnl Add extra compiler flags
dnl ---------------------------------------------------------------------
AC_SUBST([EXTRA_CFLAGS], ["-Wall -Wextra -Wparentheses -Winline -pedantic"])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
