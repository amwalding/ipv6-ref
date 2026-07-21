## ⚒️:SLAAC - Stateless Address Autoconfiguration
IPv6 devices can obtain addresses through multiple methods, depending on how the network is configured.

Here are the main IPv6 address assignment methods:

🔹 1. Stateless Address Autoconfiguration (SLAAC)
The device uses Router Advertisements (RA) from routers to auto-configure its own IP address.
Combines the network prefix from the RA and a host identifier (often derived from the MAC address).
RFC 8064 recommends stable, semantically opaque interface identifiers and recommends against embedding stable link-layer addresses.
Temporary addresses are separately standardized by RFC 8981.

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
* This DAD process is done for all IPv6 Addressing methods.
* DAD is an address-validation procedure used by multiple address-configuration methods; it is not itself SLAAC.

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
  * Forms a **global unicast address** (e.g., `2001:db8:abcd::1a2b:3c4d:5e6f:7a8b`)
  * Runs **DAD again** for this address.

### 🔹 5. **Optional: DNS Configuration**

* If the **O flag** is set, the host may use **stateless DHCPv6** to get **additional info** like DNS servers.
* DNS information can be delivered through RDNSS and DNSSL options in Router Advertisements. This is not dependent on the RA O flag being set.

### 🧠 Key Points:

* **"Stateless"** means routers don’t maintain state about individual clients.
* SLAAC is **lightweight** and suitable for **home or unmanaged networks**.
* It doesn’t provide everything—**DNS info often requires DHCPv6 or RDNSS options** in RA.

### Host Address Lifecycle Diagram:
Link-local creation → DAD → RS → RA → stable address → temporary address → DNS learning → preferred lifetime expires → address deprecated → valid lifetime expires  

