# project one (llvm project) draft 1

## c++ program code ideas: 

  - a simple program with a graph algorithm
  - begins with a list of four Strings which is the input sentence
  - then it creates a graph with each of those words as a node
  - next: apply a transformer algo with a python package and produce an output string
  - next: break down this code block by block or line by line to understand the IR

```cpp
#include <iostream>
#include <vector>
#include <string>
#include <unordered_map>
#include <unordered_set>

using namespace std;

class Graph {
private:
    unordered_map<string, vector<string>> adjacencyList;

public:
    void addEdge(const string& u, const string& v) {
        adjacencyList[u].push_back(v);
        adjacencyList[v].push_back(u); // Assuming undirected graph
    }

    void display() {
        for (const auto& pair : adjacencyList) {
            cout << pair.first << " -> ";
            for (const string& neighbor : pair.second) {
                cout << neighbor << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    vector<string> input = {"This", "is", "a", "sentence"};
    
    Graph graph;
    
    // Create nodes for each word
    for (const string& word : input) {
        graph.addEdge(word, ""); // Adding node for the word
    }
    
    cout << "Graph created with nodes:\n";
    graph.display();
    
    return 0;
}

```

- ability to use a Python library that's compatible with c++
- research these more:


1. NumPy:
NumPy is a Python library that provides support for large, multi-dimensional arrays and matrices, along with a large collection of mathematical functions to operate on these arrays. It is one of the most popular Python libraries for scientific computing and is widely used in many different fields, such as machine learning, data science, and image processing. NumPy is written in C and C++ and provides a Python interface.

2. SciPy:
SciPy is a Python library that provides a wide range of scientific computing functions, including statistical functions, signal processing functions, and optimization functions. It is built on top of NumPy and provides a more comprehensive set of scientific computing tools. SciPy is written in C, C++, and Fortran and provides a Python interface.

3. Matplotlib:
Matplotlib is a Python library that provides a comprehensive set of tools for creating 2D and 3D plots. It is widely used in many different fields, such as scientific computing, data science, and machine learning. Matplotlib is written in Python and C++ and provides a Python interface.

4. Pandas:
Pandas is a Python library that provides data structures and operations for working with structured (tabular, multidimensional, potentially heterogeneous) and time series data. It is built on top of NumPy and provides a more convenient and efficient way to work with data. Pandas is written in Python and C++ and provides a Python interface.

5. PyTorch:
PyTorch is a Python library that provides a deep learning framework. It is widely used in many different fields, such as computer vision, natural language processing, and machine learning. PyTorch is written in Python and C++ and provides a Python interface.

6. TensorFlow:
TensorFlow is a Python library that provides a machine learning framework. It is widely used in many different fields, such as computer vision, natural language processing, and machine learning. TensorFlow is written in Python and C++ and provides a Python interface.

7. Boost.Python:
Boost.Python is a C++ library that provides a way to create Python bindings for C++ code. This allows you to call C++ functions from Python and to expose C++ classes to Python. Boost.Python is a powerful tool for interfacing between Python and C++.

8. CFFI:
CFFI is a Python library that provides a way to call C functions from Python. It is a lower-level library than Boost.Python, but it is more flexible and allows you to call C functions that are not wrapped by Boost.Python.

9. SWIG:
SWIG is a tool that can be used to generate Python bindings for C and C++ code. It is a powerful tool for interfacing between Python and C/C++.

10. Cython:
Cython is a Python language extension that allows you to write Python code that is compiled to C. This can significantly improve the performance of your Python code. Cython is a good choice for Python code that is computationally intensive.


- actually, best packages for ML transformers?

The best Python package for transformers is the Hugging Face Transformers library. It is a state-of-the-art NLP library that provides a wide range of pre-trained models for a variety of tasks, including text classification, question answering, summarization, and translation. The library is easy to use and provides a comprehensive documentation.
Here are some of the key features of the Hugging Face Transformers library:
- Wide range of pre-trained models: The library provides a wide range of pre-trained models for a variety of NLP tasks, including text classification, question answering, summarization, and translation. These models have been trained on large datasets and can be used to achieve state-of-the-art results on a variety of tasks.
- Easy to use: The library is easy to use and provides a comprehensive documentation. The library provides a number of tutorials and examples that can be used to get started quickly.
- Active community: The library has an active community of users and developers. This means that there is a wealth of resources available to help users get the most out of the library.
- Regular updates: The library is regularly updated with new features and bug fixes. This means that users can be confident that they are using the latest and greatest version of the library.

- Transformers is backed by the three most popular deep learning libraries — `Jax`, `PyTorch` and `TensorFlow` — with a seamless integration between them.
- PyTorch is ideal for research and small-scale projects prioritizing flexibility, experimentation and quick editing capabilities for models. TensorFlow is ideal for large-scale projects and production environments that require high-performance and scalable models.

