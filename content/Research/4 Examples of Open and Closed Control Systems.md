---
draft: false
title: 4 Examples of Open and Closed Control Systems
date: 2024-09-13
aliases: []
tags: [Physics/Electricity-and-Magnetism]
---

## Sources

1. Farhan Sheikh, EEEProject, “[Open Loop System \[Explained\] in Detail](https://eeeproject.com/open-loop-system/)” - 2017-09-18, [archived](https://archive.md/NAjCq) on 2024-09-13
2. El Pro Cus, “[What is an Open Loop Control System & Its Working](https://www.elprocus.com/what-is-an-open-loop-control-system-its-working/)” - Accessed 2024-09-13
3. Vivien Beverley Fletcher, “[Systems Approach Universal System](https://slideplayer.com/slide/6448199/)” - 2015
4. D. Hoyt, Y. Adonyi, S. Kim, Welding Journal, “[Microwave Joining — Part 1 : Closed Loop Controlled Microwave Soldering of Lead Telluride to Copper](https://s3.amazonaws.com/WJ-www.aws.org/supplement/WJ_2016_04_s141.pdf)” - 2016
5. Electronics Coach, “[Examples of Closed-Loop Control System](https://electronicscoach.com/examples-of-closed-loop-control-system.html)” - Accessed on 2024-09-13
6. Ravi Teja, ElectronicsHub, “[Closed Loop System: How It Works & Examples](https://www.electronicshub.org/closed-loop-system/)” - 2024-06-21
7. Electronics Tutorials, “[Closed-loop Systems](https://www.electronics-tutorials.ws/systems/closed-loop-system.html)” - Accessed on 09-13-2024

## Basic Parts

1. **Reference input:** an external signal applied to the summing point
2. **Summing point:** sum of all inputs
3. **Control elements:** controls the process by sending a *control signal*
4. **Plant:** the system controlled by the feedback control system
5. **Controlled output:** output of the plant
6. **Feedback elements:**

## Open Loop Systems

### 1. Clothes Dryer

- It does not depend on the output and will stop based on the timer.

| Function                   | Component       |
| -------------------------- | --------------- |
| Reference Input ($r$)      | Timer           |
| Control Elements ($g_{1}$) | Controller      |
| Plant ($g_{2}$)            | Heating element |
| Controlled Output ($c$)    | Clothes Dryness |

### 2. Traffic light

| Function                   | Component            |
| -------------------------- | ---------------      |
| Reference Input ($r$)      | Internal Timer       |
| Control Elements ($g_{1}$) |     Controller        |
| Plant ($g_{2}$)            | Traffic Lights        |
| Controlled Output ($c$)    | Traffic Signal Output |

### 3. Flashlights

| Function                   | Component    |
| -------------------------- | ------------ |
| Reference Input ($r$)      | Light Switch |
| Control Elements ($g_{1}$) | Controller   |
| Plant ($g_{2}$)            | Bulb         |
| Controlled Output ($c$)    | Light        |

### 4. Water Faucet

| Function                   | Component   |
| -------------------------- | ----------- |
| Reference Input ($r$)      | Tap Handle  |
| Control Elements ($g_{1}$) | Valve       |
| Plant ($g_{2}$)            | Water Level |
| Controlled Output ($c$)    | Flood       |

## Closed Loop Systems

### 1. Microwave

| Function                   | Component                        |
| -------------------------- | -------------------------------- |
| Reference Input ($r$)      | Temperature and Time Selector    |
| Control Elements ($g_{1}$) | Controller                       |
| Plant ($g_{2}$)            | - Motor </br>- Fan </br>- Heater |
| Controlled Output ($c$)    | Heat                             |
| Feedback Elements ($h$)    | Thermostat                       |

### 2. Temperature Control System

| Function                   | Component                        |
| -------------------------- | -------------------------------- |
| Reference Input ($r$)      | Temperature Selector             |
| Control Elements ($g_{1}$) | Valve                            |
| Plant ($g_{2}$)            | Tank                             |
| Controlled Output ($c$)    | Achieved Temperature             |
| Feedback Elements ($h$)    | Pressure Thermometer             |

### 3. Current Limit Control

| Function                   | Component                        |
| -------------------------- | -------------------------------- |
| Reference Input ($r$)      | Current            |
| Control Elements ($g_{1}$) | Controller                            |
| Plant ($g_{2}$)            | - Converter </br>- Motor                             |
| Controlled Output ($c$)    | Load             |
| Feedback Elements ($h$)    | Current Sensor             |

### 4. Motor Controller

| Function                   | Component                        |
| -------------------------- | -------------------------------- |
| Reference Input ($r$)      | Desired Speed           |
| Control Elements ($g_{1}$) | - Gain</br>- Op-Amp                            |
| Plant ($g_{2}$)            | - DC Motor</br>- Rotating Shaft |
| Controlled Output ($c$)    | Actual Speed           |
| Feedback Elements ($h$)    | Tachometer             |
