# ArduinoMDNS2

Fixed bugs in:
- memory allocation in the mDNS service record function (`addServiceRecord`). See source: https://github.com/arduino-libraries/ArduinoMDNS/pull/23;
- insufficient memory allocation for the number of characters in the text WITHOUT the terminating null character. See source: https://github.com/arduino-libraries/ArduinoMDNS/issues/36;
- The service query message attaches some data that should not be transmitted. See source: https://github.com/arduino-libraries/ArduinoMDNS/pull/8;

[![Check Arduino status](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/check-arduino.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/check-arduino.yml)
[![Compile Examples status](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/compile-examples.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/compile-examples.yml)
[![Spell Check status](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/spell-check.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoMDNS/actions/workflows/spell-check.yml)

mDNS library for Arduino. Based on [@TrippyLighting](https://github.com/TrippyLighting)'s [EthernetBonjour](https://github.com/TrippyLighting/EthernetBonjour) library.

Supports mDNS (registering services) and DNS-SD (service discovery).

## Requirements

Any Arduino core and networking library that supports the new `virtual` `UDP::beginMulticast(...)` method, including:

 * AVR core 1.6.18 or later (bundled with IDE 1.8.2 and later) for AVR boards
 * SAMD core 1.6.13 or later for SAMD boards
 * Arduino Ethernet and WiFi101 libraries
