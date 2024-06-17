# project one frontend notes
#### date created: april 5, 2024
#### tags: #todo #key

# high-level

notes:
- try out vercel frontend components tools
  - then: what's my tech stack? 
- UI layout sketches while considering UX
  - i think different phases of each project should be diff colors though.
  - maybe each project could vary by:
    - color? no.
    - hue? no but maybe for a combined plan B
    - font? no but maybe plan C
    - depth/flat/shadows? no but maybe for a combined plan B
- additional UI elements:
  - static elements:
    - gantt
    - excel
    - lucidchart
    - screenshots of different parts of the program? doubt it.
  - dynamic elements:
    - buttons
      - to change colors for teaching effect
      - code carousel
    - embedded jupyter notebook
- design notes:
  - i like the aptos font #key
   
next steps: (april 5, 2024)
- keep working on this^
- start with [this video](https://www.youtube.com/watch?v=br2d_ha7alw)
  - from March 25, 2024 by VP of Product
  - Bringing React Components to AI
  - Learn how the Vercel AI SDK 3.0 helps you move beyond plaintext and markdown chatbots to give LLMs rich, component-based interfaces.
- https://v0.dev/ is vercel
- last fall [v0 intro article](https://vercel.com/blog/announcing-v0-generative-ui)
- [main vercel site for frontends](https://vercel.com/ai)


# mid-level

### progress april 6, 2024:
- v0 can accept either images or prompt
- so next step is to design the UI on paper
  - consider:
    - colors
    - font & font size
    - mobile-first
    - laptop display
    - embedded jupyter notebook
    - page speed
    - whichever PWA ideals i met with this site
  - pages/elements:
    - home (traditional portfolio page)
      - name
      - logos of all technologies i know
      - photo
      - bio (how many sections? 1?) what's the overlap btw this, resume, and linkedin, etc.?
        - selected hobbies? add the 'why'/mission/biz vision/career goals type stuff
    - project one
      - most minimal 
    - project two
      - mid minimal
    - project three
      - not that minimal
    - where does the overall projects evolution summary go?
    - visuals:
      - dynamic and static elements
      - which minimal maps/charts? and how to make them minimal?
        - options other than lucidchart for SWA diagrams
          - [top 8 SWA diagramming tools medium article](https://icepanel.medium.com/top-8-diagramming-tools-for-software-architecture-2fc61d095b93): "Software architecture tools can be categorized into three groups, modelling tools, diagrams as code and diagramming tools."
            - Excalidraw (most aesthetic)
            - Gliffy for UML & ERD diagrams - use idea but not aesthetic design
            - Cloudskew - idea of using tech logos for a tech stack diagram, etc.
            - Trello for Kanban to demo Agile/Scrum
              - high-level: portfolio project
              - mid-level: releases for corresponding backend/frontend milestones
                - github PRs 
              - low-level: sprints (good sprint lengths - 2 weeks)
              - agile charter
              - PBIs
              - scrum events
                - track daily scrums vs github commit messages
                - how much of all this is sidebar topics? #key
              - Miro instead of Excalidram and Gliffy
              - essentially Miro vs Lucidchart
          - high/mid/low levels and can i combine them somehow?
          - include my github contributions annual charts somehow
    - any more pages?
      - a super minimal contact page last unless that's bad UX
      - an almost purely map/chart page?
      - way to demo 'database'/data for the site because this does demo fundamental backend dev/devops knowledge
        - relate this to cache/registers/RAM/SSD memory (remember XOR has memory #todo)
        - relate this to cloud storage and datacenter memory and GCP/Azure/AWS/Cloudflare edge, etc. 
      - demo frontend knowledge including PWA & tech stacks & react 'standard library', etc.
      - an evo/map of ML page? demo what AI i used #key and how it relates to MLIR/CUDA hardware/software concepts #key
      - a page showing the evolution of my jobs and 2 open-source projects?
        - link to best w3f code/evaluations 
      - a page showing how i built this portfolio site? (or on github repo readme?)
      - a page/dropdown menu for a demo of any other key technologies i know?
        - something fun?
        - something interactive?
      - extremely short and/or longer embedded youtube videos demoing projects/learnings
        - this could demo all the different meta-map ideas like math, linguistics, philosophy, business, etc. to show both generalization and specialization and evolution of last decade of programming 
      - person project concept page with LLM/linguistics/identity language personal development 
    - think about what content will be on & links to:
      - linkedin (posts?)
      - trello
      - resume ((but might be different for each/some applications))
      - ((don't link cover letters of course))
      - put new email on there (Ashley Grevelink - ashley.grevelink@gmail.com)
      - twitter
      - youtube (& tiktok for shorts) as long as theyre 100% career-focused & minimal yet dont take away from career goals. e.g. make a 'final' video that summarizes all the rest in a playlist that's 'completed' (would need adobe premiere pro)
      - medium (posts?)
      - github & repo(s) READMEs/selected code (good for project code)


# low-level

### progress april 6, 2024:

 - agile meta
 - make initial trello/agile notes during these:
   - mid-level frontend & backend sketches/maps
   - write absolute minimal verbal if applicable to realize if core concepts translate visual/verbal
   - repeat visual/verbal for high-level
   - repeat visual/verbal for low-level
 - then agile top-down all the way down
   - agile charter
   - project planning (product owner role)
     - non-technical stakeholders as customers #key
     - KPIs & metric tracking #key
   - release planning
   - sprint planning
     - user stories to PBIs #key (which are multiple roles?)
     - planning poker
     - velocity estimation & burn-up chart
     - customer success role too
   - trello 
   - daily scrum
   - look ahead to:
     - sprint review
     - sprint retro
       - burn-down chart and measure velocity (#key to resume/cover letter quantifiables) with words & lines of codee and hours and deep flows and timeboxed pomos on routine 
     - backlog refinement
       - tester role 
     - next sprint
 - choose core concepts from mid-level
   - do this by:
     - initial map based on mid-level notes
       - (blue) identify fundamental concepts highest in the hierarchy
       - (purple) identify essential concepts to demo for parallel generalization/specialization
       - identify which concepts should be visual
       - identiy which concepts should 
     - move up one level of abstraction
     - move down one level of abstraction
     - execute (the sprint)
     - repeat
 - sketch out to realize if core concepts translate visually
 - double check verbal again and compare to visual 

### progress mon apr 8:
- paper notes on levels of abstraction diagrams and maps
- gathered the best ontological classifications ive collected/made throughout the years on 2 pieces of paper
- e.g.: (this is not the maps/diagrams of them)
  - philosophy:
    - thesis --> antithesis --> thesis (hegelian dialectic)
    - what is there, what can you know, what should we do, what's a beautiful life
  - math:
    - pure --> applied
    - discrete math:
      - formal logic:
        - premises --> argument --> proof (as a formal means to transfer/prove truth)
        - truth: axioms --> rules --> theorems --> laws
    - non-discrete/informal 'truth': statistics and empiricism (science)
  - linguistics:
    - it's all syntax and semantics
    - it's all subject verb object (and sometimes adjective, etc.)
  - computing:
    - it's all languages and systems
    - it's all objects and their properties and relationships (functions)
    - it's all blueprints and copies
    - it's all doing (operating/execution) and keeping track of the details (memory & state)
    - it's all versioning --> ...
  - modeling/systems: 
    - low-level
    - mid-level
    - high-level
    - meta-level 
    - (new emergent properties level of abstraction)
  - did a lot of writing/story/character progression/maps/diagrams too because it helps me plan the keywords/themes for a quick bio as well as the minimal text for visuals for the three projects.
  - that's all enough to help me move forward with the portfolio content design, which will help me create the project one analysis/page design, so then i can make the frontend asap that ui in mind.

- ^i should clean this all up later 

### next steps:
- draw some quick sketches of the four pages of the portfolio on paper with general content boxe
- redraw the project one page high-level
- then mid-level
- then low-level
- then use v0.dev starter tools
- then make a new vercel repo
  - find a vercel template that i can use with GitHub Pages
  - otherwise i'll have to hack together a frontend build toolchain to get it hosted
- once the portfolio website is up then:
  - set up the dev env a bit better with hot reloading
  - try super fast version with the v0.dev components
  - go back to the project one code and do the write up and diagrams
  - etc., repeat, iterate :) 

# progress tues apr 9

portfolio content plan for text/visual:
- for each project:
  - quick overview and into the project
  - biggest challenge
  - how i overcame it
  - key lesson about system fundamental(s) learned
- for bio:
  - no bio really, just the logos of tech i know categorized into their parts of the stack like my old portfolio website 

- so for project one: (rough notes)
  - quick overview and into the project
    - technical way to say it: 
      - llvm is compiler/tools to transform programming langs --> ISAs.
      - main cool thing is LLVM IR (which is essentially the vm in llvm. the asm.)
      - so i wanted to clone their open source github repository.
      - then create a small project & run llvm on my machine.
    - non-technical translation: (draft 1)
      - LLVM is a historically important collection of open-source utility code for over two-decades that's used by Apple, Windows, and Linux.
      - the acronym for LLVM became confusing so they dropped it more than a decade ago, but essentially LLVM is a compiler.
      - a compiler is software that translates programming languages down to machine code.
      - in other words, it's part of the technology stack that translates software to hardware.
      - that means Apple, Windows, and Linux use LLVM to help translate software programs into zeroes and ones. 
      - since LLVM is open source, i downloaded it from their public code library so i could try to write and run simple projects on my machine.
  - biggest challenge
    - technical lang:
      - super complex (3 months) to understand the llvm source code and cmake config and didnt know if the c++ was correct either.
    - non-technical translation:
      - over the decades, LLVM has become a really large code base, so it actually took me over three months of working on this in my free time to get it running.  
  - how i overcame it
    - technical lang:
      - i had to learn:
        - my file system way more including /opt, $PATH, bash in general, and where things i installed with bash go, and all the different versions of the lang compilers, etc.
        - overall llvm infra high-level
        - study the llvm source code, so the dir structure and some header files in llvm/lib specifically 
    - non-technical translation:
  - key lesson about system fundamental(s) learned

what to do with extra notes, if anything:
- repo READMEs
- possible code comments too

proofreading:
- cross-check the three projects with these: (etc.)
  - https://en.wikipedia.org/wiki/LLVM
    - ^interesting note: i learned CUDA has an LLVM frontend, which i didnt know was possible because i didnt think CUDA was a language #todo 
  - https://en.wikipedia.org/wiki/MLIR_(software)
  - https://en.wikipedia.org/wiki/CUDA
  - fireship LLVM video
  - fireship c++ video
  - etc.?

interview prep:
- review the project specifics so i have examples of $PATH, /opt, /llvm/lib, a header file, bash commands i needed, etc.

# progress wed apr 10
- for projects two/three get into pointers & other c++ fundamentals #todo #key
- add in the challenge section that i was just trying to get the .exe so i tried the cmake desktop GUI app too but \bin was empty both with that and cmake . in the terminal #key . needed to get something at atomic as possible running as a first step so thats what p1 turned into bc llvm is outdated anyway with lattner working on MLIR/mojo/CUDA/SIMT now
- for how i overcame it: used official docs of llvm and cmake bc running llvm is too commplicated and individual and ever-changing that there cannot be widely-accurate tutorials on the web
- so the cmake and llvm docs gave some fundamentals
- but actually i used chat gpt 3.5 until it kept repeating itself and then gemini ended up helping me with the final cmake config. ai as a learning tool is an important skill for devs these days, especilly for boilerplate and learning to read code (but not write). the code i really want to know how to write is the mojo for mlir and the c++ for cuda. agile "the primary measure of progress is working code". ai doesnt give all the answers; you need the right questions and still need a huge understanding bc these systems are so complicated
- ^ simplify that obv
- p1 fundas learned:
  - 1 basic block
  - the main low-level focus: project source code, llvm libs/headers, and cmake config
  - 3 bash commands total. configure, build, run #todo what's the diff btw config and run? (object files than bitcode i think)
  - .exe is in bitcode
  - then 1 more command to see the LLVM IR output which was actually super unexpectedly simple, short, and easy to read
  - optimization and transformation of code is just for complex loops #todo for p2/p3 i wonder if its possible with concurrency?
  - so in summary, we had cpp, cmake, object files, bitcode then ll asm file formats
  - so we turn things from:
    - cpp objects - programmers create the objects conceptually with code
    - llvm ir objects which are target-independent ("virtual machine")
    - llvm assembly asm is architecture-dependent x86, ARM, PowerPC, etc.
    - llvm object file is _machine_-dependent i.e. specific binary for the ISA of the machine
- understand this more: #todo
  - llvm ir is the additional target-independet layer of abstraction that united the computing industry to x86 in the 2000s
  - "LLVM IR allows compilation of code for various architectures without rewriting the entire compiler for each target."
  - "LLVM IR didn't eliminate the need for target-specific backends, but it significantly reduced the effort required to support new architectures. Compilers could leverage existing LLVM infrastructure and optimizations, focusing on generating efficient machine code from LLVM IR for the new target ISA."
  - "Target-Specific Backends as LLVM Components: These backends are essentially compiler plugins that reside within the LLVM framework. They are written using LLVM APIs and leverage LLVM functionalities to translate LLVM IR into target-specific machine code."
- bring it back to the lexer/parser/ast level
- discuss the os/compiler level too

### next steps:
- understand the compiler frontend/backend and how llvm fits in and if my machine is using a target-specific backend or llvm completely to run the project or a bit of both?
- simplify the p1 fundas learned
- write draft 2 p1 text content
- then do draft 1 p1 visuals/maps/diagrams

#### future ideas:
- pretty soon make a [frontend color palette](https://m2.material.io/design/color/the-color-system.html#tools-for-picking-colors)
- would be interesting to make a checklist of mental models/heuristics for programming, systems design, and debugging, etc. like charlie munger 80 models #todo

# progress th apr 11: (p1 text content draft 3) (revised draft 2 in-place)

## quick overview & into the project

llvm is open-source software used for over two decades by Apple, Microsoft, and Linux for a major and crucial part of compiling software/code into hardware instructions.

llvm means "low-level virtual machine", but the foundation dropped this acronym more than a decade ago because it had become inaccurate/confusing. but at the end of this page i explain why it was originally so.

now llvm is generally thought of as a compiler and set of compiler tools especially associated with the c/c++ language family via the clang compiler.

i've been studying compilers for some years, so in january 2024, i cloned the llvm public open-source code library to my machine so i could to write and run llvm/c++ projects.


## biggest challenge

over the years, llvm has become a huge codebase due to factors such as algorithmic optimizations, cybersecurity, and maintaining compatibility, etc. (also tools for more of the stack)

but i did have experience running a similarly complex library of software on my machine a couple years ago, which had taken about two months of work.

this time, i had to rewrite, reconfigure, and study for three months (jan 1 - mar 31, 2024) before i was able to generate an executable binary that would run successfully on my machine.


## how i overcame it

i overcame that challenge by concurrently executing on the low-level and studying on the high-level when necessary.

most of the effort was retrying over and over to generate a build with C++, CMake, and LLVM where investigating/debuggin each error code was generally a step of progress. (sidenote: CMake is build/configuration software for projects.)

in between, i studied the high-level llvm infrastructure and its source code directory layout, the order of execution of llvm filetypes (`.cpp` --> `.o` --> `.bc` --> `.ll` --> `.native`), as well as any additional theoretical compiler principles such as lexing, parsing, and linking.

another huge low-level piece is that i had to study my machine's (macOS) file system (filesys) to understand how & where language and tools software were/are installed. i did this mainly by navigating the terminal from the root (`/`), using `bash` commands, and also using the CMake desktop GUI application for an alternate approach to configuration.

finally, i used the popular machine-learning tools ChatGPT 3.5 and Gemini for rapid feedback to increase productivity/velocity. because, like the Agile development philosophy emphasizes, "working code is the primary measure of progress". i had to get a minimal-viable project running so i could attempt using more advanced algorthms and compiler features for projects two and three.


## tl;dr-type conclusion

in the end, my program generated one basic block of LLVM Intermediate Representation (IR) bitcode, which was surprisingly simple and easy to read. this IR can then be translated into the assembly code (ASM) and instruction set architecture (ISA) of any compatible x86, ARM, PowerPC, etc. computer architecture which Apple, Microsoft and Linux use/run on. because the IR is a target-agnostic bitcode runtime layer, this yielded the original "virtual machine" in LLVM's "low-level virtual machine" acronym. 

for me, the keys to the low-level were focusing on: the project source code, the llvm libraries & headers, and of course, the cmake config file.

and my take on the keys to the high-level were the concepts of: compiler frontend vs. backend, compiler vs. programming language, and
compiler vs. operating system.


# progress fri apr 12

- notes:
  - `.a` files are used for external libraries during linking (#todo: file formats of CUDA math APIs)
  - watch fireship summary vids before projects two and three (#todo)

done:
- draft possible user interface formats for portfolio (see porfolio assets folder)

- next: 
  - draft possible component graph/charts/code snippets designs 
  - choose the core ones

# progress su apr 14:

- project one visuals ideas:
- viz 1 context and into project (draft 1 done)
  - #keywords: llvm cpp oss lib github c clang apple msft linux compiler compiler tools cloned it to my machine write run llvm cpp 
- viz 2 biggest challenge
  - #keywords:
    - 2 decades huge codebase
      - show files increasing in complexity as features added
        - more of the stack
        - algorithmic optimizations
        - cybersecurity
        - maintaining compatibility
      - ran rust polkadot runtime p2p blockchain as w3f technical grant evaluator switz-based job 2 years ago (visual resume #todo interesting?) complex tech running on my computer show its tech stack down to the palette runtime w its componentsl two months
      -  timeline jan 1 - mar 31 loops: study bugs, rewrite, reconfigure ::: .exe binary on my machine
- viz 3 how i overcame it
  - #keywords w-level and high-level split viz
  - cpp cmake llvm stack infra w quick descriptions
  - order of exe cpp o bc ll native
  - lex parse link
  - filsys langs and tools installed, root bash, cmake gui app
  - chatgpt 3.5 gemini agile mvp velocity productivity (econ)
- viz 4 tldr conclusion
  - #keywords
  - one basic block llvm ir bitcode simple easy
  - ASM ISA x86 ARM PowerPC
  - apple msft linux
  - vm in llvm? doubt ill include that. unless somewhere in the stack as a lightbulb sidenote i guess. thats not minimal viz tho.
  - low level:
    - project source code
    - llvm libs headers
    - cmake config 
  - high-level
    -  compiler frontend vs. backend
    -  compiler vs. programming language
    -  compiler vs. operating system.

- next steps:
  - see if i can simplify those longform p1 viz ideas above for next time
  - then i can draw super rough drafts for them
  - then look overall at all 4 viz drafts
  - then compare with p1 text draft 3
  - then can make 4 better viz drafts for p1
  - see if i can make handdrawn viz look good by scanning & color inverting them for dark mode. dont want them to look too photo-edited though. otherwise, digital art would take too long honestly
  
# progress april 17, 2024

done:
- viz for basic tech stacks for all projects (in assets)
- viz for all p1 components categorized by four content sections

next steps: (p1)
- see if i can simplify the p1 component viz ideas because they're way too much.
- i had a thought to include more visualizations than the four main viz but idk how that could work.
- so, next step is p1 viz components draft two

# progress april 18, 2024

- i realized essentially the p1 viz components ideas are meta/high/mid/low levels
- i dont want infra diagrams to be redundant though:
  - llvm on the web (gh)
  - llvm dir tree / project source tree
  - all llvm infra/tooling diagram
  - all llvm stack (and meta stack that its in)
  - llvm process via file extension
  - all actual key code files (3)
  - key lessons:
    - lex parse link
    - backend vs frontend
    - vs language
    - vs operating system
- i was able to write about all that ^ simply though so maybe i can make it work

## progress april 19, 2024

- tried canva so i could use their icons to get this done quickly.

## progress april 22, 2024

- i've used canva before and decided i'll use canva for this. it'll be way better visually.
- i'll still draft with drawing

next steps:
- keep browsing canva and choose which icon collections i like the look of
- i doubt i'll use logos even for the open source software, ill just use names in the same font
- i'll use open source tech logos on the home page of my portfolio though for skills i know
- elements i might need: (draft one)
  - business buildings
  - server cloud
  - library of code
  - laptop
  - code snippet
  - terminal
  - file
  - compiling/building/generating file
  - running/executing file
  - stack of files
  - arrows & lines
  - perspective magnifying glass type icon optional
  - more complex ones:
    - make tokenizing, mapping, and translating via dictionaries look cool
    - visuals for english, code, bytecode, ISA, and binary 
    - chip hardware components (vna)

# progress april 23, 2024

- looked through a bunch of canva icons
- i found a bunch i like but couldn't find any collections by one artist of the same style
- i think canva might not be a good choice because of that.
- i'll probably draw and scan and flip to dark mode to see if that'll work, otherwise i have too many different icon types i need to find a cohesive collection. i dont wanna spend too much time on this. but it has to look nice.

# progress april 24, 2024

- color palette day
- decided on a custom color palette which is like london blue and light blue-grey and light/dark copper. i found this afterwards and this is kinda similar but this one is more green: https://images.squarespace-cdn.com/content/v1/638773c92dfb4812d5f5ff28/1669824525700-Q0277UJUN2T2ZDMOH2RX/image-asset.png
  - #adc6c7 light blue-grey
  - #3b738a london blue (primary color)
  - #e5a984 light copper
  - #ab7067 dark copper
- planning to use it really sparingly so it's not too gaudy. it's definitely new colors for me. 
- thankfully i could easily change it
- reviewed the material design dark theme colors and concepts https://m2.material.io/design/color/dark-theme.html#properties
- used this https://m2.material.io/design/color/the-color-system.html#tools-for-picking-colors to generate a mathematical palette but didnt like it as much as teh custom. thankfully the math was really close to the custom though just inputting the primary. i do like the primary 900 though.
- i can overlay the primary color with the dark theme surface when finalizing the website and make the different overlay transparencies if this palette works out
- tested white, 4 different greys and the light blue-grey as font & link colors on the dark theme surface and primary 900 and some look good so i just want to see it large scale on the site
- ive got some light grays and dark grays
- think i might use open-source tech/language logos for the skills section but maybe make them black/white and take the color out. not sure about that though.



# progress apr 25

- reviewing: my the frontend tech stack plan https://github.com/ashlink11/portfolio/tree/main?tab=readme-ov-file#tech-stack
- reviewing: https://pages.github.com/
- reviewing: https://v0.dev/
- note: make sure i configure metadata for this site #todo
  
> GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website.
> If you want to use a build process other than Jekyll or you do not want a dedicated branch to hold your compiled static files, we recommend that you write a GitHub Actions workflow to publish your site. GitHub provides starter workflows for common publishing scenarios to help you write your workflow.
> disable the Jekyll build process by creating an empty file called .nojekyll in the root of your publishing source, then follow your static site generator's instructions to build your site locally
> GitHub Pages does not support server-side languages such as PHP, Ruby, or Python.


- guides:
  - https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site
  - https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow

- GitHub Actions Pages workflow options: Jekyll, Hugo, mdBook, Next.js, NuxtJS, GitHub Pages Jekyll, Astro, Static HTML, & Gatsby
- i'll try Next.js `nextjs.yml`:

```yml
# Sample workflow for building and deploying a Next.js site to GitHub Pages
#
# To get started with Next.js see: https://nextjs.org/docs/getting-started
#
name: Deploy Next.js site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Detect package manager
        id: detect-package-manager
        run: |
          if [ -f "${{ github.workspace }}/yarn.lock" ]; then
            echo "manager=yarn" >> $GITHUB_OUTPUT
            echo "command=install" >> $GITHUB_OUTPUT
            echo "runner=yarn" >> $GITHUB_OUTPUT
            exit 0
          elif [ -f "${{ github.workspace }}/package.json" ]; then
            echo "manager=npm" >> $GITHUB_OUTPUT
            echo "command=ci" >> $GITHUB_OUTPUT
            echo "runner=npx --no-install" >> $GITHUB_OUTPUT
            exit 0
          else
            echo "Unable to determine package manager"
            exit 1
          fi
      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: ${{ steps.detect-package-manager.outputs.manager }}
      - name: Setup Pages
        uses: actions/configure-pages@v5
        with:
          # Automatically inject basePath in your Next.js configuration file and disable
          # server side image optimization (https://nextjs.org/docs/api-reference/next/image#unoptimized).
          #
          # You may remove this line if you want to manage the configuration yourself.
          static_site_generator: next
      - name: Restore cache
        uses: actions/cache@v4
        with:
          path: |
            .next/cache
          # Generate a new cache whenever packages or source files change.
          key: ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-${{ hashFiles('**.[jt]s', '**.[jt]sx') }}
          # If source files changed but packages didn't, rebuild from a prior cache.
          restore-keys: |
            ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-
      - name: Install dependencies
        run: ${{ steps.detect-package-manager.outputs.manager }} ${{ steps.detect-package-manager.outputs.command }}
      - name: Build with Next.js
        run: ${{ steps.detect-package-manager.outputs.runner }} next build
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./out

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```


current build process: https://github.com/ashlink11/ashlink11/actions/runs/8836633679

## progress sat apr 27, 2024

- current build just needs an `.md` file in a repo
- i did notice there was a 1-2 day delay on the build update which was really weird

## progress sun apr 28, 2024

- found this. next guide for the build: https://nextjs.org/learn-pages-router/basics/deploying-nextjs-app/github

## progress mon apr 29, 2024

- looks like i might need to try a few deployments
- `npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/main/basics/basics-final"` from https://nextjs.org/learn-pages-router/basics/deploying-nextjs-app/setup where i would do the build on vercel.com
- try v0.dev --> "React code based on shadcn/ui and Tailwind CSS."
- look for boilerplate on next.js https://vercel.com/templates/next.js
- read through this: https://vercel.com/docs/deployments/git/vercel-for-github


## progress tues apr 30, 2024

- actually the links from the last couple days arents for github pages
- i should read through the nextjs gh actions yaml file

- gh actions yt vid https://www.youtube.com/watch?v=URmeTqglS58 (watched)
- devops journey gh actions vid https://www.youtube.com/watch?v=mFFXuXjVgkU (watched) 
- beyond fireship gh actions vid https://www.youtube.com/watch?v=yfBtjLxn_6k

#### gh actions:
- workflow automation tool
- build, test, deploy
- workflow yaml file: define workflows with YAML for each step 
- can add scripts
- keywords: on, jobs, steps, uses, with, etc. (dockerfiles are FROM, RUN, COPY, EXPOSE, CMD, etc.)
- essentially configures the website environment but doesnt necessarily use an Azure container
- events, jobs, runners, steps, actions
- event: trigger for a workflow (e.g. push to main) `on: push`
  - then runs all the jobs in the workflow
- jobs have a name, e.g. run the portfolio-build job
- runner: container env that will run the code (gh runs for you by default hosted on gh)
  - microsoft windows, linux ubuntu-latest, and mac os
  - checkout code and then run the job
- `repo/.github/worflows/workflow1.yml` dir struct
- use the workflow marketplace for boilerplate

## progress sat may 4
notes:
- so vercel.com isnt hosting it
- i dont see it cloning any code other than node, cache, npm build, and github hosting
- they link this doc in the yml file https://nextjs.org/docs/ > api reference

next steps:
- i think best idea is to try to run it next and see if i get any error messages
- i do need to figure out what type of files it expects in the repo, so might need to look at the next.js vercel templates first

## progress tues may 7
- got the nextjs yml file in my ashlink11 repo
- monitoring the build

## progress fri may 10

```bash
node -v (need at least 18)

v18.16.0
```

- npx, yarn, pnpm, or bun? try bun.
- super interesting i can install bun with docker #key i could use that to demo backend dev skills (fullstack dev)

```bash
brew install oven-sh/bun/bun

bun create next-app

# TypeScript, ESLint, Tailwind CSS, App Router
dependencies:
- react
- react-dom
- next
- typescript
- @types/react
- @types/node
- @types/react-dom
- tailwindcss
- postcss
- autoprefixer
- eslint
- eslint-config-next
npm WARN EBADENGINE Unsupported engine {
npm WARN EBADENGINE   package: 'next@14.2.3',
npm WARN EBADENGINE   required: { node: '>=18.17.0' },
npm WARN EBADENGINE   current: { node: 'v18.16.0', npm: '9.6.7' }
npm WARN EBADENGINE }


# new 
npm i -g create-next-app

# then moved files up a layer

bun install

bun install v1.1.7 (b0b7db5c)
[4.81ms] migrated lockfile from package-lock.json

 14 packages installed [365.00ms]

```

- need updated node to update create-app
- install via `.pkg` from node.js

```bash
This package has installed:
	•	Node.js v22.1.0 to /usr/local/bin/node
	•	npm v10.7.0 to /usr/local/bin/npm
Make sure that /usr/local/bin is in your $PATH.
```

- that made `bun.lockb` file
- tried this just to check node version installed actually in this repoL

```bash
npm i -g create-next-app                   

npm error code EEXIST
npm error path /usr/local/bin/create-next-app
npm error EEXIST: file already exists
npm error File exists: /usr/local/bin/create-next-app
npm error Remove the existing file and try again, or run npm
npm error with --force to overwrite files recklessly.

npm error A complete log of this run can be found in: /Users/ash/.npm/_logs/2024-05-10T13_13_07_293Z-debug-0.log
```

- so i think i'm good because i guess bun installed it and it was good enough. i could redo the whole install if i have any issues #key
- now follow the next-app README 


###### test running the app

- only gives these so be careful with bun bc their readme is outdated #key


```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

```bash
❯ bun run
Usage: bun run [flags] <file or script>

Flags:
      --silent               Don't print the script command
      --filter               Run a script in all workspace packages matching the pattern
  -b, --bun                  Force a script or package to use Bun's runtime instead of Node.js (via symlinking node)
      --shell                Control the shell used for package.json scripts. Supports either 'bun' or 'system'
      --watch                Automatically restart the process on file change
      --hot                  Enable auto reload in the Bun runtime, test runner, or bundler
      --smol                 Use less memory, but run garbage collection more often
  -r, --preload              Import a module before other modules are loaded
      --inspect              Activate Bun's debugger
      --inspect-wait         Activate Bun's debugger, wait for a connection before executing
      --inspect-brk          Activate Bun's debugger, set breakpoint on first line of code and wait
      --if-present           Exit without an error if the entrypoint does not exist
      --no-install           Disable auto install in the Bun runtime
      --install              Configure auto-install behavior. One of "auto" (default, auto-installs when no node_modules), "fallback" (missing packages only), "force" (always).
  -i                         Auto-install dependencies during execution. Equivalent to --install=fallback.
  -e, --eval                 Evaluate argument as a script
      --print                Evaluate argument as a script and print the result
      --prefer-offline       Skip staleness checks for packages in the Bun runtime and resolve from disk
      --prefer-latest        Use the latest matching versions of packages in the Bun runtime, always checking npm
  -p, --port                 Set the default port for Bun.serve
      --conditions           Pass custom conditions to resolve
      --main-fields          Main fields to lookup in package.json. Defaults to --target dependent
      --extension-order      Defaults to: .tsx,.ts,.jsx,.js,.json
      --tsconfig-override    Specify custom tsconfig.json. Default <d>$cwd<r>/tsconfig.json
  -d, --define               Substitute K:V while parsing, e.g. --define process.env.NODE_ENV:"development". Values are parsed as JSON.
  -l, --loader               Parse files with .ext:loader, e.g. --loader .js:jsx. Valid loaders: js, jsx, ts, tsx, json, toml, text, file, wasm, napi
      --no-macros            Disable macros from being executed in the bundler, transpiler and runtime
      --jsx-factory          Changes the function called when compiling JSX elements using the classic JSX runtime
      --jsx-fragment         Changes the function called when compiling JSX fragments
      --jsx-import-source    Declares the module specifier to be used for importing the jsx and jsxs factory functions. Default: "react"
      --jsx-runtime          "automatic" (default) or "classic"
      --env-file             Load environment variables from the specified file(s)
      --cwd                  Absolute path to resolve files & entry points from. This just changes the process' cwd.
  -c, --config               Specify path to Bun config file. Default <d>$cwd<r>/bunfig.toml
  -h, --help                 Display this menu and exit

Examples:
  Run a JavaScript or TypeScript file
  bun run ./index.js
  bun run ./index.tsx

  Run a package.json script
  bun run dev
  bun run lint

Full documentation is available at https://bun.sh/docs/cli/run

package.json scripts (4 found):
  $ bun run dev
    next dev

  $ bun run build
    next build

  $ bun run start
    next start

  $ bun run lint
    next lint
```

- no errors with prepping the bun dev env with `bun run`
- `bun run dev` #todo note that in my final readme for portfolio


```bash
❯ bun run dev
$ next dev
  ▲ Next.js 14.2.3
  - Local:        http://localhost:3000

 ✓ Starting...
 ✓ Ready in 4.2s
(node:35195) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
 ○ Compiling / ...
 ✓ Compiled / in 2.6s (532 modules)
 GET / 200 in 2928ms
 ✓ Compiled in 197ms (250 modules)
 ○ Compiling /favicon.ico ...
 ✓ Compiled /favicon.ico in 987ms (303 modules)
 GET /favicon.ico 200 in 1054ms
```

- IT WORKED.
- portfolio website (web app #key terminology) built locally!

next:
- push to main
- check gh actions
- check site
- Get started by editing app/page.tsx
- continue with the next-app-template 


- guess i have to reconfig the gh actions nextjs template. makes sense i guess.
- instantly started building in gh actions when i pushed `nextjs.yml` to main
- oh it failed because i didnt test building it locally lol i guess its been a while since frontend dev.
- nextjs deploy docs:

> The DPS Workflow: Develop, Preview, and Ship.

> You should also update the following files:
> public/images/profile.jpg with your photo (Recommended: 400px width/height).
> const name = '[Your Name]' in components/layout.js with your name.
> `<p>[Your Self Introduction]</p> in pages/index.js with your self introduction.`

- aha. here was the create-app i was looking for: `npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/main/basics/basics-final"`
- but i think i'm fine for now #key if needed to reinstall or want a better template. we'll see with v0.dev #todo
- okay, here is `package.json` (i gathered the dependencies above from the terminal notes)

```json
{
  "name": "test",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },
  "dependencies": {
    "@types/node": "20.12.11",
    "@types/react": "18.3.1",
    "@types/react-dom": "18.3.0",
    "autoprefixer": "10.4.19",
    "eslint": "8.57.0",
    "eslint-config-next": "14.2.3",
    "next": "14.2.3",
    "postcss": "8.4.38",
    "react": "18.3.1",
    "react-dom": "18.3.1",
    "tailwindcss": "3.4.3",
    "typescript": "5.4.5"
  }
}
```

- okay YES, bun installed with node v20. great.
- ohh interesting. bun is so new you cant build nextjs app with it yet. 
  - their web docs: https://bun.sh/guides/ecosystem/nextjs 
  - their gh docs: https://github.com/vercel/next.js/blob/canary/contributing/core/building.md 
  - ^oh interesting. that has a wasm build #key

> The Next.js App Router currently relies on Node.js APIs that Bun does not yet implement. The guide below uses Bun to initialize a project and install dependencies, but it uses Node.js to run the dev server.

- their gh issues show `pnpm build`
- i wonder how `pnpm` is compatible with `bun.lockb`
- oh my god in the issues comment i found it's `bun run build`, not `bun build` okay awesome! yes.


```bash
❯ bun run build
$ next build
  ▲ Next.js 14.2.3

   Creating an optimized production build ...
(node:38993) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
(node:39003) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
 ✓ Compiled successfully
 ✓ Linting and checking validity of types    
 ✓ Collecting page data    
 ✓ Generating static pages (5/5)
 ✓ Collecting build traces    
 ✓ Finalizing page optimization    

Route (app)                              Size     First Load JS
┌ ○ /                                    5.29 kB        92.2 kB
└ ○ /_not-found                          871 B          87.8 kB
+ First Load JS shared by all            87 kB
  ├ chunks/23-0627c91053ca9399.js        31.5 kB
  ├ chunks/fd9d1056-2821b0f0cabcd8bd.js  53.6 kB
  └ other shared chunks (total)          1.86 kB


○  (Static)  prerendered as static content
```

- alright, that didn't build on gh pages. looks like i might have to manually configure `nextjs.yml` next and replace with `bun` commands
- i found this simplified `node-nextjs.yml` here https://github.com/domcloud/recipes/blob/master/node-nextjs.yml with `yarn`. might try that with `bun` though.

```yml
features:
  - node lts
nginx:
  root: public_html/public
  passenger:
    enabled: "on"
    app_start_command: env PORT=$PORT yarn start
  locations:
    - match: /_next/
      alias: public_html/.next/
commands:
  - yarn install
  - yarn build
```


- first save the existing `.yml`:

```yml
# Sample workflow for building and deploying a Next.js site to GitHub Pages
#
# To get started with Next.js see: https://nextjs.org/docs/getting-started
#
name: Deploy Next.js site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Detect package manager
        id: detect-package-manager
        run: |
          if [ -f "${{ github.workspace }}/yarn.lock" ]; then
            echo "manager=yarn" >> $GITHUB_OUTPUT
            echo "command=install" >> $GITHUB_OUTPUT
            echo "runner=yarn" >> $GITHUB_OUTPUT
            exit 0
          elif [ -f "${{ github.workspace }}/package.json" ]; then
            echo "manager=npm" >> $GITHUB_OUTPUT
            echo "command=ci" >> $GITHUB_OUTPUT
            echo "runner=npx --no-install" >> $GITHUB_OUTPUT
            exit 0
          else
            echo "Unable to determine package manager"
            exit 1
          fi
      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: ${{ steps.detect-package-manager.outputs.manager }}
      - name: Setup Pages
        uses: actions/configure-pages@v5
        with:
          # Automatically inject basePath in your Next.js configuration file and disable
          # server side image optimization (https://nextjs.org/docs/api-reference/next/image#unoptimized).
          #
          # You may remove this line if you want to manage the configuration yourself.
          static_site_generator: next
      - name: Restore cache
        uses: actions/cache@v4
        with:
          path: |
            .next/cache
          # Generate a new cache whenever packages or source files change.
          key: ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-${{ hashFiles('**.[jt]s', '**.[jt]sx') }}
          # If source files changed but packages didn't, rebuild from a prior cache.
          restore-keys: |
            ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-
      - name: Install dependencies
        run: ${{ steps.detect-package-manager.outputs.manager }} ${{ steps.detect-package-manager.outputs.command }}
      - name: Build with Next.js
        run: ${{ steps.detect-package-manager.outputs.runner }} next build
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./out

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4


```




- i pasted this into gh.com nextjs.yml and got "missing required root key `on`"
- alright i'm probably going to have to merge those two `.yml`s. planning to try tomorrow.
- this reference looks great though: https://nextjs.org/docs/pages/api-reference/create-next-app



## progress sat may 11, 2024

- i noticed yesterday i mixed up the two repos so make sure i put the local build that works into ashlink11 repo
- been doing other stuff today and planning to loop around to this again in a bit so i can complete my weekly goal of the website build done and hosted on gh pages, not just working on my machine from yesterday 


## progress tue may 14, 2024 (begin study nextjs yml)

- analyze first part of next.js yml config:

```yml
# Sample workflow for building and deploying a Next.js site to GitHub Pages
#
# To get started with Next.js see: https://nextjs.org/docs/getting-started
#
name: Deploy Next.js site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Detect package manager
        id: detect-package-manager
        run: |
          if [ -f "${{ github.workspace }}/yarn.lock" ]; then
            echo "manager=yarn" >> $GITHUB_OUTPUT
            echo "command=install" >> $GITHUB_OUTPUT
            echo "runner=yarn" >> $GITHUB_OUTPUT
            exit 0
          elif [ -f "${{ github.workspace }}/package.json" ]; then
            echo "manager=npm" >> $GITHUB_OUTPUT
            echo "command=ci" >> $GITHUB_OUTPUT
            echo "runner=npx --no-install" >> $GITHUB_OUTPUT
            exit 0
          else
            echo "Unable to determine package manager"
            exit 1
          fi
      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: ${{ steps.detect-package-manager.outputs.manager }}
      - name: Setup Pages
        uses: actions/configure-pages@v5
        with:
          # Automatically inject basePath in your Next.js configuration file and disable
          # server side image optimization (https://nextjs.org/docs/api-reference/next/image#unoptimized).
          #
          # You may remove this line if you want to manage the configuration yourself.
          static_site_generator: next
```

- run manually from action tab? does this just mean custom and not jekyll?
- check actions to make sure permissions work, but they should
- concurrent deployment? i guess if multiple commits near each other?
- the rest is jobs.
- first job: ubuntu latest is confirmed ideal rn
- yarn is package manager. change this to bun and install bun on the box. (#todonext)
- also install npm with ci (clean install)
- i guess yarn and npm are the most common ones
- then set up node. make sure bun uses node (#todonext) and check that bun is compatible with node (#todonext)
- then set up pages. make sure pages is compatible with bun (#todonext)
- otherwise, reinstall entire project with yarn, and if that doesnt work, npm
- note: doesn't seem like it'll work with React Server Components (#todonext) - check on this because i assume v0.dev uses that. but idk. but there is an option to manage the configure it myself (#todonext) which would be preferrable since i want to use latest React features.

next steps:
- use #todonext tags for very next steps
  

## progress wed may 15, 2024

- rest of nextjs yml config:

```yml
      - name: Restore cache
        uses: actions/cache@v4
        with:
          path: |
            .next/cache
          # Generate a new cache whenever packages or source files change.
          key: ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-${{ hashFiles('**.[jt]s', '**.[jt]sx') }}
          # If source files changed but packages didn't, rebuild from a prior cache.
          restore-keys: |
            ${{ runner.os }}-nextjs-${{ hashFiles('**/package-lock.json', '**/yarn.lock') }}-
      - name: Install dependencies
        run: ${{ steps.detect-package-manager.outputs.manager }} ${{ steps.detect-package-manager.outputs.command }}
      - name: Build with Next.js
        run: ${{ steps.detect-package-manager.outputs.runner }} next build
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./out

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

- cache: that's good it's clearing the cache every time so i don't have to manually, which i wouldn't even be able to.
- dependencies: these commands don't look familiar, but i'll have to figure out where those functions come from. i guess in the package manager source code? #todonext
- artifacts: i guess this is where all the extra code & assets are stored: images, setup scripts, css, source code, built code, etc.
- deploy is a different job from the rest. specifies gh pages i the env

all #todonexts from past two days:
- yarn is package manager. change this to bun and install bun on the box. (#todonext)
- then set up node. make sure bun uses node (#todonext) and check that bun is compatible with node (#todonext)
- then set up pages. make sure pages is compatible with bun (#todonext)
- otherwise, reinstall entire project with yarn, and if that doesnt work, npm
- note: doesn't seem like it'll work with React Server Components (#todonext) - check on this because i assume v0.dev uses that. but idk. but there is an option to manage the configure it myself (#todonext) which would be preferrable since i want to use latest React features.
- dependencies: these commands don't look familiar, but i'll have to figure out where those functions come from. i guess in the package manager source code? #todonext

next steps in simple terms:
- check if bun is compatible with node and gh pages & try to config bun because it's latest package manager
- if not, yarn or npm instead of bun
- research if this config template works with React Server Components and if v0.dev uses React Server Components
- research where the dependency install commands come from
- at each step: research each bash command

## progress th may 16, 2024

- these are the two most important lines in the yml i think:

```yml
      - name: Install dependencies
        run: ${{ steps.detect-package-manager.outputs.manager }} ${{ steps.detect-package-manager.outputs.command }}
      - name: Build with Next.js
        run: ${{ steps.detect-package-manager.outputs.runner }} next build
```
- looks like all these functions are in the package manager and the variables like steps and manager are part of the yml variables

## progress sat may 18, 2024:

- this is the code i need to try to change first:

```yml
          if [ -f "${{ github.workspace }}/yarn.lock" ]; then
            echo "manager=yarn" >> $GITHUB_OUTPUT
            echo "command=install" >> $GITHUB_OUTPUT
            echo "runner=yarn" >> $GITHUB_OUTPUT
            exit 0
```

- trying this first:

```yml
          if [ -f "${{ github.workspace }}/yarn.lock" ]; then
            echo "manager=yarn" >> $GITHUB_OUTPUT
            echo "command=install" >> $GITHUB_OUTPUT
            echo "runner=yarn" >> $GITHUB_OUTPUT
            exit 0

```

- first i tried running the origin nextjs.yml in a git repo because i hadn't yet. also because i noticed bun used npm to instead create-next-app, so i can't use bun clearly.

```
build
failed 2 minutes ago in 5s
Search logs
2s
0s
0s
1s
0s
Run actions/configure-pages@v5
Error: Get Pages site failed. Please verify that the repository has Pages enabled and configured to build using GitHub Actions, or consider exploring the `enablement` parameter for this action. Error: Not Found - https://docs.github.com/rest/pages/pages#get-a-apiname-pages-site
Error: HttpError: Not Found - https://docs.github.com/rest/pages/pages#get-a-apiname-pages-site
```

- github actions showed this^

- when i created nextjs.yml from Settings > Pages instead of actions it built the site. so, website build is done.

## progress mon may 20, 2024

- today's goal: finalize project page layout
- i took at look at draft two of the projects ui layout
- it looks good for desktop and not as good mobile
- i do want to make the diagrams decently complicated, so i guess the home page will just have to look good on mobile
- i will want to test it on small laptop as well as largest size monitor screens
- ui sidenote: i am doubting dark mode actually. i think light mode is more professional and daytime.
- i want it to look like a customized Medium article ideally.
- make sure i add the date of the article my name somewhere on the page like right side of nav bar i think.
- no sticky nav bar is fine because its too risky to be janky and annoying and plus the project pages won't be that long.
- i could split the two middle diagrams into left and right in-line with the text actually to add interest and give context about where you are on the page and make it cognitively easier because those diagrams will of course be simpler. but again that has to instead stack on mobile but should otherwise look fine. #todonext for tomorrow/this week.
- otherwise, that's a good start and is third draft, so time to build it and see what it looks like.


## progress wed may 22

- goal: create draft one home page layout (done)
- image saved in assets
- actually i want the same layout as my old portfolio from 2020, so i can show how i've evolved this open-source software over time to show minimal frontend skills (since i'm not applying to be a frontend dev anymore)
- wondering if i have a screenshot of my old portfolio to see the comparison. but it really don't matter too much. #todo-not-essential
- but i can take a look at the old html and css for the responsive layout cause i made it by hand #todokey


next goal: plan all canva diagrams, but for the next day just project one diagram one so its not as much as trying to do all 4 p1 diagrams in one day

## progress mon may 27
- i only have this week til saturday left of free canva pro so gotta get moving on it

## progress tue june 11
- actually dont want to use canva. i'll waste way too much time on it when i can just draw.
- p1 draft two text above from this doc, quicklink: https://github.com/ashlink11/portfolio/blob/main/addtl-readme-docs/project-one-frontend-notes.md#progress-th-apr-11-p1-text-content-draft-3-revised-draft-2-in-place
- reviewing my p1 all concepts overview diagram: https://github.com/ashlink11/portfolio/blob/main/assets/apr-17-p1-p2-p3-stacks-and-p1-components.jpg and diagram 1 draft 1 https://github.com/ashlink11/portfolio/blob/main/assets/apr-13-project-one-visual-one-draft-one.jpg
- today: made p1 diagram1 draft2, it's here: https://github.com/ashlink11/portfolio/blob/main/assets/june-11-p1-diagram1-draft2.JPG

## w june 12

- next: get my old portfolio website code and transfer it to react, then try v0.dev

## fr june 14

- added a photo of the first draft of the site color palette to assets.
- next steps are to make a test light theme with those colors.
- that'll make testing out v0.dev more fun and i wont have to redo it later.
- note: i updated the assets names so they're better organize but that will ahve broken some links throughout these notes. thats fine bc im planning to clean up the repo anyway before apps.
- note: deleted the color palette working on a draft two for later

## sun june 16
- finally tried out v0.dev which makes everything so easy
- i generated a demo and i'm happy with it
- next step: https://v0.dev/docs#integrating-generated-code-into-your-nextjs-app














