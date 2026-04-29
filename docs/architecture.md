# Firmware Architecture

## Project type

This code is **Arduino-style C++ firmware** for RP2040 (Pico/Pico W), not Pico SDK-native C.

## Repository layout

- `src/main.cpp` → application logic (`setup()` / `loop()`)
- `include/` → reserved for future headers (currently unused)
- `docs/wiring.md` → hardware connectivity and GPIO map
- `docs/architecture.md` → architecture and behavior summary
- `README.md` → quick start and usage

## Main runtime flow (`src/main.cpp`)

1. **Static definitions**
   - 4x4 key map (`keys`)
   - LED GPIO list (`ledPins`)
   - keypad row/column GPIO lists (`rowPins`, `colPins`)
2. **Initialization in `setup()`**
   - Configure all LED pins as output
   - Initialize all LEDs OFF
3. **Polling loop in `loop()`**
   - Read keypad key via `keypad.getKey()`
   - If a key is pressed, run `switch` action:
     - `1..8`: turn on corresponding blue LED
     - `9`: turn on blue LED bank (`1..8`)
     - `0`: turn off blue LED bank (`1..8`)
     - `A..D`: turn on corresponding red LED
     - `*`: turn on red LED bank (`A..D`)
     - `#`: turn off red LED bank (`A..D`)
   - Delay 10 ms

## Behavior-preservation notes

- Core logic was kept unchanged while reorganizing into `src/main.cpp`.
- No Wi-Fi API is used, even though target hardware is Pico W.
- No credentials are required.
