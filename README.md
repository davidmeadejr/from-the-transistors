
# From Transistor to Web Browser: 

**Course Objective**: Gain a deep understanding of the modern computer stack by building components from first principles, progressing from transistor-level concepts to software like an operating system and a web browser. By the end, you will have created a working virtual computer system with an OS, networking capabilities, and a basic browser.

**Prerequisites**: Basic programming in Python or C, familiarity with digital logic, and general understanding of computer architecture concepts.

---

## Section 1: Intro — Understanding the Basics of Hardware Design and Emulation

### Goals
1. **Concepts**: Overview of transistors, Field-Programmable Gate Arrays (FPGAs), and Integrated Circuits (ICs).
2. **Look-Up Tables (LUTs)**: Understand how FPGAs use LUTs to simulate logic gates.
3. **Hardware Emulation**: Learn the advantages and limitations of emulation using software (Verilator) versus real hardware.

### Projects
- [ ] **Set up Verilator**: Configure your environment for hardware simulation, allowing you to emulate FPGA components on your computer.
- [ ] **Transistor Theory**: Briefly explore how ICs and FPGAs are built on collections of transistors but recognize that this course will build on software simulations for accessibility.

---

## Section 2: Bringup — Coding Hardware in Verilog

### Goals
1. **Programming in Verilog**: Start coding hardware by writing simple modules.
2. **UART and MMIO**: Gain an understanding of memory-mapped input/output and serial communication.

### Projects
- [ ] **LED Blinker (Verilog, 10 LOC)**: Write a Verilog program to simulate an LED blinking.
- [ ] **UART Implementation (Verilog, 100 LOC)**: Implement a simple UART model and learn to communicate with hardware. Write a test echo program and an LED control program via UART.

---

## Section 3: Processor — Building a Basic ARM CPU

### Goals
1. **ARM Assembly and CPU Construction**: Learn assembly language while building a simple ARM7 processor.
2. **Assembler in Python**: Write an assembler for ARM instructions as you build the CPU in Verilog.
3. **Bootrom**: Enable code downloads over serial.

### Projects
- [ ] **Assembler (Python, 500 LOC)**: Write an assembler that converts ARM assembly to binary, forming the basis for assembling code to run on your CPU.
- [ ] **ARM7 CPU (Verilog, 1500 LOC)**: Build a basic ARM7 CPU in Verilog with fetch, decode, and execute stages.
- [ ] **Bootrom (Assembly, 40 LOC)**: Write a bootrom that enables loading code via the serial port into RAM.

---

## Section 4: Compiler — Creating a High-Level Language Compiler

### Goals
1. **C Compiler**: Build a simple C compiler in Haskell, introducing parsing and code generation concepts.
2. **Linker in Python**: Enable your compiler to output executable files that run on your CPU.
3. **libc Implementation**: Start implementing essential functions for C programs.

### Projects
- [ ] **C Compiler (Haskell, 2000 LOC)**: Develop a basic C compiler that translates C code into ARM assembly. Cover parsing, semantic analysis, and assembly generation.
- [ ] **Linker (Python, 300 LOC)**: Write a linker that generates ELF files, executable in the simulated environment.
- [ ] **libc (C, 500 LOC)**: Implement core functions (e.g., `memcpy`, `memset`, `printf`) necessary for C programming.
- [ ] **Ethernet Controller (Verilog, 200 LOC)**: Create a Verilog model of an Ethernet controller, introducing networking.

---

## Section 5: Operating System — Building a UNIX-Like OS

### Goals
1. **MMU in Verilog**: Construct a Memory Management Unit, enabling memory protection.
2. **UNIX-like Kernel**: Build a kernel with essential system calls and a file system.
3. **SD Card Driver**: Add an interface to communicate with storage.

### Projects
- [ ] **MMU (Verilog, 1000 LOC)**: Implement a simple MMU with Translation Lookaside Buffers (TLBs).
- [ ] **Operating System (C, 2500 LOC)**: Develop a UNIX-like OS with basic system calls (open, read, write, fork, exec, wait, mmap, etc.).
- [ ] **SD Card Communication (Verilog, 150 LOC)**: Write Verilog code for SD card communication and create a corresponding C driver.
- [ ] **FAT Filesystem (C, 300 LOC)**: Implement the FAT file system to read and write files.
- [ ] **User Programs (C, 250 LOC)**: Write initial user-space applications (e.g., `init`, `shell`, `cat`, `ls`).

---

## Section 6: Browser — Adding Networking and a Basic Browser

### Goals
1. **Networking Stack**: Implement a simple TCP/IP stack to support basic communication.
2. **Dynamic Linking**: Add support for dynamic linking to handle shared libraries.
3. **Text-Based Web Browser**: Develop a basic text-based browser that can interpret web content.

### Projects
- [ ] **TCP Stack (C, 500 LOC)**: Code a TCP/IP stack in the kernel, supporting `send`, `recv`, `bind`, and `connect`.
- [ ] **Telnet Daemon (C, 50 LOC)**: Build a simple telnet server to allow remote connections, demonstrating multiprocessing.
- [ ] **Dynamic Linking (C, 300 LOC)**: Implement dynamic linking to support shared libraries, optimizing memory usage.
- [ ] **Web Browser (C, 500 LOC)**: Build a minimalistic, text-based browser capable of handling basic ANSI terminal commands.

---

## Section 7: Physical Layer — Preparing for Real Hardware

### Goals
1. **FPGA Communication**: Learn to program and communicate with an FPGA via USB.
2. **Board Design**: Design a basic FPGA development board.

### Projects
- [ ] **USB to FPGA Communication (C, 200 LOC)**: Write code to control an FPGA using USB for JTAG and UART communication.
- [ ] **FPGA Board Design**: Design and build an FPGA board with essential components, such as LEDs, a reset button, USB-JTAG, and a serial interface.
