#
# Copyright (c) 2011 Red Hat, Inc.
# Copyright (c) 2011 Tomas Mraz <tm@t8m.info>
#

pythonincdir = $(includedir)/python@PYTHONREV@
pythonsitedir = @PYTHONSITEDIR@

CLEANFILES = *~ constants.c *.so

EXTRA_DIST = pwquality.c setup.py

all-local:
	CFLAGS="${CFLAGS} -fno-strict-aliasing" @PYTHONBINARY@ setup.py build --build-lib=.

install-exec-local:
	CFLAGS="${CFLAGS} -fno-strict-aliasing" @PYTHONBINARY@ setup.py install --prefix=${DESTDIR}${prefix}
