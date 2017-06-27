#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=sshpass
PKG_VERSION:=1.05
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@SF/sshpass
PKG_MD5SUM:=c52d65fdee0712af6f77eb2b60974ac7

include $(INCLUDE_DIR)/package.mk

define Package/sshpass
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=sshpass
  URL:=Non-interactive SSH authenticator
endef

define Package/sshpass/description
       Sshpass is a tool for non-interactivly performing password authentication with SSH's
endef

define Build/Compile
	$(call Build/Compile/Default,sshpass)
endef

define Package/sshpass/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/sshpass $(1)/usr/bin/
endef

$(eval $(call BuildPackage,sshpass))
