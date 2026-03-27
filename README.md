# Acorn Atom Emulator on ESP32 (CYD)

Work in progress. Basically working but still errors. eg delete key not working etc.
A lightweight Acorn Atom emulator running on an ESP32 with a Cheap Yellow Display (CYD), using a software 6502 CPU core.
I used a Guiton JC2432W328 which has CST820 capacitive touch screen and ST7789 video chip.

## Features
- 6502 CPU emulation nbased on the Bitboard one https://github.com/SMDHuman/bitboard_6502
- Original Atom ROM support (BASIC, FP, Kernel)
- Text-mode display (32x16)
- Serial keyboard input
- Optimized for ESP32 + TFT_eSPI

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

