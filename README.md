# HomeLab_Kali_Ubuntu_UFW_Wireshark
Cybersecurity: Simulating Attack with Kali using Nmap to Ubuntu and track the Pcap with Wireshark
![image](https://github.com/user-attachments/assets/df4e0d2a-d0fa-40e9-9e70-720b70177399)

In this scenario, we will perform a simulated attack using the nmap tools and capture network traffic using wireshark.
- Nmap will use nmap -A [IP target]
  - The command nmap -A is used for aggressive scanning with Nmap, which enables OS detection, version detection, script scanning, and traceroute. This provides detailed 
    information about the target system, making it useful for security assessments and network exploration. Functionality of nmap -A:
      - OS Detection: Identifies the operating system running on the target device.
      - Version Detection: Determines the versions of services running on open ports.
      - Script Scanning: Executes Nmap scripts to gather additional information about the target.
      - Traceroute: Maps the path packets take to reach the target, providing insight into the network topology.
  - Wireshark is used for capturing and analys the network traffic.
  - Ufw / Uncomplicated Firewall is used for managing firewall rules in Linux, particularly on Ubuntu and its derivatives. Its primary function is to provide an easy way to configure and manage a netfilter firewall, which is the underlying framework used by Linux for packet filtering and network address translation (NAT).
  Procedure:
  # Ubuntu
  - Install the wireshark (`sudo apt install wireshark`).
  - Install UFW (`sudo apt install ufw`).
  - `sudo ufw enable` is used to activate the Uncomplicated Firewall (UFW) on a Linux system, typically on Ubuntu and its derivatives. When you run this command, UFW will start enforcing the firewall rules that you have configured.
  -  `sudo ufw allow ssh` is used for accessing your server remotely, you need to allow SSH connections.
  -  `sudo ufw allow from [ip addresss]` is used for granted access from certain IP address for example `sudo ufw allow from 10.0.2.4` to allow access from 10.0.2.4.
  -  `sudo ufw status` is used to check the current status of the Uncomplicated Firewall (UFW) on a Linux system, typically on Ubuntu and its derivatives. This command provides information about whether UFW is active and lists the rules that are currently enforced.
  -  `sudo wireshark` to launch wireshark.
  -  start to capture the network traffic.
  - Result: alot of TCP was sent from Kali to Ubuntu  
![image](https://github.com/user-attachments/assets/a8b14560-c4b6-40dd-8d3c-6b358c0be734)

# Kali
- `nmap -A 10.0.2.15` is used for aggressive scanning with Nmap, which enables OS detection, version detection, script scanning, and traceroute.
- ![image](https://github.com/user-attachments/assets/7d83267b-4bf4-4019-abf4-852dafe3eae6)
