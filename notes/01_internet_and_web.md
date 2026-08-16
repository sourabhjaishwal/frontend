# Internet & Web Basics

> **Purpose:** Quick revision and understanding of how the Internet and Web work.

# 1. History of the Web

The Web has evolved from simple, read-only websites into interactive platforms and, potentially, decentralized applications.

## 1.1 Web 1.0 — Read-Only Web

### Definition

**Web 1.0** was the early stage of the Web where websites mainly provided **static information** that users could only read.

### Key Points

- Mostly static HTML pages.
- Very little or no user interaction.
- Users were mainly **consumers of information**.
- Content was created and controlled by website owners.

### Real-World Example

An old news website or company information page that only displayed fixed text and images.

```text
Website Owner
     |
     | Publishes Content
     v
  Website
     |
     v
   User
(Read Only)
```

---

## 1.2 Web 2.0 — Interactive and Social Web

### Definition

**Web 2.0** introduced interactive websites where users could **create, share, and interact with content** instead of only consuming it.

### Key Points

- User-generated content.
- Social media and online communities.
- Collaboration and sharing.
- Dynamic and interactive websites.

### Real-World Examples

- Facebook
- YouTube
- Wikipedia
- Blogs

```text
        Users
       /  |  \
      v   v   v
   Create Share Interact
      \   |   /
       v  v  v
     Web Platform
```

### Main Focus

**Community + Sharing + Collaboration**

---

## 1.3 Web 3.0 — Decentralized Web

### Definition

**Web 3.0** generally refers to a vision of a more decentralized web where technologies such as **blockchain** can reduce dependence on centralized platforms and enable users to have greater control over digital assets and data.

### Key Points

- Decentralization.
- Blockchain technology.
- Smart contracts.
- Digital assets and tokens.
- Decentralized applications (dApps).

### Examples

- Cryptocurrencies.
- Decentralized applications.
- Smart contracts.
- Some metaverse projects.

```text
Traditional Web

User ---> Company Server
             |
             v
          Data


Decentralized Web

       Network of Computers
       /        |        \
      v         v         v
   Node A     Node B     Node C
       \        |        /
        \       |       /
          Shared Network
```

> **Note:** Web 3.0 is still an evolving concept, and not every modern web application is decentralized or blockchain-based.

---

# 2. How Computers Communicate

### Definition

Computers communicate over the Internet by exchanging data using **network protocols**, addresses, and networking devices.

The foundation of Internet communication is the **TCP/IP protocol suite**.

### Key Concepts

- **IP Address:** Identifies a device or server on a network.
- **Protocols:** Define rules for communication.
- **Packets:** Small pieces into which data is divided.
- **Routers:** Forward packets between networks.
- **Switches:** Connect devices within a local network.
- **Cables/Wi-Fi:** Carry data between devices and networks.

---

# 3. How Data Travels Across the World

### Definition

When data is sent over the Internet, it is divided into small **packets** that travel through different network devices and are reassembled at the destination.

### How It Works

```text
Your Device
    |
    v
Wi-Fi / Local Network
    |
    v
Router
    |
    v
ISP
    |
    v
Internet
    |
    v
Routers
    |
    v
Undersea Fiber Cables
    |
    v
Destination Network
    |
    v
Server
```

### Real-World Example

When you send a WhatsApp message from India to someone in the USA:

1. Your device creates the data.
2. The data is divided into packets.
3. Packets travel through routers and network infrastructure.
4. They may travel through undersea fiber-optic cables.
5. The destination server/device receives the packets.
6. The data is reconstructed.

If one network route becomes unavailable, routing systems can choose another available route.

---

# 4. Important Networking Concepts

## 4.1 IP Address

### Definition

An **IP address** is a numerical address used to identify a device or network interface for communication over an IP network.

### Real-World Example

An IPv4 address may look like:

```text
142.250.77.206
```

Think of it as similar to a **postal address** that helps network traffic reach the correct destination.

---

## 4.2 MAC Address

### Definition

A **MAC address** is a hardware-level identifier associated with a network interface.

### Real-World Example

A network card may have an address such as:

```text
A4:5E:60:12:34:56
```

### Simple Comparison