- how can i design Project One (this project) so it's ready for Project Two (mojo/mlir)?
- Project Two additional notes (more than the README):
  - low-level IR in Mojo (implement my own GPU primitives) https://docs.modular.com/mojo/notebooks/BoolMLIR
  - Jax: "accelerator-oriented array computation and program transformation, designed for high-performance numerical computing"
  - Mojo language marries Python and MLIR for AI development: https://www.infoworld.com/article/3695588/mojo-language-marries-python-and-mlir-for-ai-development.html
  - key Mojo
    - progressive types
    - parallelization
    - ownership and borrow-checker
    - manual memory management
    - zero-cost abstractions
    - integrated auto-tuning ******* use this 
  - Lattner Lex Fridman will mojo replace PyTorch and Tensorflow: https://www.youtube.com/watch?v=2Vz2X9I5Z4k
  - Modular yt channel Introduction to Tensors in Mojo🔥: https://www.youtube.com/watch?v=3OWkXNdkx8E
  - why mojo: https://docs.modular.com/mojo/why-mojo
    - "building our platform to unify the world's ML/AI infrastructure, we realized that programming across the entire stack was too complicated. Plus, we were writing a lot of MLIR by hand and not having a good time."
    - "What we wanted was an innovative and scalable programming model that could target accelerators and other heterogeneous systems that are pervasive in the AI field. This meant a programming language with powerful compile-time metaprogramming, integration of adaptive compilation techniques, caching throughout the compilation flow, and other features that are not supported by existing languages."
   
- takeaways:
  - okay i wont be doing ^that till Project Two
  - so Project One should just be compiling LLVM and high-level/low-level IR analysis and then compare it later to Mojo/MLIR
  - alright, now I can continue with Project One

- next step:
  - CMake desktop app? (then what would be the target?)
  - CMake config with git clone llvm as target?
  - CMake config with native llvm as target? change $PATH
  - ^this has been super difficult. but at least i've studied it a tonnnnn


# next steps: (wed mar 20)

- i learned yesterday that CUDA uses CMake to compile so this will be worth it

tring to keep in mind all the factors as i'm trying. common errors:

- Missing Dependencies: correctly installed on your system and properly detected by CMake
- Version Compatibility: Ensure that you are using compatible versions of LLVM and its dependencies. Sometimes, certain LLVM features or functionalities might not be supported in older or newer versions, leading to configuration issues.
- CMake Cache: Sometimes, CMake cache files can cause problems. Try deleting the CMake cache (typically named CMakeCache.txt) in your build directory and re-running CMake to regenerate it.
- Build Configuration: LLVM supports various build configurations, such as Debug, Release, RelWithDebInfo, and MinSizeRel. Make sure you are configuring CMake with the appropriate build configuration for your needs.
- Platform-specific Issues: LLVM might have platform-specific requirements or issues. Ensure that you are following any platform-specific instructions or recommendations provided by the LLVM project.
- Compiler Compatibility: Ensure that your compiler is compatible with LLVM. LLVM often requires a modern C++ compiler (e.g., Clang or a recent version of GCC).
- CMake Options: LLVM provides various CMake options to customize the build process. Make sure you are setting these options appropriately for your requirements.
- Check most recent official docs from LLVM and CMake


# next steps: (fri mar 21)
- need time honestly for my schoolwork till monday

# next steps: (sat mar 22)
- use CMake macOS GUI
  - i have version 3.29.0-rc3
  - directions:

---

CMakeLists.txt example:
```
cmake_minimum_required(VERSION 3.10)
project(LLVMProgram)

find_package(LLVM REQUIRED CONFIG)

include_directories(${LLVM_INCLUDE_DIRS})
add_definitions(${LLVM_DEFINITIONS})

add_executable(LLVMProgram src/main.cpp)
target_link_libraries(LLVMProgram ${llvm_libs})

```


directory structure:
```css
project_directory/
│
├── .vscode/
│   ├── c_cpp_properties.json
│   └── settings.json
│
├── src/
│   └── main.cpp
│
└── CMakeLists.txt
```

The c_cpp_properties.json file is typically used for configuring C/C++ IntelliSense settings in Visual Studio Code. It should be placed in the .vscode directory within your project directory. If the .vscode directory doesn't exist, you can create it manually.

You can create or modify the c_cpp_properties.json file to include the necessary include paths for your project. For example:

```json
{
    "configurations": [
        {
            "name": "Mac",
            "includePath": [
                "${workspaceFolder}/**",
                "/path/to/llvm/include"
            ],
            "defines": [],
            "macFrameworkPath": [
                "/System/Library/Frameworks",
                "/Library/Frameworks"
            ],
            "compilerPath": "/usr/bin/clang",
            "cStandard": "c11",
            "cppStandard": "c++17",
            "intelliSenseMode": "clang-x64"
        }
    ],
    "version": 4
}
```

Replace "/path/to/llvm/include" with the actual path to the directory containing LLVM header files on your system.

Once you've placed the c_cpp_properties.json file in the .vscode directory and configured it properly, Visual Studio Code should use these settings for C/C++ IntelliSense.

