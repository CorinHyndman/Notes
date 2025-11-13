___
**OSI** Model stands for ***Open Systems Interconnection*** Model. It is a conceptual **framework** used to describe how data is transmitted and received across a network. The model divides the network communication process into **seven layers**, each with specific responsibilities and protocols. It helps standardize network functions to ensure compatibility between different systems and technologies.

---
###### Keywords
- **Layered Architecture**
    - A hierarchy of layers, each performing a specific network function.
- **Encapsulation**
    - Wrapping data with protocol information at each layer.
- **Decapsulation**
    - The reverse process at the receiving end, removing each layer’s header/trailer.
- **Protocol Data Unit (PDU)**
    - The form of data at each layer (e.g., bits, frames, packets, segments).
- **Interfaces**
    - Define how adjacent layers interact.
- **Services**
    - Functions provided by each layer to the layer above it.
- **Standards**
    - Defined by ISO to promote compatibility between vendors.
---

## The 7 Layers of the OSI Model
1. **Physical Layer (Layer 1)**
    - Deals with transmission of **raw bits** over a physical medium (cables, radio waves).
    - Defines **hardware specifications**, **voltages**, **data rates**, and **connectors**.
    - Examples: Ethernet cables, Hubs, Repeaters, Network Interface Cards (NICs).
2. **Data Link Layer (Layer 2)**
    - Responsible for **node-to-node** data transfer and **error detection**.
    - Breaks packets into **frames** and manages **MAC addressing**.
    - Examples: Ethernet, PPP, Switches, Bridges.
3. **Network Layer (Layer 3)**
    - Handles **routing** of data between devices across multiple networks.
    - Uses **logical addressing (IP)** and determines the best path.
    - Examples: IP, ICMP, Routers.
4. **Transport Layer (Layer 4)**
    - Ensures **end-to-end communication**, **data segmentation**, **error recovery**, and **flow control**.
    - Examples: TCP, UDP.
5. **Session Layer (Layer 5)**
    - Manages and controls **sessions** (connections) between applications.
    - Handles session **establishment**, **maintenance**, and **termination**.
    - Examples: NetBIOS, RPC, SQL Sessions.
6. **Presentation Layer (Layer 6)**
    - Translates data between the **application format** and **network format**.
    - Handles **data encryption, compression, and encoding**.
    - Examples: SSL/TLS, JPEG, ASCII, MPEG.
7. **Application Layer (Layer 7)**
    - Closest to the end user it provides **network services** to applications.
    - Examples: HTTP, FTP, SMTP, DNS, SSH.
---
## Data Flow

- **Sender (Encapsulation):** Data → Segments → Packets → Frames → Bits
- **Receiver (Decapsulation):** Bits → Frames → Packets → Segments → Data

Each layer adds or removes headers as the data moves through the stack.

---
![[what-is-osi-model.jpeg]]
![[layers-of-osi-model.png]]

---
## Flashcards
#flashcards

**What does OSI stand for?** :: Open Systems Interconnection.

**How many layers are there in the OSI model?** :: Seven layers.

**What is the main purpose of the OSI model?** :: To standardize communication functions and enable compatibility between different systems and protocols.

**Which layer deals with physical transmission of bits?** :: Physical Layer (Layer 1).

**What are the PDUs at each layer?** :: Physical – Bits | Data Link – Frames | Network  Packets | Transport – Segments | Session/Presentation/Application – Data

**Which layer handles routing?** :: Network Layer.

**Which layer ensures reliable delivery of data?** :: Transport Layer via TCP.

**What does the Presentation Layer do?** :: Translates, encrypts, and compresses data.

**Which layer provides end-user services like HTTP and FTP?** :: Application Layer.

**What is encapsulation?** :: The process of adding headers and sometimes trailers as data passes through network layers.

**What is decapsulation?** :: The process of removing headers and trailers as data moves up the stack on the receiving side.

**What devices operate at Layer 2 and Layer 3?** :: Switches (Layer 2) and Routers (Layer 3).