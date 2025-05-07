# cyber_lab
# 🧾 Basic Scans
nmap 192.168.62.129                        # Basic scan
sudo nmap -v 192.168.62.129                # Verbose output
nmap -V                                    # Show Nmap version
man nmap                                   # Nmap manual
nmap 192.168.62.129 192.168.62.130         # Scan multiple IPs
nmap 192.168.62.0/24 --exclude 192.168.62.130   # Subnet scan excluding a host
nmap --open 192.168.62.129                 # Show only open ports
nmap -A 192.168.62.129                     # Aggressive scan
nmap -sA 192.168.62.129                    # ACK scan (firewall rule detection)
nmap -p 80 192.168.62.129                  # Scan specific port

# 📦 Packet Tracing & Port Selection
nmap --packet-trace 192.168.62.129         # Trace packets
nmap --top-ports 10 192.168.62.129         # Scan top 10 ports

# 🛰️ Ping & Discovery Scans
nmap -PN 192.168.62.130                    # Treat host as up (no ping)
nmap -sP 192.168.62.130                    # Ping scan (ARP on LAN)
nmap -PS 192.168.62.129                    # TCP SYN Ping
nmap -Pn 192.168.62.130                    # Skip host discovery
sudo nmap -PU 192.168.62.130               # UDP Ping
sudo nmap -PY 192.168.62.130               # SCTP INIT Ping
sudo nmap -PE 192.168.62.129               # ICMP Echo Request
nmap -PP 192.168.62.129                    # ICMP Timestamp
nmap -PM 192.168.62.129                    # ICMP Address Mask
nmap -PO 192.168.62.129                    # IP Protocol Ping
nmap -PR 192.168.62.129                    # ARP Ping (LAN only)

# 🌐 Network Path Tracing
nmap --traceroute 192.168.62.131           # Trace network route

# 🧠 OS Detection
nmap -O 192.168.62.129                     # OS detection
nmap -v -O 192.168.62.129                  # OS detection with verbosity
nmap -O --osscan-guess 192.168.62.129      # Guess OS more aggressively

# 🛠️ Service & Version Detection
nmap -sV -O 192.168.62.129                 # Service and OS detection
nmap -sV --version-trace 192.168.62.129    # Detailed version detection

# 🧪 Advanced Scans
nmap -sS 192.168.62.130                    # TCP SYN scan (stealth scan)
nmap -sT 192.168.62.129                    # TCP connect scan
nmap -sU 192.168.62.129                    # UDP scan
sudo nmap -sN 192.168.62.129               # TCP NULL scan
sudo nmap -sF 192.168.62.129               # TCP FIN scan
sudo nmap -sX 192.168.62.131               # Xmas scan (FIN, PSH, URG)
sudo nmap -sA 192.168.62.131               # TCP ACK scan

# ⚙️ Custom & Protocol Scans
nmap -sS --scanflags SYNFIN -T4 www.google.com  # Custom TCP flags
nmap -sO 192.168.62.129                         # IP protocol scan

# 🧃 Packet Type Control
nmap --send-eth 192.168.62.129                 # Send raw Ethernet frames
nmap --send-ip 192.168.62.129                  # Send raw IP packets
