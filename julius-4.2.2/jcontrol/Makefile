# Generated automatically from Makefile.in by configure.
# Copyright (c) 2002-2012 Kawahara Lab., Kyoto University
# Copyright (c) 2002-2005 Shikano Lab., Nara Institute of Science and Technology
# Copyright (c) 2005-2012 Julius project team, Nagoya Institute of Technology
# All rights reserved
#
# $Id: Makefile.in,v 1.6 2012/07/27 08:44:49 sumomo Exp $
#
SHELL=/bin/sh
.SUFFIXES:
.SUFFIXES: .c .o
.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

CC=/Users/hoang8f/Lib/android/android-ndk-r8b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/darwin-x86/bin/arm-linux-androideabi-gcc -mandroid --sysroot=/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm
CFLAGS=-nostdlib -DANDROID_CUSTOM -DANDROID_DEBUG
CPPFLAGS=-I/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/include/  
LDFLAGS=-lc -lz -lgcc -llog 
RM=/bin/rm -f
prefix=/Users/hoang8f/Documents/workspace/JuliusForAndroid/jni
exec_prefix=${prefix}
INSTALL=/usr/bin/install -c

OBJ=jcontrol.o server.o japi_misc.o japi_grammar.o japi_process.o
TARGET=jcontrol

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ $(OBJ) $(LDFLAGS)

install: install.bin

install.bin: $(TARGET)
	${INSTALL} -d ${exec_prefix}/bin
	${INSTALL} $(TARGET) ${exec_prefix}/bin

clean:
	$(RM) $(OBJ)
	$(RM) config.log config.cache
	$(RM) *~ core
	$(RM) $(TARGET) $(TARGET).exe

distclean:
	$(RM) $(OBJ)
	$(RM) config.log config.cache
	$(RM) *~ core
	$(RM) $(TARGET) $(TARGET).exe
	$(RM) config.status
	$(RM) Makefile
