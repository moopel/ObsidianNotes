3/22/2025  12:05 PM
-
3/22/2025 1:15 PM 
Time Spent : 1 hour (didn't even mean to be right on the dot.)

Layer 1 - Physical Connection (Ethernet, Wifi) Packets contain Source Destination
Layer 2 - (Mac Address) PDUS(Frames) contain Source(MAC) and Destination(MAC) (Switch)
Layer 3 - (IP Address) PDUS(Packets)

Switches are better than hubs because they contain knowledge of what is connected to them through layer 2 (mac address) addresses. 
Hubs do not have this and send messages to everything connected to them

Messages being sent along the switch allows the switch to build its mac address table. 

Quiz:
	Question 1:
	Which of the following addresses will a switch use to populate the CAM table
		A. destination IP addresses
		B. source IP addresses
		C. destination MAC addresses 
		D. source MAC addresses
	Answer: ==source MAC addresses==
	Explanation: 
	A switch populates the Contact Addressable Memory table by recording the source MAC address of an inbound frame and the corresponding switch port the frame landed on.<br><br>Switches make forwarding decisions based on the destination MAC address contained in the frame header. The switch searches for an entry that matches the destination MAC address, if not found, the frame is forwarded to all ports except the port from which it received the frame.<br><br>My Explanation: The CAM table stores where mac addresses are for each of the switches ports. So if mac address 1 sends a message to mac address 2 over a switch then the switch will record that mac address 1 is on port(whatever port it is on). The destination doesn't mean anything because it doesn't know what port the destination is on unless that mac address has sent something over the switch.
	<br><br>Question 2: 
	Which of the following addresses will a switch use to make forwarding decisions?
		A. source MAC addresses
		B. source IP addresses
		C. destination IP addresses
		D. destination MAC addresses
	Answer: destination MAC addresses
	Explanation: A switch makes forwarding decisions based on the destination MAC address contained in the frame's header. The switch searches its CAM table for that MAC address and sends it to the port listed in the table if found or sends it to all ports if not found.
	<br>My Explanation: Switches look in their table for the destination MAC address which would have a port to send to if found. Source doesn't matter because you aren't forwarding back to source. 
[[Chuck CCNA Day 2]]