.vscode/settings.json:

```json
{
    "cmake.configureSettings": {
        "CMAKE_CXX_COMPILER": "/usr/bin/clang++",
        "CMAKE_EXPORT_COMPILE_COMMANDS": true
    }
}
```


llvm should have been installed this way:

```bash
brew install llvm
```

in summary:

> Building and Running:
> Open the project directory in Visual Studio Code.
> Create the .vscode directory if it doesn't exist.
> Create or update c_cpp_properties.json and settings.json files as shown above. Disable the c++/cmake vscode plugins, etc.
> Create the CMakeLists.txt file with the content provided.
> Write your LLVM program in src/main.cpp.
> Open the CMake macOS UI application.
> Set the source directory to your project directory and the build directory to a subdirectory (e.g., build).
> Click "Configure" and select your preferred generator. (e.g., "Unix Makefiles" for building with Make, or "Xcode" for building with Xcode).
> Click "Generate" to generate the build files.
> Use the CMake macOS UI application to build the project.
> After successful build, execute the generated executable file to run the LLVM program.

done:
- uninstall CMake tools plugin (done)
- uninstall CMake plugin (done)
- uninstall c/c++ extensions plugin (done)
- HUGE WIN: ^those uninstalls got rid of the header error in the main.cpp file (done)
- modify directory structure, add new config file, delete CMake cache, etc. (done)

next steps: (tues mar 26)
- since i fixed the cpp file error with the uninstalls, try basic cmake/make commands again first
- do generator research before config.
- generator research:
  - XCode or Unix Makefiles?:
  - try Unix Makefiles generator first, otherwise `xcode-select --install`, etc.
  - XCode app is not in my applications folder and i'm not sure why not.
  - is there a VSCode generator option?
  - remember: (llvm-project repo notes)
    - the CMake official docs dont have an example for macOS
    - the llvm docs example seems to need Xcode
    - research how Cmake works with macOS
    - clang config too
    - do i need to fresh install the cloned llvm repo?
    - could work: correct bash flags?
    - **i was able to build and run hello.c with clang/llvm (without cmake) so some things were right there**
    - llvm-project repo notes have more detailed source/root dir structure notes
    - specific notes from the llvm and cmake docs in that note file
    - llvm path and install notes in the note file
    - target and path info in the note file
    - i can still search for OSS llvm cmake config examples on gh
    - will i have to match all libs and headers from the project source to the root llvm dirs?
    - it could be a c++ version error or other versioning error (llvm version == clang version though)
    - worst case: try installing XCode
    - review high-level llvm infra so i include all the proper tools and libs for the build
- config choices:
  - cmake GUI app or just cmake/make
    - both need cmake/ccpp-properties configs
    - does GUI have an environment editor for $PATH, etc.?
    - CMake config with git clone llvm as target?
    - CMake config with native llvm as target? change $PATH
    - "The c_cpp_properties.json file is typically used for configuring C/C++ IntelliSense settings in Visual Studio Code."
    - figure out the llvm path
    - other properties json sub-configs
    - .vscode settings cmake config settings file

# progress (wed mar 27)
- using the macOS CMake GUI app
- created a new build folder (done)
- "Generate" defaults to Unix Makefiles and gives the choices of:
  - "use default native compilers"
  - "specify native compilers"
  - "specify toolchain file for cross-compiling"
  - "specify options for cross-compiling"

- clicked Generate > with default native compilers:

Error: "Error in configuration process, project files may be invalid"

```bash
CMake Warning (dev) in CMakeLists.txt:
  No project() command is present.  The top-level CMakeLists.txt file must
  contain a literal, direct call to the project() command.  Add a line of
  code such as

    project(ProjectName)

  near the top of the file, but after cmake_minimum_required().

  CMake is pretending there is a "project(Project)" command on the first
  line.
This warning is for project developers.  Use -Wno-dev to suppress it.

CMake Warning (dev) in CMakeLists.txt:
  cmake_minimum_required() should be called prior to this top-level project()
  call.  Please see the cmake-commands(7) manual for usage documentation of
  both commands.
This warning is for project developers.  Use -Wno-dev to suppress it.

The C compiler identification is AppleClang 15.0.0.15000309
The CXX compiler identification is AppleClang 15.0.0.15000309
Detecting C compiler ABI info
Detecting C compiler ABI info - done
Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc - skipped
Detecting C compile features
Detecting C compile features - done
Detecting CXX compiler ABI info
Detecting CXX compiler ABI info - done
Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
Detecting CXX compile features
Detecting CXX compile features - done
CMake Error at CMakeLists.txt:1 (find_package):
  Could not find a package configuration file provided by "LLVM" with any of
  the following names:

    LLVMConfig.cmake
    llvm-config.cmake

  Add the installation prefix of "LLVM" to CMAKE_PREFIX_PATH or set
  "LLVM_DIR" to a directory containing one of the above files.  If "LLVM"
  provides a separate development package or SDK, be sure it has been
  installed.


CMake Warning (dev) in CMakeLists.txt:
  No cmake_minimum_required command is present.  A line of code such as

    cmake_minimum_required(VERSION 3.29)

  should be added at the top of the file.  The version specified may be lower
  if you wish to support older CMake versions for this project.  For more
  information run "cmake --help-policy CMP0000".
This warning is for project developers.  Use -Wno-dev to suppress it.

Configuring incomplete, errors occurred!
```

