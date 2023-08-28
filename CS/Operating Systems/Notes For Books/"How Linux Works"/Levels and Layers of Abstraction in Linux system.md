> A layer or level is a classification (or grouping) of a component according to where that component sits between the user and the hardware.

#### A Linux System has 3 main levels of Abstraction 
- User Process 
- Linux Kernel 
- Hardware 
![[Screenshot from 2023-08-28 15-27-13.png]]

The **Hardware** is the base. It includes the memory as well as one or more central processing units (CPUs) to perform computation and to read from and write to memory. Devices such as disks and network interfaces are also part of the hardware.

The next level is the **kernel**, which is the core of the operating system. The kernel is software residing in memory that tells the CPU what to do. The kernel manages the hardware and acts primarily as an interface between the hardware and any running program.

**Porcesses** - the running programs that the kernel manages - collectively make up the systems's upper level, called **user space**. 

> The Kernel runs in **kernel mode** and the user processes run in **user mode**. Code running in kernel mode has unrestricted access to the processor and main memory. This is a powerful but dangerous privilege that allows a kernel process to easily
   crash the entire system. The area that only the kernel can access is called **kernel space**.

