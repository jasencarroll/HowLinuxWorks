# How Linux Work - The Big Picture

Abstractation is the concept of breaking something complicated overbearing to try and understand, into parts that are manageable for understanding.

Personally I am not willing to say I understand a system until I can see how the abstractations interact with each other. This really resonates with me as when I'm learning different things it feels very fragmented like I am tearing down bits and pieces until I can see a bigger picture of what is going on.

Do I always learn in abstractations and systems thinking?

## 1.1 Levels and Layers of Abstraction in Linux (while being on Linux)

Astractation doesn't work without organization. The way they are organized is by layers such as top layer (user interaction) and bottom layer (computer interaction, 1s and 0s), and plenty inbetween.

Linux systems have three main layers, user processes, Linux kernel, and hardware. The base is hardware and I know hardware. Kernal is next and it is the core of the operating system, the software residing in memory that tells the CPY where to look for its next instruction. The kernel manages the hardware and interfaces with any running programs. That's why you don't want a kernel panic! Processes are last, also known as user space.

Code associated with the kernel (i.e. running in kernel mode) has unrestricted access to the processor and main memory. This starts to explain how Linux is so powerful yet so volatile, having crashed a few systems myself. There is reserved memory area only the kernal can access which is called kernal space.

User mode is quite restrictive in comparison. In this space if a process makes a mistake and crashes, the kernal can recover. For example, if you're doing a lot of work and having a scientific computation running for a few days and your web browser allowing you to see the computation running crashes - your computation would continue running while the web browser is retored.

## 1.2 Hardware: Understanding Main Memory

