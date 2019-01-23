# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is concerned with managing access to shared state from different threads. Parallelism is concerned with utilizing multiple processors/cores to improve the performance of a computation. In other words; parallelism is when tasks literally run at the same time, like on a multicore processor. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Because of the stagnation of processor clock speed. With many application on the computer, the processor also became the bottleneck with only a single core. 
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > The use of concurrency in applications is generally motivated by performance gains. Concurrency can reduce latency (split a task into parts that can be executed concurrently), hide latency, and increase throughput (like the amount of data moved).
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It depends on the program. With shared variables and a lot of interweaving, a concurrent programming approach can be difficult, because of the resulting complexity due to a nondeterministic control flow. With no shared variables, concurrent programming can be a reasonable approach.  

 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Both processes and threads are independent sequences of execution. The difference is that threads run in shared memory space, while processes run in separate memory spaces. Green threads are "user-level threads". They are scheduled by an user-level process, not by the operating system. Used to simulate multi-threading on platforms that don't provide that capability. Coroutines are a general control structure whereby flow control is cooperatively passed between two different routines without returning.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > pthread_create() and `threading.Thread()` are used to create a new thread, while 'go' is a goroutine, which is a lightweight thread.
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It's a mechanism used to synchronize the execution of threads in python so that only one native thread can execute at a time. 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > multiprocessing module(?)
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The number of operating system threads that can execute user-level Go code simultaneously. The function queries and changes the limit.
