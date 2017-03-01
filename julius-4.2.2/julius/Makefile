# Generated automatically from Makefile.in by configure.
# Copyright (c) 1991-2012 Kawahara Lab., Kyoto University
# Copyright (c) 1997-2000 Information-technology Promotion Agency, Japan
# Copyright (c) 2000-2005 Shikano Lab., Nara Institute of Science and Technology
# Copyright (c) 2005-2012 Julius project team, Nagoya Institute of Technology
# All rights reserved

#
# $Id: Makefile.in,v 1.10 2012/07/27 08:44:49 sumomo Exp $
#
SHELL=/bin/sh
.SUFFIXES:
.SUFFIXES: .c .o
.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

LIBSENT=../libsent
LIBJULIUS=../libjulius
CC=/Users/hoang8f/Lib/android/android-ndk-r8b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/darwin-x86/bin/arm-linux-androideabi-gcc -mandroid --sysroot=/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm
CFLAGS=-nostdlib -DANDROID_CUSTOM -DANDROID_DEBUG
CPPFLAGS=-I. -I$(LIBJULIUS)/include -I$(LIBSENT)/include -I/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/include/ `$(LIBSENT)/libsent-config --cflags` `$(LIBJULIUS)/libjulius-config --cflags`
LDFLAGS=-Wl,-rpath-link=/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L$(LIBJULIUS) `$(LIBJULIUS)/libjulius-config --libs` -L$(LIBSENT) `$(LIBSENT)/libsent-config --libs` 
GTK_CFLAGS=
GTK_LIBS=
RM=/bin/rm -f

## install
prefix=/Users/hoang8f/Documents/workspace/JuliusForAndroid/jni
exec_prefix=${prefix}
bindir=${exec_prefix}/bin
libdir=${exec_prefix}/lib
includedir=${prefix}/include
mandir=${prefix}/man
INSTALL=/usr/bin/install -c
INSTALL_DATA=${INSTALL} -m 644
INSTALL_PROGRAM=${INSTALL}

############################################################

TARGET = julius
INSTALLTARGET = julius

OBJ = \
main.o \
recogloop.o \
module.o \
output_module.o \
output_stdout.o \
output_file.o \
record.o \
charconv.o charconv_libjcode.o libjcode/libjcode.o libjcode/detect.o

############################################################

all: $(TARGET)

$(TARGET): $(LIBSENT)/libsent.a $(LIBJULIUS)/libjulius.a $(OBJ)
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ $(OBJ) $(LDFLAGS) $(GTK_LIBS)

############################################################

install: install.bin

install.bin: $(TARGET)
	${INSTALL} -d ${exec_prefix}/bin
	${INSTALL_PROGRAM} $(TARGET) ${bindir}/${INSTALLTARGET}

depend:
	makedepend -- $(CFLAGS) -- $(OBJSENT)

smallclean:
	$(RM) *.o

clean:
#	$(RM) *.o *.bak *~ core TAGS
	$(RM) $(OBJ)
	$(RM) *.bak *~ core TAGS
	$(RM) config.log config.cache
	$(RM) $(TARGET) $(INSTALLTARGET)
	$(RM) $(TARGET).exe $(INSTALLTARGET).exe

distclean:
#	$(RM) *.o *.bak *~ core TAGS
	$(RM) $(OBJ)
	$(RM) *.bak *~ core TAGS
	$(RM) config.log config.cache
	$(RM) $(TARGET) $(INSTALLTARGET)
	$(RM) $(TARGET).exe $(INSTALLTARGET).exe
	$(RM) config.status config.h
	$(RM) Makefile

############################################################
configure:
	autoconf
	$(RM) config.h.in
	autoheader
