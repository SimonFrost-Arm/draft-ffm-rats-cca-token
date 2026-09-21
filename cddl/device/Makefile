include ../tools.mk
include ../check.mk
include frags.mk

check: check-device check-device-examples
.PHONY: check

clean: ; rm -f $(CLEANFILES)
.PHONY: clean

$(eval $(call cddl_check_template,device,$(DEVICE_FRAGS),$(DEVICE_EXAMPLES)))
