# IPv6 Reference and Repository :round_pushpin:
Hello and Welcome!

This is my IPv6 References repository.  I try to add items here of interest to anyone learning about or using IPv6.  It is a bunch of different stuff that I hope helps everyone is some way.
* Cheat Sheets
* Packet Captures
* RFC Documents
* more

If you have anything you would like to see added, please let me know.

## :card_index:Index of Items on This Page

* [IPv6 Standards and RFC's](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-standards-and-rfcs)<br />
* [IPv6 Statistics of Interest](https://github.com/amwalding/ipv6-ref/blob/main/README.md#chart_with_upwards_trendipv6-statistics-of-interest)<br />
* [IPv6 Specific/Related/Capable Tools and Tool Sets](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-specificrelatedcapable-tools-and-tool-sets)<br />
* [Comparing IPv4 to IPv6](https://github.com/amwalding/ipv6-ref/blob/main/README.md#comparing-ipv4-to-ipv6)<br />
* [IPv6 Address Types - Prefixes/Special](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-address-types---prefixesspecial)<br />
  * [IPv6 Address Tools](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-address-tools)<br />
  * [IPv6 Address Notes](https://github.com/amwalding/ipv6-ref/blob/main/README.md#notes-on-addressing)<br />
* [IPv6 vs. IPv4 Multicast Address Comparison Chart](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-vs-ipv4-multicast-address-comparison-chart)<br />
* [IPv6 Usage in Various OS Systems](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-usage-in-various-os-systems)<br />
* [Some IPv6 Basic Networking Commands](https://github.com/amwalding/ipv6-ref/blob/main/README.md#some-ipv6-basic-networking-commands-by-os)<br />

## :link:Links to My Main Web Sites
* The main CellStream, Inc. Web Site with tons of articles and how to's: https://www.cellstream.com
* The Online School of Network Sciences: https://www.netscionline.com (create a freee user account - lots of free References and more)

## :page_with_curl:IPv6 Standards and RFCs
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

## :hammer:IPv6 Specific/Related/Capable Tools and Tool Sets
Description/Name | URL 
------------------------------------ | ---------------------------------------------
Wireshark | https://www.wireshark.org :+1:
Use Google to test IPv6 | https://ipv6test.google.com/
Test your IPv6 Connectivity 1 | http://test-ipv6.com
Test your IPv6 Connectivity 2 | https://ipv6-test.com
Test your IPv6 Connectivity 3 | http://v6.testmyipv6.com/
Test your IPv6 Connectivity 4 | http://whatismyv6.com/
IPv6 Speed Test 1 | http://www.speedtest6.com/
IPv6 Speed Test 2 | http://ipv6-speedtest.net/
IPv6 addresses calculator | https://packages.debian.org/jessie/ipv6calc
IPv6 Security Testing: thc-ipv6 | https://github.com/vanhauser-thc/thc-ipv6
IPv6 Security Testing: ipv6-toolkit | https://github.com/fgont/ipv6toolkit
Pinkie | http://www.ipuptime.net/pinkie/
Diagnostic tools | https://packages.debian.org/jessie/ndisc6
IPv6 DNS Lookup Tool | http://www.webdnstools.com/dnstools/dns-lookup-ipv6
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

## :vs:Comparing IPv4 to IPv6
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

## :envelope:IPv6 Address Types - Prefixes/Special
Address Type | Binary Prefix | IPv6 Notation
------------------------------------ |------------------------------------ | ---------------------------------------------
Link-local unicast | 1111111010 | fe80::/64
Site-local unicast | 1111111011 | fec0::/10 (deprecated)
Unique local address (ULA) | 1111 110L | FC00::7 and FD00::7 
Unspecified | 00...0 (128 bits) | ::/128
Loopback | 00...1 (128 bits) | ::1/128
Multicast | 11111111 | ff00::/8
Global Unicast Address (GUA) | 0010 | 2xxx::/3 

### :hammer:IPv6 Address Tools
Tool Description | Link/Reference
------------------------------------ |------------------------------------ 
Check your own GUA IPv6 Address (if you have one) | http://whatismyipv6address.com
Check out the full IPv6 Special Addresses | https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml
IPv6 Subnet Tool in Python | https://github.com/aipi/IPv6-subnet-calculator
IPv6 Subnet Calculator | https://subnetonline.com/pages/subnet-calculators/ipv6-subnet-calculator.php

### :notebook:Notes on Addressing
* Every device selects a Link-local unicast address that is unique
* Interfaces can have multiple IPv6 Addresses
* Public prefix provided either by Router Advertisement or DHCPv6
* No more need of "NAT"
* Fragmentation function removed from routers, replaced by Path MTU Discovery

## :vs:IPv6 vs. IPv4 Multicast Address Comparison Chart
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

## :computer:IPv6 Usage in Various OS Systems
Operating System | Link to Article
-------------------------------------- | ----------------------------------------------------------------------
Windows IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-windowslinux-command-line-examples/ :+1:
MAC OS IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-osx-command-line-examples/ :+1:
GNU/Linux IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-linux-command-line-examples/ :+1:
Neighbor Discovery (ND) Table in IPv6 Windows, Linux and MAC Machines | https://www.cellstream.com/2013/09/12/neighbor-discovery-nd-table-in-ipv6-windows-machines/
Enabling IPv6 on a Computer (Windows/MAC/Linux) | https://www.cellstream.com/2013/09/12/enabling-ipv6-on-a-computer/
Disabling IPv6 on Windows | https://www.cellstream.com/2013/09/12/disabling-ipv6-communications/

## :computer:Some IPv6 Basic Networking Commands by OS
Replace IPV6ADDR with the IPv6 address in the commands below.
Replace DOMAIN with the Domain Name in the commands below.
Replace INTFC with the system name for the network interface below.

>[!NOTE]
>If you have any that I should add, please let me know.

>[!IMPORTANT]
>The best ping to test worldwide IPv6 connectivity `$ ping 2600::1` or `ping6 2600::1`  This is actually SPRINT's IPv6 address.

Action | Linux Command | MAC OS Command | Windows Command | Notes
------------------------------- | ----------------------------------- | --------------------------------- | ------------------------------------ | ----------------------------
Display IPv6 Settings | `$ sysctl net.ipv6` | `$ sysctl net.inet6` | | Attempt to show what IPv6 settings are present in the OS
General IP Interface Configuration 1 | `$ ifconfig` or `$ ip -6 a s INTFC` | `$ ifconfig` | `$ ipconfig` or `$ ipconfig /all` or `$ netsh interface ipv6 show addresses` | These are network interface configuration settings
General IPv6 Interface Configuration 2 | `$ ifconfig -a` or `$ cat /proc/net/if_inet6` | `$ ifconfig -a` or for a specific interface `$ ifconfig -L en0 inet6` | `$ netsh int ipv6 show global` | These are network interface configuration settings
Support for Temporary IPv6 Addresses | | `$ sysctl net.inte6 \| grep temp` | | Different OS versions support different IPv6 addressing features
Ping an IPv6 Address | `$ ping6 -I eth0 IPV6ADDR` | `$ ping6 IPV6ADDR` | `$ pathping -6 DOMAIN` | Use ICMP Ping to see if the target device is able to answer 
Domain ping | `$ ping6 -I eth0 DOMAIN` | `$ ping6 DOMAIN`| | Use ICMP Ping to see if a given domain name can be resolved and then reached
Traceroute | `$ traceroute6 DOMAIN` or `$ tracepath -n IPV6ADDR` | `$ traceroute6 DOMAIN`| `$ tracert -6 DOMAIN` | What is the path of routers to a given IPv6 destination
Traceroute EH-enabled | `$ sudo ./path6 -v -u 72 -d DOMAIN` | | | 
Traceroute with MTR | `$ mtr -6 DOMAIN` | | | 
Trace the path to discover the MTU | `$ tracepath6 DOMAIN` | | | Same as traceroute except with MTU allowed
View IPv6 Connections | `$ netstat -A inet6` | | | What IPv6 connections exist on the system
Display the Routing Table | `$ ip -6 route` or `$ netstat -rnA inet6` or `$ sudo route -A inet6` | `$ netstat -r -f inet6` | `$ route print -6` | Display the routing table of the system
Display Neighbor Discovery Cache | `$ ip -6 neigh show` | | | Display the Neighbor Discovery cach of the system (the replacement of the ARP cache)
Flush the Neighbor Discovery Cache | `$ ip -6 neigh flush` | | | Clear the Neighbor cache to force rediscovery
Display the PMTU information | `$ ip route get IPV6ADDR` and `$ tracepath -n IPV6ADDR`| | `$ netsh interface ipv6 show destinationcache address` | Attempt to display the Path MTU information for a given destination
DNS lookup | `$ host DOMAIN` | Check DNS `$ scutil --dns \| grep nameserver \| grep "::"` Lookup: `$ dig AAAA DOMAIN` | | Looking up IPv6 DNS records
IP show | `$ ip -6 addr` or `$ sudo ifconfig` | `$ grep inet6` | | | 
IPv6 Routing tables/IPtables | `$ sudo ip6tables -L -v --line-numbers` or `route -A inet6` | `$ netstat -r -f inet6` | `$ route print -6` or `$ netstat -r` | 
Any IPv6 Traffic? | `$ netstat -ps -6`| `netstat -s -f inet6` | `$ netstat -ps IPv6` | 
Any ICMPv6 Traffic? | | | `$ netstat -ps ICMPv6` | 
NETCAT | Listen `$ nc6 -lp 12345 -v -e "/bin/bash"` & Connect `$ nc6 localhost 12345` | | | 
SSH | `$ ssh -6 user@IPV6ADDR%eth0` | | | Using SSH in IPv6 mode
TCPDUMP | `$ sudo tcpdump -i eth0 -evv ip6` or `$ proto ipv6` | | | 
TELNET | `$ telnet IPV6ADDR PORT` | | | 
Determining Address Type | `$ addr6 -a IPV6ADDR`  | | | Requires addr6 tool
Identifying the Flow ID generation policy | `$ sudo ./flow6 -i eth0 -v --flow-label-policy -d IPV6ADDR` | | | Requires flow6 tool

## Security in IPv6 Networking
> [!WARNING]
> The content below is provided as educational information.
> Executing some of the commands shown with certain tools installed can be considered malicious by others.
> Please use caution when using any of the information below.

I would like to start with the following statement: IPv6 should not be considered any more or less secure than IPv4.

That said, there are known vulnerabilities in IPv6 with a number of exploits.  Below are some IPv6 security references and tools.

### IPv6 Security Reading and References
Reference Name | URL/RFC
------------------------------------ | ---------------------------------------------
IPv6 Fragmentation Attack | https://www.cellstream.com/2019/08/06/example-ipv6-frag-attack/
Example IPv6 SYN Flood Attack | https://www.cellstream.com/2019/08/05/example-ipv6-syn-flood-attack/
Observations on the Dropping of Packets with IPv6 Extension Headers in the Real World | https://datatracker.ietf.org/doc/html/rfc7872
Rogue IPv6 Router Advertisement | https://www.rfc-editor.org/rfc/rfc6104.txt
Neighbor Discovery Problems | https://www.rfc-editor.org/rfc/rfc6583.txt
Network Reconnaissance in IPv6 | https://www.rfc-editor.org/rfc/rfc7707.txt

### IPv6 Security Tools
>[!NOTE]
>I believe both these tool sets are standard in Parrot Linux, you can add the ipv6toolkit
>to Kali with `$ sudo apt install ipv6toolkit`

Name | Link URL
------------------------------------- | --------------------------------------------
IPv6 Security Testing: thc-ipv6 | https://github.com/vanhauser-thc/thc-ipv6
IPv6 Security Testing: ipv6-toolkit | https://github.com/fgont/ipv6toolkit

### IPv6 Tool Kit Command Examples
Action | Command | Notes
-------------------------------------- | ------------------------------------------------------ | -------------------------------------------------
DAD (Duplicate Address Detection) | `$ sudo ./na6 -i eth0 --accept-src ::/128 --solicited --override --listen --verbose` or `$ sudo ./dos-new-ip6 eth0` | DAD is the mechanism of IPv6 stateless autoconfiguration to detect whether an IPv6 address exists on the network. Every time a new computer asks about IPv6 existence, the attacker replies and claims that he is that IPv6. The new computer cannot join the network since it does not have IPv6 address. It use ICMPv6 neighbor solicitation which sends to all nodes multicast address
Neighbor Solicitation | `$ sudo ./flood_solicitate6 eth0 TARGETIPv6ADDR` | Flood the network with neighbor solicitations. If no target is supplied, query address will be 'ff02::1'








