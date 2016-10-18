Mason Ellis

CMPS 4103 - Operating Systems

Dr. Griffin

10/18/2016

#Test #1 Extra Credit

###Multi*
  1. Multi-tasking: When the computer performs context switches so fast that it seems to be running programs concurrently. 
    
        Example: The scheduler will handle multiple programs by running them all in pieces. This occurs so quickly
        that it seems like these programs are running at the same time. 
  
  2. Multi-programming: Only one program is able to execute instructions on the CPU at a time. Multi-programming is the idea of maximizing the use of the CPU and minimizing CPU idle time. 
    
        Example:  When there are multiple user programs loaded into memory, and the operating system kicks the a 
        program off of the CPU whenever it is waiting on I/O. Thus, CPU down time is minimized and the CPU is used 
        as much as possible. 
        
  3. Multi-processing: When the underlying hardware provides more than one processor or multiple cores. 
  
        Example: Utilizing Dual and Quad core processors. 
        
  4. Multi-threaded: An execution model that allows a single process to have multiple code segments run concurrently 
     within the "context" of that process. 
     
        Example: A database server that listens for and processes numerous client requests. 
        
###Review Questions From Chapter 3
  1. What is an instruction trace?
  
        A listing of the sequence of instructions that execute for a process. This allows us to characterize the 
        behavior of a process. We can also use an instruction trace to see when the process will need to wait for 
        I/O. This will help schedule the processes that are in memory. 
        
  2. What common events lead to the creation of a process?
  
        New Batch Job, Interactive log-on, created by the OS to provide a service, Spawned by existing process. 
  
  3. What does it mean to preempt a process?
  
        To preempt a process is to interrupt said process so that a process of higher priority can use the CPU.
  
  4. What is swapping and what is its purpose?
  
        Swapping is when the operating system takes part or all of a process out of main memory and places it 
        in virtual memory. This serves to allow other processes in memory. If we can place processes that have 
        a lower wait time on memory, we will reduce the idle time of the CPU. 
  
  5. Why does Figure 3.9b have two blocked states?
  
        There are two blocked states: blocked and blocked/suspended. In the blocked state, the process has beed
        taken off of the CPU because it is waiting for an event (I/O for example) but still resides in main
        memory. In the blocked/suspended state, the processes is still waiting for an event, but resides in
        virtual memory instead of main memory. Suspended means that the process has been swapped out of RAM. 
  
  6. List four characteristics of a suspended process.
      1. The process is not immediately available for execution. 
      2. The process may or may not be waiting on an event. If it is, this blocked condition is independent of 
      the suspend condition, and occurrence of the blocking event does not enable the process to be executed immediately.
      3. The process was placed in a suspended state by an agent: either itself, a parent process, or the OS, for the 
      purpose of preventing its execution.
      4. The process may not be removed from this state until the agent explicitly orders the removal.
      
  7. List three general categories of information in a process control block.
      1. Process identification
      2. Prcessor State Information
      3. Process Control Information
      
  8. Why are two modes (user and kernel) needed?
  
        It is necessary to protect the OS and key operating system tables, such as process control blocks, from 
        interference by user programs. In the kernel mode, the software has complete control of the processor and 
        all its instructions, registers, and memory. This level of control is not necessary and for safety is not 
        desirable for user programs.
  
  9. What is the difference between an interrupt and a trap?
  
        An interrupt comes from outside the process, and a trap is associated with the execution of the current 
        instruction.  
  
  10. Give three examples of an interrupt.
      1. Clock Interrupt
      2. I/O Interrupt
      3. Memory Fault
      
  11. What is the difference between a mode switch and a process switch?
  
        A mode switch may occur without changing the state of the process that is currently in the Running state.
