# Wiring and GPIO Mapping (Raspberry Pi Pico W)

## Components (derived from `diagram.json`)

- 1x Raspberry Pi Pico / Pico W (`wokwi-pi-pico`)
- 1x 4x4 membrane keypad (`wokwi-membrane-keypad`)
- 12x LEDs (`wokwi-led`)
  - 8 blue LEDs labeled `1..8`
  - 4 red LEDs labeled `A..D`
- 12x 220Ω series resistors for LEDs (`r1..r12`)
- 4x 1kΩ pull-up resistors for keypad rows (`rp1..rp4`)
- Shared GND for all LED cathodes
- 3V3 rail tied to the keypad row pull-up network

## GPIO pin mapping

### Keypad matrix

| Keypad Signal | Pico W GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

### LED outputs (from firmware `ledPins[]`)

| Logical LED | GPIO | Wokwi LED label |
|---|---:|---|
| ledPins[0] | GP11 | 1 |
| ledPins[1] | GP10 | 2 |
| ledPins[2] | GP9  | 3 |
| ledPins[3] | GP8  | 4 |
| ledPins[4] | GP7  | 5 |
| ledPins[5] | GP6  | 6 |
| ledPins[6] | GP5  | 7 |
| ledPins[7] | GP4  | 8 |
| ledPins[8] | GP3  | A |
| ledPins[9] | GP2  | B |
| ledPins[10] | GP28 | C |
| ledPins[11] | GP27 | D |

## Electrical notes

- Every LED anode is driven by a GPIO through a 220Ω resistor.
- Every LED cathode returns to GND.
- Keypad rows use external 1kΩ pull-ups to 3V3 (`R1..R4` lines), matching the diagram.
- UART monitor is connected to GP0/GP1 in Wokwi, but this firmware does not print serial logs.
