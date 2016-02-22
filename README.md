# My Notes

1. Enable Loopback playback from Line-In
```
pactl load-module module-loopback
```

2. Connecting Apple Keyboard
```
sudo apt-get install bluez-compat

hcitool scan
# Copy the physical address of the keyboard

hciconfig
# Copy the Bluetooth adapter name

bluez-simple-agent <bluetooth interface name> <Apple Keyboard physical address>

hidd --connect <Apple Keyboard physical address>
```
