---
title:  "TinyML -- Fundamentals -- Deploying -- Applications   "

mathjax: true
layout: post
categories: media
---

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Post_Picture.png?raw=true" width="700" />

## I. Concept of TinyML

### **What is Tiny Machine Learning (TinyML) ?**

TinyML is the field at the intersection of embedded Machine Learning (ML) applications, algorithms, hardware, and software. TinyML explores and optimize machine learning algorithm That's can run on small, low-powered devices like microcontrollers MCUs.It enables low-latency, low power and low bandwidth model inference at edge devices.

### **Why TinyML is important ?**
While **standard GPUs** training neural net consumes around 65 watts to 85wats, But typical **MCUs** like Arm cortex M3-M4 consumes power that **thousand times less** power consumption. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/GPU_MCU_CPU.png?raw=true" width="550" />

**The Future of ML applications is Tiny.**

### **Advantages of TinyML**

**1. Low Latency:** 

Depending Tiny applications,  If application runs inference ML model on the edge, and the data doesn't need to retrive or send to a server to run inference. This reduces the latency of the output.

**2.Low Power Consumption:**

microcontrollers consume very little power. TinyML devices to run unplugged on batteries for weeks, months, and in some cases, even years, while running ML applications on edge for a long time.

**3.Low Bandwidth:**
In the applcations, The Data doesn’t have to be sent to the server store information, so the device internet bandwidth is used very small.

**4. Cost Efficient:**

Microcontrollers facilitate automation and embedded control in electronic systems, as well as the connection of sensors and applications to the IoT. These handy little devices are also exceedingly cheap, with an average price of 60 cents per unit (and dropping).

## II. TinyML PipeLine Developments. 

### 1. Tiny Hardware

In TinyML application on MCUs and Embedded CPUs general will deploy on Arm chip architecture. 
**Why is Arm MCU and CPUs?**
The Arm architecture is one of the most popular processor architectures in the world today. 
+ Small processor for lower power consumption
+ Hide Code density for limited memory and physical size restrictions
+ The ability to use slow and low-cost memory

There are three architecture profiles: **A, R and M**

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/arm_cortex_family.png?raw=true" width="550" />





