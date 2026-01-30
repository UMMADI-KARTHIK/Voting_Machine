
🗳️ Digital Voting Machine – Verilog HDL Project
📌 Project Overview

This project implements a Digital Voting Machine (DVM) using Verilog HDL.
The system allows users to cast votes for multiple candidates and securely stores and displays the vote count.
The design focuses on vote validation, prevention of duplicate voting, and modular RTL design.

🎯 Objective

To design a reliable electronic voting system.

To prevent multiple or accidental votes.

To display vote counts digitally using LEDs or output ports.

To understand Verilog RTL design, counters, and control logic.

🧩 Features

Two operating modes:

Voting Mode (Mode 0) – Cast votes.

Display Mode (Mode 1) – Show vote counts.

Button debouncing / validation logic.

Separate vote counters for each candidate.

Priority handling when multiple buttons are pressed.

LED-based vote confirmation and result display.

Fully simulated using a Verilog testbench.

🏗️ System Architecture

The design is divided into four modules:

1. Button Control Module

Validates button press duration.

Generates a single-clock valid vote pulse.

Prevents multiple votes from one long press.

2. Vote Logger Module

Maintains individual counters for each candidate.

Counts votes only in Voting Mode.

Resets on system reset.

3. Mode Control Module

Controls LED output behavior.

Voting Mode → All LEDs glow briefly as confirmation.

Display Mode → LEDs show vote count in binary format.

4. Top Voting Machine Module

Integrates all modules.

Connects button inputs, counters, and LED outputs.

⚙️ Technologies Used

Language: Verilog HDL

Simulation Tools: EDA Playground / ModelSim / Xilinx Vivado

Concepts: Counters, FSM logic, debouncing, modular RTL design

🧪 Testbench & Verification

The testbench simulates:

Clock and reset signals

Short vs long button presses

Mode switching

Multiple candidate button inputs

Expected Behavior

Short press → No vote counted

Long press → Vote incremented

Display mode → Correct vote count shown

Multiple buttons → Priority-based counting

▶️ How to Run

Open the project in EDA Playground / Vivado / ModelSim.

Compile all Verilog modules.

Run the testbench file.

Observe waveform outputs and LED signals.

📊 Output Representation

Voting Mode: All LEDs ON briefly → vote confirmation.

Display Mode: LEDs show vote count in binary.

Reset: Clears all counters.

📚 Learning Outcomes

Verilog RTL coding practices

Counter and control logic design

Debouncing and vote validation

Modular digital system design

Simulation and waveform analysis

🔮 Future Improvements

Add LCD / 7-segment display support.

Include password or biometric validation.

Expand candidate count dynamically.

Implement FPGA hardware deployment.

👤 Author

Karthik Ummadi
B.Tech – Electronics & Communication Engineering

📄 License

This project is for academic and learning purposes.
