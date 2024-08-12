---
draft: false
tags: [Physics/Electricity-and-Magnetism]
title: AC to DC Conversion
date: 2024-08-12
aliases: []
---

## Theory

1. Transformer: Inducing Voltage
	- The number of windings in a transformer determines how much change in voltage we can obtain
	- Currents introduced through windings produces a magnetic field, with poles forming along the winding axis. A second coil placed near the winding axis will induce a current due to the magnetic field, thus also generating voltage.
	- Adding a magnetically permeable core between coils enhances the induced current effect and reduces the loss.
	- You can wrap windings and the core together to save space and get a desired voltage. This is because the windings are made of insulated wires. Nevertheless, it only outputs AC because it requires magnetic coupling to work—ac currents allow magnetic fields to change polarity by switching between positive and negative voltages at 50 to 60 Hz.
2. Rectifier: Constant Polarity
	- Using the full-wave rectifier, we convert negative AC pulses to positive ones, and also keep the positive pulses. Doing this will lead to a pulsed DC voltage that goes from 0 to 120 Hz.
		- We can create a full-wave rectifier using individual discrete diodes, or use a diode particularly made for that purpose.
		- Full-wave rectifiers are chosen instead of half-wave ones because it reduces the time between high and low pulses, which in turns produces a more stable output
	- The voltage required in diodes results in a small amount of voltage loss
3. Capacitors: Rippling Minimization
	- Capacitors are used across the ‘+’ and ‘-’ terminals to smooth out the ripples from the resulting pulsed DC voltages. The capacitor charges from 0 to the maximum pulsed DC voltage (120 Hz).
	- As the voltage drops, the capacitors discharges at a slower rate until the supply has 0 voltage. Afterward, the voltage rises again and eventually recharges the capacitor, then the cycle repeats
	- Larger capacitors lets voltage stay higher for a longer period of time, thus less rippling
4. Voltage Regulator: Stabilizing and Specifying Voltage Output
	- as long as the ripple doesn’t drop to a particular value (like +12VDC), we can use it for powering a voltage regulator
		- voltage regulators stabilizes a wobbly input voltage to a specific output voltage

> [!INFO]- Full-Wave Rectifier
> - Williams, B. W. (1992). “Chapter 11”. Power electronics : devices, drivers and applications (2nd ed.). Basingstoke: Macmillan. ISBN 978-0-333-57351-8.
> 	- Like a absolute function, full-wave rectifiers convert the entirety of the input waveform into a value with a constant polarity.
> 	- It converts the polarities into a pulsating DC and gives greater average output voltage

> [!INFO]- Diode Bridge
> - Williams, B. W. (1992). “Chapter 11”. Power electronics : devices, drivers and applications (2nd ed.). Basingstoke: Macmillan. ISBN 978-0-333-57351-8.
> 	- Four diodes in a bridge configuration are essential in creating a full-wave rectifier; otherwise, a center-tapped transformer with two diodes are used.
> - Yazdani, Amirnaser; Iravani, Reza. Voltage-Sourced Converters in Power Systems Modeling, Control, and Applications. Willey. ISBN 9780470521564.
> 	- Diode bridges are bridge rectifiers of four diodes. They are utilized for converting AC from input terminals to DC on the output terminals.
> 	- This is done by converting negative portions of the input AC waveform to positive, which is then smoothed out using a low-pass filter for the resulting DC output.

> [!INFO]- Transformer
> - Bedell, Frederick (1942). “History of A-C Wave Form, Its Determination and Standardization”. Transactions of the American Institute of Electrical Engineers. 61 (12): 864. doi:10.1109/T-AIEE.5058456. S2CID 51658522.
> 	- A transformer is a passive component which transfers energy from one circuit to another circuit (or circuits)
> 	- It induces a varying voltage when one of the coils in the transformer’s coil produces a varying magnetic flux (Faraday’s law of induction)

