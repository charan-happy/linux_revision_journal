### Preparing for the Lab
If you don’t have an AWS account:
- **Virtual Machines:** Use VirtualBox/VMware with Ubuntu Server or CentOS Stream ISOs.
- **Free Cloud Alternatives:** Oracle Cloud Free Tier or Google Cloud’s free trial.
- **Local Terminal:** macOS/Linux users can practice commands locally.

**Troubleshooting SSH Issues:**
- **"Permission Denied"**: Run `chmod 400 my-key.pem` and verify username (`ec2-user` for Amazon Linux, `ubuntu` for Ubuntu).
- **Connection Timeout**: Ensure the security group allows SSH (port 22) and check the public IP.

### Part 1: Lab - Launching Two Different Linux Instances
1. **Launch Your First Instance (RHEL-based):**
   - Log in to the **AWS Management Console** and navigate to the EC2 Dashboard.
   - Click **"Launch Instance"** and select the **Amazon Linux 2** AMI.
   - Choose a `t2.micro` instance type and create a new key pair (`.pem` file). **Save this file securely.**
   - Complete the launch process and wait for the instance to be "Running."

2. **Launch Your Second Instance (Debian-based):**
   - Repeat, selecting the **Ubuntu Server** AMI.
   - Use the **same key pair** for simplicity.
   - Complete the launch process and wait for the instance to be "Running."

### Part 2: Connect, Explore, and Identify
1. **Connect to Amazon Linux 2:**
   - Run `chmod 400 my-key.pem`.
   - Connect: `ssh -i "my-key.pem" ec2-user@<amazon_linux_ip_address>`.

2. **Connect to Ubuntu:**
   - Open a new terminal tab/window.
   - Connect: `ssh -i "my-key.pem" ubuntu@<ubuntu_ip_address>`.

### Part 3: Questions for the Lab & Review
1. **Command-Line Basics:**
   - Run `pwd`, `ls`, and `man ls` on either instance.
   - **Questions:** What does `pwd` tell you? Why is `man` useful?

2. **Identify the Distribution:**
   - Run `cat /etc/os-release` on both instances and compare.
   - **Question:** What are the key differences in the output?

3. **Identify Package Managers:**
   - Run `sudo yum update` on Amazon Linux 2 and `sudo apt update` on Ubuntu.
   - **Question:** What happens? Explain the difference in one sentence, referencing the package managers section above.

4. **Distribution vs. Kernel:**
   - **Question:** Explain the difference between the **Linux kernel** and a **Linux distribution** in your own words.

5. **Role of the GNU Project:**
   - **Question:** What is the role of the GNU Project in the Linux ecosystem?

### Part 4: Write and Run a Simple Script
1. On either instance, create `hello.sh`:
   ```bash
   nano hello.sh
   ```
2. Add:
   ```bash
   #!/bin/bash
   echo "Hello, Linux World!"
   echo "My current directory is: $(pwd)"
   echo "My distribution is:"
   cat /etc/os-release | grep PRETTY_NAME
   ```
3. Save (`Ctrl+O`, `Enter`, `Ctrl+X`), make executable (`chmod +x hello.sh`), and run (`./hello.sh`).
4. **Question:** What does each line do? Compare outputs on both instances.

### Part 5: Challenge for DevOps/SRE/Cloud Engineers
- **Task:** Run `uname -r` to check the kernel version on either instance. Compare it to the latest stable version on kernel.org. Why might cloud providers like AWS use older kernels?
- **Hint:** Consider stability, compatibility with cloud tools, and enterprise support.
