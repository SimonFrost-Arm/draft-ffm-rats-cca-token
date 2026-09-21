.DEFAULT_GOAL := check
MAKECMDGOALS ?= $(.DEFAULT_GOAL)

SUBDIRS := platform
SUBDIRS += realm
SUBDIRS += device
SUBDIRS += top

$(MAKECMDGOALS): ; for d in $(SUBDIRS) ; do $(MAKE) -C $$d $@ ; done