also gave these values:

```
CMAKE_BACKWARDS_COMPATIBILITY  2.4
CMAKE_BUILD_TYPE
CMAKE_INSTALL_PREFIX           /usr/local
CMAKE_OSX_ARCHITECTURES
CMAKE_OSX_DEPLOYMENT_TARGET
CMAKE_OSX_SYSROOT              /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk
EXECUTABLE_OUTPUT_PATH
LLVM_DIR                       LLVM_DIR-NOTFOUND
```

- ^those might be all the additional elements the CMakeLists.txt wants with this GUI Generator config
- studying it. (below)
  
- the CMakeLists.txt currently has:

```
find_package(LLVM REQUIRED CONFIG)

include_directories(${LLVM_INCLUDE_DIRS})
add_definitions(${LLVM_DEFINITIONS})

llvm_map_components_to_libnames(llvm_libs core irreader)

add_executable(MyLLVMProgram main.cpp)
target_link_libraries(MyLLVMProgram ${llvm_libs})
```

- make sure i need all of those ^ so try removing each and checking the GUI (todo)

### GUI says i need:

- `project(ProjectName)`
- `cmake_minimum_required()`
> Please see the cmake-commands(7) manual for usage documentation of both commands.

- `(find_package)`
- `CMAKE_PREFIX_PATH`
> CMake Error at CMakeLists.txt:1 (find_package)
> CMake Error at CMakeLists.txt:1 (find_package):
  > Could not find a package configuration file provided by "LLVM" with any of
  > the following names:
    > LLVMConfig.cmake
    > llvm-config.cmake
  > Add the installation prefix of "LLVM" to CMAKE_PREFIX_PATH or set
  > "LLVM_DIR" to a directory containing one of the above files.  If "LLVM"
  > provides a separate development package or SDK, be sure it has been
  > installed.


- also, $PATH, etc., in file sys:
  - `LLVMConfig.cmake`
  - `llvm-config.cmake`

- `cmake_minimum_required(VERSION 3.29)`
  > should be added at the top of the file.  The version specified may be lower
  > if you wish to support older CMake versions for this project.  For more
  > information run "cmake --help-policy CMP0000".

^summary:

i have 6:
- `find_package(LLVM REQUIRED CONFIG)`
- `include_directories(${LLVM_INCLUDE_DIRS})`
- `add_definitions(${LLVM_DEFINITIONS})`
- `llvm_map_components_to_libnames(llvm_libs core irreader)`
- `add_executable(MyLLVMProgram main.cpp)`
- `target_link_libraries(MyLLVMProgram ${llvm_libs})`

GUI terminal error output says I need 4 more:
- `(find_package)`
- `LLVM_DIR` and/or `CMAKE_PREFIX_PATH`
  - (installation prefix of "LLVM")
  - (also, $PATH, etc., in file sys):
    - (LLVMConfig.cmake))
    - (llvm-config.cmake)
- `cmake_minimum_required(VERSION 3.29)`

GUI config screen says I need these 8 sub-configs: (1 repeat)
```
CMAKE_BACKWARDS_COMPATIBILITY  2.4
CMAKE_BUILD_TYPE
CMAKE_INSTALL_PREFIX           /usr/local
CMAKE_OSX_ARCHITECTURES
CMAKE_OSX_DEPLOYMENT_TARGET
CMAKE_OSX_SYSROOT              /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk
EXECUTABLE_OUTPUT_PATH
LLVM_DIR                       LLVM_DIR-NOTFOUND
```

- in total i might need 17 elements in the CMakeLists.txt
- ^this is a huge win because i was having super major trouble knowing that
- remember: `"Error in configuration process, project files may be invalid"`

- next steps:
  - go through each sub-config line-by-line
    - consider if the problem is actually in the c++ project source code though
    - GUI can auto-update the 8 sub-configs on the GUI config screen (but not the rest?)
  - ^if that doesn't work, try a different "Generate" option
    - "specify native compilers"
    - "specify toolchain file for cross-compiling"
    - "specify options for cross-compiling"

### progress (thurs mar 28, 2024)

- new attempt for CMakeLists.txt:
  - need to find the llvm path first though (see under the config) 

