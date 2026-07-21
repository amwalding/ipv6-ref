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
* [IPv6 Addressing](https://github.com/amwalding/ipv6-ref/blob/main/docs/addressing.md)<br />
* [SLAAC](https://github.com/amwalding/ipv6-ref/blob/main/docs/slaac.md)<br />
* [IPv6 Usage in Various OS Systems](https://github.com/amwalding/ipv6-ref/blob/main/docs/ipv6-os-commands)<br />
* [Some IPv6 Basic Networking Commands](https://github.com/amwalding/ipv6-ref/blob/main/README.md#some-ipv6-basic-networking-commands-by-os)<br />
* [Security in IPv6 Networking](https://github.com/amwalding/ipv6-ref/blob/main/README.md#locksecurity-in-ipv6-networking)<br />
  * [IPv6 Security Reading and References](https://github.com/amwalding/ipv6-ref/blob/main/README.md#notebookipv6-security-reading-and-references)<br />
  * [IPv6 Security Tools](https://github.com/amwalding/ipv6-ref/blob/main/README.md#hammer_and_wrenchipv6-security-tools)<br />
  * [IPv6 Tool Kit Command Examples](https://github.com/amwalding/ipv6-ref/blob/main/README.md#computeripv6-tool-kit-command-examples)<br />
  * [IPv6 addresses & domains Research/Investigation](https://github.com/amwalding/ipv6-ref/blob/main/README.md#magipv6-addresses--domains-researchinvestigation)<br />
  * [Domain Name System and Autonomous System Research/Investigation](https://github.com/amwalding/ipv6-ref/blob/main/README.md#magdomain-name-system-and-autonomous-system-researchinvestigation)<br />

## :link:Links to My Main Web Sites/IPv6 Repos
* The main CellStream, Inc. Web Site with tons of articles and how to's: https://www.cellstream.com
* The Online School of Network Sciences: https://cellstream.online (create a freee user account - lots of free References and more)
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



