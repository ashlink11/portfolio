# portfolio

## tech plan:

- high-level models and corresponding low-level code

####: high-level:

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

####: low-level:

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



## personal bio plan:

- icons for all langs i know
- quick bio
- photo
- links:
  - programming-based twitter
  - linkedin
  - my github home page



## timeline: (interview process is about 3-4 months for big tech)
(created: Mar 9, 2024)
(last updated: """ )

- apply to ~6 semiconductor design (compiler) engineer jobs by june 1 (3 months from now)
- apply to ~9 more semiconductor design (compiler) engineer jobs by aug 1 (5 months from now)




## tech stack (frontend)

- components/styling:
  - see if i can use old portfolio's HTML & CSS via Bootstrap & Sass
  - otherwise, use Google's Material Design components will be enough for relatively static site
  - if i need dynamic components, then React if I can re-configure the build toolchain
- build toolchain: yarn, parcel & GitHub Pages
  - if parcel is broken, use webpack built into the standard react-create-app as long as it's compatible with GitHub Pages

note:
- ^these choices don't have to be ideal because i'm not looking for frontend jobs anymore. they just have to work.

- embedded jupyter notebook package options:
  - `JupyterLite` by JuptyerLab. ships with Python kernel powered by Pyodide and IPython. its REPL runs entirely in the browser. posted in Mar 2022: (https://blog.jupyter.org/jupyter-everywhere-f8151c2cc6e8) (been building it for at least 3 years)
  - `nbconvert` is a Python package that allows you to convert Jupyter notebooks to other formats, such as HTML, PDF, and Markdown. You can use nbconvert to embed a Jupyter notebook in a static website or blog post.
  - `nteract` is a Python package that allows you to create interactive web applications from Jupyter notebooks. You can use nteract to embed a Jupyter notebook in a web application, such as a dashboard or a data visualization tool.
  - `papermill` is a Python package that allows you to execute Jupyter notebooks as Python scripts. You can use papermill to embed a 




























