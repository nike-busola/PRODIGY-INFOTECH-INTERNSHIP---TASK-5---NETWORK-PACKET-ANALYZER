Highlights of the packet sniffer script: Ethical Disclaimer & Consent: The script begins with a detailed disclaimer stating that the tool is for educational use only and outlines strict terms for ethical usage. It prompts the user to accept these terms, and the program exits if the terms aren’t accepted.

Packet Processing Function: The packet_sniff(packet) function is the core of the sniffer. It checks if a captured packet contains a TCP layer using packet.haslayer(TCP).

It extracts important details from the packet: Source IP and Destination IP (from the IP layer). Source Port and Destination Port (from the TCP layer). Protocol (from the IP layer). Payload: Converts the TCP payload to a string and limits the display to the first 50 characters.

Output Handling: The packet details are formatted into a multi-line string and printed to the console. The same details are appended to a file (packet_sniffer_results.txt) for record keeping.

Sniffing Configuration: The script uses Scapy’s sniff() function with a filter set to capture only TCP packets. It processes packets using the packet_sniff function. The store=0 parameter is used to avoid storing the packets in memory, and count=10 limits the capture to 10 packets.

Result Confirmation: After capturing packets, the script prints the file name and location where the results are saved, confirming successful execution.
