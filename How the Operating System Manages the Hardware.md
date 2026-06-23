
The operating system can be thought of as a layer of software interposed between application programs and hardware.
All application programs must go through the OS before affecting the hardware devices

![[image 3.png]]


As this figure suggests, flies are abstractions for I/O devices, virtual memory is an abstraction for both the main memory and disk I/O devices, and processes are abstractions for the processor, main memory, and I/O devices. We will discuss each in turn.

1. **Processes:**
A single CPU can do only one thing at a time. But the operating system uses <span style="color:rgb(231, 24, 176)">context switching</span> to switch between programs and give the illusion that there are multiple programs running together.

![[image-1.png|Context Switching]]

As the above figure indicates, <span style="color:rgb(231, 24, 176)">the transition from one process to another is managed by the operating system kernel</span>. The kernel is the portion of the operating system code that is always resident in memory. When an application program requires some action by the operating system, such as to read or write a file, it executes a special system call instruction, transferring control to the kernel. The kernel then performs the requested operation and returns back to the application program. Note that the kernel is not a separate process. Instead, it is a collection of code and data structures that the system uses to manage all the processes. 

<span style="color:rgb(231, 24, 176)">In modern systems a process can actually consist of multiple execution units, called threads, each running in the context of the process and sharing the same code and global data.</span>
Multi-threading is also another way to make programs run faster when multiple processors are available.


2. **Virtual Memory**

Virtual memory is the abstraction that provides each process with the illusion that it has exclusive access over memory.

![[image-2.png|697]]


This illusion is created thorough dynamic memory allocation through the heap and stack etc.


3. **Files**

A file is a sequence of bytes.

<span style="color:rgb(231, 24, 176)">Every I/O device, including disks, keyboards, displays, and even networks, is modeled as a file.</span>

All input and output in the system is performed by reading and writing files, using a small set of system calls known as Unix I/O. 

This simple and elegant notion of a file is nonetheless very powerful because it provides applications with a uniform view of all the varied I/O devices that might be contained in the system.



