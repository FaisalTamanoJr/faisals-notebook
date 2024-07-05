---
draft: false
title: RC and RL  Circuits
date: 2024-07-03
aliases: []
tags: ["Physics/Electrical-Engineering"]
---

Related concepts: [[Capacitors]], [[Inductors]], [[Step Response Of First Order Circuits]]

## Introduction

RC circuits contain a resistor and a capacitor, while RL circuits contain a resistor and an inductor. They are known as *first-order circuits* because setting up an equation that defines a voltage in an RC circuit or a current in an RL circuit involves first-order differential equations.

$$
\begin{align}
C \frac{dv}{dt} + \frac{v}{R} &=0 \\
L \frac{di}{dt} + Ri &= 0
\end{align}
$$

## RC Circuit without a Source

- The initial charge of the capacitor is $Q_{0}$, which can also be $q(t=0)$, while the voltage across it is $V_{0}$ or $v_{c}(t=0)$
- According to Kirchhoff’s Current Law (KCL), $i_{C}+i_{R}=0$
- Through derivations, $v(t)=V_{0}e^{-t/\tau}$
- The larger the time constant $\tau$, the longer it will take for the voltage to decay to 0

## RC Circuit with a Source

- When a source is connected, there will be no current flowing through the capacitor because it stops once it is filled; hence, it will be an open circuit and all resistors in series with it will be disregarded
	- The capacitor’s voltage ($V_{0_{C}}$) will be equal to the resistor parallel to it

## RC Time Constant

$$
\tau = RC
$$

- It tells us how fast the capacitor will discharge or charge
	- The larger the capacitor the more charge it could take; therefore, the larger the time constant too
- The larger the resistor, the greater the opposition to the flow of current; thus, it would take longer for the capacitor to discharge and would increase the time constant magnitude
- One time constant means a drop in 36.8% of the voltage stored in the capacitor

## RL Time Constant

$$
\tau = \frac{L}{R}
$$

 - Because the inductance ($L$) resists the change in current, it delays the current from reaching its steady-state value; thus, the larger the inductance, the larger the time constant.
 - Because the resistance reduces the current, it lessens the change in current and, therefore, making it quicker for the current to reach its steady-state. In other words, as resistance increases, the time constant decreases.

## RL Circuit with a Source

- The inductor acts like a short-circuit when a voltage source is connected; hence, all resistors parallel to it will be disregarded.
	- The inductor’s current ($I_{o_{L}}$) will be equal to the resistor in series with it.
- If there are more than two currents and a current source, you can use the current divider principle by putting the resistors you are not interested in finding the current in the numerator and the sum of two products of each parallel resistors at the denominator. Multiply the result with the current source afterwards to find the current of a particular resistor.

## RL Circuit without a Source

- The capacitor’s current after the voltage source has been disconnected is $i(t)=i_{0}e^{-t/\tau}$

## General Strategy for Solving RC Circuits

1. Find the following
	1. $v_{C}(t=0)$
	2. $v_{C}(t=\infty)$
	3. $\tau=RC$
2. Solve for the equation
	1. $v_{c}(t)=v_{C}(\infty)+[v_{C}(0)-v_{C}(\infty)]e^{-t/\tau}$

## General Strategy for Solving RL Circuits

1. Find the following
	1. $i(t=0)$
	2. $i(t=\infty)$
	3. $\tau=\frac{L}{R}$
2. Solve for the equation
	1. $i_{L}(t)=i_{L}(\infty)+[i_{L}(0)-i_{L}(\infty)]e^{-t/\tau}$

> [!TIP]
> You can use Kirchhoff’s Voltage Law(KVL) to check your answers

## Sources

1. [Introduction to RC and RL Circuits](https://youtu.be/uXuuJOdQoO4)
2. [RC Circuit without Voltage Source](https://youtu.be/i-4S3nYiF9Y)
3. [RC Time Constant](https://youtu.be/GXUzJ3a4Dpk)
4. [RC Circuit Example 1](https://youtu.be/j-2gxZ0svgQ)
5. [RC Circuit Example 2 Part 1](https://youtu.be/8JzYj1p6vOQ)
6. [RC Circuit Example 2 Part 2](https://youtu.be/BMX3iYSxoAQ)
7. [RC Circuit Example 3](https://youtu.be/K4PaoIKAvX0)
8. [L/R Time Constant](https://youtu.be/dekDAFiRFsk)
9. [RL Circuit Example](https://youtu.be/mGINjDi3c_Q)
10. [RL Circuit Example 2](https://youtu.be/pd8cEL8hhi8)
11. [RL Circuit Example 3](https://youtu.be/lR9iR9u2bRE)
12. [General Strategy of Solving RC Circuits](https://youtu.be/N0vcIGaXsn4)
13. [General Strategy of Solving RC Circuits Example](https://youtu.be/j-1fh9R37fY)
14. [General Strategy of Solving RL Circuits](https://youtu.be/ZYrO0I35mho)
15. [General Strategy of Solving RL Circuits Example](https://youtu.be/NQQxDu-c_h0)
