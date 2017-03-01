# Generated automatically from Makefile.in by configure.
# Copyright (c) 2003-2012 Kawahara Lab., Kyoto University 
# Copyright (c) 2003-2005 Shikano Lab., Nara Institute of Science and Technology
# Copyright (c) 2005-2012 Julius project team, Nagoya Institute of Technology
# All rights reserved
#
# $Id: Makefile.in,v 1.8 2012/07/27 08:44:57 sumomo Exp $
#
SHELL=/bin/sh
.SUFFIXES:
.SUFFIXES: .c .o
.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

LIBSENT=../libsent
CC=./../ndk/android-ndk-r8b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/darwin-x86/bin/arm-linux-androideabi-gcc -mandroid --sysroot=./../ndk/android-ndk-r8b/platforms/android-8/arch-arm
CFLAGS=-nostdlib -DANDROID_CUSTOM -DANDROID_DEBUG
CPPFLAGS=-I$(LIBSENT)/include -I./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/include/   `$(LIBSENT)/libsent-config --cflags`
LDFLAGS=-Wl,-rpath-link=./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L$(LIBSENT) `$(LIBSENT)/libsent-config --libs`
RM=/bin/rm -f
prefix=./../jni
exec_prefix=${prefix}
INSTALL=/usr/bin/install -c

all: mkbinhmm mkbinhmmlist

mkbinhmm: mkbinhmm.o $(LIBSENT)/libsent.a
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ mkbinhmm.o $(LDFLAGS)

mkbinhmmlist: mkbinhmmlist.o $(LIBSENT)/libsent.a
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ mkbinhmmlist.o $(LDFLAGS)

install: install.bin

install.bin: mkbinhmm mkbinhmmlist
	${INSTALL} -d ${exec_prefix}/bin
	${INSTALL} mkbinhmm mkbinhmmlist ${exec_prefix}/bin

clean:
	$(RM) mkbinhmm.o mkbinhmmlist.o
	$(RM) *~ core
	$(RM) mkbinhmm mkbinhmm.exe
	$(RM) mkbinhmmlist mkbinhmmlist.exe

distclean:
	$(RM) mkbinhmm.o mkbinhmmlist.o
	$(RM) *~ core
	$(RM) mkbinhmm mkbinhmm.exe
	$(RM) mkbinhmmlist mkbinhmmlist.exe
	$(RM) Makefile
