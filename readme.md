
# Zephyr ble hid usb translator
Abomination of code that proxies/translates HID from a Bluetooth device to a USB device so that USB keyboards/mice can be used with BIOS/UEFI.

To pair with your keyboard, simply flash this in a nrf52840 board
and it will auto pair with the first keyboard it finds

## How to unpair or re pair with a device

You can plug the USB to your computer leaving the user button pressed.
The device will blink 3 times and it will remove any pairing keys. You
can re pair with your device by putting it in pair mode.

Alternatively, you can flash the firmware with the line `#define RESET_PAIRS`
uncommented. It will delete any pair key and reset the device. Once you have
done that, comment the line and flash again.