```text
IP Address
   |
   +-- Used for network communication
   +-- Can change depending on the network

MAC Address
   |
   +-- Identifies a network interface
   +-- Assigned to the network hardware
```

> **Note:** A MAC address is not literally permanent in every situation; modern devices can use randomized MAC addresses, especially for Wi-Fi privacy.

---

## 4.3 Domain Name

### Definition

A **domain name** is a human-readable name used to access a website instead of remembering its IP address.

### Examples

```text
google.com
amazon.in
github.com
```

### Real-World Example

Instead of remembering:

```text
142.250.77.206
```

you can type:

```text
google.com
```

---

## 4.4 Routing

### Definition

**Routing** is the process of determining where network packets should go and forwarding them through appropriate network paths.

### Real-World Example

A router works somewhat like a **traffic controller** that decides which road network traffic should use to reach its destination.

```text
Packet
  |
  v
Router A
 /     \
v       v
Path 1  Path 2
  \     /
   v   v
Destination
```

---

## 4.5 Router

### Definition

A **router** connects different networks and forwards packets toward their destination.

### Real-World Example

Your home Wi-Fi router connects your local devices to your ISP and the Internet.

---

## 4.6 Switch

### Definition

A **network switch** connects multiple devices within a local network and forwards data to the appropriate device.

### Real-World Example

In an office, a switch can connect multiple computers, printers, and other devices to the same local network.

```text
PC 1 ----\
PC 2 -----\
PC 3 ------> Switch ----> Router ----> Internet
Printer ---/
```

---

## 4.7 Undersea Cables

### Definition

**Undersea fiber-optic cables** are physical cables laid beneath oceans that carry large amounts of Internet traffic between countries and continents.

### Real-World Example

International Internet communication between India and the USA can travel through submarine cable networks.

> The Internet is not "wireless" everywhere. A significant amount of global Internet traffic travels through physical fiber-optic infrastructure.

---

# 5. ISP — Internet Service Provider

### Definition

An **ISP** is a company that provides users with access to the Internet.

### Examples

- Jio
- Airtel
- BSNL

### Real-World Example

```text
Your Device
     |
     v
Wi-Fi Router
     |
     v
ISP
     |
     v
Global Internet
```

Without an Internet connection provided by an ISP or another network provider, your device cannot normally access the public Internet.

---

# 6. DNS — Domain Name System

### Definition

**DNS** is a system that translates human-readable domain names into IP addresses that computers can use to locate servers.

### Real-World Example

You enter:

```text
google.com
```

DNS helps find the corresponding IP address.

```text
You type:
google.com
     |
     v
    DNS
     |
     v
IP Address
     |
     v
Google Server
```

### Simple Analogy

DNS is like the **phonebook of the Internet**.

```text
Person Name  ---> Phone Number
Domain Name  ---> IP Address
```

### Why DNS Is Needed

Without DNS, users would have to remember IP addresses for every website.

---

# 7. How ISP and DNS Work Together

### Definition

When you access a website, DNS helps identify the server's IP address, while your network connection through an ISP allows your device to communicate with that server.

### Example

```text
1. User types google.com
          |
          v
2. Browser needs IP address
          |
          v
3. DNS lookup
          |
          v
4. IP address found
          |
          v
5. Network connection through ISP
          |
          v
6. Request reaches server
          |
          v
7. Server sends response
```

> **Important:** DNS resolution and ISP connectivity are separate concepts, but both participate in accessing Internet resources.

---

# 8. Client-Server Architecture

## 8.1 Client-Server Model

### Definition

The **client-server model** is an architecture where a client requests data or services, and a server processes the request and sends back a response.

### Real-World Example

When you open Google in your browser:

```text
Client
(Browser)
    |
    | Request
    v
Server
(Google)
    |
    | Response
    v
Client
(Browser)
```

### Basic Rule

> **Client asks → Server responds**

---

## 8.2 Client

### Definition

A **client** is a device or software application that requests data or services from a server.

### Examples

- Web browser.
- Mobile application.
- Desktop application.

### Responsibilities

- Sends requests.
- Receives responses.
- Displays or uses the received data.

---

## 8.3 Server

### Definition

