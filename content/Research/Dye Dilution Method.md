---
draft: false
title: Dye Dilution Method
date: 2024-08-04
aliases: []
tags: [Biology]
---

## Lund-Johansen

To measure the cardiac output, this method injects a known amount of dye inside the circulatory system. It is withdrawn at a distal site afterward to generate and examine the concentration curve of the dye.

$$
\begin{align}
\text{Flow (Q)} && Q=\frac{m}{\bar{c}\times t}
\end{align}
$$

> [!NOTE]
> - $m$ is the injected dye’s amount
> - $\bar{c}$ is the dye’s concentration
> - $t$ is the time of the concentration curve without recirculation

Requirements and limitations:

1. It does not provide a *beat-to-beat* measurement
2. The cardiac output must be stable for about 10 seconds during exercise and 30 seconds at rest. This is because the method requires that the flow and volume of the vascular bed are constant.
3. Fluids entering the system should leave the vascular bed.

History

1. Stewart was first to measure cardiac output using an indicator and recording the indicator’s concentration at a distal site.
2. Many years later, Hamilton and his group modified Stewart’s equation and addressed its re-circulation issue. For this reason, the method became officially known as the *Stewart-Hamilton technique*.
3. Many later, Cardiogreen became the established dye indicator for cardiac output measurement.
	1. It has an absorption maximum in the infrared part of the spectrum ($805 \mu m$). This range is where the oxygen and unsaturated haemoglobin’s spectrum intersect.
	2. It can be rapidly withdrawn (at least 10 cardiac outputs can be recorded per hour).
	3. It is non-toxic

Process

1. Dye is injected into a flow of unknown rate
2. Concentration is measured distal to the injection site
3. Concentration curve of the dye is determined

## Louvaris Et Al.

- the dye-dilution is an invasive techniques that measures cardiac output during exercise.
- The dye-dilution technique requires an arterial catherer, but is easier to use than the direct Fick method and is more accurate than thermodilution.
- It is a discontinuous method, meaning that it involves separate injection of dye and rapid repetition of measurements.

## Stewart J.

- Cardiac output is the volume of blood pumped by the heart for a specified period (rate of flow into the aorta).

Process

1. Dye dilution method involves injecting the dye into the right atrium and flowing through the heart into the aorta.
2. To measure the dye’s concentration, a probe is inserted into the aorta while the dye leaves at equally spaced times on a time interval $[0,T]$. This step stops when there is no more dye left.

We can determine the cardiac output using the following formula:

$$
F=\frac{A}{\int ^T _{0} c(t)\, dt }
$$

> [!NOTE]
> - $F$ is the rate of flow
> - $A$ is the total amount of dye
> - $T$ is the duration for the time interval
> - $c(t)$ is the concentration of the dye at time $t$

The rate of flow is a measurement for the cardiac output. We can express it in liter per minute ($L/min$) or liter per second ($L/s$).

## Sources

1. Zafeiris Louvaris, Stavroula Spetsioti, Vasileios Andrianopoulos, Nikolaos Chynkiamis, Helmut Habazettl, Harrieth Wagner, Spyros Zakynthinos, Peter D. Wagner, Ioannis Vogiatzis, The Clinical Respiratory Journal, “[Cardiac output measurement during exercise in COPD: A comparison of dye dilution and impedance cardiography](https://doi.org/10.1111/crj.13002)” - 2019-02-05
2. Lund-Johansen P., European heart journal, “[The dye dilution method for measurement of cardiac output](https://doi.org/10.1093/eurheartj/11.suppl_i.6)” - 1990-12-01
3. Stewart J., Early transcendentals, “Further applications of integrations” - 2007
