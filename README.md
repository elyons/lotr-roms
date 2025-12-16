# Commands for minipro:

# Process to read chip with minipro
* Install minipro: https://gitlab.com/DavidGriffith/minipro/
* Make sure minipro is seen on USB devices
  ```
  lsusb
  ```
* Determine correct chip type by looking at the top of the chip (often under a sticker)
* Search minipro database for correct chip.  Use:
  ```
  minipro -L M27C4001
  ```
  which returns:
  ```
Found TL866CS 03.2.86 (0x256)
Device code: 53132168
Serial code: 08428995D581BE8F644B4F75
USB speed: 12Mbps (USB 1.1)
MBM27C4001
MBM27C4001@PLCC32
MBM27C4001@TSOP32
M27C4001@DIP32
M27C4001@PLCC32
M27C4001@TSOP32
M27C4001@DIP32
M27C4001@PLCC32
M27C4001@TSOP32
  ```
* Select the base or one that ends with "@DIP32" if you are using a DIP chip.

# burn GAL16V8D chip: 
```
minipro -p GAL16V8D -w GOLD-PAL-U213.jed
```


