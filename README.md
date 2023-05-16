# USB Mouse to XAC Joystick

Translate USB mouse/trackball to USB joystick compatible with Xbox Adaptive
Controller. A Kensington trackball works well with this program. A large
trackball can be operated by foot, wrist, elbow, etc.

## Hardware

For Adafruit RP2040 Feather USB Host board. The board supports USB host
and device at the same time. Lots more information at https://learn.adafruit.com/adafruit-feather-rp2040-with-usb-type-a-host.

* Adafruit Feather RP2040 with USB Type A Host

## Dependencies

Use this board package.

* https://github.com/earlephilhower/arduino-pico

The following libraries can be installed using the IDE library manager.

* "Adafruit TinyUSB Library" by Adafruit
* "Pico PIO USB" by sekigon-gonnoc

The next must be downloaded as a ZIP file. Use the IDE "Add .ZIP Library" to
install it.

* https://github.com/touchgadget/flight_stick_tinyusb

## IDE Tools options required

* Set "Board" to "Adafruit Feather RP2040 USB Host"
* Set "USB Stack" to "Adafruit TinyUSB"
* Set "CPU Speed" to 120MHz.
