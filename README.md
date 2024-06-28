# portfolio

## project one: 
- (completed) [project one config notes](./addtl-readme-docs/project-one-config-notes.md)
- (completed) [project one advanced llvm notes](./addtl-readme-docs/project-one-advanced-llvm-notes.md)
- (in progress) [project one summary notes](./addtl-readme-docs/project-one-summary-notes.md)
- (in progress) [project one frontend notes](./addtl-readme-docs/project-one-frontend-notes.md)

## project two: 
- (in progress) [project two plan notes](./addtl-readme-docs/project-two-plan-notes.md)

## project three:
- (in progress) [project three plan notes](./addtl-readme-docs/project-three-plan-notes.md)


## overall strategy:

- meta-level
- high-level
- mid-level
- and corresponding low-level code
- use parallel visual and verbal problem solving for present this portfolio

# meta-level:

## meta-level frontend ui/ux and content

#### ui/ux 

- TL;DRs & minimalistic text content always
- original lucidchart diagrams (w simple titles) for:
  - (*** mandatory) explanation of this github repo directory layout/structures and key code functionality
  - LLVM/MLIR/Modular IRs & infrastructure/tooling & build/compile orders
  - this portfolio's color palette and design elements?
  - generic hardware-to-software stack
  - math and physics topics i've studied
  - how ontologic classification of reality, cognitive science, & linguistics correspond to OOP (& maybe show context of branches of philosophy)
  - elements of prog langs i know (C++, Java, JavaScript, Python, Rust, Ruby, HTML, CSS)
  - history of significant LLM & ML paradigms' research papers, APIs, etc.
  - history of ISA breakthroughs and technology, i.e. SIMD to SIMT
  - chart of metatheory, metalinguistics, metaontology, metaphilosophy, mental models, metaprogrammaing, metaML, metalogic etc.
- Excel charts, Gantt charts, Sankey diagram, classification custom double axis charts, etc. for tracking this portfolio's progress/timeline/roadmap
- aesthetic considerations with which to create Figma UI dark mode designs for this portfolio site (including Jupyter notebook & terminal aesthetics) (also including resume, twitter, github, and linkedin)
  - truly modern flat Google open-source material design paradigm (industry-standard accessible contrasts, font sizes, etc.)
  - metamodernism (current haute/rare aesthetic paradigm)
  - please reference the specific examples on https://cari.institute/aesthetics
    - cassette futurism (for terminal & buttons)
    - corporate hippie (reminds me of corporate flat in general)
    - cyberbougie (color palette)
    - eco-beige (consider this palette insteaq of cyberbougie palette because is last/current-gen pop culture aesthetic PLUS*** it invokes DAYTIME)
    - factory pomo (for lang icons/logos section)
    - genericana (reminds me of certain corporate elements)
    - gen x soft club (because of minimalism and palette)
    - laser grid (because it reminds me of current AI-generated art paradigm themes)
    - nu-brutalism (flat design, ability to include many cards at once, and vintage yet post-modern fonts)
    - pixelscape (fun aesthetic for programming & reminds me of the semiconductor chip design metaphor/visualizations)
    - pastel southwestern (for even softer palette than cyberbougie but similar)
    - pastel fantasy (also reminds me of current AI art paradigm)
    - superflat pop (because it was very ahead of its time in terms of flat, palette, themes, and art paradigm)
    - synthwave (essentially dark cyberbougie palette but more neon; also like laser grid)
    - vaporwave (like synthwave properties plus yellow in palette and additionally evokes Y2K and frutiger aero)
    - vector minimalism (evokes last-gen corporate design)
    - Y2K aesthetic (because good to know when cyberbougie-esque palette started and how it evolved; also interesting themes)
    - zen-x (reminds me of eco-beige yet much more calm and feels like how i feel when i can get in deep flow with code/work)

#### personal bio plan:

- icons for all langs i know
- quick bio
- photo
- links:
  - programming-based twitter
  - linkedin
  - my github home page
 



## meta-level backend

- TL;DRs & minimalistic text content always
- at least one portfolio page with a Jupyter notebook:
  - use the classic MNIST dataset?
  - demo one of current promising ML theories?
  - demo integration of many current promising ML theories
  - ability to change Jupyter code to see diff output (***to prove functionality)
- buttons at bottom of a Jupyter notework to:
  - compile with LLVM
  - compile with MLIR
  - compile with Mojo/Modular
