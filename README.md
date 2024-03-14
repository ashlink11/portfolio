# portfolio

## overall strategy:

- meta-level
- high-level
- mid-level
- and corresponding low-level code



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
3. modular project (SIMT?)
   - mojo(python)/MLIR IR
   - MNIST dataset unless i can think of something better
     - can i apply current models to this?
     - which is the best current singular model to use for this?
   - try to make the project run in the Modular browser env for proving the project
4. cuda project
   - nvcc/ptx (parallel thread execution) (SIMT?)
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


## mid-level backend plan (today is mar 15, 2024)

todo next:
1. simplify high-level backend plan
2. start going on low-level backend plan
3. work on backend M-F
4. take a look at frontend on the weekends




# low-level plans

## low-level frontend plan 

## low-level backend plan 





















