---
title:  "Embedded System Project"
mathjax: true
layout: post
categories: media
---

## III. Integrated TDR monitoring system on physical modelling for disaster prevention. (08/2019-07/2020) 

Research and Experiment Conducted on Centrifuge Machine in National Central University 

**NCU Centrifuge Maching**

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/_posts/IMGP8079.JPG?raw=true" width="700" /> 
                                                                                                
This study proposed the development embedded TDR (Time Domain Reflectometry) system integrated with centrifuge reverse fault physical modeling to simulate sliding at depth to simulate the shear plane in the centrifuge modeling at the different earth gravity levels. 
The prototype model can investigate through the 1/N scale model by enhancing the N time level earth gravity field. 


<img src= "https://github.com/Nhiem/tran.github.io/blob/master/_posts/TDR_System.png?raw=true" width="500" /> 
Fig 1. Demonstrate of TDR system

### Design & Integreate Embedded TDR DAQ integreate with Centrifuge DAQ System

+	**Centrifuge DAQ System**

The centrifuge DAQ system, as shown in Fig.1, consists of the control mounted PC, Ethernet switch, WDM converter, fiber optic rotary joint, NI PCI-6250 card, and NI SCXI modules (National Instruments). The mounted SRC-200 PC is an x86 compatible computer manufactured by Small PC Inc. The NI PCI-6250 card is a multi-function data acquisition board installed in the mounted PC. The NI SCXI modules container which mounts on the centrifuge contains 4 types of modules for various measuring purpose. The SCXI-1531 is an 8-channel accelerometer input module. The SCXI-1520 is an 8-channel universal strain gauge input module which also builds on 350 ohms resistances. The SCXI-1540 is an 8-channel linear-voltage differential transformer. (LVDT) module. The SCXI-1102C is a 32-channel voltage meter module amplifier. 

+ **TDR DAQ**	

The 8-channel Line Impedance Analyzer TDR1500x8 SYMPULS is shown in Fig 3 (a). The impedance analyzer TDR 1500x8 with a multiplexer is used for precise analysis of various lines. TDR 1500x8 shows directly the line impedance as a function of the propagation time or the distance. The variation of the impedance of a given line is shown in the form of an oscillogram directly on the personal computer. The reﬂections and transitions are displayed directly and can be analyzed with accuracy to millimeters. The combination of a fast pulse generator and sampling scope leads to a system-rise time of less than 200ps. The TDR1500x8 uses a fully digital time-base that makes it unsusceptible to environmental changes.


<img src= "https://github.com/Nhiem/tran.github.io/blob/master/_posts/centrifuge_researhc.png?raw=true" width="600" /> 
Fig 2 Diagram shown TDR DAQ configure in centrifuge DAQ system.



TDR impedance analyzer is embedded in centrifuge DAQ system by connecting with computer PA-2000 by connecting through USB protocol port as shown in Fig.2 The system can access the TDR console in the control room, and utilize the LabVIEW program to launch the acquisition sequence at the mounted PC through the remote desktop program. LabVIEW program was written for continuous taking TDR waveform reflection during testing, and the program interface is shown in Fig.3. (b).
                                    


<img src= "https://github.com/Nhiem/tran.github.io/blob/master/_posts/LabVIEW_program.jpg?raw=true" width="600" /> 
Fig 3. TDR transmission line impedance analyzer TDR1500*8 SYMPULS, (b) LabVIEW program interface controls TDR analyzer for taking waveform reflection.
                                                                                                
### Project Report Information 
The written report: <a href="https://github.com/Nhiem/tran.github.io/blob/master/_posts/TDR_Report.pdf" target="_blank">PDF.</a>


