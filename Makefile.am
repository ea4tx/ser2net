sbin_PROGRAMS = ser2net
ACLOCAL_AMFLAGS = -I m4
AM_CFLAGS=-Wall -I$(top_srcdir)
AM_CPPFLAGS = -DSYSCONFDIR="\"${sysconfdir}\"" -DDATAROOT="\"${datarootdir}\""
ser2net_SOURCES = controller.c dataxfer.c readconfig.c \
	ser2net.c led.c led_sysfs.c yamlconf.c auth.c
ser2net_LDADD = -lgensio -lyaml $(OPENSSL_LIBS)
noinst_HEADERS = controller.h dataxfer.h readconfig.h \
	ser2net.h led.h led_sysfs.h absout.h
man_MANS = ser2net.8 ser2net.yaml.5
EXTRA_DIST = $(man_MANS) ser2net.yaml ser2net.spec ser2net.init

SUBDIRS = tests

DIST_SUBDIRS = $(SUBDIRS)
