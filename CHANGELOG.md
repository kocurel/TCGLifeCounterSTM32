# Changelog

## [0.0.5] - 2026-02-09
### Added 
- Kyocera AVX 06033D104KAT2A capacitor library.
- Murata GRM188R61E106KA73D capacitor library.
- Samsung CL21B106KOQNNNE capacitor library.
- Murata GRM188Z71C475KE21D capacitor library.
- Samsung CL10B104KB8NNNC capacitor library.
- Samsung CL10B105KO8NNNC capacitor library.
#### STM32
- Added a 100nF capacitor at every Vdd pin.

### Fixed
#### Li-Po charger
- Changed the capacitors of MCP73831T-2ATI_OT to match the schematic (increased the capacitance to 10uF).4

### Improved
#### Display backlight boost converter
- Changed the two 1uF capacitors from AP3012KTR-E1's output line to a 1uF 100nF pair.
- Added a 100nF capacitor on the input line

## [0.0.4] - 2026-02-08
### Fixed
- Added missing GND on AP3012KTR-E1.

## [0.0.3] - 2026-02-08
### Added
- USB C symbol on the schematic and 3D model.
- STMicroelectronics ESDA25SC6Y TVS diode library.
- Samsung CL10A106KP8NNNC capacitor library.
- Microchip MCP73831T Li-Po charger library.
- Liteon LTST-C191KRKT red charging indicator LED library.
- Samsung CL10A475KP8NNNC 4.7uF capacitor library.
- Diodes Incorporated AP2112K-3.3TRG1 LDO library.
- Kemet C0603C104K8RACTU 100nF capacitor library.
- Finished the mcu power delivery circuit.

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
