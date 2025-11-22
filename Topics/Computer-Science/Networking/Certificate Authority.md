___
**Certificate Authorities (CAs)** stands for **trusted third-party entities that issue X.509 digital certificates**. They are central to Public Key Infrastructure (PKI), enabling secure [[TLS & HTTPS|TLS]] communication by verifying that a public key truly belongs to the domain or organisation claiming it. CAs underpin global internet trust by validating domains before issuing certificates.

---
###### Keywords
- **X.509**
    - Standard defining certificate structure, fields, and trust chaining.
- **Root Certificate / Trust Anchor**
    - A self-signed certificate implicitly trusted by operating systems and browsers.
- **Intermediate Certificate (Sub-CA)**
    - Delegated signing authority used to reduce exposure of the root key.
- **End-Entity Certificate**
    - Certificate issued to servers or clients for authentication, or encryption.
- **Domain Validation (DV)**
    - Confirms domain control.
- **Organisation Validation (OV)**
    - Adds checks on business name, address, and ownership.
- **Extended Validation (EV)**
    - Highest assurance, verifying legal status, physical location, and authorised individuals.
- **DANE**
    - Uses DNSSEC to bind certificates or keys directly to DNS records.
- **DNSSEC**
    - Protects DNS integrity using cryptographic signatures.

---
## Description

Certificate Authorities operate at the core of the global trust ecosystem by issuing digital certificates conforming to the ITU-T X.509 standard. These certificates bind a public key to the entity controlling a domain, server, or service. Because CAs act as trusted intermediaries, operating systems and browsers rely on their signed certificates to authenticate servers during TLS handshakes.

Publicly trusted CAs typically large international organisations or government bodies maintain roots embedded in major trust stores like those maintained by Microsoft, Apple, and Mozilla. Alongside these global CAs, private or specialised PKIs also exist, such as the RPKI used by Regional Internet Registries and the IGTF used in distributed scientific computing. These systems rely on securely distributed root certificates rather than browser trust stores. However the CA model faces a core weakness: **any trusted CA can issue a certificate for any domain**

---
![[public-certificate-authority.png]]
![[certificate-authority-chain.png]]  

---
## Flashcards
#flashcards

**What is a Certificate Authority (CA)?** :: A trusted entity that issues X.509 certificates to authenticate public keys and domain ownership.

**Why are intermediate certificates used?** :: To avoid exposing root keys and to limit damage if a signing key is compromised.

**What is the main vulnerability of the CA model?** :: Any trusted CA can issue certificates for any domain, creating a single point of systemic trust.

**What does DNSSEC do?** :: Cryptographically verifies DNS data to prevent tampering.

**How does DANE enhance certificate security?** :: It allows domains to publish certificate or public-key information directly in DNSSEC-protected records.

**What differentiates DV, OV, and EV certificates?** :: DV verifies domain control; OV verifies organisational details; EV includes stronger legal and identity validation.