# IHP HBT Characterization

*Prepared by Bao TON - APC*

## 1. Measurement Description

The purpose of this measurement is to characterize the Heterojunction Bipolar Transistor (HBT) from IHP.

The test circuit consists of 6 groups of transistors, with each group containing 40 transistors in parallel. Each transistor has an emitter length ($E_l$) of $40 \mu m$. The circuit, designed by Jean Mesquida (APC), is part of the R&T BiCMOS project ASIC, which was taped out in November 2024. The test board was provided by Bao TON (APC).

Measurements were performed using a **B1500A Semiconductor Device Parameter Analyzer** at two distinct temperatures:
- **Room temperature:** 300K
- **Cryogenic temperature:** 77K

The results presented were obtained using a new test board which incorporates several improvements:
- Two Murata Ferrite Beads ($1000 \Omega$) in series at the input.
- A two-stage filter at the output, composed of capacitors ($1 \mu F$) and Murata Ferrite Beads.

## 2. Gummel Plot Analysis: Cryogenic vs. Room Temperature

The following plots show the collector current ($I_C$), base current ($I_B$), and current gain ($\beta$) as a function of the base-emitter voltage ($V_{BE}$).

### 2.1. Room Temperature (300K)

![Gummel Plot at Room Temperature](plot/gummel_300K_new.png)

### 2.2. Cryogenic Temperature (77K)

![Gummel Plot at Cryogenic Temperature](plot/gummel_77K_new.png)

### 2.3. Comparison

The comparison plot below overlays the Gummel plots at both temperatures.

> **Note:** The new test board setup introduces oscillation in the low-voltage range for the room temperature measurement. Data from the previous test board, which shows a clearer characteristic over a longer range, is intended to be added here for a more complete comparison.

![Comparison of Gummel Plots at Cryogenic and Room Temperatures](plot/gummel_CT_RT.png)

## 3. Output Characteristics ($I_C$ vs. $V_{CE}$)

In this measurement, the transistor's base was biased with a constant current source ($I_B$), while the collector-emitter voltage ($V_{CE}$) was swept. The plots illustrate the difference in output characteristics between room temperature (300K) and cryogenic temperature (77K).

### 3.1. Room Temperature (300K)

- **Base Current ($I_B$):** Swept from $5 \mu A$ to $25 \mu A$ in steps of $5 \mu A$.

![IC-VCE Characteristics at Room Temperature](plot/IcVce_RT_new.png)

### 3.2. Cryogenic Temperature (77K)

- **Base Current ($I_B$):** Swept from $5 \mu A$ to $20 \mu A$ in steps of $5 \mu A$.

![IC-VCE Characteristics at Cryogenic Temperature](plot/IcVce_LNT_new.png)

### 3.3. Comparison

- **Base Current ($I_B$):** Swept from $5 \mu A$ to $20 \mu A$ in steps of $5 \mu A$ for both temperatures.

![Comparison of IC-VCE Characteristics](plot/IcVce_compare_new.png)

## 4. Data and File Organization

### 4.1. Plot Directory

All generated plots are located in the `plot/` directory.

### 4.2. Data Directories

The measurement data is organized as follows:

- **Data from the new test board:**
```
R&TBiCMOS/
└── dat_to_plot/
            ├── gummel/
            └── IcVce/
```
- **Data from the original (old) test board:**
```
R&TBiCMOS/
└── old_PCB/

```
# Aknowledgement 

ASICs and Measurement was done due to the contribution of **R&T BiCMOS** multi-wafer project and **Laboratory
of Astroparticles and Cosmology (APC)**
