Place the GDS file with the following nomenclature in this folder: M2_ChipOdyssey.gds

Also, update the README.md file to include the pin list and pin description.

[Pin List and Description]
Number of Pins:
Power
4 (Analog VDD, VSS, Digital VDD, VSS)
TIA
3 (V+, V-, Out)
Comparator
12 (V+, V-, Clk, Out, 8 offset correction) (will try to reduce offset correction pins with calibration circuit)
SAR Logic
9 (In, 6 digital out, 1 ready pin for clock cycles, 1 ready pin for full conversion cycle)
CDAC
3 (Vref, ADC reset, DAC out)
Switch Matrix
3 (1 between TIA and CDAC, 1 between CDAC and Comparator, 1 between Comparator and SAR Logic)
Total: 34 pins
Area Estimate: 600um x 400um
Used this paper as minimum estimate and added our approximate TIA and other component area: https://drive.google.com/file/d/191QjsD6ZHyCCeeVFDZAnm8slRRV7lbvb/view?usp=sharing 
Also added ADC gds file to submission

Link to Pin Padframe: https://docs.google.com/presentation/d/1M6atEBdrpoQDF44i9qx-kfYodAoFVWYvb3GMPAhebwY/edit?usp=sharing 
