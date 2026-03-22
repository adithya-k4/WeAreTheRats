# v1 firmware

This folder contains the Arduino sketch and local source files for the `v1`
firmware.

## Current IMU / input configuration

The current `v1` configuration is set up for:

- `BNO085` enabled
- `IMU_LSM6DS3` disabled
- touch sensor on `D3` (`MOUSE_LEFT`), active high
- touch sensor on `D6` (`MOUSE_ACTIVATE`), active high
- push button on `D10` (`KEYPAD_ACTIVATE`), active low

See `local_constants.h` for the active pin assignments and compile-time flags.

## How to flash it to the board

This is Arduino firmware, so you do **not** run the ZIP file directly.

1. Download or clone the repository.
2. If you downloaded a ZIP, extract it.
3. Open `v1/WeAreTheRats.ino` in the Arduino IDE.
4. Keep the entire `v1/` folder together, since the sketch depends on the
   local source files in this directory.
5. Select your XIAO board and serial/USB port.
6. Install any missing Arduino libraries reported by the IDE.
7. Click **Upload**.

## Dependencies

The sketch includes external Arduino libraries such as:

- `bluefruit.h`
- `TensorFlowLite.h`

The BNO085 support files used by this sketch are vendored in this folder,
including `Adafruit_BNO08x.*`, `sh2*`, and `shtp*`.
