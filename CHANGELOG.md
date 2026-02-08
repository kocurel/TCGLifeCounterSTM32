# Changelog


## [0.0.3] - 2026-02-08
### Added
- USB C symbol on the schematic and 3D model.
- STMicroelectronics ESDA25SC6Y TVS diode library.
- Samsung CL10A106KP8NNNC capacitor library.
- Microchip MCP73831T Li-Po charger library.
- Liteon LTST-C191KRKT red charging indicator LED library.
- Samsung CL10A475KP8NNNC 4.7uF capacitor library.

## [0.0.2] - 2026-02-07

### Added
- Documented switch comparison analysis (docs/switch_analysis.txt).
- Omron B3F-4050 tactile switch library.
- Diodes Incorporated AP3012KTR-E1 step-up (boost) converter library.
- TDK VLS3012CX-100M-1 inductor library.
- Diodes Incorporated 1N5819HWQ-7-F Schottky rectifying diode library.
- Samsung CL21B105KBFNNNE capacitor library.
- Documented backlight power stage analysis (docs/backlight_analysis.txt).

### Technical Notes (Backlight Power Completed)
- Topology: Low-side current sensing using AP3012 FB pin (Vref=1.25V).
- Target Current: 15.24mA (via 82R/0603 1% Sense Resistor).
- Brightness Control: PWM dimming implemented via SHDN pin (recommended freq: 200Hz - 1kHz).
- Mechanical Clearance: All components selected for H < 1.5mm to fit within the 3mm stack-up limit under the LCD.

# END OF CHANGELOG

## [0.0.1] - 2026-02-07

### Added
- Initial project structure.
- Datasheets and libraries for the display, the FPC connector and STM microcontroller
