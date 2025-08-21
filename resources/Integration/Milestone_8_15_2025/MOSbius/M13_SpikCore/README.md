Place the GDS file with the following name in this folder: M13_SpikCore.gds

### The proposed pin list and pin descriptions can be found [here](https://docs.google.com/spreadsheets/d/1vhMIvf8tOUEVN5lxGAr1D5x2heG8VZecuYUK63GFHpc/edit?usp=sharing)

### The GDS file has been updated to reflect the use of the Bootstrapped TG for one row of the SW matrix.

### The padframe proposal pinout can be found [here](2025%20Chipathon%20Padframe%20Template.pdf)

The limitation of 22 IOs for the design restricts the use of components. Integration with other teams' OnChip designs could require a higher number of IOs.



| Pin number | Name    | Type    | Description                                      |
|------------|---------|---------|--------------------------------------------------|
| 34         | CLK_TG  | Digital | Clock signal for a TG                            |
| 35         | VDD_AH  | analog  | Power supply for AH neuron                       |
| 36         | I_IN0   | analog  | Input from AH neuron 0                           |
| 37         | VOUT_0  | analog  | Output from AH neuron 0                          |
| 38         | I_IN1   | analog  | Input from AH neuron 1                           |
| 39         | VOUT_1  | analog  | Output from AH neuron 1                          |
| 40         | I_IN2   | analog  | Input from AH neuron 2                           |
| 41         | VOUT_2  | analog  | Output from AH neuron 2                          |
| 42         | I_IN3   | analog  | Input from AH neuron 3                           |
| 43         | VOUT_3  | analog  | Output from AH neuron 3                          |
| 44         | VDD3V3  | analog  | 3.3V power supply                                |
| 45         | VSS     | analog  | Ground                                           |
| 46         | VIN_LIF   | analog  | Input from commuted LIF neuron                   |
| 47         | VOUT_LIF  | analog  | Output from commuted LIF neuron                  |
| 48         | V_EX    | analog  | Excitatory control pin for synapses              |
| 49         | V_INH   | analog  | Inhibitory control pin for synapses              |
| 50         | VIN_S0   | analog  | Input voltage for synapse 0                      |
| 51         | VOUT_S0  | analog  | Output voltage for synapse 0                     |
| 52         | VIN_S1   | analog  | Input voltage for synapse 1                      |
| 53         | VOUT_S1  | analog  | Output voltage for synapse 1                     |
| 54         | VIN_S2   | analog  | Input voltage for synapse 2                      |
| 55         | VOUT_S2  | analog  | Output voltage for synapse 2                     |
| 56         |          |         |