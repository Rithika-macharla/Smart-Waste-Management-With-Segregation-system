# Smart-Waste-Management-With-Segregation-system
# Smart Waste Management with Automatic Dry/Wet/Metal Segregation

This project implements a **smart waste‑management bin** that automatically segregates waste into **dry, wet, and metal** categories using a **rotating dumping mechanism**. The system uses simple sensors and a microcontroller (such as Arduino/NodeMCU/ESP32) to detect, classify, and route each item into the correct bin without any manual effort.

## Project Objective

- Automate source‑level segregation of household or institutional waste into:
  - **Dry waste** (paper, plastic, non‑organic).
  - **Wet waste** (organic/food waste).
  - **Metal waste** (cans, foil, metallic objects).
- Improve recycling efficiency and reduce contamination between waste streams.
- Provide a compact, low‑cost hardware prototype suitable for small‑scale deployment in homes, hostels, or offices.

## Key Features

- Uses **IR sensor** to detect when an object is dropped into the chute.
- **Moisture sensor** identifies wet (organic) waste.
- **Metal‑detection sensor (inductive type)** recognizes metallic items.
- Microcontroller (Arduino/NodeMCU/ESP32) runs a simple classification logic.
- **Servo‑driven rotating flap or pipe** directs waste into the appropriate bin (dry / wet / metal).
- Optional future extension: IoT‑based bin‑level monitoring and alerts.

## Hardware Requirements

- 1 × **Microcontroller**: Arduino Uno / NodeMCU / ESP32
- 1 × **IR sensor** (for object detection at the chute entrance)
- 1 × **Moisture sensor** (rain‑drop or soil‑moisture‑type sensor)
- 1 × **Metal‑detection sensor** (inductive proximity sensor)
- 1–2 × **Servo motor(s)** (e.g., SG90 for the rotating mechanism)
- 3 × **Bins** (for dry, wet, and metal waste)
- Wires, power supply (5 V adapter or USB power bank)
- Chassis/box to assemble the chute and bins

## Software Requirements

- Arduino IDE (or ESP‑based IDE if using ESP32/NodeMCU).
- Basic Arduino libraries (e.g., `Servo.h` for controlling the servo).
- Simple sequential logic for:
  - Reading sensor values.
  - Classifying waste as metal / wet / dry.
  - Rotating the servo to the correct bin angle.

## How It Works

1. The user drops waste into the central chute.
2. The **IR sensor** detects the object and triggers the system.
3. The microcontroller:
   - Checks the **metal sensor** output.
   - If metal is detected, the item is routed to the **metal bin**.
   - If not, the **moisture sensor** decides:
     - **Wet** → route to **wet bin**.
     - **Dry** → route to **dry bin**.
4. The **servo‑driven rotating flap or pipe** turns to the corresponding angle, guiding the waste into the correct bin.
5. After the item is dumped, the servo returns to the neutral position and waits for the next item.

## How to Use This Repo

1. Clone the repository:
   ```bash
   git clone https://github.com/Rithika-macharla/Smart-Waste-Management-With-Segregation-system.git
