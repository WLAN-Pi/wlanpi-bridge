# wlanpi-bridge (Bridge Mode)

Mode to bridge WLAN Pi interfaces

## Overview

Bridge mode that creates a bridge interface using networkd to configure network interfaces and attaches the following interfaces to the bridge interface:

 - eth0 (physical interface on WLAN Pi)
 - eth1 (interface created when iPhone attached via USB)
 - usb1 (interface created when Android phone connected)
 - wlan0 (first wireless NIC)
 - wlan1 (2nd wireless NIC, if present)

Bridge interface details:
 - br0 : DHCP cient

Network services used:
 - systemd/networkd
 - wpa_supplicant@wlan0.service
 - wpa_supplicant@wlan1.service

The main use-case for this mode is to allow a phone's data connection to be shared with a device hanging off eth0 of a WLAN Pi.

Use the front panel menu system of the WLAN Pi to switch between Classic mode and Bridge mode (Home > Modes > Bridge > Confirm) 

Once in bridge mode, the WLAN Pi may be accessed via:
 - OTG mode via usb0 (169.254.42.1)
 - br0 DHCP address


 