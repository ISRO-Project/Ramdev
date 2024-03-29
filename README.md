# URSC Project Notes

# January

<br>

<details>
  <summary>Week 1 - 23/01</summary>
  
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
  <summary> 24/01 </summary>

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
  <summary> 25/01 </summary>

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
  <summary>Week 2</summary>

#### 1 & 2/02

### Tasks Assigned - Connect PS & PL with GPIO, Use LEDS and DIP Switches to show PS & PL are connected, Create a waveform(counter) and probe it on an oscilloscope

-> First caught up with the "Hello World" program developed by Sanee and Shashank. Worked with Vivado and Vitis to understand the toolflow.

-> Encountered "sstate-cache" error while trying to install pentalinux offline.

-> The necessary files are downloaded but are required to be transfered to our system.

-> Implemented a "NAND" gate by linking an "AND" gate on the Programming Logic(PL) and a "NOT" gate on the Processing 
System(PS).

-> Used Switches as input and an LED was used to display the output.

resources, ref: [ZCU102 Evaluation
Board - User Guide](https://www.xilinx.com/support/documents/boards_and_kits/zcu102/ug1182-zcu102-eval-bd.pdf), [PetaLinux offline build without internet access](https://support.xilinx.com/s/article/Petalinux-offline-build-flow?language=en_US), [ZYNQ for beginners: programming and connecting the PS and PL](https://www.youtube.com/watch?v=_odNhKOZjEo&list=PLtC_AnOn1Cx9LUfca0HdIBXK9lNFQfEte), [xdc file for ZCU 102](https://account.amd.com/en/forms/downloads/design-license.html?cid=473474&filename=zcu102-xdc-rdf0405.zip)

</details>

<br>

<details>
  <summary> Week 3 </summary>

#### 5 to 9/02
  
# Keyboard input throught UART

##### Block Diagram
![302697579-5602405d-e566-434e-95bb-04feea77fc23](https://github.com/ISRO-Project/Ramdev/assets/43489027/7324e49e-7438-4fae-8944-409e8ec62557)


##### GPIO Block Configuration
![302697547-3995e500-8fab-430d-9a3b-720e2bd8f48b](https://github.com/ISRO-Project/Ramdev/assets/43489027/2ba0aa2f-d41c-48ff-858f-5c6d6e58fd3b)

-> Create HDL Wrapper, Generate Bitstream and Export.

-> Lauch Vitis and create a new platform project with the newly made XSA file.

-> Create a new application project.

-> Edit the helloworld.c file to include the below code:


```bash
#include <stdio.h>
#include "xparameters.h"
#include "xgpio.h"
#include "xuartps.h"

#define LED_GPIO_DEVICE_ID XPAR_AXI_GPIO_0_DEVICE_ID
#define UART_DEVICE_ID XPAR_PSU_UART_1_DEVICE_ID

int main() {
    XGpio Gpio;  // GPIO instance for controlling LEDs
    XUartPs Uart; // UART instance for communication
    u8 readBuffer[10]; // Buffer to store received UART data

    // Initialize GPIO for LEDs
    XGpio_Initialize(&Gpio, LED_GPIO_DEVICE_ID);
    XGpio_SetDataDirection(&Gpio, 1, 0x0); // Set LED GPIO as output

    // Initialize UART
    XUartPs_Config *UartCfgPtr = XUartPs_LookupConfig(UART_DEVICE_ID);
    XUartPs_CfgInitialize(&Uart, UartCfgPtr, UartCfgPtr->BaseAddress);

    while (1) {
        // Receive one byte from UART
        XUartPs_Recv(&Uart, readBuffer, 1);

        // Check if the received character is a digit between '0' and '7'
        if (readBuffer[0] >= '0' && readBuffer[0] <= '7') {
            int ledIndex = readBuffer[0] - '0';
            // Turn on the corresponding LED using the GPIO
            XGpio_DiscreteWrite(&Gpio, 1, 1 << ledIndex);
        }
    }

    return 0;
}

```  
-> Build Project and run on Hardware.

-> Input given through CuteCom lights up the corresponding LED.

</details>

<br>

<details>
  <summary> Week 4 </summary>

# Tuesday, 20/2 
- Petalinux Image installation on the board.
- Switched the board to SD card boot mode
- Tried to get webcam input through the ZCU 102 board.

# Wednesday, 21/2
- Successfully got camera input
- Started working on running the Cloud/No Cloud classifier using the board.

# Thursday, 22/2
- Completed the classifier implementation using the MX_Full model.
- Started to work on running it using Resnet 50 and Resnet 101.

# Friday, 23/2
- Both Resnet implementations completed but on seeing results decided that they are not suitable for our classifier.
- Yolo implementation for object detection started.

</details>

<br>

<details>
  <summary> Week 5 </summary>

# Monday, 26/2
- Yolov3 running on CPU for single frame captured through webcam.

# Tuesday, 27/2
- Tried to run using DPU but not successful. Several issues while using Darknet for DPU (Referred to https://pjreddie.com/darknet/yolo/).

# Wednesday, 28/2
- Successfully ran multiple frame capture and Yolov3 detection on CPU.
- 2 min per frame to detect and display output.


 



