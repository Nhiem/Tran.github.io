---
title:  "TinyML -- Collaborative Optimization "
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

Our goals! to create practical neural-network based algorithms to address the issue of deploying large model size can’t fit into memory of embedded device. We proposed the machine learning algorithm base on combination: 
[**knowledge Distillation**] **+** [**Deep Compression**] (Model weight Pruning --> Model weight Clustering --> Model Quantization (Low bit precision and Quantization Noise)


The main concept of our algorithm, **first** using knowledge distillation which focus on techniques train the large and complex network on ensemble model which can extract important features from the given data. The knowledge from the complex model that call teacher model can transfer the knowledge to new smaller model call student model to obtain high-accuracy. **Second**, we jointly train deep model with different deep compression technique in different parts of model including parameter pruning, clustering, aware quantization during training and post training quantization. The main advantage of the algorithm extremely compresses the deep CNNs model with optimization model by knowledge distillation and jointly deep compression.

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Knowledge_distillation_model_compression.png?raw=true" width=700/>

**Deep collaborative compression distillation knowledge algorithm**


#### 1.Knowledge Distillation

Knowledge distillation is a model compression method that was first proposed by Bucila et al. [10] and generalized by Hinton et al. [11]. In general, it can be described as a special instance of learning with privileged information, e.g. Vapnik & Izmailov [12] In distillation knowledge or the extraction of features of a given supervised dataset is transferred from the large complex model call the teacher model to the smaller model call student model that mimic teacher model by minimizing a loss function with the target is the distribution class probabilities predicted by teacher model.

[10] [Bucila, Caruana, and Niculescu-Mizil 2006] Bucila, C.; Caruana, R.; and Niculescu-Mizil, A. 2006. Model compression. In SIGKDD, 535–541. ACM.
[11] [Hinton, Vinyals, and Dean 2015] Hinton, G.; Vinyals, O.; and Dean, J. 2015. Distilling the knowledge in a neural network. In NIPS Deep Learning and Representation Learning Workshop.
[12] [Lopez-Paz et al. 2015] Lopez-Paz, D.; Bottou, L.; Scholkopf, B.; and Vapnik, V. 2015. Unifying distillation and privileged information. arXiv preprint arXiv:1511.03643.

#### 2. Deep Compression Pipeline 

**[Model parameter Pruning --> Clustering(paramters sharing same values) --> Quantization(low bit preicision int4, int8) ]**

Both the teacher model and student from Distillation Technique's jointly apply **collaborative optimization** at each convolution layer. We deploy the model’s collaborative optimizing weight pruning technique to eliminate the redundant connection while retaining meaning and 
informational connection, and followed by applying weight clustering which will share the same weight across multiple connections. 
Eventually, the quantization aware training applied from the int4, int8 bit precision quantization is deployed during the training. The combination collaborative optimization of pruning, clustering, and quantization will compress the network without interfering with each other and will lead to a significant high compression ratio. As the result of optimization makes the storage required by tens and a hundred MB to a few MB of size and significantly reduces more than an order of 
magnitude of the model complexity, the storage requirement, and the increased latency  performance of the model, and less low energy consumption.  

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Collaborative_optimization.png?raw=true" width=700/>


#### 3. Deep Compression Experiment on Embedded CPUs Systems: 

The experiment conducted on two embedded hardware platform from NVIDIA Jetson Nano & Raspberry Pi. Both hardwares development platform using Arm Cortex A architectures. 

<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/embedded_CPU_Experiment.png?raw=true" width=700/>

The design of model optimizations is depending on the tasks, you might need to make tradeoff between model complexity, size, performance. If the applications require high accuracy, then you might need to design large and complex model. For tasks that require less precission, you should use a smaller model because they not only use less disk space and memory, but they are also generally faster and more energy efficient.

Experiment Conducted MobileNetV2 with Deep Compression Pipeline.

**Notebook--Code** 
**https://colab.research.google.com/drive/1wraoCjrIalXSWRTftNJuVMYc3D26N4xw?usp=sharing** 

1. The model was firs apply sparsity from [50% to 80% zeros in weights] sparsity by [**Constantsparsity**, **Schedule**, **Prunable**, **PruneForLatency**] we can customize the layers to aplly the sparsity, usually the layer take most computation like **Conv2D** and **Dense** layer.

2. Following Apply the cluster_weights() to enforce the model's parameter to share the same value by Kmean cluster{Cluster centroid can be initialized **LINEAR**, **RANDOM**, **DENSITY_BASED**, **KMEANS_PLUS_PLUS**} 

3. Last is the Quantizations, Deep compression pipeline implement [**Quantization Aware Training** or **Post Quantization**].  For the model **Quantization Aware Training** emulates inference-time quantization that inject the model the errors cause by quantize lower-precision (e.g. 4-bit, 8-bit instead of 32-bit float) model can be update learn during training, leading to benefits during deployment.
**Model Post Quantization** includes general techniques to reduce CPU and hardware accelerator latency, processing, power, and model size with little degradation in model accuracy. Model parameter can be quantize to 4-bits, 8-bits, 16-bits instead of 32 bits.

#### Result of Model reduction Size and Model Accuracy -- Model Convert to .tflite format for speed up infrence in embedded CPUs

1. **Model Size Reductions** 
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/model_size.png?raw=true" width=700/>

2. **Model Accuracy** 
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/model_accuracy.png?raw=true" width=700/>

3. **Model Inference Time -- Memory Usages.
<img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/experiment_Raspi.png?raw=true" width=600/> <img src= "https://github.com/Nhiem/tran.github.io/blob/master/tinyml/jetson_nano_experiment.png?raw=true" width=600/>

#### 3. Method Mathematic & Details Information: 
Article for  **Deep Collaborative Optimization Techniques** :<a href="https://github.com/Nhiem/tran.github.io/blob/master/tinyml/Deep_Collaborative_Optimization_Techniques.pdf" target="_blank">PDF.</a>






