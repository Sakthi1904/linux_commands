# Process Control Block (PCB)

A **Process Control Block (PCB)** is a data structure used by the operating system to store information about each process during its execution.

## PCB Structure

| **Component**            | **Description**                  |
|--------------------------|----------------------------------|
| **Process ID (PID)**     | `<PID value>`                    |
| **Process State**        | `Running / Ready / Waiting`      |
| **Program Counter (PC)** | `<address>`                      |
| **CPU Registers**        | `<register values>`              |
| **Memory Management Info**| `<memory locations>`            |
| **Scheduling Info**      | `<priority, queue>`              |
| **I/O Status Information**| `<open files, devices>`         |
| **Process Privileges**   | `<access rights>`                |
| **Parent/Child Pointers**| `<parent/child IDs>`            |
| **Exit Status**          | `<success/failure>`              |




## Explanation of Fields:

1. **Process ID (PID)**: A unique identifier for the process.
2. **Process State**: The current state of the process (e.g., Running, Ready, Waiting).
3. **Program Counter (PC)**: The address of the next instruction to be executed.
4. **CPU Registers**: The saved values of the CPU registers when the process is not running.
5. **Memory Management Info**: Information about the memory location the process is using.
6. **Scheduling Info**: Information about the process's scheduling, like priority or queue.
7. **I/O Status Information**: Information about the input/output devices the process is using.
8. **Process Privileges**: The access rights and permissions of the process.
9. **Parent/Child Pointers**: Information about the parent and child process relationships.
10. **Exit Status**: The exit status of the process when it terminates (success or failure).

---


# Process Control Block (PCB)

A **Process Control Block (PCB)** is a data structure used by the operating system to store information about a process. It acts as a repository for all the essential information required by the OS to manage and control processes during their execution. Each process has its own PCB, and it is created when the process is initialized and destroyed when the process terminates.

## Key Components of a Process Control Block (PCB):

1. **Process ID (PID)**:  
   - A unique identifier for the process.

2. **Process State**:  
   - Indicates the current state of the process (e.g., **new**, **ready**, **running**, **waiting**, **terminated**).

3. **Program Counter (PC)**:  
   - Holds the address of the next instruction to be executed by the process.

4. **CPU Registers**:  
   - Stores the values of various registers (such as accumulator, data register, etc.) for the process when it is not executing. These are needed to resume the process after a context switch.

5. **Memory Management Information**:  
   - Information related to the process’s memory, such as base and limit registers or pointers to the process’s page tables.

6. **Scheduling Information**:  
   - Includes priority, scheduling queues, and other information relevant to the scheduling of the process.

7. **I/O Status Information**:  
   - Information about I/O devices allocated to the process, such as open files or devices in use.

8. **Accounting Information**:  
   - Data for tracking resource usage, such as CPU time used, memory usage, and other statistics relevant for process management.

9. **Pointer to Parent/Child Process**:  
   - Links to the parent and/or child processes (in case of process creation or termination).

The PCB helps the operating system manage processes effectively, especially when switching between them (context switching). When a process is interrupted or switched out of the CPU, the PCB is saved so that the process can resume where it left off when it is scheduled to run again.


