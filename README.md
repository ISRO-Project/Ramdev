# URSC Project Notes

# January

<br>

<details>
  <summary>Day 1 - 23/01</summary>
  
### Task Assigned - SOC vs FPGA

# SoC (System on Chip):

![500px-ARMSoCBlockDiagram svg](https://github.com/ISRO-Project/Ramdev/assets/43489027/12a9f5fa-5b8d-4bfe-9446-df12eaedcb2b)

-> A System on a Chip (SoC) is an integrated circuit that integrates most or all components of a computer or other electronic system1. It usually includes a CPU (via a microprocessor or microcontroller), memory, input/output (I/O) ports, and secondary storage on a single substrate, such as silicon.

-> Higher-performance SoCs are often paired with dedicated and physically separate memory and secondary storage (such as LPDDR and eUFS or eMMC, respectively) chips, that may be layered on top of the SoC in what's known as a package on package (PoP) configuration, or be placed close to the SoC. Additionally, SoCs may use separate wireless modems.

-> Characteristics:
  - High level of integration
  - Low power consumption
  - Fixed architecture
  - Limited flexibility

ref: [System on a chip](https://en.wikipedia.org/wiki/System_on_a_chip), [Architecture of SoC](https://www.geeksforgeeks.org/architecture-of-soc/), [System on a Chip: How Smaller, Faster Devices are Made](https://www.ansys.com/en-in/blog/what-is-system-on-a-chip)

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

ref: [ARM - What Is an FPGA?, Why Do Developers Select FPGA?](https://www.arm.com/glossary/fpga#:~:text=Field%20Programmable%20Gate%20Arrays%20(FPGAs,requirements%20after%20the%20manufacturing%20process.)), [AMD - Field Programmable Gate Array (FPGA)](https://www.xilinx.com/products/silicon-devices/fpga/what-is-an-fpga.html), [What's an FPGA?](https://www.youtube.com/watch?v=iHg0mmIg0UU&pp=ygUEZnBnYQ%3D%3D)

## SoC vs FPGA:
  - Flexibility: FPGAs provide more flexibility as they can be reprogrammed to desired application or functionality requirements after manufacturing. SoCs, on the other hand, are less flexible once designed.
  - Cost: FPGAs are generally more costly.
  - Power Consumption: FPGAs tend to consume more power.
  - Use cases:
    - FPGA - Flexibility and Customization, Complex designs, Prototyping
    - SoC - Integration and ease of use, Mobile Devices
</details>

<br>

<details>
  <summary>Day 2 - 24/01</summary>

### Task Assigned - ZCU 102, KCU 105

# Zynq UltraScale+ MPSoC ZCU102 Evaluation Kit

![1682465100889](https://github.com/ISRO-Project/Ramdev/assets/43489027/43092a3f-ee2e-435b-956f-117ebd792d1a)

-> ZCU 102 is a development board produced by Xilinx, a subsidiary of AMD, designed for prototyping and evaluating systems based on Xilinx Zynq UltraScale+ MPSoC. MPSoC stands for Multi-Processor System on Chip, which integrates a quad-core Arm Cortex-A53, dual-core Cortex-R5F, and a Mali-400 MP2 GPU, along with programmable logic fabric. ZCU 102 supports various peripherals and interfaces, such as PCIe, USB3, DisplayPort, SATA, Ethernet, and HDMI, as well as two FMC connectors for I/O expansion. ZCU 102 is suitable for applications in automotive, industrial, video, and communications domains.

#  AMD Kintex UltraScale FPGA KCU105 Evaluation Kit

![1684436489475](https://github.com/ISRO-Project/Ramdev/assets/43489027/9272f141-864f-4065-ac96-6c1829ce3b11)

-> KCU 105 is a development board that uses a Kintex UltraScale FPGA, a type of programmable logic device that can implement various digital circuits. The board has many features and interfaces that allow you to prototype and test different applications, such as video processing, cryptography, and neural networks.

-> Comparison

| Device                    | Zynq UltraScale+ MPSoC XCZU9EG               | Kintex UltraScale FPGA XCKU040               |
|---------------------------|----------------------------------------------|----------------------------------------------|
| Processor                 | Quad-core Arm Cortex-A53, dual-core Cortex-R5F, Mali-400 MP2 GPU | None                                         |
| System Logic Cells (K)    | 600                                          | 530                                          |
| Memory (Mb)               | 32.1                                         | 21.1                                         |
| DSP Slices                | 2,520                                        | 1,920                                        |
| Maximum I/O Pins          | 328                                          | 520                                          |
| Interfaces                | PCIe, USB3, DisplayPort, SATA, Ethernet, HDMI, FMC | PCIe, USB3, DisplayPort, Ethernet, FMC        |
| Clocks                    | 4 Si570 programmable oscillators, 2 Si5324 jitter attenuators | 4 Si570 programmable oscillators, 1 Si5324 jitter attenuator |
| Power                     | 12 V AC/DC adapter                           | 12 V AC/DC adapter                           |

ref: [Zynq UltraScale+ MPSoC ZCU102 Evaluation Kit](https://www.xilinx.com/products/boards-and-kits/ek-u1-zcu102-g.html), [AMD Kintex UltraScale FPGA KCU105 Evaluation Kit
](https://www.xilinx.com/products/boards-and-kits/kcu105.html)
</details>

<br>

<details>
  <summary>Day 3 - 25/01</summary>

### Task assigned - Systolic Array Architecture, 3x3 Dot Product implementation, Analyse working of 100x100

# Systolic Array Architecture

##### Systolic Array Architecture for CNN
![Systolic-Array-Architecture-for-CNN](https://github.com/ISRO-Project/Ramdev/assets/43489027/425a98a6-ecd4-40fd-9838-8dbcdc8cd42b)

-> A systolic array architecture is a type of parallel computing that uses a network of simple processing units called cells or nodes. Each node computes a partial result based on the data received from its neighbours and passes it along to the next node. The data flows through the network in a rhythmic way, like the pulse of the heart

-> A systolic array is composed of a grid of cells, each of which performs a simple operation on the data it receives from its neighbours. The data flows through the array in a regular pattern, like a wave or a pulse. The output of each cell is passed to the next cell in the direction of the data flow. The final result is obtained at the edge of the array after a certain number of cycles.

-> Systolic arrays are often used for applications that require high performance and efficiency, such as matrix multiplication, image processing, neural networks, and cryptography.

-> Characteristics:
  - Makes multiple uses of each data item, reduced need for
fetching/refetching
  - High concurrency
  - Scalability
  - Energy Efficiency

ref: [Parallel processing – systolic arrays](https://www.geeksforgeeks.org/parallel-processing-systolic-arrays/), [Systolic Arrays](https://www.sciencedirect.com/topics/computer-science/systolic-arrays), [Computer Architecture:
VLIW, DAE, Systolic Arrays ](https://course.ece.cmu.edu/~ece740/f13/lib/exe/fetch.php?media=onur-740-fall13-module5.3-vliw-dae-systolic.pdf)

### 3x3 Dot Product Implementation using Systolic Arrays and analysis of 100x100
-> Understood the concept using [A Beginner's Guide to Systolic Arrays: 3x3 multiplication using systolic arrays](https://www.youtube.com/watch?app=desktop&v=vADVh1ogNo0).

![maxresdefault](https://github.com/ISRO-Project/Ramdev/assets/43489027/18922b4d-f554-4d25-b8a8-66c54784b421)

-> 100x100 multiplication will follow the same procedure with the final output coming in the 10,000th cycle.

</details>

<br>

# February

<br>

<details>
  <summary>Day 4, 5 - 1 & 2/02</summary>

### Tasks Assigned - Connect PS & PL with GPIO, Use LEDS and DIP Switches to show PS & PL are connected, Create a waveform(counter) and probe it on an oscilloscope

-> First caught up with the "Hello World" program developed by Sanee and Shashank. Worked with Vivado and Vitis to understand the toolflow.
-> Encountered "sstate-cache" error due to offline installation of pentalinux.
-> The necessary files are downloaded but are required to be transfered to our system.
-> Implemented a "NAND" gate by linking an "AND" gate on the Programming Logic(PL) and a "NOT" gate on the Processing System(PS).
-> Used Switches as input and an LED was used to display the output.

resources, ref: [ZCU102 Evaluation
Board - User Guide](https://www.xilinx.com/support/documents/boards_and_kits/zcu102/ug1182-zcu102-eval-bd.pdf), [PetaLinux offline build without internet access](https://support.xilinx.com/s/article/Petalinux-offline-build-flow?language=en_US), [ZYNQ for beginners: programming and connecting the PS and PL](https://www.youtube.com/watch?v=_odNhKOZjEo&list=PLtC_AnOn1Cx9LUfca0HdIBXK9lNFQfEte), [xdc file for ZCU 102](https://account.amd.com/en/forms/downloads/design-license.html?cid=473474&filename=zcu102-xdc-rdf0405.zip)

### Pending - keyboard input using UART, waveform 
