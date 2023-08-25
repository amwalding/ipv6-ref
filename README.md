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

Name | URL 
------------------------------------ | ---------------------------------------------
Original Dec 1998 IPv6 Spec | https://www.rfc-editor.org/rfc/rfc2460.txt
IPv6 Addressing Architecture | https://www.rfc-editor.org/rfc/rfc4291.txt
Neighbor Discovery for IPv6 | https://www.rfc-editor.org/rfc/rfc4861.txt

## IPv6 Specific/Related/Capable Tool Sets
Name | URL 
------------------------------------ | ---------------------------------------------
IPv6 addresses calculator | https://packages.debian.org/jessie/ipv6calc
IPv6 Security Testing: thc-ipv6 | https://github.com/vanhauser-thc/thc-ipv6
IPv6 Security Testing: ipv6-toolkit | https://github.com/fgont/ipv6toolkit
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
Address type | Binary prefix | IPv6 notation
------------------------------------ |------------------------------------ | ---------------------------------------------
Link-local unicast | 1111111010 | fe80::/64
Site-local unicast | 1111111011 | fec0::/10 (redacted)
Unique local address (ULA) | 1111 110L | FC00::7 and FD00::7 
Unspecified | 00...0 (128 bits) | ::/128
Loopback | 00...1 (128 bits) | ::1/128
Multicast | 11111111 | ff00::/8
Global Unicast Address (GUA) | 0010 | 2xxx::/3 


* Every device selects a Link-local unicast address that is unique
* Interfaces can have multiple IPv6 Addresses
* Public prefix provided either by Router Advertisement or DHCPv6
* No more need of "NAT"
* Fragmentation function removed from routers, replaced by Path MTU Discovery


