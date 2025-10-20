# 🥧 Raspberry Pi Network Sensor - Writeup

**Date Completed:** October 19, 2025  
**Time Invested:** ~2 hours  
**Difficulty:** Beginner → Intermediate  

---

## 🎯 What I Built

A **network packet capture device** using a Raspberry Pi 5, sitting on my home lab network to monitor traffic.

**Why?** Learning how networks work by *watching* them live. or I think sooo

---

## 🔧 Hardware

- Raspberry Pi 5 (8GB RAM)
- Ethernet cable (connected to network switch)
- Power supply

---

## 📋 Setup Steps

### Step 1: Flash Raspberry Pi OS

Downloaded Pi OS Lite 64-bit, flashed to SD card using Balena Etcher.

### Step 2: First Boot & SSH Enable

Booted Pi, waited for first-boot setup (~3-5 min), then SSH was enabled automatically.

### Step 3: Configure Static IP

Edited `/etc/dhcpcd.conf`:
```bash
sudo vim /etc/dhcpcd.conf
```

Added:
```
interface eth0
static ip_address=10.0.0.17/24
static routers=10.0.0.1
static domain_name_servers=10.0.0.1 8.8.8.8
```

**Why static IP?** So I can *always* find it at `10.0.0.17`. No guessing games! 🎯

### Step 4: Install Tools
```bash
sudo apt update
sudo apt install tcpdump vim git htop tmux -y
```

### Step 5: Test Packet Capture
```bash
sudo tcpdump -i eth0 -n
```

**Result:** ✅ Packets flowing! Saw DNS queries, DHCP traffic, everything!

---

## 🎓 What I Learned

- **Static IP assignment** = devices stay findable
- **tcpdump basics** = how to see network traffic raw
- **SSH over VPN** = works even with Mullvad blocking ICMP
- **First boot waits longer** = patience is a debugging skill uwu

---

## 🔮 Next Steps

- [ ] Set up persistent tcpdump logging
- [ ] Parse logs with Python script
- [ ] Build dashboard to visualize traffic
- [ ] Deploy second Pi as honeypot

---

## 📚 Resources

- [Raspberry Pi Docs](https://www.raspberrypi.com/documentation/)
- [tcpdump Tutorial](https://www.tcpdump.org/)
- [DHCPCD Config Guide](https://manpages.debian.org/dhcpcd.conf)

---

*This project taught me that learning by *doing* > reading docs forever!*
