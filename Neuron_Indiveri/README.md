# Leaky Integrate-and-fire Neuron Design and Simulation Project

## Overview

The **Leaky Integrate-and-fire Neuron Design and Simulation Project** focuses on the design, simulation, and analysis of a MOSFET-based circuit which emulates the activity of a neuron by generating spikes at the output terminal as a result of input current pulses. The circuit is based on the diagram provided in the research paper "A VLSI array of low-power spiking neurons and bistable synapses with spike-timing dependent plasticity" by Indiveri et al, 2006.

## Project Structure

- **/design**: Contains the image(Neuron_Indiveri.png) as well as the design files(schematic folder) of the schematic developed using Cadence Virtuoso.
- **/simulation**: Contains circuit diagram as well as the image of the transient response of the circuit. (see Transient_Response_Neuron_indiveri.png)

## Circuit Description

The input current Iinj is integrated by the integrating capacitor to produce a voltage Vmem at one terminal of the capacitor. When Vmem increses enough
to make the first inverter switch, the voltage Vspk is driven to Vdd. During the spike emission period(while Vspk is high), a current with amplitude
set by Vadap is sourced into the gate-to-source parasitic capacitance on node Vca. Thus, the voltage Vca increases with every spike, but when there is 
no spiking activity. Vca slowly leaks to zero through leakage currents. The voltage Vca sets the current Iadap which is exponentially proportional 
to Vca. Increase in Iadap slows down the charging process of the capacitor Cmem and the spiking frequency of the neuron decreases. Thus, spike-timing
dependent plasticity is implemented.

## Tools and Technologies

- **EDA Tool**: Cadence Virtuoso
- **Process Technology**: GPDK90

## Getting Started

1. **Clone the Repository**: Clone the project repository to your local machine using the command:
   ```bash
   git clone https://github.com/code-n-conquer/Neuron_Simulation.git
