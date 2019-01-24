# Mutex and Channel basics

### What is an atomic operation?
indivisible operation, an operation that is not interruptable. Implemented using hardware instructions

### What is a semaphore?
 Integer flag with value always greater than or equal to 0. It lets you communicate resource availability between threads. (atomic)

### What is a mutex?
 Mutual exclusion. the only one using it can Signal() and "unlock" it. A concept of ownership

### What is the difference between a mutex and a binary semaphore?
 Mutex, da har brukeren eierskapet og bestemmer når han vil sette den fri. Binary semaphore kan kaste ut brukeren, for å la noen andre bruke den. men den sørger for at bare en bruker den om gangen.

### What is a critical section?
 Code where the resource is blocked.

### What is the difference between race conditions and data races?
Race conditions are when the result depends on the ordering in time.

 A data race happens when there are two memory accesses in a program where both:
- target the same location
- are performed concurrently by two threads
- are not reads
- are not synchronization operations

### List some advantages of using message passing over lock-based synchronization primitives.
> No need for mutex or semaphores because no shared resources. 

### List some advantages of using lock-based synchronization primitives over message passing.
> Doesn't need to think in another way then normal programming. 
