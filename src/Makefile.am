bin_PROGRAMS=rmw
AM_CFLAGS= -std=gnu99 -Wall -I./functions -I./gnu_coreutils-8.26 -DSYSCONFDIR=\"${sysconfdir}\" -DLOCALEDIR=\"${localedir}\"
rmw_SOURCES=			\
./gnu_coreutils-8.26/argmatch.c \
./gnu_coreutils-8.26/error.c \
./gnu_coreutils-8.26/getprogname.c \
./gnu_coreutils-8.26/priv-set.c \
./gnu_coreutils-8.26/remove.c \
./gnu_coreutils-8.26/root-dev-ino.c \
./gnu_coreutils-8.26/yesno.c \
./gnu_coreutils-8.26/timespec.c \
./gnu_coreutils-8.26/dirname.c \
./gnu_coreutils-8.26/openat.c \
./gnu_coreutils-8.26/closein.c \
./gnu_coreutils-8.26/closeout.c \
./gnu_coreutils-8.26/version-etc.c \
./gnu_coreutils-8.26/progname.c \
./gnu_coreutils-8.26/propername.c \
./gnu_coreutils-8.26/inttostr.c \
./gnu_coreutils-8.26/quotearg.c \
./gnu_coreutils-8.26/exitfail.c \
./gnu_coreutils-8.26/rm.c			\
primary_funcs.c			\
main.c 				\
./functions/restore_rmw.c 	\
./functions/config_rmw.c	\
./functions/trivial_rmw.c 	\
./functions/strings_rmw.c 	\
./functions/purging_rmw.c	\
./functions/messages_rmw.c


PACKAGE = @PACKAGE@
VERSION = @VERSION@
top_srcdir = @top_srcdir@
subdir = src

datadir = @datadir@
datarootdir= @datarootdir@
localedir = @localedir@

LIBS = @LIBINTL@ @LIBS@
rmw_LDADD = @LIBINTL@

distdir = ../$(PACKAGE)-$(VERSION)/$(subdir)
dist: Makefile $(DISTFILES)
	for file in $(DISTFILES); do \
	  ln $$file $(distdir) 2>/dev/null || cp -p $$file $(distdir) || exit 1; \
	done
