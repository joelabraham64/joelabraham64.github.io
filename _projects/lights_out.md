---
layout: page
title: Pseudo Lights Out Game
description: A modular, state-based C program inspired by the Lights Out puzzle
img: assets/img/4.jpg
importance: 7
category: Software
related_publications: false
---

## Overview

The **Pseudo Lights Out Game** is a console-based application written in C, inspired by the classic *Lights Out* puzzle. The project was developed to explore modular software design, state-based logic, and structured programming in a low-level language.

The program simulates a house composed of multiple windows, each represented by a binary on/off state. Users interact with the system through single-character keyboard input, toggling individual windows while the application continuously updates and displays the current system state.

Unlike the traditional *Lights Out* game, this implementation does not include neighbor-based toggling. Instead, it functions as a deterministic state machine in which each window is toggled independently.

---

## Software Design

The application is organized into multiple source and header files to enforce **separation of concerns**:

- `main.c` – Program control loop and user interaction  
- `house.c / house.h` – House-level state management  
- `window.c / window.h` – Individual window state and toggle logic  
- `ezinput.c / ezinput.h` – Single-character, validated user input handling  

This modular design improves readability, maintainability, and extensibility, and mirrors real-world software practices used in systems and embedded programming.

---

## Game States

### Initial State

At program startup, a subset of windows is enabled, resulting in the following initial configuration:

![Initial State](/assets/img/initial_state.jpg)


---

### Winning Input Sequence

While the program does not explicitly enforce a win condition in code, a “solved” state can be interpreted as all windows being turned off.

For the default starting configuration, the system reaches this solved state by toggling the following windows:

**Winning input sequence:**
4, 5, 7, 8, 9

Each input toggles the corresponding window’s state.

---

### Final State

After applying the winning input sequence, all windows are turned off, resulting in the following final configuration:

![Initial State](/assets/img/final_state.jpg)

The program continues running until the user exits by entering `0`.

---
**Source Code:**  
[View the project on GitHub](https://github.com/joelabraham/lights_out)


## Skills Demonstrated

- Modular programming in **C** using multiple source and header files  
- State-machine logic and deterministic control flow  
- Structured data design using `struct` and function-based encapsulation  
- Robust user input handling and validation  
- Separation of concerns and maintainable software architecture  
- Debugging and iterative feature development in C  

---


