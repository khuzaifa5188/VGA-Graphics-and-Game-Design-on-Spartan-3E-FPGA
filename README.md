# VGA Graphics & Game Design on Spartan-3E FPGA

A hardware-accelerated game implemented entirely in **Verilog HDL**. This project demonstrates real-time VGA signal generation, sprite rendering, and game logic processing directly on the Xilinx Spartan-3E FPGA.

## 🎮 Project Overview
Unlike software-based games, this project uses dedicated digital logic to drive a VGA display. It bypasses any CPU/OS to achieve zero-latency graphics rendering by calculating pixel data on-the-fly at a 25MHz pixel clock.

## 🛠️ Hardware Specifications
* **FPGA:** Xilinx Spartan-3E (XC3S500E)
* **Language:** Verilog HDL
* **Display Output:** 640x480 @ 60Hz VGA
* **Clock:** 50MHz onboard oscillator (divided to 25MHz for VGA timing)
* **Input:** Onboard push buttons/switches for player movement.



## 🚀 Key Modules
1. **VGA Controller:** Generates the precise timing for Horizontal and Vertical synchronization.
2. **Graphics Engine:** Handles object positioning, color generation, and "scanning" to determine which pixel to draw in real-time.
3. **Collision Detection:** Purely combinational and sequential logic that detects overlap between coordinate registers.
4. **Game Logic (FSM):** A Finite State Machine that manages game states (Start, Play, Game Over, Reset).

## 📊 Technical Features
* **Zero Latency:** High-speed hardware execution ensures no lag between input and display.
* **Bitmap/Tile Memory:** Efficient use of Block RAM (BRAM) for storing custom graphics and characters.
* **RGB Color Control:** 3-bit/8-bit color depth implementation based on Spartan-3E DAC constraints.



## 📁 Repository Structure
* `/hdl`: Source Verilog files (.v)
* `/constraints`: User Constraint Files (.ucf) for pin mapping.
* `/assets`: Memory initialization files (.coe) for textures/sprites.
* `/docs`: Project report and architecture diagrams.

## 🔧 How to Deploy
1. Open **Xilinx ISE Design Suite**.
2. Create a new project for the Spartan-3E (XC3S500E).
3. Import the `.v` files and the `.ucf` file.
4. Synthesize the design and generate the Bitstream (`.bit`).
5. Program the FPGA using **iMPACT** or Digilent Adept.

## 👨‍💻 Author
**Muhammad Khuzaifa**
