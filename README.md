
# Graduation Project: [Project Name]
> Based on the predecessor: **TCG Life Counter**

## Project Overview
Ten projekt to zaawansowany licznik punktów życia do gier karcianych (TCG), będący ewolucją modelu TCG Life Counter. Głównym celem jest optymalizacja mechaniczna i elektroniczna urządzenia, ze szczególnym uwzględnieniem miniaturyzacji (limit wysokości komponentów H < 3mm) oraz poprawy kultury pracy interfejsu użytkownika.

## Author
* **kocurel** - *Initial Work / Lead Developer*

## Versioning
Currently: **v0.0.5** (Power delivery changes, schematic cleanup, LCD pin labeling, switching to a 100 pin STM32)
**v0.0.4** (Minor fix) 
**v0.0.3** (MCU power delivery circuit) 
**v0.0.2** (Backlight power circuit)
**v0.0.1** (Initial Draft)

## Hardware Architecture & Design Decisions
Projekt charakteryzuje się specyficznymi rozwiązaniami inżynierskimi wymuszonymi przez ciasną obudowę:

### 1. Power Management (Backlight)
Zasilanie podświetlenia LCD zostało zrealizowane w oparciu o przetwornicę **AP3012** w konfiguracji **Constant Current**:
- **Current Stabilization:** Zastosowano *Low-Side Sensing* z rezystorem pomiarowym **82 Ohm**, co wymusza stabilny prąd **15.24 mA** dla diod LED.
- **BOM Optimization:** Wszystkie kondensatory filtrujące zostały ujednolicone do modelu **Samsung CL21B105KBFNNNE** (1uF, 50V, 0805) w celu eliminacji efektu *DC Bias*.
- **Brightness Control:** Sterowanie jasnością odbywa się przez pin **SHDN** przy użyciu sygnału PWM (zalecana f: 200Hz - 1kHz).

### 2. UI & Mechanicals
- **Tactile Switches:** Przejście na model **Omron B3F-4050** (130gf) w celu redukcji hałasu i poprawy ergonomii nacisku.
- **Stack-up:** Maksymalna wysokość komponentów pod wyświetlaczem wynosi **1.5 mm**, co zapewnia bezpieczny margines wewnątrz profilu 3 mm.

## Project Structure
- `/hardware` - Pliki projektowe KiCad 9.0 (Schematy, PCB, Biblioteki).
- `/docs` - Dokumentacja techniczna i analizy porównawcze:
    - `backlight_analysis.txt` - szczegółowa analiza pętli FB i doboru kondensatorów.
    - `switch_analysis.txt` - porównanie parametrów akustycznych przełączników.
- `/firmware` - Kod źródłowy mikrokontrolera (C/C++).

## Getting Started
### Prerequisites
- **KiCad 9.0+** (wymagany do otwarcia najnowszych plików `.kicad_pro`).

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
