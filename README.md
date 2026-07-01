# 🔍 Network Scanner with nmap

Part of my [project portfolio](https://github.com/Th3Slime).

## 📌 Overview
Network reconnaissance lab run on my Linux home lab server (Lenovo laptop) — my first serious time in a Linux terminal day-to-day. This README is honest about the learning curve, not just the finished commands.

**Goal:** Discover active devices and open ports on my network.
**Why:** Understanding network visibility is essential for vulnerability assessment.

## 🛠 Tools Used
`nmap` · Linux terminal (Ubuntu-based)

## 🧪 Methodology
```bash
sudo apt update && sudo apt install nmap        # install nmap
nmap -sn 192.168.1.0/24                         # ping scan: find live hosts
nmap -sV 192.168.1.1                            # service/version detection on a target
nmap -oN scan_results.txt 192.168.1.1           # save results to a file
```

## 🔍 Real problems I hit (and what they taught me)
- Some scans failed due to permission restrictions → learned why elevated privileges matter and when `sudo` is actually required for raw-socket scan types
- Firewall rules were silently dropping scan responses → had to learn how different Nmap scan types (`-sS` vs `-sT` vs `-sn`) interact with local/remote filtering
- Devices weren't showing up in host discovery → fixed by reviewing subnet ranges and adjusting scan flags rather than assuming the tool was broken

## 🧠 Lessons Learned
Coming into this with zero Linux background, the terminal was intimidating for about a day — then it became the OS I preferred over a GUI. Nmap results are only meaningful once you understand *why* a scan behaves the way it does (permissions, filtering, scan type), not just what the output says.

## 📸 Evidence
*(Add screenshots here: `nmap -sn` host discovery output, `nmap -sV` service detection output)*

## 📚 Skills Demonstrated
Network reconnaissance · port/service enumeration · Linux CLI fluency · methodical troubleshooting

## 🔗 Related Projects
- [Windows-AD-GPO-Home-Lab-Project](https://github.com/Th3Slime/Windows-AD-GPO-Home-Lab-Project)
- [Password-Auditing-with-John-the-Ripper](https://github.com/Th3Slime/Password-Auditing-with-John-the-Ripper)
- [Firewall-Configuration-with-UFW-Uncomplicated-Firewall-](https://github.com/Th3Slime/Firewall-Configuration-with-UFW-Uncomplicated-Firewall-)
