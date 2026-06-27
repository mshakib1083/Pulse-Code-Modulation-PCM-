# Pulse Code Modulation (PCM)

**Course:** EEE 310 - Communications Laboratory  
**Domains:** Digital Communications, Signal Processing, Hardware Design  

[![Read Full PDF Report](https://img.shields.io/badge/📄_Read_Full_Report-PDF-blue)](assets/report.pdf)

## Project Overview
This project explores the implementation of Pulse Code Modulation (PCM), a fundamental technique for digitally representing sampled analog signals. By performing sampling, quantization, and encoding, the system transforms continuous-time signals into a digital stream suitable for high-fidelity communication over digital channels.

## System Architecture & Methodology
The PCM process is divided into three critical stages, each implemented using dedicated hardware circuits.

### 1. Sampling Stage
The sampling stage converts the continuous analog input into a discrete-time signal using sample-and-hold circuitry.

| Sample & Hold (LF398N) | Sampling (NMOS) |
| :---: | :---: |
| ![S&H Circuit](assets/sampling_ckt_LF398N.png) | ![NMOS Sampling](assets/sampling_ckt_nmos.png) |

### 2. Quantization Stage
The quantization stage maps the sampled values into a finite set of discrete levels using a 3-bit quantizer to maintain signal integrity.

![Quantizer Circuit](assets/quantizer_ckt.png)  
*Figure: 3-bit Quantizer circuitry used to convert sampled levels into discrete binary values.*

### 3. Encoding Stage
The encoding stage converts the quantized levels into a digital binary stream using a priority encoder and parallel access shift registers for serial transmission.

| Priority Encoder | Shift Register |
| :---: | :---: |
| ![Encoder](assets/encoder_ckt.png) | ![Shift Register](assets/shift_register_ckt.png) |

## Full Hardware Implementation
The complete system combines these stages to demonstrate the full PCM transmitter chain on a breadboard setup.

![Full Circuit Schematic](assets/full_ckt.png)  
*Figure: Complete schematic diagram of the PCM transmitter chain.*

![Physical Hardware](assets/hardware.png)  
*Figure: Final hardware prototype showcasing the integrated PCM components.*
