# Early-Detection-of-Wrist-Movement-Intention-Using-Wearable-Forearm-sEMG

Python signal-processing and classification tools developed during an Undergraduate Research Opportunity at Imperial College London.

**Author:** Muhammad Abubakar  
**Supervisor:** Prof. Kristel Fobelets  
**Project:** *Early Detection of Wrist Movement Intention Using Wearable Forearm sEMG*

## Overview

This project investigates whether surface electromyography (sEMG) recorded from the forearm can be used to detect **voluntary wrist/hand movement intention before substantial mechanical movement occurs**.

The work builds on the wearable sEMG platform developed by **Abby Finka** as part of her Imperial College London final-year project:

> **Development of a Flexible EMG Readout Board for Wearable Hand Movement Prediction**

Her original repository, including the ADS1198/ESP32-S3 acquisition hardware, firmware, BLE interface and Python visualisation software, can be found here:

**Original hardware/software platform:**  
https://github.com/abbyfinka/FYP-Knitted-EMG

This repository contains the software developed during my follow-on project, focusing specifically on:

- EMG baseline calibration
- Channel-specific movement-onset detection
- Early transient extraction
- Time-domain feature extraction
- Initial hand-gesture classification

The aim is not simply to classify the final hand position, but to identify useful muscle activity **as early as possible after activation begins**.

---

## Background

The original wearable system uses an **ADS1198 analogue front end** and **ESP32-S3 microcontroller** to acquire eight differential sEMG channels from a knitted forearm armband.

The previous project focused primarily on classification once a hand/wrist movement had developed.

My project instead investigated the **transient period immediately after muscle activation**, with the longer-term goal of enabling assistive devices to distinguish intended voluntary movement from involuntary motion such as tremor.

During algorithm development, recordings from an **OpenBCI Cyton** board were also used as a controlled and repeatable EMG source while the custom wearable hardware was being debugged.

---

## Processing Pipeline

The software was developed as a staged pipeline:

```text
Resting EMG
    |
    v
Baseline calibration
    |
    v
Channel-specific activation thresholds
    |
    v
EMG onset detection
    |
    v
Transient window extraction
    |
    v
Feature extraction
    |
    v
Gesture classifier
