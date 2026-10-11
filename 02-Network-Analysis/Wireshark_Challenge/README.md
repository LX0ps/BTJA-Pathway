# Challenge Scenario 
 In this activity we analyze 2 pcaps files PCAP 1 and PCAP 2 using wireshark.

# PCAP 1 

#  1. Which protocol was used over port 3942?

- Open wireshark and navigate to statistics>endpoints>UDP.
- Right click on the line with the port 3942 and select "apply as filter">"selected".
- We then return to the main wireshark screen to view the filtered traffic.
- We see the protocol used for port 3942 is SSDP (Simple Service Discovery Protocol).

# 2. What is the IP address of the host that was pinged twice?
- Ping works by sending icmp echo requests to a network interface and waiting a response back.
- We go to the filter bar and type icmp to focus on that traffic.
- Specifically we type "filter icmp or icmp.type == 8" (Echo Request) and check the destination IP address of the ping packets.  IP: 8.8.4.4.

# 3. How many DNS query response packets were captured?

- We go to the filter bar and type the filter "dns.flags.response == 1". Read the total number of displayed packets shown in the bottom-right status bar.
- The number of DNS query response packets captured is 90.

# 4. What is the IP address of the host which sent the most number of bytes?
- We go to statistics>endpoints>ipv4 then click on Tx Bytes column header to sort transmitted bytes in descending order.
- We then find that the IP with the most number of bytes is IP: 115.178.9.18.



# PCAP 2 

# 1. What is the WebAdmin password?

- We go to the filter bar and apply http filter.
- Right click packet 4123 (or any http post request).
- Choose follow>http stream to read the cleartext credentials.
- We see the webadmin password is "sbt123".

# 2. What is the version number of the attacker’s FTP server?

- We go to the filter bar and apply ftp filter.
- We look for the initial response banner string sent by the ftp server.
- The version we find is 1.5.5.

# 3. Which port was used to gain access to the victim Windows host?

- We go to filter bar and filter by ip.dst==192.168.56.103 and observe the destination port receiving incoming connections from the attacker.
- The port is 8081.

# 4. What is the name of a confidential file on the Windows host?

- We go and right click on packet 4128/4130.
- Choose follow>tcp stream to inspect the directory listing output.
- We discover a file named "Employee_Information_Confidential.txt".

# 5. What is the name of the log file that was created at 4:51 AM on the Windows host? 

- We go in the same tcp output on packet 4128.
- Follow the tcp stream and inspect the directory timestamps.
- We find files created on 7/16/2019 at 4:51 AM.
- The name of the file is LogFile.log


