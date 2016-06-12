# iOS Development

## 1. Lazy fix to try HTTP url request (Apple tighten the security to enforce HTTPS request)
Add the following entry into the Info.plist
```xml
<key>NSAppTransportSecurity</key>
<dict>
  <!--Include to allow all connections (DANGER)-->
  <key>NSAllowsArbitraryLoads</key>
      <true/>
</dict>
```

# OSX

## 1. Making a bootable USB from ISO file
http://borgstrom.ca/2010/10/14/os-x-bootable-usb.html

# Ubuntu 14.04 Setup

## 1. Enable Loopback playback from Line-In
```
pactl load-module module-loopback
```

## 2. Connecting Apple Keyboard & Trackpad
```
sudo apt-get install bluez-compat

hcitool scan
# Copy the physical address of the keyboard

hciconfig
# Copy the Bluetooth adapter name

bluez-simple-agent <bluetooth interface name> <Apple Keyboard physical address>

hidd --connect <Apple Keyboard physical address>
```
