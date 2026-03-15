# Traffic Light Controller (VHDL)

## Project Overview

This project implements a **Traffic Light Controller** using **VHDL** for FPGA-based digital systems. The controller manages traffic signals for **North–South and East–West directions** while supporting a **pedestrian crossing request**.

The system is designed using a **Finite State Machine (FSM)** architecture to ensure safe and coordinated traffic signal operation. State transitions are controlled by timing logic and pedestrian input signals.

This project demonstrates fundamental concepts of **digital system design, hardware description languages, and FPGA-based control systems**.

---

## Features

* VHDL-based hardware design
* Finite State Machine (FSM) implementation
* Traffic signal control for **North–South and East–West lanes**
* **Pedestrian crossing request button**
* Safe sequencing to prevent conflicting traffic signals
* Fully testable using simulation tools

---

## System Architecture

The controller is implemented as a **Finite State Machine** that cycles through different traffic signal states.

Typical state sequence:

1. North-South Green / East-West Red
2. North-South Yellow / East-West Red
3. North-South Red / East-West Green
4. North-South Red / East-West Yellow

If a **pedestrian request button** is pressed, the controller schedules a pedestrian crossing phase after the current traffic cycle completes.

State transitions are controlled using **clock-driven timing counters**.

---

## Design Components

### 1. Traffic Light Controller

Main VHDL module that implements the FSM and controls all traffic light outputs.

Responsibilities:

* Managing state transitions
* Generating traffic signal outputs
* Processing pedestrian input

### 2. Timing Logic

Clock-based counters define the duration of each traffic state (Green, Yellow, Red).

### 3. Pedestrian Control

Allows pedestrians to request crossing safely by activating a pedestrian signal after the current traffic phase.

---

## Project Structure

```
Traffic-Light-Controller/
│
├── traffic_light_controller.vhd   # Main VHDL design
├── testbench.vhd                  # Simulation testbench
└── README.md                      # Project documentation
```

---

## Simulation

The design can be simulated using standard FPGA development tools such as:

* ModelSim
* Xilinx Vivado Simulator
* QuestaSim

Simulation verifies:

* Correct state transitions
* Proper signal timing
* Pedestrian request behavior
* Conflict-free traffic operation

---

## How It Works

1. The system starts with a predefined traffic state.
2. A clock signal drives timing counters.
3. After a specified duration, the FSM transitions to the next state.
4. Traffic lights change according to the active FSM state.
5. If a pedestrian request is detected, a pedestrian crossing phase is inserted into the cycle.

---

## Possible Improvements

Future improvements for the project may include:

* Adjustable traffic timing parameters
* Pedestrian countdown display
* Emergency vehicle priority control
* FPGA board implementation with LEDs
* Sensor-based adaptive traffic control

---

## Technologies Used

* **VHDL**
* **Finite State Machines (FSM)**
* **Digital Logic Design**
* **FPGA Development**
* **ModelSim / Vivado Simulation**

---

## Author

**Mircivan Hakbilen**
Electrical and Electronics Engineering Student

