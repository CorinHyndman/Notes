___
**TLS (Transport Layer Security) & HTTPS (HTTP over TLS)** are the protocols responsible for securing communication on the web. TLS provides encryption and authentication while HTTPS is HTTP traffic sent over a TLS-protected channel.

---
###### Keywords
- **TLS Handshake**
    - The negotiation process where client and server agree on keys, algorithms, and authenticate the server.
- **HTTPS**
    - HTTP tunnelled through TLS to create a secure, encrypted web connection.
- **Cipher Suite**
    - A set of algorithms used for key exchange, encryption, and message authentication.
- [[Certificate Authorities|Certificate Authoritie (CA)]]
    - Trusted entity that issues X.509 certificates used for authentication.
- **Server Certificate**
    - An X.509 certificate proving the server controls the domain the client is connecting to.
- **TLS Versions**
    - TLS 1.2 and TLS 1.3 are the modern versions, with TLS 1.3 being faster and more secure.
- **Session Resumption**
    - Tickets or session IDs allowing faster reconnections without full handshakes.
- **Perfect Forward Secrecy (PFS)**
    - Ensures session keys cannot be recovered even if long-term keys are compromised.
- **SSL (Secure Sockets Layer)** 
	- SSL is an older cryptographic protocol designed to protect data transmitted between a client and a server by encrypting the communication channel. SSL has been replaced by TLS however the term “SSL” is still commonly used to refer to TLS-based secure connections.

---
## Description
**Transport Layer Security (TLS)** is the cryptographic protocol that enables secure communication between clients and servers. Its primary goals are encryption and authentication. TLS sits between the [[OSI Model|application layer and the transport layer]], ensuring that data exchanged between client and server cannot be read or modified.

**HTTPS** applies TLS to web traffic, protecting browser-based communication. When users visit an HTTPS website, the browser and server perform a TLS handshake (not to be confused with TCP handshake) to authenticate the server using its certificate, which is issued by a trusted [[Certificate Authority]]. Through this handshake, the parties agree on secure parameters and derive keys for encryption of all subsequent communication.

Trust in HTTPS fundamentally depends on the **public key infrastructure (PKI)**: specifically, the authenticity of server certificates signed by trusted entities. These certificates form a chain that leads back to a root certificate stored in the user's browser or operating system.

---

![[ssl-tls-handshake.webp]]
![[how-https-works.png]]
___
## Flashcards
#flashcards

**What does TLS provide?** :: Encryption, integrity protection and authentication.

**How does HTTPS relate to TLS?** :: HTTPS is HTTP transported over a TLS-encrypted session.

**What role do CAs play in TLS?** :: They issue X.509 certificates used to authenticate servers.

**What is the TLS handshake?** :: The negotiation process where client and server authenticate and establish shared encryption keys.

**What is Perfect Forward Secrecy?** :: A feature ensuring past sessions remain secure even if long-term keys are compromised.

**Why is server authentication important in HTTPS?** :: It prevents impersonation attacks by verifying the server's identity with a certificate.