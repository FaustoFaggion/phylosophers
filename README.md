# 42SP - Philosophers

This project was create to teach the basics of threading a process.

## What is a Thread?
A thread is an execution context, which is all the information a CPU needs to execute a stream of instructions. A process can contain multiple threads.

## Thread X Process
A program under execution is known as a process and a thread is a basic unit execution. Thread is a basic unit of CPU utilization.

### Threads

Threads Comprises:
- A Thread ID
- A Program counter
- A register set
- A stack
Threads share with other threads belonging to the same process the follow resources:
- Code section
- Data section
- Open files
- Signals
Share the same resources the was allocated to the process by the Operate System.

### Process

- Run independily from others process
  - Have independent memory space
  - When create a process, the parent variables are duplicated for the child process.
  - Changes in variables on the parent process don't afect the variables in the child process.
- File handlers are duplicated.

### Advantages

- Responsiveness > May allow a program to continue running even if part of if is blocked or is performing a lengthy operation, therreby increasing responsiveness to the user.
- Resource Sharing > Allows several different threads to share the same adress space, making the process more economic. Create resources for process it is costly.
- Utilization of Multiprocessor Architecture > Where threads can be running parallel on different processors, making a multithread process run tasks in parallel. A single thread process can run only on one CPU no matter how many CPUs are avaiable.

### Thread execution:

- Read the data in your own register.
- Apply a function required using the data saved in his register.
- Return the result to the data in memory.

## Types of Threads

- User Threads > Supported above the kernel and are managed whitout kernel support.
- Kernel Threads > Supported an manage directly by the operating system.

### Relationship User x Kernel Threads

- Many to One

<img width=1800 src="./readme/many_to_one_thread.png">

- One to One
 
<img width=1800 src="./readme/one_to_one_thread.png">

- Many to Many > Best solution(most used model)

<img width=1800 src="./readme/many_to_many_thread.png">

### Race Condition

A situation where several threads access and manipulate the same data concurrently and the outcome of the execution depends on the particular order in which the access takes place.

[Race Condition(process syncronization)](https://www.youtube.com/watch?v=ph2awKa8r5Y&list=PLBlnK6fEyqRiVhbXDGLXDk_OQAeuVcp2O&index=56)

### Critical Section

Is a section in which the process may be changing commom data, writing commom files and so on.
When one process is executing in its critical section, no other process is to be allowe to execute in its critical section.

[Critical Section](https://www.youtube.com/watch?v=UtEORPakw5Y&list=PLBlnK6fEyqRiVhbXDGLXDk_OQAeuVcp2O&index=58)


### Paralelism

Threads runing simultaniously in different cores. It just can happen if there is a multi core processor.

### Links

README:

[Tutorial README](https://www.youtube.com/watch?v=eJojC3lSkwg)

Makefile:

[Tutorial Makefile](https://www.youtube.com/watch?v=GExnnTaBELk)

Threads:

[Introdution to Threads](https://www.youtube.com/watch?v=LOfGJcVnvAk&list=PLBlnK6fEyqRiVhbXDGLXDk_OQAeuVcp2O&index=31)

[Multithreading Models](https://www.youtube.com/watch?v=HW2Wcx-ktsc&list=PLBlnK6fEyqRiVhbXDGLXDk_OQAeuVcp2O&index=32)

[Waht is a Thread](https://www.geeksforgeeks.org/thread-in-operating-system/)

[Compiling threads](https://www.youtube.com/watch?v=j9csJohayPU)

[Code Valt - threads](https://www.youtube.com/playlist?list=PLfqABt5AS4FmuQf70psXrsMLEDQXNkLq2)