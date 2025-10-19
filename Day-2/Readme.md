# Learning Objectives
- Understanding what is linux and its history
- Know the roles and functions of linux kernel
- Identify major linux distributions and their usecase
- Understand the linux ecosystem and opensource philosophy
- Recognize why linux is critical for DevOps, SRE, and all Cloud Engieers
- Be familiar with package management concepts and commands

## Why Learn Linux?

- Linux sits at the core of today’s technological world. From the supercomputers powering scientific innovation to the servers running the internet and the smart devices in your home, Linux is omnipresent—often working quietly behind the scenes. 
- It's the preferred operating system for developers, system administrators, and cybersecurity experts due to its reliability, flexibility, and open-source nature. 
- Gaining proficiency in Linux is a foundational skill for anyone aiming to build a successful career in technology.

## Why Linux Matters to You as a DevOps/SRE/Cloud Engineer
Linux is the foundation of modern infrastructure, making it indispensable for DevOps, Site Reliability Engineers (SREs), and Cloud Engineers:
- **DevOps:** Linux powers CI/CD pipelines (e.g., Jenkins, GitLab) and container platforms (e.g., Docker, Kubernetes). Bash scripting automates deployment workflows.
- **SRE:** Linux’s stability and configurability ensure reliable, scalable systems. SREs use Linux for monitoring (e.g., Prometheus), logging, and high-availability setups.
- **Cloud Engineers:** Major cloud platforms (AWS, GCP, Azure) run on Linux instances. Linux proficiency is key for managing VMs, optimizing costs, and configuring cloud services.
- **Automation and Scalability:** Linux’s command-line tools and scripting enable automation, while its lightweight nature supports scaling across thousands of servers.
- **Industry Dominance:** Over 96% of the top 1 million web servers and 100% of the top 500 supercomputers run Linux (as of 2025).

**Quick Fact:** Most cloud-native tools (e.g., Kubernetes, Terraform) are Linux-native, and employers expect Linux proficiency for DevOps/SRE/Cloud roles.

## what is linux ?

- Linux is a free, open-source, Unix-like kernel developed by Linus Torvalds in 1991. It serves as the foundational core for a wide variety of operating systems known as "Linux distributions" or distros. 
- You'll find Linux powering everything from servers and desktop computers to embedded systems, supercomputers, IoT devices, and even Android smartphones.

**Analogy**
- Think of the Linux kernel as a car’s engine —it’s the vital component that makes the whole system run. However, just as a car needs more than an engine (like a body, seats, and dashboard) to function as a complete vehicle, a Linux distribution packages the kernel with essential tools, software, and interfaces to create a fully functional operating system.

# A Brief History of Linux
- 1983: Richard Stallman starts the GNU Project to create a free, Unix-like operating system.
- 1991: Linus Torvalds releases the first Linux kernel (version 0.01) as a personal project.
- 1993: Debian, one of the oldest Linux distributions, is founded.
- 1994: Linux kernel 1.0 is released, marking a stable milestone.
- 2000s: Linux gains traction in servers, supercomputers, and embedded systems.
- 2010s: Linux powers Android, cloud platforms (AWS, Azure), and containers (Docker).
- 2025: Linux runs on over 80% of cloud workloads and is the foundation for AI and IoT ecosystems.

Fun Fact: Linus Torvalds still oversees Linux kernel development through the Linux Kernel Mailing List (LKML), ensuring its collaborative spirit.

## Core Components of Linux
Linux is structured in layers, from hardware to user applications. Here's a high-level overview:

+----------------------------------------------------+
| User Applications (Vim, Docker, Apache, etc.)     |
+----------------------------------------------------+
| Shell (Bash, Zsh, Fish, etc.)                     |  <-- Part of the OS
+----------------------------------------------------+
| System Libraries (glibc, libc, OpenSSL, etc.)     |  <-- Part of the OS
+----------------------------------------------------+
| System Utilities (ls, grep, systemctl, etc.)      |  <-- Part of the OS
+----------------------------------------------------+
| Linux Kernel (Process, Memory, FS, Network)       |  <-- Core of the OS
+----------------------------------------------------+
| Hardware (CPU, RAM, Disk, Network, Peripherals)   |
+----------------------------------------------------+

![alt text](image.png)


# what will you learn ?

