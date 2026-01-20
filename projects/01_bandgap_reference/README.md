# Precision Bandgap Reference – SkyWater 130nm

This project implements a precision CMOS bandgap reference suitable for use in
power management units, data converters, PLLs, and mixed-signal SoCs.

The design follows a complete analog IP development flow:
specification → architecture → schematic → simulation → layout → LVS/DRC → results.

## Key Features
- ~1.2 V temperature-compensated reference
- Startup circuit for guaranteed power-on operation
- Designed and verified across PVT corners
- Layout with matching-aware techniques
- Open-source EDA toolchain

## Process and Tools
- Process: SkyWater 130nm CMOS
- Schematic: Xschem
- Simulation: Ngspice
- Layout: Magic, KLayout
- LVS/DRC: Netgen, Magic

## Status
Specification complete. Architecture and schematic design in progress.

