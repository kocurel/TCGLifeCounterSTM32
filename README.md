# STATUS: **WIP**

## Project: [TCGLifeCounterSTM32]
> Based on the predecessor: **TCGLifeCounterESP32**

## Project Overview
An advanced life counter for Trading Card Games (TCG), serving as an evolution of the TCG Life Counter model. The main focus is on mechanical and electronic optimization, specifically targeting miniaturization (component height limit H < 3mm) and UI tactile improvements.

## Versioning
- **v0.0.5**: Power delivery changes, schematic cleanup, LCD pin labeling, switching to a 100-pin STM32
- **v0.0.4**: Minor fix
- **v0.0.3**: MCU power delivery circuit
- **v0.0.2**: Backlight power circuit
- **v0.0.1**: Initial Draft

## Hardware Architecture & Design Decisions

### 1. Power Management (Backlight)
LCD backlight power delivery is based on the **AP3012** step-up converter in a **Constant Current** configuration:
- **Current Stabilization**: Implemented Low-Side Sensing with an **82 Ohm** sense resistor, forcing a stable **15.24 mA** current for the LEDs.
- **Brightness Control**: Managed via the **SHDN** pin using a PWM signal.

### 2. UI & Mechanicals
- **Tactile Switches**: Switched to **Omron B3F-4050** (130gf) to reduce noise and improve actuation ergonomics.
- **Stack-up**: Maximum component height under the display is **1.5 mm**, ensuring a safe clearance margin within the 3 mm profile.

## Project Structure
- `/hardware` - KiCad 9.0 project files (Schematics, PCB, Libraries).
- `/docs` - Technical documentation and comparative analyses:
    - `backlight_analysis.txt` - Detailed analysis of the FB loop and capacitor selection.
    - `switch_analysis.txt` - Comparison of switch acoustic parameters.
- `/firmware` - MCU source code (C/C++).

## Getting Started
### Prerequisites
- **KiCad 9.0+** (Required to open the latest `.kicad_pro` files).
# STATUS: **WIP**

## Project: [TCGLifeCounterSTM32]
> Based on the predecessor: **TCGLifeCounterESP32**


## Project Overview
Ten projekt to zaawansowany licznik punktów życia do gier karcianych (TCG), będący ewolucją modelu TCG Life Counter. Głównym celem jest optymalizacja mechaniczna i elektroniczna urządzenia, ze szczególnym uwzględnieniem miniaturyzacji (limit wysokości komponentów H < 3mm) oraz poprawy kultury pracy interfejsu użytkownika.

## Versioning
