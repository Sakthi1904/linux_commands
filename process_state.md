# Process Lifecycle States

## 1. New (Created)
- **Symbol:** 🆕 or NEW
- **Description:** The process is being created. It has not started running yet, and the operating system is setting up the necessary resources for it.
- **Transition:** From NEW → READY after initialization is complete.

## 2. Ready
- **Symbol:** 🟢 or READY
- **Description:** The process is ready to run but is waiting for CPU time. It is in the Ready Queue and can be scheduled for execution by the operating system.
- **Transition:** From READY → RUNNING when the scheduler assigns the CPU.

## 3. Running
- **Symbol:** 🟠 or RUNNING
- **Description:** The process is currently being executed by the CPU. The instructions of the process are being processed.
- **Transition:** From RUNNING → WAITING (if the process requires I/O or resources), or RUNNING → TERMINATED (if it completes or gets killed).

## 4. Waiting (Blocked)
- **Symbol:** 🔴 or WAITING / BLOCKED
- **Description:** The process is waiting for some event (like input/output operations to complete) or resource allocation (e.g., waiting for data from disk or network). It cannot continue executing until the event or resource becomes available.
- **Transition:** From WAITING → READY when the event or resource is available, and the process can continue execution.

## 5. Terminated (Exit)
- **Symbol:** ⚪ or TERMINATED / EXIT
- **Description:** The process has finished executing and is now terminated. Its memory and other resources are released by the operating system. The process no longer exists in the system.
- **Transition:** From RUNNING → TERMINATED after the process completes.

---

## Diagram of Process States

Here’s how the process states might look with transitions, represented with symbols:

```scss
🆕  -->  🟢  -->  🟠  -->  🔴  -->  ⚪
(New)    (Ready)   (Running)   (Waiting)   (Terminated)

    ↑                      ↓
  (Ready) ←---  (Waiting)
```


# Explanation of Transitions:

### New (🆕) → Ready (🟢):
- The process moves from the "New" state to the "Ready" state after it is initialized and is ready to run.

### Ready (🟢) → Running (🟠):
- The process in the Ready queue gets CPU time and starts executing.

### Running (🟠) → Waiting (🔴):
- If the process needs to wait for I/O (like reading data from a disk), it moves to the "Waiting" state.

### Waiting (🔴) → Ready (🟢):
- Once the I/O operation or event is completed, the process moves back to the Ready state to be scheduled again for execution.

### Running (🟠) → Terminated (⚪):
- After the process completes its execution, it moves to the "Terminated" state.

---

## Summary of States:

| State       | Symbol | Description                                              |
|-------------|--------|----------------------------------------------------------|
| New         | 🆕     | Process is being created, initializing resources.        |
| Ready       | 🟢     | Process is ready to execute, waiting for CPU.            |
| Running     | 🟠     | Process is currently being executed by the CPU.          |
| Waiting     | 🔴     | Process is waiting for an event/resource (e.g., I/O).     |
| Terminated  | ⚪     | Process has finished execution and is now terminated.    |

This is the lifecycle of a process in most operating systems, transitioning between these states based on what the process needs at a given moment.

Let me know if this clears things up!

---

## Steps in the Cycle (Explained with Transitions):

### New (🆕) → Ready (🟢):
- When a new process is created, it first enters the **New** state.
- The operating system initializes the process, and once it is ready to execute, it moves to the **Ready** state.

### Ready (🟢) → Running (🟠):
- Once the process is ready, it moves to the **Running** state when the OS scheduler gives it CPU time to execute.

### Running (🟠) → Waiting (🔴):
- If the process requires an external resource (e.g., waiting for data from disk or input from the user), it moves to the **Waiting** state.
- While waiting, the process is not using the CPU, so other processes can run.

### Waiting (🔴) → Ready (🟢):
- Once the event the process was waiting for is completed (e.g., I/O finishes), the process moves back to the **Ready** state, waiting for the CPU to be scheduled again.

### Running (🟠) → Terminated (⚪):
- When the process has completed its work or has been terminated by the OS or another process, it moves to the **Terminated** state.

---

## Key Points:

- **Ready state**: The process is waiting for CPU time.
- **Running state**: The process is actively executing.
- **Waiting state**: The process is paused because it's waiting for something (e.g., I/O).
- **Terminated state**: The process has completed its task or has been killed.

---

## Summary of the Process Cycle:

1. The process starts as **New**, is initialized, and moves to **Ready**.
2. The process waits in **Ready** until it gets CPU time and enters **Running**.
3. While running, the process may go to **Waiting** if it needs something (e.g., I/O).
4. Once the waiting condition is met, the process returns to **Ready** to be scheduled again.
5. The process eventually completes execution and enters **Terminated**.

---

## Example:

Let's say you have a program that processes files.

1. **New**: The program starts, and the OS creates a process for it.
2. **Ready**: The process waits in the Ready queue to get CPU time.
3. **Running**: The process starts reading files from disk.
4. **Waiting**: The process needs to wait for data to be read from the disk (it’s in the **Waiting** state).
5. **Ready**: Once the data is read, it goes back to the **Ready** state.
6. **Running**: The process continues execution.
7. **Terminated**: After finishing all the work, the process terminates.
