AUTOMAKE_OPTIONS = subdir-objects
SUBDIRS =
AM_CXXFLAGS =
AM_CPPFLAGS =

if !NO_TESSDATA_PREFIX
AM_CXXFLAGS += -DTESSDATA_PREFIX=@datadir@/
endif

if VISIBILITY
AM_CXXFLAGS += -fvisibility=hidden -fvisibility-inlines-hidden
AM_CPPFLAGS += -DTESS_EXPORTS
endif

include_HEADERS = \
	basedir.h errcode.h fileerr.h genericvector.h helpers.h host.h memry.h \
	ndminx.h params.h ocrclass.h platform.h serialis.h strngs.h \
	tesscallback.h unichar.h unicharcompress.h unicharmap.h unicharset.h

noinst_HEADERS = \
    ambigs.h bits16.h bitvector.h ccutil.h clst.h doubleptr.h elst2.h \
    elst.h genericheap.h globaloc.h indexmapbidi.h kdpair.h lsterr.h \
    nwmain.h object_cache.h qrsequence.h sorthelper.h stderr.h \
    scanutils.h tessdatamanager.h tprintf.h unicity_table.h unicodes.h \
    universalambigs.h

noinst_LTLIBRARIES = libtesseract_ccutil.la

libtesseract_ccutil_la_SOURCES = \
    ambigs.cpp basedir.cpp bitvector.cpp \
    ccutil.cpp clst.cpp \
    elst2.cpp elst.cpp errcode.cpp \
    globaloc.cpp indexmapbidi.cpp \
    mainblk.cpp memry.cpp \
    serialis.cpp strngs.cpp scanutils.cpp \
    tessdatamanager.cpp tprintf.cpp \
    unichar.cpp unicharcompress.cpp unicharmap.cpp unicharset.cpp unicodes.cpp \
    params.cpp universalambigs.cpp

if T_WIN
AM_CPPFLAGS += -DWINDLLNAME=\"lib@GENERIC_LIBRARY_NAME@\"
endif
