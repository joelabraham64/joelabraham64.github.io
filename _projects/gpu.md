---
layout: page
title: GPU Prototype
description: Ongoing project building a basic parallel GPU-style accelerator on the iCEstick iCE40 FPGA
img: assets/img/Capture.PNG
importance: -1
category: Hardware
related_publications: false
---

## Overview

This is an **ongoing hardware project** focused on building a **very basic GPU-style accelerator** on the **iCEstick (iCE40 FPGA)**. The main goal is to explore how GPU-like speedups come from **parallelization**, even with limited FPGA resources, by running many small processing elements in parallel on the same workload.

Rather than targeting a full graphics pipeline, this project is centered around designing a minimal, educational “GPU core” that demonstrates the core ideas behind GPUs: **SIMD/SIMT-style execution, parallel compute units, and high-throughput operations**.

---

## Project Goals

- Implement a small set of **parallel compute lanes** (processing elements) on the iCE40
- Create a simple **instruction/control model** (broadcast control with lane-level execution)
- Build a lightweight **memory interface** suitable for small test workloads
- Demonstrate measurable speedup vs. a single-lane design on FPGA

---

## Architecture (Work in Progress)

Planned high-level blocks:

- **Controller / Dispatcher**  
  Issues operations to multiple compute lanes in parallel (GPU-like “warp” control at a very small scale)

- **Parallel Compute Lanes**  
  Multiple identical ALU-style units that run the same operation across different data elements

- **On-chip Memory / Buffers**  
  Simple scratchpad-style buffers for storing inputs/outputs (within iCE40 constraints)

- **Output / Verification Interface**  
  A basic way to inspect results (UART and/or LED/debug signals depending on the build)

---

## Constraints

The iCEstick iCE40 platform is intentionally resource-limited, so this project emphasizes:
- Small, efficient RTL blocks
- Careful tradeoffs between lane count vs. timing/resource usage
- Simple memory patterns and constrained bandwidth
- Step-by-step verification before scaling complexity

---

## Testing and Verification

Current / planned verification approach:
- Unit tests for each lane (ALU ops, registers, control)
- Small vector workloads to validate parallel correctness
- Comparison against a software reference model
- Timing/resource checks after each major feature addition

---

## Output and Demo Plan

Planned demo outputs include:
- Running small parallel kernels (e.g., vector add, dot product variants, simple image-style operations)
- Showing correctness via printed/serial output or debug traces
- Comparing runtime/throughput between:
  - 1-lane “CPU-like” version
  - multi-lane “GPU-like” parallel version

---

## Status

**In progress.**  
This page will be updated as the RTL, testing harness, and demo workloads mature.
