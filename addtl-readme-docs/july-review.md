# july portfolio review
###### created: tues july 9
###### updated: ^

## existing notes but reorganized:

- hardware study first (new plan to study hardware --> software at this stage)
  - nvidia latest gpu
  - google tpu
  - aws gravitron
- ISA study
  - simt
  - OpenCL
  - OpenGL
  - what each chip uses
  - what each compiler can make as a virtual ISA (?)
- compiler study
  - llvm
  - mlir
  - nvcc/ptx
  - xla/openxla
  - tvm
  - triton compiler (openai)
- machine learning/deep learning algo study
  - dl network graphs
  - transformers 
- ml frameworks
  - pytorch 
  - tensorflow
  - jax
  - modular?
- common issues avoided & written into docs:
  - race conditions
  - memory bottlenecks with matmul
  - matmul issues in general #todo
  - parallel vs concurrent #todo
  - deadlocks
  - thread starvation
  - daemon conflicts
  - double free error, etc. (#todo more cpp issues)
- frontend:
  - writeups with 4-part structure developed
  - hand-drawn diagrams for each section
  - progression from project 1 through 3
  - aesthetic website design
  - react components to demo my frontend background
  - etc.

## by project:

#### project 1
- llvm ir
- cpp
- cmake
- ssa isa (simt?)
- one basic block
- fundamental aspects of cpp standard lib

#### project 2
- modular (is a ml framework or cloud distro at scale?)
- mojo (python)
- mlir
- mnist algo? or transformer algo?
- some more fundamentals of a standard lib but this time mojo

#### project 3
- nvidia gpus
- ^corresponding ISA study
- cuda kernel
- cpp (but look into pycuda)
- one of the ~6 compilers they reference
- multiple basic blocks in IR
- cuda math apis
- transformer algo? or dl network graph algo? feature engineering, regression & modeling too.
- interesting things from the cpp standard library


## review summary tues july 9
- i do think the tech stack goal is robust
- i could instead research more into other tech stacks but that seems to be balanced across the tech ecosystem (also from volunteer open-source to corporate open-source)
- one change is now that ive done the project 1 code, next i want to study hardware, then ISA when beginning project 2
- i would like to finish up the website basics & project 1 page at least an mvp
- next: plan out full timeline & then plan out this week