> [!INFO]- Voltage Regulator
> - [Original Link](https://pact.in/blog/2024/04/automatic-voltage-stabilizer), [Archived Link](https://archive.md/IRz9y)
> 	- It is a system for automatically stabilizing voltage. Depending on the design, it can regulate one or more AC or DC voltages.

## Practical Parts

Schematic from instructible:
![Schematic](https://content.instructables.com/FIE/C85T/HX504L7L/FIEC85THX504L7L.png?auto=webp&frame=1&width=1024&fit=bounds&md=abe8f491deaca1d589645591ba9e67c2)

1. Prerequisite Info
	- The AC power cable connects to the primary winding side of the transformer
	- The bridge rectifier connects to the secondary winding side of the transformer
	- Once the power cable is plugged in, the multi meter will be used to check the output voltage on the secondary pins
		- A transformer with a 10:1 step down ratio is needed for 220VAC mains; majority of voltage regulators are limited to 35VDC input at most.
	- Be aware of the circuit’s power requirements. Transformers have current limitations; voltage regulators are commonly restricted to sourcing 1 amp maximum.
	- Attach a proper heat sink. If you’re unsure, use fuses.
2. Parts
	- 1 transformer
	- 5 diodes or a purpose build bridge rectifier with an additional diode
		- The latter will require 1 additional diode to reverse bias the regulator output.
	- 4 capacitors
		- Ensure that the voltage ratings of the capacitors are higher than the voltages they will be experiencing (i.e., a diode bridge yielding +30VDC will be incompatible with a capacitor rated for +25VDC, and might result in an explosion)
	- a voltage regulator
		- Ensure that the transformer’s output stays at least 2V above the output level of the regulator, since it will regulate down to the output voltage required.
	- wires
	- heat sink
		- [Original Link](https://www.ti.com/lit/an/slva462/slva462.pdf), [Archived Link](https://archive.md/Fh2HD)
		- necessary when the voltage regulator is yielding high current or the input voltage is considerably higher than the output voltage.
3. Tools
	1. solderless breadboard (for prototyping and testing)
	2. soldering iron and solder
	3. printed circuit board
	4. wire cutters/strippers

## Results Explanation (From Instructables)

Image 3:
![Image 3](https://content.instructables.com/F78/Z66P/HX504MHX/F78Z66PHX504MHX.png?auto=webp&frame=1&fit=bounds&md=407cc2468f5e1c6ff7ab5de6e46781de)

Image 4:
![Image 4](https://content.instructables.com/FSM/2HKR/HX504MHI/FSM2HKRHX504MHI.png?auto=webp&frame=1&fit=bounds&md=00e2054a8d1dca290621c5f245bc933f)

> Images 3 and 4 are o-scope images to show what is going on in the circuit. After the transformer steps down the AC voltage the diode bridge makes the signal DC, but with some serious fluctuations. Image 4 shows why we add the smoothing capacitor. This image was taken with a smaller capacitor so I could highlight the effect the capacitor has on the signal

Image 5:
![Image 5](https://content.instructables.com/FA8/QINR/HX504MHH/FA8QINRHX504MHH.png?auto=webp&frame=1&fit=bounds&md=86a372bb2fedc9962c40ec6c3c7123ce)

> Image 5 shows the final regulated DC voltage at +4.8VDC. The datasheet for the 7805 shows that 4.75-5.25VDC is normal, so we are well within specs.

## LTSpice Designing

- Parts
	- Transformer
		- For stepping the voltage down to another level
		- ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAb1BMVEX///8AAABgYGDb29svLy+Ghobu7u7n5+fOzs78/Pz29vZ5eXnGxsbg4OCTk5Pz8/Orq6s5OTlsbGw+Pj4qKipVVVWbm5uxsbHW1tZycnK+vr6lpaWAgIAlJSVaWloMDAwbGxu3t7dISEhGRkZQUFCFXZ2DAAAEIklEQVR4nO2aa1uqQBRG2V4QBclLmrfMyv//Gw+kKdVAWx10e1rrWyPNs18dYC4rCAAAAAAAAAAAAAAAAOCahM1zmfV7NdfW68/Orq5z6CWWS3iOB/1awvUH8eNFlcWHrpbrxplsJ+PnvK/WNPQcL5y2Pr6+4WRybnHrpadaOlGaFzPqVF4VJcUfup9E1X3mw6qVRtV9XpNO+pINiqp7ciOrwl8r2VRc211l+VI76XZ0l1lVFT9MS9qFv9rSKr802ohMu94q80dvlBVW+qk+4TQb8Q8e6/LJovj4+oY6YTZCn7xW5ZX+y5ccRbQJ2yIzz1V5JSwdqMqEAxFrT5hvdEQS5we6hE3jv2DOq4izXZWw+yiDOoryy0hSV7Mq4VLWtdTkl+xWdD3rNQm7Ir4nf7XQdj5sNAkHMq+pJr90nNVrErakWVNNnhmKYzWlSBhWTeVMkbomJYqEi9LpgjUiV6WKhKm81laTX/oy+dmoSDiy/7bf47yfFAkbzteMRUJ5/NmoSlj3tpYvOjL+2ahKaHzSfaDpenErEsYlk3Z7PLlmpoqES/G1OVY3c9d+jSLhzPUMNolz6q2Ztbnn7PZYSMPRqkkYW96hKTB2bipqEjZlU0tFnnmVN1ezagU8uYclfu/FPfdSJWzewxJ4W7KK1e1EpfJeQ01eyUp378crdxOHMvJflE/S0u1OZcJQbC8SR+X7udo97/DF+bKxQX8sm9LTYPW5RbiRR6PbNdkIfS+fk+jPnnrrbKTaO1x7yI8Py8/WTjo/zKbuWV+mXhu9ZP7rMfcpCYMwP+RuLAwsiLtJkjyttrlSsPrFxzgpYbaKbuedvsWDJIluOWKbe61j+PvS9cSEGdF433s9LouOTms8/LBNxr/eNqcmDKfjnW3yPrz53obONjkt4T3aJqck7LaxTW4Dtgm2yecntk8vsE0+wTYxDbbJB9gmtsE2ycE2MQ62SYBtYh5skwDbxDzYJgG2iXWwTXKwTSyDbbID28Qu2CafYJt4rcsb2CbYJgWs2SYTbJMcbJPvYJtcm51tUnXDYJsUwDa5IdgmR7BNDINtsgfbxDTYJvtrsE1Mg20SYJuYB9skwDYxD7ZJgG1iHmyTANvEOtgmOdgmlsE2OVzm/n9sk1uDbXIA2wTb5Npgm+Rgm/wE2+R6YJvswDYpgG1yQ7BNjmCbGAbbZM8ftk3uYdcb22R/DbaJabBNAmwT82CbBNgm5sE2CbBNzINtEmCbWAfbJAfbxDKX2SZtbJObg23yCbaJ17q88ddtk+cvCVeuJeSB+7RN5uviwmG5rtwZ9W6bhM1zmc20tsmJHG2TaHZ2dcevPJbLeJ4vvMbbkcStC+s6Htcu140z2Y7ag0VY22MhTAbpfHtucet7WVADAAAAAAAAAAAAAAAAAADA/8I/jtBK8jqYE5UAAAAASUVORK5CYII=)
	- Diode Bridge
		- For rectification
		- ![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5YB27XRTWhWa0gnuJXppd8FQoBpdEHl2RNA&s)
		- ![](https://www.shindengen.com/products/semi/column/files/images/bridgediode01_1.png)
	- Capacitor
		- For smoothing voltage and provide the voltage dc traits
	- LM317 circuit or voltage regulator
		- for decreasing the voltage
		- ![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvY07KuNBbtHWgmCuVNo8RiLXh0J3Z6gZeQYUsUeow37AZj87rjHQlCoErYWo19GxfC4w&usqp=CAU)

1. Voltage Source
	1. Sin Wave
	2. Amplitude: 311 V
		1. Although the voltage is 220V, you cant directly input that, so just use an internal series resistance of 30 milliohms to convert it from 311 to approximately 220
	3. Freq: 60 Hz
2. Transformer
	1. Steps the voltage enough to a level that LM317 can receive (37 V)
	2. 100 micro henry and 3 micro henry (L1 and L2)
3. Diode bridge
	1. For rectification
	2. 1N4007
4. Capacitor
	1. Lets the input voltage possess dc characteristics
	2. Voltage ripples as a result of periodic recharge and discharge
	3. 100 microFarad
5. 1k ohms Resistor
6. Voltage regulator
	1. The LM317 voltage regulator decreases the value to the desired dc voltage
7. Resistors
	1. Use the resistors to turn the resulting voltage into the desired dc voltage output
8. DC Output
	1. 15 V

## Sources

1. <https://www.instructables.com/AC-to-DC-Conversion/>, [Archived Link](https://archive.is/2WLp8)
2. Williams, B. W. (1992). “Chapter 11”. Power electronics : devices, drivers and applications (2nd ed.). Basingstoke: Macmillan. ISBN 978-0-333-57351-8.
3. Yazdani, Amirnaser; Iravani, Reza. Voltage-Sourced Converters in Power Systems Modeling, Control, and Applications. Willey. ISBN 9780470521564.
4. Bedell, Frederick (1942). “History of A-C Wave Form, Its Determination and Standardization”. Transactions of the American Institute of Electrical Engineers. 61 (12): 864. doi:10.1109/T-AIEE. S2CID 51658522.
5. <https://pact.in/blog/2024/04/automatic-voltage-stabilizer,> [Archived Link](https://archive.md/IRz9y)
