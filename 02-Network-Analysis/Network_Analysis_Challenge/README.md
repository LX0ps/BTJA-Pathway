# Challenge Scenario 

Alexis is a fictional cybersecurity company with thousands of employees. An attacker has gained unauthorized entry into its premises and has connected their laptop to an unused port on a switch. The attacker now has access to the company’s internal networks. Within the internal network, there is a central server where critical proprietary data is stored. In this capture, the attacker is attempting to collect SSH credentials that they can use to log into the central server.


# PCAP 3 

# 1.	What is the MAC address of the attacker?

- We type in filter bar ssh to display the traffic and trim the packets we need to inspect to 142

<img width="1100" height="507" alt="pcap3" src="https://github.com/user-attachments/assets/caf0594a-4c40-45ab-ae69-2bd6450a0f60">

- I checked Statistics > Conversations. Looks like there are only two devices that are communicating via SSH.

<img width="1893" height="744" alt="pcap31" src="https://github.com/user-attachments/assets/b2efca48-d18d-4722-9a91-3cc26e156aa3" />

- I went back to the main screen of Wireshark and checked the first packet showing on screen (packet 765). I checked the ethernet details to find the answer.

<img width="1076" height="535" alt="pcap32" src="https://github.com/user-attachments/assets/1a273902-3b4c-4a46-b553-660b9e72c19c" />

- The mac address: **08:00:27:3d:27:5d**

# 2. What is the type of attack which is taking place that allows the attacker to listen in on conversations between the central server and another host?

- Man-in-the-Middle (MITM) Attack: An attacker secretly intercepts and relays communication between two parties, capturing or modifying data without their knowledge. The attacker can re-route exchanges and control the communication transparently.

# 3. What is the file which was downloaded from the central server?

- We navigate to Statistics > Protocol Hierarchy to get an overview of all the protocols used in the PCAP file.
- Under TCP, we can see that FTP traffic was captured in the PCAP file.
- I went back to the main screen of Wireshark and typed ftp in the display filter.
- I selected packet 550 and followed the TCP stream. File Name: **Alevis_Employee_Information_Chart.csv**

<img width="816" height="715" alt="pcap33" src="https://github.com/user-attachments/assets/838fd56e-261c-4411-a5fe-745c53344aad" />

# 4. What department does Borden Danilevich work in?

- Apply ftp filter and then right click any fpt packet.
- Follow tcp stream.
- Switch to Stream 1 (which contains the raw contents of the downloaded CSV file).
- Search (Ctrl + F) for the keyword Borden.
- Inspect the 5th column representing the department field. Answer: **Sales**.

# 5. What is the SSH password of the Domain Administrator?

- Conducted a search within the CSV file for the keyword "Admin" to identify the SSH password.
- The password is :  **gMR<4eXf]e6W**.

<img width="1037" height="140" alt="pcap34" src="https://github.com/user-attachments/assets/0b2c16f1-920a-42fd-a371-b992188c1fab">









  
