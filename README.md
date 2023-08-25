# ipv6-ref
Hello and Welcome!

This is my IPv6 References repository.  I try to add items here of interest to anyone learning about or using IPv6.  It is a bunch of different stuff that I hope helps everyone is some way.

If you have anything you would like to see added, please let me know.


## IPv4/IPv6 Comparison
Setting | IPv4 | IPv6
------------------------------------ |------------------------------------ | ---------------------------------------------
Address | 32 bits | 128 bits
Neighbor Discovery | ARP | NDP, ICMPv6
Auto configuration |  ICMP & DHCP | ICMPv6 & DHCPv6 (optional) 
Packet transmition | Broadcast / Multicast | Multicast
ICMP | ICMPv4 | ICMPv6
Fragmentation | Both in hosts and routers | Only in hosts
Local network | 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | ULA fc00::/7, fd00::/8
Headers Comparison 1 | Options | Extensions
Headers Comparison 2 | Next Header | Protocol
Headers Comparison 3 | Hop Limit | Time to Live
Loopback address | 127.0.0.1 | ::1
