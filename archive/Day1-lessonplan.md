# Cyber Squad - Day 1: Linux and Networking Foundations in the Range

**Platform:** U.S. Cyber Range (cloud Exercise Area), accessed in a web browser.
**Duration:** about 4 hours including breaks.
**Mode:** Each student launches their own isolated Linux environment from the teacher's class.

---

## Learning objectives
- Log in to the U.S. Cyber Range and launch a Linux lab environment.
- Navigate the Linux file system from the command line.
- Explain basic networking terms and run simple diagnostic commands.

## Vocabulary (acronyms expanded and defined)
- **Cyber range**: a safe, isolated, cloud-based practice lab where students can use real security tools without touching the public internet or real victims.
- **CLI = Command Line Interface**: controlling a computer by typing commands.
- **OS = Operating System**: Windows, macOS, or Linux.
- **VM = Virtual Machine**: a computer that runs as software inside the cloud.
- **IP = Internet Protocol**; **IP address**: the numeric address of a device on a network.
- **DNS = Domain Name System**: the internet phone book that turns names into IP addresses.
- **SSH = Secure Shell**: a secure way to log in to another computer.

## Instructor setup (do before class)
1. Sign in to the U.S. Cyber Range at https://www.uscyberrange.org/ with your educator account.
2. Create a class or course and enroll students, or generate student invite links.
3. From the Courseware Repository, review **Course 6302: Cybersecurity Fundamentals**, the recommended introductory high school course, and select an introductory Linux exercise for the Exercise Area.
4. Confirm each student can reach their environment in a browser before the activity begins.

## Student lab (in the Exercise Area)
1. Log in and open today's Linux environment from your class.
2. Open the terminal and try these commands:
   - `pwd` shows your current folder (print working directory).
   - `ls` lists files; `ls -la` shows hidden files and details.
   - `cd foldername` moves into a folder; `cd ..` goes back up.
   - `cat filename` prints a file; `mkdir squad` makes a folder.
3. Networking basics:
   - `ip addr` shows your machine's IP address.
   - `ping -c 4 <target-in-lab>` checks if a device responds (use only targets inside the range).
   - `whoami` shows your username.
4. Save your work: create a folder named `cybersquad` and a text file inside it describing three commands you learned.

## Mini-lesson: how a network message travels
```
  Your VM  --(IP packet)-->  Switch/Router  --(DNS lookup)-->  Destination VM
  Everything here stays INSIDE the isolated range. Nothing reaches the real internet.
```

## In the news (real and verifiable)
Most of the world's web servers, cloud systems, and Android phones run on Linux, so command-line skills are a genuine job requirement in cybersecurity. The U.S. Cyber Range, operated by Virginia Tech, grew out of the Virginia Cyber Range and now provides hands-on cybersecurity labs to educators nationwide.

## Assessment
- Numerical: if a subnet allows 256 addresses and 3 are reserved, how many are usable for hosts? (Answer: 253.)
- MCQ: SSH stands for a) Secure Shell b) System Service Host c) Safe Server Host. (Answer: a.)
- Practical check: student shows the `cybersquad` folder and the file they created.

## Optional coding
Open **Day1.ipynb** for a short Python refresher that mirrors the command-line concepts.
