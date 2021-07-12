---
title:  "TinyML -- Collaborative Optimization -- Binary Neural Networks"
mathjax: true
layout: post
categories: media
---
# Bringing Machine Learning Algorithms to Edge, Embedded Devices.  

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/tinyml_MCU.png?raw=true" />


## 1. Deep Collaborative Optimization Techniques.  

### This Study Aims To.

Deep learning techniques have been transformed, how mobile and embedded devices interpret and react smarter and efficiency to the world. The growth of the future of machine learning on edge, embedded, mobile devices will need more addition breakthrough in **efficient of learning algorithm** and **hardware acceleration** development. 
This proposes method try to create the **Optimal and Efficient** learning algorithm to deploy on **IoT**, **EMBEDDED***, **MOBILE** Devices. 
For machine learning to fulfill its promise in many mobiles and embedded devices, there are existing many challenges we need to address. These fundamental challenges include **memory-constrained**, **low latency**, **privacy**, **bandwidth**, **power consumption, and real-time performance, hardware accelerator** and many more. The concept of pushing computing closer to where sensors gather data is a central point of modern embedded systems at the edge of the network. 

We propose **End_to_End approach computer vision on embedded devices** is a compact **PIPELINE**  deploying advanced deep learning algorithms on edge devices especially for computer vision applications like autonomous vehicles and IoT requires special capabilities. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/end_to_end_pipeline_computer_vision.png?raw=true" />


### Collaborative optimization algorithm pipline detail.


[**knowledge Distillation**] + [**Deep Compression**] **(Model weight Pruning --> Model weight Clustering --> Model Quantization (Low bit precision and Quantization Noise)**

Our goals! to create practical neural-network based algorithms to address the issue of deploying large model size can’t fit into memory of embedded device. We proposed the machine learning algorithm base on combination **knowledge distillation** and **deep model compression** of CNNs model. 
The main concept of our algorithm first using knowledge distillation which focus on techniques train the large and complex network on ensemble model which can extract important features from the given data. The knowledge from the complex model that call teacher model can transfer the knowledge to new smaller model call student model to obtain high-accuracy. Second, we jointly train deep model with different deep compression technique in different parts of model including parameter pruning, clustering, aware quantization during training and post training quantization. The main advantage of the algorithm extremely compresses the deep CNNs model with optimization model by knowledge distillation and jointly deep compression.
