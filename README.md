## Task 1: NAND Gate Design in RTL Logic and Impact of Up-Pull Resistor

- First, using the **IC_Encounter** tool, design a **NAND gate** in RTL logic and verify its functionality.
- Then, apply necessary changes to examine the impact of an **Up-Pull resistor** on:
  - Output loading
  - Induced delay
  - Functional correctness
- Clearly explain the reason behind each observed effect.

## Task 2: XOR Gate Design Using Different Logic Styles

Design a 2-input **XOR (Exclusive-OR)** function using the following technologies:

- **Pseudo-NMOS**
- **DCVSL (Differential Cascode Voltage Switch Logic)**
- **Dual-Rail Domino Logic**

For each technology:

- Explain its operational theory.
- Demonstrate functional correctness using the **Encounter_IC** tool.

---

## 🧪 Task 1: RTL NAND Gate Design and Effect of Pull-Up Resistor

### 1. RTL NAND Gate Design with Encounter_IC

- The NAND gate was initially designed at the RTL level.
- Functional verification was performed using the `icfb` software environment.

### 2. Pull-Up Resistance Impact on Delay and Output Load

- The resistance was changed from **640Ω** to **10kΩ** and **20kΩ**.
- As shown in the waveform diagrams, increasing the pull-up resistor results in:
  - Higher delay in the circuit
  - Longer rise times
  - Decreased speed in reaching logic '1' at the output
  
### 3. Explanation of Delay

- Increasing resistance leads to a higher RC time constant.
- Consequently, rise time increases, and output transitions are delayed.

## ⚙️ Task 2: XOR Gate Design in Different Logic Families

The XOR gate was implemented and analyzed using the following logic styles:

### 1. Pseudo-NMOS (Static & Dynamic)

- Structure uses an always-on PMOS transistor.
- Pull-up is weak; pull-down is dynamic using NMOS logic.
- A **keeper transistor** was added to hold the output level in dynamic operation.
- Waveform simulation shows correct functionality through precharge and evaluation phases.

### 2. DCVSL (Differential Cascode Voltage Switch Logic)

- Consumes no static power.
- Uses cross-coupled PMOS transistors and complementary NMOS networks.
- Both output and its complement are generated simultaneously.
- Simulation confirms correct output and complementary behavior.

### 3. Dual-Rail Domino Logic

- Consists of precharge and evaluation phases like traditional domino logic.
- Both output and its complement are generated.
- XOR was designed using this technique and verified using simulations.
- Improved version includes a **keeper transistor** for charge retention.

## ✅ Summary

- RTL and transistor-level implementations were carried out successfully using Encounter_IC and custom schematics.
- Delay analysis showed the effect of pull-up resistor values on performance.
- Multiple logic families were compared based on performance, power, and area.

---

**Note**: All schematics, waveforms, and circuit layouts were generated and verified using standard VLSI CAD tools including `icfb` and `Encounter_IC`.
