# URSC Project Notes

<details>
  <summary>January</summary>

<br>

<details>
  <summary>Day 1 - 23/01</summary>
  
### Work Assigned -> SOC vs FPGA

# SoC (System on Chip):

![500px-ARMSoCBlockDiagram svg](https://github.com/ISRO-Project/Ramdev/assets/43489027/12a9f5fa-5b8d-4bfe-9446-df12eaedcb2b)

-> A System on a Chip (SoC) is an integrated circuit that integrates most or all components of a computer or other electronic system1. It usually includes a CPU (via a microprocessor or microcontroller), memory, input/output (I/O) ports, and secondary storage on a single substrate, such as silicon.

-> Higher-performance SoCs are often paired with dedicated and physically separate memory and secondary storage (such as LPDDR and eUFS or eMMC, respectively) chips, that may be layered on top of the SoC in what's known as a package on package (PoP) configuration, or be placed close to the SoC. Additionally, SoCs may use separate wireless modems.

-> Characteristics:
  - High level of integration
  - Low power consumption
  - Fixed architecture
  - Limited flexibility

references: [System on a chip](https://en.wikipedia.org/wiki/System_on_a_chip), [Architecture of SoC](https://www.geeksforgeeks.org/architecture-of-soc/), [System on a Chip: How Smaller, Faster Devices are Made](https://www.ansys.com/en-in/blog/what-is-system-on-a-chip)

# FPGA (Field Programmable Gate Array):

##### Zynq UltraScale+ MPSoC ZCU104 Evaluation Kit
![1682465137359](https://github.com/ISRO-Project/Ramdev/assets/43489027/a23a5428-9fd0-4f91-b4a3-9264f2094e40)

-> Field Programmable Gate Arrays (FPGAs) are integrated circuits often sold off-the-shelf. They’re referred to as ‘field programmable’ because they provide customers the ability to reconfigure the hardware to meet specific use case requirements after the manufacturing process. This allows for feature upgrades and bug fixes to be performed in situ, which is especially useful for remote deployments.

-> FPGAs contain configurable logic blocks (CLBs) and a set of programmable interconnects that allow the designer to connect blocks and configure them to perform everything from simple logic gates to complex functions. Full SoC designs containing multiple processes can be put onto a single FPGA device

##### A Simplified CLB
![2210](https://github.com/ISRO-Project/Ramdev/assets/43489027/76948c8b-aebc-4b71-8761-c27149b1ab6c)

-> Characteristics:
  - Reconfigurability
  - Well suited for Parallel Processing
  - Custom Hardware Acceleration
  - High power consumption

references: [ARM - What Is an FPGA?, Why Do Developers Select FPGA?](https://www.arm.com/glossary/fpga#:~:text=Field%20Programmable%20Gate%20Arrays%20(FPGAs,requirements%20after%20the%20manufacturing%20process.)), [AMD - Field Programmable Gate Array (FPGA)](https://www.xilinx.com/products/silicon-devices/fpga/what-is-an-fpga.html), [What's an FPGA?](https://www.youtube.com/watch?v=iHg0mmIg0UU&pp=ygUEZnBnYQ%3D%3D)
