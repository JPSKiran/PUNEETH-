# 🏏 T20 Cricket Game on FPGA (Artix-7 Edge Board)

## 📘 Overview

This project implements a mini T20 cricket game in Verilog on the **Artix-7 Edge FPGA** board. It simulates two batting innings using a pseudo-random LFSR and displays real-time score, overs, and game result using 7-segment displays and LEDs.

---

## 🎯 Features

- 🔁 Random event generation using LFSR
- 🔢 7-Segment display for:
  - Team scores
  - Overs and balls
- 💡 LEDs for:
  - Wickets
  - Overs completion
  - Winning team scroll
- 🔘 Push-button for ball-by-ball control
- ⏱️ Real-time simulation

---

## 🧩 Code Structure

### 🔝 `t20_cricket_game.v` (Top Module)
- Integrates all modules
- Handles user input, score control, and game state transitions

### 📦 Submodules

| File                | Description                                          |
|---------------------|------------------------------------------------------|
| `lfsr.v`            | 8-bit LFSR for random score/wicket generation       |
| `score_manager.v`   | Manages score, wickets, overs, innings, winner      |
| `seven_seg_driver.v`| Converts binary values to 7-segment format          |
| `led_controller.v`  | Controls LEDs for visual result display             |
| `debounce.v`        | Debounces push-button input                         |

---

## 🖥️ Hardware Setup

- **Board**: Artix-7 Edge FPGA  
- **Input**: Push-button (1-bit)
- **Output**:  
  - 7-Segment Displays for score & overs  
  - LEDs for wickets, overs completed, and winner scroll

---

## 🧪 Simulation

- **Tool**: ModelSim / Vivado Simulator
- **Testbench**: `t20_cricket_tb.v`
- Tests:
  - LFSR randomness
  - Game state transitions
  - Winner declaration logic

---

## 📸 Visuals

### 🔋 Score Generator
![2_score_generate](https://github.com/user-attachments/assets/1766dd47-0539-489f-a288-5a1026bf77d4)

### 🔁 Game Flow
![Game Flow](https://github.com/obulsai/T20-CRICKET/blob/ede03724f2d1148bce0b87dbe8296671ec4f2e01/Module_designs/game_flow.jpeg)

### 📐 Elaborated RTL Design
![elaborated_design](https://github.com/user-attachments/assets/4c0f9973-ffaf-4aef-8488-3ceb38a175cc)


---

## ▶️ Run Instructions

1. Open project in **Vivado 2020.2+**
2. Synthesize and Implement the design
3. Generate Bitstream and program to FPGA
4. Press the push-button for each delivery
5. Monitor:
   - Score and overs on 7-segment displays
   - Wickets, innings, and result via LEDs

---

## 🎥 Demo Video

📺 [Watch on YouTube](https://youtu.be/kWOw-FWc5Vg?si=2BD5atmlYgCtzvvv)

---

## 🚀 Future Enhancements

- Simulate bowler variations
- Add over countdown timer
- Use UART/OLED for commentary and score stats

---

## 👤 Author

**J.PSKiran**  
ECE 4th Year, RGUKT ONGOLE  
🔗 GitHub: [JPSKiran](https://github.com/JPSKiran)  
📹 Project Demo: [YouTube](https://youtu.be/kWOw-FWc5Vg?si=2BD5atmlYgCtzvvv)
