### Part 1: VM Creation & First Boot
1. Follow Steps 1-3 above—get Ubuntu 25.04 installed & logged in as linuxthefinalboss.
2. **Exercise:** Run `neofetch` (install if needed: `sudo apt install neofetch`)—screenshot your system info.
3. **Question:** What kernel version shows? (Compare to Day 1's `uname -r`.)

### Part 2: Network Check & Fix
1. Ping test: `ping 8.8.8.8` (IP) & `ping google.com` (DNS).
2. **Exercise:** If DNS fails, edit /etc/resolv.conf (add `nameserver 8.8.8.8`) → Test again.
3. **Question:** How does VM networking differ from your host?

### Part 3: Snapshot Practice
1. Take "Baseline" snapshot.
2. **Exercise:** Install a fun tool (`sudo apt install cowsay -y; cowsay "Hello VM!"`) → Take "With Cow" snapshot.
3. Restore to Baseline—cow gone? Reinstall to confirm.
4. **Question:** Imagine a bad config change—how does snapshot save you?

### Part 4: Simple Config Tweak
1. **Exercise:** Change hostname: `sudo hostnamectl set-hostname my-lab-server` → Reboot → `hostname` confirms.
2. Add to snapshot chain: "Renamed Host."
3. **Question:** Why tweak hostname in a VM (e.g., for multi-VM testing)?

### Part 5: Quick Challenge - Boot Observation
- Reboot VM; time the boot (`time sleep 1` post-login for fun).
- **Exercise:** Run `journalctl -b -p err` (boot errors? Usually none!).
- **Question:** What service starts last (hint: `systemd-analyze blame`)?

### Part 6: Multi-VM Networking (Bridge Mode)
1. **Create Second VM:** Repeat Part 1 steps for a second Ubuntu VM ("VM2-Lab").
2. **Switch to Bridge:** For both VMs: Settings → Network → Adapter 1 → Attached to: Bridged Adapter → Name: Your WiFi/Ethernet interface (e.g., en0).
3. **Start Both:** Boot VM1 & VM2—note their IPs (`ip addr show` or `ifconfig`).
4. **Test Access:** From VM1: `ping <VM2-IP>` (should reply). From host terminal: `ping <VM1-IP>` (bridge exposes to network).
5. **Exercise:** Install netcat (`sudo apt install netcat -y`); in VM1: `nc -l 1234`; in VM2: `nc <VM1-IP> 1234` → Type message (transmits!).
6. **Question:** Why bridge over NAT for multi-VM? (Direct comms, like a LAN party.)