# Guide_to_SYCL
## Intel Developer Cloud (IDC) Account
To gain access to a wealth of resources, discussions, and support related to Intel's oneAPI toolkit, you can create an Intel Developer Zone (IDZ) account using the attached documents:

Creating an IDC Account Guide: https://www.youtube.com/watch?v=PhzlMQ8-GE4&t=696s
## Purpose
The Jupyter Notebooks in this training shows challenges of heterogenous programming and how SYCL programming language can solve application development across CPUs, GPUs and FPGAs.

These training modules teach basics of SYCL programming to offload computation to GPUs and also goes deeper into SYCL concepts for optimization like Sub-Groups, Kernel Reductions, Buffer-Accessor memory model, pointer-based approach using Unified Shared Memory and Task scheduling.

Modules also teach usage of Intel oneAPI Data Parallel C++ Library to simplify heterogenous programming and tools usage. Debugger tools and Performance analysis tools like Intel VTune Profiler and Intel Advisor.

Also, it familiarizes you with the use of Jupyter notebooks as a front-end for all training exercises. This workshop is designed to be used on the DevCloud and includes details on submitting batch jobs on the DevCloud environment.

At the end of this course you will be able to:

Understand the challenges of Heterogenous Computing.
Write a SYCL program that offloads computation to accelerator devices like CPUs, GPUs or FPGAs from any vendor.
Perform analysis and profile the SYCL code using Intel oneAPI tools to find performance bottle necks.
License
Code samples are licensed under the MIT license. See License.txt for details.

Third party program Licenses can be found here: third-party-programs.txt

Content Details
Pre-requisites
C++ Programming
Training Modules
Modules	Description
oneAPI Introduction	+ Introduction and Motivation for SYCL.
+ SYCL Hello World
+ Compiling SYCL and DevCloud Usage
SYCL Program Structure	+ SYCL Classes - device, device_selector, queue, basic kernels and ND-Range kernels, Buffers-Accessor memory model
+ SYCL Code Anatomy
+ Implicit Dependency with Accessors, Synchronization with Host Accessor and Buffer Destruction
+ Creating Custom Device Selector
+ Lab Exercise: Vector Increment to Vector Add
SYCL Unified Shared Memory	+ What is Unified Shared Memory(USM) and Motivation
+ Implicit and Explicit USM code example
+ Handling data dependency using depends_on() and ordered queues
+ Lab Exercise: Unified Shared Memory
SYCL Sub Groups	+ What is Sub-Groups and Motivation
+ Querying for sub-group info
+ Sub-group shuffle algorithms
+ Sub-group group algorithms
+ Lab Exercise: Sub-Groups
SYCL Kernel Reductions	+ What are Reductions
+ Challenges with parallelizing reductions
+ sycl::reduce_over_group function for sub-groups and work-groups
+ sycl::reduction object in parallel_for
+ Lab Exercise: Kernel Reductions
SYCL Buffers and Accessors in depth	+ Buffers and Accessors
+ Buffer properties and usecases
+ Create Sub-buffers
+ Host accessors and usecases
+ Lab Exercise: Buffers and Accessors
SYCL Task Scheduling and Data Dependency	+ Different types of data dependencies
+ Execution of graph scheduling
+ modes of dependencies in Graphs scheduling
+ Lab Exercise: Task Scheduling
SYCL Local Memory And Atomics	+ Query Local memory type and size
+ Local memory and Group barriers
+ Local Accessor usage
+ Atomic Operations Buffers
+ Atomic Operations USM
+ Lab Exercise: Atomic Operation
Intel® oneAPI DPC++ Library (oneDPL)	+ Introduction to Intel oneAPI DPC++ Library (oneDPL)
+ Lab Exercise: Gamma Correction with oneDPL
Intel® Advisor	+ Offload Advisor Tool usage and command-line options
+ Lab Exercise: Generate Offload Advisor Report
+ Roofline Analysis and command-line options
+ Lab Exercise: Generate Roofline Report
Intel® VTune Profiler	+ Intel VTune™ Profiler usage in Intel DevCloud environment using command-line options
+ Lab Exercise: VTune Profiling by collecting gpu_hotspots for sample application.
Intel® Distribution for GDB on DevCloud	+ Use the Intel® Distribution for GDB to debug kernels running on GPUs.
Learn SYCL Programming
The modules listed above include Introduction to oneAPI, oneAPI Tools, SYCL Programming and Libraries. A sub-set of these modules that only focus on SYCL programming are listed below. Use these modules to just learn SYCL Programming Basics:

Modules	Skill Level	Description
SYCL Program Structure	basic	You will learn how to write a basic SYCL program that offloads computation to GPU
You will learn about SYCL Buffer Memory Model to manage data movement between host and device.
SYCL Unified Shared Memory	basic	You will learn how to write a basic SYCL prgram that uses Unified Shared Memory(USM) which is pointer-based memory model.
SYCL Sub Groups	intermediate	You will learn how to program to low-level hardware to take advantage of concurrent execution of parallel computation
SYCL Kernel Reductions	intermediate	You will learn how to write SYCL code to perform reductions effeciently on accelerator devices.
SYCL Buffers and Accessors in depth	intermediate	You will learn more advanced properties of buffer memory model.
SYCL Task Scheduling and Data Dependences	intermediate	You will learn how data movement can be controlled in SYCL programs when using Buffers and USM.
You will also lean about graph scheduling with buffers memory model
SYCL Local Memory and Atomics	intermediate	You will learn how to utilize device's Shared Local Memory to reduce latency in accessing data for kernel computation and Atomic operations to avoid data race conditions.
Content Structure
Each module folder has a Jupyter Notebook file (*.ipynb), this can be opened in Jupyter Lab to view the training contant, edit code and compile/run. Along with the Notebook file, there is a lab and a src folder with SYCL source code for samples used in the Notebook. The module folder also has run_*.sh files which can be used in shell terminal to compile and run each sample code.

Install Directions
The training content can be accessed locally on the computer after installing necessary tools, or you can directly access using Intel DevCloud without any installation.

