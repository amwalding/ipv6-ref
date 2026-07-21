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
Support for Temporary IPv6 Addresses | | `$ sysctl net.inet6 \| grep temp` | | Different OS versions support different IPv6 addressing features
Ping an IPv6 Address | `$ ping6 -I eth0 IPV6ADDR` | `$ ping6 IPV6ADDR` | `$ ping -6 DOMAIN` | Use ICMP Ping to see if the target device is able to answer 
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
IP config | `$ ip -6 route get ADDRESS` or `$ sudo ifconfig {pipe} grep inet6` | | | 
IPv6 Packet Filtering | `$ sudo ip6tables -L -v --line-numbers` or `route -A inet6` | `$ netstat -r -f inet6` | `$ route print -6` or `$ netstat -r` | 
Any IPv6 Traffic? | `$ netstat -ps -6`| `netstat -s -f inet6` | `$ netstat -ps IPv6` | 
Any ICMPv6 Traffic? | | | `$ netstat -ps ICMPv6` | 
NETCAT | Listen `$ nc6 -lp 12345 -v -e "/bin/bash"` & Connect `$ nc6 localhost 12345` | | | 
SSH | `$ ssh -6 user@IPV6ADDR%eth0` | | | Using SSH in IPv6 mode
TCPDUMP | `$ sudo tcpdump -i eth0 -evv ip6` or `$ sudo tcpdum -i eth0 -evv proto ipv6` | | | 
TELNET | `$ telnet IPV6ADDR PORT` | | | 
Determining Address Type | `$ addr6 -a IPV6ADDR`  | | | Requires addr6 tool
Identifying the Flow ID generation policy | `$ sudo ./flow6 -i eth0 -v --flow-label-policy -d IPV6ADDR` | | | Requires flow6 tool

## Some Powershell Commands
Get-NetIPConfiguration, Get-NetIPAddress, Get-NetNeighbor, Get-NetRoute, and Test-NetConnection
