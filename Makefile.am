NULL =

SUBDIRS = cards glines gnobots2 gnometris iagno mahjongg same-gnome

EXTRA_DIST = \
	autogen.sh	\
	AUTHORS		\
	ChangeLog.pre-2-24 \
	gnome-games-extra-data.doap \
	$(NULL)

DISTCHECK_CONFIGURE_FLAGS = --disable-silent-rules

# Build ChangeLog from GIT or SVN history
# (SVN r69 was the first ChangeLog-less checkin).
# Only build this when in a git or svn checkout.

ChangeLog:
	$(AM_V_GEN) if test -f $(top_srcdir)/.git/HEAD; then \
		git log --stat > $@; \
	fi

dist: ChangeLog

.PHONY: ChangeLog
