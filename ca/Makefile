#
# $Id: Makefile,v 1.1 2003/02/26 23:30:03 lolo Exp $
#
# Translation by:
# 2003  Josep Monés i Teixidor <jmones@puntbarra.com>
#

LINUXDOC := linuxdoc

all: GPGMiniHowto_big.html \
     GPGMiniHowto.html     \
     GPGMiniHowto.txt      \
     GPGMiniHowto.rtf      \
     GPGMiniHowto.dvi      \
     GPGMiniHowto.pdf      \
     GPGMiniHowto.ps


# One HTML big file
GPGMiniHowto_big.html : GPGMiniHowto.sgml
	$(LINUXDOC) -B html -s 0 $<
	mv GPGMiniHowto.html $@

# Other formats
GPGMiniHowto.html \
GPGMiniHowto.txt  \
GPGMiniHowto.rtf :\
GPGMiniHowto.% : GPGMiniHowto.sgml
	linuxdoc -B $* $<

GPGMiniHowto.dvi \
GPGMiniHowto.pdf \
GPGMiniHowto.ps :\
GPGMiniHowto.% : GPGMiniHowto.sgml
	linuxdoc -B latex -o $* $<
