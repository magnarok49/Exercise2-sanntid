# Mutex and Channel basics

### What is an atomic operation?
> *The 'smallest operation' a system can do, one that brings the system from one definitive state to another.*
> *Typically a single RISC operation.* 
> *This operation appears indivisible to other processes, ensuring that it is not interrupted half-way. *

### What is a semaphore?
> *A flag symbolizing that a resource is busy, *
> *threads requiring a resource will have to wait for this flag to be lowered, *
> *then seize it for themselves, before continueing.*
> *Semaphores can have an arbitrary value, and any process can increment/decrement it.*

### What is a mutex?
> *A semaphore, specialized for mutually exclusive cases.*
> *Typically also keeps track of who has the resource at this moment, and thus who is allowed to release it.*

### What is the difference between a mutex and a binary semaphore?
> *Semaphores are essentially just variables, whereas mutex's are binary flags.*
> *Thus semaphores can handle an arbitrary amount of a resource available,*
> *where mutex's handle only a single resource, that can only be handled by a single actor at one time.*
> *Mutexes can also provide control to ensure that only a thread which has the resource is allowed to release it.*

### What is a critical section?
> *Some part of a program which accesses shared resources, IE, where one might need semaphores/mutex's.*
> *Consequentially, this is the part of the program where a thread might interfere with other threads.*

### What is the difference between race conditions and data races?
 > *Race condition is some aspect of a program where timing affects the outcome of the program.*
 > *IE non-deterministic shit*
 > *A data-race is a setting where 2 or more threads/concurrent processes attempt to access the same memory,*
 > *where both are not reads.* 

### List some advantages of using message passing over lock-based synchronization primitives.
> *Avoid deadlocks, where several threads are waiting for resources which others control.*
> *Avoid locking in general, threads can do other stuff while waiting for a resource. *
> *Scalability, since messages are sent asynchronously, one can easily increase the amount of threads, without increasing complexity too much.*

### List some advantages of using lock-based synchronization primitives over message passing.
> *Simplicity, threads do not necessarily need to be aware of eachother.*
