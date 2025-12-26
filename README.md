# 65nm Standard Cell Library Design

## Overview
This repository contains the design and characterization of a comprehensive standard cell library using 65nm CMOS technology. The project involves the schematic design, custom layout, verification (DRC/LVS), and parasitic extraction for **8 distinct logic cells**.

## Design Objectives
* **Technology Node:** 65nm
* **Uniform Cell Height:** All cells scaled to **5.660 μm** for row compatibility.
* **Optimization:** Minimized area using a **0.52 μm pin pitch** and **0.39 μm offsets**.
* **Simulation Conditions:**
    * Load Capacitance: **45 fF**
    * Input Slew Rate: **35 ps**

## Library Specifications

| # | Cell Name | Function | Cell Width (μm) | Cell Area (μm²) |
|:-:|:----------|:---------|:---------------:|:---------------:|
| 1 | **INVERTER** | `NOT(A)` | 0.900 | 5.0940 |
| 2 | **NAND2** | `NOT(AB)` | 1.420 | 8.0372 |
| 3 | **NOR2** | `NOT(A+B)` | 1.420 | 8.0372 |
| 4 | **XOR2** | `A⊕B` | 2.980 | 16.8668 |
| 5 | **AOI22** | `NOT(AB+CD)` | 2.460 | 13.9236 |
| 6 | **OAI22** | `NOT((A+B)(C+D))` | 2.460 | 13.9236 |
| 7 | **OAI21** | `NOT((A+B)C)` | 1.940 | 10.9804 |
| 8 | **NAND3** | `NOT(ABC)` | 1.940 | 10.9804 |

## Verification Flow
1.  **Schematic Entry:** Logic verification in Cadence Virtuoso.
2.  **Custom Layout:** Minimized polysilicon and metal routing area.
3.  **Physical Verification:**
    * **DRC:** Zero errors for individual cells and multi-cell placement.
    * **LVS:** Netlists matched perfectly.
4.  **Parasitic Extraction (PEX):** Generated netlists with parasitic R/C.
5.  **HSPICE Simulation:** Validated timing and functionality under 45fF load.

---
**Authors:**  Aryan Verma  
**Course:** EECT / CE 6325 – VLSI Design (Fall 2025)  
**Instructor:** Prof. Carl Sechen
All cells layout and schematic are zipped in **amock 1** folder