A **server** is a computer system or software service that receives requests, processes them, and provides data or services to clients.

### Responsibilities

- Accepts requests.
- Runs application logic.
- Accesses databases.
- Returns responses.

---

# 9. HTTP Request-Response Cycle

### Definition

The **HTTP request-response cycle** is the process in which a client sends an HTTP request to a server, and the server returns an HTTP response.

### Flow

```text
User Action
    |
    v
Browser
    |
    | HTTP Request
    v
Web Server
    |
    | Process Request
    v
Application / Database
    |
    | HTTP Response
    v
Browser
    |
    v
Display Result
```

### Example

You visit:

```text
example.com
```

The browser may request:

```text
GET / HTTP/1.1
```

The server responds with resources such as:

- HTML
- CSS
- JavaScript
- Images
- JSON data

---

# 10. What Happens When You Visit a Website?

A simplified process looks like this:

```text
1. Enter URL
       |
       v
2. Browser processes URL
       |
       v
3. DNS resolves domain
       |
       v
4. Browser connects to server
       |
       v
5. Browser sends HTTP/HTTPS request
       |
       v
6. Server processes request
       |
       v
7. Server sends response
       |
       v
8. Browser downloads required resources
       |
       v
9. Browser renders webpage
```

### Example

When you type:

```text
www.example.com
```

the browser needs to find the appropriate server, communicate with it, request resources, and then render the received content.

---

# 11. Frontend vs Backend

## 11.1 Frontend

### Definition

The **frontend** is the part of a web application that runs in the user's browser and that users directly see and interact with.

### Technologies

- HTML
- CSS
- JavaScript

### Real-World Example

A login page containing:

```text
+----------------------+
|      Login           |
|                      |
| Email:    [       ]  |
| Password: [       ]  |
|                      |
|       [ Login ]      |
+----------------------+
```

This visible interface is frontend.

---

## 11.2 Backend

### Definition

The **backend** is the server-side part of an application that handles business logic, authentication, APIs, and data processing.

### Responsibilities

- Authentication.
- Authorization.
- Business logic.
- Database operations.
- API handling.

### Real-World Example

When you enter your login credentials:

```text
Frontend
   |
   | Email + Password
   v
Backend
   |
   | Check Credentials
   v
Database
   |
   | User Found?
   v
Backend
   |
   v
Frontend
```

---

# 12. Static vs Dynamic Websites

## 12.1 Static Website

### Definition

A **static website** serves mostly pre-created files and generally displays the same content to users unless the files are manually changed.

### Examples

- Simple portfolio.
- Basic company information page.
- Documentation site.

### Flow

```text
Browser
   |
   | Request
   v
Web Server
   |
   | Pre-built HTML
   v
Browser
```

### Advantages

- Simple to build.
- Fast.
- Easy to host.
- Often inexpensive.

---

## 12.2 Dynamic Website

### Definition

A **dynamic website** generates or changes content based on user actions, application logic, or stored data.

### Examples

- Facebook feed.
- Amazon product pages.
- Online banking applications.

### Flow

```text
User
 |
 v
Frontend
 |
 v
Backend
 |
 +----> Database
 |
 v
Dynamic Response
 |
 v
Frontend
```

### Example

When you open an e-commerce website, the products displayed may depend on:

- Database data.
- Search queries.
- User preferences.
- Availability.
- Location.

---

# 13. Web Hosting

### Definition

**Web hosting** is a service that provides server infrastructure where website files and applications are stored and made accessible over the Internet.

### Real-World Example

```text
Your Website Files
        |
        v
Hosting Server
        |
        v
Internet
        |
        v
Users
```

Hosting providers include services from companies such as Hostinger, AWS, GoDaddy, Google Cloud, and Microsoft Azure.

### Important Note

A domain name and hosting are different:

```text
Domain
   |
   | "Where?"
   v
example.com

Hosting
   |
   | "Where are files stored?"
   v
Server
```

---

# 14. Types of Web Hosting

## 14.1 Shared Hosting

### Definition

**Shared hosting** places multiple websites on the same physical server and shares its resources.

### Best For

- Small websites.
- Beginners.
- Simple portfolios.

### Advantage

