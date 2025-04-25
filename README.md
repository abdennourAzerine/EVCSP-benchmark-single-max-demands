# EVCSP Benchmark Instances (CSV Format)

This repository provides benchmark instances for the **Electric Vehicle Charging Scheduling Problem (EVCSP)** in CSV format, suitable for reproducibility and comparison in scheduling optimization studies.

## 📘 Problem Overview

The EVCSP involves scheduling a set of EV charging demands over a discrete time horizon, across multiple chargers, while adhering to:
- **Power capacity constraints** (global grid limit)
- **Charger exclusivity** (no overlap on a single charger)
- **Preemptive scheduling** (charging can be paused/resumed)
- **Deadline constraints** (vehicles must finish charging by departure time)


## 📁 Folder Structure
EVCSP-benchmark/
├── chargers/
│   ├── group1.csv
│   ├── group2.csv
│   └── ...
├── instances/
│   ├── group1_instance1.csv
│   └── ...
├── README.md
└── LICENSE  # Optional: add MIT license or similar


---

## 🔋 Charger Files (`/chargers/`)

Each file corresponds to a scenario group and contains:

- **Line 1:** Title (ignored)
- **Line 2:** Index of chargers (for readability) and Global grid capacity \( w_G \) (in kW)
- **Remaining Lines:** Each row is of the format: charger_power_kw, number_of_chargers
## 🚗 Demand Instance Files (`/instances/`)

Each file represents a single instance and contains:

- **Header:** `index,arrival_time,departure_time,required_energy`
- **Rows:** One per vehicle charging demand


- Time is in **hours**
- Energy in **kWh**
- tau is fixed to 0.1

---

## 📊 Instance Groups

Four groups of scenarios, each defined by:
- **n:** Number of charging demands
- **m:** Total number of chargers
- **\( w_G \):** Grid power capacity (kW)

| Group | n   | m  | Grid Capacity \( w_G \) |
|-------|-----|----|--------------------------|
| 1     | 10  | 15 | 50                       |
| 2     | 40  | 24 | 75                       |
| 3     | 50  | 27 | 100                      |
| 4     | 100 | 30 | 125                      |

Each group has **10 instances**.

---

## ⚙️ Usage

You can load these CSV files directly using Python, pandas, or your preferred tool. 

---

## 📄 License

Released under the **MIT License**. Free to use, modify, and distribute with attribution.

---

## 📣 Citation

If these datasets help your research or application, please cite the associated paper (coming soon).

