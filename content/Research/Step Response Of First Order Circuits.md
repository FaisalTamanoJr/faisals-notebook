---
draft: false
title: Step Response of First Order Circuits
date: 2024-07-03
aliases: []
tags: [Physics/Electrical-Engineering]
---

Related concepts: [[Capacitors]], [[Inductors]]

## RC Circuits

### Natural and Forced Response

Assuming that there was some initial energy stored in the capacitor, the voltage across the capacitor or the complete response is the sum of the natural response and the forced response; mathematically, this is expressed as

$$
v=v_{n}+v_{f}
$$

Where the natural response of the circuit comes from the existing stored energy in the capacitor; it is equal to $v_{0}e^{t/\tau}$. In contrast, the forced response comes from the input source that drives current through the circuit, which is equal to $V_{s}(1-e^{-t/\tau})$.

The natural response decays over 5 time constants ($\tau$)

### Transient and Steady Response

Assuming that there is some voltage across the capacitor or some charge stored inside the capacitor, the equation that describes the voltage across the capacitor from $t=0$ to $t=\infty$ is

$$
v(t)=v_{s}+(v_{0}-v_{s})e^{-t/\tau}
$$

Where $v_{s}$ is the steady state response and the rest pertains to the transient response. Similar to the natural response, the transient response only lasts for about $5$ time constants ($\tau$)

1. At $t>5\tau$, the steady-state response is equal to the complete response
2. At $t<5\tau$, we get the transient response

## RL Circuits

The current through the inductor is the sum of the transient and steady-state portion of the current

$$
i=i_{ss}+i_{t}
$$

Where

$$
\begin{align}
i_{ss} &= \frac{V}{R} \\
i_{t} &=(I_{0}-\frac{V}{R})e^{-t/\tau} 
\end{align}
$$

Therefore,

$$
i(t)=\frac{V}{R}+(I_{0}-\frac{V}{R})e^{-t/\tau}
$$

In this context, the transient current is the temporary current before reaching its steady-state, and the steady-state current refers to the current that the inductor stopped opposing because it stayed constant. [^1]

## Sources

1. [Natural and Forced Response](https://youtu.be/PsQP2mOANAA)
2. [Transient and Steady State Response](https://youtu.be/KPOQ-cdGbjQ)
3. [Step Response of an RL Circuit](https://youtu.be/tEmksld8sC0)

[^1]: The inductor becomes a short circuit at this point
