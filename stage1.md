---
layout: page
title: Stage 1
subtitle: Simulation model development
---

We have designed an electrical circuit as an analogue to the ventilator, simulating ventilator splitting. In mapping air flow to an electrical circuit we equate volume to charge, flow to current, pressure to voltage, resistance to resistance and compliance to capacitance. We will use this model to test ventilator splitting in various different configurations whilst varying lung physiology and disease processes (varying compliance/resistance) in the 2 lung models.

![](/img/diagram_elements.png)

### Results so far

You can read the [publication](https://royalsocietypublishing.org/doi/10.1098/rsos.200585),
in Royal Society Open Science. 
We used this model to demonstrate use of both the previously suggested basic Y connector splitter and our modified splitter. The model showed that using the modified setup, we can demonstrate that it is possible to achieve the same tidal volumes in 2 patients with mismatched lung compliances and that tidal volume of one patient can be manipulated independently of the other.

The simulation files and documentation can be found in our
[GitHub repository](https://github.com/splitvent/splitvent).

### Circuit design

#### Standard
![](/img/simmodel_standard.png)

#### Modified
![](/img/simmodel_modified.png)

Solís-Lemus JA, Costar E, Doorly D, Kerrigan EC, Kennedy CH, Tait F, Niederer S, Vincent PE and Williams SE. A simulated single ventilator/dual patient ventilation strategy for acute respiratory distress syndrome during the COVID-19 pandemic. R Soc open sci 2020; 7: 200585


{% include readnext.html text="Stage 2" url="/stage2/" %}

