<h1>Use Wireshark To Analyze Network Packets</h1>

<h2>Description</h2>
<p>This project showcases the use of Wireshark on Kali Linux for capturing and analyzing network traffic. The goal is to demonstrate practical skills in network security, packet analysis, and Linux administration by setting up a Virtual Machine in VirtualBox, installing Kali Linux, and performing various packet capture and analysis tasks.</p>

<p>Key highlights of this project include configuring optimal VM settings, capturing live network data, and analyzing protocols like HTTP, DNS, and ICMP. Screenshots and a detailed report are included to illustrate the steps and insights gained throughout the project. This project demonstrates my proficiency in network troubleshooting, packet-level analysis, and technical documentation, contributing to my professional cybersecurity portfolio.</p>

<h2>Tasks</h2>
1. HTTP Analysis  <br>
2. DNS Analysis  <br>
3. ICMP Capture  <br>
<br />

<h2>Project Skills</h2>
- Kali Linux Installation and Configuration  <br>
- VirtualBox Setup with Optimized Memory and CPU  <br>
- Wireshark Packet Capture and Analysis  <br>
- Network Troubleshooting Techniques  <br>
- Documentation and Report Writing  <br>
<br />

<h2>Utilities Used</h2>

- [Wireshark](https://www.wireshark.org/)
- [Kali Linux](https://www.kali.org/)

<h2>Steps and Screenshots</h2>

<p align="center">
1. Set Up the Virtual Machine on VirtualBox
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/1c7e9e70-5f2b-4fe0-a7d6-be691a25c4b3" alt="Power Up Kali Linux Virtual Machine">
</p>

<p align="center">
2. Update Kali Linux<br>
    
```shell
sudo apt update && sudo apt upgrade -y
```    
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/c93a42c7-e0b8-49d8-b87d-cfbbdf7fc73e" alt="Update Kali Linux">
</p>

<p align="center">
3. Install Wireshark<br>
    
```shell
sudo apt install wireshark -y
```    
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/28c3ae8b-3323-404e-981e-10d98e729ae1" alt="Install Wireshark">
</p>

<p align="center">
4. Add User to Wireshark Group<br>
    
```shell
sudo usermod -aG wireshark $(whoami)
```    
</p>

<p align="center">
5. Reboot VM to apply group changes<br>
    
```shell
sudo reboot
```    

<p align="center">
6. Open Wireshark from the Applications menu or by running wireshark in the terminal.<br>
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/63d30c30-abd8-477b-ac18-fa8f675e064e" alt="Open Wireshark from the Applications menu or by running wireshark in the terminal.">
</p>

<p align="center">
7. Select an active network interface to start capturing packets (e.g., eth0).<br>
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/d00fd0b4-84c4-469c-b68d-2e619cf5e538" alt="Select an active network interface to start capturing packets (e.g., eth0).">
</p>

<p align="center">
8. Begin Packet Capture:<br>
  - Click "Start Capturing Packets" (blue shark fin icon).<br>
  - Let the capture run while browsing some websites or running terminal commands in Kali to generate traffic.
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/273f8183-2cd0-46b3-966b-bafe381ae3a0" alt="Select an active network interface to start capturing packets (e.g., eth0).">
</p>

<p align="center">
9. Stop the capture after a few minutes<br>
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/7a48c0ef-9fbb-466d-ab6b-3d855e3f251e" alt="Stop the capture after a few minutes">
</p>

<p align="center">
10. Task 1: HTTP Analysis: Filter by HTTP packets<br>
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/2f50dd56-9930-407e-b82e-cf9bb5558c18" alt="Task 1: HTTP Analysis: Filter by HTTP packets">
</p>

<p align="center">
11. Inspect GET requests to see how data is transmitted.<br>
    
```shell
http.request.method == "GET"
```    
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/c0fc5c6f-0b23-435a-8319-adebe5f32f95" alt="Inspect GET requests to see how data is transmitted.">
</p>

<p align="center">
12. Task 2 DNS Analysis: Filter by DNS.<br>   
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/0ea93847-4a4c-4280-a869-029c4ea8327a" alt="Task 2 DNS Analysis: Filter by DNS.">
</p>

<p align="center">
13. Filter by specific domain name.<br>
    
```shell
dns.qry.name == "example.com"
```    
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/65986a60-1d1a-45b3-841f-95bed2ad9a24" alt="Filter by specific domain name.">
</p>

14. Filter by specific domain name.<br>
    
```shell
dns.qry.name == "example.com"
```    
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/65986a60-1d1a-45b3-841f-95bed2ad9a24" alt="Filter by specific domain name.">
</p>

<p align="center">
15. Task 3 Use the ICMP capture filter and start capturing traffic<br>   
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/551adc3b-7b96-4d13-ba34-0b8ac3e50f25" alt="Task 3 Use the ICMP capture filter and start capturing traffic">
</p>

<p align="center">
16. Use the ping command followed by an IP address or domain name.<br>   
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/990befbd-5dd7-485a-9e1e-8fd508ac0d89" alt="Use the ping command followed by an IP address or domain name.">
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/1e108ed4-b0ef-43f5-8171-2c865d2915c5" alt="Use the ping command followed by an IP address or domain name.">
</p>

<p align="center">
17. Click on any packet to view its details in the Packet Details pane, where you can see information like the type of ICMP message, sequence numbers, and other relevant data.<br>   
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/01f13532-9708-4ef6-a01d-354227a97a61" alt="Click on any packet to view its details in the Packet Details pane, where you can see information like the type of ICMP message, sequence numbers, and other relevant data.">
</p>
