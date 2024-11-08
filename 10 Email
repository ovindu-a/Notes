# Electronic Mail and Messaging

### Author: Sunimal Rathnayake, Slides by Prof. Gihan Dias

---

## 1. Electronic Mail (E-Mail)
- **Purpose**: Used to send messages across the Internet or other connected networks.
- **Recipients**: Messages can be sent to one recipient, multiple recipients, or a mailing list.
- **Devices**: Computers, phones, PDAs, and other devices can send and receive messages.
- **E-mail Address**: A unique identifier for each mailbox (e.g., gihan@cse.mrt.ac.lk).

---

## 2. Why is E-Mail Popular?
- **Reach**: Enables communication with almost anyone.
- **Ease of Use**: User-friendly, accessible at the recipient’s convenience.
- **Cost**: Low-cost communication method.
- **Reliability**: Generally a reliable form of message delivery.
- **Speed**: Fast delivery, with messages stored for later reading.
- **Integration**: Works with paper-based systems and other applications.

---

## 3. E-Mail vs. Web
- **Web**: Mostly real-time, unidirectional, and multimedia.
- **E-mail**: Asynchronous, bi-directional, and multimedia-friendly.

---

## 4. Instant Messaging (IM)
- **Popular Platforms**: WhatsApp, Facebook Messenger, Viber.
- **Online Presence**: Both sender and recipient need to be online.
- **Features**: Text-based with image support, short messages, fast delivery, presence indicators.

### Web Forums
- Used by groups for communication (e.g., Google Groups, Facebook Groups).
- Accessed via login; messages can be read, replied to, and archived.

---

## 5. E-Mail Systems

### E-Mail Access Methods
- **Direct Login**: Directly logging into the server (text-based, less common now).
- **Client-Server Model**: Using an e-mail client (e.g., Outlook) to connect to a server.
- **Web-Based**: Accessing e-mail through a web browser (e.g., Gmail).

### Structure of an E-Mail System
- **Mail Client (User Agent)**: Used to compose, send, receive, and store messages.
- **Mail Server (MTA)**: Transfers e-mail across networks.
- **Message Store**: Stores messages for user access.

---

## 6. Mail User Agent (MUA)
- Also called a “mail reader.”
- **Functions**: Compose, edit, and read e-mails (e.g., Gmail, Outlook).
- **Connection**: Connects to servers for outgoing and incoming mail.

---

## 7. Mail Gateway (MTA)
- **Functions**: Receives, forwards, and stores e-mail for clients or other MTAs.
- **Features**: May scan for malware and spam, handle mailing lists.

---

## 8. Message Store
- **Purpose**: Holds incoming mail until accessed by the client.
- **Structure**: Can include inbox and other folders.

---

## 9. Sending E-Mail
- **Mail Gateway**: Client connects to a mail gateway (MTA) which does not need to know all recipients.
- **Submit Protocol**: Used to send mail; may require authentication and use TLS for security.
- **Domain Lookup**: Mail gateway uses DNS to find the destination server (MX records).
- **Scans**: Outgoing and incoming e-mails may be scanned for malware.

### Using a Firewall
- **Network Security**: Mail gateways and servers are often behind firewalls for protection.

---

## 10. Simple Mail Transfer Protocol (SMTP)
- **Description**: Simple text-based protocol for e-mail transfer.
- **Model**: Client-server model with command-response structure.
- **Commands**: Uses four-letter commands (e.g., `EHLO`, `MAIL`).
- **Responses**: Numeric responses followed by user information text.

### Sample SMTP Session

```
220 mail.mrt.ac.lk; ESMTP Sat, 7 Aug 2004 08:35:53 +0600
EHLO mail.mrt.ac.lk
250-mail.mrt.ac.lk Hello localhost.localdomain
250 HELP
MAIL From:gihan@mail.mrt.ac.lk
250 Sender ok
RCPT To:gihan@cse.mrt.ac.lk
250 Recipient ok
DATA
354 Enter message, end with “.”
[message content]
.
250 Message accepted for delivery
QUIT
221 Closing connection
```

---

## 11. Mailing Lists
- **Special Address**: Mailing list address managed by a list manager.
- **Function**: List manager sends copies of messages to all recipients.

---

## 12. Receiving E-Mail
- **Direct Server Access**: Users can access message store directly if logged in.
- **Mail Retrieval Protocols**:
  - **POP3**: Older protocol for downloading mail.
  - **IMAP**: Newer, allows server-stored folders and partial message retrieval.

---

## 13. Security in E-Mail
- **Challenges**: Includes spam, viruses, and forgery.
- **Secure Protocols**: Mail can be encrypted and signed (e.g., PGP, S/MIME).
- **Authentication Protocols**:
  - **Sender Policy Framework (SPF)**: DNS-based protocol to verify sending IP addresses.
  - **DomainKeys Identified Mail (DKIM)**: Uses cryptographic signatures for authenticity.

---

## 14. Format of an E-Mail Message
- **Structure**: Defined by RFC 822 with an envelope, headers, and body.
  - **Envelope**: Delivery information (sender, recipients).
  - **Headers**: Information about the message (From, To, Subject, Date).
  - **Body**: The main content of the message.
  - **Attachments**: Optional, added using MIME.

---

## 15. Multipurpose Internet Mail Extensions (MIME)
- **Purpose**: Allows non-text attachments in e-mails.
- **Headers**:
  - **MIME-Version**: Version indicator.
  - **Content-Type**: Type of data (e.g., text, image).
  - **Content-Transfer-Encoding**: Encoding method.
  - **Content-ID**: Identifier for specific content.
  - **Content-Description**: Description of the content.

### MIME Types
- **Text**: Plain, HTML.
- **Image**: JPEG, GIF.
- **Audio**: Basic, 32kadpcm.
- **Video**: MPEG, QuickTime.
- **Application**: Data requiring application processing (e.g., msword).

---

## 16. Messaging Overview
- **Purpose**: Enables text, images, and files to be sent between users or devices.
- **Common Platforms**: SMS, WhatsApp, Slack, etc.
- **Proprietary Systems**: Many systems (e.g., WhatsApp) require both sender and receiver to be on the same platform.

### eXtensible Messaging and Presence Protocol (XMPP)
- **Open Protocol**: Standardized protocol for messaging (XML-based).
- **Features**: Supports presence, attachments, groups.
- **Examples**: Used by WhatsApp, Google for messaging and IoT communication.

---

## 17. Conclusion
- E-mail and messaging remain vital communication tools, with security measures like SPF, DKIM, and encryption enhancing their reliability.