---
draft: false
title: LBYCPC3 Project Proposal Notes
date: 2024-10-16, 10:14
aliases: []
tags: []
---

## Sources

1. RealPars, “[PID Controller Explained](https://youtu.be/fv6dLTEvl74)” - 2021-12-20
2. MATLAB, “[Everything You Need to Know About Control Theory](https://youtu.be/lBC1nEq0_nk)” - 2022-10-27

## Terminologies and Basic Concepts

- *State observers* or *point estimators* are systems that give an estimate of the internal state of a given real system. One use of it is in stabilizing a system through state feedback.
- *Filters* in control system can improve a system’s performance and stability by removing unwanted noise or disturbance from either input or output signals.
- *Error* is the difference between the **setpoint** and the **process variable**
- *Degree of Freedom* are the number of variables that can be controlled in the process

### Controllers

- Controllers ensure that the process is as close as possible to the desired output regardless of disruptions. It does this by comparing the *transmitter process variable* (or PV signal) and the **setpoint**
- An *on-off controller* turns on when the measured is below the desired output and turns off when the measured is above the desired output.
- *Proportional-integral-derivative (PID) controller* determines the appropriate amount and speed for correction.
	- Proportional block creates an output signal proportional to the error signal’s magnitude
	- Integral block creates an output signal proportional to the error signal’s magnitude and duration
	- Derivative block creates an output signal proportional to the error signal’s rate of change
	- *Controller tuning* adjusts the P, I, and D depending on the specific process requirements

### Control Theory

Goal: To control a system.

Parts:

1. Reference $r$
2. Feedback/Feedforward controller
3. Control inputs $u$ - intentional inputs to control the system.
4. Disturbances $d$ - unintentional inputs that affect the system despite being unwanted.
5. System
6. States - the system’s states change as the system dynamics interact with the external inputs
	- We can measure it with a sensor, though it will introduce noise; therefore, returning an inaccurate measurement of the state to the controller
	- Challenges:
		1. Reduce measurement noise
		2. Observe the state in a way that we estimate it by manipulating the measurements
7. State estimation
	- depends on the amount and type of noise, the type of state

Types of Controllers:

1. **Feedforward or open loop:** It takes in a reference $r$ and generates a control input/signal without needing to measure the system state
	- Can be very vulnerable to disturbances/uncertainty
	- Changes how we operate a system
2. **Feedback or closed loop:** Uses the reference and the current state of the system to determine the appropriate control inputs
	- In a situation where disturbances or errors affect the system, the controller can adjust the control inputs accordingly (self-correcting).
	- Changes the dynamics of a system; hence, it is more dangerous.
		- It makes it so that the future state of the system is determined by the current state of the system.
	- Types of feedback controllers.
		1. *Linear*, such as PID and full state feedback, that assume that the system has a **linear** nature.
		2. *Non-linear*, such as on-off, sliding mode, and gain scheduling.
		3. *Robust*, such as mu synthesis and rejection control, that focuses on satisfying requirements even when with uncertainties.
		4. *Adaptive*, such as extremum-seeking and model-reference adaptive, that adapt to the system over time
		5. *Optimal*, such as linear quadratic regulator, which focuses on minimizing the total cost and balances effort and performance
		6. *Predictive*, such as model predictive control, which stores a model in the controller that simulates the future state and determines the best control input to make the future state correspond to the simulated model.
		7. *Intelligent*, such as reinforcement learning and fuzzy control, that determines the best controller based on data

Two ways of modeling:

1. Using first principles
2. Using system identification to fit a model to a given data

Steps:

1. Planning the right reference for the feedback controller to produce the right controller input
2. Determine if feedback or feedforward
3. Produce a mathematical model of the system
4. Estimate the state if feedback
5. Simulation, analysis and test to evaluate the performance of the designed system
