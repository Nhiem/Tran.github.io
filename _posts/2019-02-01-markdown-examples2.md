---
title:  "TinyML -- Fundamentals -- Deploying -- Applications   "

mathjax: true
layout: post
categories: media
---

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Post_Picture.png?raw=true" width="700" />

# I. Concept of TinyML

### **What is Tiny Machine Learning (TinyML) ?**

TinyML is an exciting new field that intersects embedded Machine Learning (ML) applications, algorithms, hardware, and software. This field seeks to optimize machine learning algorithms that can run on small, low-powered devices such as microcontrollers (MCUs). TinyML enables low-latency, low power, and low bandwidth model inference at edge devices, which opens up a world of possibilities for innovative new applications in a variety of fields.

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Applying_TinyML.png?raw=true" width="350" />



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

#### **How to Train and Deployment your Machine Model?**

There are many different framework that you can deploy for TinyML application as shown in figure below. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/model_size_reduction.png?raw=true" width="550" />

**Example Using XCubeAI and Tensorflow Lite deploy ML models for TinyML applications**

**+ Runing Models with TFlite in Colab**
https://colab.research.google.com/github/tinyMLx/colabs/blob/master/3-3-7-RunningTFLiteModels.ipynb

**+ Runing Models XCubeAI**

https://www.st.com/resource/en/user_manual/dm00570145-getting-started-with-xcubeai-expansion-package-for-artificial-intelligence-ai-stmicroelectronics.pdf


The most popular and handful is **Tensorflow Lite & Tensorflow Lite Micro**, With TensorFlow there are a number of different ways you can deploy these models. The overall **TensorFlow ecosystem** can be represented using a diagram like this -- with the left side of the diagram showing the architecture and APIs that can be used for training models. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/the_overal_eco_system.png?raw=true" width="550" />

+ The standard **TensorFlow models** that you’ve been creating this far, trained without any post-training modification can be deployed to Cloud or Servers. https://www.tensorflow.org/tfx/guide/serving

+ TensorFlow Lite is a runtime that is optimized for smaller systems such as Android, iOS and embedded systems that run a variant of Linux, such as a Raspberry Pi. https://www.tensorflow.org/lite/microcontrollers

+ TensorFlow.js provides a javascript-based library that can be used both for training models and running inference on them in JavaScript-based environments such as the Web Browsers or Node.js.
https://www.tensorflow.org/js

+ TensorFlow Lite Micro, which is built on top of TensorFlow Lite and can be used to shrink your model **even further to work on microcontrollers** and is a core enabling technology for TinyML
**Detail about tensorflow Lite Micro For embedded MCUs and CPUs**. 
https://www.tensorflow.org/lite/microcontrollers

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Tensorflow_lite_Micro.png?raw=true" width="550" />

### 3. TinyML Applications 

By summarizing and analyzing data at the edge on low power devices, TinyML offers many unique solutions. Even though TinyML is an emerging field. 
Machine Learning Applications is real-world problems is really import range from computer visions to Audio-Voice, Sensor fusions.   

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/General_applications_of_MachineLearning.PNG?raw=true" width="650" />

Three main important fields for TinyML applications: 

1. **Industrial Predictive Maintenance**: Machines are prone to fault. Using TinyML on low powered devices, it is possible to monitor the machine and predict faults ahead of time constantly. This predictive maintenance can lead to significant cost savings.

2. **Healthcare**: Globally, healthcare systems are facing increasing chronic symptoms and struggling with the pressure of increased costs, TinyML helps improve medical care, from follow-up to prevention to provide cost-effective operators for low-power electronic devices across healthcare. 

3. **Civil Infrastructure - Logistics -- SmartHome**: Rely heavily on data for activities such as dynamic pricing, supply management, and analysis of future demand as they become more connected to the network through digital transformation. The integrity and security of this data is paramount to organizations that manage a wide range of critical infrastructures such as electricity, solar, gas, heat, and water.
+ The supply chain is becoming more complex and the need for effective logistics extends to all industries. IoT enables end-to-end visibility, how businesses transport products, manage inventory and mobile assets, replenish inventory, manage retail experiences, plan and perform maintenance Will be renewed.
+  With IoT Home, the home fits seamlessly into the resident's family. New home appliances powered by internet connectivity, such as smoke detectors, televisions, refrigerators, smart lighting and heating, are now constantly using sensor technology to gather data from the physical world around us.



## III. TinyML Design Principles. 

In order to design optimally TinyML applications, we have to overcome the major challenges implement machine learning in embedded devices. 
There are three important principles:
**Principle 1: Minimize Feature Scope for Portability**
Most embedded devices are resource constraints including memory, computing cability. In TinyML, machine learning model, input data, output prediction are in memory. Embedded ML engineer should really consider to design optimal and efficient algorithm to overcome the contrains objectives in embedded devices. 

*Example of Memory usage of specific Embedded devices*

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/memory_usage.png?raw=true" width="650" />

**Principle 2: Embedded devices Ecosystem**

Because the difference of Embedded devices plateforms there is no one-size-fits-all optimzation solution.As a result of device fragmentation, developers can’t build software that runs well on different embedded platforms. In order to tackle this challenge, the authors ensure that optimizing the core library operations is easy.


**Principle 3: Reuse Tools and Scalability**

Exporting a model comes with its own set of challenges. It is also important to note that most models are trained on floating operations and these operations consume more space and memory and would therefore be unsuitable for an embedded device. This can be addressed by converting them to a quantized representation. This, however, increases the exporter complexity. To address these challenges, a converter is built on top of the existing TensorFlow Lite toolchain. 


## IV TinyML Implementation End-to-End Pipeline

**TinyML Life Cycle**

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/Life_cycle_ML.png?raw=true" width="650" />

**1 Capture Data** 
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/capture_data.png?raw=true" width="100" />

Capture a sufficient amount of representative data about the phenomenon that is being modeled. This usually involves placing sensors on or near the object being monitored in order to record its state and changes over the time. Examples of physical parameters include acceleration, temperature, sound, and visual depending on your application.

**2 Processing Clean, label Data**
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/clean_data.png?raw=true" width="100" />

Raw data has been acquired from sensors need to be labeled and pre-processing. The data sets must be characterized so that the different outputs can be classified correctly. 

**3 Machine Learning Model**
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/training_model.png?raw=true" width="100" />

The Neural Network in an iterative manner so that the Network's outputs can minimize desirable error criteria. Training, and testing is typically performed using off-the-shelf Deep Learning frameworks. This is usually done on a powerful computing platform with computational power such sever and cloud, to allow many iterations in a short period of time.

**4 Convert ML into optimized code for MCUs**
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/convert_model.png?raw=true" width="100" />

The next step is to embed the pre-trained ML algorithm into an MCU (optimized code minimizing complexity and memory requirements).

**5 Process & analyze on real-world data**
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Binary_Neural_Network/process_analysis.png?raw=true" width="100" />

Finally, deploy ML algorithm embedded in an MCU in your application.

