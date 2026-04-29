# Raspberry Pi Pico W Keypad-to-LED Controller

Arduino-style RP2040 firmware for a **Raspberry Pi Pico W** that reads a 4x4 membrane keypad and drives 12 LEDs.

## Features

- 4x4 keypad scan through `Keypad` library
- 12 independent LED outputs
- Group control shortcuts:
  - `9` = ON all blue LEDs (`1..8`)
  - `0` = OFF all blue LEDs (`1..8`)
  - `*` = ON all red LEDs (`A..D`)
  - `#` = OFF all red LEDs (`A..D`)
- No Wi-Fi usage (Pico W wireless remains unused)

## Repository structure

```text
.
├── CMakeLists.txt
├── README.md
├── docs/
│   ├── architecture.md
│   └── wiring.md
├── include/
└── src/
    └── main.cpp
```

## Hardware summary

See full mapping in [`docs/wiring.md`](docs/wiring.md).

- Board: Raspberry Pi Pico / Pico W
- Input: 1x 4x4 membrane keypad
- Output: 12x LEDs via 220Ω resistors
- Pull-ups: 4x 1kΩ on keypad rows to 3V3

## Build/flash options

> Important: The firmware uses Arduino APIs (`setup`, `loop`, `digitalWrite`, `Keypad.h`).
> Build using an RP2040 Arduino core (Arduino IDE / Arduino CLI), not Pico SDK-native examples.

### Option A: Wokwi (quickest)

1. Create a new Wokwi Raspberry Pi Pico project.
2. Paste `src/main.cpp` into the sketch file.
3. Use the provided `diagram.json` as the circuit.
4. Start simulation and press keypad buttons.

### Option B: Real Pico W (Arduino IDE)

1. Install Arduino IDE 2.x.
2. Install RP2040 board package (e.g., Earle Philhower core).
3. Install **Keypad** library from Library Manager.
4. Create/open sketch and paste `src/main.cpp` content.
5. Select board: **Raspberry Pi Pico W**.
6. Put board in BOOTSEL mode, select serial/UF2 target, and upload.

## Pin behavior reference

- Blue bank (`1..8`) → GP11, GP10, GP9, GP8, GP7, GP6, GP5, GP4
- Red bank (`A..D`) → GP3, GP2, GP28, GP27
- Keypad columns → GP19..GP16
- Keypad rows → GP26, GP22, GP21, GP20

## Wi-Fi and secrets

This project does **not** use Wi-Fi, sockets, or cloud APIs. No credentials are needed or stored.
