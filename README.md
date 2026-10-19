# Custom STM32F103 Development Board

A custom two-layer PCB designed in KiCad around the STM32F103C8T6 microcontroller. Inspired by the STM32 Blue Pill development board, this project focuses on custom hardware design, accessible debugging and peripheral connections, power regulation, clock circuitry, and PCB manufacturing preparation.

## Project Overview

The goal of this project was to design a custom STM32 development board from the schematic through PCB layout and manufacturing preparation. Using the Blue Pill as a reference point, I developed my own circuit schematic and PCB layout, making component-level design decisions to support programming, debugging, and external hardware integration.

I referenced STM32 datasheets, application notes, component documentation, and online hardware design resources to guide decisions involving power regulation, clock circuitry, USB connectivity, and analog power filtering.

## Key Features

- **Microcontroller:** STM32F103C8T6 ARM Cortex-M3
- **PCB Design:** Custom two-layer PCB designed in KiCad
- **Power Management:** USB Micro-B input and AMS1117-3.3 voltage regulation
- **Debugging and Expansion:** Accessible headers for development and external connections
- **Clock Circuitry:** 16 MHz external crystal oscillator with supporting components
- **Analog Power Filtering:** Ferrite bead for analog supply filtering
- **USB Connectivity:** USB Micro-B connector with supporting circuitry
- **Peripheral Access:** Headers for external connections and peripheral integration
- **Mechanical Design:** Mounting holes and rounded board corners
- **Design Validation:** KiCad Design Rules Checker (DRC)
- **Manufacturing Outputs:** Gerber files and NC drill data

## PCB Preview

<img width="1546" height="1242" alt="image" src="https://github.com/user-attachments/assets/05a38b3f-ab81-4a8f-8bb3-cb19a414bcc5" />
<img width="1830" height="1626" alt="image" src="https://github.com/user-attachments/assets/24a57296-e745-4fe2-92f7-f9a08d200814" />
<img width="1918" height="1358" alt="image" src="https://github.com/user-attachments/assets/c174e58e-6e41-438b-9353-fc6bad63a3e1" />

## Hardware Design

### Power Management

Designed the board's power circuitry around a USB Micro-B input and AMS1117-3.3 voltage regulator to provide a 3.3 V supply for the microcontroller. Integrated the supporting components and power connections into the schematic and PCB layout.

### Clock Circuitry

Integrated a 16 MHz external crystal oscillator and its supporting circuitry into the STM32 hardware design. Used microcontroller documentation and component references to guide the clock circuit implementation.

### Debugging and Peripheral Expansion

Designed accessible board headers to simplify connections to external hardware and support development and testing. These connections provide flexibility when integrating the microcontroller with peripherals and test equipment.

### USB Connectivity

Integrated a USB Micro-B connector and supporting circuitry into the custom design. This involved incorporating the relevant USB connections and associated components into the schematic and physical PCB layout.

### Analog Power Filtering

Incorporated a ferrite bead into the analog supply path to help attenuate high-frequency noise coupling into sensitive analog circuitry. This design choice reflects consideration of power integrity and analog signal quality at the PCB level.

### PCB Layout and Routing

Designed and routed a two-layer PCB in KiCad, including component placement, copper routing, copper zones, board outline geometry, and mounting holes. Balanced electrical connectivity with physical layout and manufacturing considerations.

## Design Decisions: Custom Board vs. STM32 Blue Pill

The STM32 Blue Pill served as inspiration for this project. Rather than simply reproducing an existing development-board layout, I designed a custom schematic and PCB to gain experience with component selection, circuit integration, debugging access, and board-level design decisions.

| Design aspect | Custom design |
|---|---|
| PCB layout | Independently designed two-layer layout in KiCad |
| Analog power | Ferrite bead incorporated into the analog supply path to help reduce high-frequency noise coupling |
| Clock source | 16 MHz external crystal oscillator |
| Debugging and expansion | Accessible headers for external connections and development |
| Power circuitry | Custom schematic integration of USB input and 3.3 V regulation |
| Mechanical design | Custom board outline, mounting holes, and component placement |

These design choices provide a different implementation from a standard Blue Pill layout. The goal was to understand and control the supporting circuitry and physical design rather than depend entirely on a predesigned development board.

The ferrite bead, custom layout, and accessible headers address specific design considerations, but their presence alone does not establish better overall performance than the Blue Pill. Quantitative comparisons would require hardware measurements and testing.

## Design Process

1. **Research and component selection:** Consulted STM32 datasheets, application notes, component datasheets, and existing development-board designs to understand circuit requirements and implementation options.
2. **Schematic capture:** Designed the microcontroller circuitry, power regulation, clock circuit, USB connections, and supporting components in KiCad.
3. **PCB layout:** Transferred the schematic into a two-layer board, arranged components, routed copper traces, and incorporated copper zones and mechanical features.
4. **Design validation:** Ran KiCad's Design Rules Checker (DRC) to check the PCB layout against configured design constraints.
5. **Manufacturing preparation:** Generated Gerber files and NC drill data for PCB fabrication.

## Tools and Technologies

- **KiCad:** Schematic capture, PCB layout, 3D visualization, and design-rule checking
- **STM32F103C8T6:** ARM Cortex-M3 microcontroller
- **PCB Design:** Two-layer routing, component placement, copper zones, and mechanical layout
- **Hardware Research:** Datasheets, application notes, and component documentation
- **Manufacturing:** Gerber files and NC drill data

## Repository Structure

```
custom-stm32-pcb/
├── kicad/
│   ├── customPCB.kicad_pro
│   ├── customPCB.kicad_sch
│   └── customPCB.kicad_pcb
├── manufacturing/
│   ├── Gerber copper layers
│   ├── Solder mask and silkscreen layers
│   ├── Board outline
│   └── NC drill file
├── images/
│   ├── pcb_3d.png
│   └── pcb_layout.png
└── README.md
```

## Project Status

- [x] Schematic design
- [x] Two-layer PCB layout and routing
- [x] KiCad design-rule checking
- [x] Gerber and NC drill generation
- [x] PCB fabrication and assembly documentation
- Complete!

## Future Improvements

- Document the exact pin assignments and functions of each header.
- Add a bill of materials (BOM) with component values, footprints, and manufacturer part numbers.
- Document hardware bring-up procedures and debugging connections.
- Verify power rails, clock operation, programming, USB functionality, and peripheral interfaces.
- Record measured results and potential improvements in future board revisions.

## Design References

The design process was informed by technical documentation and reference material, including:

- STMicroelectronics STM32F103x8/xB datasheet
- STM32F1 reference manual
- STMicroelectronics hardware application notes relevant to oscillator design and USB connectivity
- Component datasheets for the voltage regulator, crystal, ferrite bead, and supporting circuitry
- KiCad documentation for schematic capture, PCB layout, and design-rule checking
- Existing STM32 development-board designs used as architectural references

## License

Add a license appropriate for the hardware design and documentation before permitting reuse or redistribution.