```
cmake_minimum_required(VERSION 3.29)

project(MyLLVMProgram)

# Set the LLVM_DIR and CMAKE_PREFIX_PATH to locate LLVM
set(LLVM_DIR /path/to/llvm/installation/lib/cmake/llvm)
set(CMAKE_PREFIX_PATH /path/to/llvm/installation)

# Find LLVM package
find_package(LLVM REQUIRED CONFIG)

# Include LLVM headers
include_directories(${LLVM_INCLUDE_DIRS})

# Add LLVM definitions
add_definitions(${LLVM_DEFINITIONS})

# Map LLVM components to libraries
llvm_map_components_to_libnames(llvm_libs core irreader)

# Set build type (you can adjust this as needed)
set(CMAKE_BUILD_TYPE Debug)

# Set installation prefix
set(CMAKE_INSTALL_PREFIX /usr/local)

# Set target architecture and deployment target
set(CMAKE_OSX_ARCHITECTURES x86_64)
set(CMAKE_OSX_DEPLOYMENT_TARGET 14.4)

# Set the macOS system root
set(CMAKE_OSX_SYSROOT /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk)

# Set executable output path
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

# Add your executable target
add_executable(MyLLVMProgram main.cpp)

# Link LLVM libraries to your executable
target_link_libraries(MyLLVMProgram ${llvm_libs})
```

- finding the llvm install

```bash
find / -name llvm-config.cmake
# ^did not work and started searching Photos and Contacts oddly
# lots of searching /System/Volumes but "not permitted"

echo $LLVM_DIR
# ^no result
```

- couldnt find it but used the GUI native install option
- result:

```bash
The C compiler identification is AppleClang 15.0.0.15000309
The CXX compiler identification is AppleClang 15.0.0.15000309
Detecting C compiler ABI info
Detecting C compiler ABI info - done
Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc - skipped
Detecting C compile features
Detecting C compile features - done
Detecting CXX compiler ABI info
Detecting CXX compiler ABI info - done
Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
Detecting CXX compile features
Detecting CXX compile features - done
CMake Error at CMakeLists.txt:10 (find_package):
  Could not find a package configuration file provided by "LLVM" with any of
  the following names:

    LLVMConfig.cmake
    llvm-config.cmake

  Add the installation prefix of "LLVM" to CMAKE_PREFIX_PATH or set
  "LLVM_DIR" to a directory containing one of the above files.  If "LLVM"
  provides a separate development package or SDK, be sure it has been
  installed.


Configuring incomplete, errors occurred!
```

- ^so it seems the only issue is finding the llvm install dir with its own cmake config. interesting. i didnt know it had a cmake config. that could help a lot.
- also only got 6 errors in the GUI screen from that attempt^:

```
CMAKE_BUILD_TYPE
CMAKE_INSTALL_PREFIX           /usr/local
CMAKE_OSX_ARCHITECTURES
CMAKE_OSX_DEPLOYMENT_TARGET
CMAKE_OSX_SYSROOT              /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk
LLVM_DIR                       LLVM_DIR-NOTFOUND
```

- next steps:
  - go for a second GUI attempt by focusing on the llvm-config.cmake first, then the other GUI screen errors 

# progress fri mar 29, 2024

- "CMake should locate the library automatically if it's installed in a standard location. If not, you might need to specify the path to the library using find_library or similar commands."
- `locate` command finds files
- `not symlinked into /usr/local`
- brew info yielded: (see context below this list)
  - `usr/local/Cellar/llvm/17.0.6_1` (7,207 files, 1.8GB)
  - `/usr/local/opt/llvm/lib/c++`
  - `/usr/local/opt/llvm/lib`
  - `/usr/local/opt/llvm/include`

```bash
brew info llvm

==> llvm: stable 17.0.6 (bottled), HEAD [keg-only]
Next-gen compiler infrastructure
https://llvm.org/
/usr/local/Cellar/llvm/17.0.6_1 (7,207 files, 1.8GB)
  Poured from bottle using the formulae.brew.sh API on 2024-02-02 at 17:29:55
From: https://github.com/Homebrew/homebrew-core/blob/HEAD/Formula/l/llvm.rb
License: Apache-2.0 with LLVM-exception
==> Dependencies
Build: cmake ✘, ninja ✘, swig ✘
Required: python@3.12 ✘, z3 ✘, zstd ✔
==> Options
--HEAD
	Install HEAD version
==> Caveats
To use the bundled libc++ please add the following LDFLAGS:
  LDFLAGS="-L/usr/local/opt/llvm/lib/c++ -Wl,-rpath,/usr/local/opt/llvm/lib/c++"

llvm is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have llvm first in your PATH, run:
  echo 'export PATH="/usr/local/opt/llvm/bin:$PATH"' >> ~/.zshrc

For compilers to find llvm you may need to set:
  export LDFLAGS="-L/usr/local/opt/llvm/lib"
  export CPPFLAGS="-I/usr/local/opt/llvm/include"
==> Analytics
install: 44,707 (30 days), 145,108 (90 days), 470,071 (365 days)
install-on-request: 19,652 (30 days), 63,470 (90 days), 309,979 (365 days)
build-error: 498 (30 days)
```

- fixed the CMakeLists.txt and it configured and generated with this:
  - note: i hadn't updated cmake yet to the latest version
  - GUI output is below the config file

