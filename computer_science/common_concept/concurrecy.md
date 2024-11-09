# Concurrency

## CPU Scheduling

CPU scheduling divides into two primary approaches

- Preemptive Scheduling. Current running process is halted after some time and jumps to another process waiting in the queue.
- Cooperative Scheduling. Runs current running process until it is terminated or reaches a waiting state, then jumps to another process.

In OS threading, Preemptive Scheduling is utilized with the advantages of reduced response time, even distribution, and reliability.

## OS Thread and Green Thread

- OS thread. Thread provided by the OS (when we speak of thread, we usually mean OS thread). Each process is assigned a stack and rest (code, data, heap) are shared. Context switching involves the kernel, thus overhead is relatively larger.
- Green thread. User-level thread, e.g., goroutine, tokio. Memory, including stack, are shared and stack isolation is managed by runtime. Context switching doesn't involve the kernel, posing lighter overhead.

OS thread and Green thread uses M:N matching.

- Blocking
- Non-blocking
- Sync
- Async

## Scheduler

### Task handling process

- CPU intensive task
- I/O intensive task

### Task distribution

- Round Robin
- Work Stealing

[reference]

- [[1]](https://velog.io/@pandawithcat/RUST-%EB%A1%9C-%EA%B3%B5%EB%B6%80%ED%95%98%EB%8A%94-%EB%B9%84%EB%8F%99%EA%B8%B0-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-1#concurrency-vs-parallelism)
- [[2]](https://www.geeksforgeeks.org/preemptive-and-non-preemptive-scheduling/)
- [[3]](https://stackoverflow.com/questions/5713142/green-threads-vs-non-green-threads)
