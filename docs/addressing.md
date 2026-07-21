This is my IPv6 addressing reference.
Since most people learning IPv6 will have IPv4 knowledge, I start with a comparison of v4 to v6 and then dive in from there.

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
| **Documentation Prefix**| `2001:db8::/32`       | The original Documentation prefix                                                     |
|                         | `3FFF::/20`           | Newer Dcomentation Prefix                                                             |
| **Anycast**             | Not a separate prefix | Same address assigned to multiple nodes; nearest node responds.                       |
| **Deprecated**          | `FEC0::/10`           | Former Site-local prefix                                                              |

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
* IPv6 does not require address-conservation NAT for ordinary Internet access. Firewalls provide security policy independently of address translation. Translation may still be used for IPv4 interoperability through mechanisms such as NAT64 and 464XLAT.
* Fragmentation function removed from routers, replaced by Path MTU Discovery

## :vs:IPv6 vs. IPv4 Multicast Address Comparison Table
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
FF02::9	| IPv6/RIPng Routers	| 224.0.0.9	| RIPv2 Routers
FF02::A	| EIGRP Routers	|	224.0.0.10	| IGRP Routers
FF02::B	| Mobile Agents	|	224.0.0.11	| Mobile Agents
FF02::1:2	| DHCP Servers/Relay Agents	|	224.0.0.12	| DHCP Servers/Relay Agents
FF02::D	| All PIM Routers	|	224.0.0.13	| All PIM Routers
FF02::E	| RSVP-Encapsulation	|	224.0.0.14	| RSVP-Encapsulation

>[!NOTE]
>I should probably not be showing IPv4 and IPv6 multicast registries presented as a direct one-for-one conversion table.

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
