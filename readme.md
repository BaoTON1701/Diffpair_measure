# BJT Characterization:

## 1. Gummel Plot Analysis

This repository contains Python scripts for generating Gummel plots to 
characterize Bipolar Junction Transistors (BJTs) at different operating 
temperatures. The analysis focuses on the relationship between the 
base-emitter voltage ($V_{BE}$) and the resulting collector ($I_C$) and 
base ($I_B$) currents, as well as the current gain ($\beta$).

### Gummel Plot: Cryogenic vs. Room Temperature

The plot below shows the simulated BJT performance at both room 
temperature (e.g., 300K) and cryogenic temperature (e.g., 77K). The top 
panel displays the current gain ($\beta$), while the bottom panel shows 
the collector and base currents on a logarithmic scale.

![Gummel Plot at Cryogenic and Room Temperatures](plot/gummel_CT_RT.png)

### Key Features of the Plot
* **Top Plot**: Current Gain ($\beta$) vs. $V_{BE}$. The y-axis is on the 
right.
* **Bottom Plot**: Collector Current ($I_C$) and Base Current ($I_B$) vs. 
$V_{BE}$. The y-axis is on the left.
* **Seamless Stacking**: The plots are stacked with no vertical space for 
direct comparison.
* **Homogeneous Grid**: A shared x-axis and continuous grid lines aid in 
correlating gain behavior with current levels.

## How to Generate
The plot is generated using a Python script. To reproduce the figure, run 
the main script.

## 2. $I_C$ vs $V_{CE}$ sweep

In this measurement, we will bias the base of BJT transistor by current 
source $I_B$ then sweep $V_{CE}$. The plot will show the different between 
the characteristic at room temperature $T = 300K$ and cryogenic temperature 
$T = 77K$.

### 2.1. $I_C$ vs $V_{CE}$ sweep with low base current in CR 
![IcVce at low base current injection](plot/IcVce_sweep_low_Ib.png)

In this plot, the base current bias ranges from $500nA$ to $2250nA$. It clearly
show that at low base current density, the current $I_C$ wrt $V_{CE}$ behave
stably and there is no clear offset of $V_{CE}$.


 
