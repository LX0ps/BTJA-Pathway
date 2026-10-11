# Challenge Scenario

In this activity you’ll be putting your new TCPDump skills to the test by analyzing two PCAPs. You will be able to complete both of the challenges using the knowledge we have covered in the previous lessons.

# PCAP 4 

# 1. How many UDP packets have been captured?

- We setup a VM (kali linux) to perform packet analysis.
- Run the command on cli: **sudo tcpdump -r SBT-PCAP4.pcap udp --count**.
- We see 3290 UDP packets were captured.
<img width="951" height="130" alt="pcap41" src="https://github.com/user-attachments/assets/d5e547f7-316a-45dc-ba5e-a2e699f62103" />

# 2. How many TCP packets have both the SYN and ACK flags set?
- SYN + ACK = 00010010 which is 18 in decimal form.
- Run the command **tcpdump -r SBT-PCAP4.pcap “tcp[tcpflags] == 18” –count**.
- The tcp packets are 20.

<img width="960" height="133" alt="pcap42" src="https://github.com/user-attachments/assets/30f32a0a-b3c1-4892-8500-c1e0ca3cb1ea" />

# 3. Which version of chrome was used to connect to securityblue.team? 
- Open cli and run the command **tcpdump -r SBT-PCAP4.pcap -vvv | grep -i chrome**.
- We get the version of chrome which is **80.0.3987.87**.

  <img width="944" height="196" alt="pcap43" src="https://github.com/user-attachments/assets/7d54efa7-de70-4a73-b16f-1e60c6708aab" />

  # 4. How many packets have a TTL value of 38?

  - Run the tcpdump command on cli: **tcpdump -v -r SBT-PCAP4.pcap | grep “ttl 38” | wc -l** or **tcpdump ip[8] == 38 -r SBT-PCAP4.pcap --count**.
  - We see that we get 710 packets.
 
  <img width="940" height="137" alt="pcap44" src="https://github.com/user-attachments/assets/00b437ac-d41d-4f61-93de-e83bcb590a44" />



# PCAP 5 

# 1. What is the name of the PNG file on the webserver at 192.168.56.111?

- We run the command **tcpdump -A -r SBT-PCAP5.pcap | grep png** to get the name of the PNG file on the web server at 192.168.56.111.
- We get the name of the png file which is **proprietary.png**.

<img width="965" height="136" alt="pcap5" src="https://github.com/user-attachments/assets/8ec9ad00-3256-4429-b562-d8a789f19372" />


# 2. Which version of OpenSSH is running on the server?

- We run the command **tcpdump -vvv -r SBT-PCAP5.pcap | grep OpenSSH** to see the version of openssh.
- We get two results. The first one is the client connecting to the server. The next one is the server connecting to the client.
- We need to check the SSH version of the second result.
- We find client 7.6 version and the server 7.9p1 debian 10

<img width="938" height="228" alt="pcap51" src="https://github.com/user-attachments/assets/332e1103-a03a-4394-8220-9c7fae67548d" />

# 3. On which port is the .zip file being served? 

- We run the command **tcpdump -A -r SBT-PCAP5.pcap | grep .zip -B 3** to find the port of the zip file.
- The port we get is 3016

<img width="954" height="457" alt="pcap52" src="https://github.com/user-attachments/assets/55bbbebb-08ed-44b9-8d0e-63afc65364bb" 


  # 4. When was a packet with a TCP checksum value of 53203 captured?

- Convert the 53203 to hexadecimal
- 53203=0xCFD3, 06:04:46.207925

<img width="1895" height="163" alt="pcap53" src="https://github.com/user-attachments/assets/40bd6f96-5a0b-4eb8-b062-ad19dbb3c527" />







  









