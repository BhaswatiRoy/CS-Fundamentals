## Types of OS

- Batch OS - batches of similar jobs are created and executed one by one
- Multitasking OS - specific time is given to any process
- Distributed OS - machines connected via networks and located in diff geographical locs 
- Real time OS - live working and time is imp factor - hard & soft types
- Clustered OS - similar to distributed but all machines under same cluster

## Kernel vs Monolithic Kernel vs Sockets

- Kernel = heart of OS, helps us to directly communicate with the OS and perform tasks in kernel modes by help of system calls
- Monolithic Kernel = all OS tasks are performed in kernel mode only
- Sockets = serves as endpoints in networks to perform tasks like sending & receiving data all across the network

## Process vs Threads

process - heavy weight tasks, system calls involved, entire copy of process created, context switching is slower, blocking 1 process dont affect others

threads - light weight tasks, no system calls, no copy only extra threads, context switching faster, blocking 1 process affects others

## Types of Processes

1. I/O Bound - input output
2. CPI Bound - CPU work based

## Virtual Memory

- To scale our systems we use an extra memory of a hard disk which enables programs to run which are greater than physical memory creating an illusion of extra space.
- Concept used in virtualization and cloud computing

## Thrashing

Degree of multiprogramming increased but entire memory is not utilized properly

## RAID

Redundant array of independent disks - making use of multiple disks to improve performance

## Deadlocks

Cyclic wait where all processes waits for resources which are assigned to other processes

Conditions -
- Mutual Exclusion - no 2 processess stay in critical section at same time
- Hold & Wait - holding 1 and waiting for 1
- No Preemption - process that can go to wait state before finishing are preemptive process
- Circular Wait - in resource allocation graph (RAG)

## Fragmentation 

Has space in memory but can't allocate processes

1. Internal - memory blocks of fixed size
2. External - memory blocks of diff side

## Spooling 

Data is temporarily held in memory for some work. Eg - printing

## Semaphore & Mutex

Semaphores = integer value used in mutual exclusion manner by different concurrent processes to achieve synchronization.
- Counting Semaphore - value range is -infinity to +infinity
- Binary Semaphore - value range is -1 to +1

## Belady's Anomaly

Increase in no of frames lead to increase in page faults whereas theoritically it shouldn't be true

## Starvation 
- Low priority processes keep waiting and high priority ones keep processing. 
- To solve this we use Aging which means too old processes get executed even if low priority.

## Thrashing 

Too high degree of multiprogramming causes too many page faults sometimes.

## Demand paging 

Bring pages to main memory only if there is demand.

## Binding 

Assigning value to variables

- Static binding - occurs during compile time
- Dynamic binding - occurs during run time

## Bankers algo 

Resource allocation method for deadlock avoidance

## Multiprogramming vs Multitasking

Multitasking - process waits for I/O
Multiprogramming - doesn't wait for I/O


