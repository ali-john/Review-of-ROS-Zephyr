# Review-of-ROS-Zephyr
----

![image](https://user-images.githubusercontent.com/63426759/200950292-e4ea2303-af2a-44a3-8be6-42a0c7e814b8.png)
  A real-time operating system (RTOS) is an operating system (OS) for real-time applications that processes data and events that have critically defined time constraints. A RTOS is distinct from a time-sharing operating system, such as Unix, which manages the sharing of system resources with a scheduler, data buffers, or fixed task prioritization in a multitasking or multiprogramming environment. Processing time requirements need to be fully understood and bound rather than just kept as a minimum. All processing must occur within the defined constraints. Real-time operating systems are event-driven and preemptive, meaning the OS is capable of monitoring the relevant priority of competing tasks, and make changes to the task priority. Event-driven systems switch between tasks based on their priorities, while time-sharing systems switch the task based on clock interrupts.
  
 A key characteristic of an RTOS is the level of its consistency concerning the amount of time it takes to accept and complete an application's task; the variability is 'jitter'. A 'hard' real-time operating system (hard RTOS) has less jitter than a 'soft' real-time operating system (soft RTOS). A late answer is a wrong answer in a hard RTOS while a late answer is acceptable in a soft RTOS. The chief design goal is not high throughput, but rather a guarantee of a soft or hard performance category. An RTOS that can usually or generally meet a deadline is a soft real-time OS, but if it can meet a deadline deterministically it is a hard real-time OS.
 
An RTOS has an advanced algorithm for scheduling. Scheduler flexibility enables a wider, computer-system orchestration of process priorities, but a real-time OS is more frequently dedicated to a narrow set of applications. Key factors in a real-time OS are minimal interrupt latency and minimal thread switching latency; a real-time OS is valued more for how quickly or how predictably it can respond than for the amount of work it can perform in a given period of time.

## Aspects of Study.
In this study, following aspects of Zephyr are studied:

  - OS structure
  - Kernel
  - Thread/Process Handling
  - Resource Management
  - File Systems
  - Booting
  - Security 
  - CPU Scheduling
  - Main Memory
----

## Advantages of Zephyr

  - Single Address Space

It creates a monolithic image that is loaded and executed on a system's hardware by combining application-specific code with a custom kernel. In a single shared address space, both application and kernel code run.

  - Highly configurable
  
It enables an application to include only the capabilities it requires at the time it requires them, as well as to specify the quantity and size of those capabilities.

  - Compile-time resource definition
  
It enables the definition of system resources at compile time, which reduces code size and improves performance.
 
 - Minimal error checking
 
 To reduce code size and improve performance, it provides minimal run-time error checking. To aid in debugging during application development, an optional error-checking infrastructure is provided.
 
 ----
 ## Zephyr Kernel
 
 ![image](https://user-images.githubusercontent.com/63426759/200951865-46ee8624-76e4-44a7-a3d3-5e4d9d435d78.png)
 
Spaces-Zephyr kernel has only one single address space, just a kernel space and no user space. It is highly configurable and not modular. Moreover, it is library based RTOS. There is only one executable that runs in a single address space. To dynamically load applications at run-time, no loader is required. The operating system code is kept to a bare minimum. Function calls are used to implement system calls. When calling an operating system call, no context switches are required. In this case, there is also a lack of security due to hardware memory separation. Threads are used to implement application and operating system calls in the same address space. Bugs in one part of the system can have a large impact on the entire system.

----

 
 
 
