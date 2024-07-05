---
draft: false
title: Thevenin's theorem
date: 2024-07-02
aliases: []
tags: ["Physics/Electrical-Engineering"]
---

Related concepts: [[Superposition]]

Thevenin’s theorem is usually used to find the current through a *resistor load*.

It involves the conversion of a linear circuit into a Thevenin circuit—a circuit composed of a Thevenin voltage and resistor—which is then combined back with the resistor load.

Its purpose is to make it easier to find the load resistor’s current

$$
I_{R_{L}} = \frac{V_{TH}}{R_{TH}+R_{L}}
$$

## Thevenin’s Resistance

To find the Thevenin resistance:

1. Remove load resistor and current sources
2. Short the voltage sources
3. The combination of remaining resistance is the Thevenin’s resistance

## Thevenin’s Voltage

To find Thevenin voltage:

1. Remove the resistor load
2. Find the voltage across the open terminals

## Sources

1. [Thevenin's theorem](https://youtu.be/Mv7WETB8KG0)
2. [Thevenin's theorem example 1](https://youtu.be/jg_SPiM3bgI)
3. [Thevenin's theorem example 2](https://youtu.be/UUDRGTqdLrM)
