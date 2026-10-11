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