```
cmake_minimum_required(VERSION 3.29)

project(ModuleMakerTest)

# Set the LLVM_DIR and CMAKE_PREFIX_PATH to locate LLVM
set(LLVM_DIR /usr/local/opt/llvm/)
set(CMAKE_PREFIX_PATH /usr/local/opt/llvm/)
# set(LLVM_DIR /path/to/llvm/installation/lib/cmake/llvm)
# set(CMAKE_PREFIX_PATH /path/to/llvm/installation)

# Find LLVM package
find_package(LLVM REQUIRED CONFIG)

# Include LLVM headers
include_directories(${LLVM_INCLUDE_DIRS})

# Add LLVM definitions
add_definitions(${LLVM_DEFINITIONS})

# Map LLVM components to libraries
llvm_map_components_to_libnames(llvm_libs core irreader)

# Set build type (you can adjust this as needed)
set(CMAKE_BUILD_TYPE Debug)

# Set installation prefix
set(CMAKE_INSTALL_PREFIX /usr/local)

# Set target architecture and deployment target
set(CMAKE_OSX_ARCHITECTURES x86_64)
set(CMAKE_OSX_DEPLOYMENT_TARGET 14.4)

# Set the macOS system root
set(CMAKE_OSX_SYSROOT /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk)

# Set executable output path
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

# Add your executable target
add_executable(ModuleMakerTest)

# Link LLVM libraries to your executable
target_link_libraries(ModuleMakerTest ${llvm_libs})
```

- GUI result:

```bash
The C compiler identification is AppleClang 15.0.0.15000309
The CXX compiler identification is AppleClang 15.0.0.15000309
Detecting C compiler ABI info
Detecting C compiler ABI info - done
Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc - skipped
Detecting C compile features
Detecting C compile features - done
Detecting CXX compiler ABI info
Detecting CXX compiler ABI info - done
Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
Detecting CXX compile features
Detecting CXX compile features - done
Performing Test HAVE_FFI_CALL
Performing Test HAVE_FFI_CALL - Success
Found FFI: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libffi.tbd
Looking for histedit.h
Looking for histedit.h - found
Found LibEdit: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/include (found version "2.11")
Performing Test Terminfo_LINKABLE
Performing Test Terminfo_LINKABLE - Success
Found Terminfo: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libcurses.tbd
Found ZLIB: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libz.tbd (found version "1.2.12")
Found zstd: /usr/local/lib/libzstd.dylib
Found LibXml2: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libxml2.tbd (found version "2.9.13")
Configuring done (2.0s)

Configuring done (0.1s)
Generating done (0.0s)
```

- ^in GUI can see it changed `LLVM_DIR` to `/usr/local/opt/llvm/lib/cmake/llvm`
- wouldnt compile with `cmake .` due to old cmake version.
- updated cmake:

```bash
cmake --version

cmake version 3.23.3
CMake suite maintained and supported by Kitware (kitware.com/cmake).


brew upgrade cmake

Warning: Treating cmake as a formula. For the cask, use homebrew/cask/cmake or specify the `--cask` flag.
...
==> Upgrading cmake
  3.23.3 -> 3.29.0
==> Pouring cmake--3.29.0.sonoma.bottle.tar.gz
==> Caveats
To install the CMake documentation, run:
  brew install cmake-docs
...
==> Summary
_  /usr/local/Cellar/cmake/3.29.0: 3,383 files, 59.3MB
# remove a bunch of Homebrew caches:
Removing: /Users/ash/Library/Caches/Homebrew/c-ares--1.26.0... (309KB)
Removing: /Users/ash/Library/Caches/Homebrew/ca-certificates--2023-12-12... (127.7KB)
Removing: /Users/ash/Library/Caches/Homebrew/icu4c--73.2... (29MB)
Removing: /Users/ash/Library/Caches/Homebrew/libnghttp2--1.59.0... (220.1KB)
Removing: /Users/ash/Library/Caches/Homebrew/libuv--1.47.0... (346.5KB)
Removing: /Users/ash/Library/Caches/Homebrew/nghttp2--1.59.0... (816.1KB)
Removing: /Users/ash/Library/Caches/Homebrew/node--21.6.1... (15.8MB)
Removing: /Users/ash/Library/Caches/Homebrew/python@3.12--3.12.1_1... (15.8MB)
Removing: /Users/ash/Library/Caches/Homebrew/readline--8.2.7... (549.7KB)
Removing: /Users/ash/Library/Caches/Homebrew/sqlite--3.45.1... (2.3MB)
Removing: /Users/ash/Library/Caches/Homebrew/xz--5.4.5... (674.7KB)
Removing: /Users/ash/Library/Caches/Homebrew/z3--4.12.5... (13.0MB)
Removing: /Users/ash/Library/Caches/Homebrew/zstd--1.5.5... (846.3KB)
Removing: /Users/ash/Library/Logs/Homebrew/python@3.12... (2 files, 2KB)
Removing: /Users/ash/Library/Logs/Homebrew/openssl@3... (64B)
Removing: /Users/ash/Library/Logs/Homebrew/ca-certificates... (64B)
Removing: /Users/ash/Library/Logs/Homebrew/node... (64B)

cmake --version

cmake version 3.29.0
```


