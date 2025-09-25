# Lab1 h
Command: ps aux 
Explanation: a → show processes for all users
u → show user/owner of process
x → show processes not attached to a terminal

Command: pstree-p 
Explanation: The command pstree -p is used on Linux/Unix systems to display running processes in a tree-like structure, showing their parent-child relationships.

 Command: top
 Explanation: The top command in Linux is a real-time process monitoring tool. It shows you what’s happening on your system right now — like CPU, memory usage, and which processes are consuming resources.

 Command: nice -n 10 sleep 300 &
 Explanation: nice -n 10 sleep 300 & starts a background process (sleep 300) with low CPU priority (nice 10).

Since sleep doesn’t actually use CPU (it just waits), the niceness doesn’t matter much in this case — but it’s a good example for learning.

 Command: taskset -cp 3050
 Explanation: taskset -cp 3050 shows which CPU cores the process with PID 3050 is allowed to run on.

Command: ionice -c 3 -p 3050
Explanation: ionice -c 3 -p 3050 lowers process 3050’s disk priority to the idle class, so it only uses disk I/O when no one else needs it.

Command: lsof -p 3050 | head -5
Explanation: lsof -p 3050 | head -5 shows the first 5 files opened by process 3050 — like its working directory, executable, libraries, or sockets.

Command: strace -p 3050
Explanation: strace -p 3050 attaches to process 3050 and shows all the system calls it makes, in real time.

Command: sudo fuser -n tcp 8080
Explanation: sudo fuser -n tcp 8080 tells you which process is using TCP port 8080, so you can identify (and if needed, stop/kill) it.

Command: pidstat -p 3050 2 3
Explanation: pidstat -p 3050 2 3 monitors process 3050 and prints its CPU usage every 2 seconds, for 3 times, then stops.

Command: sudo cgcreate -g cpu,memory:/testgroup
EXplanation: sudo cgcreate -g cpu,memory:/testgroup creates a new cgroup named testgroup that can control CPU and memory usage for processes assigned to it.

![WhatsApp Image 2025-09-25 at 11 20 39_2c2d791a](https://github.com/user-attachments/assets/775fcc9e-9393-4453-bb84-0f56532a4f0f)


![WhatsApp Image 2025-09-25 at 11 20 39_1b590f21](https://github.com/user-attachments/assets/41aca843-d8c9-4564-91a3-386767b9911c)

![WhatsApp Image 2025-09-25 at 11 20 38_e75a35e8](https://github.com/user-attachments/assets/0f1ecef7-8cbc-4cc3-bbc1-66ef8c7c8c1d)

![WhatsApp Image 2025-09-25 at 11 20 38_91f3544d](https://github.com/user-attachments/assets/e3aa1dc2-3b69-4683-bcdd-83106c09f112)

![WhatsApp Image 2025-09-25 at 11 20 37_739f10c7](https://github.com/user-attachments/assets/d29fc683-5062-4920-894c-1fba276679a1)

![WhatsApp Image 2025-09-25 at 11 20 37_1c2854fc](https://github.com/user-attachments/assets/19ae4f65-5277-49fa-b1e2-c47675039591)
