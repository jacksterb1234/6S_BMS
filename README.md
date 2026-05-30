# 6S BMS — 6-Cell Battery Management System

A custom **6-series (6S) Battery Management System** PCB designed in KiCad for robotics and high-power applications. The design features cell voltage sensing, balancing, and CAN bus communication for integration with external controllers.

## Features

- **6S cell configuration** — supports 6 series lithium cells
- **Analog Front End (AFE):** Texas Instruments BQ76925 for cell monitoring and balancing
- **CAN Bus communication:** TCAN3404 transceiver for robust data transmission
- **Cell voltage sensing** with dedicated sense schematic (`6S_Cell_Sense`)
- **Passthrough board** schematic for power routing
- **Custom KiCad footprints** and symbols for all major ICs
- Designed with **JLCPCB assembly** constraints in mind

## Repository Structure

```
6S_BMS/
├── Kicad/                  # Main KiCad project files
├── 6S_BMS-backups/         # KiCad automatic backups
├── ZXTP25040DFHTA/         # Custom footprint: PNP transistor
├── ul_B8B-XH-A-LF-SN-/    # Custom footprint: JST connector
├── ul_BQ76925RGER/         # Custom footprint: BQ76925 AFE IC
├── ul_DLW21SN900HQ2L/      # Custom footprint: Common mode choke
├── ul_TCAN3404DRBRQ1/      # Custom footprint: CAN transceiver
├── ul_UCC12050DVE/         # Custom footprint: Isolated DC-DC
├── 6S_BMS.kicad_sch        # Main schematic
├── 6S_BMS_Passthrough.kicad_sch  # Passthrough board schematic
├── CAN.kicad_sch           # CAN bus sub-schematic
└── 6S_Cell_Sense.pdf       # Cell sense circuit reference
```

## Tools Used

- **KiCad** — Schematic capture and PCB layout
- **JLCPCB** — PCB fabrication and assembly

## Key ICs

| Part | Function |
|------|----------|
| BQ76925RGER | 6S analog front end (cell monitoring & balancing) |
| TCAN3404DRBRQ1 | Automotive CAN FD transceiver |
| UCC12050DVE | Isolated 5V DC-DC converter |
| ZXTP25040DFHTA | PNP transistor for cell balancing |
| DLW21SN900HQ2L | Common mode choke (CAN EMI filtering) |

## Author

**Jackson Barber** — [github.com/jacksterb1234](https://github.com/jacksterb1234)
