#
# Copyright (C) 2011-2015 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

all: .done

.done:
	patch -d $(TOP) -p3 -i $(CURDIR)/fix-path.patch
	cp -f ./500-system-profile.patch ../../../openwrt_trunk/feeds/packages/utils/bash/patches/
	rm -f ../../../openwrt_trunk/feeds/packages/utils/bash/patches/200-redhat-parser-oob.patch
	rm -f ../../../openwrt_trunk/feeds/packages/utils/bash/patches/201-redhat-variable-affix.patch
	@touch $@

clean:
	@rm -f .done

.PHONY: clean
