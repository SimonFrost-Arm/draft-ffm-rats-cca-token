include ../tools.mk
include ../check.mk

FRAGS := cca-top-claims.cddl
FRAGS += generic-sign1.cddl

include ../platform/frags.mk
include ../realm/frags.mk
include ../device/frags.mk

FRAGS += $(addprefix ../realm/,$(REALM_FRAGS))
FRAGS += $(addprefix ../platform/,$(PLATFORM_FRAGS))
FRAGS += $(addprefix ../device/,$(DEVICE_FRAGS))

check: check-top check-top-examples
.PHONY: check

clean: ; rm -f $(CLEANFILES)
.PHONY: clean

EXAMPLES := $(wildcard examples/*.diag)

$(eval $(call cddl_check_template,top,$(FRAGS),$(EXAMPLES)))
