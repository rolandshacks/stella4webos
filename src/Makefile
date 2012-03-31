###############################################################################
#
# Makefile
#
###############################################################################

TARGET = stella
#LIBS = vengine
#LIBDIRS = ../vengine/target
DEBUG = 0

###############################################################################

VERSION   = 1
REVISION  = 0

RESOURCES = $(sort $(subst .svn,,$(wildcard ../resources/*)))

DEF      += WEBOS=1 HAVE_INTTYPES UNIX DISPLAY_OPENGL HAVE_GLES SOUND_SUPPORT

INCDIRS  += . ./emucore ./gui ./common ./unix ./zlib ./libpng

SRCDIRS   = emucore gui common unix libpng

SRC       = $(foreach dir,$(SRCDIRS),$(wildcard $(dir)/*.cxx) $(wildcard $(dir)/*.c))
SRC      += $(filter-out zlib/minigzip.c,$(wildcard zlib/*.c))

#SRC       = $(wildcard emucore/*.cxx gui/*.cxx common/*.cxx unix/*.cxx) \
#            $(wildcard libpng/*.c) \
#            $(filter-out zlib/minigzip.c,$(wildcard zlib/*.c))
          
###############################################################################
#include ../../vengine/generic.mak
include ./generic.mak
