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

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Arm_architecture family.PNG?raw=true" width="550" />

To consider our TinyML applications by the **algorithm complexity** to **power consumption** from MCU to CPUs processers to decide which type of processor MCUs? or CPUs for our deployment.

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/arm_cortex_family.png?raw=true" width="550" />

### 2. Machine Learning Framework 

**#### How to Train and Deployment your Machine Model?**
There are many different framework that you can deploy for TinyML application as shown in figure below. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/model_size_reduction.png?raw=true" width="550" />

**Example Using XCubeAI, Tensorflow Lite, and TVM deploy ML models for TinyML applications **

**+ Runing Models with TFlite in Colab**
https://colab.research.google.com/github/tinyMLx/colabs/blob/master/3-3-7-RunningTFLiteModels.ipynb

**+ Runing Models XCubeAI**

**https://www.st.com/resource/en/user_manual/dm00570145-getting-started-with-xcubeai-expansion-package-for-artificial-intelligence-ai-stmicroelectronics.pdf**


The most popular and handful is **Tensorflow Lite & Tensorflow Lite Micro**, With TensorFlow there are a number of different ways you can deploy these models. The overall **TensorFlow ecosystem** can be represented using a diagram like this -- with the left side of the diagram showing the architecture and APIs that can be used for training models. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/the_overal_eco_system.png?raw=true" width="550" />

+ The standard **TensorFlow models** that you’ve been creating this far, trained without any post-training modification can be deployed to Cloud or Servers. **https://www.tensorflow.org/tfx/guide/serving**

+ TensorFlow Lite is a runtime that is optimized for smaller systems such as Android, iOS and embedded systems that run a variant of Linux, such as a Raspberry Pi. **https://www.tensorflow.org/lite/microcontrollers**

+ TensorFlow.js provides a javascript-based library that can be used both for training models and running inference on them in JavaScript-based environments such as the Web Browsers or Node.js.
**https://www.tensorflow.org/js** 

+ TensorFlow Lite Micro, which is built on top of TensorFlow Lite and can be used to shrink your model **even further to work on microcontrollers** and is a core enabling technology for TinyML
**Detail about tensorflow Lite Micro For embedded MCUs and CPUs**. 
**https://www.tensorflow.org/lite/microcontrollers** 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Tensorflow_lite_Micro.png?raw=true" width="550" />





