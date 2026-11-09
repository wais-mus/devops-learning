# Linux Terminal Basics

## What I learned
I learnt the really useful tool of the command Manual (man) as it helps me reference quickly the descriptive tools i can use to get the answers i need, 
always checking where i am with "pwd" is great for ensuring i am where im meant to be.

## Key commands and what they do
| Command | What it does | When I'd use it |
|---|---|---|
| `pwd` | Prints the current folder | First thing after logging into a server |
| `ls -la` | Lists all files, including hidden, in long format | Checking permissions and owners |
| `cd -` | Jumps back to the previous folder | Switching between two folders quickly |
| `man ls` | Opens the manual for a command | Looking up an option without Google |
| `type cd` / `which ls` | Shows what kind of command it is / where it lives | Troubleshooting "command not found" |

## Lab evidence

|From my lab the command  'ls -la' was the most interesting as it showed me the list of all files and hidden files in the currentl folder i am in/
<img width="612" height="390" alt="image" src="https://github.com/user-attachments/assets/1a66b946-7c97-4156-9d34-4bbcf07f4296" />


## How this relates to my IT job

In IT support, the first thing I do with an unfamiliar device is find out what it is
and what state it's in before I change anything. On Windows I'd check
`winver` or System Information. These commands are the Linux version of that first check.

| Task | Linux command | Why it matters at work |
|------|---------------|------------------------|
| Identify the OS and version | `cat /etc/os-release` | Confirms whether a server is on a supported version before patching or raising a ticket with a vendor |
| Confirm which machine I'm on | `hostname` | Avoids running a fix on the wrong server, which is easy to do with several SSH sessions open |
| Check what's in a config folder | `ls /etc/ssh \| wc -l` | A quick sanity check of what's configured before troubleshooting remote access problems |
| Find the largest log file | `ls -lS ~/logs` | Full disks are a common cause of outages; finding oversized logs is often the first step |


**What changes for me:**

I've usually done these checks through a GUI or remote
management tool. Doing them from the terminal is faster, works over SSH on any
server, and can be scripted, which is what DevOps work builds on.
