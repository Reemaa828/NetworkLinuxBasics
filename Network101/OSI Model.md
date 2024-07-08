
# What's an OSI Model? 
Open System Interconnection model: is a theoretical model made so different computing devices can communicate with each other efficiently made by the ISO.
It's also a:
- **Universal Language:** Breaks down network communication into 7 layers, ensuring all devices speak the same networking language
- **Troubleshooting Tool:** Helps isolate the source of network problems by pinpointing the specific layer where the issue occurs.

# 7 Layers of OSI Model ℹ️

| Layer | OSI model layer    | Protocols                                                                         | Devices             | Protocol data unit |
| ----- | ------------------ | --------------------------------------------------------------------------------- | ------------------- | ------------------ |
| 1     | Application Layer  | HTTPS, HTTP, SMTP, FTP                                                            | -                   | Data               |
| 2     | Presentation Layer | TLS(SSL)                                                                          | -                   | Data               |
| 3     | Session Layer      | -                                                                                 | -                   | Data               |
| 4     | Transport Layer    | TCP (connection oriented), UDP (connectionless oriented)                          | -                   | Segments           |
| 5     | Network Layer      | IP                                                                                | Hub, Switch, Router | Packets            |
| 6     | Data Link Layer    | MAC                                                                               | -                   | Frame              |
| 7     | Physical Layer     | Electrical signal (copper wire), Light signal (optical fibre), Radio signal (air) | Ethernet, WAP, NIC, | Bits               |

## 1️⃣ Application Layer 

![[Pasted image 20240708054835.png]]

Application Layer doesn't mean the programs or network applications but it means the Protocols that make these network applications work on the network correctly.
the network applications depends on application layer protocols to function.
so application layer provides network services for network application with the help of protocols to perform user activities.
**Protocols used:**

- HTTPS/HTTP : web surfing.
- FTP: downloading files.
- SMTP: emails.
- Telnet: virtual terminals.

## 2️⃣ Presentation Layer
![[Pasted image 20240708061443.png]]


It performs mainly data translation, encryption & decryption, and compression in the network. On the sender’s side, it receives the data from the applying layer and performs data encryption and compression to it. At the receiver’s end, it receives the data from the transport layer and performs data translation, decryption, and uncompresses data.

**Protocols used:**

- SSL: secure socket layer for encryption and decryption.

## 3️⃣ Session Layer

![[Pasted image 20240708063900.png]]

- The session Layer is responsible for opening and closing communication between two devices, the session layer ensures that session is opened long enough until all data is being transferred. 

- The session layer also performs authentication and authorization for establishing a safe connection in the network.

- The session layer can also sets checkpoints when data is being transferred; the session sees the data; if the data got interrupted the device can resume from the last checkpoint and will not start from scratch.

The main tasks of session layer:
- session management
- authentication
- authorization
- download files in data packets

## 4️⃣ Transport Layer

