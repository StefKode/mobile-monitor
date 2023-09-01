# monitor
A script to monitor the data consumption for a teathered network interface (USB) on Linux

# Install
You should make sure to have a reliable network interface name when connecting your mobile device.

Recommended is to create a udev rule:

```
edit /etc/udev/rules.d/99-persistent-net.rules

# add:
SUBSYSTEM=="net", ACTION=="add", ATTRS{product}=="<product-device>", NAME="mobile0"

udevadm control --reload-rules
udevadm trigger
```
(source: https://unix.stackexchange.com/questions/750214/disable-udev-renaming-for-android-usb-tethering-using-randon-macs)
