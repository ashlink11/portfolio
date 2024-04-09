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




























