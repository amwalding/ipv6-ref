# IPv6 Reference and Repository
Hello and Welcome!

This is my IPv6 References repository.  I try to add items here of interest to anyone learning about or using IPv6.  It is a bunch of different stuff that I hope helps everyone is some way.
* Cheat Sheets
* Packet Captures
* RFC Documents
* more

If you have anything you would like to see added, please let me know.

## IPv6 Standards and RFCs
I have a ZIP file in the repo called IPv6 RFCs.zip that contains all the RFC's.  I update it from time to time.  Essentially it is a complete library of the IPv6 related RFC's in TXT format in one place to save time.

To see all the IPv6 Related RFC's click here: https://www.rfc-editor.org/search/rfc_search_detail.php?page=25&title=ipv6

That said, there are some really important IPv6 RFC's I have listed below.  This filtered list simply point to the online version of the RFC at the IETF web site.

Decription/Name | URL 
------------------------------------ | ---------------------------------------------
Original Dec 1998 IPv6 Spec | https://www.rfc-editor.org/rfc/rfc2460.txt
IPv6 Addressing Architecture | https://www.rfc-editor.org/rfc/rfc4291.txt
Neighbor Discovery for IPv6 | https://www.rfc-editor.org/rfc/rfc4861.txt
IPv6 Standardization | https://www.rfc-editor.org/rfc/rfc8200.txt

## :chart_with_upwards_trend:IPv6 Statistics of Interest 
Name | URL 
------------------------------------ | ---------------------------------------------
Google | https://www.google.com/intl/en/ipv6/statistics.html :+1:
APNIC Labs | https://stats.labs.apnic.net/ipv6/ :+1:
IPv6 BPG Table | https://bgp.potaroo.net/v6/as6447/ :+1:
More IPv6 Stats | http://ipv6-test.com/stats/
Cisco | https://6lab.cisco.com/stats/
Top Alexa by country | https://www.vyncke.org/ipv6status/ :+1:
NRO | https://www.nro.net/statistics
Ripe | https://www.ripe.net/publications/ipv6-info-centre/statistics-and-tools
World IPv6 Launch | http://www.worldipv6launch.org/measurements/
M.R.P. | http://www.mrp.net/ipv6_survey/
Microsoft IPv6 page | https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)?redirectedfrom=MSDN

## IPv6 Specific/Related/Capable Tools and Tool Sets
Description/Name | URL 
------------------------------------ | ---------------------------------------------
Wireshark | https://www.wireshark.org :+1:
Test your IPv6 Connectivity 1 | http://test-ipv6.com
Test your IPv6 Connectivity 2 | https://ipv6-test.com
IPv6 addresses calculator | https://packages.debian.org/jessie/ipv6calc
IPv6 Security Testing: thc-ipv6 | https://github.com/vanhauser-thc/thc-ipv6
IPv6 Security Testing: ipv6-toolkit | https://github.com/fgont/ipv6toolkit
Pinkie | http://www.ipuptime.net/pinkie/
Diagnostic tools | https://packages.debian.org/jessie/ndisc6
Scapy | http://www.secdev.org/projects/scapy/
Chiron | http://www.secfu.net/tools-scripts/
Scanners | Nmap / Metasploit / Scan6 / Halfscan6
Online scanner | http://www.ipv6scanner.com/
Online scanner | http://www.subnetonline.com/pages/ipv6-network-tools/online-ipv6-port-scanner.php
Neighbor discovery protocol monitor | https://packages.debian.org/jessie/ndpmon
Netcat6 | https://packages.debian.org/source/jessie/amd64/nc6
Scan detective | https://github.com/regulatre/ipv6-scan-detective
Rogue IPv6 router detector | https://github.com/xme/rrhunter
Evil foca | http://www.informatica64.com/
Firewall tester | https://github.com/timsgit/ipscan
Online Network Utilities | https://centralops.net/