- outputs of IR & description
- outputs of ISA & description
- stored in GCP/Azure?
- links to check results:
  - block of text/code to copy into GPT 3.5 and Gemini, etc.
  - links to LLVM/MLIR/Modular GH repos but with my process (bash commands, configs, etc.)






# high-level plans (frontend and backend)


## high-level frontend tech stack & ui/ux

#### tech stack

- components/styling:
  - see if i can use old portfolio's HTML & CSS via Bootstrap & Sass
  - otherwise, use Google's Material Design components will be enough for relatively static site
  - if i need dynamic components, then React if I can re-configure the build toolchain
- build toolchain: yarn, parcel & GitHub Pages
  - if parcel is broken, use webpack built into the standard react-create-app as long as it's compatible with GitHub Pages

note:
- ^these choices don't have to be ideal because i'm not looking for frontend jobs anymore. they just have to work.
- the page should be mostly static with minimal dynamic elements (no embedded jupyter notebook like i had researched)

#### ui/ux

- easily be able to copy code sections from my site and link to a free online Jupyter notebook to test code
- one page for each project I'm demoing (basically a graphics-based minimal-text code walkthrough but also for non-technical people)
  - one LLVM project (c++)
  - one Modular/MLIR project 
  - one CUDA project
- great non-techincal report for portfolio website page with:
   - excel graphs/charts w lucidchart aesthetic, etc.
   - architecture map
   - copyable code
   - link to Jupyter-notebook-type sites for proof


## high-level backend plan:

#### project progression ideas: (today is Mar 14, 2024)
  
1. llvm project (SIMT?)
   - c++
   - extremely basic but good representation of the c++ standard library
     - study quick map of c++ std for:
       - I/O file read/write
       - class/object
       - list
       - data types to demo the stack & heap
       - recursive loop if possible
       - basic search algo DFS/BFS recursion and find the exit condition
     - should correspond to basic LLVM IR
     - still study std LLVM IR though.
   - **_apr 4 update_**: finished it with one basic block
3. modular project (SIMT?)
   - update: 
   - mojo(python)/MLIR IR
   - MNIST dataset unless i can think of something better
     - can i apply current models to this?
     - which is the best current singular model to use for this?
   - try to make the project run in the Modular browser env for proving the project
4. cuda project
   - nvcc/ptx (parallel thread execution) (SIMT?)
   - **_apr 4 update_**: demo c++ std lib & mult basic blocks here instead of project one.
   - choose: c/c++ or python/PyCUDA
     - do i want to demonstrate just my IR experience or possibly also ML experience?
   - can i do an integration of all best models thus far?
   - search kaggle for an already-cleaned dataset and then do
     - basic fundamental principles
     - feature engineering
     - regression
     - modeling
   
#### notes:
- diff repo for each one
- where does SIMT apply?

- plan complexity levels and skills demoed for each
- plan order in which i do them
- plan how much time dedicated to each and deadlines
- 3 projects total because combine Modular/MLIR

#### time left:

2.5 months till first round of applications:
- last 2 weeks mar
- april
- may

then 1.5 more months till second round of applications:
- june
- first 2 weeks july 

#### project timelines

- LLVM project 
  - ideal:
    - total time: 4 weeks
    - finished by: April 30
    - (_**code done apr 4**_)
  - deadline: May 31

- Modular project 
  - ideal:
    - total time: 6 weeks
    - finished by: May 31
  - deadline: May 31 or July 15 if i'm really struggling

- CUDA project
  - ideal:
    - total time: 6 weeks
    - finished by: July 15
  - deadline: July 15 (to begin final applications Aug 1)
 





# mid-level plans

## mid-level frontend plan

consider all these at same time:
- build toolchain
- v0.dev can create the UI & UX components i want
- nice UI design (diff design for each project?)


## mid-level backend plan 

todo list:
1. simplify high-level backend plan for project one (made progress Fri Mar 15)
2. start going on low-level backend plan
3. work on backend M-F
4. take a look at frontend on the weekends

