---
draft: false
title: Capacitors
date: 2024-07-02
aliases: []
tags: ["Physics/Electrical-Engineering"]
---

A capacitor has two plates with a dialectric in between. When connected to a voltage source, the positive charges goes to one plate, which repels the positive charges on the opposite plate and results to the lack of positive charge in that opposite plate. In addition, the positive charges of the opposite plate is also attracted to the negative side of the voltage source.

The positive charge on one plate and the other negative charge on the other plate generates an electric field in the capacitor.

## Capacitance

Two ways to find the capacitance:

1. The charge collected on the plates relative to the voltage used to drive the charge to the plates
	- $C=\frac{Q}{V}$ \[Farads\]
2. The proportion between the size of the plates and the distance between them
	- $C=\epsilon_{0} \frac{A}{d}$ \[Farads\]
		- $A$ = area of the plates
		- $d=$ distance between the plates
		- $\epsilon_{0}=8.85 \times 10^{-12} [\frac{C^2}{Nm^2}]$

## Equivalent Capacitance

When dealing with a parallel capacitor

$$C_{eq}=C_{1}+C_{2}+\dots+C_{N}$$

When dealing with a series capacitor

$$ C_{eq}=\left(\frac{1}{C_{1}}+\frac{1}{C_{2}}+\dots+\frac{1}{C_{N}}\right)^{-1} $$

## Charge and Voltage

1. When the capacitors are in series
	- The charge will be equal for each capacitor
	- $V=\frac{Q}{C}$
2. When the capacitors are in parallel
	- The voltage will be equal for each capacitor
	- $Q=CV$

## Energy

1. Because $i=C\frac{dv}{dt}$ and $p=iv$, $p=\left( C \frac{dv}{dt} \right)v$
2. Because $\displaystyle u=\int^t_{t_{0}} p \, dt$, $\displaystyle u=\frac{1}{2}Cv^2$ (after some derivations)
	1. $u$ is energy

## Capacitors with Current Source

To compute for the currents

1. At steady state—when capacitors are filled up with charge—we remove the capacitors because there is no current through those capacitors.
2. Compute for the currents across the resistors

To compute for the voltage drop across the capacitors

- The voltage drop is the same as the resistor parallel to it

## Sources

1. [Capacitors](https://youtu.be/wR1IfIHj-LA)
2. [Equivalent Capacitance](https://youtu.be/DmyWlwbixO8)
3. [Finding the Charge On & Voltage Across Capacitors](https://youtu.be/HQjUUN7Cff4)
4. [Energy and Capacitors](https://youtu.be/SNrmAFEgivQ)
5. [Equivalent Capacitance 2](https://youtu.be/tAejkZoXONo)
6. [Capacitors with Current Source](https://youtu.be/4XuZwG6pzhM)
