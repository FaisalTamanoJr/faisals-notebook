---
draft: false
title: 2nd Order Circuits
date: 2024-07-04
aliases: []
tags: [Physics/Electrical-Engineering]
---

Related concepts: [[Capacitors]], [[Inductors]]

A second order circuit contains a resistor and two energy storing devices, namely capacitors, and/or inductors (or vice-versa). Performing Kirchhoff’s Voltage Law (KVL), taking the derivative, and dividing by L gives us the 2nd order differential equation

$$
\frac{d^2i}{dt^2}+ \frac{R}{L} \frac{di}{dt} + \frac{1}{LC} = 0
$$

This gives us the relationship

$$
\begin{align}
i_{r}=\frac{v}{r} && \frac{di_{L}}{dt}=\frac{v_{L}}{L} && i_{C}=C \frac{dv}{dt}
\end{align}
$$

## Strategy to Solving

Look for the values of the following

1. $i(t=0^-)$ and $v(t=0^-)$
2. $i(t=0^+)$ and $v(t=0^+)$
3. $\frac{di}{dt}(t=0^+)$ and $\frac{dv}{dt}(t=0^+)$
4. $i_{L}(t\to \infty)$ and $v_{C}(t\to \infty)$

Usually, the values for 1. and 2. are the same because the voltage across the capacitor and the current through an inductor cannot change instantaneously.

To find the rate of change of the current through an inductor with respect to time

$$
\frac{di_{L}}{dt} = \frac{v_{L}}{L}
$$

To find the rate of change of the voltage across a capacitor with respect to time

$$
\frac{dv_{C}}{dt} = \frac{i_{C}}{C}
$$

## Solving a Source Free RCL Circuit Using KVL

When we are solving a source free RCL circuit, we assume that the there are initial conditions for the capacitor and/or the inductor (or vice-versa) to generate the circuit’s current flow.

The amount of energy stored in a capacitor depends on the amount of charge collected by the capacitor, whereas the amount of energy stored in an inductor depends on the amount of current flowing through it. As a result, when there is maximum current through the inductor, there will be no charge in the capacitor. If, however, there is maximum charge in the capacitor, then there will be no current flowing through the inductor.

- Maximum energy in the inductor → no energy in the capacitor
- Maximum energy in the capacitor → no energy in the inductor

The resistor in the circuit dissipates the circuit’s remaining energy.

What happens in the circuit dictates the voltage polarity of each component:

- The direction of the current influences the resistor’s polarity
- The charge on the capacitor influences it’s polarity
- The rate of change of the current influences the inductor’s polarity

Using KVL we can derive the equation for solving source free RCL circuits

$$
-iR - L \frac{di}{dt} - \frac{1}{C} \int ^t _{0}i\, dt =0
$$

or

$$
iR + L \frac{di}{dt} + \frac{1}{C} \int ^t _{0}i\, dt =0
$$

## Sources

1. [What is 2nd Order Circuits](https://youtu.be/BY4ounBzi3I)
2. [What is 2nd Order Circuits Part 2](https://youtu.be/kvHEYIYbTQY)
3. [Key to Solving 2nd Order Circuits](https://youtu.be/B79Kye6U_vw)
4. [Source Free RCL KVL](https://youtu.be/wy2ierjxZos)
