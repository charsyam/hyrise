hyr-server := $(realpath $(dir $(lastword $(MAKEFILE_LIST))))

include $(hyr-server)/../../../rules.mk

include $(PROJECT_ROOT)/src/lib/access/Makefile
include $(PROJECT_ROOT)/src/lib/net/Makefile
-include $(PROJECT_ROOT)/extensions/Makefile # may fail

hyr-server.binname := hyrise-server
hyr-server.deps := hyr-access extensions
hyr-server.libs := boost_program_options
$(eval $(call full_link_binary,hyr-server))

all: $(hyr-server.binary)
