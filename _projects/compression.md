---
layout: page
title: Compression
description: Run-Length Encoding (RLE) Compression and Analysis
img:
importance: 4
category: Software
---

## Overview

This project implements a **run-length encoding (RLE) compression algorithm** in C and pairs it with a Python-based analysis script to study and visualize compression behavior. The goal is to explore fundamental data compression techniques, sequential data processing, and the trade-offs between compression efficiency and input characteristics.

Run-length encoding is a simple, lossless compression method that replaces consecutive repeated values with a single value and a count. While straightforward, RLE highlights important concepts in algorithm design, state tracking, and file-based data processing.

---

## C Implementation

The core compression logic is implemented in **C**, where input data is processed sequentially and encoded as value–count pairs. The program is organized into multiple source and header files to enforce **modular design** and separation of concerns.

Key characteristics of the C implementation include:
- Sequential scanning of input data
- Detection and encoding of repeated runs
- Clear separation between program control logic and compression functionality
- File-based input and output handling

This structure improves readability, maintainability, and mirrors software design patterns used in systems-level programming.

---

## Python Analysis and Visualization

To support evaluation and reporting, a **Python script** using NumPy and Matplotlib is included to analyze and visualize the behavior of the RLE compression algorithm.

The Python component:
- Generates numerical data related to compression behavior
- Produces plots illustrating trends such as compression efficiency
- Exports figures as PDF files suitable for reports or submissions

This separation of implementation (C) and analysis (Python) reflects a realistic engineering workflow, where performance-critical code is written in a low-level language and evaluated using higher-level tools.

---

## Skills Demonstrated

- Implementation of **run-length encoding (RLE)** compression algorithms  
- Sequential data processing and state tracking in **C**  
- Modular software design using multiple source and header files  
- Command-line program structure and file I/O  
- Data analysis and visualization using **Python**, NumPy, and Matplotlib  
- Separation of algorithm implementation and performance analysis  

---

## Potential Extensions

This project provides a foundation for future improvements, including:
- Decoding support for full compression/decompression pipelines
- Compression ratio analysis for different input patterns
- Comparison with other lossless compression techniques
- Integration of analysis directly with compressed output files
