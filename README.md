# Simple Integrate-and-Fire Self-Resetting Neuron Design and Simulation Project

## Overview

The **Simple Integrate-and-Fire Self-Resetting Neuron Design and Simulation Project** focuses on the design, simulation, and analysis of a MOSFET-based circuit which emulates the activity of a neuron by generating spikes at the output terminal as a result of constant current input. The circuit is based on the diagram provided in Chapter the book "Analog VLSI and Neural Systems" by Carver Mead, 1989.

## Project Structure

- **/design**: Contains the image(Neuron_Circuit.png) as well as the design files(schematic folder) of the schematic developed using Cadence Virtuoso.
- **/simulation**: Contains circuit diagram as well as the image of the transient response of the circuit. (see Zoomed_In_Tran_Res.png)

##Circuit Description
Given here is a circuit which emulates a neuron that has a prolonged depolarized state, as biologists say. The neuron goes to a HIGH voltage state and just remains there. 
For reuse of this circuit, a mechanism to turn the output low needs to be devised.
One way to turn off a neuron is to leak some charge away to ground when the output is high; that is the purpose of transistors NMl and NM2 in the circuit. NMl is a current-control transistor. The pulse duration is controllable and NMl is used as a pulse-duration control. Once the output is on, transistor NM2 is on, and the capacitor connected to the node Vout starts discharging through NMl and NM2. If the voltage bias on NM1 is increased, then the charge leaks away from CI faster, and the circuit will turn itself off sooner. Once Vout 
reaches Vh, the positive-feedback sequence is initiated once again. A small decrease in Vout results in a large decrease in Vout , which results in an even further decrease in Vout. The output is slammed to ground, and the nerve pulse is terminated.

## Tools and Technologies

- **EDA Tool**: Cadence Virtuoso
- **Process Technology**: GPDK90

## Getting Started

1. **Clone the Repository**: Clone the project repository to your local machine using the command:
   ```bash
   git clone https://github.com/code-n-conquer/Neuron-Simulation-Project.git
