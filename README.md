# DSPatch

DSPatch is a custom audio development board for experimenting with real-time digital signal processing, embedded audio, and guitar effects.

The board is built around an STM32H573 microcontroller and TLV320AIC3204 audio codec, with integrated analog audio I/O, power management, USB connectivity, and user controls.

> **Status:** Work in progress — initial schematic design

## Overview

DSPatch is intended to provide a reusable hardware platform for developing and testing embedded audio applications without relying on a commercial development board.

The basic signal path is:

**Instrument Input → Analog Front End → Audio Codec → STM32 DSP → Audio Codec → Analog Output**

The TLV320AIC3204 provides ADC/DAC conversion and interfaces with the STM32H573 for real-time digital audio processing.

## System Architecture

![DSPatch Block Diagram](docs/block-diagram.png)

## Hardware

The current design is divided into five schematic sections:

- **MCU** — STM32H573 processor, programming/debug, USB, and support circuitry
- **Codec** — TLV320AIC3204 audio codec and digital interface
- **Audio I/O** — instrument input/output, buffering, protection, and filtering
- **Power** — DC input protection and regulated supply rails
- **Controls** — user controls and external interfaces

PDF versions of the current schematics are available in [`hardware/schematics`](hardware/schematics).

## Project Goals

- Real-time audio DSP
- Guitar and instrument-level audio I/O
- USB programming and communication
- Flexible platform for developing digital audio effects
- Custom PCB suitable for hardware and firmware experimentation
- Accessible test points and expansion interfaces

## Documentation

Detailed design information, component selection, calculations, and design decisions are maintained separately in the project design documentation.

## Roadmap

- [x] Define system architecture
- [x] Select MCU and audio codec
- [ ] Complete schematic design and review
- [ ] PCB layout
- [ ] Prototype assembly and bring-up
- [ ] Codec and digital audio interface validation
- [ ] Analog performance testing
- [ ] DSP firmware and effects development

## License

TBD
