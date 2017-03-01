# Generated automatically from Makefile.in by configure.
# Copyright (c) 1991-2012 Kawahara Lab., Kyoto University
# Copyright (c) 2000-2005 Shikano Lab., Nara Institute of Science and Technology
# Copyright (c) 2005-2012 Julius project team, Nagoya Institute of Technology
# All rights reserved

SHELL=/bin/sh
.SUFFIXES:
.SUFFIXES: .c .o
.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

LIBSENT=../../libsent
CC=/Users/hoang8f/Lib/android/android-ndk-r8b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/darwin-x86/bin/arm-linux-androideabi-gcc -mandroid --sysroot=/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm
CFLAGS=-nostdlib -DANDROID_CUSTOM -DANDROID_DEBUG
CPPFLAGS=-I/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/include/  -DHAVE_MALLOC_H=1  -I$(LIBSENT)/include `$(LIBSENT)/libsent-config --cflags`
LDFLAGS=-Wl,-rpath-link=/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -L/Users/hoang8f/Lib/android/android-ndk-r8b/platforms/android-8/arch-arm/usr/lib/ -lc -lz -lgcc -llog -L$(LIBSENT) `$(LIBSENT)/libsent-config --libs`
RM=/bin/rm -f
prefix=/Users/hoang8f/Documents/workspace/JuliusForAndroid/jni
exec_prefix=${prefix}
INSTALL=/usr/bin/install -c

############################################################

OBJ = dfa_determinize.o

TARGET=dfa_determinize

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ $(OBJ) $(LDFLAGS)

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
