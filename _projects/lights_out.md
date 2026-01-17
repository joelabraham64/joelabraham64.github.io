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

Unlike the traditional *Lights Out* game, this implementation does not include neighbor-based toggling or a win condition. Instead, it serves as a foundational state-machine framework that emphasizes clean control flow, input validation, and maintainable code structure.

---

## Software Design

The application is organized into multiple source and header files to enforce **separation of concerns**:

- **Input handling** is abstracted into a dedicated module to ensure safe, predictable user interaction.
- **Window logic** is encapsulated using structured data types and helper functions.
- **House-level state management** coordinates window behavior and system updates.

This modular approach improves readability, maintainability, and extensibility, and closely mirrors real-world software design practices used in systems and embedded programming.

---

## Skills Demonstrated

- Modular programming in **C** using multiple source and header files  
- State-machine logic and deterministic control flow  
- Structured data design using `struct` and function-based encapsulation  
- Robust user input handling and validation  
- Separation of concerns and maintainable software architecture  
- Debugging and iterative feature development in C  

---

## Potential Extensions

This project provides a strong foundation for future enhancements, including:
- Grid-based neighbor toggling (full *Lights Out* mechanics)
- Win condition detection
- Dynamic configuration of system size
- Embedded-style input/output adaptation

---

