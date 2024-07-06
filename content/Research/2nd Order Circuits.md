---
draft: false
title: 2nd Order Circuits
date: 2024-07-04
aliases: []
tags: [Physics/Electrical-Engineering]
---

Related concepts: [[Capacitors]], [[Inductors]], [[Waves]]

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

## Source Free RCL Circuit and KVL

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

## Solving Source-free RCL Circuits

Because we want to convert this equation

$$
\frac{d^2i}{dt^2}+\frac{R}{L} \frac{di}{dt} + \frac{1}{LC} i = 0
$$

to

$$
i(t)=Ae^{st}
$$

We transform each part and get an equation that is dependent on $s$; therefore, $s$ is its characteristic equation

$$
s=-\frac{R}{2L} \pm \sqrt{ \left( \frac{R}{2L} \right)^2 - \frac{1}{LC} }
$$

If we let $\alpha = \frac{R}{2L}$ (the damping factor)[^damping] and $\omega_{0}=\frac{1}{\sqrt{ LC }}$ (natural frequency of the circuit),[^natural_frequency] then we can simplify the characteristic equation into

$$
s=-\alpha\pm \sqrt{ \alpha^2-\omega_{0}^2 }
$$

There are three possible cases/solutions based on the previously shown equation’s discriminant:

1. overdamping;
	- $\alpha^2 > \omega_{0}^2$
2. critical damping; and
	- $\alpha^2 = \omega_{0}^2$
3. underdamping
	- $\alpha^2 < \omega_{0}^2$
	- Solution:

> [!NOTE]
> - $\omega_{d}=\sqrt{ \omega_{0}^2-\alpha^2 }$
> 	- The oscillations are slower because it assumes that there is resistance, unlike $\omega_{o}$
> 	- also known as the *damped natural frequency*

### Overdamping

Overdamping is the case where the damping factor $\alpha$ is greater than the natural frequency $\omega_{0}$. In this case, we will have two solutions to our characteristic equation, $s_{1}$ and $s_{2}$; as a result, our general equation will be

$$
i(t)=A_{1}e^{s_{1}t}+A_{2}e^{s_{2}t}
$$

> [!TIP]
> $s_{1}$ and $s_{2}$ should both always be negative and real values

The constants $A_{1}$ and $A_{2}$ can be solved using the initial conditions of the current and its change

This case entails that the current $i(t)$ will never reach the $Ae^{-\alpha t}$ curve until time goes to infinity

### Critical Damping

Critical damping occurs when the damping factor $\alpha$ is equal to the natural frequency $\omega_{0}$, where the current curve intersects with the $Ae^{-\alpha t}$ curve at its maximum point and comes closer together as time approaches infinity.

Because the damping factor and natural frequency are the same, we can rewrite the function for the current in terms of the damping factor

$$
\frac{d^2i}{dt^2}+\frac{2\alpha di}{dt}+\alpha^2i=0
$$

Through derivations and some algebraic and calculus tricks, we can formulate the following equation for the current:

$$
i(t)=(A_{1}t+A_{2})e^{-\alpha t}
$$

### Underdamping

In this case, the resistor is so small that the damping factor $\alpha$ is less than the natural frequency $\omega_{0}$. For this reason, we will get an imaginary number when solving the characteristic equation. Furthermore, we will rewrite the characteristic equation to

$$
s_{1},s_{2}=-\alpha\pm \sqrt{ -(w_{0}^2-\alpha^2) }
$$

which then gives us

$$
-\alpha \pm jw_{d}
$$

where $w_{d}$ is the *damped natural frequency* or $\sqrt{ w_{0}^2 - \alpha^2 }$. This natural frequency, unlike natural frequency $\omega_{0}$, is the rate of oscillation where resistance is present. As a consequence, the damped natural frequency has smaller frequency and larger period than the one without a damping factor because its current is being dissipated by the resistor.

![undamped_vs_damped.webp](https://qph.cf2.quoracdn.net/main-qimg-8b286b5aedd2d6d4e58d66bbb8c2b772.webp)

Because $s_{1}$ and $s_{2}$ have imaginary numbers resulting from having a smaller $\alpha$, the equation for solving their current slightly differs from the overdamping case. Through algebraic and trigonometric techniques, we can obtain the following equation for the current:

$$
i(t)=e^{-\alpha t}[B_{1}\cos \omega_{d}t+B_{2}\sin \omega_{d}t]
$$

where

$$
\begin{align}
B_{1}&=(A_{1}+A_{2}) \\
B_{2}&=(A_{1}-A_{2})j
\end{align}
$$

> [!SUMMARY]
> - *Overdamping* slowly returns to equilibrium without oscillating
> - *Critical damping* quickly returns to equilibrium without oscillating and passes it once at most
> - *Underdamping* quickly returns to equilibrium but will oscillate and, thus, cross the equilibrium multiple times
> ![damping graphs.jpg](https://qph.cf2.quoracdn.net/main-qimg-e953072f07fb52d303e439dd2d19cbce-lq)

## Sources

1. [What is 2nd Order Circuits](https://youtu.be/BY4ounBzi3I)
2. [What is 2nd Order Circuits Part 2](https://youtu.be/kvHEYIYbTQY)
3. [Key to Solving 2nd Order Circuits](https://youtu.be/B79Kye6U_vw)
4. [Source Free RCL KVL](https://youtu.be/wy2ierjxZos)
5. [Three Solutions for Source Free RCL](https://youtu.be/XRBYHBJ-Wn8)
6. [Overdamping](https://youtu.be/_mFD9c_-Te4)
7. [Critical damping](https://youtu.be/3y_-NwHwE00)
8. [Underdamping](https://youtu.be/7yxTYhUoV4c)
9. [Underdamping Frequency](https://youtu.be/RwERYhySKFc)
10. [Example 1](https://youtu.be/yvaegtA3XaU)
11. [Example 2](https://youtu.be/idY0ZF5tk0o)
12. [Example 3](https://youtu.be/hxPbKucrtBo)
13. [Example 4](https://youtu.be/XU1gcNCp6ao)

[^damping]: Damping in physics refers to the restriction of vibratory motion, and, as such, the damping factor deals with how much the circuit’s oscillations decrease over time.
[^natural_frequency]: Natural frequency is the rate at which the circuit’s oscillations tends to oscillate in the absence of resistance
