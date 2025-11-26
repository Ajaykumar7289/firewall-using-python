!!Firewall using Python

📖 PROJECT OVERVIEW  
A lightweight and efficient personal firewall developed in Python using the Scapy library.  
It captures inbound and outbound packets in real time, applies customizable filtering rules,  
and logs all traffic activity for auditing and analysis.

🎯 OBJECTIVES  
• Capture and inspect real-time network traffic  
• Create customizable rule sets for filtering IPs, ports, and protocols  
• Log all allowed and blocked packets with timestamps  
• Optional GUI dashboard for live monitoring  

🧰 TOOLS & TECHNOLOGIES  
Component            Purpose  
------------------------------------------------  
Python 3             Core programming language  
Scapy                Packet sniffing & analysis  
Tkinter              Optional GUI interface  
iptables (Linux)     System-level rule enforcement (optional)  

⚙️ FEATURES  
✅ Live packet sniffing  
✅ Rule-based filtering (IPs, ports, protocols)  
✅ Real-time terminal logging  
✅ Log file generation (firewall_log.txt)  
✅ Expandable Tkinter-based GUI  

🧩 PROJECT STRUCTURE  
Personal-Firewall-using-Python/  
│  
├── firewall.py            # Core packet sniffing and rule-handling logic  
├── firewall_gui.py        # Optional GUI for live monitoring  
├── rules.json             # Custom rules (blocked IPs/ports)  
├── firewall_log.txt       # Log file for traffic activity  
└── README.md              # Documentation  

🚀 HOW TO RUN  

1️⃣ Install Dependencies  
sudo apt update  
sudo apt install -y python3 python3-pip python3-tk  
python3 -m pip install --user scapy  

2️⃣ Start the Firewall  
sudo python3 firewall.py --iface eth0  
(Replace **eth0** with your active network interface.)  

3️⃣ Modify Rules  
Edit rules.json:  
{  
  "blocked_ips": ["192.168.1.5", "10.10.10.10"],  
  "blocked_ports": [80, 443]  
}  
Restart the script — blocked packets will show as 🚫 in the logs.

📋 SAMPLE LOG OUTPUT  
2025-10-25 15:51:17 - 🚫 BLOCKED: 10.119.67.247 → 23.220.75.232 TCP dport=80 | Blocked Port  
2025-10-25 15:51:18 - ✅ ALLOWED: 10.119.67.103 → 239.255.255.250 UDP dport=1900 | Allowed  
2025-10-25 15:51:19 - ✅ ALLOWED: IPv6 Neighbor Discovery Packet | No IP layer  
2025-10-25 15:51:20 - ✅ ALLOWED: 0.0.0.0 → 255.255.255.255 UDP dport=67 | Allowed  

📸 SCREENSHOTS  
![Firewall Running](screenshots/firewall.running)

Description: This screenshot displays the live packet monitoring interface from the GUI module.  
It shows real-time updates of incoming and outgoing network packets.




🧠 LEARNING OUTCOMES  
• Hands-on experience in packet sniffing and network traffic analysis  
• Understanding of firewall logic and rule-based filtering  
• Python scripting applied to real-world cybersecurity tasks  
• Logging and auditing mechanisms for network events  

🏁 CONCLUSION  
This project demonstrates how Python and Scapy can be used to implement a  
functional personal firewall. With extended rule sets, alerting systems,  
and anomaly detection, it can be upgraded into a fully capable IDS/IPS solution.

👨‍💻 AUTHOR  
**Rupani Ajay Kumar**

📂 Repository: *Firewall-using-Python*
