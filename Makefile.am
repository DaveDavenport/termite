# Specify automake version.
AUTOMAKE_OPTIONS  = 1.11.3

##
# Rofi the program
##
bin_PROGRAMS=termite

LIBS=\
	 @gtk_LIBS@\
	 @vte_LIBS@

AM_CXXFLAGS=\
		  @gtk_CFLAGS@\
		  @vte_CFLAGS@\
		  @EXTRA_CFLAGS@\
		  -Wno-deprecated-declarations

termite_SOURCES=\
				source/termite.cc\
				util/clamp.hh\
				util/maybe.hh\
				util/memory.hh\
				source/url_regex.hh

man1_MANS=\
		  man/termite.1

man5_MANS=\
		  man/termite.config.5

EXTRA_DIST=\
		   $(man1_MANS)\
		   $(man5_MANS)\
		   termite.terminfo\
		   termite.desktop\
		   README.rst\
		   TODO.rst

install-data-local: termite.terminfo
		mkdir -p $(DESTDIR)$(prefix)/share/terminfo/
		tic -x ${top_srcdir}/termite.terminfo -o $(DESTDIR)$(prefix)/share/terminfo/
