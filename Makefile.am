NULL =

SUBDIRS= cards glines gnobots2 gnometris iagno mahjongg same-gnome

EXTRA_DIST = \
	autogen.sh	\
	MAINTAINERS	\
	AUTHORS		\
	$(NULL)

DISTCHECK_CONFIGURE_FLAGS = --enable-old

if !ENABLE_OLD
dist-hook:
	@echo You need to build with --enable-old in order to make dist
	@false
endif
