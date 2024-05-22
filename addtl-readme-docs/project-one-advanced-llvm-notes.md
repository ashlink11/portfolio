# project one (llvm project) advanced llvm notes
#### start mar 31, 2024

- .exe output is:

```bash
❯ ./bin/ModuleMakerTest 
BC??5b
      0$JY?f????
                Q?L!
                    5
                     !?#?A?I29??
                                ?b?
                                   EB?
                                      Bd2K
22?Hp?!#D??A?d? CF? ?22?*(*?1|?\? ??? 
"f?B??RB?ɐq?PH
	&C?B2&
?#?d `!
Esb1????f=?C8?ÌB?yxs?q
                      ???3
                          B??Ρf0=?C8??=?C=?=?x?tpyH?ppzpvx?p ????0n0???P3??!?!?af0?;??;?C9?<??<?;??v`{h7h?rh7??p??p`v(v?vx?w???q?r??y??,???????0bȡ?̡??a?!ā?a֐C9?C9?C9?C9??8?C8?;??/??<??;?;??
    ?i?pX?rp?thx`?t?t???S??P??@? ?P3 (???A?!܁?????fQ8?C:??;?P$v`{h7`?wxx?QL???P3j?a?!??~??!?aT??8??;?C=?C9??<?C;??;?Ì?
?y??w?z(r??\????P?0#??A?????fH;??=???8?C9??<??9??;?<?H?v`?qX????`??? ?0? ?Pn?0?0?????P?0#??a???!?!?!?!?!f ?;?C=?9??9?X?ppwxzH?wp????0???@??0?s?w?_??pp?t??tЇr???A9??8?C=?C9?@Ġʡ?A??f$c0???0?@?0C!?usH?_??|??r???<??<??8?C:??;?Ì?
                                         H!Ba?!??R??-

?A???!?!??4?`?P? ?@? ?P????y(?p`vx?z(rXp??8?;??=??k?!??? ?a? ??aС?a?a?? ?P?
                                                                            ?usH??8??;?C9??9??;?C9?=?;??<??;?;?=??<?C8??a A,?"('?A86???L?x?a??
q 2"??]
       ?main17.0.6test%
```

next steps:
- examine these notes for possible solutions:

```
The code you provided compiles and links successfully, but the output is gibberish because you're writing the LLVM module to standard output (outs()) instead of a file. Here's how to fix it and understand the output better:

Fix for Writing to a File:

Include fstream: Add #include <fstream> at the beginning of your code to work with files.

Create an Output Stream: Replace WriteBitcodeToFile(*M, outs()) with:

C++
std::error_code EC;
raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);

// Check for errors
if (EC) {
    llvm::errs() << "Error opening file: " << EC.message() << '\n';
    return 1;
}

WriteBitcodeToFile(*M, OutFile);
Use code with caution.
This code opens a file named "ModuleMakerTest.bc" for writing and writes the bitcode representation of your module to it.

Understanding the Output:

The gibberish output you see when writing to outs() is the actual bitcode representation of your LLVM module. It's not human-readable by default.

Alternative: Using opt for Analysis:

Instead of writing the bitcode to a file, you can use the opt tool from the LLVM installation to analyze or optimize your module:

opt -S src/ModuleMakerTest.cpp -o ModuleMakerTest.ll
This command runs the opt tool on your source code (src/ModuleMakerTest.cpp) and generates an assembly-like representation of the module in a file named "ModuleMakerTest.ll". This output is still not human-readable in its entirety, but it might be easier to understand than the raw bitcode.

Additional Tips:

Consider using a debugger to step through your code and inspect the values of variables like M to verify that the module is being created correctly before writing it to a file.
Refer to the LLVM documentation on WriteBitcodeToFile for more details and alternative ways to write the module (https://llvm.org/docs/BitCodeFormat.html).
Explore LLVM's tools like lli for interpreting the bitcode and running the generated code.
```

## progress tue april 2, 2024:

- attempt change writing to file then output to just writing to file

```cpp
  // Output the bitcode file to stdout (makes gibberish in terminal)
  // WriteBitcodeToFile(*M, outs());

  // write the bitcode to a file instead
  std::error_code EC;
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);
```

- output:

```bash
~/dev/ModuleMakerTest ± ● main
❯ cmake .
-- Configuring done (0.2s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/ash/dev/ModuleMakerTest

~/dev/ModuleMakerTest ± ● main
❯ make
[ 50%] Building CXX object CMakeFiles/ModuleMakerTest.dir/src/ModuleMakerTest.cpp.o
/Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:69:61: error: no member named 'open_flags' in namespace 'llvm::sys::fs'; did you mean 'OpenFlags'?
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);
                                                   ~~~~~~~~~^~~~~~~~~~
                                                            OpenFlags
/usr/local/opt/llvm/include/llvm/Support/raw_ostream.h:42:6: note: 'OpenFlags' declared here
enum OpenFlags : unsigned;
     ^
/Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:69:61: error: incomplete type 'llvm::sys::fs::OpenFlags' named in nested name specifier
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);
                                                   ~~~~~~~~~^~~~~~~~~~~~
/Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:69:93: error: no member named 'open_flags' in namespace 'llvm::sys::fs'; did you mean 'OpenFlags'?
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);
                                                                                   ~~~~~~~~~^~~~~~~~~~
                                                                                            OpenFlags
/usr/local/opt/llvm/include/llvm/Support/raw_ostream.h:42:6: note: 'OpenFlags' declared here
enum OpenFlags : unsigned;
     ^
/Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:69:93: error: incomplete type 'llvm::sys::fs::OpenFlags' named in nested name specifier
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);
                                                                                   ~~~~~~~~~^~~~~~~~~~~~
4 errors generated.
make[2]: *** [CMakeFiles/ModuleMakerTest.dir/src/ModuleMakerTest.cpp.o] Error 1
make[1]: *** [CMakeFiles/ModuleMakerTest.dir/all] Error 2
make: *** [all] Error 2
```

- ^errors with the other method
- back to the outs() method
- can't read bitcode but try the incremental llvm commands instead:

```
❯ opt -S src/ModuleMakerTest.cpp -o ModuleMakerTest.ll
opt: src/ModuleMakerTest.cpp:1:1: error: expected top-level entity
#include "llvm/Bitcode/BitcodeWriter.h" 
^
# then had to move .cpp comments to bottom but didnt work

~/dev/ModuleMakerTest ± ●● main
❯ opt ModuleMakerTest.bc -o ModuleMakerTest.opt.bc
opt: ModuleMakerTest.bc: error: Could not open input file: No such file or directory
```

next steps:
- dont use `opt` commands but something else like `clang`?
- remember, i got [this non-llvm lib tutorial from llvm docs](https://llvm.org/docs/GettingStarted.html#an-example-using-the-llvm-tool-chain) to run, so try/review those commands first for base process
- then can try [this basic llvm docs llvm lib config/build/run tutorial](https://llvm.org/docs/GettingStarted.html#getting-the-source-code-and-building-llvm) for incremental compiling commands
- more possibilities:
  > Consider using a debugger to step through your code and inspect the values of variables like M to verify that the module is being created correctly before writing it to a file.
  > Refer to the LLVM documentation on WriteBitcodeToFile for more details and alternative ways to write the module (https://llvm.org/docs/BitCodeFormat.html).
  > Explore LLVM's tools like lli for interpreting the bitcode and running the generated code.
- goal: "generate an assembly-like representation of the module in a file named `ModuleMakerTest.ll`."

## progress wed april 3

- [non-llvm example on llvm.org](https://llvm.org/docs/GettingStarted.html#an-example-using-the-llvm-tool-chain)
  - `clang hello.c -o hello` to native exe
  - `clang -O3 -emit-llvm hello.c -c -o hello.bc` to LLVM bitcode file
  - `./hello` run and `lli hello.bc` to run with LLVM JIT (`lli`)
  - `llvm-dis < hello.bc | less` to look at LLVM ASM assembly
  - `llc hello.bc -o hello.s` compile to native ASM using LLC code gen
  - `gcc hello.s -o hello.native` assemble ASM into a native exe
  - `./hello.native` run native exe
- [custom build basic llvm.org llvm lib config/build/run tutorial](https://llvm.org/docs/GettingStarted.html#getting-the-source-code-and-building-llvm)
  - use git clone shallow for llvm install
  - configure llvm and clang `cmake -S llvm -B build -G <generator> [options]` (for advanced projects)
  - build llvm and clang `cmake --build build [--target <target>]`
  - build only llvm and no other sub-projects (???todo: understand this and which command is which? they both build.) - set up an llvm build with debugging info, then compile llvm and run llvm tests `cmake -S llvm -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug` then `ninja -C build check-llvm`
- [stand-alone builds (use pre-built native clang/llvm libs)](https://llvm.org/docs/GettingStarted.html#stand-alone-builds)
  -  once llvm is installed:
 
```bash
cmake -G Ninja -S path/to/llvm-project/$subproj \
      -B $buildir_subproj \
      -DLLVM_EXTERNAL_LIT=/path/to/lit \
      -DLLVM_ROOT=/path/to/llvm/install/prefix
```

```
Both the LLVM_ROOT and LLVM_EXTERNAL_LIT options are required to do stand-alone builds for all sub-projects. Additional required options for each sub-project can be found in the table below.

The check-$subproj and install build targets are supported for the sub-projects listed in the table below.

Sub-Project - Required Sub-Directories - Required CMake Options

llvm - llvm, cmake, third-party - LLVM_INSTALL_UTILS=ON

clang - clang, cmake - CLANG_INCLUDE_TESTS=ON (Required for check-clang only)

lld - lld, cmake - n/a options
```

notes:
- these might be useful required options for project two (#projecttwo)
- probably don't need for this project unless outs() is complicated.
- what is a sub-project?
- different configs probably aren't needed.
- **focus on c++ outs() code next and looking up the specific bug.**

## progress thurs apr 4, 2024

- updated the outs() to this:

```cpp
#include "llvm/Bitcode/BitcodeWriter.h" 
#include "llvm/IR/BasicBlock.h"
#include "llvm/IR/Constants.h"
#include "llvm/IR/DerivedTypes.h"
#include "llvm/IR/Function.h"
#include "llvm/IR/InstrTypes.h"
#include "llvm/IR/Instruction.h"
#include "llvm/IR/Instructions.h"
#include "llvm/IR/LLVMContext.h"
#include "llvm/IR/Module.h"
#include "llvm/IR/Type.h"
#include "llvm/Support/raw_ostream.h"
#include "llvm/Support/FileSystem.h" // Added for file operations
#include <fstream>

using namespace llvm;

int main() {
  LLVMContext Context;

  // Create the "module" or "program" or "translation unit" to hold the
  // function
  Module *M = new Module("test", Context);

  // Create the main function: first create the type 'int ()'
  FunctionType *FT =
    FunctionType::get(Type::getInt32Ty(Context), /*not vararg*/false);

  // By passing a module as the last parameter to the Function constructor,
  // it automatically gets appended to the Module.
  Function *F = Function::Create(FT, Function::ExternalLinkage, "main", M);

  // Add a basic block to the function... again, it automatically inserts
  // because of the last argument.
  BasicBlock *BB = BasicBlock::Create(Context, "EntryBlock", F);

  // Get pointers to the constant integers...
  Value *Two = ConstantInt::get(Type::getInt32Ty(Context), 2);
  Value *Three = ConstantInt::get(Type::getInt32Ty(Context), 3);

  // Create the add instruction... does not insert...
  Instruction *Add = BinaryOperator::Create(Instruction::Add, Two, Three,
                                            "addresult");

  // explicitly insert it into the basic block...
  Add->insertInto(BB, BB->end());

  // Create the return instruction and add it to the basic block
  ReturnInst::Create(Context, Add)->insertInto(BB, BB->end());

  // Output the bitcode file to stdout but    
  // this makes gibberish in terminal
  // WriteBitcodeToFile(*M, outs());

  // write the bitcode to a file instead
  // std::error_code EC;
  // raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::open_flags::OF_CREAT | sys::fs::open_flags::OF_WRONLY);

    // Output the bitcode file to a file
  std::error_code EC;
  raw_fd_ostream OutFile("ModuleMakerTest.bc", EC, sys::fs::OF_None); // Open the file for writing
  WriteBitcodeToFile(*M, OutFile); // Write the bitcode to the file

  if (EC) {
    errs() << "Error writing bitcode to file: " << EC.message() << '\n';
    return 1;
  }

  // Delete the module and all of its contents.
  delete M;
  return 0;
}

//===- examples/ModuleMaker/ModuleMaker.cpp - Example project ---*- C++ -*-===//
//
// Part of the LLVM Project, under the Apache License v2.0 with LLVM Exceptions.
// See https://llvm.org/LICENSE.txt for license information.
// SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception
//
//===----------------------------------------------------------------------===//
//
// This programs is a simple example that creates an LLVM module "from scratch",
// emitting it as a bitcode file to standard out.  This is just to show how
// LLVM projects work and to demonstrate some of the LLVM APIs.
//
//===----------------------------------------------------------------------===//

```

- ^`cmake .` and `make` of that created the `ModuleMakerTest` .exe in bin
- running the .exe created a `ModuleMakerTest.bc` file in the top-level dir
- `llvm-dis ModuleMakerTest.bc -o ModuleMakerTest.ll` created `ModuleMakerTest.ll` file in the top-level dir
- ^opening that file showed:

```ll
; ModuleID = 'ModuleMakerTest.bc'
source_filename = "test"

define i32 @main() {
EntryBlock:
  %addresult = add i32 2, 3
  ret i32 %addresult
}
```

notes:
- this is huge progress. now i have the simplest possible llvm program running on my laptop and showing the LLVM ASM code which is really simple so i can understand it. this is the foundation to building all the rest of the projects.

next steps:
- wrap up the analysis of the LLVM ASM code
- get the frontend up and running
- that will complete Project One
- ideal timeline is:
> LLVM project
> ideal:
  > total time: 4 weeks
  > finished by: April 30
  > deadline: May 31

- so i should finish it way before the deadline which gives way more time for projects two and three. and project three is CUDA which is the most important.






















