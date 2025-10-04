# VSD-RISC-V-SoC-Tapeout-Program-Week-2
###  BabySoC Fundamentals & Functional Modelling

## 📌 Objective

The goal of Week 2 is to build a strong foundation in **System-on-Chip (SoC) fundamentals** and gain hands-on experience with **functional modelling** using **Icarus Verilog (iverilog)** and **GTKWave**.

By the end of this week, you should be able to:

* Explain the basics of SoC design and its components.
* Understand why BabySoC is used as a simplified model for learning.
* Perform functional modelling of BabySoC using simulation tools.
* Analyze and document simulation results (waveforms & logs).

---

## 📝 Part 1 – Theory (Conceptual Understanding)

Reference: [Fundamentals of SoC Design](https://github.com/hemanthkumardm/SFAL-VSD-SoC-Journey/tree/main/11.%20Fundamentals%20of%20SoC%20Design)

### 🔹 What is a System-on-Chip (SoC)?

A **System-on-Chip (SoC)** integrates all the essential components of a computer or electronic system into a single chip. It typically includes:

* **CPU/Core** – for computation and instruction execution
* **Memory** – SRAM, DRAM, cache storage
* **Peripherals** – timers, UART, GPIOs, communication interfaces
* **Interconnect/Bus** – data pathways connecting components

### 🔹 Why BabySoC?

BabySoC is a simplified model that:

* Introduces SoC concepts without overwhelming complexity
* Allows learners to practice simulation, debugging, and waveform analysis
* Serves as a stepping stone before RTL design and physical design

### 🔹 Role of Functional Modelling

* Functional modelling verifies **logical correctness** of the design before implementation.
* Helps visualize dataflow, reset behavior, and clocking.
* Provides confidence before moving to RTL and physical stages.

📄 **Deliverable (Theory):**
A concise write-up (1–2 pages) summarizing SoC fundamentals and BabySoC’s role in learning SoC design.

---

## ⚙️ Part 2 – Hands-on Functional Modelling

Reference: [VSDBabySoC Project Labs](https://github.com/hemanthkumardm/SFAL-VSD-SoC-Journey/tree/main/12.%20VSDBabySoC%20Project)

### 🔹 Tools Required

* **[Icarus Verilog (iverilog)](http://iverilog.icarus.com/)** → For compiling Verilog code
* **[GTKWave](http://gtkwave.sourceforge.net/)** → For viewing simulation waveforms

### 🔹 Steps Performed

1. Clone the BabySoC project repo:

   ```bash
   git clone https://github.com/hemanthkumardm/SFAL-VSD-SoC-Journey.git
   cd SFAL-VSD-SoC-Journey/12.\ VSDBabySoC\ Project
   ```

2. Compile the BabySoC Verilog modules:

   ```bash
   iverilog -o babySoc_sim BabySoC_tb.v BabySoC.v
   ```

3. Run the simulation and generate `.vcd` file:

   ```bash
   vvp babySoc_sim
   ```

4. Open the `.vcd` file in GTKWave:

   ```bash
   gtkwave dump.vcd
   ```
<img width="1375" height="266" alt="image" src="https://github.com/user-attachments/assets/a8446de4-7ca8-4eda-8ed3-cfd62c8b9364" />


5. Analyze the following:

   * ✅ **Reset Operation** – verify initialization behavior
   * ✅ **Clocking** – check clock waveform and synchronization
   * ✅ **Dataflow** – trace signal interactions between modules

### 🔹 Deliverables

* **Simulation logs** (`.out` / `.log`)
* **GTKWave screenshots** showing correct BabySoC behavior
* **Short explanations** for each screenshot (e.g., reset sequence, clock signals, data transfer)

---

## ✅ Outcomes of Week 2

* Gained **conceptual clarity** on SoC fundamentals.
* Understood the purpose of **BabySoC** as a simplified model.
* Successfully performed **functional modelling** using Verilog simulation.
* Documented and explained waveform behavior for reset, clock, and dataflow.

---

🔗 **References**

* [Fundamentals of SoC Design Notes](https://github.com/hemanthkumardm/SFAL-VSD-SoC-Journey/tree/main/11.%20Fundamentals%20of%20SoC%20Design)
* [VSDBabySoC Project Labs](https://github.com/hemanthkumardm/SFAL-VSD-SoC-Journey/tree/main/12.%20VSDBabySoC%20Project)

---