Lower cost.

### Disadvantage

Resources are shared with other websites.

---

## 14.2 VPS / Dedicated Hosting

### Definition

**VPS hosting** provides an isolated virtual server environment, while **dedicated hosting** provides an entire physical server to one customer.

### Best For

- Growing applications.
- Websites requiring more control.
- Applications with higher resource requirements.

---

## 14.3 Cloud Hosting

### Definition

**Cloud hosting** runs applications using a scalable infrastructure of connected computing resources rather than relying on a single traditional server.

### Examples

- AWS.
- Google Cloud.
- Microsoft Azure.

### Key Benefit

```text
More Traffic
     |
     v
More Resources
     |
     v
Better Scalability
```

---

# 15. TCP — Transmission Control Protocol

### Definition

**TCP** is a connection-oriented transport protocol that provides reliable and ordered delivery of data between applications.

### Key Features

- Reliable delivery.
- Error detection.
- Retransmission of lost data.
- Maintains packet order.
- Connection-oriented communication.

### Real-World Uses

- Web communication.
- Email.
- File transfers.

### Simple Flow

```text
Sender
  |
  | Packet 1
  | Packet 2
  | Packet 3
  v
Network
  |
  v
Receiver
  |
  | Reassembles in order
  v
Complete Data
```

If a packet is lost, TCP can retransmit it.

---

# 16. TCP 3-Way Handshake

### Definition

The **TCP 3-way handshake** is the process used to establish a TCP connection between a client and server.

### Steps

```text
Client                         Server
  |                              |
  | -------- SYN --------------> |
  |                              |
  | <------ SYN + ACK ---------- |
  |                              |
  | -------- ACK --------------> |
  |                              |
  |      Connection Ready        |
```

### 1. SYN

Client requests to establish a connection.

### 2. SYN-ACK

Server acknowledges the request and agrees to establish the connection.

### 3. ACK

Client confirms the server's response.

The TCP connection is now established.

---

# 17. UDP — User Datagram Protocol

### Definition

**UDP** is a connectionless transport protocol that prioritizes speed and low latency over guaranteed delivery and ordering.

### Key Features

- No connection setup.
- No 3-way handshake.
- Low overhead.
- Fast communication.
- No guarantee that packets arrive.
- Packets may arrive out of order.

### Real-World Uses

- Online gaming.
- Live video streaming.
- Voice calls.
- Video calls.

### Simple Flow

```text
Client
  |
  | Packet 1 ---->
  | Packet 2 ---->
  | Packet 3 ---->
  v
Server
```

The sender does not wait for confirmation that every packet was received.

---

# 18. TCP vs UDP

| Feature        | TCP                       | UDP                       |
| -------------- | ------------------------- | ------------------------- |
| Connection     | Connection-oriented       | Connectionless            |
| Handshake      | 3-way handshake           | No handshake              |
| Reliability    | Reliable                  | No delivery guarantee     |
| Ordering       | Maintains order           | No ordering guarantee     |
| Retransmission | Yes                       | No                        |
| Speed          | Generally slower          | Generally faster          |
| Best For       | Reliable data transfer    | Low-latency communication |
| Examples       | Web, email, file transfer | Gaming, streaming, calls  |

### Easy Memory Trick

```text
TCP = Accuracy & Reliability
UDP = Speed & Low Latency
```

---

# 19. HTTP — HyperText Transfer Protocol

### Definition

**HTTP** is an application-layer protocol used for communication between clients and servers on the Web.

It defines how clients make requests and how servers return responses.

### Basic Flow

```text
Browser
   |
   | HTTP Request
   v
Server
   |
   | HTTP Response
   v
Browser
```

---

# 20. HTTP Versions

## HTTP/1.0

- Introduced early HTTP communication.
- Typically created a new TCP connection for each request.

## HTTP/1.1

- Introduced persistent connections.
- Multiple requests could reuse a connection.
- Improved efficiency compared to HTTP/1.0.

## HTTP/2

- Supports multiplexing.
- Multiple streams can use a single connection.
- Uses a binary framing layer.
- Improves performance.

## HTTP/3

