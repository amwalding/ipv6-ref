# ipv6-ref
Hello and Welcome!

This is my IPv6 References repository.  I try to add items here of interest to anyone learning about or using IPv6.  It is a bunch of different stuff that I hope helps everyone is some way.

If you have anything you would like to see added, please let me know.


## Comparing IPv4 to IPv6
Setting | IPv4 | IPv6
------------------------------------ |------------------------------------ | ---------------------------------------------
Address Length | 32 bits | 128 bits
Transmission Types | Unicast / Broadcast / Multicast | Unicast / Multicast
Neighbor Discovery | ARP | NDP, ICMPv6
Address Configuration |  Static/ICMP/DHCP | Static/ICMPv6/DHCPv6 (optional) 
ICMP | ICMPv4 | ICMPv6
Headers Difference 1 | Options | Extensions
Headers Difference 2 | Next Header | Protocol
Headers Difference 3 | Hop Limit | Time to Live
Fragmentation | Both in hosts and routers | Only in hosts, PMTU Discovery
Private Network Prefixes | 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | ULA fc00::/7, fd00::/8 but no translation
Loopback Address | 127.0.0.1 | ::1
Multicast Address | 224.x.y.z | FF0s::/8, where s is the scope