- then bash configured and generated. result:
  
```bash
-- The C compiler identification is AppleClang 15.0.0.15000309
-- The CXX compiler identification is AppleClang 15.0.0.15000309
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test HAVE_FFI_CALL
-- Performing Test HAVE_FFI_CALL - Success
-- Found FFI: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libffi.tbd
-- Looking for histedit.h
-- Looking for histedit.h - found
-- Found LibEdit: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/include (found version "2.11")
-- Performing Test Terminfo_LINKABLE
-- Performing Test Terminfo_LINKABLE - Success
-- Found Terminfo: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libcurses.tbd
-- Found ZLIB: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libz.tbd (found version "1.2.12")
-- Found zstd: /usr/local/lib/libzstd.dylib
-- Found LibXml2: /Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/lib/libxml2.tbd (found version "2.9.13")
-- Configuring done (2.3s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/ash/dev/ModuleMakerTest
```

```bash
make

[ 50%] Building CXX object CMakeFiles/ModuleMakerTest.dir/src/ModuleMakerTest.cpp.o
In file included from /Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:15:
In file included from /usr/local/opt/llvm/include/llvm/Bitcode/BitcodeWriter.h:16:
In file included from /usr/local/opt/llvm/include/llvm/ADT/StringRef.h:12:
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:68:10: error: unknown type name 'constexpr'
  static constexpr uintptr_t Log2MaxAlign = 12;
         ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:68:29: error: expected ';' at end of declaration list
  static constexpr uintptr_t Log2MaxAlign = 12;
                            ^
                            ;
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:71:14: error: expected ';' after expression
    uintptr_t Val = static_cast<uintptr_t>(-1);
             ^
             ;
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:71:15: error: use of undeclared identifier 'Val'
    uintptr_t Val = static_cast<uintptr_t>(-1);
              ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:71:33: error: unknown type name 'uintptr_t'; did you mean 'intptr_t'?
    uintptr_t Val = static_cast<uintptr_t>(-1);
                                ^~~~~~~~~
                                intptr_t
/Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/include/sys/_types/_intptr_t.h:32:33: note: 'intptr_t' declared here
typedef __darwin_intptr_t       intptr_t;
                                ^
In file included from /Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:15:
In file included from /usr/local/opt/llvm/include/llvm/Bitcode/BitcodeWriter.h:16:
In file included from /usr/local/opt/llvm/include/llvm/ADT/StringRef.h:12:
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:72:5: error: use of undeclared identifier 'Val'
    Val <<= Log2MaxAlign;
    ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:72:13: error: use of undeclared identifier 'Log2MaxAlign'
    Val <<= Log2MaxAlign;
            ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:73:33: error: use of undeclared identifier 'Val'
    return reinterpret_cast<T*>(Val);
                                ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:77:14: error: expected ';' after expression
    uintptr_t Val = static_cast<uintptr_t>(-2);
             ^
             ;
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:77:15: error: use of undeclared identifier 'Val'
    uintptr_t Val = static_cast<uintptr_t>(-2);
              ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:77:33: error: unknown type name 'uintptr_t'; did you mean 'intptr_t'?
    uintptr_t Val = static_cast<uintptr_t>(-2);
                                ^~~~~~~~~
                                intptr_t
/Library/Developer/CommandLineTools/SDKs/MacOSX14.4.sdk/usr/include/sys/_types/_intptr_t.h:32:33: note: 'intptr_t' declared here
typedef __darwin_intptr_t       intptr_t;
                                ^
In file included from /Users/ash/dev/ModuleMakerTest/src/ModuleMakerTest.cpp:15:
In file included from /usr/local/opt/llvm/include/llvm/Bitcode/BitcodeWriter.h:16:
In file included from /usr/local/opt/llvm/include/llvm/ADT/StringRef.h:12:
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:78:5: error: use of undeclared identifier 'Val'
    Val <<= Log2MaxAlign;
    ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:78:13: error: use of undeclared identifier 'Log2MaxAlign'
    Val <<= Log2MaxAlign;
            ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:79:33: error: use of undeclared identifier 'Val'
    return reinterpret_cast<T*>(Val);
                                ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:83:33: error: expected ')'
    return (unsigned((uintptr_t)PtrVal) >> 4) ^
                                ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:83:21: note: to match this '('
    return (unsigned((uintptr_t)PtrVal) >> 4) ^
                    ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:84:33: error: expected ')'
           (unsigned((uintptr_t)PtrVal) >> 9);
                                ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:84:21: note: to match this '('
           (unsigned((uintptr_t)PtrVal) >> 9);
                    ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:216:35: error: a space is required between consecutive right angle brackets (use '> >')
struct DenseMapInfo<std::pair<T, U>> {
                                  ^~
                                  > >
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:217:16: warning: alias declarations are a C++11 extension [-Wc++11-extensions]
  using Pair = std::pair<T, U>;
               ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:218:21: warning: alias declarations are a C++11 extension [-Wc++11-extensions]
  using FirstInfo = DenseMapInfo<T>;
                    ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:219:22: warning: alias declarations are a C++11 extension [-Wc++11-extensions]
  using SecondInfo = DenseMapInfo<U>;
                     ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:251:19: warning: variadic templates are a C++11 extension [-Wc++11-extensions]
template <typename... Ts> struct DenseMapInfo<std::tuple<Ts...>> {
                  ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:251:52: error: no member named 'tuple' in namespace 'std'
template <typename... Ts> struct DenseMapInfo<std::tuple<Ts...>> {
                                              ~~~~~^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:251:58: error: 'Ts' does not refer to a value
template <typename... Ts> struct DenseMapInfo<std::tuple<Ts...>> {
                                                         ^
/usr/local/opt/llvm/include/llvm/ADT/DenseMapInfo.h:251:23: note: declared here
template <typename... Ts> struct DenseMapInfo<std::tuple<Ts...>> {
                      ^
fatal error: too many errors emitted, stopping now [-ferror-limit=]
4 warnings and 20 errors generated.
make[2]: *** [CMakeFiles/ModuleMakerTest.dir/src/ModuleMakerTest.cpp.o] Error 1
make[1]: *** [CMakeFiles/ModuleMakerTest.dir/all] Error 2
make: *** [all] Error 2

```

