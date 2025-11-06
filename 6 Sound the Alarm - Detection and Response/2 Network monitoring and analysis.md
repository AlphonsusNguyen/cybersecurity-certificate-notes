## Network

- IoC: Indicators of compromise, observable evidence that there may have been a security incident. IOC helps security analysts detect network traffic abnormalities by providing a way to identify an attack
- Data exfiltration: Unauthorized transmission of data from a system
- Network _traffic_: Amount of data that moves across network.
- Network _data_: The data itself.

*Reminder: Packets contain three components: the header, the payload, and the footer.
## Monitoring

- Flow analysis: Monitoring if any unusual ports / packets / protocols are in use.
- Packet payload info: Orgs might look inside packets at the actual data.
- Temporal patterns: Is data transferred inside typical working hours?

## Security professionals use network traffic analysis:
 - To understand network traffic patterns
 - To monitor network activity
- To identify malicious activity

## Defensive measures

- Prevent attacker access
- Monitor network activity
- Protect assets
- Detect and stop exfiltration


## Network protocol analyzers:
use both software and hardware capabilities to capture network traffic and display it for security analysts to examine and analyze.
- First, packets must be collected from the network via the Network Interface Card (NIC), which is hardware that connects computers to a network, like a router. NICs receive and transmit network traffic, but by default they only listen to network traffic that’s addressed to them. To capture all network traffic that is sent over the network, a NIC must be switched to a mode that has access to all visible network data packets, which is called monitoring mode or promiscous mode.
- The network protocol analyzer collects the network traffic in raw binary format.
- Enabling promiscuous can expose your device to potential attacks because it allows sensitive information like passwords and other confidential data to be captured
  
## Packet captures  
"P-cap": Packet capture (unnecessary term, eh?)

Can come in following formats (copied verbatim):

1. **Libpcap** is a packet capture library designed to be used by Unix-like systems, like Linux and MacOS®. Tools like tcpdump use Libpcap as the default packet capture file format.
2. **WinPcap** is an open-source packet capture library designed for devices running Windows operating systems. It’s considered an older file format and isn’t predominantly used.
3. **Npcap** is a library designed by the port scanning tool Nmap that is commonly used in Windows operating systems.
4. **PCAPng** is a modern file format that can simultaneously capture packets and store data. Its ability to do both explains the “ng,” which stands for “next generation.”

## IP packet details

### IPV4

- Version: v4/6
- Internet Header Length: Length of header + options
- Type of Service: Priority
- Total Length
- Identified, Flags, Fragment Offset: Fragment = packet has been split into chunks, info on how to reassemble.
- Time To Live: How long until drop
- Protocol: E.g. tcp = 6
- Header checksum
- Source & destination address
- Options is sometimes used for debugging etc
- Finally, the actual data!

### IPV6

- Version
- Traffic class: Similar to type of service
- Flow label: Identifies if from specific source(?)
- Payload length
- Next header(?)
- Hop limit: Similar to TTL
- Source & destionation address

## tcpdump

`sudo tcpdump -i any -v -c 1`

- sudo: Need to run as superuser.
- tcpdump: Duh, want to use tcpdump.
- -i any: Interface to sniff on (any).
- -v: Verbose
- -c 1: Count, capture 1 packet
  
-i eth0: Capture data from the eth0 interface.
-nn: Do not attempt to resolve IP addresses or ports to names.This is best practice from a security perspective, as the lookup data may not be valid. It also prevents malicious actors from being alerted to an investigation.
-c9: Capture 9 packets of data and then exit.
port 80: Filter only port 80 traffic. This is the default HTTP port.
-w capture.pcap: Save the captured data to the named file.
&: This is an instruction to the Bash shell to run the command in the background

