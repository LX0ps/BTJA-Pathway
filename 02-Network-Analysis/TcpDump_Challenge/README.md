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

  









