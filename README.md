# AM64x Dev Board

This project starts from proc101d (TMDS64EVM).

There are two official dev boards for AM64x. 

TMDS64EVM (codenamed proc101 and d is the latest version) has discrete power supplies, 
DDR4 memory, 3 gigabit ethernet, pcie support, high speed signal interface 
and advance debugging support.

AM64x Starter Kit has TPS65220 pmic, LPDDR4 memory, 2 gigabit ethernet sockets, USB3 support.

This is not an unopinionated design, though many features are going to be preserved in main branch. The project is mostly targeted battery powered, wireless and headless devices, which means, ethernets, display or camera supports are generally not required. But this is not for sure. Possibly some clients require those features.



## TODO

- [ ] what does test automation test? and how



## Simplified Power

- All current monitors are removed.
- LM5140 removed. 
  - VCC_5V0 removed. 
  - VCC_3V3_SYS is provided by a TPS62826.
- VCC3V3_PREREG reserved. The regulator is changed to TPS62826.
- Soc_DVDD3V3 merged into VCC_3V3_SYS.
- SoC_DVDD1V8 merged into VCC1V8.
- Fixed 0.85V core voltage, which means R1/R3 installed and R2/R4 not populated. Further, R1/R3 are removed, VDD_CORE, VDDR_CORE, as well as VDDA_CORE are merged into VDD_CORE.





| Net Name       | -    | Zone/Plane            |
| -------------- | ---- | --------------------- |
| VCC3V3_PREREG  |      | PWR1 zone             |
| VCC_3V3_SYS    |      | PWR1 plane, PWR2 zone |
| VCC1V8         |      | PWR2 zone             |
| VDDA_1V8       |      | PWR2 zone             |
| - VDDA_1V8_MCU |      |                       |
| VDD_CORE       |      | PWR1 zone             |







