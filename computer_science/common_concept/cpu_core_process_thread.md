# Core vs Process vs Thread

- Core. A physical unit that can execute instructions. By default, a core can run a single thread at a time (Intel's hyperthreading enable running 2 threads but recent Intel CPU have removed it)
- Process. An instance of running program. Each process are isolated from others, to share data between process, IPC is utilized.
- Thread. Single sequence of execution within a process. Threads share code, data, heap, though stack is isolated between threads.
