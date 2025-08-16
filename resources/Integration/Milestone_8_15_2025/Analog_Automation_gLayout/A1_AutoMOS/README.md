## Instructions

Place the GDS file with the following nomenclature in this folder: A1_AutoMOS.gds

Also, update the README.md file to include the pin list and pin description.


### GDS file

This is very preliminary version. Just two of the 5 blocks we have in
schematic.


### Pin list

Link to the pin list:
https://docs.google.com/spreadsheets/d/1fHQSTDq1Uh_aIy8z8KXEGHcneteHOJtz9p10SLcYZMg/edit?usp=sharing

| Pin name        | Type    | Direction | Description                                | Power Domain | ESD/IO                   | Purpose    |
| --------------- | ------- | --------- | ------------------------------------------ | ------------ | ------------------------ | ---------- |
| VDD             | Power   | Inout     | 5V power supply                            | 5V           | gf180mcu_fd_io__dvdd     | Functional |
| VTEST           | Power   | Inout     | 5V power supply for test structures        | 5V           | gf180mcu_fd_io__dvdd     | Test       |
| VSS             | Power   | Inout     | Ground                                     | 5V           | gf180mcu_fd_io__dvss     | Functional |
| SUB             | Power   | Inout     | Substrate                                  | 5V           | gf180mcu_fd_io__dvss     | Functional |
| BIAS_EN         | Digital | Input     | Enable for internal bias generator         | 5V           | gf180mcu_fd_io__in_c     | Functional |
| LDO_OUT         | Power   | Inout     | 1.8V LDO output voltage                    | 1.8V         | gf180mcu_fd_io__dvdd     | Functional |
| LDO_EN          | Digital | Input     | Enable for LDO                             | 5V           | gf180mcu_fd_io__in_c     | Functional |
| VCO_IN          | Analog  | Inout     | VCO control input voltage                  | 1.8V         | gf180mcu_fd_io__asig_5p0 | Functional |
| VCO_EN          | Digital | Inout     | Control input voltage                      | 1.8V         | gf180mcu_fd_io__in_c     | Functional |
| VCO_OUT         | Digital | Inout     | Output voltage                             | 1.8V         | gf180mcu_fd_io__bi_t     | Functional |
| TEST_EN         | Digital | Input     | Enable for test module                     | 5V           | gf180mcu_fd_io__in_c     | Test       |
| TEST_SEL_0      | Digital | Input     | Test input selector, bit 0                 | 5V           | gf180mcu_fd_io__in_c     | Test       |
| TEST_SEL_1      | Digital | Input     | Test input selector, bit 1                 | 5V           | gf180mcu_fd_io__in_c     | Test       |
| TEST_SEL_2      | Digital | Input     | Test input selector, bit 2                 | 5V           | gf180mcu_fd_io__in_c     | Test       |
| TEST_OUT        | Analog  | Inout     | Test output for internal signal monitoring | 5V           | gf180mcu_fd_io__asig_5p0 | Test       |
| LDO_VREF_OVRD   | Digital | Input     | LDO reference override                     | 5V           | gf180mcu_fd_io__in_c     | Debug      |
| LDO_VREF        | Analog  | Inout     | External 0.9V reference                    | 5V           | gf180mcu_fd_io__asig_5p0 | Debug      |
| LDO_IBIAS_OVRD  | Digital | Input     | LDO bias override                          | 5V           | gf180mcu_fd_io__in_c     | Debug      |
| LDO_IBIAS       | Analog  | Inout     | External 10uA current bias (source)        | 5V           | gf180mcu_fd_io__asig_5p0 | Debug      |
| VCO_IBIAS_OVRD  | Digital | Input     | VCO bias override                          | 1.8V         | gf180mcu_fd_io__in_c     | Debug      |
| VCO_IBIAS       | Analog  | Inout     | External 10uA current bias (sink)          | 1.8V         | gf180mcu_fd_io__asig_5p0 | Debug      |
| TEST_IBIAS_OVRD | Digital | Input     | VCO bias override                          | 1.8V         | gf180mcu_fd_io__in_c     | Debug      |
| TEST_IBIAS      | Analog  | Inout     | External 10uA current bias (sink)          | 1.8V         | gf180mcu_fd_io__asig_5p0 | Debug      |

### List of team members:

- Luighi Viton Zorrilla
- Julio Vilca Pizarro
- Rodrigo Marin
