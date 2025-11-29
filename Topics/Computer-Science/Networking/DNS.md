___
**DNS** stands for **Domain Name System**. It is the global system that translates human readable domain names into machine readable IP addresses, enabling browsers and clients to locate resources on the internet.
___
###### Keywords
- **Domain Name**
	- A human-friendly identifier (e.g., google.com_) mapped to an IP address.
- **Resolver**
	- A client component (usually provided by the OS/ISP) that queries DNS servers on behalf of applications.
- **Authoritative DNS Server**
	- Holds the official DNS records for a domain.
- **Root Servers**
	- The highest level of the DNS hierarchy; direct queries to TLD servers.
- **TLD (Top-Level Domain)**
	- The last part of a domain (e.g., _.com_, _.org_, _.net_).
- **DNS Record**
	- A structured data entry storing information like IP mappings.
- **TTL (Time to Live)**
	- Determines how long a DNS answer can be cached.
___
## Description
The Domain Name System is a distributed, hierarchical naming database that allows clients to resolve domain names into the network addresses required for routing traffic. DNS operates through recursive queries and a layered authority model. Its design allows for decentralized management of domain names while maintaining global consistency.
##### Stages of a DNS query
1. **Client Request** - An application (e.g., browser) asks the local resolver for the IP of a domain.
2. **Resolver Cache Check** - The resolver checks its cache if the entry exists and is valid (TTL not expired) then it returns it immediately.
3. **Recursive Query to Root** - If uncached the resolver queries a root server for the domain’s TLD direction.
4. **TLD Server Lookup** - The resolver asks the corresponding TLD server (e.g., _.com_) for the authoritative name servers of the domain.
5. **Authoritative Server Response** - The authoritative DNS server returns the final record.
6. **Return & Cache** - The resolver returns the answer to the client and caches it for future use.
___
![[dns-query-resolution-process.png]]
![[how-dns-works.jpg]]
___
## Flashcards
#flashcards

**What does DNS stand for and what does it do?** :: Domain Name System it translates human-readable domain names into IP addresses.

**What is a DNS resolver?** :: A component that performs DNS lookups on behalf of clients, often recursively.

**What is an authoritative DNS server?** :: The server that stores and provides the official DNS records for a domain.

**What is TTL in DNS?** :: Time to Live it determines how long a cached DNS response remains valid.

**What are root servers responsible for?** :: Directing DNS queries to the appropriate TLD name servers.