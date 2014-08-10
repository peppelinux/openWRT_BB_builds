NinucsWRT revision 41591 BarrierBraker for very cheap router tl-wr841nd
=========

OpenWRT customization designed for Calabria Ninux.org needs, mostly used for my configurations.
This firmware is the results of experimentation and brain crushing with Ninux.org guys, please share and enjoy as it come. Its Configuration could be used with BB sources

git clone https://github.com/openwrt-es/barrier-breaker-openwrt.git

cd barrier-breaker-openwrt

scripts/feeds update && scripts/feeds install olsrd && scripts/feeds install luci && scripts/feeds install openvpn

cp ../config_base_busybox_olsrd_luciccl_tc_openvpnclient-server_pptp .config

make menuconfig

make V=99 -j 4

In this special flavour I decided to include all theese...

    base-files_155-r41591_ar71xx.ipk
    busybox_1.22.1-2_ar71xx.ipk
    dnsmasq_2.71-3_ar71xx.ipk
    dropbear_2014.63-1_ar71xx.ipk
    firewall_2014-07-10a_ar71xx.ipk
    fstools_2014-06-22-e0430f5c62f367e5a8e02755412977b02c3fc45e_ar71xx.ipk
    hostapd-common_2014-06-03-1_ar71xx.ipk
    ip6tables_1.4.21-1_ar71xx.ipk
    iptables_1.4.21-1_ar71xx.ipk
    iw_3.15-1_ar71xx.ipk
    iwinfo_49_ar71xx.ipk
    jshn_2014-06-24-39a8fae44186c074265482a09eaa8465334f8183_ar71xx.ipk
    jsonfilter_2014-06-19-cdc760c58077f44fc40adbbe41e1556a67c1b9a9_ar71xx.ipk
    kmod-ath9k-common_3.10.44+2014-05-22-1_ar71xx.ipk
    kmod-ath9k_3.10.44+2014-05-22-1_ar71xx.ipk
    kmod-ath_3.10.44+2014-05-22-1_ar71xx.ipk
    kmod-cfg80211_3.10.44+2014-05-22-1_ar71xx.ipk
    kmod-crypto-aes_3.10.44-1_ar71xx.ipk
    kmod-crypto-arc4_3.10.44-1_ar71xx.ipk
    kmod-crypto-core_3.10.44-1_ar71xx.ipk
    kmod-crypto-ecb_3.10.44-1_ar71xx.ipk
    kmod-crypto-hash_3.10.44-1_ar71xx.ipk
    kmod-crypto-manager_3.10.44-1_ar71xx.ipk
    kmod-crypto-pcompress_3.10.44-1_ar71xx.ipk
    kmod-crypto-sha1_3.10.44-1_ar71xx.ipk
    kmod-gpio-button-hotplug_3.10.44-1_ar71xx.ipk
    kmod-gre_3.10.44-1_ar71xx.ipk
    kmod-ip6tables_3.10.44-1_ar71xx.ipk
    kmod-ipt-conntrack_3.10.44-1_ar71xx.ipk
    kmod-ipt-core_3.10.44-1_ar71xx.ipk
    kmod-ipt-nat_3.10.44-1_ar71xx.ipk
    kmod-ipt-nathelper_3.10.44-1_ar71xx.ipk
    kmod-iptunnel_3.10.44-1_ar71xx.ipk
    kmod-ipv6_3.10.44-1_ar71xx.ipk
    kmod-lib-crc-ccitt_3.10.44-1_ar71xx.ipk
    kmod-mac80211_3.10.44+2014-05-22-1_ar71xx.ipk
    kmod-mppe_3.10.44-1_ar71xx.ipk
    kmod-ppp_3.10.44-1_ar71xx.ipk
    kmod-pppoe_3.10.44-1_ar71xx.ipk
    kmod-pppox_3.10.44-1_ar71xx.ipk
    kmod-pptp_3.10.44-1_ar71xx.ipk
    kmod-sched-core_3.10.44-1_ar71xx.ipk
    kmod-slhc_3.10.44-1_ar71xx.ipk
    kmod-tun_3.10.44-1_ar71xx.ipk
    libblobmsg-json_2014-06-24-39a8fae44186c074265482a09eaa8465334f8183_ar71xx.ipk
    libgcc_4.8-linaro-1_ar71xx.ipk
    libip4tc_1.4.21-1_ar71xx.ipk
    libip6tc_1.4.21-1_ar71xx.ipk
    libiwinfo-lua_49_ar71xx.ipk
    libiwinfo_49_ar71xx.ipk
    libjson-c_0.11-2_ar71xx.ipk
    libjson-script_2014-06-24-39a8fae44186c074265482a09eaa8465334f8183_ar71xx.ipk
    liblua_5.1.5-1_ar71xx.ipk
    liblzo_2.06-1_ar71xx.ipk
    libnl-tiny_0.1-3_ar71xx.ipk
    libpolarssl_1.3.7-1_ar71xx.ipk
    libpthread_0.9.33.2-1_ar71xx.ipk
    libubox_2014-06-24-39a8fae44186c074265482a09eaa8465334f8183_ar71xx.ipk
    libubus-lua_2014-07-03-f688c7ad0b2435a89bfd13f5496cabf596b54c8f_ar71xx.ipk
    libubus_2014-07-03-f688c7ad0b2435a89bfd13f5496cabf596b54c8f_ar71xx.ipk
    libuci-lua_2014-04-11.1-1_ar71xx.ipk
    libuci_2014-04-11.1-1_ar71xx.ipk
    libustream-polarssl_2014-03-25-fc0b5ec804ee43c532978dd04ab0509c34baefb0_ar71xx.ipk
    libxtables_1.4.21-1_ar71xx.ipk
    lua_5.1.5-1_ar71xx.ipk
    luci-app-firewall_svn-r10472-1_ar71xx.ipk
    luci-base_svn-r10472-1_ar71xx.ipk
    luci-lib-nixio_svn-r10472-1_ar71xx.ipk
    luci-mod-admin-full_svn-r10472-1_ar71xx.ipk
    luci-proto-ppp_svn-r10472-1_ar71xx.ipk
    luci-ssl_svn-r10472-1_ar71xx.ipk
    luci-theme-bootstrap_svn-r10472-1_ar71xx.ipk
    luci_svn-r10472-1_ar71xx.ipk
    mtd_20_ar71xx.ipk
    netifd_2014-06-29-77206574a21d406f6098b604c6e0774116afdb91_ar71xx.ipk
    odhcp6c_2014-06-04-26c5466e626735f27dd073b727b02612c5a807cd_ar71xx.ipk
    odhcpd_2014-07-01-4267915aef64aae345972c77148b11759a172b14_ar71xx.ipk
    olsrd-mod-arprefresh_0.6.6.2-4_ar71xx.ipk
    olsrd-mod-dyn-gw-plain_0.6.6.2-4_ar71xx.ipk
    olsrd-mod-dyn-gw_0.6.6.2-4_ar71xx.ipk
    olsrd-mod-mdns_0.6.6.2-4_ar71xx.ipk
    olsrd-mod-nameservice_0.6.6.2-4_ar71xx.ipk
    olsrd-mod-txtinfo_0.6.6.2-4_ar71xx.ipk
    olsrd_0.6.6.2-4_ar71xx.ipk
    openvpn-nossl_2.3.4-1_ar71xx.ipk
    opkg_9c97d5ecd795709c8584e972bfdf3aee3a5b846d-7_ar71xx.ipk
    ppp-mod-pppoe_2.4.6-1_ar71xx.ipk
    ppp-mod-pptp_2.4.6-1_ar71xx.ipk
    ppp_2.4.6-1_ar71xx.ipk
    procd_2014-07-02-619ec82ececcbe9b9d1ca18ac6bc7c5c68c96825_ar71xx.ipk
    px5g_1_ar71xx.ipk
    resolveip_2_ar71xx.ipk
    swconfig_10_ar71xx.ipk
    tc_3.15.0-1_ar71xx.ipk
    uboot-envtools_2014.04-4_ar71xx.ipk
    ubox_2014-05-30-c3d4118eee505f41c4d20a87f326479530837569_ar71xx.ipk
    ubus_2014-07-03-f688c7ad0b2435a89bfd13f5496cabf596b54c8f_ar71xx.ipk
    ubusd_2014-07-03-f688c7ad0b2435a89bfd13f5496cabf596b54c8f_ar71xx.ipk
    uci_2014-04-11.1-1_ar71xx.ipk
    uhttpd-mod-ubus_2014-06-11-dabd7dea6445aaa0e5b8d9add1872fa7393b3a85_ar71xx.ipk
    uhttpd_2014-06-11-dabd7dea6445aaa0e5b8d9add1872fa7393b3a85_ar71xx.ipk
    wpad-mini_2014-06-03-1_ar71xx.ipk

luci and openvpn also have SSL support, I also included pptp for windows stupid-legacy-costrinctions.

