cmake_minimum_required(VERSION 3.13)

project(pico-w-keypad-led C CXX ASM)

# Note:
# This repository contains Arduino-style firmware (setup/loop and Keypad.h).
# Build with an RP2040-capable Arduino core/toolchain (e.g., Earle Philhower core)
# rather than the Pico SDK-native flow.

add_custom_target(info ALL
  COMMAND ${CMAKE_COMMAND} -E echo "Use Arduino IDE or Arduino CLI to build src/main.cpp"
)