- Uses **QUIC** as its transport protocol.
- QUIC runs over UDP.
- Designed to improve performance and connection handling for modern Internet applications.

### Evolution

```text
HTTP/1.0
   |
   v
HTTP/1.1
   |
   v
HTTP/2
   |
   v
HTTP/3
```

---

# 21. HTTP Status Codes

### Definition

An **HTTP status code** is a number sent by a server to indicate the result or status of an HTTP request.

| Range | Meaning       | Examples      |
| ----- | ------------- | ------------- |
| 1xx   | Informational | 100 Continue  |
| 2xx   | Success       | 200 OK        |
| 3xx   | Redirection   | 301, 302      |
| 4xx   | Client Error  | 400, 401, 404 |
| 5xx   | Server Error  | 500, 503      |

### Common Codes

**200 OK**
The request was successful.

**301 Moved Permanently**
The resource has permanently moved to another URL.

**302 Found**
The resource is temporarily available at another URL.

**400 Bad Request**
The server cannot process the request because it is invalid.

**401 Unauthorized**
Authentication is required or has failed.

**404 Not Found**
The requested resource could not be found.

**500 Internal Server Error**
The server encountered an unexpected problem.

**503 Service Unavailable**
The server is temporarily unable to handle the request.

---

# 22. HTTPS — HyperText Transfer Protocol Secure

### Definition

**HTTPS** is HTTP communication protected using **TLS encryption**, helping secure data exchanged between a client and server.

### Why HTTPS Is Important

It helps provide:

- **Confidentiality** — Others cannot easily read encrypted traffic.
- **Integrity** — Helps detect unauthorized modification of data.
- **Authentication** — Certificates help verify the identity of the website.

### Example

```text
HTTP

Browser -------- Plain HTTP --------> Server
                  |
                  v
             Less Secure


HTTPS

Browser ===== Encrypted TLS ========> Server
                  |
                  v
              More Secure
```

HTTPS is especially important for:

- Banking.
- Online payments.
- Login pages.
- Personal information.

---

# 23. SSL/TLS

### Definition

**TLS (Transport Layer Security)** is a cryptographic protocol used to secure communication over networks; **SSL** is its older predecessor.

### Important Concepts

```text
HTTPS
  |
  v
HTTP + TLS
  |
  +--> Encryption
  +--> Authentication
  +--> Data Integrity
```

### Encryption

Makes data difficult for unauthorized parties to read.

### Authentication

Helps verify that you are communicating with the intended website.

### Integrity

Helps ensure that data has not been modified during transmission.

> **Remember:** Modern HTTPS uses TLS. SSL is an older technology that has been deprecated.

---

# 24. Proxy Server

### Definition

A **proxy server** acts as an intermediary between a client and another server, forwarding requests on behalf of the client.

### Flow

```text
Client
  |
  v
Proxy
  |
  v
Internet / Server
```

### Common Uses

- Content filtering.
- Network access control.
- Caching.
- Hiding the client's IP from the destination in some configurations.

### Real-World Example

A school or office may use a proxy to filter or control access to websites.

---

# 25. Reverse Proxy

### Definition

A **reverse proxy** sits in front of one or more backend servers and receives client requests on their behalf.

### Flow

```text
Client
  |
  v
Reverse Proxy
  |
  +------> Server 1
  |
  +------> Server 2
  |
  +------> Server 3
```

### Common Uses

- Load balancing.
- Security.
- SSL/TLS termination.
- Caching.
- Routing requests to different backend services.

### Example

A popular website may have thousands of users connecting to a reverse proxy, which distributes requests across multiple backend servers.

---

# 26. Proxy vs Reverse Proxy

| Proxy                                 | Reverse Proxy                            |
| ------------------------------------- | ---------------------------------------- |
| Represents the client                 | Represents the server                    |
| Sits between client and Internet      | Sits between clients and backend servers |
| Can hide client identity              | Can hide backend server details          |
| Used for filtering and access control | Used for load balancing and security     |

### Easy Memory Trick

```text
Proxy        → Protects / represents CLIENT
Reverse Proxy → Protects / represents SERVER
```

---

# 27. VPN — Virtual Private Network

### Definition

