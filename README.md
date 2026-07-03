# Grid-Connected Solar PV Integration — ETAP Simulation

A power system simulation built in **ETAP 19.0.1**, modeling a hybrid distribution network that combines utility grid supply with solar PV generation at the 11 kV / 0.415 kV level.

![ETAP Single Line Diagram](./images/etap-single-line-diagram.jpeg)

## 📌 Overview

This project demonstrates how renewable energy sources can be integrated into a conventional grid-fed distribution system, and how switching configurations affect power flow and reliability. The model includes a utility source, two inverter-connected solar PV arrays, a step-down transformer, and a mix of motor, lighting, and general loads on the low-voltage side.

## ⚡ System Components

| Tag | Component | Rating / Voltage | Function |
|-----|-----------|-------------------|----------|
| U1 | Utility Grid Source | 1024 MVAsc | Main grid supply / infinite bus |
| Bus2 / Bus3 | 11 kV Busbars | 11 kV | Medium-voltage distribution points |
| Cable1 | MV Cable | 11 kV | Transfers power between buses |
| T1 | Power Transformer | 1 MVA, 11/0.415 kV | Steps down voltage to LV level |
| Bus1 | Main LV Busbar | 0.415 kV | Distributes power to loads |
| PVA2 / PVA3 | Solar PV Arrays | DC generation | Convert sunlight to DC electricity |
| Inv3 | Inverter | DC → AC | Converts PV DC output to AC for grid injection |
| SW1 / SW2 | Disconnect Switches | Manual | Isolation for safety / maintenance |
| Load1 | General Load | 0.5 kVA | Small lighting / general load |
| Mtr1 / Mtr2 | Induction Motors | 1 HP each | Motor-driven equipment (pumps, fans) |
| Lump1 | Lumped Load | 3 kVA | Larger lighting / equipment load |

## 🖼️ Diagram Explained

To make the schematic accessible to non-specialists, each component was mapped to its real-world physical equivalent — from solar panels and inverters to transformers and switchgear.

![Real-Life Explanation Infographic](./images/etap-real-life-explanation.jpeg)

## 🎥 Demo

A short screen recording of the simulation is included: [`demo.mp4`](./media/demo.mp4)

## 🔍 Key Observations

- PV arrays PVA2 and PVA3 generate DC power, converted to AC by inverter Inv3 before feeding the 11 kV bus.
- Power from the utility grid (U1) and PV sources is combined and distributed through Bus2 and Bus3.
- Transformer T1 steps the voltage down from 11 kV to 0.415 kV to supply the low-voltage bus (Bus1).
- All LV loads (motors, general load, lumped load) are supplied from Bus1.
- Switches SW1 and SW2 allow independent isolation of each PV branch for maintenance without interrupting the rest of the network.

## 🛠️ Tools Used

- **Software:** ETAP 19.0.1
- **Analysis type:** Load flow / power distribution modeling

## 📄 Report

A full write-up is available in [`report.pdf`](./report.pdf).

## 📂 Repository Structure

```
├── images/
│   ├── etap-single-line-diagram.jpeg
│   └── etap-real-life-explanation.jpeg
├── media/
│   └── demo.mp4
├── report.pdf
└── README.md
```

## 👤 Author

Designed and simulated by Anass

