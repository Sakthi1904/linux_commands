| Signal Number | Signal Name     | Full Form                 | Explanation                                                                 | Syntax Example                              |
|---------------|-----------------|---------------------------|-----------------------------------------------------------------------------|---------------------------------------------|
| 1             | SIGHUP          | Hangup                    | Indicates that the terminal or controlling process has disconnected. Often used to reload configurations. | `kill -SIGHUP <pid>`                        |
| 2             | SIGINT          | Interrupt                 | Interrupts the process, often triggered by Ctrl+C in the terminal.          | `kill -SIGINT <pid>`                        |
| 3             | SIGQUIT         | Quit                      | Similar to SIGINT but causes a core dump for debugging.                      | `kill -SIGQUIT <pid>`                       |
| 4             | SIGILL          | Illegal Instruction       | Sent when a process tries to execute an illegal machine instruction.         | `kill -SIGILL <pid>`                        |
| 5             | SIGTRAP         | Trap                      | Sent by the process when it hits a breakpoint or other trap condition.      | `kill -SIGTRAP <pid>`                       |
| 6             | SIGABRT         | Abort                     | Sent by the process to abort itself (usually due to a fatal error).         | `kill -SIGABRT <pid>`                       |
| 7             | SIGBUS          | Bus Error                 | Sent when a process causes a bus error (e.g., accessing invalid memory).    | `kill -SIGBUS <pid>`                        |
| 8             | SIGFPE          | Floating Point Exception  | Sent when a process encounters a floating point error (e.g., division by zero). | `kill -SIGFPE <pid>`                        |
| 9             | SIGKILL         | Kill                      | Immediately terminates the process without giving it a chance to clean up. This signal cannot be caught. | `kill -9 <pid>`                             |
| 10            | SIGUSR1         | User-defined Signal 1     | Used by applications to implement custom actions.                           | `kill -SIGUSR1 <pid>`                       |
| 11            | SIGSEGV         | Segmentation Violation    | Indicates that a process has attempted to access restricted memory.        | `kill -SIGSEGV <pid>`                       |
| 12            | SIGUSR2         | User-defined Signal 2     | Another user-defined signal for custom actions.                             | `kill -SIGUSR2 <pid>`                       |
| 13            | SIGPIPE         | Broken Pipe               | Sent when a process writes to a pipe with no readers, usually causing it to terminate. | `kill -SIGPIPE <pid>`                       |
| 14            | SIGALRM         | Alarm                     | Sent when a timer set by the alarm() system call expires.                   | `kill -SIGALRM <pid>`                       |
| 15            | SIGTERM         | Terminate                 | Requests a process to terminate gracefully, allowing cleanup.              | `kill -SIGTERM <pid>`                       |
| 17            | SIGCHLD         | Child Status Change       | Sent to a parent process when a child process terminates or stops.          | `kill -SIGCHLD <pid>`                       |
| 18            | SIGCONT         | Continue                  | Resumes a paused process.                                                  | `kill -SIGCONT <pid>`                       |
| 19            | SIGSTOP         | Stop                      | Pauses a process; it cannot be ignored or caught.                           | `kill -SIGSTOP <pid>`                       |
| 20            | SIGTSTP         | Terminal Stop             | Pauses the process, typically sent by pressing Ctrl+Z in the terminal.      | `kill -SIGTSTP <pid>`                       |
| 21            | SIGTTIN         | Background read from tty  | Sent to a process that tries to read from the terminal while in the background. | `kill -SIGTTIN <pid>`                       |
| 22            | SIGTTOU         | Background write to tty   | Sent to a process that tries to write to the terminal while in the background. | `kill -SIGTTOU <pid>`                       |
| 23            | SIGURG          | Urgent I/O condition      | Sent when there is urgent or out-of-band data to be processed by the process. | `kill -SIGURG <pid>`                        |
| 24            | SIGXCPU         | CPU Time Limit Exceeded   | Sent when a process exceeds its CPU time limit.                             | `kill -SIGXCPU <pid>`                       |
| 25            | SIGXFSZ         | File Size Limit Exceeded | Sent when a process exceeds its file size limit.                           | `kill -SIGXFSZ <pid>`                       |
| 26            | SIGVTALRM       | Virtual Timer Alarm       | Sent when a virtual timer expires (used for profiling or real-time tasks). | `kill -SIGVTALRM <pid>`                     |
| 27            | SIGPROF         | Profiling Timer Alarm     | Sent when a profiling timer expires (used for CPU profiling).              | `kill -SIGPROF <pid>`                       |
| 28            | SIGWINCH        | Window Change             | Sent when the size of the terminal window changes.                          | `kill -SIGWINCH <pid>`                      |
| 29            | SIGIO           | I/O Pending               | Sent when an I/O operation becomes available on a file descriptor.         | `kill -SIGIO <pid>`                         |
| 30            | SIGPWR          | Power Fail                | Sent when there is a power failure or when the system detects a power-related issue. | `kill -SIGPWR <pid>`                       |
| 31            | SIGSYS          | Bad System Call           | Sent when a process makes an invalid system call.                           | `kill -SIGSYS <pid>`                        |
| 34            | SIGRTMIN        | Real-time Signal Minimum  | The lowest real-time signal, used for real-time applications.               | `kill -SIGRTMIN <pid>`                      |
| 35            | SIGRTMIN+1      | Real-time Signal          | Real-time signal 1, used for real-time applications.                       | `kill -SIGRTMIN+1 <pid>`                    |
| 36            | SIGRTMIN+2      | Real-time Signal          | Real-time signal 2, used for real-time applications.                       | `kill -SIGRTMIN+2 <pid>`                    |
| 37            | SIGRTMIN+3      | Real-time Signal          | Real-time signal 3, used for real-time applications.                       | `kill -SIGRTMIN+3 <pid>`                    |
| 38            | SIGRTMIN+4      | Real-time Signal          | Real-time signal 4, used for real-time applications.                       | `kill -SIGRTMIN+4 <pid>`                    |
| 39            | SIGRTMIN+5      | Real-time Signal          | Real-time signal 5, used for real-time applications.                       | `kill -SIGRTMIN+5 <pid>`                    |
| 40            | SIGRTMIN+6      | Real-time Signal          | Real-time signal 6, used for real-time applications.                       | `kill -SIGRTMIN+6 <pid>`                    |
| 41            | SIGRTMIN+7      | Real-time Signal          | Real-time signal 7, used for real-time applications.                       | `kill -SIGRTMIN+7 <pid>`                    |
| 42            | SIGRTMIN+8      | Real-time Signal          | Real-time signal 8, used for real-time applications.                       | `kill -SIGRTMIN+8 <pid>`                    |
| 43            | SIGRTMIN+9      | Real-time Signal          | Real-time signal 9, used for real-time applications.                       | `kill -SIGRTMIN+9 <pid>`                    |
| 44            | SIGRTMIN+10     | Real-time Signal          | Real-time signal 10, used for real-time applications.                      | `kill -SIGRTMIN+10 <pid>`                   |
| 45            | SIGRTMIN+11     | Real-time Signal          | Real-time signal 11, used for real-time applications.                      | `kill -SIGRTMIN+11 <pid>`                   |
| 46            | SIGRTMIN+12     | Real-time Signal          | Real-time signal 12, used for real-time applications.                      | `kill -SIGRTMIN+12 <pid>`                   |
| 47            | SIGRTMIN+13     | Real-time Signal          | Real-time signal 13, used for real-time applications.                      | `kill -SIGRTMIN+13 <pid>`                   |
| 48            | SIGRTMIN+14     | Real-time Signal          | Real-time signal 14, used for real-time applications.                      | `kill -SIGRTMIN+14 <pid>`                   |
| 49            | SIGRTMIN+15     | Real-time Signal          | Real-time signal 15, used for real-time applications.                      | `kill -SIGRTMIN+15 <pid>`                   |
| 50            | SIGRTMAX-14     | Real-time Signal          | The second highest real-time signal.                                       | `kill -SIGRTMAX-14 <pid>`                   |
| 51            | SIGRTMAX-13     | Real-time Signal          | The third highest real-time signal.                                        | `kill -SIGRTMAX-13 <pid>`                   |
| 52            | SIGRTMAX-12     | Real-time Signal          | The fourth highest real-time signal.                                       | `kill -SIGRTMAX-12 <pid>`                   |
| 53            | SIGRTMAX-11     | Real-time Signal          | The fifth highest real-time signal.                                        | `kill -SIGRTMAX-11 <pid>`                   |
| 54            | SIGRTMAX-10     | Real-time Signal          | The sixth highest real-time signal.                                       | `kill -SIGRTMAX-10 <pid>`                   |
| 55            | SIGRTMAX-9      | Real-time Signal          | The seventh highest real-time signal.                                      | `kill -SIGRTMAX-9 <pid>`                    |
| 56            | SIGRTMAX-8      | Real-time Signal          | The eighth highest real-time signal.                                       | `kill -SIGRTMAX-8 <pid>`                    |
| 57            | SIGRTMAX-7      | Real-time Signal          | The ninth highest real-time signal.                                        | `kill -SIGRTMAX-7 <pid>`                    |
| 58            | SIGRTMAX-6      | Real-time Signal          | The tenth highest real-time signal.                                        | `kill -SIGRTMAX-6 <pid>`                    |
| 59            | SIGRTMAX-5      | Real-time Signal          | The eleventh highest real-time signal.                                     | `kill -SIGRTMAX-5 <pid>`                    |
| 60            | SIGRTMAX-4      | Real-time Signal          | The twelfth highest real-time signal.                                      | `kill -SIGRTMAX-4 <pid>`                    |
| 61            | SIGRTMAX-3      | Real-time Signal          | The thirteenth highest real-time signal.                                   | `kill -SIGRTMAX-3 <pid>`                    |
| 62            | SIGRTMAX-2      | Real-time Signal          | The fourteenth highest real-time signal.                                   | `kill -SIGRTMAX-2 <pid>`                    |
| 63            | SIGRTMAX-1      | Real-time Signal          | The fifteenth highest real-time signal.                                    | `kill -SIGRTMAX-1 <pid>`                    |
| 64            | SIGRTMAX        | Real-time Signal Maximum  | The highest real-time signal.                                              | `kill -SIGRTMAX <pid>`                      |
