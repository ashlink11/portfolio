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


# DEADLINE: (pushing this back a week) next FRIDAY March 29 I have to compile the simplest c++ program possible with LLVM

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










 