A **VPN** creates an encrypted connection between your device and a VPN server, helping protect network traffic and making websites see the VPN server's IP address instead of your device's public IP.

### Simplified Flow

```text
Without VPN

Your Device
    |
    v
    ISP
    |
    v
Internet
    |
    v
Website


With VPN

Your Device
    |
    | Encrypted Connection
    v
VPN Server
    |
    v
Internet
    |
    v
Website
```

### Common Uses

- Protecting traffic on untrusted networks.
- Remote access to private company networks.
- Changing the apparent public IP location.
- Accessing services available to a particular region, where permitted.

### Real-World Example

If you connect to a VPN server in the USA while physically located in India, websites may see the VPN server's US-based IP address.

> **Important:** A VPN does not make you completely anonymous. Your VPN provider may still be able to observe certain metadata or traffic depending on its policies and technical setup.

---

# 28. Complete Internet Request Flow

The following diagram combines many concepts from these notes:

```text
                  USER
                    |
                    v
              Web Browser
                    |
                    | 1. Enter Domain
                    v
                  DNS
                    |
                    | 2. Find IP Address
                    v
             IP Address Found
                    |
                    v
           ISP / Network Connection
                    |
                    v
                 Router
                    |
                    v
              Internet
                    |
                    v
          Reverse Proxy / CDN
                    |
                    v
              Web Server
                    |
                    v
             Backend Server
                    |
                    v
                Database
                    |
                    | Data
                    v
             Backend Server
                    |
                    v
              Web Server
                    |
                    | HTTP/HTTPS Response
                    v
              Web Browser
                    |
                    v
            Rendered Web Page
```

---

# 29. Quick Revision Summary

| Concept         | Simple Meaning                                 |
| --------------- | ---------------------------------------------- |
| Web 1.0         | Read-only, mostly static Web                   |
| Web 2.0         | Interactive and social Web                     |
| Web 3.0         | Vision of a more decentralized Web             |
| IP Address      | Network address used for communication         |
| MAC Address     | Identifier associated with a network interface |
| Domain Name     | Human-readable website address                 |
| DNS             | Converts domain names into IP addresses        |
| Router          | Forwards packets between networks              |
| Switch          | Connects devices within a local network        |
| ISP             | Provides Internet connectivity                 |
| Routing         | Determines paths for network traffic           |
| Packet          | Small unit of transmitted data                 |
| Client          | Requests data or services                      |
| Server          | Processes requests and provides services       |
| Frontend        | User-facing part of an application             |
| Backend         | Server-side logic and data processing          |
| Static Website  | Mostly pre-built, fixed content                |
| Dynamic Website | Content generated or changed using logic/data  |
| Hosting         | Infrastructure that stores and serves websites |
| TCP             | Reliable, ordered transport                    |
| UDP             | Fast, connectionless transport                 |
| HTTP            | Web communication protocol                     |
| HTTPS           | HTTP secured with TLS                          |
| TLS             | Protocol that secures network communication    |
| Proxy           | Intermediary acting on behalf of clients       |
| Reverse Proxy   | Intermediary acting on behalf of servers       |
| VPN             | Encrypted connection to a VPN server           |

---

# 30. Key Takeaways

1. The **Internet** is the global network infrastructure that connects computers and devices.
2. The **Web** is a service that runs on the Internet and uses technologies such as HTTP/HTTPS.
3. **DNS** translates domain names into IP addresses.
4. **Routers** forward packets between networks.
5. **TCP** prioritizes reliable delivery, while **UDP** prioritizes speed and low latency.
6. **HTTP** defines communication between web clients and servers.
7. **HTTPS** adds TLS-based security to HTTP communication.
8. The **frontend** handles the user interface, while the **backend** handles server-side logic.
9. **Static websites** primarily serve pre-built content, while **dynamic websites** generate content based on logic or data.
10. **Hosting** makes websites and applications accessible over the Internet.
11. A **proxy** generally represents clients, while a **reverse proxy** generally represents backend servers.
12. A **VPN** encrypts the connection between your device and a VPN server and can change the public IP address visible to websites.
13. The Internet relies on many layers of technologies working together—from **DNS and IP addressing** to **routing, transport protocols, HTTP, and servers**.
