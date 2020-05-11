---
layout: page
title: Stage 2
subtitle: Control system development
---

In implementing this system, we are assuming use of pressure-controlled ventilation, it would therefore be of crucial importance to be able to monitor the tidal volume that the ventilator is delivering to each individual patient for the given pressure delivered. We know that in ARDS the aim would be for a lung protective ventilation strategy in which being able to monitor, and control individual tidal volumes delivered to the patients is vital. In this stage of the project we aim to develop systems and strategies to easily measure/ monitor and therefore enable adjustment of the tidal volumes delivered to each patient.

### Approach

We propose using a combination of moving horizon estimation and model predictive control to determine and then adjust the tidal volume delivered to each patient. Both the estimation-based monitoring and control strategy will be found as the solution of one or more optimization problems. These advanced techniques allow us to systematically incorporate constraints, such as minimum and maximum safe tidal volumes, nonlinearities and uncertainties.
In the estimator, a series of measurements will be taken of the tidal flow over a single or multiple inhale-exhale cycles. We will use the dynamics and structure of the circuit model shown in link to simulation section of website. By taking a sufficient number of noisy measurements we can determine the equivalent resistance-compliance values and tidal volume of each individual patient to best fit the measurements, as well as bounding the range of possible tidal volume per patient that is consistent with the measurements.
This is shown in the figure below, were we take a few measurements of the flow at the ventilator during a single inhale-exhale cycle. We are able to reconstruct the flows being delivered to each of the unique patients by only measuring this combined flow at the ventilator, such that the tidal volumes of each patient can be estimated. Importantly, this procedure requires no additional sensors.

![](/img/2Patient_Estimation_Flow_uniform.png)
<fig>Figure 1: Two patient flow estimation</fig>

Based on the identified patient parameters, we use model predictive control to determine how best to adjust the control strategy such that both patients receive the appropriate flow From figure 2, we can observe that it is impossible, by changing the PIP and PEEP pressure only, for patients with different characteristics to both receive the same amount of desired tidal volume treatment. However, as shown in figure 3 by adding variable tube sections and adjusting each tube, based on our control scheme, we can provide the extra flexibility necessary for both patients to receive the ideal treatment on the same ventilator.

![](/img/2Patient_Controlled_withoutAS_Flow.png)
<fig>Figure 2: Two patient flow control with no adjustable tube section</fig>

![](/img/2Patient_Controlled_withAS_Flow.png)
<fig>Figure 3: Two patient flow control with adjustable tube section</fig>

{% include readnext.html text="Stage 3" url="/stage3/" %}

