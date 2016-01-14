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
		  @vte_CFLAGS@

termite_SOURCES=\
				source/termite.cc\
				source/url_regex.hh

