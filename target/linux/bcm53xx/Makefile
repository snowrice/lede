# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (C) 2013 OpenWrt.org

include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=bcm53xx
BOARDNAME:=Broadcom BCM47xx/53xx (ARM)
FEATURES:=squashfs nand usb pci pcie gpio pwm
CPU_TYPE:=cortex-a9
SUBTARGETS:=generic

KERNEL_PATCHVER:=6.6
KERNEL_TESTING_PATCHVER:=6.1

define Target/Description
	Build firmware images for Broadcom based BCM47xx/53xx routers with ARM CPU, *not* MIPS.
endef

include $(INCLUDE_DIR)/target.mk

KERNELNAME:=zImage dtbs

DEFAULT_PACKAGES += nvram \
	osafeloader oseama otrx \
	kmod-gpio-button-hotplug \
	kmod-leds-gpio

$(eval $(call BuildTarget))