1. llvm project
   - c++ [c++ standard library](https://en.cppreference.com/w/cpp/header)
   - extremely basic but good representation of the c++ standard library
     - study quick map of c++ std for:
       - I/O file read/write
       - class/object
       - list
       - data types to demo the stack & heap
       - recursive loop if possible
       - basic search algo DFS/BFS recursion and find the exit condition
     - should correspond to basic LLVM IR
       - C++ LLVM metaphor concepts:
         - abstraction/standardization - abstract away low-level details for portable code; high-level abstraction of SEMANTICS
         - generics/templates which are data structures and algos for many data ttypes
         - modularity/composition (of containers, algos, I/O) to create complexity (IR: basic blocks, instructions, functions)
         - optimizations/transformation  
     - still study std LLVM IR though. :::
       - basic blocks (single entry point & single exit point (except for branches, loops, etc.))
       - instructions (arith ops, memory accesses, function calls and control flow inst) mnemonic codes - SSA form (Static Single Assignment)
       - functions (name and signature (return type and params) and body) (`define`)
       - values: constants, vars, and results ::: are types
       - data types: int, float, vect, pointers, structures, arrays and user-defined types
       - global vars accessed from any function (starts with `@`)

      
notes:
  - CUDA can use LLVM to create a SIMT-execution-model-style ISA ("instructions for managing threads, accessing memory, performing arithmetic and logical operations, and controlling execution flow.")
  - how do basic blocks handle control flow instructions? (branches between basic blocks have explicit instructions)
  - SSA: "SSA is a form of intermediate representation used in compiler design, particularly in optimizing compilers. In SSA form, each variable is assigned exactly once, and each use of the variable refers to that specific definition. This property simplifies data-flow analysis and enables certain optimizations such as common subexpression elimination and dead code elimination."
  - ISA "encompasses the set of instructions that a processor architecture supports, along with their encoding, semantics, and behavior"


# low-level plans

## low-level frontend plan 

- try out v0.dev next
- actually try out vercel frontend components tools

## low-level backend plan 

1. llvm project 
  - c++ content: primitive var cast to object var in a list in an object sounds ideal (no read/write needed cause I'm not a networking specialist)
  - c++ algo options:
    - (no) RNN recursive neural networks - recursive algo
    - (no) GBMs gradient boosting machines - tree-based algos (also decision trees, random forest, 
    - (no) GNNs and GCNs graph neural networks and graph convoluational networks - graph algos
    - transformer: (graph algo)
      - core component: self-attention mechanism
        - attention scores via dependencies & relationships
        - then compute weighted sums of the input embeddings, generating context-aware representations for each word
      - multiple layers processed in parallel (parallelism / concurrency / multithreading / SIMT, PTX, etc.)
      - essentially filter algos ?
      - long-range dependencies which RNNs couldnt
      - in NLP, token in sequence are nodes in graph, attention scores and edge weights btw all pairs
      - can then capture hierarchical structures efficiently
  - llvm ir: use 3 basic blocks to show how entry and exit would work in that case
    - DFS and BFS both can search graphs, doesnt matter which one, whatever works w the program
    - non-technical semantics: knowledge graph of relationship strength between objects then make a hierarchy
    - no generics is fine
    - can discuss modularity and composition (see above section for details)
    - optimizations: on purpose, use the type of loop that can be optimized 
    - transformation: ^then show how llvm ir transforms the loop
    - might need like 4 basic blocks actually for 6 relationships and one four-word sentence (then use code for input and output with slight modifications)
    - will include arith ops for wts, memory access of course (registers, cache, RAM ideally but maybe save that for projects 2 or 3)
    - will include values (vars and results)
    - make sure to use pointer but its fine w/o array and struct actually for this one
    - no global var is fine i think till later (#todo for project 2/3)
    - the function calls will be the node creations and the search
    - the control flow is the loop
    - make sure to map to SSA and talk about importance of explicit single assignments in terms of basic blocks and the looping
       
next:
- compile a c++ llvm cmake config asap or rapidly pivot to compiling it somehow in browser, etc.
- new repo and write out the algo in c++
- make the config
- examine the IR with the tooling
- get it on the frontend asap
- 3/28 note: i've been noticing SDK needs in project 1 notes file and also CUDA SDKs too:
  - [NVIDIA SDK glossary](https://developer.nvidia.com/sdk-glossary?ncid=em-even-320346-vt53&AY0sih1l1UctMMIQTiqyC6aG0vIU7hk9NTqbq_hdl8IdJheje-8uln1-X4z-2ibgdTCXrtCR6nme4nSZM2oaFQ&mkt_tok=MTU2LU9GTi03NDIAAAGSH2kFQN7hB2EUkz0R4yCQOaSKpCpT72cvdEC-pNi79okOwy6M5E_BiaeCznSZvrfNlYg6rNnfmrKodZKUzjQS70M5767F97VL3kGAx5nvuqSq4WGu63g)
  - additional NVIDIA resource: [Deep Learning Institute](https://www.nvidia.com/en-us/training/?ncid=em-even-886387-vt53&AY0sih1l1UctMMIQTiqyC6aG0vIU7hk9NTqbq_hdl8IdJheje-8uln1-X4z-2ibgdTCXrtCR6nme4nSZM2oaFQ&mkt_tok=MTU2LU9GTi03NDIAAAGSH2kFQCObZqwKtC-J_STITgfFWZDSCosu8VYBbsKCN8FD3qjzelrdm_VJtF9egQhWN6J-rkJvV8cXrMGaUjtCY9T7ytL86J6CS1YzTAK761Eu1Jt2coo])
  - `CMAKE_OSX_SYSROOT              /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk`
  -  If "LLVM" provides a separate development package or SDK, be sure it has been installed.
  -  Set the macOS system root `set(CMAKE_OSX_SYSROOT /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk)`

additional portfolio notes:
- remember when i had the goal to build a compiler and work that into these projects
- study leetcode arrays, for example cityscape problem; model data structures and algos concepts
- use parallel visual and verbal problem solving
- research ISO/ISEE/x86, etc. standards, protocols, etc. to see if/how they apply to these projects (esp new standards and CUDA Math API standards, etc.) (#todo for projects 2/3)

#### apr 4, 2024 next steps:
- use this doc to do project one code analysis
- archive the rest of project one high-med-low level plans out of this readme
- create frontend asap to demo project one

#### progress apr 5, 2024:
- new project one summary readme with high/mid/low levels structure

#### progress apr 21, 2024:
- this week is gonna be a chill portfolio week because of the school term and i'm ahead of schedule on my portfolio goals
- a bunch of my green checks from 2024 disappeared because i took an old work email off my account and some of my commits were via that email but i can update the logs to get those back and plan to soon

#### progress may 1, 2024:
- some long term extra ideas:
  - would be cool to compare low-level functionality and multithreading/concurrency in c++, c, zig, go, rust, mojo, pytorch?, sql, any DSLs from the APIs i use
  - look up nvidia APIs, etc.
  - also implement a graph algo in each
  - compare common/rare brugs
  - compare standard library overviews
  - compare how they handle i/o networking and IEEE protocols, Web APIs etc
  - compare their ideals & programming principles in general
- leetcode: c++, python, java, javascript. trees (ast), graphs.
- open-source contribution: llvm, mlir, mojo, pytorch, tensorflow (understand why lex, etc., said pytorch is a language)
- extra free online courses:
  - edx stanford compilers
  - coursera stanford machine learning 3x courses (andrew ng courses)
  - coursera princeton computer architecture
  - some embedded systems/digital circuits
  - advanced compilers if i could find one  

#### progress may 5, 2024:
- may plan: 25 minutes work on this per day
- june plan: 55 minutes work on this per day
- july 1: apply to first round of jobs

next steps:
- plan next two months in detail week by week
- get done what i need to get done this week


#### progress may 6, 2024

detailed may-june github/website plan:
(format: month.week, e.g. first week of may is 5.1)

###### meta-level (updated end of week 5.2)

5.1: site backend - get local build working (done)
5.2: site backend - get remote build working on github.io (done)
5.3: site frontend - mvp: bio (home) & p1 pages (remember to use canva)
5.4: site frontend - draft tw p1 page
6.1: project two backend - code
6.2: project two backend - code
6.3: site frontend - project two
6.4: site frontend - bio page with new photo

###### high-level

tbd (more detailed week by week - split into 7 days and long seshs on weekends)

###### mid-level

detailed 5.1 (this week) plan:
mon: today. planning
tues: create proper dir structure in existing repo (done)
wed: 
thurs: if i get it, review react
fri: if i get it, review shadcn & tailwind
sat: website with just a React/shadcn/tailwind page live on ashlink11.github.io (nothing on it yet)

###### low-level (use this for literally doing the work (.exe-level))

detailed 5.1: (for the rest of the week) 
- fri: (finish portfolio website build)
  - clone ashlink11 repo to laptop 
  - checkout new branch
  - `--create-next-app` with flags
    - https://nextjs.org/learn-pages-router/basics/create-nextjs-app/setup
    - https://nextjs.org/docs/pages/api-reference/create-next-app
    - https://v0.dev/ has to be compatible with react, shad-cn, tailwind so search their docs 
  - push back to gh
  - commit PR to main
  - look at site and look at gh actions hosted terminal results
  - if doesnt work, might have to duplicate repo w new name, go back a commit on main, and git pull so i dont lose commits
  - then i can try diff ways and repeat till i get it
- sat:
  - debug yesterdays if i didnt get the build done
  - or plan next week (5.2)

detailed 5.2: (25m/day because all of may is 25m a day goal because there's other foundation like 530am wakeups, yoga, lifting, and 4 classes this 2 month term which is may-june; also i'm ahead of timeline enough) 
- sun: day off
- mon: (today) planning week
- tues: attempt site build on gh hosting (yml file manual rewrite attempt one - see what chatgpt and gemini say bc i havent tried them yet)
- wed: either continue tues work or study gh configs more or see where i'm at
- thurs: tbd
- fri: tbd
- sat: tbd

## notes fri may 17 for project three (updated tues may 21)

new fireship bend video https://www.youtube.com/watch?v=HCOQmKTFzYY

- cuda blocks locks mutexes regexes
  - 24 cpu cores
  - 16k gpu cores
- python single threaded
  - clock cycle around 4GHz
  - 1 inst / cycle
  - 4b inst/sec four gips
  - python has threading.Thread(), huge complexity though
- parallelism gotchas:
  - race conditions
  - deadlocks
  - thread starvations
  - daemon conflicts
- maybe cpu doesnt have enough juice
  - diagram with core, l1 cache, control)x4, l2 cache x2, l3 cache, dram, etc.
  - thousands of cuda cores
  - cpp though.
- python converted to bytecode and run on PVM
- bend:
  - elements of computation structured into a graph (network)
  - interaction combinators
  - when two nodes run into each other, follow simple set of rules that rewrites computation to run in parallel until all merged then runs and returns
  - yves lafont paper 1990s interaction combinators
  - HVM2 higher order VM on github
    - not meant to be used directly
    - bend interfaces with it
  - bend implemented in rust
  - syntax similar to python
  - uses rust interpreter single threaded
  - bend has no loops, instead has fold
    - notes not from this video:
      - fold == reduce
      - catamorphic structure
      - makes a list of lists into a list
      - there's double fold, fold, and bend?
    - search and replace for data types
    - consume recursive data types in parallel like a list or a tree
    - first construct recursive data type called bend
    - bend is opp of fold
  - perf testing
    - ben run app.bend // 1 hour
    - bend run-c app.bend // uses all 24 threads on cpu, 30 seconds
    - bend run-cu app.bend // 1.5 seconds, 16,384 CUDA cores, nvidia rtx 4090

## progress sun may 19, 2024

todo:
- update url to remove the last `/ashlink11`

week 5.3 plan:
- goal: make draft one of website frontend and push it live
  - design ui including canva
    - finalize project page layout
    - create draft one home page layout
    - plan all canva diagrams by choosing canva elements, otherwise i will need an alternative to canva
  - use v0.dev or find an alternative or create from scratch with react, perhaps using figma, although that might take a lot of time
- sun: plan week
- mon: finalize project page layout
- tues: create draft one home page layout
- wed: plan all canva diagrams
- fri: use v0.dev & push live
- sat: use v0.dev & push live

## tues june 18: next: redo timeline & make monthly, weekly plans for projects

## mon june 24
- okay ive been feeling meh on making the website. its not difficult ive just not had a good routine.
- i think next i should study the code for fun

## tues june 25
- defining portfolio goals:
  - pursue projects to be able to study lots of hardware-adjacent software topics including basic knowledge of hardware and keep my full-stack knowledge fresh
  - with p3, demonstrate useful working code
- so, right now, working on the portfolio site is useful to keep my frontend skills fresh
- next p2 can just be fun studying really and getting basic code working
- and thatll save me time to make p3 more difficult with writing more code

#### wed june 26: feeling very tired. gotta start making this part of my morning routine again cause that worked well and do 25m m-f, 1-3 hours on saturdays and day off on sundays
#### thurs june 27: i've been working on my schedule and when i get it worked out, i'll get around to the portfolio schedule





