**Linux Learning Journey**<br>
    |--> Fundamentals<br>
- Commmands & FileSystem<br>
- Users and permissions<br>
- Process Management


    |---> System Administration<br>
    - Networking<br>
    - Security<br>
    - Service Management

  |--> Advanced Topics<br>
    - Performance Tuning<br>
    - Containers <br>
    - Troubleshooting

  |--> Real-world Projects<br>
    - DevOps Scenarios<br>
    - Mega Project



- **How to Get the Most Out of This Course:**
  - Practice hands-on with every topic (use a VM, WSL, or cloud instance)
  - Complete all exercises and review solutions
  - Experiment, break things, and learn by doing
  - Join online communities for support and networking

- **Recommended Prerequisites:**
  - Curiosity and willingness to learn
  - Basic computer and internet skills

- **Setting Up Your Learning Environment:**
  - **Online Terminal (Easiest):**
    - [KillerCoda](https://killercoda.com/) — Interactive scenarios and Linux terminals
    - [Play with Docker](https://labs.play-with-docker.com/) — Free instant Linux VMs with Docker support
  - **VirtualBox VM:** Download Ubuntu ISO + VirtualBox, create new VM with 2GB RAM
  - **WSL (Windows):** Run `wsl --install` in PowerShell as Administrator
  - **Cloud VM:** AWS EC2 t2.micro (free tier), GCP Compute Engine, or Azure VM
  - **Links**: Try free tiers from:
    - [AWS Free Tier](https://aws.amazon.com/free/)
    - [Google Cloud Free Tier](https://cloud.google.com/free)
    - [Azure Free Account](https://azure.microsoft.com/en-us/free/)
    - [DigitalOcean Free Trial](https://www.digitalocean.com/)


# Exercises
1. Write down your personal goals for this course.
2. Join a Linux or DevOps online community (e.g., Reddit, Discord, LinkedIn group).
3. Set up your first Linux environment (online terminal, VM, WSL, or cloud instance).
4. Research and note down 3 ways Linux is used in the tech industry.
5. **Share your daily learnings publicly on social media (Twitter, LinkedIn, etc.) using hashtags `#linuxthefinalboss` and `#getfitwithsagar`. This helps you get noticed by recruiters and builds your professional brand.**

## Solutions
1. **goals:** 
- "Get a High paying DevOps job"
- "Automate tasks with Linux"
- "Understand cloud infrastructure"
- "Be Really very good at Linux".

2. **Recommended communities:**
   - **Course Discord:** https://discord.gg/mNDm39qB8t (Join for course support and discussions)
   

3. **Setup Instructions:**
   - **Online Terminal:** Try [KillerCoda](https://killercoda.com/) or [Play with Docker](https://labs.play-with-docker.com/)
   - **VirtualBox:** Download VirtualBox + Ubuntu ISO → New VM → 2GB RAM → Install Ubuntu
   - **WSL:** Open PowerShell as Admin → `wsl --install` → Restart → Install Ubuntu from Microsoft Store
   - **AWS:** Launch EC2 → Ubuntu Server → t2.micro → Connect via SSH

4. **Linux usage examples:** Web servers (Apache/Nginx), cloud infrastructure (AWS/GCP), container orchestration (Docker/Kubernetes), automation (Ansible/Terraform), security testing (Kali Linux).

## Completion Checklist
- [✅] Defined personal learning goals
- [ ✅] Joined at least one Linux/DevOps community
- [✅ ] Set up Linux environment and can access terminal
- [✅] Researched Linux industry applications
- [✅ ] Ready to start Day 1
- [x] Shared learnings publicly with hashtags #linuxthefinalboss and #getfitwithsagar

## Troubleshooting
- **VirtualBox issues:** Enable virtualization in BIOS/UEFI
- **WSL not working:** Ensure Windows 10 version 2004+ or Windows 11
- **Cloud VM access:** Check security groups allow SSH (port 22)

## Feedback & Suggestions
We want to make this series as helpful as possible.  
Please share your feedback or suggest topics for future days in the **#linux-the-final-boss** Discord channel or the Google Group.  
Your input will help us improve and ensure we cover what's most valuable to you!

## Next Steps
Once you've completed the checklist above, you're ready for the next step!

Proceed to [Day 1: What is Linux?](../Day_01/notes_and_exercises.md)  