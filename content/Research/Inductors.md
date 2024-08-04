---
draft: false
title: Inductors
date: 2024-07-02
aliases: []
tags: ["Physics/Electricity-and-Magnetism"]
---

An inductor is a wire wrapped around a tube that resists the change in current: if the current tries to increase, the inductor keeps it from increasing; if the current tries to decrease, the inductor keeps it from decreasing.

$$
L={\frac{N^{2}\mu A}{\ell}}
$$

> [!NOTE]
> - $L =$ the constant of proportionality or the inductance (in henry \[H\])
> - $N =$ the number of times the wire loops around the tube
> - $\mu =$ the permeability of the core—the capacity of the magnetic field to stay inside the tube relative to what is in it
> - $A =$ the cross-sectional area of the tube
> - $\ell =$ the length of the tube

There is a magnetic field around the current-carrying wire; as a result, it produces a magnetic field inside the tube.

The voltage across an inductor is

$$
 v=L \frac{di}{dt} 
$$

In comparison to other circuit elements

- Resistors have *resistance* to oppose the current
- Capacitors have *capacitance* or the capacity to store charges
- Inductors have *inductance* to oppose the change in current

## Energy

Although the inductor initially opposes the change in current, the current will eventually flow through it and establish a magnetic field. This magnetic field will increase alongside the current flowing through the inductor; hence, it stores some amount of energy.

Because

$$
p=L i \frac{di}{dt}
$$

we can derive the total work/energy and get

$$
 w = \frac{1}{2} Li^2 
$$

## DC Current

When a current is suddenly applied from a DC source, it does not instantly reach its final value because the inductor opposes the change in the current of the circuit. The time it takes to approach its final value depends on the time constant ($\tau = \frac{L}{R}$); usually, the current reaches more than 99% of its final value after 5 time constants.

To find the current at any point in time, use the following equation:

$i(t)= i_{final}(1-e^{-t/\tau})$

The final/steady-state value of the current can be obtained by solving for it when it is no longer opposed by the inductor (i.e., the inductor acts like a short circuit).

## Current and Voltage

To find the voltage across the inductor given current and inductance

$$
v(t)=L \frac{di(t)}{dt}
$$

On the other hand, given the voltage, we can find the current through

$$
 i=\frac{1}{L}\int_{0}^t v \, dt  
$$

## Series and Parallel Inductors

When inductors are in series

$$
L_{eq}=L_{1}+L_{2}+\dots+L_{N}
$$

When inductors are in parallel

$$
L_{eq}=\left(\frac{1}{L_{1}}+\frac{1}{L_{2}}+\dots+\frac{1}{L_{N}}\right)^{-1}
$$

## Sources

1. [Inductors](https://youtu.be/z-C-tu-80jA)
2. [Energy Stored in the Inductor](https://youtu.be/WnFFlE2u3rM)
3. [DC Current through an Inductor](https://youtu.be/WR6qVvnDnI4)
4. [Inductors: Given Current, Find the Voltage](https://youtu.be/Ngi2MMQVNk0)
5. [Inductors: Given Voltage, Find the Current](https://youtu.be/-moS7PVIRA8)
6. [Equivalent Inductance Example 1](https://youtu.be/AEg_cW9ozaY)
7. [Equivalent Inductance Example 2](https://youtu.be/qlb2SK9hRwA)
