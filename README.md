# wlanpi-bridge

Mode to bridge WLAN Pi interfaces

## Requirement

Create a mode that will create a bridge interface using networkd and attach the following interfaces to the bridge:

 - eth0 (physical interface on WLAN Pi)
 - eth1 (interface created when iPhone attached via USB)
 - usb0 (interface created when Android phone connected)

The main use-case for this mode is to allow a phone's data connection to be shared with a device hanging off eth0 of a WLAN Pi.
 