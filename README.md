# USB Mouse to XAC Joystick

![XAC connected to Logitech trackball via Adafruit board](./images/mouse2xac.jpg)

Translate USB mouse/trackball to USB joystick compatible with Xbox Adaptive
Controller. A Kensington trackball works well with this program. A large
trackball can be operated by foot, wrist, elbow, etc. Be sure to use a
5 volt, 2 amp power supply on the XAC.

The Perixx PeriPad 501 glidepad now works. Only a light touch is required
to move the joystick.

Be sure to use the Xbox joystick calibration to make full use of the pointing
device (mouse, trackball, or glidepad).

Tested with XAC firmware version 5.17.3202.0 (updated on May 25, 2023).

## Hardware

For Adafruit RP2040 Feather USB Host board. The board supports USB host
and device at the same time. Lots more information at https://learn.adafruit.com/adafruit-feather-rp2040-with-usb-type-a-host.

* Adafruit Feather RP2040 with USB Type A Host

## The Easy Way

The latest code can be blasted into the Adafruit board without installing
the Arduino IDE, libraries, etc. Look for the UF2 file which is currently named
mouse2xac.ino.adafruit_feather_usb_host.uf2.

See the Adafruit tutorial to put the board in bootloader mode.
https://learn.adafruit.com/adafruit-feather-rp2040-with-usb-type-a-host/pinouts#buttons-and-rst-pin-3143253

Look for a USB drive named RPI-RP2. Drag and drop the UF2 file on the RPI-RP2
drive. Wait a few seconds for it finish. The board is now ready to be plugged
into an XAC. Skip the next section!

## The Hard Way

Install the Arduino IDE. Then install this board package.

* https://github.com/earlephilhower/arduino-pico

The following libraries must be installed using the IDE library manager.

* "Adafruit TinyUSB Library" by Adafruit
* "Pico PIO USB" by sekigon-gonnoc

The following library must be downloaded as a ZIP file. Use the IDE "Add .ZIP
Library" to install it.

* https://github.com/touchgadget/flight_stick_tinyusb

## IDE Tools options required

* Set "Board" to "Adafruit Feather RP2040 USB Host"
* Set "USB Stack" to "Adafruit TinyUSB"
* Set "CPU Speed" to 120MHz.

At this point compile and upload mouse2xac.ino.

WARNING: This program disables the USB CDC ACM serial port so use the BOOT
and RESET buttons to enter the bootloader before using the IDE to upload.

## Troubleshooting

The Adafruit USB host board does not always recognize USB devices when plugged
in to its type A connector. Try plugging the USB mouse/trackball into the
Adafruit board before plugging the Adafruit board into the XAC. This seems to
work better.

Some USB devices require the XAC be powered by a 5 volt, 2 amp power supply.
For example, the large Kensington trackball does not work without the power
supply.
