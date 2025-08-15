### Pin out and estimated size:

- Pinout: [here](https://docs.google.com/spreadsheets/d/1oHUfVFixzPntKKVUWIWM3LTt6kUj857WtGabhhOZUMs/edit?usp=sharing)

| Pin Number | Pin Name    | Type       | Direction    | Description                      |
|------------|-------------|------------|--------------|-----------------------------------|
| 1          | VSS         | Ground     | Bidirectional| Power - GND                       |
| 2          | VDD         | 3V3 Power  | Bidirectional| Power - GND                       |
| 3          | V_IN        | Analog     | Input        | Input Current                     |
| 4          | V_AUX       | Analog     | Input        | Bias Input - CCM                   |
| 5          | V_OUT_VCM   | Analog     | Output       | Output of nFET VCM                 |
| 6          | V_OUT_BCM   | Analog     | Output       | Output of nFET BCM                 |
| 7          | V_OUT_CCM   | Analog     | Output       | Output of nFET CCM                 |
| 8          | V_BIAS_IN   | Analog     | Input        | Bias Input - Current Sources       |
| 9          | EN<0>       | Digital    | Input        | Enable signal                      |



- Area : **(97.65 um x 40.05 um)** + 25%

- GLayout fork: https://github.com/Sud-ana/gLayout-mahowalders/tree/main/blocks/composite/regulated_cascoded_cmirror

### Brief description of your project
**Objective:** This project proposes the automated design and layout of a high-impedance, energy-efficient bias generation block using regulated current mirror architectures. Integrated into the gLayout toolchain (Python2GDS), this design aims to enhance layout portability, stability, and scalability across process corners.

**Design:**  
We compare three bias current mirror architectures: 

* Vanilla Current Mirror (VCM), as a reference  
* Self-Biased Common-Source CM (SB-CM), with improved impedance, moderate complexity  
* Regulated Cascode CM (RC-CM), with high output impedance, better stability, but requires auxiliary bias

All three versions will be parametrically instantiated via gLayout, enabling on-demand generation and automated layout. 

**Expected Contributions:** 

* gLayout-compatible IP blocks for advanced analog biasing  
* On-silicon testing of all three architectures, with a focus on RC-CM  
* Performance benchmarking and trade-off analysis (stability, impedance, layout area, and bias dependencies)

### List of team members
- Quentin Halbach
- Sudhansu Mishra
- Saptarshi Ghosh

### Links to our proposal slides

- Proposal Slides: [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?usp=sharing)
- Proposal in Google Docs: [here](https://docs.google.com/document/d/1FZdyJ7MXu66QQ6_0kkzPwPryskKX2VRuOPmt5tDAb5Y/edit?usp=sharing)
- Proposal in GitHub: [here](https://github.com/Sud-ana/gLayout-mahowalders/blob/main/blocks/composite/regulated_cascoded_cmirror/design_proposal/README.md)
- GDS submission Pull Request: https://github.com/sscs-ose/sscs-chipathon-2025/pull/116
- Pull Request: https://github.com/ReaLLMASIC/gLayout/pull/32

### Link to process tracker
Tracking sheet: [here](https://docs.google.com/spreadsheets/d/1k9veHdDh-e81fpdIpsUblsUgEMs8aU_Jj_eBLXmVOYY/edit?usp=sharing)

### Link to schematic/simulation review slides
- Top Level : schematic [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g374a1cc00bb_1_9#slide=id.g374a1cc00bb_1_9) and tb [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g374a1cc00bb_1_17#slide=id.g374a1cc00bb_1_17)

- Vanilla Current Mirror (VCM): [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g363dc07a788_0_6#slide=id.g363dc07a788_0_6) 
- Self-Biased Common-Source CM (SB-CM): [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g363dc07a788_0_51#slide=id.g363dc07a788_0_51)
- Regulated Cascode CM (RC-CM):  Schematic [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g363dc07a788_0_58#slide=id.g363dc07a788_0_58) and layout (WIP) [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g3645e9268a9_0_20#slide=id.g3645e9268a9_0_20)
- Simulation: [here](https://docs.google.com/presentation/d/1ZooMX9Att2mCr0K19jeGHpoaXq7p1V3HSQcLWzNX5dM/edit?slide=id.g363dc07a788_0_73#slide=id.g363dc07a788_0_73)



Thanks,

Team Mahowalders
