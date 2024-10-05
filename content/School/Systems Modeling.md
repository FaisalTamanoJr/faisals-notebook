---
draft: false
title: 2024.10.05 Laplace Transforms and Systems Modeling (Lab Introduction Info Research)
date: 2024-10-05, 10:29
aliases: []
tags: []
---

## Sources

1. Control Tutorials for MATLAB & Simulink, “[Introduction: System Modeling](https://ctms.engin.umich.edu/CTMS/index.php?example=Introduction&section=SystemModeling)” - Accessed on 2024-10-05
2. Byju’s, “[Laplace Transform](https://byjus.com/maths/laplace-transform/)” - Accessed on 2024-10-05
3. Electrical4U, “[Transfer Function of Control System](https://www.electrical4u.com/transfer-function/)” - 2024-04-17
4. Tutorialspoint, “[Modelling of Mechanical Systems](https://www.tutorialspoint.com/control_systems/control_systems_modelling_mechanical.htm)” - Accessed on 2024-10-05
5. Dr. Nhut Ho, University Northridge “[Modeling Electrical Systems](https://www.ecs.csun.edu/~nhuttho/me584/Chapter%204%20Electrical%20Systems_for%20class_part%201.pdf)” - Accessed on 2024-10-05

## 1. System Modeling

- The first step to designing control system processes is to produce the right mathematical model to represent the system to be controlled.
	- This can either be derived from physical laws or from experimental data.

### Basic Parts of Dynamic Systems

*Dynamic systems* are systems that evolve over time according to a fixed rule, typically expressed as first-order differential equations.

> [!EXAMPLE] Example 1
>
> $$
> \dot{x}=\frac{dx}{dt}=f(x(t),u(t),t)
> $$
>
> - $f$ is the function producing the rate of change $\frac{dx}{dt}$
> 	- It can be **time-invariant** if it does not depend on time, thus, $\dot{x}=f(x,u)$
> - $x(t)$ (or the state variables) is the configuration of the system at time $t$
> 	- may depend on time even if the function $f$ itself is time-invariant
> - $u(t)$ (or the control inputs) is the vector containing the external inputs
> 	- may depend on time even if the function $f$ itself is time-invariant

Given the **initial state** $x(t_{0})$ and the **time history of inputs** $u(t)$ between $t_{0}$ and $t_{1}$, we can **integrate** the system equation (at Example 1) to determine any of the system’s future state.

$n$ is referred to as the *system order*, which is used for determining the dimensionality of the *state-space*. It also indicates the minimum number of state variables needed to solve state equations or predict the system’s future behavior.

> [!NOTE] Linearity of Dynamic Systems
> Although, in reality, most physical systems are nonlinear, many of them are also approximately linear at a certain range of values.

Before the introduction of more advanced computers, scientists and engineers only analyzed *linear time-invariant (LTI)* systems. As a result, control theory was predominantly founded on these assumptions. Moreover, they solved many engineering challenges using LTI techniques.

### State-Space Representation

> [!INFO] Standard State-Space Representation for LTI Systems
>
> $$
> \begin{align}
> \dot{x}&=Ax+Bu \\ y&=Cx+Du
> \end{align}
> $$
>
> - $x$ is the state variables vector
> - $u$ is the input/control vector
>
> - $\dot{x}$ is the time derivative of the state vector
> - $A$ is the system matrix
> - $B$ is the input matrix
>
> - $y$ is the output vector
> - $C$ is the output matrix
> - $D$ is the feedforward matrix

- The output vector $y$ and its equation is useful due to the existence of state variables which are often not directly observed.
- $C$ defines which states variable the controller can use.

## 2. Laplace Transforms

- *Laplace transform* is useful for reducing differential equations into algebraic ones. For this reason, they play a large role in control system engineering.
- It is an integral transform that converts a derivative function with $t$ to a complex function with $s$. It is defined by the formula

$$
F(s)=\int ^{+\infty}_{0} f(t)\cdot e^{-s\cdot t}\, \cdot dt 
$$

- The purpose of Laplace transform is to transform equations into easier problems.
- Laplace transform is used in engineering fields for applications such as electrical circuit analysis, system modeling, and digital signal processing because these usually involved differential equations.

## 3. Transfer Functions

- *Transfer function* pertains to the ratio of the Laplace transform, assuming that the initial conditions are non-existent, of an output to input of a specific system.
	- The impulse input is related to the output because of the resulting transfer function that can be extracted.
	- $G(s)=\frac{C(s)}{R(s)}$
- Poles and zeros are useful to know where the transfer function approaches infinity or zero. In this regard, they can also play a major role in influencing a system’s behavior.
- In control system analysis, the Laplace transform allows for a consistent representation of various signal types.
- To find the transfer function, we would need to get equations for the system, then their Laplace transform (with initial conditions set to 0). Afterward, we determine a system output and input, then produce the ratio needed in a transfer function (output divided by input).
- Although systems have varying kinds of signals, they can be uniformly represented using their Laplace form.

## 4. Modelling of Mechanical Systems

### Translational Mechanical Systems

- Unlike rotational mechanical systems, they only move along a straight path.
- 3 basic elements of translational mechanical systems
	1. mass
		1. $F=M\frac{d^2x}{dt^2}$
	2. spring
		1. $F=Kx$
	3. damper
		1. $F=B\frac{dx}{dt}$
- The net force is 0 due to applied and opposing forces being in directions that counter act one another.

### Rotational Mechanical Systems

- In contrast to translational mechanical systems, they move about a fixed axis.
- Three basic elements of rotational mechanical systems
	1. moment of inertia
		- $T=J\frac{d^2\theta}{dt^2}$
	2. torsional spring
		1. $T_{k}=K\theta$
	3. dashpot
		- $T=B\frac{d^2\theta}{dt^2}$