## Comparing IPv4 to IPv6
Setting | IPv4 | IPv6
------------------------------------ |------------------------------------ | ---------------------------------------------
Address Length | 32 bits | 128 bits
Transmission Types | Unicast / Broadcast / Multicast | Unicast / Multicast
Neighbor Discovery | ARP | NDP, ICMPv6
Address Configuration |  Static/ICMP/DHCP | Static/ICMPv6/DHCPv6 (optional) 
ICMP | ICMPv4 | ICMPv6
Header Difference 1 | Variable Length w/Options | Fixed length (40 bytes) w/Extensions
Header Difference 2 | Header Checksum | No Header Checksum
Header Difference 3 | Protocol | Next Header
Header Difference 4 | TTL - Time to Live | Hop Limit
Header Difference 5 | Not applicable | Flow Label (generally not used) 
Fragmentation | Both in hosts and routers | Only in hosts, PMTU Discovery
Private Network Prefixes | 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | Site Local fec0::/10, ULA fc00::/7, fd00::/8 but no translation
Loopback Address | 127.0.0.1 | ::1
Multicast Address | 224.x.y.z | FF0s::/8, where s is the scope

## IPv6 Address Types - Prefixes/Special
Address Type | Binary Prefix | IPv6 Notation
------------------------------------ |------------------------------------ | ---------------------------------------------
Link-local unicast | 1111111010 | fe80::/64
Site-local unicast | 1111111011 | fec0::/10 (deprecated)
Unique local address (ULA) | 1111 110L | FC00::7 and FD00::7 
Unspecified | 00...0 (128 bits) | ::/128
Loopback | 00...1 (128 bits) | ::1/128
Multicast | 11111111 | ff00::/8
Global Unicast Address (GUA) | 0010 | 2xxx::/3 

### IPv6 Address Tools
Tool Description | Link/Reference
------------------------------------ |------------------------------------ 
Check your own GUA IPv6 Address (if you have one) | http://whatismyipv6address.com
Check out the full IPv6 Special Addresses | https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml
IPv6 Subnet Tool in Python | https://github.com/aipi/IPv6-subnet-calculator
IPv6 Subnet Calculator | https://subnetonline.com/pages/subnet-calculators/ipv6-subnet-calculator.php

### Notes on Addressing
* Every device selects a Link-local unicast address that is unique
* Interfaces can have multiple IPv6 Addresses
* Public prefix provided either by Router Advertisement or DHCPv6
* No more need of "NAT"
* Fragmentation function removed from routers, replaced by Path MTU Discovery

## IPv6 vs. IPv4 Multicast Address Comparison Chart
IPv6 Address | Description | IPv4 Address | Description
-------------------- | ------------------------------- | -------------------- | -------------------------------
na | na  | 224.0.0.0	| Multicast Network Address (Reserved)
FF02::1	| All Nodes on Link Local	|	224.0.0.1	| All systems on the subnetwork
FF02::2	| All Routers on Link Local	|	224.0.0.2	| All Routers on the subnetwork
FF02::3	| Unassigned	|	224.0.0.3	| Unassigned
FF02::4	| DVMRP Routers	|	224.0.0.4	| DVMRP Routers
FF02::5	| All OSPF Routers	|	224.0.0.5	| All OSPF Routers
FF02::6	| ll OSPF Designated Routers	|	224.0.0.6	| All OSPF Designated Routers
FF02::7	| ST Routers	|	224.0.0.7	| ST Routers
FF02::8	| ST Hosts	|	224.0.0.8	| ST Hosts
FF02::9	| RIPv2 Routers	| 224.0.0.9	| RIPv2 Routers
FF02::A	| EIGRP Routers	|	224.0.0.10	| IGRP Routers
FF02::B	| Mobile Agents	|	224.0.0.11	| Mobile Agents
FF02::C	| DHCP Servers/Relay Agents	|	224.0.0.12	| DHCP Servers/Relay Agents
FF02::D	| All PIM Routers	|	224.0.0.13	| All PIM Routers
FF02::E	| RSVP-Encapsulation	|	224.0.0.14	| RSVP-Encapsulation

## IPv6 Usage in Various OS Systems
Operating System | Link to Article
-------------------------------------- | ----------------------------------------------------------------------
Windows IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-windowslinux-command-line-examples/ :+1:
MAC OS IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-osx-command-line-examples/ :+1:
GNU/Linux IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-linux-command-line-examples/ :+1:
Neighbor Discovery (ND) Table in IPv6 Windows, Linux and MAC Machines | https://www.cellstream.com/2013/09/12/neighbor-discovery-nd-table-in-ipv6-windows-machines/
Enabling IPv6 on a Computer (Windows/MAC/Linux) | https://www.cellstream.com/2013/09/12/enabling-ipv6-on-a-computer/
Disabling IPv6 on Windows | https://www.cellstream.com/2013/09/12/disabling-ipv6-communications/


## Security in IPv6 Networking

### IPv6 Security References

### IPv6 Security Tools