- ^oh. didn't  i'm getting unknown types and syntax errors in the llvm install files.
- background info on the build-run process:

```md
After running cmake ., which generates the necessary build files (such as Makefiles), running make initiates the compilation process based on those generated build files.

Here's what happens in detail:

Dependency Check: make checks the dependencies of your project. It looks at the source files and header files to determine what needs to be compiled.

Compilation: It then compiles the necessary source files into object files (.o files).

Linking: Once all necessary source files have been compiled into object files, make links them together along with any required libraries to generate the final executable or library file.

Output: Finally, make produces the final executable or library specified in the CMakeLists.txt file or the default target if none is specified.

make is a tool that automates the building process based on instructions provided in the Makefile or CMakeLists.txt, which are generated by CMake based on your project configuration.
```

- ^so i'm not to compile source to object files (`.o`).
- i probably didn't generate the right build files, meaning bad CMakeLists.txt
- adding `set(CMAKE_CXX_STANDARD 14)` didn't work.
- ***might need compiler flags
- might have to check `include` paths to correct headers (dont think so though)
- try GUI again and figure out how to run it.

results:
- so i was able to 'build' with both the GUI and bash, but in either case there was no file in the `build_dir/bin`
- `ls -la` didnt help.


next steps:
- figure out why `bin` is empty and why the build seemed successful but didn't build the executable.

### progress sat march 30, 2024

- `bin` actually was probably empty because it takes `cmake .` and `make`/`make install` to actually install the binaries
- and `make` has errors i listed above.
- further research:

```
The errors you're encountering indicate that there are issues with the compilation of your source files due to problems with constexpr, uintptr_t, and other types. These errors suggest that the compiler is having trouble understanding or recognizing certain C++11 features or standard library types.

Here are a few steps you can take to resolve these errors:

Compiler Compatibility: Ensure that you're using a compiler that supports the C++11 standard or later. Some older compilers may not fully support features introduced in C++11, such as constexpr.

Include Paths: Verify that your project's include paths are correctly set up. It seems like your project is including headers from LLVM, so make sure the paths to LLVM headers are included properly in your CMakeLists.txt file.

CMake Configuration: Check your CMake configuration to ensure that the correct compiler flags and standards are being used. You might need to explicitly specify the C++ standard version (e.g., C++11, C++14, C++17) in your CMakeLists.txt file.

LLVM Installation: Make sure that LLVM is properly installed on your system and that the version you're using is compatible with your project's requirements.

Update LLVM: If you're using an older version of LLVM, consider updating to a newer version that may have better compatibility with modern C++ standards.

Compiler Options: If you're still encountering issues, you may need to adjust your compiler options or flags to ensure compatibility with the C++11 standard and LLVM headers.

Check Dependencies: Verify that all dependencies required by your project, including LLVM and any other libraries, are installed correctly and are compatible with each other.

By addressing these potential issues, you should be able to resolve the compilation errors and successfully build your LLVM project. If you're still having trouble, consider seeking assistance from the LLVM community or forums specific to your development environment.
```

- alright, that's extremely helpful^ knowing it's likely a c++ versioning error and not a llvm/clang version error.
- plus thats good because i havent studied c++ versioning yet.
- latest version of c++ is c++ 20. from 2020.
- my project is likely using c++ 11.

next steps: (only a small progress day, but it's fine)
- upgrade my program to c++








# DEADLINE: (updated) next FRIDAY Apr 5 I have to compile the simplest c++ program possible with LLVM
