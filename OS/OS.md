# Process
Process is a program in execution
The first thing that the OS must do to run a program is to load its code and any static data into memory
OS allocates resources, adresss space for process (stack memory & heap memory) 
CPU start executing instruction by loading instruction from RAM to register

1.Created 2.Running 3.Waiting 4.Ready 5.Terminated

2 ways to communicate: Shared memory or Message Passing

# Threads
- Thread is basic unit of execution within a process
- A process can have many threads
- Have their own stack, state, register, program counter

# Compare
All threads in a process share the same adress space of a process

Create/Communicate between/ threads is expensive

1 process per core

Even a computer with one CPU core can "simultaneously" support dozens or hundreds of threads. But we all [should] know that this is merely a trick by the operating system though the magic of time-slicing. In reality, that single core can only execute one thread at a time; then the OS switches contexts and that core executes code for another thread, and so on. It is a basic Law of Computing that given a single CPU resource, executing A and B sequentially will always be faster than executing A and B "simultaneously" through time-slicing. Once the number of threads exceeds the number of CPU cores, you're going slower by adding more threads, not faster.

Multiprocessing are classified according to the way their memory is organized.
Multiprocessing improves the reliability of the system
Multiprocessing can improve performance by decomposing a program into parallel executable tasks.
The code is usually straightforward.
Takes advantage of multiple CPU & cores

In the multithreading process, each thread runs parallel to each other.
Threads do not allow you to separate the memory area. Therefore it saves memory and offers a better application performance
