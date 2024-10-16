# cmos_inverter_design
I have designed and tested a CMOS inverter using Cadence Virtuoso Software.

## Introduction:

A CMOS inverter is a fundamental digital logic circuit used in electronics, particularly in integrated circuits. It operates by inverting the input signal, turning a logical '1' (high voltage) into a logical '0' (low voltage), and vice versa. CMOS stands for Complementary Metal-Oxide-Semiconductor, a technology that uses both p-type and n-type MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors) to achieve low power consumption and high efficiency.
Structure of CMOS Inverter:
•	The CMOS inverter consists of two transistors:
o	PMOS (P-channel MOSFET): Connected between the output and the positive power supply (VDD). It is ON when the input is LOW and OFF when the input is HIGH.
o	NMOS (N-channel MOSFET): Connected between the output and the ground (VSS). It is ON when the input is HIGH and OFF when the input is LOW.
Working:
•	Input is LOW (0): The PMOS transistor conducts, connecting the output to VDD (logic high). The NMOS transistor is off, isolating the output from the ground, making the output HIGH.
•	Input is HIGH (1): The NMOS transistor conducts, pulling the output to ground (logic low). The PMOS transistor is off, isolating the output from VDD, making the output LOW.

## Schematic Design:

![Screenshot 2024-10-14 214707](https://github.com/user-attachments/assets/7d792820-b84e-445b-9dd7-ef943c26528a)

## Symbol:

![Screenshot 2024-10-16 220121](https://github.com/user-attachments/assets/d52f7c10-8e44-41a7-91cf-51c12abe6bd4)

## Designing the testbench:

![Screenshot 2024-10-14 214652](https://github.com/user-attachments/assets/738e5107-1ffa-4605-953f-186e45e23c8f)

## Transient Analysis Waveforms:

![Screenshot 2024-10-14 214606](https://github.com/user-attachments/assets/36b2892c-9dad-452d-9621-d4888271711e)

## Layout:

The layout of a CMOS inverter represents the physical implementation of the design on a silicon chip. It defines how the components (PMOS and NMOS transistors, metal interconnects, etc.) are arranged and how they are connected.

![Screenshot 2024-10-14 222825](https://github.com/user-attachments/assets/c80af197-0883-40e6-9e54-03d9bb0bb44d)

## AV_extracted View:

The AV extracted view (Assura Verified Extraction) is a more detailed representation of the circuit after the layout. It includes parasitic elements like resistances and capacitances that are inevitable in real-world fabrication but are not present in the ideal circuit. After creating the layout, the extracted view is used to verify how the physical layout will behave in terms of electrical performance. It helps check for issues like parasitic resistances, capacitances, and cross-talk between metal layers.

![Screenshot 2024-10-14 222756](https://github.com/user-attachments/assets/e82e0931-4db5-43c6-b045-a827b69d2475)

## Layout vs Schematic:

![Screenshot 2024-10-14 231414](https://github.com/user-attachments/assets/009111b0-b7c8-4a7a-9fd0-ee644ab28b35)

## Delay Estimation:

![Screenshot 2024-10-15 013926](https://github.com/user-attachments/assets/334d0470-e905-441f-950d-521c44e8194c)
![Screenshot 2024-10-16 130959](https://github.com/user-attachments/assets/313c1846-2b8a-4ded-9e32-cd4b3f163be5)

## Power Dissipation:

![Screenshot 2024-10-16 132456](https://github.com/user-attachments/assets/79f791ee-28de-4a4b-b5f9-21439bae3d3e)
![Screenshot 2024-10-16 132326](https://github.com/user-attachments/assets/81f4d515-d540-4c4b-8b6f-7ab4062dab82)

## Noise Margins:

Noise margin is a critical concept in digital circuits, such as a CMOS inverter, which defines the ability of a logic gate to tolerate noise (unwanted electrical signals) without misinterpreting the input signal.

To calculate the noise margin we first take the derivative of the dc analysis curve and at -1V we get two horizontal intercepts denoting VIL and VIH.

*NMH = VOH−VIH* = 1.2V - 0.614V = 0.586V

*NML = VIL−VOL* = 0.314V - 0 = 0.314V

![Screenshot 2024-10-16 133843](https://github.com/user-attachments/assets/9084b361-f66f-4f21-8d46-1ffdd46a1553)
