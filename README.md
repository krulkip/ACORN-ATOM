# ACORN-ATOM
CYD emulator for ACORN ATOM
# Acorn Atom Emulator on ESP32 (CYD)

A lightweight Acorn Atom emulator running on an ESP32 with a Cheap Yellow Display (CYD), using a software 6502 CPU core.

## Features

- 6502 CPU emulation
- Original Atom ROM support (BASIC, FP, Kernel)
- Text-mode display (32x16)
- Serial keyboard input
- Optimized for ESP32 + TFT_eSPI

## Architecture

### CPU
Software emulation of the 6502 processor executing instructions from emulated RAM.

### Memory Map

| Address Range | Purpose |
|--------------|--------|
| $0000–$7FFF | RAM |
| $8000–$81FF | Video RAM |
| $C000–$CFFF | BASIC ROM |
| $D000–$DFFF | FP ROM |
| $F000–$FFFF | Kernel ROM |

### Video

- 32x16 characters
- Memory-mapped at $8000
- Custom ASCII mapping

### Input

Serial input mapped to Atom OS input routines.

## Build

- Arduino IDE
- ESP32 board support
- TFT_eSPI configured for ST7789

## Status

Stable version: V038

## Future Work

- Keyboard matrix emulation
- Sound
- Graphics
- File loading

