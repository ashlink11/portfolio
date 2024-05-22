# project three plan notes
##### created: apr 15, 2024

## ideal backend tech stack (high-level)

- language:
  - C++
  - (& C) 
- model: deep learning network models/algorithms
  - network graphs
    - graph partitioning
    - tensor sharding
    - ^current and next-gen?
  - what do deep learning engineers need for their software? 
- compiler: performance optimizations
  - XLA
  - (& OpenXLA, TVM, MLIR, LLVM, OpenAI Triton)
  - performance tuning & analysis
  - debugging, performance, testing
  - what makes a deep learning compiler?
- ML frameworks:
  - JAX
    - research its APIs 
  - (& TensorFlow, PyTorch)
  - e.g. what is contributing to these like?
- ISA: (GPU/GPU architecture e.g. SIMT, etc.) (backend codegen)
  - CUDA
  - & OpenCL
  - (& OpenGL)
  - what do architects need?
- cloud distribution at scale: (training & inference)
  - is there a nvidia cloud platform?
  - (& Modular)
  - (etc.)  

- next steps:
  - research how nvcc and ptx fit into this
  - re-plan project two so i can get here
  - tune project one page to lead to here

optional considerations:
- target AWS Graviton chips (64-bit ARM-based) "The processor family is distinguished by its lower energy use relative to x86-64, static clock rates, and omission of simultaneous multithreading. It was designed to be tightly integrated with AWS servers and datacenters, and is not sold outside Amazon."
  - read up on the hardware: https://en.wikipedia.org/wiki/AWS_Graviton
  - products such as AWS Nitro, Enhanced Network Adapter (ENA), and Elastic Fabric Adapter (EFA), in compute with AWS Graviton and F1 EC2 Instances, in machine learning with AWS Neuron, Inferentia and Trainium ML Accelerators, and in storage with scalable NVMe.
  - Knowledge of code generation, compute graph optimization, resource scheduling
  - Data structure and algorithms
  - Compiler - Optimizing compilers (internals of LLVM, clang, etc)
  - Machine Learning - Experience with XLA, TVM, MLIR, LLVM
  - Deep learning models and algorithms
  - Tensorflow, PyTorch, or MxNET frameworks 
  - code generation, compute graph optimization, resource scheduling
  - optimization mathematics such as linear programming and nonlinear optimization.
  - Neuron SDK***
  - partners like PyTorch, Epic Games, Snap, AirBnB, Autodesk, Amazon Alexa, Amazon Rekognition
  - AWS Neuron Team
  - AWS Inferentia and Trainium
  - AWS ML services teams
- target Google TPUs
  - High Performance Computing (HPC)
  - GPU architecture & Nvidia software stack NCCL, CUDA
  - machine learning accelerators
  - large machine learning models
  - GCP clients large model development journey massive scale
  - large model research and developers
  - Develop horizontal scaling compiler tools and infra necessary for large-scale training reliability and sustainable compiler development velocity.
  - Collaborate with open source contributors to the horizontal scaling capabilities of the compiler on GPU.
  - performance, systems data analysis, visualization tools, or debugging. 
































