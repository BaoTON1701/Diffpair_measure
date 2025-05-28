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

![IcVce at low base current injection](plot/IcVce_sweep_low_Ib.png)

* **The plot at room temperature**: $I_B$ ranges from $1 \mu A$ to $12 \mu A$, step = $1 \mu A$
* **The plot at cryogenic temperature**: $I_B$ ranges from $0.5 \mu A$ to $2.25 \mu A$ with step $0.25 \mu A$ at the first 8 curves then $3 \mu A$ to $8 \mu A$ with step $1 \mu A$ for the rest

The plot clearly show that at low base current density, the current $I_C$ wrt $V_{CE}$ behave
stably and there is no clear offset of $V_{CE}$ but when the current become higher (up to $I_B = 3 \mu A$), it starts to appear NDR effect and the collector current start to oscillate. The negative differential resistance (NDR) effect can also observe as an abnomaly peak  in the result of $I_C - V_{CE}$ sweep at cryogenic temperature and high base current.


 
