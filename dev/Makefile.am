AM_CPPFLAGS = -I$(top_srcdir)/include

AM_CFLAGS = $(GLOBAL_CFLAGS) $(libgnutls_CFLAGS) $(libtasn1_CFLAGS) $(LFS_CFLAGS)
AM_LDFLAGS = $(libgnutls_LIBS) $(libtasn1_LIBS) $(libpthread_LIBS) $(libplist_LIBS)

if ENABLE_DEVTOOLS
noinst_PROGRAMS = ideviceclient afccheck filerelaytest housearresttest lckd-client

ideviceclient_SOURCES = ideviceclient.c
ideviceclient_CFLAGS = $(AM_CFLAGS)
ideviceclient_LDFLAGS = $(AM_LDFLAGS)
ideviceclient_LDADD = ../src/libimobiledevice.la

lckd_client_SOURCES = lckdclient.c
lckd_client_CFLAGS = $(AM_CFLAGS) $(libglib2_CFLAGS)
lckd_client_LDFLAGS = -lreadline $(AM_LDFLAGS) $(libglib2_LIBS)
lckd_client_LDADD = ../src/libimobiledevice.la

afccheck_SOURCES = afccheck.c
afccheck_CFLAGS = $(AM_CFLAGS)
afccheck_LDFLAGS = $(AM_LDFLAGS)
afccheck_LDADD = ../src/libimobiledevice.la

filerelaytest_SOURCES = filerelaytest.c
filerelaytest_CFLAGS = $(AM_CFLAGS)
filerelaytest_LDFLAGS = $(AM_LDFLAGS)
filerelaytest_LDADD = ../src/libimobiledevice.la

housearresttest_SOURCES = housearresttest.c
housearresttest_CFLAGS = $(AM_CFLAGS)
housearresttest_LDFLAGS = $(AM_LDFLAGS)
housearresttest_LDADD = ../src/libimobiledevice.la

endif # ENABLE_DEVTOOLS

EXTRA_DIST = ideviceclient.c lckdclient.c afccheck.c filerelaytest.c housearresttest.c
