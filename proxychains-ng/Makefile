#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=proxychains-ng
PKG_VERSION:=4.12
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=HEAD
PKG_SOURCE_URL:=https://github.com/rofl0r/proxychains-ng
PKG_SOURCE_SUBDIR:=$(PKG_NAME)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_RELEASE).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/proxychains-ng
	SECTION:=net
	CATEGORY:=Network
	TITLE:=ProxyChains New Generation
	DEPENDS:=+libpthread
	SUBMENU:=Web Servers/Proxies
endef

define Build/Configure
endef

define Build/Compile
	$(call Build/Compile/Default)
endef

define Package/proxychains-ng/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/proxychains4 $(1)/usr/bin/proxychains4
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/libproxychains4.so $(1)/usr/lib/libproxychains4.so
	$(INSTALL_DIR) $(1)/etc
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/proxychains.conf $(1)/etc/proxychains.conf
endef
	
$(eval $(call BuildPackage,proxychains-ng))
