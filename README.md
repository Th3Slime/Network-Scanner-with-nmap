# Network-Scanner-with-nmap
**Goal**: Discover active devices and open ports on your network.  **Why**: Understanding network visibility is essential for vulnerability assessment.

1. Install Map nmap: 
sudo apt update && sudo apt install nmap  # Update packages and install nmap

2. Scan your local network:
nmap -sn 192.168.1.0/24  # Replace with your network IP range

3. Scan a target for open ports: 
nmap -sV 192.168.1.1  # Replace with a target IP (e.g., your router)

Save results to a file 
nmap -oN scan_results.txt 192.168.1.1  # Output to a file
