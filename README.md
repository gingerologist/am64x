# AM64x Dev Board

This project starts from proc101d (TMDS64EVM).

There are two official dev boards for AM64x. 

TMDS64EVM (codenamed proc101 and d is the latest version) has discrete power supplies, 
DDR4 memory, 3 gigabit ethernet, pcie support, high speed signal interface 
and advance debugging support.

AM64x Starter Kit has TPS65220 pmic, LPDDR4 memory, 2 gigabit ethernet sockets, USB3 support.

This is not an unopinionated design, though many features are going to be preserved in main branch. The project is mostly targeted battery powered, wireless and headless devices, which means, ethernets, display or camera supports are generally not required. But this is not for sure. Possibly some clients require those features.


