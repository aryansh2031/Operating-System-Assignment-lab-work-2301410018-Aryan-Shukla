Task 1: Process Creation Utility

Write a Python program that creates N child processes using os.fork(). Each child should print:

Its PID, its Parent PID, and a custom message. The parent should wait for all children using os.wait(). 

Task 2: Command Execution Using exec()

Modify Task 1 so that each child process runs a Linux command (ls, date, ps, etc.) using os.execvp() or subprocess.run(). 

Task 3: Zombie and Orphan Processes

Zombie: Fork a child and skip wait() in the parent. Orphan: The parent exits before the child finishes. Use ps -el | grep defunct to find zombies. 

Task 4: Inspecting Process Info from /proc

Take a PID as input. Read and print:

Process name, state, and memory usage from /proc/[pid]/status. Executable path from /proc/[pid]/exe. Open file descriptors from /proc/[pid]/fd. 

Task 5: Process Prioritization

Create multiple CPU-intensive child processes. Assign different nice() values. Observe and log the execution order to show how the scheduler is affected. 

Expected Output:

Child-parent process tree.  
Executed system commands from child processes.  
Verified zombie/orphan states using ps.  
Process details from /proc.  
Impact of priority using different nice values. 

Complexity Analysis: 

Time Complexity: O(n) for n processes.  
Space Complexity: O(n) due to keeping process IDs and logs. 

Practical Applications:

Operating system kernel development.  
Performance tuning through scheduling.  
Real-time and embedded system programming.  
Debugging tools and monitoring systems. 

Concepts Used:  
- os.fork(), os.getpid(), os.getppid()  
- os._exit(), os.wait(), os.nice()  
- subprocess.run(), os.execvp()  
- Reading /proc/[pid]/status, /exe, and /fd  
