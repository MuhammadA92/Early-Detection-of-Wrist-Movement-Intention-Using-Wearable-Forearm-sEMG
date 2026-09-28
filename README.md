# Early Detection of Wrist Movement Intention Using Forearm sEMG

Software and wearable-electronics development from an Undergraduate Research Opportunity at Imperial College London, investigating whether forearm surface electromyography (sEMG) can be used to detect voluntary wrist and hand movement intention before substantial mechanical movement occurs.

**Author:** Muhammad Abubakar  
**Supervisor:** Prof. Kristel Fobelets  
**Institution:** Imperial College London  
**Project:** Undergraduate Research Opportunity (UROP), 2026

## Project Overview

This project builds on the wearable sEMG platform developed by **Abby Finka** during her final-year MEng project at Imperial College London:

**[Development of a Flexible EMG Readout Board for Wearable Hand Movement Prediction](https://github.com/abbyfinka/FYP-Knitted-EMG)**

Finka's project developed an eight-channel wearable sEMG acquisition system based on the **ADS1198 analogue front end** and **ESP32-S3 microcontroller**, with Bluetooth Low Energy transmission and a Python interface for visualising and recording EMG data.

My follow-on project focused on two main areas:

- **Wearable hardware redesign:** miniaturising and modularising the existing electronics to improve integration with the knitted forearm armband.
- **Movement-intention detection:** investigating the early transient period of the EMG signal to detect muscle activation before substantial mechanical movement, rather than focusing only on classification of the final hand or wrist position.

The longer-term motivation is the development of assistive wearable systems capable of identifying intended voluntary movement early enough to distinguish it from involuntary motion such as tremor.
