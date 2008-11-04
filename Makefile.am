NULL =

SUBDIRS = cards glines gnobots2 gnometris iagno mahjongg same-gnome

EXTRA_DIST = \
	autogen.sh	\
	MAINTAINERS	\
	AUTHORS		\
	ChangeLog.pre-2-24 \
	$(NULL)

DISTCHECK_CONFIGURE_FLAGS = --enable-old

if !ENABLE_OLD
dist-hook:
	@echo You need to build with --enable-old in order to make dist
	@false
endif

# Build ChangeLog from GIT or SVN history
# (SVN r69 was the first ChangeLog-less checkin).
# Only build this when in a git or svn checkout.

ChangeLog:
	@if test -f $(top_srcdir)/.git/HEAD; then \
		git log --stat > $@; \
	elif test -f $(top_srcdir)/.svn/entries; then \
		svn log -v --xml -r HEAD:69 $(SVN_ROOT)/$(SVN_MODULE)/$(SVN_BRANCH) | \
			xsltproc --stringparam strip-prefix "$(SVN_MODULE)/$(SVN_BRANCH)" \
				 --stringparam include-rev "yes" $(top_srcdir)/svn2cl.xsl - > $@; \
	fi

dist: ChangeLog

.PHONY: ChangeLog
