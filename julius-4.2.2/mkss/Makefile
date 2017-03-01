# Generated automatically from Makefile.in by configure.
# Copyright (c) 1991-2012 Kawahara Lab., Kyoto University
# Copyright (c) 2001-2005 Shikano Lab., Nara Institute of Science and Technology
# Copyright (c) 2005-2012 Julius project team, Nagoya Institute of Technology
# All rights reserved 
#
# $Id: Makefile.in,v 1.7 2012/07/27 08:44:57 sumomo Exp $
#
SHELL=/bin/sh
.SUFFIXES:
.SUFFIXES: .c .o
.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

LIBSENT=../libsent
LIBJULIUS=../libjulius
CC=./../ndk/android-ndk-r8b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/darwin-x86/bin/arm-linux-androideabi-gcc -mandroid --sysroot=./../ndk/android-ndk-r8b/platforms/android-8/arch-arm
CFLAGS=-nostdlib -DANDROID_CUSTOM -DANDROID_DEBUG
CPPFLAGS=-I. -I$(LIBJULIUS)/include -I$(LIBSENT)/include -I./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/include/ `$(LIBSENT)/libsent-config --cflags` `$(LIBJULIUS)/libjulius-config --cflags`
LDFLAGS=-Wl,-rpath-link=./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L./../ndk/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L$(LIBJULIUS) `$(LIBJULIUS)/libjulius-config --libs` -L$(LIBSENT) `$(LIBSENT)/libsent-config --libs`
RM=/bin/rm -f
prefix=./../jni
exec_prefix=${prefix}
INSTALL=/usr/bin/install -c

############################################################

TARGET=mkss

all: $(TARGET)

$(TARGET): mkss.c $(LIBSENT)/libsent.a $(LIBJULIUS)/libjulius.a
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ mkss.c $(LDFLAGS)

############################################################

install: install.bin

install.bin: $(TARGET)
	${INSTALL} -d ${exec_prefix}/bin
	${INSTALL} $(TARGET) ${exec_prefix}/bin

############################################################

clean:
	$(RM) *.o *~ core
	$(RM) $(TARGET) $(TARGET).exe

distclean:
	$(RM) *.o *~ core
	$(RM) $(TARGET) $(TARGET).exe
	$(RM) Makefile
